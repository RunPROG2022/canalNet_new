---
sidebar_position: 1
---

# Profile Extraction

The first step in longitudinal or vertical design is to create profile data for canal routes in the network. This is easily achieved by the methods and procedures described here.

CanalNET automatically creates profile data for canal routes. These data are essential for the detailed analysis and design of each route in the longitudinal direction. This section covers how this data is created, and its contents.

## 2D Versus 3D Profiles

Conventionally, profile data are extracted along the canal alignment line. The data is produced as station vs elevation data pairs. This is the 2D version of the profile data, that is used in longitudinal designs.

![](Images/Image%20104.png)

While still usable, such profiles miss significant detail on the sides of the canal, that can lead to substantial errors when estimating quantities.

On the other hand, 3D profiles (or strip profiles) consider terrain variations on both sides of the alignment to allow accurate analysis and reporting of quantieis. The profile data is taken at desired station increments both longitudinally, and transverse wise.

![](Images/Image%20105.png)

In CanalNET, the 3D profile extraction can be customized to the nature of the terrain, and the expected foot print of the canal structures. Hence, it is **Strongly** recommended to generate profile data by canal generation.

For instance, a first generation canal (a main or primary canal) crossing undulating terrain could benefit from a 50m wide offset specification. This will help capture adequate surface geometry both to the left and right. For Teritiary canals however, a 10m wide offset may be more than enough. Such custom settings can be easily applied (as shown below.)


> **Tip:** 3D profiles can be extracted and used in both CanalNET and iCAD products. However, they can only be visualized (as above) using iCAD interface.

How profiles data is extracted is specified by the `Offset Stations` parameter of the process, covered below.

## Extract Profile for a Single Canal Route
[Back to Home](../index.md#wellcome)


1. Start by loading a topographic data from AutoCAD host object to the CanalNET workspace. Refere these guides on [how to host topo data](../Surface_Modelling/manage.md#hosting-surface-data) and [how to load Topo Data](../Surface_Modelling/manage.md#loading-surface-data).[Refer here for guidance](../Surface_Modelling/manage.md)

   Before proceeding to the next step make sure the menu item `Workspace > Surface Data > Load Hosted Data` is checked.

   ![](Images/Image%20103.png)

   The succesful loading of nce the topo data is available in the workspace, proceed to next steps.

2. Selelect the as many as desired routes for profile extraction task by clicking on them. Then start `Workflow > Vertical Design > Route Profile` menu command.

   ![](Images/Image%20106.png)

   
3. The variable editor dialog appears. Choose the offset specification desired for the 3D profile extraction as shown.

   ![](Images/Image%20107.png)

   > **Tip:** Notice the notation for offset specificaiton [-25:5:-15, -12.5:2.5:12.5, 15:5:25]. Using this data will be collected at 5m intervals from -25 to -15, then at 2.5m intervals from -12.5 to +12.5 (requesting higher resolution near the center of the canal alignment) and at 5m interval from +15 to +25. This is a shorter version to stating the entire offset locations as:
   
   [-25, -20, -15, -12.5, -10, -7.5, -5, -2.5, 0, 2.5, 5, 7.5, 10, 12.5, 15, 20, 25]


4. Upon hitting `Apply` button, the profile data is extracted and stored in the data file. (Not yet visible)

## View Profile Data
   
> **Note:** This process assumes that a resolved and sized network is ready in CanalNET workspace. With out nodes, the process will not complete (and throw an error).

To view the contents of the profile data:

1. Use the `Workflow > Vertical Design > Soft Reload Route` menu command.

   ![](Images/Image%20114.png)

   The canal alignment will be drawn in solid line. 

   > **Tip:** Canal routes drawn in broken lines are those with out profile data. If drawn with a solid line (as above), this confirms availablity of the profile data.

2. Make sure the interface is on the default view from `View > View Mode` and selecting `Default View`. This view allows to show profile data.

   ![](Images/Image%20115.png)

3. Click on the route to view the profile data. This will show the data on the top window as shown below.

   ![](Images/Image%20116.png)

   **Tip:** If not shown, make sure the *Multi-Select* mode is off, and try again.

4. Start cross-section view from the bottom left, and click on the vertical bars in the profile view. The cross-section data at the desired station is shown in the detail view axis (bottom right of the interface.)

   ![](Images/Image%20117.png)


> **Tip:** You can view larger cross-section windo from `View > View Mode` and selecting *Bigger Detail View.*

## Extract Profile for Multiple Routes
   
   This process assumes that a resolved and sized network is ready in CanalNET workspace. If not selection by subroutes methods will not work.

1. One can also select a group of canals by fucntion. To a secondary canal and its teritiary branches, first pick the secondary canal, and start the `Edit > Select Routes > Select Sub Routes` menu command.

   ![](Images/Image%20108.png)

2. On the dialog, choose both generations, and hit `Ok`.

   ![](Images/Image%20109.png)

   The results is confirmed, and the desired canals are selected.

3. Invoke the profile command as above, and this time specificy a smaller offset window of say 12m, from -6 to +6 at 2m intervals. Hit `Apply` to complete the command.

   ![](Images/Image%20110.png)


4. Select desired routes, and use `Workspace > Vertical Design > Soft Reload` to bring the data from the data file to the workspace.

   ![](Images/Image%20111.png).

   Confirm to the *Multi Route Softreload* dialog, and the data is loaded to workspace. 

   ![](Images/Image%20112.png)
   
   Once all data are created, reload the data to the workspace.

   > **Note:** All canals with profile data are shown in solid lines, and the rest in broken lines.


## Clearing/Re-extracting Profile Data

If needes, profile data can be re-extracted at any given time - either for single canals or for multiple canals.

1. Select the routes for which profile data extraction is required, and start `Workflow > Vertical Design > Profile Data`.

   ![](Images/Image%20118.png)

   This will display the dialog shown. 

2. If you choose `Re-extract`, the editor will appear. Change any settings, and hit on `Apply` to continue.

   ![](Images/Image%20119.png)

   The profile extraction will be done again, and the data available upon `Workflow > Vertical Design > Soft Reload`.

3. If you choose `Clear` the profile data contents will be removed both from the canal(s) in workspace, and the data file. The canal route lines will be changed to broken line (as shown below).
   
   ![](Images/IMage%20120.png)
   

## A Note about Data File

Profile data is mainly stored in the data file. Data files are created alongside the AutoCAD project file to store CanalNET specific data. Upon use (for instance when Soft Reloading) they are linked to the corresponding canal routes (known by their AutoCAD IDs).

The data file for any AutoCAD file is located in the same folder as the AutoCAD file itself.

For an open AutoCAD file, to access the data file:

1. Start `Workspace > File Utilities > Open Project`. 
   
   ![](Images/IMage%20122.png)

2. This will start the Windows Explorer window. The file with .xsd extension is the data file used by CanalNET, and iCAD. All the route, node and profile informations (and more) are stored here.

![](Images/Image%20121.png)

>**Note:** If this file is moved or renamed, the data and works saved will not be accessible.


[Back to Top](#)
