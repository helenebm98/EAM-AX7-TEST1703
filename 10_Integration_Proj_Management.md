# Integration to Project Management and Accounting

Objects in the **Enterprise asset management** module can be related to a project. A project related to an object is called an object project. Using an object project means that all work order projects, which are related to the object, will be created as sub projects to the object project. Sub projects may have different project types compared to the parent project, meaning that it is possible to have projects of type "Internal", "Time and Material", or "Investment" related to the same object project.


### Objects and Projects

Object projects can be set up on the objects manually in **Enterprise asset management** > **Common** > **Objects** > **All Objects** > select object > **Edit** button > **Project** FastTab > **Project ID** field. An object project can also be created automatically, either when the object is created, or manually by using the "Create project integration" function (**Enterprise asset management** > **Common** > **Objects** > **All Objects** > select object > **Edit** button > **Project** FastTab > **Create project integration** button). If you want object projects to be created automatically when creating objects, select the **Auto create projects** check box option in the **Enterprise asset management parameters** detail view (**Enterprise asset management** > **Setup** > **Enterprise asset management parameters** > **Objects** link > **Auto create projects** check box).


#### Top Level Objects

You can create object projects for objects without a parent project, also called top level objects. This means that for the top level object, the project created will be a sub-project to the main object project set up in **Enterprise asset management parameters** (**Enterprise asset management** > **Setup** > **Enterprise asset management parameters** > **Objects** link > **Main project** field). Project type and other related settings will be inherited from the parent project.



#### Sub-projects

In **Enterprise asset management parameters** > **Objects** link > **Project hierarchy** field, the parent project when creating object projects for sub objects is determined. If "No hierarchy" is selected, the parent project will be the main project setup in parameters, same as top-level objects. If "Hierarchy" is selected, the parent project will be the object project set up on the parent object. With the "Hierarchy" option, the project structure will be identical to the object structure. If using "Hierarchy", it is recommended that you expand length of the project ID data type, as you can easily exceed the 20 characters allocated.



#### Project Format

The project format for object projects is set up in **Enterprise asset management**  > **Setup** > **Enterprise asset management parameters** > **Objects** link > **Work order project mask** field. This format determines how many sub projects an object project can have, meaning how many work orders can be related to the object. If the "Hierarchy" option is used, the setup in the **Work order project mask** field determines how many sub objects and work orders can be related to an object.


---


### Projects, Sub Projects, and Project Activities for Objects

Objects and work order lines that are created in the **Enterprise asset management** module are created in the **Project management and accounting** module as projects, sub projects, and project activities.

In the **Project management and accounting** module, you set up the main project to be used for **Enterprise Asset Management**. In **Enterprise asset management** > **Setup** > **Enterprise asset management parameters** > **Objects** link > **Main project** field, you select the primary maintenance project, and once that parameter is set up, there is full integration with the project module (see also the figure below showing relations between **Enterprise asset management parameters** and **All projects**).

###### NOTE
Regarding object data setup: If you want to build an object / project structure based on location (or another classification), you create an object as a location, and the sub-objects you create will then become sub-locations (or another classification type that you have selected).

Object projects may be useful if your company manages large, specialized projects, for example, construction projects for a bridge or a large piece of production equipment. In the figure below, you will see a graphic overview of object integration with the **Project management and accounting** module if you have decided to use the project hierarchy.


![Figure 10-01](/Figures/10-01_ObjectAndProject_withHierarchy_004_AX7.png)


In the figure below, you will see a graphic overview of object integration with the **Project management and accounting** module if you have decided not to use the project hierarchy.


![Figure 10-02](/Figures/10-02_ObjectAndProject_NoHierarchy_Graphic_AX7.png)


The two figures below show the relation between the setup in **Enterprise asset management parameters** (**Enterprise asset management** > **Setup** > **Enterprise asset management parameters**), an object created as a sub-object, which is displayed in **All objects** (**Enterprise asset management** > **Common** > **Objects** > **All Objects** > select object in the list), and the related object project in **All projects** (**Project management and accounting** > **Projects** > **All projects** > select project in the list > **Edit**).


![Figure 10-03](/Figures/10-03_ProjMan_AllProjects_and_EAM_Param_AX7-002.png)


###### NOTE
In **Enterprise asset management parameters** displayed above, the **Auto create projects** check box defines how projects are created. If the check box is selected, an object project is automatically created on a new object. If the **Auto create projects** check box is cleared, the user must manually create project integration when the object is created. This is done in **All objects** > **Project** FastTab. Select the **Create project integration** button if you want to manually create a project for the object.


![Figure 10-04](/Figures/10-04_AllObjects_List_MultiLevel_AX7-01A.png)


---


### Forecasts, Work Orders, and Projects

In Enterprise Asset Management, integration to the **Project management and accounting** module is done to optimize cost control, allowing users to track costs on job type forecasts and work order lines.job type forecasts, work order lines, and customers (regarding service jobs).

To track job type forecasts, two settings must be made:

1. In **Enterprise asset management parameters**, select a project in the **Forecast project** field (**Enterprise asset management** > **Setup** > **Enterprise asset management parameters** > **Objects** link > **Project** FastTab > **Forecast project** field).

2. In **Job type setup**, when you create a job type setup line, an activity number is automatically created for the line (**Enterprise asset management** > **Setup** > **Work orders** > **Jobs** > **Job type setup**).

Job type forecasts serve two purposes: You are able to track costs on job type forecasts in the **Project management and accounting** module. Furthermore, forecasts are automatically transferred to a work order line project when you select a job type on a work order line.

To track costs on work order lines, you must first set up work order projects. Refer to the [Work Order Project Setup](08_Work_Orders.md#work-order-project-setup) section for a description of the procedure.


---


#### Work Order Line Projects

When you create a work order line on a work order, and the object selected on the work order line is not related to an object project, the work order project is determined by the setup of the parent project for work orders in **Work order project setup** (**Enterprise asset management** > **Setup** > **Work order** > **Project setup**).

Work order line projects are created by using a combination of the following work order information:

- The Customer account selected on the work order
- The Work order type selected on the work order

- The Object type related to the object on the work order line
- The Expected start and end time set on the work order

It is possible that not all of the information types mentioned above are found on a work order. Therefore, the search for a work order parent project is done by using a combination of the information types and selecting the project ID for the combination that corresponds with work order data:

1. Customer account, Work order type, Object type, and Expected start and end time
2. Customer account, Object type, and Expected start and end time

3. Customer account and Expected start and end time
4. Work order type, Object type, and Expected start and end time

5. Object type, and Expected start and end time
6. Expected start and end time


Example: In the figure below, the setup of customer account "US-027" means that every work order line created for that customer account will be a sub project of Project ID "000190", found by using the combination shown in step 3. above.


![Figure 10-05](/Figures/10-05_WO_ProjectSetup_Form_ParProj_ASM_AX7-01A.png)


The purpose of the project ID on the work order line, and the related activity number (**Enterprise asset management** > **Common** > **Work orders** > **All Work orders** > select work order in list > **Edit** button > **Line details** FastTab > **Project ID** field and **Activity number** field), is to track costs related to the work order line (and the object selected on the work order line) in the **Project management and accounting** module. Read more about cost control in Enterprise Asset Management in the [Cost and Date Control](20_ControllingAndReporting.md#cost-and-date-control) section.

In the figure below, you will see a graphic overview of work order projects and related project activities.


![Figure 10-06](/Figures/10-06_ObjectAndProject_WorkOrderProjects_AX7-01.png)


###### NOTE
When a new work line is created on a work order, a work order project is automatically created for the line. The financial dimensions for the object related to the work order line are automatically transferred to the work order project. The project activity created for a work order line has related information attached to it regarding job type, variant, and trade. Those data are useful if, for example, you create a purchase order from a work order (see the [Procurement](08_Work_Orders.md#procurement) section), or if you use the **Project management and accounting** module for time registration.
If the object was installed on a functional location, and that object is later installed on another functional location, the financial dimensions related to the new functional location is automatically updated on the object. Subsequently, when you create a work order line for the object, the work order project for the work order line automatically gets the financial dimensions that are now related to the object. This means that when you use functional locations, costs can always be tracked on the functional locations on which an object was installed at any given time. The automatic update of financial dimensions ensures complete traceability of costs when carrying out project controlling and reporting.

---

**Object Projects:**
It is optional if you want to make a project relation to an object when you create the object. Setup regarding object-project relations is done in **Enterprise asset management parameters** > **Objects** link > **Project** FastTab. It may be useful to use object projects for large construction projects for continuous project, cost, and lifecycle management.

---

**Work Order Projects:**
A work order must always have a project relation. If the object selected on the work order has a project relation, the object project is used. If the object does not have a project relation, a work order project is created based on the setup in **Work order project setup**. Work order projects with no related object projects may be useful for maintenance and repair jobs related to discrete or process production equipment.

Whether your company chooses to use object project setup or work order project setup, or a combination, depends on the company's focus on construction or maintenance as well as the requirements for cost management and reporting. In the figure below, you will see an example of the different phases in a construction project, and how you can use both object projects and work order projects in the different phases.


![Figure 10-07](/Figures/10-07_ConstructionProject_Example_Boiler_AX7.png)


---

### Work Order Projects, Work Order Stages, Project Stages, and Project Types

To ensure correct use of work order stages, and related project stages, on work orders, consider the dependencies in relation to the **Project management and accounting** module:

- In the **Project management and accounting** module, project stages are set up on project types in the **roject management and accounting parameters** form.

- In the **Project management and accounting parameters** form, remember to select relevant project stage check boxes for all the project types you are going to use. In the figure below, five stages Created - Estimated - Scheduled - In process - Finished have been selected for the project types "Time and material" and "Internal". Those five stages are relevant for both internal maintenance and service maintenance jobs.

- In Enterprise Asset Management, project types are defined by the project groups you set up in the Work order project setup form > Project group link.

- The project groups set up in the Work order project setup form are used when you create work orders.

- When a work order is created, a work order project is automatically created for the work order, according to the setup in the Work order project setup form.

- Work order stages must each have a related project stage.

- The project stage related to a work order stage must be defined as an active stage for the project group defined in the work order project, which is automatically created on a work order.

- The automatic allocation of a work order project, when you create a new work order, is based on the setup in the Work order project setup form.

Associations between work order project groups, related project types, project stages, and work order stages are shown in the figure below.


![Figure 10-08](/Figures/10-08_Proj_Integration_WO_ProjectSetup_AX7-01.png)


![Figure 10-09](/Figures/10-09_Proj_Integration_ProjectManParameters_Form_AX7-03.png)


![Figure 10-10](/Figures/10-10_Proj_Integration_WOStages_Form_AX7-03.png)


Refer to the [Work Order Project Setup](08_Work_Orders.md#work-order-project-setup) section regarding how to set up work order projects, and the [Work Order Stages](08_Work_Orders.md#work-order-stages) section regarding how to create work order stages.

The figure below shows a graphic overview of the various projects that are created in the **Enterprise asset management** module to allow integration with the **Project management and accounting** module, and the work processes to which the projects are related.


![Figure 10-11](/Figures/10-11_Proj_Integration_FlowDiagram_ASM_AX7.png)


---


### Customers and Projects

If a work order is related to a customer, a project contract ID is automatically created on the work order line (**Enterprise asset management** > **Common** > **Work orders** > **All Work orders** > select work order in the list > **Edit** button > **Header view** button  > **Project** FastTab > **Project contract ID** field). The project contract ID is used for invoicing. Invoices are sent to the customers based on posted transactions on work order line projects (as well as contract and warranty agreements that may be related to the customer).


![Figure 10-12](/Figures/10-12_WO_Form_ProjectContractID_field_AX7-02.png)


Refer to the [Invoicing](17_Invoicing.md#invoicing) chapter to learn more about invoicing. Refer to the [Warranty](18_Warranty.md#warranty), [Setup for Contracts](21_Setup_for_Contracts.md#setup-for-contracts), and [Create Contracts](22_Create_Contracts.md#create-contracts) chapters to learn more about warranty and contracts.

