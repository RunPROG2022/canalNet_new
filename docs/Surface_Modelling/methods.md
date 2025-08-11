---
sidebar_position: 2
---

# Key Concepts on Topographic Data Use
[Back to Home](../index.md#wellcome)

In this section, the basis for topographic data processing as a geometric surface are presented, along with the considerations used to work on alignments for proile extraction. The topics covered include:

- Surface interpolation
- Data Query
- Extrapolation
- Curves on alignments
- Other considerations on Alignments


## Surface Interpolant
[Back to Top](#)

Surface fitting and interpolation, as applied in the context of topographic data processing in iCAD and CanalNETWORK products, specifically refers to the use of scattered data of the form x, y, z triplet to determine a representative surface model of the form z= F(x,y) and using this surface model to generate elevation (z) values at arbitrary x, y locations. This means, data from typical surveying work or other sources that is available in x, y, z format can be used to reach at the desired surface model, and undertake subsequent tasks.

To estimate the surface model for a given set of x,y,z data, iCAD builds on scattered interpolation algorithm in matlab. This algorithm performs Delauney triangulation over the data set, with the aim of creating a surface fit made up of small triangles. A Delaunay Triangulation maximizes  the smallest occuring triangle over all triangulations og the point set. In other words, any other triangulation will have a smaller angle at vertices.

![d](Images/2.png)

It is important to note that the method:

- assumes a perfect plane inside each triangle, and 

- the elevation at any point inside or on the edge of each triangle is calaculated using linear interpolation

## Query on Topograhic Data
[Back to Top](#)

Once the surface interpolant is determined, elevation at querry points of x, y is detemined from the same, using the following relation ship.

z= F(x, y)

where

F= f(x,y,z) is the surface interpolant.

The surface data extraction algorithm in iCAD and CanalNETWORK software products is applied at least in the following functions:

- Point  Query: This function is used to interactively querry elevation data from x,y input obtained from the AutoCAD environment. The function reads the x, y (or E, N) data from user selection in AutoCAD, and displays the elevation value calculated from z= F(x,y)

- Profile Extraction: The fundamental input to profile extraction is an alignment path object defined in AutoCAD environment. This object provides the  x, y data at fixed intervals along the path object. The same function is applied on x,y data set to return corresponding elevation values. 
  
  ![[  ] ](Images/Image%2040.png)
  
  *Fig: Alignmnet route, vertices and querry points showing for an alignment route with and without offset querry points.*
  
  When extracting strip elevation data for an alignment object, normal lines are generated at fixed intervals. In addition to x,y data at center line - i.e., on the alignment route - other x,y data are created at offset locations specified by the user along these normal lines. The offset locations are applied on both sides of the alignmnet. The resulting x,y data set forms a strip area along the alignment route. The elevation data at this data set is calculated from z= f(x,y).
  
![Alignment Offsets Diagram](./Images/Image%2041.png)
 
  
  *Schematic showing Alignment route, and offset querry points consideration. Offsets are read from Left to Right, facing in the direction of progress of the alignment route.*

    Note: The intervals for extracting profile data are specified by the user. The algorithm includes vertex points along the alignmnet route object, but the user has the option to exclude these points during the extraction process.

- Profile Reload tools: Sometimes engineers want to modify alignment routes to meet some design requirements. This is naturally handled with in the AutoCAD environment. In such cases, both iCAD and CanalNETWORK products offer a function that allows reloading profile data for an alignmnet object whose vertices are modified. Reload functions essentially repeat the profile extraction steps described above using  settings used to create the original profile data.

## Extrapolation
[Back to Top](#)

The implementation of the surface interpolant function in above described querry methods of either iCAD or CanalNETWORK product, allows extrapolation to determine elevation data ouside the area covered by input x,y data set. This meanse, the implementation can estimate elevation values for points outside the boundary area defined by the inpit data set. 

![Extrapolation Schematic](./Images/Fig2.jpg)


*Schematic showing point data set, boundary area defined by the data set, and querry points for extrapolaiton.*

It is important to note that:

- The returned values are derived from linear extrapolation

- the reliability of the values returned decreases significantly as the querry points move away from the boundary area, original data set. 

Hence, the extrapolation capability is to be considered as only a complimentary feature to obtain a crude estimate of terrain variation beyond the boundary area. There is no guarantee that designs based on extrapolated data will be of acceptable quality and accuracy.

## Curve Handling During profile extraction
[Back to Top](#)

Curves, if found in the AutoCAD alignment object, will be considered while extracting prorfile data. The requirements for succesful data extraction are:

- the begining and ending segments of the alignment route must be straight segments of at least longer than the incremental distance for profile extraction. This is set to 20meters by default.

- Curve radius(R), the curve length (L), and the chord length (Lc) are all greater than or equal to 20meters

- The backward tangent and forward tongent lines to the curve begining and ending, respectively, align with the preceeding and following segments with in acceptable error.

> Note that these are limitations set to ensure practicality of designs, as curves of a smaller size are not encouraged in practice. If all the conditions are not met, no curve data will be extracted. 

Route curvatures meeting all these requirements are succesfully extracted as curves. The data will contain curve data listing the key parameters including:

- curve begining point, PC

- Curve tangent point, PT

- Tangent Intersection point, PI

- Curve Median point, PM

- Curve Center location, PC.

The schematic below shows detailed curve information extracted.

![Curve Details](./Images/Image%20curve2.png)

![CAD Curve Example](./Images/cadCurve.png)


The following sample route geometry shows the validity of curves for profile extraction.

![Route Geometry Sample](./Images/Image%20008.png)


There are seven curves on the route, including the compound curve near station 500. The table report states that 3 out of 7 curves are extracted.

![Curve Report](./Images/Image%2031.png)


![Curve Data Analysis](./Images/Image%2033.png)




Curve 1 is discarded, because curves at the begining and end do not mee tangency requirements.

Curve 3 of radius 15 units is discarded, becasue its radius is less than the minimum treshold of 20m.

Curve 4 is discarded because the calculated radius of 55.34 is not similar to that found from tangency requirements of 150m.

Curve 5 and 6 are compound curves, discarded because tangency requirements are not met for either curve.

However, the data is collected at the specified incremental station to the last end.

For the same route, removing the last vertex, will cause a curve to be at the last segment. This results in two issues: (a) reduced length of the alignment route, and (b) miscalculated Point of Tangency. To avoid such issues, always ensure there is a stratight segment at the end of every alignment routes.

![Modified Alignment](./Images/Image%2035.png)


![Curve Analysis Results](./Images/Image%2038.png)


## Notes about Alignments
[Back to Top](#)

The profile extraction process relies on a number of assumptions to execute the above mentioed tasks. Observing the following conventions and assumptions will help to avoid failed attempts, and hence save time. 

**Flow direction**: Profile extraction process is designed to work from the begining vertex of the alignment object towards the its end vertex, when extracting elevations at incremental locations. This is based on the key convention stating, 'alignments are drawn from upstream to downstream direction.' All preceeding and subsequent tasks to profile extraction build on this convention. It is therefore mandatory to work accordingly, to avoid mulitple invonveniences as the design task progresses.

**Scaling of routes**: Canal routes are required to be referenced to a pair of axes generated by iCAD product. Generally, this referencing is not limited in any way. That is to say, the user can adopt any prefered scalling for the referencing to work. However, when applied to canal routes, the scaling used may impact the quality - or even success  - of profile extraction. It is recommended to strictly adhere to a scaling of 1:1 or larger (e.g., 2:1) when prepating layout plans for use with CanalNETWORK software.

A known issue exists where profile extraction process fails or returns poor quality data, when a small scale (like 1000:1) is used to draw and reference alignment routes.

**Incremental lengths**: iIncremental length is input for every profile extraction task. Often this is kept at 20m interval. iCAD and CanalNETWORK products can process and use profile data extraction at finer intervals of upto 2.5 meters. This can be helpful when precise design - and hence even more accurate BoQ estimates - are required. However, reducing the incremental distance, can imply heavier computational cost during design process. This is simply because there will be more station points to process for every route at all stages of design, and production (for Lsec, Plan, xsec etc). 

The optimal incremental distance to be used shall depend on the project scale/type, available DEM data resolution, expected variabilities of terrain, as well as the anticipated canal size. We recommend to limit minimum incremental distance to 10meters.

**Curve data limitations:** The size of curves that can be read in to alignment profile data, as seen above, is limited by design for iCAD and CanalNETWORK products. Irrigation canals are, by practice, expected to meet some general principles of practice. The software products attempt to implemtn a pragramatic approach towards filtering curves provided by the user in the original AutoCAD drawing. As mentioned above, the smallest allowable curve radius and length, are limited to 15 and 20 meters, respectively. We anticipate that provissions below these limits are not practical, and hence are automatically filtered out during the extraction process.


[Back to Top](#)

