# Functional Locations

Functional locations are elements of a technical structure, for example, functional units within a system. Functional locations are created hierarchically, and you install objects on functional locations. The setup of functional locations in your company depend on company requirements. Here are examples of how you can use functional locations:

- Functional (user-oriented, manage objects with similar behavior)

- Process-related (work flow-oriented)

- Spatial (geographical locations, sites)

Each functional location is managed independently in Enterprise Asset Management. Useful features and information extracted from functional locations include:

- Set up object specification requirements

- Set up maintenance sequences for preventive and reactive maintenance

- Manage installed objects

- Track active requests and work orders related to installed objects

- Track faults registered on objects

- Track maintenance costs on objects related to a functional location at any given time

Functional locations provide traceability of objects in relation to requests, work orders, fault registrations, condition assessments, production stop registrations, and object counter registrations.

---
###### NOTE

Even if an object is installed on different functional locations during its lifetime, the costs can be related to each different location. This means that object costs are always related to the functional location on which the object was installed at a given time.

Functional locations are ++not++ flexible, meaning that once you have set up a functional location hierarchy, you cannot move locations around in the hierarchy. When you have created a functional location hierarchy, the next step is to install objects in the hierarchy. This procedure is described in the [Install Objects on Functional Locations](#install-objects-on-functional-locations) section.

---

### Functional Location Stages

Functional location stages define the stages that a functional location can go through, for example, created, active, and ended. You are able to view all functional locations, regardless of their stage, in the **All functional locations** list page. You can change the stage of a functional location by selecting it in the **All functional locations** list page and clicking the **Functional location stage** button.

---

#### Set Up Functional Location Stages

1. Click **Enterprise asset management** > **Setup** > **Functional locations** > **Stage** > **Stages**.
2. Click **New** to create a new functional location stage.

3. Insert the stage ID in the **Stage** field and a name for the functional location stage in the **Name** field. In the **Stage groups** field, you can see the number of functional location stage groups that uses the functional location stage.
4. On the **General** FastTab, select the **Active** check box if the functional location should be active at this stage.

5. Select the **Create object** check box if it should be possible to automatically create an object with the same name as the functional location and install it on the functional location at this stage.
   ###### NOTE
   This check box relates to the **Object type** field on the **General** FastTab in the **Functional location types** form (**Enterprise asset management** > **Setup** > **Functional locations** > **Functional location types**).

6. Select the **Rename location** check box if it should be possible to change the name of the functional location at this stage.
7. Select the **New sub locations** check box if it should be possible to add new sub locations to the functional location at this stage.

8. Select the **Install objects** check box if it should be possible to install objects on the functional location at this stage.

9. Select the **Delete functional locations** check box if it should be possible to delete the functional location at this stage.
10. Select an object stage in the **Reference** field if you want the object stage for all objects installed on the functional location to be automatically updated at this stage. Example: If you close down a functional location, and set the functional location stage to "Ended", you may want to automatically change the object stage of the objects installed on that functional location to "Not in use".


![Figure 5-01](/Figures/05-01_FuncLocationStages_Form_AX7-01.png)


---

###### NOTE
Functional location stages, stage groups, and types are related and used in the same way as work order stages, work order stage groups, and work order types. Refer to the [Work Order Stages](08_Work_Orders.md#work-order-stages) section for a general explanation regarding stage group, type, and stage relations.

---

#### Set up Functional Location Stage Groups

When you have created the stages required for your requests, they can be divided into groups. This is done to create the stage group flow that may be used for different types of requests. As a minimum, one standard request stage group should be created.

1. Click **Enterprise asset management** > **Setup** > **Functional locations** > **Stage** > **Stage groups**.
   
2. Click **New** to create a new stage group.
3. Insert the stage group ID in the **Stage group** field and a name for the stage group in the **Name** field.In the **Stages** and **Functional location types** fields, you can see the number of stages selected in the stage group, and the number of functional location types that uses the stage group.
   
4. On the **Stages** FastTab, select the stages that should be included in the group. This is done by clicking on a stage in the **Stages remaining** section and clicking the ![Figure 5-02](/Figures/05-02_Button_Select_StageGroups.png) button.
5. If you want to select all the available stages for a group, click the ![Figure 5-03](/Figures/05-03_Button_SelectAll_StageGroups.png) button. All stages are transferred to the Stages selected section.
6. If you want to remove a selected stage from the group, select the stage in the **Stages selected** section and click the ![Figure 5-04](/Figures/05-04_Button_Deselect_StageGroups.png) button.
   
7. Click **Stage updates** to define which stages can follow a selected stage.


![Figure 5-05](/Figures/05-05_FuncLocationStageGroups_Form_AX7.png)


---

#### Functional Location Types

Functional location types are used to manage how objects are installed on a functional location. You can also set up object types, maintenance sequences, and specification requirements to be used on a functional location that uses the specific functional location type. When you create a functional location, the functional location type is mandatory.

###### NOTE
In order to work with functional locations, you must create a default functional location to be used only for the purpose of creating new objects. For that default functional location, you should create a default functional location type that is really simple and allows multiple objects to be installed on the default functional location. See the Create Functional Locations section for more information on how to set up functional locations.

---

#### Create a Default Functional Location Type

This procedure shows how to create a default functional location type to be used for a default functional location.

1. Click **Enterprise asset management** > **Setup** > **Functional locations** > **Functional location types**.
   
2. Click **New** to create a functional location type.
3. Insert a functional location type ID in the **Functional location type** field, for example, "Default", and a name in the **Name** field.
4. Select a stage group in the **Functional location stage group** field.
   
5. Select the **Multiple objects** check box to allow more objects to be installed on a functional location (the default functional location) using this type.

Now, the default functional location type to be used only on a default functional location is created. You should not add any more requirements or restrictions to this default functional location type.


![Figure 5-06](/Figures/05-06_FuncLocationTypes_Default_Form_AX7-01.png)


---

#### Create Functional Location Types

1. Click **Enterprise asset management** > **Setup** > **Functional locations** > **Functional location types**.
   
2. Click **New** to create a functional location type.
3. Insert a functional location type ID in the **Functional location type** field and a name in the **Name** field.
4. Select a stage group in the **Functional location stage group** field. Refer to the [Functional Location Stages](#functional-location-stages) section for more information on functional location stages and stage groups.
   
5. Select the **Multiple objects** check box if it should be possible to install more than one object on the functional location.
6. Select the **Update object dimension** check box if you want objects installed on a functional location of this type to automatically use the financial dimensions related to the functional location. This means that if you change financial dimensions in the **Functional location** detail view, and the functional location uses a functional location type with this check box selected, financial dimensions are automatically updated on all objects installed on that functional location.
   
7. The **Object type** field is used if you want to automatically create one object for the functional location with the same ID and name as the functional location you are creating. For example, this may be relevant if you create a static functional location, such as a building or a pipeline. In that case, select the object type you want to use for the automatically created object. Remember that if you make a selection in this field, the **Multiple objects** check box must be cleared.
8. On the **Object types** FastTab, select the object types to be related to the functional location type. Click **Add line** and select the object types. If you add object types here, only objects using those object types can be installed on a functional location using this functional location type. If no object types are selected on the **Object types** FastTab, all object types may be installed.
   
9. On the **Maintenance sequences** FastTab, select the maintenance sequences that should automatically be set up on new functional locations using this functional location type. Click **Add line** and select the sequences. If you add maintenance sequences here, only those sequences can be used on a functional location using this functional location type.
10. On the **Object specification requirements** FastTab, set up specification requirements to be related to the functional location type. Click **Add line** and select the requirements for the line. These specification requirements function as guidelines. They are not validated against specifications set up on an object (**Enterprise asset management** > **Common** > **Objects** > **All objects** > select object in the list > **General** tab > **Specifications** button). The specification requirements are shown when you install objects on functional locations.
   
11. On the **Permitted types** FastTab, select the functional location types that should be valid for the sub functional location types related to a parent functional location type, which uses the selected functional location type. In the figure below, you see that a parent functional location using the type "City" allows the functional location types "Site", "Plant", and "Warehouse" as related sub functional locations.



![Figure 5-07](/Figures/05-07_FuncLocationTypes_Form_AX7-01.png)


###### NOTE

In the **Details** section at the top of the form, you can get an overview of the number of object types, maintenance sequences, specification requirements, and permitted functional location types set up on the functional location type. The **Functional locations** field shows the number of functional locations that use the functional location type.

You can use the **Copy** button to copy settings from a functional location type to the selected functional location type.


### Introduction to Functional Locations

Click **Enterprise asset management** > **Common** > **Functional locations** > **All functional locations** to open the list. The **All functional locations** list contains all functional locations and displays some of the information related to a functional location. You can also select **Active functional locations** to see a list of all active functional locations, or **My active functional locations** to see a list of the functional locations you are related to as a worker (set up in [Workers and Worker Groups](06_Objects.md#workers-and-worker-groups)).


![Figure 5-08](/Figures/05-08_AllFunctionalLocations_List_AX7-01.png)


In the **All functional locations** list, click on a link in the **Functional location** column to show the Details view of the selected record. Click the **Edit** button to open the location for editing. In the details view, you will see detailed information related to the location as well as a Fact Box to the right of the screen, displaying the functional location hierarchy. Click on the blue 'left arrow' / 'right arrow' button in the small blue box placed above the Fact Box to show or hide the Fact Box.


![Figure 5-09](/Figures/05-09_FunctionalLocation_DetailsView_AX7-001.png)


The action pane buttons are organized in tabs on the action pane. Here is a brief description of the buttons relating to Enterprise Asset Management:

| Button name | Description |
|--------|--------|
|Edit                  |Toggle button to switch between edit mode and view mode in the form.        |
|New                   |Create new functional location.        |
|Delete                |Delete the selected functional location.        |
|Rename                |Rename the selected functional location.        |
|Copy functional location        |Copy functional location hierarchy.        |
|Install object        |Install object including child objects on the functional location.        |
|Replace object        |Replace object hierarchy with another object hierarchy on the functional location.        |
|Cost control          |Open **Functional location cost control** to make a cost calculation for the selected functional locations.        |
|Objects               |Open **All objects** to see a list of objects related to the selected functional location.        |
|Requests              |Open **Active requests** to see a list of requests related to the selected functional location.        |
|Work orders           |Open **Active work orders** to see a list of work orders related to the selected functional location.        |
|Faults                |Open **Object faults** to see a list of object fault registrations related to the selected functional location.        |
|Functional location stage        |Update the stage of the selected functional location.        |
|Stage log             |Log displaying the stages of the selected functional location.        |



### Create Functional Locations

When you create a functional location hierarchy, be aware once you have created a functional location, you cannot move it from the original location. This means that you should carefully consider the structure of your functional locations before you start creating them in Enterprise Asset Management. If you regret a functional location, you can delete it, provided that it has not yet been taken into use.

To be able to work with functional locations, you start by creating two "categories" of functional locations:

- Create ++one++ default functional location with not sub locations. This functional location is used only as the standard location for objects when you create new objects.
- Create the functional location hierarchies required for managing maintenance and service jobs in your company.

---

#### Create a Default Functional Location

When you use functional locations, start by creating one default location to be used when you create new objects. This functional location is the one you select in **Enterprise asset management** > **Setup** > **Enterprise asset management parameters** > **Objects** link > **Default functional location** field. The default functional location can be used when you create new objects, and you have not yet set up a functional location hierarchy for those objects.

1. Click **Enterprise asset management** > **Common** > **Functional locations** > **All Functional locations**.
2. In **All functional locations**, click **New**.
   
3. Insert an ID in the **Functional location** field, for example, "0000" or "Default", to indicate that this is a special functional location.
4. Insert name for the default functional location in the **Name** field.
   
5. Do ++not++ select a parent in the **Parent** field - leave this field blank.
6. In the **Functional location type** field, select the functional location type to be used for the default functional location. See the [Functional Location Types](#functional-location-types) section for more information on how to set up functional location types.
   
7. Click **OK**. You should not add further data to this functional location as it is only used as a temporary location for new objects until you install the objects on the functional locations used by your company.

The figure below shows an example of a default functional location. No requirements regarding object specifications or maintenance sequences have been added to this location. The location does not have any sub locations, and no financial dimensions are used on the functional location.


![Figure 5-10](/Figures/05-10_FunctionalLocation_Default_DetailsView_AX7-01.png)


---

#### Create Functional Locations

The following procedure describes how you create the functional locations required for maintenance managementservice management in your company.


1. Click **Enterprise asset management** > **Common** > **Functional locations** > **All Functional locations**. You can create a functional location from grid view or details view.
2. Click the **New** button.
   
3. Insert an ID in the **Functional location** field.
4. Insert a name for the functional location in the **Name** field.
   
5. If the functional location is a sub location in a hierarchy, select the parent location in the **Parent** field.
6. Select a type in the **Functional location type** field.
   
7. Click **OK**.
8. Select the functional location and click the **Edit** button to add further information.

###### NOTE

Depending on your setup of functional location stages, you may have to create all sub locations for a functional location, and then change the functional location stage before you can start installing objects. See the [Install Objects on Functional Locations](#install-objects-on-functional-locations) section for more information on object installation. See the [Functional Location Stages](#functional-location-stages) section to learn more about setup of functional location stages.

In Details view, you will see FastTabs on which you can add and edit information about the functional location.


---

#### General Information

This section provides an overview of parent and child information in the functional location hierarchy. In the **Details** section, you can see the number of object specification requirements, maintenance sequences, and objects related to the functional location. In the **Inventory** section, you can select the site and warehouse to which the functional location is related. Site and warehouse is used in connection with work order item forecasts. When creating an item forecast, site and warehouse information from the functional location of the object is automatically used. In the **Stage** section, information about the functional location stage is displayed.


---

#### Installed Objects


Refer to the [Install Objects on Functional Locations](#install-objects-on-functional-locations) section for more information on object installation. You can use the "View" button on this FastTab to show more fields on the FastTab. The **Effective** and **Sub object** fields can be shown in the grid.


---

#### Object Specification Requirements

On this FastTab you can add specific requirements for the objects that you install on the functional location. These requirements are for information purposes only. They do not prevent you from installing objects with other specification requirements. Click **Add line** and select the specification type. Then you insert the relevant **Value** and select a threshold in the **Threshold criteria** field.


---

#### Preventive Maintenance

Here you can add maintenance sequences and rounds to the functional location, including a start date. The objects installed on a functional location may have other maintenance sequences set up. All maintenance sequences and rounds can be used for scheduling object calendar entries for a functional location and its currently installed objects.


###### NOTE

If you update the setup of object types, products, and models on maintenance sequences in **All functional locations** detail view > **Preventive maintenance** FastTab after you have scheduled maintenance sequences, existing object calendar entries related to that functional location are automatically deleted. In order to create new calendar entries, which correspond with the updated maintenance sequence setup on the functional location, you must run a new maintenance sequence schedule for that functional location. Read more about maintenance sequence scheduling in the [Schedule Maintenance Sequences](11_Preventive_Reactive_Maint.md#schedule-maintenance-sequences) section.


---

#### Address

Insert the functional location address on the **Address** FastTab. Addresses on functional locations are inherited, meaning if a sub location has no address defined, the address of the parent location is used.


---

#### Workers

On this FastTab, you can add workers affiliated with the functional location, and you can select a functional location as primary for the worker. This information is used when a worker creates an operations log. The functional location, which is a primary location for the worker, is automatically selected when the worker creates a new operations log.


---

#### Financial Dimensions

You can select financial dimensions for the functional location. [Functional Location Types](#functional-location-types) can be set up to allow for automatic update of financial dimensions from a functional location. This means that objects installed on a financial dimension automatically get the financial dimensions for the functional location. This is useful if you want different cost centers, depending on locations.

![Figure 5-11](/Figures/05-11_FunctionalLocation_DetailsView_AX7-01A.png)

When data regarding **Site**, **Warehouse**, **Address**, and **Financial dimensions** are updated on a parent functional location, the related sub functional locations can be updated accordingly if you make that selection during the update. A dialog opens providing you with the following update scenarios:

![Figure 5-12](/Figures/05-12_UpdateSubFuncLocationsDialog_AX7.png)


---

#### Copy a Functional Location Hierarchy

If your company has several functional locations with similar location structures, you can use the copy function in Enterprise Asset Management to quickly create a number of similar location hierarchies. When you copy a specific functional location or an entire hierarchy, the new location or hierarchy has the same name as the one you copied. After the copy procedure is done, you can easily change the name or other settings on the new functional location, provided that the functional location stage selected for the new functional location allows it.

1. In **All functional locations**, select the functional location you want to copy. For example, you select a top location (parent) if you want to copy the entire functional location structure including sub locations.
2. Click the **Copy functional location** button. The location you selected in the list page is shown in the **Copy from** field.
   
3. Insert the name of the new location in the **New functional location** field.
4. In the **Parent** field, you should only insert a parent ID if the location you are creating should be part of an existing functional location hierarchy.
   
5. Click **OK**. The new functional location hierarchy is shown in **All functional locations**.

###### NOTE
When you copy a functional location structure, functional location stages in the new hierarchy are set to the "first stage" that you have created for functional locations. Whether you can rename or delete a functional location using the **Rename** and **Delete** buttons in **All functional locations**, depends on the current stage of the functional location.


---

#### Delete a Functional Location

A functional location with related sub locations can be deleted if no objects have been installed on any of the functional locations you are trying to delete, and if the current functional location stage allows it.

1. In **All Functional locations**, select the functional location you want to delete.
2. If required, update the functional location to a functional location stage that allows deletion of a functional location.
   
3. Click **Delete**.

###### NOTE
If you cannot delete a functional location, instead you can handle deletion by setting up a functional location stage for this purpose. For example, you can set up a "Scrapped" or "Deleted" stage, which should not be an active stage, in the **Functional location stages** form.


---

### Install Objects on Functional Locations

When you have created functional location hierarchies, next step is to install objects on the relevant functional location. Refer to the [Objects](06_Objects.md#objects) chapter for more information on how to create objects.

If you have created an object hierarchy, the entire hierarchy must be installed on a functional location. This means that only top-level objects (objects without a current parent object) can be selected on a functional location, and all related sub objects will be included in the installation on the functional location. When you install objects on a functional location, the financial dimensions of the functional location may be automatically transferred to the object, depending on the setup on the functional location type selected on the functional location. See the [Functional Location Types](#functional-location-types) section for more information on how to set up functional location types.


###### NOTE
You can set up object types on a functional location type. If a functional location uses a functional location type that has object types related to it, then, when you install object on the functional location, only parent objects with a similar object type is shown in the list of possible objects to be installed on the functional location.

---

After you have installed objects on a functional location, you can replace a parent object or an object hierarchy, if required. Just as with installation of objects, you select a parent object to be replaced, and all related child objects will also be replaced. Read more about how to replace objects on a functional location at the end of this section.

#### Install an Object Hierarchy on a Functional Location

1. Click **Enterprise asset management** > **Common** > **Functional locations** > **All Functional locations** or **Active functional locations**.
2. Select the functional location on which you want to install an object.
   
3. Click the **Install object** button. In the **Specifications** section, you will see a list of the object specifications requirements set up on the functional location type used on the functional location. The specifications are for your information. The system does not validate the specifications against the **Object specifications** that may be set up on the object you select. You must carry out that validation after you have selected an object in the **Object** field.
![Figure 5-13](/Figures/05-13_InstallObject_On_FuncLocation_AX7-001.png)

4. In the **Object** field, select the parent object you want to install. All related child objects are automatically included in the installation. In the **Object specifications section** to the right of the object list, you will see the object specifications related to the selected object.
   ![Figure 5-14](/Figures/05-14_InstallObject_On_FuncLocation_SelectObject_AX7-001.png)
5. In the **Effective** field, select a date and time to indicate the start time of the object installation. From this date and time, costs regarding the object and related sub objects will be related to the functional location.
###### NOTE
The object specifications set up on the object have been added to the **Specifications** section. **Engine volume** and **Max Load** were added as requirements on the functional location, and because the object has requirements of the same type, the object requirements values have been added to the **Value** fields. This means that you can now validate the object values against the requirements set up on the functional location. The two requirements set up on the functional location are marked with a check mark. The third line regarding **Oil capacity** has been added as an object requirement. That line does not have a check mark because that is a requirement from the object, not a functional location requirement.
   ![Figure 5-15](/Figures/05-15_InstallObject_On_FuncLocation_SelectObject_AX7-01-01.png)
6. Click **OK**.
###### NOTE
If you want to change the installation of an object and install it on another functional location, the procedure is the same as described in steps 1-6 in this procedure. When you install the object on a new functional location, the object is automatically uninstalled from the previous functional location. Any active requests or work orders that may have been created on the object before you re-installed it on another functional location are ++not++ automatically transferred to new functional location. If required, you must manually re-create those requests and work orders for the object after re-installation on a new location.
   
7. If you want to see a list of all the objects, including sub objects, that are installed on the functional location, select the functional location in **All Functional locations**, and click the **Objects** button.
8. If you want to see a list of active requests, active work orders, or fault registrations related to the objects installed on a functional location, select the functional location in **All Functional locations**, and click the **Requests** or **Work orders** or **Faults** button.

###### NOTE
When object-related data are changed, those data are automatically updated on the functional location on which the object is installed. The automatic update relates to changes on requests, work orders, object fault registrations, production stop registrations, and object counter registrations.

---

#### Auto-Create One object on a Functional Location

It is possible to set up functional location stages and functional location types to handle automatic creation of ++one++ object on a functional location. The object gets the same ID and name as the functional location. This may be useful if you are handling maintenance on large, static objects, for example, a building.

Before you can auto-create an object on a functional location, the following setup data must be available:

- Create a functional location type in which you have selected an object type in the **Object type** field. Refer to the [Functional Location Types](#functional-location-types) section.

- Create a functional location stage that handles auto-creation of an object by selecting the **Create object** check box. Refer to the [Functional Location Stages](#functional-location-stages) section.

When the setup data are available, you are ready to create an object.

1. In **All Functional locations**, ensure that the functional location on which you want to auto-create the object uses the functional location type set up for handling auto-creation of an object.
2. Select the functional location in the list.
   
3. Click **Functional location stage** and select the stage you created for this purpose. One object is now automatically installed on the functional location. The object has the same name as the functional location.

