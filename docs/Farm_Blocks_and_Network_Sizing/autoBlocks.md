---
sidebar_position: 2
---

# Automatically Created Farm Blocks
[Back to Home](../index.md#wellcome)

Where fast estimates are required, the auto estimator tool can be used. The tool is available from `Workflow > Farm Blocks > Auto Estimate...` as shown below.

![Auto Estimate tool](Images/Image%20032.png)

Note: This should be applied on a fully resolved network, else errors will be encountered in the process.

To use the tool:

1. Start it as described above.
   
   Upon initiating the warning dialog appears, reiterating the results - if any is found - are approximate.
   
   ![Warning dialog](Images/Image%20022.png)
   
   Accept the subsequent confirm action messages. 
   
   ![Confirm action dialog](Images/Image%20023.png)

2. Next, you are prompted to provide a bugger distance. This value is used to determine the distance beween adjacent farm blocks. Note the value is a negative value, indicating that the areas determined will be shrinked away from boundary lines determined by the algorithm.
   
   ![Buffer distance dialog](Images/Image%20024.png)

3. The final result is presented as shown below, giving the sum total of farm parcel areas found for the network. You can see that the blocks are only calculated for the last generation canals.
   
   ![Sum total farm parcel areas](Images/Image%20025.png)
   
   The process ends with the below dialog.
   
   ![Process end dialog](Images/Image%20026.png)

The above process, has already assigned each route in the network with the corresponding estimated areas of the farm parcel area. This can be viewed from `Workflow > Farm Blocks > Edit Block Area` command. The procedure is same as that for the manual process described further above.

The table will display a result similar to below snapshot.

![AutoEstimate result table](Images/Image%20028.png)

You can select/deselect parcels by left-clicking on them, and choose to delete them.

> Note: Delete job can not be undone. You will have to regenerate the blocks again.

 You can also view the size of selected parcels by rightclicking on them and choosing `Properties`.

![Parcel properties](Images/Image%20027.png)

[Back to Top](#)