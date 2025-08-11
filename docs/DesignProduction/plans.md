# Generating Plan Views
[Back to Home](../index.md#wellcome)

Plan view is a key product in the design workflow. It presents detailed alignment and embankement information, along with locations for various structures and station markers along the route. Plan views are also used to provide a view of parallely running canal routes, to refine any constructabilty issues.

![imageIntro](images/Image%20092.png)

### Generating Full Length Plans
[Back to Top](#)

To succesfuly generate plan views for a given route, the profile data must be fully updated. To do this, while the route is selected in plan view:

1. Clear any selection in Profile View area

2. go to `Explore Solutions > Table Data > LSec Profile Data`. This will update the profile data for the route.

Then, you can start plan view generation. There are two steps to generate plan view:

1. Create the plan view data from `Explore Solutions > Plan View (Current Route)` . 
   
   ![fig5](Images/Image%20108.png)
   
   This will automatically start creating the data. However, if there is an existing data, you will be promoted with the *Re-extract Trail?* dialog. 
   
   ![fig6](Images/Image%20109.png)
   
   Choose `Update` if there are any changes to CBL information, otherwise choose `Use Current`.

2. Next the *Edit Variables* dialog is open, allowing to set specifications for creating the plan drawing.
   
   ![fig](Images/Image%20110.png)
   
   <u>OnApply</u>: Save option simply saves the settings. Generate Drawing option creates the drawing per the table of specification. Use the `Save` option.
   
   <u>Contour Intervals</u>: the inverval value to be used to generate contour lines with the plan view. a value of \< 0.5 indicates, no contour is needed. Default is set to 0.
   
   <u>Length of Control Markers</u>: The length of control markers on the plan view. This will also determine the length of station/curve markers.
   
   Note: Providing 0 value supresses all markers. Providing too large a value could result in curve markers crossing each other, giving poor presentation quality. Recommended values are:
   
   - Large canals 20-40units
   
   - small canals 5-10 units
   
   <u>Lateral Exageration Scale</u>: Often canal layouts appear as narrow and to conjusted, making it difficult to view details and poor presentation. To aid this, an exageration scale can be set between 1 to 10. Usually, 3 to 5 gives good drawings.
   
   Note: When exageration scale is applied, the distance normal to the route center line is multiplied by the specified scale factor. True ground distance is obtained by dividing the measuered distance in AutoCAD environment to the product of this scale value and that of the plot scale.
   
   Note: too large exageration values may distort true appearance of the layout components on edge, and RoW markers, as well as on contour lines - especially on curve locations.
   
   Note: On posed plan view generation (generating plans of adjacent routes) the exageration scale is set to 1.0.
   
   <u>Control Markers and Drop Markers Direction:</u> The direction of marker lines with respect to the centerline of the alignment route.
   
   <u>Station Range:</u> The range of values to generate plan view for. These are automatically rounded to the nearest available value on the station date list.
   
   <u>Show Route Geometry</u>: control the visibility of route center line, and all curve and control markers.
   
   <u>Fit BBox</u>: Set to None, the plan view is generated in natural North UP orientation. When set to *Pick AutoCAD*, the user is prompted to pick a bounding object in AutoCAD. The drawing creation attempts to automatically determine the best orientation and scaling for the drawing to fit in to the selected area.
   
   Tip: Upon creating the drawing to AutoCAD the exageration scale is exported along with the north symbol. Use the `Aligned Annotation` addon tool to generate this info.
   
   Upon hitting `Apply`, the settings are saved, and the command exits.

3. To create a plan view from the updated data just created above, make sure selection in profile view is cleared, and go to `Explore Solutions > Plan View (Contd).` This will invoke the variable editor again, allowiing to revise any settings. 
   
   ![fig2](Images/Image%20112.png)
   
   Note the *Station Range* values are set to the default values of start to end of the route. You can input a valid range, and hit apply. The plan view is generated as shown below. A table data describing the setting out detail for the route of the specified station range is also included.
   
   ![a](Images/Image%20113.png)
   
   Note: To create full length plans, leave station range to default values, or seleect full range from the drop down menu.

4. To exit from plan view, right click on *Plan View Area* and choose `Refresh Nodes and Routes` option. This will clear the plan drawing, and repoulate route and node information.

### Generating plan views for a selected segement
[Back to Top](#)

One can quickly create a plan view for a segment of the route profile as follows:

1. Select a segment in the profile view area.

2. start the command `Explore Solutions > Plot to AutoCAD > Plan View (Contd)` or use Ctrl+W short cut. The plan fof the selcted segment is generated.

This step is particularly helpful when making modifications to the CBL of a segment, and an updated plan view is needed to see the change. Simply start the profile data update command (Ctrl+L) and request the plan view (Ctrl+W). This saves significant time, especially when working on very long canals where the drawing creation time is relatively longer. 

### Generating plan view for user defined station range
[Back to Top](#)

One can also create plan views from an interactively selected window. To use this method:

1. Select any node in profile view area.

2. Start the command Ctrl+W. An cursor waits for user input. Click and drag to create the rectangle that represents the desired range of plan view generation. Release when done. 
   
   ![figInter](Images/Image%20114.png)

3. If the range selected specifies a length less than 100meters, the command exits after blinking the rectangle. Otherwise, the plan view is created for the desired range.




## Known Limitations and Issues
[Back to Top](#)

Below is a list of observed limitations that users can expect.

1. Berm Provissions on Drop locations: Plan views do not show how terrain changes along side a canal drop.

[Back to Top](#)