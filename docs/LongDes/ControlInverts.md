---
sidebar_position: 3
---

# Adjust Control Inverts
[Back to Home](../index.md#wellcome)

Controls comprise key components in longitudinal design of routes. They represent acual control structures, such as Turn outs and division boxes. The primary task of the engineer can be to design the invert levels of these controls.

> Note: Canal Controls, represented as vertical bars in the profile view axis, represent invert and hydraulic information at and upstream of the control location.

Controlling inverts and other hydraulic characteristics hosted by the control is possible from the `Node Panel` at the right side of the interface. 

It is important to note that, all values displayed for a control node, are an exact copy of the design criteria, applied during canal sizing operation.  Hence, any edit the user does for the control is effectively over-riding the provissions of the design criteria.

Select a control node in the profile view. Then: 

![](Images/Image%20012.png)

To change the invert level upstream of the control:

* Use Node Invert Level edit box to directly input elevation values

* Use the left `<` and right `>` arrow to increment the current value of the invert level for the control

> Note: The algorithm maintains the settings in the design criteria regardless of the the user inputs. Hence, there is a limit to how high or low the invert can be raised or lowered. For instance, any control can not be raised above the level that is maintained by the bed slope of the upstream canal section.

![](Images/Image%20013.png)

There are two ways to change invert level downstream of the control:

* Set Exit Drop: Type the desired value directly the Exit Drop edit box (with respect to upstream invert level.) Typically, this value is a negative value representing a drop in elevation calculated with respect to the upstream invert.

* Set Head Loss: Check the HL option box, and type a desired head loss value. This is also typically a negative value indicating the desired headloss to maintain as the flow transitions through the control. This process, calculates an exit drop at the control that can satisfy the desired head loss amount, and apply to the control.

![](Images/Image%20014.png)

Change how drops are located upstream of the selected control, by:

* Change or set a fit height *fitHt* for drop positioning at `Use Fit Height` edit box. Drops are located in one of three ways:
  
  * *fitHt* &lt;=0 ensures that drops are inserted where the bed level is exactly *fitHt* units below the OGL 
  
  * *fitHt*  >0 ensures that drops are inserted where the FSL level is exactly *fitHt* units above the OGL.
  
  * *fitHt* =-99 ensures that there is no drop inserted upstream of the current control.

* Check the `Fit DBL for No Drop` option to set *fitHt* to -99.

![](Images/Image%20015.png)

To Change the bed slope upstream of the control,

* edit the `Change Bed Slope` edit box to desired value. This is typicall a positive value equal to the desired canal slope (H:V).

* Click on the drop down menu at the right of the edit box, to pick from a set of default values.

![imag](Images/Image%20016.png)

Finally, to change the functions of the control:

* By default, all controls are configured as Turnout structures. You can decide to change it to a division box struture or no structure at all. If HR/CR provissions are expected, then turning off both checkboxes ensure the control is treated as a simple junction (no structure associated to it, and no head losses applied to branch canals). Such controls have no quantities associated with them.

   ![Image 076](./Images/Image%20076.png)

* To change the function of the control to a division box structure, check the Division Box option. (Note: Division boxes are allowed on Parent Canals whose capacity is ≤ 80 litres per second.)

* This will throw the confirm dialog shown below.
  
  ![d](Images/Image%20001.png)

* If user resonds with Yes button, then, this will invoke hydraulic calculation and design algorithm to size and position the control along with its branch canal(s) appropriately.

* One can view the results of the hydraulic analysis by clicking on the R button next to the Division box check box. A report of the following form will be generated informing the user of the hydraulic analysis carried out, and the adjustments made to the inverts of the offtaking canals.
  
  ![a](./Images/Image%20002.png)
  
  ![a](./Images/Image%20003.png)

* The same button also redesigns the division box currently selected, for any changes that may have been made to invert levels, flow depths, or similar. A new report, and a new set of invert levels are calculated and applied to the offtaking canals corresponding to the modification made.

To reapply the default criteria set for the entire route, thereby removing any and all overrides done manually, the user must resize the canal. See part of this guide on [Design Criteria creation and use](..DesignCriteria/AboutDesignCriteria.md)  for more details.

[Back to Top](#)



