---
sidebar_position: 7
---

# Change and Re-apply Design Criteria
[Back to Home](../index.md#wellcome)

It may be necessary to apply a specialized set of criteria to a certain canal in the network, to accomodate site specific conditions. That is, with out impacting how the standard design criteria set is applied in the entire network. In such cases, one can follow below methods to achieve the desired design refinement.

## Reset Design Criteria to Default
[Back to Top](#)

To reset the design criteria for a route:

1. Select the route desired, and start the command `Workspace > Manage Design Criteria > Set/Edit Design Criteria ...`  or Ctrl+E. This will display the current settings for the route.

2. Further downfor *On Apply Use For* parameter, choose *Reset To Default*, and hit `Apply`.
   
   
   
   ![fig](Images/Image%20070.png)

3. Confirm to the dialog by hitting `(Re)Apply` button.
   
   ![fsds](Images/Image%20071.png)

This will extract default design criteria and apply the current route. To review, start the menu command again and proceed.


## Override design criteria (Exception)
[Back to Top](#)

Canal routes, every time they are refreshed, refer to the design criteria corresponding to their level or generation. To override some of these parameters as the site condition may require, users have to change junction node and canal segment assembly criteria. This makes the job time consuming, particularly for long canal routes.

Instead, users can over ride the entire design criteria for a canal route and allow specific criteria for a route. 

![](Images/Image%20006.png)

To set override values and apply to the current route:

* Start the editror from Workspace > Manage Design Criteria > Set Edit Design Criteria... 

* Change the values of the desired parameters 

* Go to the final row, and for the *On Apply Use for* choose *Current Route*. 

* Hit `Apply `to complete.  This will review every aspect of the route to conform to the new set of criteria.

Note: The new set of criteria are also saved on to the exception data string for the route. This allows to re-visit the input data at a latter stage, and modify it. If not needed, it can be removed from `Edit > Route Exception > Manage Exceptions...`

Important: Exception design criteria EXCLUDE all variables in the command criteria group of variables.

[Back to Top](#)