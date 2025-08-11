---
sidebar_positon: 2
---

# Manage Vertical Drops
[Back to Home](../index.md#wellcome)

## Adjust Size of Drops

Drops are created automatically following the variation of the ground level. They are positioned strictly per the provisions of *CBL_designSettings* parameter set in the design criteria. See [Design Criteria Creation and Use] for the meaning and use of each of these variables.

For many reasons, the automated design output will not satisfy the engineers desires. Each drop can be edited and adjusted as follows:

To change the location of the drop:

- Click on the desired drop. An interactive tool appears reading station location for the new locatio of the drop. Click at the desired new location, and the drop is repositioned to a new station.

![](Images/Image%20017.png)

Annotation information can also be used to guide drop insertion. Often times, one may want to locate the position of drops manually based on FSL-OG or CTL-OGL values. This can be achieved by using the above same method, but after invoking supported annotations. 

In the example below, the drop near statio 1600 is automatically positioned using the setting of FitHt=-0.5.This can be confirmed by starting the relevant annotator from `Explore Solutions > Annotators > CBL-OGL`. It can be seen in the annotator, CBL-OGL= -0.513, slightly higher than specified because of the position the reading is taken. 

![image036](images/Image%20036.png)

Assume, it is required to move this drop to a location where CBL-OGL is about -0.20. First, move the drop further right to about station 1+670.

![Image037](images/Image%20037.png)

Now, click on the drop again. The interactive, marker tracks the value of CBL-OGL as you move the location. Drag to the new location where CBL-OGL meets the desired value. In this case it is near station 1+639. Click, and the drop is positioned.

![image038](images/Image%20038.png)

As shown below, there are other ways to edit drop positions. To manually change the location and/or height of the drop:

![](Images/Image%20018.png)

![](Images/Image%20019.png)

* right click on the desired drop, and choose Adjust Drop conext menu item. This will start a dialog box. 

* Enter the desired station,  and click on Apply. The drop is repositioned accordingly.

* Enter a desired drop height, and click apply. The drop height us adjusted accordingly.

> Note: User inputs are guided by allowable values for the specific drop.

Some times the last drop inserted in a canal segment can have odd values (not suitable for construction.) In such cases the user can make fine adjustment by typing in numeric expressions in the `Edit Node Invert` edit box inside the Node Panel.

![](Images/Image%20030.png)

In above snapshot, the drop height of 0.836 can be adjusted to 0.800 by adding 0.036 to the invert level of the downstream control. The result is shown below.

![](Images/Image%20031.png)

## Manage Invalid Drop Locations
[Back to Top](#)

In rare instances, the sum effect of the drop location parameters specified by the user is not actionable. As a result, it may not be straight forward to position some drops. Also, the `Explore Drops` command may not collect and report drops in such segments.

![figy](images/Image%20052.png)

In the above instance, the user wanted to adjust the first drop, and left-cliked on it. The Auto-Locator moves to an invalid station reading. This is often the case when working with short length segments, common to the first segment of all distributary canals.

Upon clicking (to accept the new location), the *Invalid Input* dialog appears, with recommendation to change values in *CBL_designSettings*. The corresponding setting for this particular instance are as follows:

![figy2](Images/Image%20053.png)

It can be seen that, the drop can only be located before the first control when attempting to maintain *Min. Control Spacing* settings. This is because, the set minimum control spacing of 15 meters can not be achieved in the current segment. Note the distance between the contols is 17m. To accomodate a drop, a segment length of 25m (5+15+5) is required, that is not available.

There are two ways to resolve this issue: 

(1) Increase the segment length available: this must be avoided, because it entials chaning the layout design to create more space between the controls.

(2). Change the allowbale minimum distance between controls (as shown in row 4 of above figure.) Changing the first value to 2.5m for instance (i.e, dictating to observe only 2.5meters between controls) allows to re-position the drop feasibly in the segment range.

![figy3](Images/Image%20054.png)

> Note: The minimum acceptable spacing between structures is sligthly greater than 5.0meters. In line with this, it is strongly recommended that the available distance between any two controls in the network is at least 20meters.

## Provide predefined list of drops
[Back to Top](#)

Once can also override the entire list of drop heights and their stations in a canal segment, to replace with own predefined list. This may be particularly helpful when modeling existing projects.

To do this:

1. Right click on any one drop of the desired segment, and choose `Edit Segment Drops...`. This will invoke the drop adjust dialog.
   
   ![figkk](Images/Image%20055.png)

2. Input the drop heights in the first row, and thier stations in the second row. 

3. Hit `Apply` when done.

This will create a new CBLinformation for the segment that accomodates the prescribed drop heights and locations.

> Note: The invert of the control at the downstream end of the segment will adjust automatically to a corresponding elevation.

> Note: There are no limits to the size of the data length to be provided for such prescrptions. However, both the height and locaiotn data must be of the same length, and respect the data input expectations. Otherwise, the action will not take effect.


[Back to Top](#)