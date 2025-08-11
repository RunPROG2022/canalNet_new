---
sidebar_position: 6
---

# Solving for optimal flow section for individual segments
[Back to Home](../index.md#wellcome)

Flow sections for individual segments, and the wider network of canals in general, are often expected to perform under established constraints that include:

- minimum non-silting velocity

- maximum non-scouring velocity

- Maximum allowable shear stress

The flow section design tool offers the capabilty to interactively vary the bed slope of a given canal segment and see impacts on above parameters. The accepted design detail can be applied to the segment at the end.

This tool is availiable for a single segment in the profile view, and accesible from the `Indicator Button` in the `Assembly Pannel` pannel.

To start it, select a desired segment from the profile view. The `Performance Indicator Button` will be active. Click on it. The *Canal Section Design* interface will pop up.

![](Images/Image%20023.png)

> **Important Note:** Note that, the interface starts with the solution for the set design criteria. If changes are made to B or D (e.g., using the minPw solver), the intial display still correspond to the solution for the design criteria settings.


The main purpose of this interface, among others, may be to anlyze the variation of the flow section as the slope varies. As the slope is varied, by dragging the vertical bar the flow section and corresponding flow velocity and sheat stress developed are computed and displayed. The colored scales on the gauge bars provide feedback on appropriateness of the slope.

To see how performance of the canal varies:

* change the slope by clicking on (or draging the marker) on the vertical slider bar representing the bed slope of the canal. The flow section, the resulting velocity and shear stress values change accordingly.

* The updated flow section is drawn, and also the details written to the `Results` area on the right of the interface.

The Solver function offers a convenient and automatic tool to determine the best fitting slope that respects the constraints for limiting velocity and shear stress set in the design criteria. The following Goal settings are available:

* `Min So` to find the minimum (steepest) slope possible with above constraints
* `Max So` to find the maximum (flattest) slope possible with above constraints
* `Min Pw` to find the section with the minimum wetted perimeter
* `Max Tau` to design the section with limiting shear stress value for the given canal bed material.

Upon hitting the `Solve` button, results are generated accordingly. Note that the minimum (steepest) slope allowed is limited to 1/50 and the maxium (flattest) slope is limited to 1/10000.


Upon satisfactory design, close the dialog, and accept the Apply request in the dialog that appears.


   ![](Images/Image%20027.png)

> Note: The `Max Tau` options is availabe when tractive force method is enabled by setting Tau_max variable (in design criteria) to 0.

[Back to Top](#)