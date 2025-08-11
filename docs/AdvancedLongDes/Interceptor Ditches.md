---
sidebar_position: 3
---

# Interceptor Drain Ditches

Interceptor ditches can be inserted on any canal segment. These features can succesfully create drainage ditches on base canals under the following conditions: 
- when base canal is traversing in cut conditions
- when berm provisions are made, and application conditions are met.

   

  ![test](Images/Image%20077.png)
  

   The ditch features created in this manner are accessed by major tasks, including LSec profile table generation, bill of quantity estimation, and plan view generation.
  
  ![test](Images/Image%20078.png)
  

## Insert Interceptor Drains
[Back to Top](#)

Follow below steps to insert these features in to your design:

1. Dedicate a canal generation from the current naming style, that will be used for hydraulic design of the drainage canals. Set hydraulic design creiteria as needed.

    In below example, a KC generation is used. The important parameters are highlighted.

    ![](Images/Image%20079.png)
    


    >**Important Note:** Canal naming styles and their design criteira must be kept consitent at all times. Any changes will need meticulous work to reflect/capture them all in design product outputs.

1. Navigate the canal route, and click on the node representing the desired segment on which to add drainage canals. Then go to `Workflow > Interceptor Drain > Insert/Edit...` menu command. 

    If creating Interceptor drains for the first time, the following dialog will appear, and let you pick a canal generation for template.

    ![](Images/Image%20081.png)

    Then following dialog appears, allowing to customize design values from the criteria created above.

    ![](Images/Image%20080.png)

1. Use the above menu command as well, to **edit parameters for an existing node**. Select the node control in profile view axis, and start the menu command. The exsitng settings will be displayed and can be edited.


1. Set the desired values for the canal, and hit apply. The drainage canal section is automatically sized for dimensions and applied. 

    **Note:** The bed slope of the base canal is used in the hydraulic calculations.

    **Note:** The direction is decided often on the side of larger berm provission. Hence the setting in above dialog may not always be respected.

This ensures the drainage ditches are built in to the network in further anlysis work. Create a cross-section, Lsec data table or plan view as you would normally do, and you will notice the ditches are included.

## Clear Interceptor drain provissions
[Back to Home](../index.md#wellcome)

There are two ways to clear interceptor ditch data on control nodes.

1. To clear data on single nodes, select the node in profile view, and start the `Workflow > Interceptor Drain > Clear ...` menu command.  When prompted, confirm action.

    ![](Images/Image%20082.png)

2. To clear data on multiple nodes, clear any selection in profile veiew axis, and start the menu command. Pick desired nodes to clear, and hit `OK` button.

   ![](Images/Image%20083.png)

**Known Limitations:** Ditches may not be applied near the begining or end stations of station range in cut, where berm provissions could not be met. Read the [Chapter: About Design Criteria] to learn more on conditions governing berm provissions. 

[Back to Top](#)
