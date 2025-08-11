---
sidebar_position: 4
---

# Identifying and Resolving Connectivity Issues
[Back to Home](../index.md#wellcome)

The following are commonly encoutered isses with the connectivity established.

### Wrongly Placed EoC Nodes

![Wrongly created EOC Node instead of a Junction node.](Images/Image%20016.png) 

These are best handled by the menu command `Workflow > Nodees > Convert EoC Nodes`. To handle manually, 

1. First right-click on the branch canal to select it.

1. Then left-click on the EOC node to be corrected. This will invoke the *Edit Node* dialog, detailing the current connectivity status at the specific node.
   
   ![Edit Node Dialog for the EoC node](Images/Image%20017.png) 
   
   *Edit Node Dialog for the EoC node*

2. Click on the` To Current Node` button to link the picked route to the node. This will correct the issue, also changing the square node marker to a circle node marker correctly representing a canal junction.
   
   ![Resolved Junction Node at End of Canal.](Images/Image%20018.png) 
   
   *Resolved Junction Node at End of Canal.*

### Reversing Routes
[Back to Top](#)

CanalNET's governing convention is the all canals must be drawn away from the parent canal. For supply canals this would require drawing routs in the direction of flow.

In CanalNET, after node creation, reverse drawn routes are easily identified by the square nodes appeading on the cross section with the parent canal. In AutoCAD, the vertex editing tool is used. 

![Network showing reversed canal route](./Images/Image%20067.png)

In the example, the upper left canal route has its end-of-canal node lying on the parent canal. This shows that route is reveresed. Clicking on the *Current Vertex* property, index 1 shows the end of the route, confirming the route is reversed.

To fix this issue,

1. In CanalNET, select the route(s) that need to be reversed.
2. start the command from `Workflow > Prep Network > Reverse Selected Routes...` menu item.
   ![Image 069](./Images/Image%20069.png)

   Notice, and confirm to the message, `This will remove all refered Nodes and Profile Data.`

3. All necessary changes are made to the AutoCAD object and the network data base, and status reported as shown below.

   ![AutoCAD object and network database status after reversal](./Images/Image%20070.png)

    Note the end-of-canal node is removed (Show nodes option displayed here). Also the AutoCAD vetex status have changed, confirming the change in AutoCAD.

1. Re-run Node ID to create the node corresponding to the new changes. The bracnh node is now correctly created.

   ![Branch node correctly created after reversal](./Images/Image%20071.png)


Note that, reversing routes manages the following task in one invokation:
   - delete refered nodes in the network data base to avoid residual data that causes error
   - Delete the profile data (if any) associated with the parent AutoCAD object, because this is no more relevant
   - Reimport the object coordinates to CanalNETWORK environment.

Note, also that, When working on already resolved and sized networks, routes reversed using the above tool will require the **pipe workflow** to be carried out, i.e, Node ID, Naming, Sizing (if needed with Farmblocks), Profile Extraction, and Soft-reloading.

### Missing Junction Nodes
[Back to Top](#)

Rarely, the algorithm seems to miss nodes where there should be one. Apparently intersecting canals may not have nodes after the NodeID process described above. Such a case is shown below.

![fig40](Images/Image%20046.png)

 In this case the user can introduce nodes manually. 

1. Relax the *Route Extension Length* parameter in `Work Space > Edit Preferences` to a reasonable amount depending on the distance bewtween the begining of the branch canal and the apparent intersection point with the parent canal. Usually a value of 2 meters gives good results. (Note: Max allowes is 5)
   
   ![fig 41](Images/Image%20047.png)

   > **Tip:** See Annex on Project Preferences for details.

2. Select the parent and branch canals. Make sure to enable multi-select from `Edit MultiSelect (Routes)`, to be able to make two route selections.

3. Run the Node ID process from `Workflow > Nodes > ID Nodes` . This will automatically prompt you for possible actions. 
   
   ![fig43](Images/Image%20048.png)
   
   Choose `Manual Add`.

4. If succesfully found, a dialog will display the location for the newly found node as shown below. Hit insert, and node will be inserted.
   
   ![fig48](Images/Image%20049.png)

### Mulitple Parent Nodes
[Back to Top](#)

The key purpose of node resolution is to ensure that each branch canal has only one parent canal. However, some canal arrangements may mislead the software and assign two routes as parents for a single brnach canal. Again, this ALWAYS happens when the assumptions and conventions listed early in this section are not fully observed during layout preparation in the AutoCAD environment.

CanalNETWORK can automatically locate these nodes in the network. The user must manually resolve the issue.

To identify nodes where multiple parent condition may be an issue, go to Workflow > Nodes > Diagnose Multiple-Parent Nodes. If found, the command will list such locations in a table.

![Multiple Parent Node issue identification](Images/Image%20023.png) 

![Resulting table for Multiple Parent Node issue identification](Images/Image%20024.png)

*Menu command and resulting table for Multiple Parent Node issue identification. The table shows both First and Second Nodes refering to the same branch canal (not shown in the table)*

Once this is ready, the user can navigate to each location and resolve the issue. To go to a particular node listed in the table, select it in the table, then use `View > Go To Route...` menu command, or simply click on the interface and use `Ctrl + G` keyboard shortcut:

![Go to Route menu command](Images/Image%20025.png)

*Go to Route menu command*

 The layout view will pan and zoon in to the desired node location.

In the table list of nodes shown above, both nodes refer to the one branch canal. This can be noted by left-clicking on each node, one at a time. It can be seen that the *Edit Node* dialog lists the same branch canal to each node. 

![Edit Node dialog showing same branch canal](Images/Image%20026.png)

![Edit Node dialog showing same branch canal](Images/Image%20027.png)

Obviously, the lower-right node is the issue. This is because, it is the end of a canal and no branch is expected or implied in the drawing. What caused this issue is the fact that the canal in question ends very close to the begining of the other canal. The AutoCAD drawing measurement confirms this.

![AutoCAD measured distance between end of a canal and begining of another canal.](Images/Image%20028.png)

 *AutoCAD measured distance between end of a canal and begining of another canal. Based on the preference (shown to the right) search radius for a neighbouring canal is 2x2meters (4meters) locating the wrong canal as a parent canal.*

![Preference search radius for a neighbouring canal](Images/Image%20029.png)

To resolve the issue:

1. Left-Click on the route for which multiple parents are assigned. It will be selected.

2. Left-Click on the mistaken Node (lower right inthis case). This will invoke the *Edit Node* dialog. 

3. Click on the `Remove Cur` button. This action will do two things: detach the branch canal from the node, and convert the node to EoC node.

![Edit Node dialog for mistaken Node](Images/Image%20030.png)

The issue is resolved. Repeat the above steps for all other such nodes.

Before continuing to the next step, Re run the test `Workflow > Nodes > Diagnose Multiple-Parent Nodes...`  to verify all issues are succesfully resolved, or new issues are not created in the process.

[Back to Top](#)