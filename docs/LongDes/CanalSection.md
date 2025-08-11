---
sidebar_positoin: 3
---

# Adjust Canal Assembly for Segments
[Back to Home](../index.md#wellcome)

The last area of control for the user to guide and influence longitudinal canal is the `Canal Assembly` panel. In this panel, information regarding the parameters that determine the shape and size of the canal section and its flow parameters can be adjusted. 

> Note: When a node is selected, this panel shows flow information in the segment upstream (downstream for drain) of the control.

The small rectangular button, indicated with an arrow in below figure, is known as Perfoamnce Indicator butto. It shows the acceptability of the flow conditions. Numerous comparisons are made with respect to available design criteria to show the perofmance, namely:

- A **RED** color indicates a high level alert, showing either limiting velocities or shear stress limits are exceeded. The text contains one or two exclamation marks.



    ![test](Images/Image 075.png")

- A **YELLOW**  color indicates low level alert, showing actual flow velocities exceed criteria velocity values. The text contains a question mark.

- A **GREEN** color indicates acceptable perfomance in all respects. The text contains neither question marks or exclamation marks.

For detailed information about the different flow paramters, see section on [Exploring Flow Sections](#Exploring-Flow-Sections) further below.

tells that either the velocity limits or the shear stress limits are not respected, and redesign is needed.

The user can interact with the canal assembly informaiton in many ways. Select(click on the OGL profile line) a canal segment or reach in the profile view that you want to edit and follow below guideline:

![test](Images/Image%20021.png)

To change the flow section, drop design or construction parameters:

* click on `Edit Assembly` drop down menu, and choose the relevant design option. This will open up a dialog to edit corresponding variables fot the canal segment. See [Design Criteria Setting and Use](../) for details on each variable and their design implication.

![](Images/Image%20022.png)

To redesign the flow section by adjusting the slope within allowable performance criteria:

* Click on the `Perfoamcne Indicator` button. This will invoke a dedicated interface to interactively design the section. 

* After making the desired changes, close the interface. The user will be promted to apply the changes, and the profile view will update automatically to update the changes.

* See further below topic [Solving Optimal flow sections for Individual segments] further below for guidance on using the solve function.

[Back to Top](#)