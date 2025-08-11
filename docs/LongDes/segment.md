
# Update Segment Data
[Back to Home](../index.md#wellcome)

Information for hydraulic and formation design in segments may require updating from time to time. Typically, a segment may exhibit a behaviour that is not expected as below:

- Variation in exit level

- Non-conformance with OGL and (beg/end) control inverts

The below picures demonstrates one such instance. Here, the control level and the CBL level at the control do not much. In this particular instance, it resulted from adjusting drop heights for the specific segment.

![figx](Images/Image%20051.png)

To resolve these issues, DO NOT USE ReDraw Node DBL button, as shown at bottom right. This will erase all drop station and heigh information, and create a new data set. Instead, refresh the profile view by clicking the canal route in plan view.

> Note: ReDraw Nod DBL button, resets ALL drop information (i.e. station and fall heights) to null, and re-create them based on automatic settings. Beware, that this action, aslo does the same for the immediate downstream segment (if any). Use this button with descrition.

In above note, you notice that the reDraw button also creates an auto-generated data set for drop location in the immediate-next segment of the control. This is mandatory process, to ensure that any changes in invert level of the control node, is accomodated with respect to the downstream setment.

[Back to Top](#)