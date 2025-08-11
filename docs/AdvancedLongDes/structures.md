---
sidebar_position: 8
---

# Place holders for Special Structures
[Back to Home](../index.md#wellcome)

CanalNET has a number of built in structures which can be placed along any canal route. These include drops, turnouts, division boxes, Outfalls, Head and Cross Regulators, and more. If your version of the application does not have the structure you need to model your network, you can opt to put a place-holder. Using place holders, any hydraulic condition (headloss and span) can be modelled.

### Spot Space holders
[Back to Top](#)

To represent structures that do not have significant span, you can use one floating node. The floating node can have:
- Name
- Head Loss

![](Images/Image%20092.png)

*Fig: Example of a spot spaceholder for a simple structure, representing a headloss of 20cms along the Main Canal route*

### Span Space holders
[Back to Top](#)

If the strcture can take a significant span length, then two floating nodes can be used to represent it. The length between the two floating nodes is set as a special (X) segment. Such segments are not considered in BoQ, Plan and LSec generation.

![](Images/Image%20091.png)

*Fig: Example of a span spaceholder for a flume structure along a main canal rotue. Note, the X-Segment checkbox on the Node Control Setting Panel*

THe floating nodes can be labeled for annotation purposes, and rich drawing generation.

[Back to Top](#)