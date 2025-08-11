# AutoCAD Edit or Create Alignment Markers
[Back to Home](../index.md#1-wellcome)]

To create markers along an alignment use below steps:

1. Start the menu `Workflow > Plot to AutoCAD > Edit/Create Alignment Marker`. AutoCAD will be ready in select mode, promoting *Pick Alignment object to Mark:* 
   
      ![](Images/Image%2051.png)

2. Pick the object for marking. If the object is not referenced, a dialog will apear to confirm the process. Accept and continue. If not, it will continue. 
   
      ![](Images/Image%20124.png)


3. If the Alignment has longitudinal informaiton, it will continue to step 4. If not,  a dialog will apear to confirm. Accept `Set New`. Input the deisred starting station for the object.
   
   ![fig](Images/Image%20125.png)
   
   ![fig](Images/Image%20126.png)
   
   Markers are created using default settings.
   
   ![fig](Images/Image%20128.png)
   
   Start the command again, and select the marked alignment to edit the specification for the markers.
   
   

4. Upon selection of a marked object, the below dialog appears to change how the markers are displayed.
   
   ![fig](Images/Image%20127.png)
   
   - Begining Station: Starting marker value. 
   
   - Ending Station: Ending marker value. 
   
   - Marker spacing: Minor and Major Steps for marking the alignment. Major marker locations bear text information, while minor marker locaitons are drawn as simple ticks.
   
   - Text Format: [A.B notation] A represents the location of + sign on station markers, and B represents the number of decimal places to use when generating station tetxts. For example, for station value of 12345.3456:
     
     - 3.0 will give 12+345
     
     - 3.2 will give 12+345.34
     
     - 0.3 will give 12345.345
   
   - Text Orientation: Parallel orientation rotates anotation texts parallel to the alignemnt object, while Perpendicular rotates them to appear normal to the alignment.
   
   - Text Position: Specified whethter text is to be put to the right or to the left of the alignment object.
   
   - Skip Beg/End markers. If editing markers on plan views, the end markers are automatically generated and need not change. Use this option to skip affecting them.
   
   Partial stations can be marked by specifing statting and ending stations accordingly. For the above example, using 300, 900) will work out as below.
   
   ![Img](Images/Image%2052.png)
   
   [Back to Top](#)


