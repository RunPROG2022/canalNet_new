---
sidebar_position: 3
---

# 3. Output Files and Management
[Back to Home](../index.md#wellcome)

In previouse sections, the input data requirements and soruces are described for use in CanalNET software. Here, data output types, storage and retrival are discussed.

## Data Storage
[Back to Top](#)
CanalNET operates side by side with AutoCAD. Specifically, CanalNET creates data for AutoCAD objects, and retrives them using AutoCAD objects. This meanse, each AutoCAD project file will have its dedicated data source file for use with CanalNET tasks and processes.


There are three kinds of files that can be created by CanalNET (or iCAD).

- Regular files (.xsd)
  Regular working files are normally used to store data from CanalNET and its various processes. These files has ""excactly the same name** as the autocad project file used to create them, except their extension is .xsd.

  > **Important Note:** Do not rename regular working files, or data inside the file will not be accessible by CanalNET. If a must, change the names of both the AutoCAD file and the data file. 

- Temprary files (.lsd)
  Temporary files are created upon executing key workflows in CanalNET. These are safeguard copies of the regular data file containing new data that is NOT YET saved to the regular working file. They can be used to backup previous works (e.g, when power outage causes sudden application closure with out saving)

- Backup files (.xsd) 
  Backup files are created by the user at any point of the project development phase, and can be restored when needed. They represent (compressed) copies of the regular working files used in the project.


> **Important Note:** These files can not be opened by CanalNET using double click or drag-n-drop methods. CanalNET only needs to access the data stored, through an open AutoCAD project file.


> **Tip:**It is acceptable to use both CanalNET and iCAD on a single AutoCAD file. But it is highly recommended to avoid using them simultaneously.


The data files created by CanalNET can be viewed by using the menu command `Workflow > File Utilities > Open File Location` menu command.

    ![](Images/Image%2001.png)

    Notice, the .xsd, .lsd files in the folder corresponding to an open AutoCAD project file.

## Saving Workspace Data
[Back to Top](#)

While working in CanalNET, data can be saved as follows.

> **Note:** Data is saved to (or through) AutoCAD objects, and not directly to a file.

1. FIrst, prepare a host object in AutoCAD that will be used to save the data. This can be a simple box or a polyline object.
   
   ![](Images/Image%2011.png)

2. Start the commend from `Workspace > Save Network`. Then confirm on `Go to AutoCAD` button.
   
   ![](Images/Image%2010.png)

3. In AutoCAD, pick the retangle object prepared in step 1 above. Provide a tag for the object as shown below.
   
   ![](Images/Image%2012.png)

   >**Important Note:** Tag texts must be more than 6 characters long, can only be alphanumeric characters, and can not contain spaces. They can use underscpre character.

4. The data is saved to the object, and confirmed with the dialog.
   
   ![](Images/Image%2013.png)

  Note, the shape of the host object changes to the standard sketch designated for network data as shown above.

## Opening a Saved Network Data
[Back to Top](#)

To open a saved network data

1. If not already, open the AutoCAD project file and make sure the host object pointing to the stored network data is visible.

2. Clear contents of CanalNET workspace from `Workspace > Clear Workspace Contents` or `Ctrl`+`0`. Confirm by hitting `All`.
   
   ![](Images/Image%2014.png)

   This will empty any data on the workspace.
   
3. Start the command `Workspace > Load Network`. AutoCAD will be in select mode, promoting to *Pick a Network Host Object...*.
4. Pick on the host object, and the contents are read in to CanalNET workspace.
  
    ![](Images/Image%2015.png)

[Back to Top](#)



## Creating Backup Data
[Back to Top](#)

Backup files can be creatd easily at any time. To create, 

1. Start the command `Workspace > File Utilties > Backup Data File ...`.
   
   ![](Images/Image%2002.png)

2. On the prompt, choose   `Yes` and the explorer window appears with a suggested name for the backup file.

    ![](Images/Image%2003.png)

    > **Note:** The suggested name contains the data and month of the day be default, but can be changed to any desired value or identifier the user chooses.

3. Upon completion, the confirmation dialog appears. Click `Ok` to exit.

    ![](Images/Image%2004.png)

## Restoring Backup data
[Back to Top](#)

Restoring a backup data to CanalNET workspace is done as follows:

1. Start `Workflow > FIle Utilities > Restore Backup...`. This opens the explorer dialog.
   
   ![](Images/Image%2005.png)

2. Choose the desired backup data source, and click `Open`.
   
   ![](Images/Image%2006.png)

3. The confirmation dialog appears with a success report to complete the process.

Both the CanalNET workspace and the regular working file (.xsd) have now an updated copy of the data file.


[Back to Top](#)

