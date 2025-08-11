---
sidebar_position: 7
---

# Creating and Managing Design Criteria
[Back to Home](../../index.md#wellcome)

## Introduction

Establishing a set of design criteria is the basis of design work. These data are also the key input data for tackling the sizing and detailing of a network of canal system in CanalNETWORK. See Standard workflow in Introduction to see at which stage of project design this may be required. However, it is highly recommended to set a design criteria set as the first step in creating a project workspace. 

> **Note:** Design criteria can be edited at any stage of the design process. However, your changes may not have any impact until you have re-applied it by invoking other processes. Most variables are applied to the actual route data base during the network sizing stage, and reapplying newly modified design criteria requires invoking this task, risking the loss of all design works you have completed earlier. It is therefore, a strongly recommended practice to set the data set at the beginning and to try and maintain it thorough the project design process.

CanalNETWORK environment in the software offers tools to set and edit key criteria for design work, corresponding to each generation of canals. 

There are options for creating design criteria set for a given project. These are:

* Default Criteria set, found in software library
* Pre-created criteria file stored in *.dcf* file


## Default criteria set
[Back to Top](#)

This method very common among users. It brings forward the builtin default criteria set depending on the naming style of choice. Once the default criteria is loaded, one can always edit the contents to suit project conditions. To use the default criteria set:

1. Start an empty project from `Workspace > Clear Workspace` then selecting `All` for the confirmation dialog.

   Go to `Workspace > Manage Design Criteria > New Naming` to select a desired naming style for your network of canals.

   ![Naming Style Selection](Images/Image%20002.png)

   ![Naming Options](Images/Image%20003.png)

2. Click Yes on the *Get Design Criteria* dialog. This will copy the built-in default design criteria to the workspace.

   ![Get Criteria Dialog](Images/Image%20004.png)

3. To edit the criteria for each route to suit project conditions, go to `Workspace > Manage Design Criteria > Set/Edit Design Criteria`

4. In the *Pick Level* dialog, choose the desired canal level or generation to edit.

   ![Pick Level Dialog](Images/Image%20005.png)

5. Edit the parameters to your requirement and click on `Apply` to save changes to the workspace.

   ![Edit Parameters](Images/Image%20006.png)

   In recent release new variable sets are included to allow flexibility in the design of complex cut and fill shapes. See the section About Design Criteria for details.

6. Repeat the same for each generation of canal route.

## Saving Design Criteria to a File
[Back to Top](#)

To create a naming preference and design criteria for saving to a file:

1. Create and refine the design criteria set following the steps above for *Default Criteria Set*

2. Go to `Workspace > Manage Design Criteria > Edit Current Naming`

   ![Edit Naming](Images/Image%20011.png)

   Provide details for the *Next Action* variable group:

   ![Next Action Variables](Images/Image%20012.png)

   - In the *On Apply use for* variable, select *Save to File* option
   - In the *New Descriptive Label* insert a detail describing the criteria set

   ![Descriptive Label](Images/Image%20013.png)

   **Note:** If you see the *Can't Save!* dialog, clear your workspace and start over.

3. Hit Apply and provide a descriptive filename in the *Select File to Write* dialog.

   ![Save Dialog](Images/Image%20014.png)

## Import from a Pre-created Criteria File
[Back to Top](#)

To import criteria from an existing *.dcf* file:

1. Start CanalNETWORK or clear the workspace
2. Click on `Workspace > Manage Design Criteria > Import From File`

   ![Import Menu](Images/Image%20007.png)
   
   Confirm the replacement dialog:

   ![Replace Dialog](Images/Image%20020.png)

3. Select your file in the *Select File to Open* dialog:

   ![File Open Dialog](Images/Image%20008.png)

4. Review imported criteria in the success dialog:

   ![Success Dialog](Images/Image%20009.png)

5. Select levels to import in the field matching dialog:

   ![Field Selection](Images/Image%20021.png)

6. Confirm final import status:

   ![Import Status](Images/Image%20022.png)

## Important Notes
[Back to Top](#)

**Key considerations:**
- Design criteria and naming style must remain consistent
- Changing naming style after establishing criteria causes conflicts
- Imported criteria files must match existing naming structure

![Criteria Replacement](Images/Image%20016.png)

**Tip:** Always establish naming style before setting design criteria to avoid inconsistencies.

## Attempting to Solve Criteria Inconsistency
[Back to Top](#)

If inconsistencies occur:

1. Match naming style to existing criteria fields
2. Use either:
   - `Edit Current Naming`
   - `New Naming` with matching fields

**Note:** After resolving inconsistencies, save criteria to a new file for future use.

[Back to Top](#)
