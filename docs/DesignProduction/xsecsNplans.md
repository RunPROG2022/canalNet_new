# Exploring Sections and Plans to AutoCAD
[Back to Home](../index.md#wellcome)

You can explore sections in plan view in one of two ways. Start the Cross-Sections command from `XSEC` button, and click on a vertical section bar (solid, not dotted) created in profile view. An interactive vertical bar is created that allows you to pick a section. As you hover in the profile view, a red start marker is shown in plan view, pointing to the exact location of the selected station. Upon click, the section for that station is generated.

> Note: This tool also works with any of the annotation markers and drop positioning tools. 

![image9](Images/Image%20115.png)

You can also create a data tip in plan view along the centerline of the route, and use `Ctrl+G` key short cut. This will start a dialog confirming the station. Hit `Ok` to create the section.

![image](Images/Image%20116.png)

> Note: Station information on Data Tips of plan view are re-calculated based on rendered geometery, and may not always be precise to actual stations used to create the cross-section view.

### Creating Extended Plan Views
[Back to Top](#)

You can generate plan views of two parallelly running canals at the same time, to see any overlap issues or to confirm if adeuate space is maintained between the two. To do this:

1. First, click on the larger canal route which whose plan is needed, and pose it using `Explore Solutions > Plot Extended XSection` menu command. This will invoke the dialog shown. Accept to confirm.
   
   ![figu](Images/Image%20117.png)
   
   If you go back to the menu, you will notice that the menu is Checked with the name and ID of posed route.
   
   ![imageu](Images/Image%20118.png)

2. Then go to plan view, and click on the other canal route running close to posed canal above and parallel to it. Use one of the above methods to specifiy a plot range for the plan view. The plan view is created for the specified range for both routes.
   
   ![imageuuu](Images/Image%20119.png)
   
   Note: The range for the posed canal is estimated automatically. No need for the user to input this value.

You can use explore methods mentioned above to visualize and interact in all three view areas.

![imagett](Images/Image%20120.png)

Note the following points when using this method:

- Both routes should be uptodate for profile data and plan view data for a succesful plan view creation.

- Exageration scales are set to 1.00.

- Contrours may or may not be created depending on the plan view creation settings of both routes.

- Contours, if created, can not be plotted, because there are two instances of the same data type on plan view.



### Automatic Exporting of plan view
[Back to Top](#)

The quickest way to generate plan views to AutoCAD is shown below.

1. Start command from `Explore Outputs > Plan Views > Plan View (Contd)`. In the dialog, set all paramenters as desired, and makesure to choose *Pick AutoCAD* for Fit to BBox parameter. Hit Apply.

2. Work will start but not complete. Go to AutoCAD, and Pick the BBox for plan view. You can choose the same object, or a differnet one. The plan view is now generated rotated and scaled per the original BBox.
   
   
   
   ![fdsf](Images/Image%2053.png)
   
   

3. Plot this directly from `workflow > Plot to AutoCAD > Plot Plan to AutoCAD`. In AutoCAD select the BBox again. The complete drawing is generated. 

Notes on Colors:

- color standards for producing drawings can be specified in `Workspace > Preferences`. 

- All drawing elements are generated per set color standard.

- Axis and their labels, alignment markers and annotations, plan view slope lines and other text information are generated using the currently selected layer, and color in AutoCAD.

- Annotations and objects are exported to AutoCAD in groups, and its easy to edit them for color or other details.
  
  

### Manual Exporting plan view or their components to AutoCAD
[Back to Top](#)

1. To generate the drawings to AutoCAD, use the standard tool from `Workflow > Render To AutoCAD` or `Ctrl + P`,  The first step would be to copy the axes information to the region of plot in AutoCAD, hence choose *Copy BBox*. 
   
   ![[  ]](Images/Image%20010.png) 
   
   Then selct Plot to BBox (AutoCAD) option, and upon prompt in AutoCAD, pick the object that defines the drawing area. 
   
   ![[  ]](Images/Image%20011.png) 
   
   On On the `uiPlotOption`s dialog box, choose:
   
   a) ALL: if the plan view is generated using a fit area (as shown in the second figure above)
   
   b) specify a plot scale, otherwise.
   
   ![[  ] ](Images/Image%20012.png)
   
   *Choose Plot scaling depending on the type of plan view drawing desired*
   
   ![[  ]](Images/Image%20013.png) *Axis reference information created to AutoCAD environment*
   
   Once the axis information is created in AutoCAD, along with a referenced starting object, use `Workflow > Render to AutoCAD`, select all objects, and click `Apply`. Upon prompt, choose the referenced object, and follow the dialogs to complete generating all groups of objects to AutoCAD.
   
   ![[  ] ](Images/Image%20014.png)
   
   *Use Select All button to choose all groups of objects.*
   
   ![[  ] ](Images/Image%20015.png)
   
   *Fig AutoCAD drawing, after few edits on line colors, and text annotation creation.*
   
   If only certain components of the drawing are needed, select those only, and continue. The desired elements are added to the drawing.


[Back to Top](#)