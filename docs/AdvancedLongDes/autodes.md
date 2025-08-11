---
sidebar_position: 2
---

# AutoDesign Tool
[Back to Home](../index.md#wellcome)

CanalNET often delivers an acceptable design at the first attempt. However, on occasions where more considerations are deemed necessary, the autodesign feature can offer alternate and more refined vertical designs. These tools can be applied either to:
- specific segment of a canal
- the entire canal route it self (for all segments)
- or a collection of canal routes.


## AutoDesign a Canal Segment
[Back to Top](#)

By default, the software generates a tentaive longitudinal profile for the route upon refreshing the profile view. Characteristics of this tentaive design include, bur are not limited to, the following:

* applies the set design slope from the design criteria for the specific route through out the reach

* automatically positions the invert levels of controls to ensure flow of water down stream. To this end, controls may be fixed for no drop structure upstream of the control location, or with drop structure depending on available gradient.

For many reasons, this tentative design will not meet operational requirements. For example, slope must vary depending on the ground level variation. Accordingly flow velocity varies. Further more minimum flow level above ground leve is often a strict requirement. This tentative design does not, however, account for this.

Auto Design tool implements a sophisticated algorithm to factor all the above requireemnts during design work. In the latest version, Auto Design tool is improved to complete longitudinal design of routes faster. The tool now generates the best achievable bed level profile for the given set of conditions to the route. The given set of conditions are as depicted in:

* design criteria provisions, most notably the following:
  
  * maximum and minumum allowable velocities, 
  
  * allowable shear stress.
  
  * allowable minimum FSL above OGL

* variation of ground level in the entire reach of the route

Once again, the careful selection and setting of design criteria for canal routes can not be overemphasized. It affects the outputs of the automatic design, and hence directly impacts the time an engineer spends to complete the design of a single route.

## AutoDesign for Route
[Back to Top](#)

The above procedure used for designing a single segment of a given route can be applied for an entire length of a route. To do so

* Go to `Workflow > Design and Analysis > Auto Design Current Route ` 

* The process will continue in the background (with out invoking the *Canal Section Design* interface), but applying the changes to the segments.

Note the following added functionalities in this use-case:

1. Automatically considers the available slope from the OGL. Note here that the ground slope is calculated from invert levels of the upstream and downstream nodes of each segment, and hence assumed to be straight line.

2. Automatic positioning of inverts attempting to respect minimum FSL-OGL value in the design criteria set, where possible.

To see the viability of the result from this auto-design process, the user can create and manage annotations - especially:

* Drop heights: looking out for non-standard drops that may have been created, and adjusting if necessary. (see below [Design Aids Available for Completing Design of Routes] below.)

* minFSL-OGL: looking out for red-colored texts, indicating the desired criteria value is not met on those controls, and adjusting the inverts manually if needed. (See [Adjust Control Inverts] above.)

## AutoDesigning a Selection of Routes
[Back to Top](#)

![](Images/Image%20007.png)

AutoDesign tool can be applied to a selection of routes in one go. To start the tool:

* Select the desired routes in the plan view (iwth Multi-select mode set to ON). Use available tools from `Edit > Select Routes` if needed.

* Go to `Workflow > Design and Analaysis > AutoDesign Route(s)...` 

This will start the process for all selected routes sequentially.

Important: It is important to revisit the designs for each route designed with the Auto tool, and make any adjustments before production.

*Note: AutoDesign task can not be undone. To reset to original tentative settings, select the route, apply Resize. Design parameters are reapplied. To view the updated view, click on the route in plan view, which will refresh the view in Profile View Axis.*

[Back to Top](#)