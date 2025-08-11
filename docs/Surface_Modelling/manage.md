---
sidebar_position: 1
---

# Managing Topo Data in CanalNET
[Back to Home](../index.md#1-wellcome)


## Hosting Surface Data
[Back to Top](#)

Before using topographic data in CanalNET, the data must be hosted on an AutoCAD object. Once hosted, the data is always accessible for loading in to CanalNET workspace. 



1. First, prepare a host object in AutoCAD that will host the data. Draw a simple polyline object, or a rectangle.
   
   ![](Images/Image%20010.png)

   > **Tip:** CanalNET can host and retrive data on AutoCAD objects. This does not affect other workflows while using AutoCAD/Civil 3D in any way.

2. Start the menu command `Workspace > Surface Data > Host Data` menu command.

   ![](Images/Image%20005.png)

   
3. In the import dialog, pick the source data file.

   ![](Images/Image%20050.png)

4. Accept the default settings, and hit `Next`. Then hit `Finish` to accept the data. 


   ![](Images/Image%20051.png)

   ![](Images/Image%20052.png)

   >**Important Note:** Make sure your data appears with three variable names in the left column as shown above. If not, your data will cause errors at a latter stage.

5. AutoCAD is now in select mode. Pick the object prepared earlier.
   ![](Images/Image%20053.png)

6. When prompted, provide a tag string to the object.

   ![](Images/Image%20054.png)
   
   **Tip:** Tag Strings are used to easily identify objects in AutoCAD while in use with CanalNET.

   The data is hosted, and confirmation obtained as shown below. The shape of the object also changes to correspond to one of available sketches for surface data.

   ![](Images/Image%20055.png)

## Check Hosted Data on Objects
[Back to Top](#)

The presence and content of the data set hosted on an AutoCAD object can be viewed as follows:

1. Start the `Workspace > Surface Data > View Hosted Data` menu command. 

   ![](Images/Image%20056.png)

2. If you get the following prompt, close the dialog and start the `Workspace > Invoke AutoCAD Addons` menu command to establish the desired link with the current AutoCAD file.

   ![](Images/Image%20049.png)

   Then, start the command in step 1 above.

3. AutoCAD should be in select mode. PIck the object desired whose data content is needed. The data is displayed in the table viewer interface.

   ![](Images/Image%20057.png)


   >**Tip:** *Copy Table* button can be used to copy the contents of the table to Windows Clipboard, and to use it in other applications (e.g., MS Excel, MS Word...) for reporting or further analysis.

## Loading Surface Data.
[Back to Top](#)

Before using topographic suruface data for analysis in CanalNET, the data must be available to the workspace. This can be achieved as follows:

1. Start the menu command `Workspace > Surface Data > Load Hosted Data`. This will put AutoCAD in select mode.

   ![](Images/Image%20004.png)

2. In AUtoCAD, pick the desired object. 

   ![](Images/Image%20060.png)
   
3. The data is loaded to the workspace. This can be confirmed by the **Thick Mark** besides the `Load Hosted Data` menu item, as shown below.
    
    ![](Images/Image%20061.png)
   

At this stage, the data is available in the workspace, and one can proceed with profile extraction or 3D inquiry tasks as needed.

## Clearing Loaded Topographic Data
[Back to Top](#)

If needed, data clearing can be done at any time. 
- Start `Workspace > Surface Data > Load Hosted Data` menu commnad. If there is an existing data the following dialog appears.
![](Images/Image%20063.png)
- Choose `Clear`, and the data will be cleared. The thickmark indicator on the menu is also removed.
  
[Back to Top](#)

