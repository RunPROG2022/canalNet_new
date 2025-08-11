

# Creating and Editing Axes in AutoCAD
[Back to Home](../index.md#wellcome)

Often times one may need to create axes and edit the information displayed depending on the data ploted. 

   ![]( Images/Image%2040.png"

### Create a new axes
[Back to Top](#)

1. Start the menu command from `Explore Outputs > Plot to AutoCAD > Create Axes`. 

2. In AutoCAD, pick the object defining the bounding box for the axes area.

3. The variable editor dialog appears. Set axis limits for Abscisa and Ordinate as desired.
   
   <   ![]( Images/Image%2041.png)
   
   WCS data: Uses the AutoCAD World Coordinate System the object is located to create an axis. This will enlarge the BBox a little to set starting and ending positions.
   
   Ref Data: Use this if the object selected for the bounding box is referenced to a an existing axes pair. All objects (except Host objects) created by iCAD and CanalNETWORK are by default referenced to an accompanying axes.
   
   User: This option lets users define their own start and end for both vertical and horizontal axis.
   
   Note: The value sets are START, STEP, END.
   
  ![](Images/Image%2042.png)
   
   



### Editing Axis
[Back to Top](#)

Used to change the appearance and orientation of axis labels, use below steps.

1. Start the menu `Workflow > Plot to AutoCAD > Edit Axis...` 

2. In the dialog, ckick on the first row second column cell, and pick the axis to edit in AutoCAD.
   
   ![](Images/Image%2044.png)
   

3. The dialog box populates the values of the current setting in the box. Edit as desired.
   
   - Axis Limits: START, STEP, END (step is not always applied and depends on the size of the axis)
   
   - Label Position:
     
     - [1, 0] Left: put labels on left side, (refernce counterclockwise to the box), 
     
     - [1, 1] Left Rotated: as above, but rotated to 90deg.
     
     - [-1, 0] Right: put labels on right side, (refernce conterclockwise to the box)
     
     - [-1, 1] Right Rotated: same as above, but rotated to 90deg
   
   - Label number format: specify how many decimals to use for axis labels.
     
     NB: It is not recommended to change below data, especially for axis contaning referened plots.
   
   - Data Scale: Input if specific scaling is required for the axis.
   
   - Text Height: Leave the maximum number to allow automatic sizing of texts. 



Upon completion, the axis will be redrawn in AutoCAD with the new changes.


[Back to Top](#)