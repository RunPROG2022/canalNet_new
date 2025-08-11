---
sidebar_position: 2
---

# Node Identification
[Back to Home](../index.md#wellcome)

**Node** is a feature located along a canal route, represetning connetivity to any branch canal, user inserted feature or at the end of the canal.

Nodes are key features in canal networks. They can be automatically created or user created. There are three types of nodes.

1. Canal junciton nodes: are created where a branch canal meets a parent canal. These are represented as circles. These are represented as Circles.

2. End of Canal Nodes: are created where a canal route terminates with out connection to a branch canal. Such nodes are represented as squares. These are represented as squares.

3. Floating Nodes: are created by the user to represent different hydraulic or structural conditions. (These are discussed in advanced tools.)
 

   ![Figure showing appearance of Junction Nodes and End-of-Canal nodes in layout view area.](Images/Image%20012.png) 

*Figure showing appearance of Junction Nodes and End-of-Canal nodes in layout view area.*

Follow below three steps for a full proof process:

1. Menu ` Workflow > Nodes > ID Nodes`, automatically identify and insert nodes as needed.

   ![Confirm dialog before Node Identification process for entire network.](Images/Image%20015.png)

   > Tip: Node ID can be done for one or more selected routes. To do so, start the menu command after selecting the desired routes.
   
   ![Confirm dialog before Node Identification process.](Images/Image%20014.png)
   
   *Figure showing the confirm dialog before Node Identification process.*
   
2. Menu `Workflow > Nodes > Convert EoC Nodes` handles any *inappropriately* identified end of canal nodes, that must be converted to junction nodes.

   ![](Images/Image%20074.png)
   
   *Figure: Showing End-of-Canal (EoC) node that needs fixing.*

   ![Convert EoC Nodes menu command](Images/Image%20019.png)


   ![Confirm Operation dialog.](Images/Image%20020.png)

   Upon confirmation, the automatic conversion process will proceed and report the number of nodes converted (if any).

   ![](Images/Image%20075.png)

3. The final step is to run the `Workflow > Node Id > Diagnose Multiple Parent Nodes` command. This will find and highlight any nodes that may vaiolate basic node behaviours. Typically, routes with multiple begining junctions to different rotues. See [Avoiding Pitfalls here](../Data%20Preparation/Data%20Preparation.md)

   ![](Images/Image%20076.png)


   ![](Images/Image%20077.png)

   It is important to ensure there are **NO** such nodes in the network before proceeding, as confirmed by the dialog.

[Back to Top](#)