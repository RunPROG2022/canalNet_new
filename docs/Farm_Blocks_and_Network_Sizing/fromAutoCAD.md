---
sidebar_position: 1
---

# Farmblocks from AutoCAD
[Back to Home](../index.md#wellcome)

Farm blocks can be created in CanalNET workspace using one of two possible methods.

1. Read drawing objects representing farm blocks in AutoCAD. This is the most accurate method, and also can be very time consuming.

2. Automatically estimate the area each canal may be serving. This is a quick process, and also the least accurate.

 
To read farmblock area data from AutoCAD, first create the farm blocks using polyines. There are a few ways to draw farm blocks.

* Field canal irrigating to both sides: Draw ensclosing polyline objects around the area served by the field canal. 
  
  ![Area crossing canal](Images/Image%20001.png)

* Field canal irrigating only either to the left or to the right: creat a polygon area covering the area served by the canal, and add a zero area extension at a location convenient to cross with the feeded canal.
  
  To add a zero area extenaion, click on the boundary and hover over the vertex you want to edit and choose `Add Vertex` menu item.
  
  ![Add Vertex menu](Images/Image%20003.png)
  
  Pick a location over the other side of the canal.
  
  ![Pick location over canal](Images/Image%20004.png)
  
  Finally modify the resulting geometry by moving the next vertes to over lap with the previous vertex.
  
  ![Modify geometry](Images/Image%20005.png)
  
  ![Final geometry](Images/Image%20006.png)
  
  The final geometry is shown above. This ensures the the area crosses the desired canal route, with out any change on the area of the block area delineated (hence the term zero-area extension.)

> Note: Each farmblock area should cross ONLY one serving canal. The converse is also true, i.e., each canal should only be crossed by one farmblock boundary. Otherwsie, the first canal that is found to cross with a given farmblock is assigned the area of the farmblock. 

Once these are ready:

1. Collect all farm blocks to fascilitate easy import. This can be done in either of two ways. Either instantiate all the farm blocks in to one or few host objects, or construct/ move all farm block boundaries to a separate layer.

2. To import from a host instance object go to `Workflow > Farm Blocks > (Re)Import Farm Blocks...` menu command. To import from layer go to `Workflow > Farm Blocks> (Re)Import Farm Blocks By Layer...` Both methods are valid.
   
   ![Import farm blocks menu](Images/Image%20007.png)
   
   This will start the *Choose* dialog. 
   
   ![Choose dialog](Images/Image%20008.png)
   
   If importing for the first time, or desire to overwrite all existing associated data, choose `Reset All`. If you want to append the current collection to the existing data, choose `Update Only`.  For the case under consideration, Reset All would be the right choice, so hit the corresponding button.
   
   ![Reset All dialog](Images/Image%20009.png)
   
   Confirm the action in the dialog.
   
   ![Confirm action dialog](Images/Image%20010.png)
   
   The *Done* dialog completes import process. The farmblocks imported are shown in the layout view area overlapping the network elements.

At this stage you can view the quantities of areas associated to each serving canal route, by using `View > Route Text > Select & Show Text...` and picking `A` field in the dialog.

![Show area label](Images/Image%20014.png)

You can also generate a table from `View > Workflow > Farm Blocks > Edit Blocks...` , and selecting `Current` when prompted.

![Edit Blocks table](Images/Image%20017.png)

![Current table](Images/Image%20015.png)

![Current table](Images/Image%20016.png)

One can modify the block data for any one route at any time, in one of two ways:

(a) by simply ReImporting the farm block object corresponding to the route. In this case you should choose `Update Only` button when prompted.

(b) by starting the Edit Block menu command, choosing `Reset` and editing the areas manually. Some times, geometrically editing farm blocks may not be a choice for the engieer. Rather editing a table may be required. This may be the case for canals in existing projects whose area is already prescribed. In this case:

1. Start Edit Blocks menu command as above

2. Choose `Reset`. This will erase any cummulative area information in the network and reset data to the original data during import.

3. simply start editing in the table, and hit `Apply`.
   
   ![Edit Block table](Images/Image%20019.png)

You can see that, the area corresponding to the parent canal is 0.00. This is because it does not serve a particular farm block. The area it serves shall be determined from cummlative of the areas that the sub-canals serve individually. To do this, 

1. First select the primary most canal for the network, to indicate the final direction of cummulation.

2. Then go to `Workflow > Farm Blocks > Edit Block Areas...` and choose `Cummulate` button.

3. The table data is updated to show the cummulated area each route is serving, as shown below. Hit `Apply` to continue to the next step.
   
   ![Cummulated area table](Images/Image%20018.png)

> Note: Area served is shown as a label in the layout view area ONLY for canals associated with Farm Blocks. Other canal routes will show Canal capacities as available.

> Note: If farm block data is updated, DO NOT forget to cummulate areas again to reflect the changes in the table, and `Apply` the new figures to the data base.

[Back to Top](#)