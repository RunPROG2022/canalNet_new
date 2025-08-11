---
sidebar_position: 3
---

# Editing Farm Blocks
[Back to Home](../index.md#wellcome)

Farm blocks automatically created can be edited and updated by using the context menu accessed by right-clicking on any block.

To select blocks for processing, click on the desired blocks. The blocks will be selected or deselected accordingly. Use `Select All` option to select all blocks.

![Select blocks](Images/Image%20034.png)

To view area and associated property, use the `Properties` context menu.

![Properties context menu](Images/Image%20035.png)

To Delete blocks, use `Delete Block(s)` context menu. This is helpful, when canals that do not supply water to fields are assigned a block.

You can also draw the farm blocks to AutoCAD. This allows to easily edit the vertices of each farm block and update from it. To achieve this a farm block host object is required. The object must be referenced to the comman area reference axis, and tagged appropriately.

To Link a Host Object: go to `WorkFlow > Farm Blocks > Host Object` . 

![Host Object menu](Images/Image%20036.png)

This will display the dialog showig the contents of the selected host object if any are found. Click on the `Link` button to accept.

![Host Object dialog](Images/Image%20037.png)

Note: The menu item now shows the changes made.

![Menu item change](Images/Image%20038.png)

To draw blocks to AutoCAD, select the desired blocks and choose the `Draw to CAD` context menu. This will create the drawings to AutoCAD. You can edit the vetrices of any of the blocks.

![Draw to CAD context menu](Images/Image%20041.png)

To update from the drawings, select the desired blocks to update, and choose `Update from CAD` context menu. A dialog will show 

![Update from CAD context menu](Images/Image%20042.png)

Such work saved in AutoCAD can be reloaded to the CanalNETWORK environment using `Workflow > FarmBlocks> AutoEstimate...` tool, if the FarmBlock Host object is available and linked.

**Helpful Tips:**

- It is highly recommended to create and use a separate layer to contain the host object and the blocks of farm parcels. With the number of objects increasing in the AutoCAD environment, it may be hard to keep track of changes, and accidentally delete uninteded objects that may cause problems at later stage.

- Blocks drawn to AutoCAD and edited, can be imported entirely to CanalNETWORK by using `Workflow > FarmBlocks > Auto Estimate...` again.

- Using `Edit > Highlight Selection in AutoCAD` helps to know which block is for which route while working in AutoCAD.
  
- You can not import farm blocks using manual steps, while a FarmBlock host object is linked to the current workspace. The following message will appear if attempted.
  
  ![Highlight selection info](Images/Image%20043.png)

- Highlighting in AutoCAD works only if a Host Object is provided.
- when plotting, if the drawn blocks are offset from their expected location (as shown here), reference the host object again and try. It should be resolved.

    ![Offset blocks example](Images/Image%20045.png)

[Back to Top](#)