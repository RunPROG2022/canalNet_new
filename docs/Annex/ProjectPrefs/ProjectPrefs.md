# Project Preferences

## Introduction
[Back to Home](../../index.md#wellcome)

Much of the work carried out by most processes in CanalNET is dictated by settings that are found in workspace variables called **Network Preferences**. They include settings for drawing elements, hydraulic calculations, quantity estimation as well as determine the visibilty and interaction with the interface.

This section introduces each of the setting parameters available, corresponding to the following major groups:

- [Project Preferences](#project-preferences)
  - [Introduction](#introduction)
  - [Network Preferences](#network-preferences)
  - [Node Graphic Template](#node-graphic-template)
  - [Control BoQ Settings](#control-boq-settings)


The variable set is accessible from `Workspace > Edit Preferences `

> **Note:** User specified settings for a given project, are saved along with other data to the project file data base, and are persistent across sessions - i.e., settings are remembered between sessions.




## Network Preferences

The settings under this group are used to determine key values that determine core network resolution, invert levels, and dimension settings for the project. They are applied and used at different stages of the project development.

> **Important Tip:** Do not focus on the *italics* settings, as they are less used (in advanced analysis).

| S.No. | Variable Name                    | Description                                                                                                                                                                                                                                         | Default Value |
|-------|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|
| 1     | Parent Canal Invert (m)          | Desired invert level of the primary level canal.                                                                                                                                                              | -0.8          |
| 2     | *Farm Duty (l/sec/ha)*            | Designed duty for the farm area. Overridden by settings in the design criteria. In latest releases (Version 1.5), this variable can be set to 0 to force node invert location to always meet downgrade conditions with respect to upstream nodes. | 1.2           |
| 3     | Node Invert Levels (m)           | Default invert levels for positioning nodes (or controls) defined relative to OGL at location.                                                                                                                | -0.5          |
| 4     |*Max. Tolerance to compare FSL (m*)*| Maximum tolerance value to be used in comparing FSL values, especially used in flow test tasks. Please refer to relevant material on flow test tool.                                                          | 0.005         |
| 5     |*Max. Distance b/n Merge Nodes (m)*| Any nodes found within this distance range are merged together and treated as one node.                                                                                                                       | 5             |
| 6     |*Control Branch Invert (-)*        | 0: Lock with Node – branch invert is set to parent invert or hydraulically determined level, whichever is minimum; 1: Free from Node – branch invert is fixed based on hydraulic calculations regardless of parent invert level. | 1             |
| 7     | *Associated Canal on Import (-)*   | Import associated canal flow section on each route during import. Applicable only in older versions.                                                                                                          | 0             |
| 8     | Route Extension Length (m)       | Extension length for beginning of routes, while attempting to establish intersection with other canals. Used to create buffer zone around canal routes to locate intersecting routes.                         | 2             |
| 9     |*Extrapolate Profile Data (-)*     | Allow or deny extrapolation of transverse profile data beyond the limits of the offset range, if needed.                                                                                                      | 1             |
| 10    | Round Dims for Construction (-)  | Rounding value for bottom width of canal flow sections, and drop provision. Value ≥ 0.05 rounds B values to value specified; drop heights applied will be limited to allowable increments specified.      | 0             |

## Node Graphic Template

Node graphic settings serve as a template to control the display and sizing of information on various the main interface - such as nodes, texts and symbols.

| S.No. | Variable Name                    | Description                                                                                          | Default Value |
|-------|----------------------------------|------------------------------------------------------------------------------------------------------|---------------|
| 1     | Display Height of Node bar (m)   | Height of nodes or control markers in the profile view area.                                         | 2.5           |
| 2     |*In-Route Node Marker symbol (-)* | Marker to be used for representing junction nodes.                                                   | o (Circle)            |
| 3     | *Max. Marker Size for Nodes (pts)* | Largest size of markers in layout view area.                                                         | 15            |
| 4     |*Min. Marker Size for Nodes (pts)*| Smallest size of markers.                                                                            | 10            |
| 5     |*End-of-Canal Marker symbol (-)*  | Marker to be used for representing End-of-Canal markers.                                             | s (Square)            |
| 6     | Marker Size for EOC (pts)        | Size of EoC markers.                                                                                 | 10            |
| 7     |*Available Head Margin (%)*       | Percent of flow head to be considered during flow test tasks, when determining available heads.       | 1             |
| 8     | Text Font Height (-)             | Font height to be used in display of text information in graphic display areas of the main interface. | 10            |
| 9     | Color template (-)               | Color template to be used in creation of profile, plan and section details. Also used in AutoCAD.     | Default       |


> **Note:** The *italics* parameters are less frequently changed/used.


## Control BoQ Settings

The settings in this group control how quantity estimation algorithms function, and allow user preferences to be built in to project data.


| S.No. | Variable Name                    | Description                                                                                          | Default Value |
|-------|----------------------------------|------------------------------------------------------------------------------------------------------|---------------|
| 1     | B/H ratio (wall)                 | Ratio of width to height of vertical structures (e.g., drop falls), used in calculating concrete/masonry volume. | 0.65          |
| 2     | Excavation cut slope             | Cut slopes to be assumed for controls (turnouts, division boxes) and drops, when determining excavation volumes. | 0.25          |
| 3     | Working space (m)                | Amount of working space to consider in volume calculations for above.                                 | 0.3           |
| 4     | Compacted fill Ht (m)            | Height of compacted fill to be considered in determining both cut and fill volumes for above.         | 0.1           |
| 5     | Consider Structure Reaches (-)   | Option to exclude earth volumes of structure locations when calculating canal volumes. Yes: Exclude volumes; No: Do not consider structures. | Yes           |
| 6     | BoQ List of Items (-)            | Level of detail desired for BoQ report generation: either detailed (default) or summarized.           | Detailed      |

> **Note**: Invert levels -0.5 denotes, to use the OGL level at the begining of the canal less 0.5m. It is defined relative to the OGL at the point of interest.

> **Note**: Bottom width roundup value also forces minimum allowable width to 0.30m.

[Back to Top](#)