---
sidebar_position: 1
---

# Generate Names to AutoCAD
[Back to Home](../index.md#wellcome)


CanalNET automatically assigns names to canal routes in a network. These names can be re-created in AutoCAD environment as follows.

1. Make sure AutoCAD is ready to accept the export. For instance, create a separate layer to hold the text contents and make it the current layer. Change the current color, and text style as needed.
   
2. Create a sample text in AutoCAD. This will be used as a source to dictate the height of all naming texts to be created.
   
   ![](Images/Image%2010.png)

   
3. If not already, create the names in CanalNET using `View > Route Text > Select and Show Text...` and selecting the desired elements to include in the text.

    ![](Images/Image%2009.png)

4. Start the menu command `Explore Solutions > Plot to AutoCAD > Plot Route Text` menu command.
   
   ![](Images/Imag%2011.png)

   Confirm to the prompt, and pick the prepared text in step 2 above.

5. This will recreate the text information in AutoCAD to the current layer, style and color.

    ![](Images/Image%2012.png)

[Back to Top](#)