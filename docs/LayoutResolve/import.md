---
sidebar_position: 1
---

# Importing Layouts to CanalNET
[Back to Home](../index.md#wellcome)

 
First step is to import the drawing elements reresenting the canal routes to the CanalNET environment. There are different ways to achieve this.

> **Tip:** AutoCAD drawings are often plagued with duplicate elements, resulting in errors later. Use **Overkill** command to clear any such duplicate objects, before importing to CanalNET.


1. To import a individual routes - i.e., a single route or multiple routes at a time - Go to `Workspace > Pick Route (AutoCAD)` .
   
   ![Import individual routes](Images/Image%20005.png)

   ![Import individual routes dialog](Images/Image%20066.png)

2. To import alignment routes drawn on a layer, go to Workflow > Pick Routes (AutoCAD Layer). This will invoke a dialog listing all the layers in the current drawing. 

   ![Pick host object](Images/Image%20006.png)
   
   ![Pick routes from layer](Images/Image%20007.png)
   
   Pick the desired layer, and hit OK. This will import all alignment routes found on the specified layer to the plan view area.
   
   Note: This method is recommended for drawings whose layers are well organized, especially for the different levels of canals expected in the project.

3. One can also import a collection of canal routes at once. To do this:
   
   * First, create an instance of all canal routes (of similar generation) on a host object with in the AutoCAD environment, using the AutoCAD addon tool.
   
   * Then go to `Workspace > Pick Rotue (AutoCAD)` menu command, and when prompted pick the host object.
     
   This will import all the canal routes instanced in the host object. 
     
    

> Note: A complete canal route data consists an alignment data (x, y) and a profile data. The ***Partial Data Routes*** indicated in below figure may apear when importing canal routes whose profile data is not yet ready. Such routes are represented with broken lines in the plan veiw area of the interface.

![Partial Data Routes](Images/Image%20010.png) 

*Routes in plan view area showing canal routes with complete data set, and partial data set.*

> **Remember**, routes that are NOT drawn as polyline, and whose length is less than 20M will be filtered out during the import process.

## Saving Networks
[Back to Top](#)

It sounds to early to save the work. But it is better to open a saved network, rather than import a network as new.

Follow the steps on [Saving Network Data](../FileManagement/FileManagement.md#saving-workspace-data).



## Removing Unwanted Routes
[Back to Top](#)

Unwanted polyline objects may be imported to CanalNET environment during the process of importing canals. Also, the user may want to remove a canal route and re-import it again. To remove such objects:

1. Select the objects to remove in the layout view (plan view) area. If needed, enable multi-select from` Edit > Multi Select (Routes)` to allow selection of multiple routes at a time.

2. Use `Edit > Remove Route` menu command. Alternatively, press the `Delete` key.
   
   ![Remove Route](Images/Image%20008.png)

   ![Delete dialog requesting confirmation for selected routes.](Images/Image%20011.png) 

   *Delete dialog requesting confirmation for selected routes.*

Once satisied with the import process, the next step is Node Identification.

## Clearing Workspace Contents

To clean the workspace contents of CanalNET software, and start over:

1. Start the menu command `Worlspace > Clear Workspace Contents...`. 

   ![](Images/Image%20072.png)

2. Confirm to the dialog, by selecting `All` button.

   ![](Images/Image%20073.png)

   > **Note:** The `Purge` button allows to remove any *invalid* node that does not have all the required data fields. Such issues may be rare. It is possible to clear only node elements by choosing `Nodes`. 

[Back to Top](#)