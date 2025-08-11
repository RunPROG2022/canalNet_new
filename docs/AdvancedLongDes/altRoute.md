---
sidebar_position: 4
---

# Alternate Routes Design
[Back to Home](../index.md#wellcome)

Alternative route analysis is a powerful way to formulate cost effective canal routes and their provissions. The command is available from `Workflow > Routes > ALternate Routes ...`

All canal routes are established using one alignment object from the AutoCAD ennvironment. To use this tool, an alternate alignment object must be prepared along with the existing alignment. Alternate routes are best prepared using the `Gradient Search` tool from `Workflow > Inquire 3D > Inquire Points` menu command. The following figures show alignments created using the tool for a teritiary drain and supply canal respectively.


![](Images/Image%20084.png)

*Fig: Alternate routes for drainage Routes, starting and ending with the same constraints*

![](Images/Image%20085.png)

*Fig: Alternate Route for a supply canal, slightlt longer than the original route, and beyond (extension of) the last branch canal route*

> **Note:** To use the tool, the original canal must be fully defined for flow cnditions.

To do alternatre route anlysis for a given route,
1. Click on the route in plan view to display its longitudinal profile view. Assuming volume comparison is the objective for the alternate route analysis, annotate for earth volume as shown below.
    
    ![](Images/Image%20086.png)

1. Go to `Workflow > Routes > ALternate Route...`. Click on `Create`.

    ![](Images/Image%20088.png)

2. In AutoCAD, pick the alignment for the alternate route. The CanalNET interface will update both in plan and profile views, to show the alternate alignment.

    ![](Images/Image%20090.png)

    Choose `Cancel`, and work on the longitudinal design as needed. When done, redo annotation to compare values.

1. To revert, to original design, start the menu command again, and choose `Revert'.
1. To test a variation of the alternate alognment, simply edit the AutoCAD object for the alternate route. Start the menu command, and choose `Update`.

1. To remove the alternate route information, start the menu command, and choose `Delete`.

> **Note:** Designs on Alternate routes are only available until `Update` button is used - whixh causes all Nodes to loose DBL data and force redraw.

[Back to Top](#)