# Work Orders

Work orders are used to manage, provide required information for, and register consumption on maintenance and service jobs. A work order may contain one or more work order lines, and one or more objects can be connected to a work order. Each work order line defines a maintenance or service job scheduled on the object.


---


### Job Groups and Job Types, Variants, and Trades

An object has an object type attached to it. The object type defines which job types, meaning which maintenanceservice jobs, can be carried out on an object. When you create a work order, selecting a job type is mandatory. It is only possible to select the job types that are related to the object type setup used on the object.

Refer to the [Introduction](01_Overview.md#introduction) chapter for a graphic outline of objects and job types, and their connection to a work order.

Job variants can be set up on a job type. Job variants define variations of a job type, for example, size (small, medium, large), periods (weekly, bi-weekly, 1 month, 3 months), and configurations (low standard, flexible, high performance).

Job trades are information regarding professional trade, for example, mechanical, electrical, and hydraulic. Competency requirements can be set up on a job trade. All job trades can be used in relation to all job types. Selecting job variant and/or job trade on work a order is optional.

For each job type, variations of job type setup can be created. Example: If you have a job type called "Service", you can create variations for that job type relating to "Trucks 30,000 km", "Cars 30,000 km", and "Vans 30,000 km".

Job groups are used to collect a group of job types for overview purposes. Examples could be "Calibration", "Inspection", "Overhaul", and "Instrumentation".

First, you set up the required job groups, job variants, and job trades. Next you create job types. Then, you create all the variations of job types that are required for your equipment in **Job type setup**. Forecasts, checklists, and tools can be set up for a combination of job type in **Job type setup**.


###### NOTE

A job type can only be related to one job group.


---


#### Create a Job Group


1. Click **Enterprise asset management** > **Setup** > **Work orders** > **Jobs** > **Job groups**.
2. Click **New**.

3. Insert a job group ID in the **Job group** field.
4. Insert a name for the group in the **Name** field.


When you have related job groups to job types, you will see how many job types are related to the job group in the **Job types** field.


![Figure 8-01](/Figures/08-01_JobGroups_Form_AX7-01.png)


---


#### Create a Job Variant


1. Click **Enterprise asset management** > **Setup** > **Work orders** > **Jobs** > **Job variants**.
2. Click **New**.

3. Insert the job variant ID in the **Variant** field and a description of the job variant in the **Description** field.
4. On the **Job types** FastTab, click **Add** to add a job type.

5. Select the job type in the **Job type** field.
6. Repeat steps 4-5 to add more job types to the variant. In the **Job types** field you can see the number of job types added to the selected job variant.


![Figure 8-02](/Figures/08-02_JobVariants_Form_AX7-01.png)


---


#### Create a Job Trade


1. Click **Enterprise asset management** > **Setup** > **Work orders** > **Jobs** > **Job trades**.
2. Click **New**.

3. Insert the job trade ID in the **Trade** field and a description of the job trade in the **Description** field.
4. On the **Competencies** FastTab > **Skills** tab, click **Add** to add a new skill to be related to the job trade.

5. Select the skill in the **Skill** field.
6. Select the skill level in the **Level** field.

7. Repeat steps 4-6 to add more skills to the job trade. In the **Skills** field you can see the number of skills added to the selected job trade.
8. Click the **Certificates** tab if you want to add certificates to the job trade.

9. Click **Add** to add a new certificate.
10. Select the certificate in the **Certificate type** field.

11. Repeat steps 9-10 to add more certificates to the job trade. In the **Certificates** field you can see the number of certificates added to the selected job trade.



![Figure 8-03](/Figures/08-03_JobTrades_Form_AX7-01.png)


---


#### Create a Job Type


1. Click **Enterprise asset management** > **Setup** > **Work orders** > **Jobs** > **Job types**.
2. Click **New**.

3. Insert a job type ID in the **Job type** field.
4. Insert a name for the job type in the **Name** field. In the **Details** group, you can see an overview of the number of job variants, skills, certificates, succeeding jobs, and object types created on the job type. In the **Setup lines** field, you see the number of job type setup lines set up on the job type. In the **Objects** field, you see the number of active objects that are currently using the job type.


5. On the **General** FastTab, select a job group in the Job group field.
6. Select the **Maintenance stop** check box if this job type requires a maintenance stop of the equipment before the job can be carried out.

7. On the **Description** FastTab, insert a description of the job type.
8. On the **Variants** FastTab, you can add job variants to the job type.

9. On the **Competencies** FastTab, you can add skills and certificate requirements to the job type.
10. If a specific job type is required as the next job type to be carried out, add it on the **Succeeding jobs** FastTab. You can also set up **Variant** and **Trade** related to the job type. In the **Displacement** field, you can add number of days that the succeeding job should start before or after the job using this job type has started. If you insert a positive number, for example "5", it means that the succeeding job starts five days after the start of the job that is related to the job type. If you insert a negative number, for example "-3", it means that the succeeding job will start three days before the scheduled start of the job that is related to the job type.
   ###### NOTE
   If you add more than one job type line, the sequence of the lines indicate the order in which they should be carried out, starting from the top of the list.

11. On the **Object types** FastTab, you can add object types to the job type.


![Figure 8-04](/Figures/08-04_JobTypes_Form_AX7-01.png)


---


#### Create Job Type Setup Lines and Related Forecasts, Checklists, Tools, Description, and Attachments


1. Click **Enterprise asset management** > **Setup** > **Work orders** > **Jobs** > **Job type setup** or **Enterprise asset management** > **Setup** > **Work orders** > **Jobs** > **Job types** > select a job type > **Job type setup** button.
2. Click **New**.

3. Depending on how specific the job type setup should be, make selections in the **Functional location**, **Object type**, **Product**, **Model**, and/or **Object** fields.
4. If a job type has not automatically been inserted, select a job type in the **Job type** field.

5. If required, select a job variant and a job trade in the **Variant** and **Trade** fields.
6. Click the **Forecast** button. In **Job type setup forecast**, you can make forecasts on hours, items, expenses, and fees.

7. Click **Add** on the relevant tabs and make your selections to create the required forecasts for the job type.
8. On the **Items** tab, you can select inventory dimensions to be shown on the item line. Select **Inventory** > **Dimensions**, select the dimensions you want to display, and the select the **Save setup** check box and click **OK**.

9. On the **Items** tab, click **Item where used** if you want to get an overview of where the item on the selected line is used in Enterprise Asset Management in relation to objects, job type setup, spare parts, and work orders. Read more about this overview in the [Items Where Used](20_ControllingAndReporting.md#items-where-used) section.
10. On the **Forecast totals** FastTab, you see an overview of forecast totals showing total number of hours and forecast lines created.
   ###### NOTE
   If you want to copy a forecast setup from another job type, select the **Copy forecast** button and select the job type from which to copy the setup.

11. Click **Save** to save your updates.
12. Close **Job type setup forecast**.

13. In **Job type setup**, click the **Checklist** button.
14. In **Job type setup checklist**, you can add checklists to the selected job type setup. The line numbers indicate the sequence of the checklists.

15. Select the **Worker mandatory** check box if if the worker working with the checklist must insert his or her name on the checklist line before it can be completed.
16. Select the **Date mandatory** check box, if the worker working with the checklist must insert the date of inspection on the checklist line before it can be completed.

17. Insert notes relating to the checklist on the **Notes** FastTab.
18. On the **Measuring points** FastTab, Add measurement lines, if relevant.
   ###### NOTE
   If you want to copy a checklist setup from another job type, select the **Copy checklist** button and select the job type from which to copy the setup.

19. Click **Save** to save your updates.
20. Close **Job type setup checklist**.

21. In **Job type setup**, click the **Tools** button.
22. In **Job type setup tools**, you can add the tools (resources) to be used for the job type. Select the tool in the **Resource** field.
   ###### NOTE
   If you want to copy a tool setup from another job type, select the **Copy tools** button and select the job type from which to copy the setup.

23. Click **Save** to save your updates.
24. Close **Job type setup tools**.

25. In **Job type setup**, click the **Description** button > **Edit**, and add a description related to the selected job type setup, if required.
26. Click **Save** to save the description.
   ###### NOTE
   If a description is added, that description overrules a description set up on the job type. If no description is added in this form, the description, if any, in **Job types** is used. Descriptions are automatically transferred to work orders using the job type or job type setup.

27. Close **Description**.
28. If you want to set up attachments on a selected job type setup line, click **Attach documents**. Attachments set up on a job type setup line will automatically be included on a work order line that uses that particular job type setup line.

29. Click the **New** button and select a document type.
30. Upload the document or file.

31. Fill out the **Attachments** form. This attachment setup uses standard **Dynamics 365 for Finance and Operations** document setup functionality.
32. Click **Save** to save the attachment.
   ###### NOTE
   Attachments on a job type setup line are only printed with a work order report if the document types of the attachments are selected in **Enterprise asset management** > **Setup** > **Enterprise asset management parameters** > **Document types**. Examples of attachments could be a guideline explaining how to complete a specific job, or a predefined checklist (if you do not use the checklist functionality for job type setup lines).

33. In **Job type setup**, you can see the number of forecasted hours as well as the number of setup lines created for items, expenses, fees, checklists, measuring points, and tools on each line. In the **Objects** field, you see the number of active objects related to the job type setup.
34. If you want to copy a job type setup to another job type setup, select the setup line to which you want to copy another setup, click **Copy setup**, and select a job type setup to copy.

35. If you want to see a list of the objects, maintenance sequences, or rounds that currently use a job type setup line, select the line and click **Used by**.


![Figure 8-05](/Figures/08-05_JobTypeSetup_Form_AX7-02.png)



When the system selects the available job type setup to be used on a work order line, the selection is based on the object and the related object type setup. Enterprise Asset Management goes through all job type setup records related to the job type, which is related to the object type, to check for a possible match, always checking the most specific combination first. This means that, first, a possible match regarding **Trade** is checked. If no match is found, **Variant** is checked. If no match is found, **Job type** is checked, and so on. As you can see in the layout of **Job type setup**, this means that Enterprise Asset Management checks each record from right to left for a match (**Trade**, then **Variant**, then **Job type**, **Object**, **Model**, **Product**, and **Object type** to find the most specific combination. If no match is found, the "default" record is used in which only the job type is selected.


###### NOTE
For each job type setup line you create, a project activity ID is automatically related to the line. The project activity is created on the forecast project selected in **Enterprise asset management parameters** > **Objects** link > **Forecast project** field. The purpose of the project activity is to manage forecasts on hours, items, expenses, and fees in relation to work orders. Job type forecasts are automatically transferred to the work order line, and they are copied from the forecast project to the work order project created for the work order line. The purpose of the project activity is to manage forecasts in relation to work orders.


---


#### Overview of Job Types Related to Objects

When you have created the required job type setup combinations, it is possible to get an overview of the current job type setup related to a specific object in **All Objects**. The overview shows a combination of all job type setup combinations that can be used on the object type selected on the object, including combinations with variations of job variants and job trades.


1. Click **Enterprise asset management** > **Common** > **Objects** > **All Objects** or **Active objects**.
2. In the list, select the object for which you want to see an overview of job type combinations.

3. On the **General** tab, click the **Job types** button.
4. In the left side of **Object job types**, you will see a list of all the job type combinations related to the selected object.

5. Select a job type combination to see the related setup for checklists, forecasts, and tools. At the top of the form, in the **Details** group, you will see number of related checklists, measurements, hours, and so on, that are related to the selected job type combination.
6. If you want to see details for the selected job type, click the **Job types** button.



![Figure 8-06](/Figures/08-06_ObjectJobTypes_Form_AX7-01.png)


---


#### Automatic Update of Job Type Forecasts

In Enterprise Asset Management, you can automatically update any changes in job type forecasts regarding hour costs, item costs, and expenses, which have been updated in other modules in Dynamics 365 for Finance and Operations. This is done to ensure that the latest cost prices are always used in your job type forecasts. It is also possible to make similar updates for [work order forecasts](08_Work_Orders.md#forecasts).


1. Click **Enterprise asset management** > **Periodic** > **Forecast** > **Update job type forecast**.
2. In the **Update job type forecast** dialog, you can add selections regarding specific job types, if required.

3. Click **Filter**, then click **Select** to make those selections.
4. If required, you can set up automatic update as a batch job by filling out the fields on the **Run in the background** FastTab.

5. Click **OK** to start the forecast update.


![Figure 8-07](/Figures/08-07_UpdateJobTypeForecast_Dialog_AX7-01.png)


---


### Work Order Stages

Work order stages define the stages that a work order can go through, for example, Created, Scheduled, In progress, and Ended. Work order stages may be updated manually on a work order, or they may be updated automatically, for example during work order scheduling.

The work order stages required for your work orders must be attached to matching project stages in the **Project management and accounting** module > **Project management and accounting parameters**. First, you set up project stages in **Project management and accounting**, then you set up work order stages and stage groups in **Enterprise asset management**.

Here is a short description of the check boxes in **Work order stages** > **General** FastTab > **Work order** and **Schedule** sections:


| Button name | Description |
|--------|--------|
|Active                |Select if the work order should be active at this stage.      |
|Add line              |Select if it should be possible to add work order lines to a work order at this stage.        |
|Delete                |Select if it should be possible to delete a work order at this stage.        |
|Delete line           |Select if it should be possible to delete work order lines on a work order at this stage.        |
|Allow scheduling      |Select if it should be possible to schedule a work order at this stage.        |
|Set actual start      |Select to ensure that when a work order is updated to this stage, the user is asked to select an actual start date and time for the work order. |
|Set actual end        |Select to ensure that when a work order is updated to this stage, the user is asked to select an actual end date and time for the work order. |
|Post journals         |Select if work order journals should be automatically posted at this stage.  |
|Ready                 |If selected, it means that when a work order is updated to this stage, the work order line schedule status for all work order lines created on the work order is automatically updated to "Ready".  |
|Start                 |If selected, it means that when a work order is updated to this stage, the work order line schedule status for all work order lines created on the work order is automatically updated to "Started". |
|End                   |If selected, it means that when a work order is updated to this stage, the work order line schedule status for all work order lines created on the work order is automatically updated to "Ended".  |


###### NOTE regarding Post journals

If journal posting results in an error, an Infolog message is shown, and the work order stage update is canceled. If you want to check the journal lines of a work order, click **Enterprise asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders** or **My active work orders** > select work order in list > **Journals**. This automatic setup of work order journal posting at a certain stage is the same as when you click the **Post journals** button in [work order journals](15_Consumption.md#register-consumption).


---


#### Set Up Project Stages and Work Order Stages


1. Click **Project management and accounting** > **Setup** > **Project management and accounting parameters**.
2. Click **Project stage**.

3. For each stage you want to use, select the project type check boxes required for your work orders. The project types define rules regarding which financial tasks are allowed, for example, create forecast, create estimates, create beginning balances, and so on.
###### NOTE
If the project stage for the project type is not selected, and that project stage is used on a work order stage, the work order projects will not be updated accordingly.
4. Close **Project management and accounting parameters**.

5. Click **Enterprise asset management** > **Setup** > **Work order** > **Stage** > **Stages**.
6. Click **New**, to create a new work order stage.

7. Insert a stage ID in the **Stage** field and a name for the stage in the **Name** field. In the **Stage groups** field, you can see the number of work order stage groups that uses the work order stage.
8. On the **General** FastTab, in the **Work order** and **Schedule** sections, select the functions that should be available for the stage by selecting the relevant check boxes. Refer to the table above for some of the stage descriptions.

9. In the **Project section** > **Stage** field, select the the project stage to be related to the work order stage.
10. In the **Project section**, select the **Close activities** check box if project activities related to each work order line should be automatically closed at this stage.
###### NOTE
The project activity number related to a work order line is shown in **Enterprise asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders** or **My active work orders** > select work order > **Edit** button > select work order line > **Line details** FastTab > **General** tab > **Project** section > **Activity number** field.

11. Select one or more of the **Copy hour forecast**, **Copy item forecast**, **Copy expense forecast**, **Copy fee forecast** check boxes if you want to automatically copy work order project forecasts to work order journals at this stage.
12. In the **Schedule** group, select one of the check boxes if you want schedule status for work order lines to be updated at this stage. Refer to the descriptions of **Ready**, **Start**, and **End** in the table above.
###### NOTE
Schedule lines related to work order lines are shown in **Enterprise asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders** or **My active work orders** > select work order > **Edit** button. In **All Work orders** Details view, select a work order line on the **Work order lines** FastTab > see related schedule lines on the **Line details** FastTabs. The status of a schedule line is shown on the **Schedule** tab in the **Status** field. The **Status** field may show one of the following statuses: Scheduled - Ready - Started - Stopped - Ended.

13. In the **Requests** section > **Stage** field, select the the request stage to which related requests are updated. This is an automatic update of related requests. The update can only be done if the request stage is selected in the request stage group used for the request.
14. Select the **Update object BOM** check box if all items used on a work order should automatically be updated in **Object BOM** when the work order is updated to this stage. For example, this could be relevant for a work order stage defining that the work order is completed / ended.

15. Select the **Delete pool reference** field if you want work orders to be automatically deleted from work order pools at this stage.
16. The **Kanban stage** field is used if your company uses kanban functionality on a Mobile EAM Client to let workers manage and complete work orders using the **Kanban** module. Select the kanban stage to which a work order should be updated at this work order stage.
###### NOTE
You can read more about kanban functionality in the document "Mobile EAM Client Training Material", which describes the features and functions of the mobile client.

17. On the **Validate** FastTab, select the check boxes for the validation types you want to activate at this stage. In the **Type** field regarding each validation type, select the type of message that should be shown if mandatory fields related to the validation type have not been validated. If you select the message type "Error", the work order stage update is canceled until the related mandatory fields have been updated on the work order.



###### NOTE
The **Production stop**, **Fault symptom**, **Fault cause**, and **Fault remedy** check boxes on the **Validate** FastTab relate to the check boxes in the **Mandatory** section in **Work order types** (**Enterprise asset management** > **Setup** > **Work orders** > **Work order types**). In order to activate those validations, the related check boxes must also be selected on the work order type used on the work order.

When a work order is updated to a work order stage for which the **Committed cost** check box is selected on the **Validate** FastTab, it means that total committed costs (meaning total amount of expenses that the legal entity has committed to pay) are calculated for each work order line. An Infolog is shown if the committed cost amount is larger than zero. The types of cost commitment to be included are selected in **Project management and accounting** > **Setup** > **Project management and accounting parameters** > **Cost control** > **Cost commitments** section.

When a work order is updated to a work order stage for which the **Production stop** check box is selected, a production stop validation is made on the object related to a work order. If a production stop has been registered, and it does not have an 'ended' registration, a message is displayed when the work order is updated to this stage.


![Figure 8-08](/Figures/08-08_ProjManParameters_ProjStages_Form_AX7-01.png)


###### NOTE
In **Project management and accounting parameters**, you can set up user-defined project stages if you require special stages for your **Enterprise Asset Management** setup that are not included in the standard project setup.

See the [Forecasts, Work Orders, and Projects](10_Integration_Proj_Management.md#forecasts-work-orders-and-projects) section for more information on the relation between work order stages, project stages, and work order projects.


![Figure 8-09](/Figures/08-09_WO_Stages_Form_AX7-01.png)


###### NOTE
When you change stage on a work order to a work order stage that is not active (meaning the **Active** check box on the **General** FastTab is not selected for that stage in the **Work order stages** view), not yet posted journals related to the work order will automatically be deleted. This is done to ensure automatic cleanup of unused data.

However, if you manually set a work order to be inactive (**Enterprise asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders** > select work order in list > **Edit** button > **Header view** button > **General** FastTab > clear the **Active** check box), related but not yet posted journals will not automatically be deleted.


---


#### Stage Group, Type, and Stage Relations

Stage groups refer to work flows, and stages are selected in a stage group in a sequential order. Stage groups are set up on types. Types determine the size or extent of work flows and work processes. For example, a standard work order type, "Maintenance", may be related to a work order stage group containing many stages. A "Corrective" work order type, which is used for work orders that have not been scheduled, or work orders for which the job was completed before the work order was made because of a need of urgency, may have a related work order stage group that only contains a few work order stages.

The idea behind using types is that when a type is defined on, for example, a work order or an object, the related work processes (stages) are automatically defined. Refer to the [Work Order Types](08_Work_Orders.md#work-order-types) section for more information about how to set up work order types.



###### NOTE
Stages, stage groups, and types apply to: [Functional locations](05_Functional_Locations.md#functional-location-stages) - [Objects](06_Objects.md#object-stages) - [Requests](07_Requests.md#request-stages) - Work orders - [Contracts](21_Setup_for_Contracts.md#contract-stages).


The figure below shows the relation between work order types, work order stage groups, and related work order stages.


![Figure 8-10](/Figures/08-10_WO_Type_StageGroup_Relation_AX7-002A.png)


---


#### Work Order Stage Groups

When you have created the work order stages required for your work orders, stages can be divided into work order groups. As a minimum, one standard work order stage group should be created.


1. Click **Enterprise asset management** > **Setup** > **Work order** > **Stage** > **Stage groups**.
2. Click **New** to create a new work order stage.

3. Insert the stage group ID in the **Stage group** field and a name for the stage group in the **Name** field. In the **Stages** and **Work order types** fields, you can see the number of stages selected in the stage group, and the number of work order types that uses the stage group.
4. On the **Stages** FastTab, select the stages that should be included in the group. This is done by clicking on a stage in the **Stages remaining** section and clicking the ![Figure 8-11](/Figures/08-11_Button_Select_StageGroups.png) button.

5. If you want to select all the available stages for a group, click the ![Figure 8-12](/Figures/08-12_Button_SelectAll_StageGroups.png) button. All stages are transferred to the **Stages selected** section.
6. If you want to remove a selected stage from the group, select the stage in the **Stages selected** section and click the ![Figure 8-13](/Figures/08-13_Button_Deselect_StageGroups.png) button.

7. Click **Stage updates** to define which stages can follow a selected stage.
8. On the **General FastTab**, in the **Scheduled stage** field, select the stage that should always be selected for a work order when you have completed [Work Order Scheduling](13_WO_Scheduling.md#work-order-scheduling) on that work order, regardless of the previous stage of the work order. In the **Quotation created stage** field, select the stage that should always be selected after you have created a quotation on a work order, regardless of the previous stage of the work order.

9. In the **Unscheduled stage** field, select the stage that should always be selected for a work order in case work order scheduling is deleted.
10. Save the work order stage group.



![Figure 8-14](/Figures/08-14_WO_StageGroups_Form_AX7-02.png)


---


### Work Order Types

A work order type is used to categorize a work order, for example relating to preventive maintenance or corrective maintenance. A work order type defines the work order stage group affiliation. **Work order stage group** defines which stages can be set on a work order, for example, "Created", "In Process", and "Finished".

Refer to the [Work Order Stages](#work-order-stages) section for more information about work order and project stages.


1. Click **Enterprise asset management** > **Setup** > **Work orders** > **Work order types**.
2. Click **New** to create a new work order type.

3. Insert the work order type ID in the **Work order type** field and a name for the work order type in the **Name** field.
4. Select a stage group in the **Work order stage group** field.

5. Select the **One worker** check box if all work order lines related to a work order of this type should be scheduled to the same worker.
6. In the **Cost type** field, select cost type, "Corrective", "Preventive", or "Investment". All work order lines on a work order must contain the same cost type.

7. In the **Mandatory** section, select the check boxes for which you want to ensure that information relating to faults or production stops is added to the work order.
8. Click **Save**.


###### NOTE
The check boxes in the **Mandatory** section relate to the check boxes on the **Validate** FastTab in **Work order stages** (**Enterprise asset management** > **Setup** > **Work orders** > **Stage** > **Stages**).


![Figure 8-15](/Figures/08-15_WO_Types_Form_AX7-01.png)

---


### Work Order Project Setup

In the **Enterprise asset management** module, a project relation on a work order line is mandatory. The project associated with the work order line allows you to track costs on different projects related to Enterprise Asset Management, for example, internal maintenance projects, service management projects, and investment projects. Refer to the [Integration to Project Management and Accounting](10_Integration_Proj_Management.md#integration-to-project-management-and-accounting) chapter for more information about project relations to work orders and objects.

Before you start creating work orders, you must set up work order projects. **Work order project setup** contains two links, **Parent project** and **Project group**. In the **Project group** section, you select project groups to be associated with work order types, object types, objects, and customers. You must set up at least one project group record because all projects require a relation to a project group.

In the **Parent project** section, you can set up project relations to be used in case no project is set up on the object selected on the work order line. Parent project setup is not required if your company uses object projects. It is only relevant if you want to use work order projects instead of object projects.

The setup allows complete integration with the **Project management and accounting** module, allowing you to track costs related to work orders in the related projects. Read more about the relation between work order projects, project stages and work order stages in the [Forecasts, Work Orders, and Projects](10_Integration_Proj_Management.md#forecasts-work-orders-and-projects) section. The following procedure describes the work order project setup:

1. Click **Enterprise asset management** > **Setup** > **Work orders** > **Project setup**. Make sure that the **Parent project** link is selected.
2. Click the **Add** button.

3. Select a **Work order type**, **Functional location**, **Object type**, **Customer account**, and/or **Object** in the related fields. It is possible to fill out only one field, two fields, or all fields for each line. The number of fields you fill out determine the combination used when selection of a project ID is done in Enterprise Asset Management. Read more about the combinations and the selection process in the ///"Forecasts, Work Orders and Projects" section.
   ###### NOTE
   If you select a functional location, the related sub locations are automatically included. If you select an object, it is possible to create more work order project setup lines for the same object, but select different projects for the same object.
4. In the **Project ID** field, select the project to be related to the setup you created in step 3.
5. In the **Expiration** field, you can select a date if the project setup is to be valid for only a limited period. If no limitation is relevant, make sure that the "Never" option is selected.
   ###### NOTE
   Select **View** > **All** to see the **Effective** field. The standard setup regarding start date is the date you add the work order project to the form. If required, you can set up a limited period for the work order project in the **Effective** and **Expiration** fields.
![Figure 8-16](/Figures/08-16_WO_ProjectSetup_Form_ParProj_ASM_AX7A.png)

6. Click the **Project group** link. In this section, as a minimum, you associate a work order type with a project group.
7. In the **Work order type** field, select a work order type.

8. If you want the project group association to be more specific, select **Customer account**, **Object type**, and/or **Object** in the related fields.
9. In the **Project group** field, select the project group to be related to the work order type. Examples: A work order type called "Preventive maintenance" may be associated with a project group called "Prev Maint" or "Internal". A work order type called "Investment", to be used for work orders related to investments and fixed assets, may be associated with a project group called "Invest" or "Investment".

10. Click **Save**.


![Figure 8-17](/Figures/08-17_WO_ProjectSetup_ProjGroup_ASM_AX7-01.png)


###### NOTE
You must create at least one general project group record, and in that record, project group "Internal" must be selected (as shown in the first record in the screenshot above).

Each time a new work order line is created, Enterprise Asset Management searches for a project group to be related to the work order line project, based on the setup described in this section. All project groups have a related project type. Project groups that use the project type "Time and material" or "Fixed-price" are only valid for objects that are related to a customer account.

Regarding Parent project and Project group, when the system selects the available work order project or project group, the selection is based on the records you created in the procedure above. Enterprise Asset Management goes through records related to the work order project to check for a possible match, always checking the most specific combination first. For the work order parent project, this means that, first, a possible match regarding Object is checked. If no match is found, Object type is checked. If no match is found, Functional location is checked, and so on. As you can see in the layout of the form, this means that Enterprise Asset Management checks each record from right to left for a match (Object, then Object type, Functional location, Work order type, and Customer account to find the most specific combination. If no match is found, the "default" record is used in which only a Project ID is selected. Finding the related project group is a similar process. First, a possible match regarding Object is checked, then Object type, Customer account, and Work order type. Also in this case, if no match is found, the "default" record is used in which only a Project group is selected.


---


### Priority and Description

When you create a new work order, you may want to prioritize the work order and add a general description to it. You can create priorities and descriptions in the **Priority** and **Work order description** detail views.


#### Create Priority


1. Click **Enterprise asset management** > **Setup** > **Work orders** > **Priority**.
2. Click **New**.

3. Insert a priority, for example a number, in the **Priority** field.
4. Insert a name for the priority in the **Name** field.

5. On the **Work orders** FastTab, you can define expected start and end expected end, which are used for manually created work orders and work orders created on the basis of requests. These fields are used to indicate a time frame in which work orders should be started and ended.
6. In the **Start day** field, insert a number indicating number of days calculated from the creation of the work order in which period the work order should start. Example 1: Insert "0" if you want the work order to start at the time of work order creation. Example 2: Insert "7" if you want the work order to start within one week after creation of the work order.

7. Select the **Set start time** check box if you want to insert a start time on the work order together with the start date. If you select the check box, insert start time in the **Start time** field. If you clear the **Set start time** check box, current time of day is used.
8. In the **End day** field, insert a number indicating number of days calculated from the start date of the work order in which period the work order should end. Example: Insert "7" if you want the work order to end within a week from the start date of the work order.

9. Select the **Set end time** check box if you want to insert an end time on the work order together with the end date. If you select the check box, insert end time in the **End time** field. If you clear the **Set end time** check box, current time of day is used.
10. Click **Save**.


![Figure 8-18](/Figures/08-18_Priorities_Form_AX7-01.png)


#### Create Description


1. Click **Enterprise asset management** > **Setup** > **Work orders** > **Descriptions**.
2. Click **New**.

3. Insert the description in the **Description** field.
4. Click **Save**.


---


### Scheduled Execution

Work order priorities, which are described in the previous section, can be used to set up scheduled execution. You can use scheduled execution to provide flexibility in work planning for the maintenance worker or service worker by setting up more detailed or less detailed requirements as to the interval during which a work order should be completed. For example, if a maintenance or service worker has completed a job faster than expected in a production facility or at a customer site, the worker may be able to complete a job nearby, not necessarily planned for the current day, but for the current week. This approach provides the possibility of optimizing worker planning and job completion.

Scheduled execution can be set up for various levels related to a work order. You can set up generic lines - as shown in the figure below - that are not limited to specific work order types, object types, and so on. Or you can create specific scheduled execution lines that apply to a work order type, object type, job type, and so on, or a combination.


1. Click **Enterprise asset management** > **Setup** > **Work orders** > **Scheduled execution**.
2. Click **New** to create a new scheduled execution line.

3. If required, make selections in the **Work order type**, **Object type**, **Product**, **Model**, **Job group**, **Job type**, **Variant**, or **Trade** fields.
4. Select a work order priority in the **Priority** field. If you leave this field blank, you can make the most generic scheduled execution line - as shown in the first record in the figure below. That line is set up to allow all work orders that have no work order priority to be scheduled for a specific date and time.

5. Select the time interval in the **Scheduled execution** field.
6. Click **Save**.


![Figure 8-19](/Figures/08-19_ScheduledExecution_Form_AX7-01.png)


---


### Fault Management

In Enterprise Asset Management, you can manage faults detected on objects by describing symptoms, areas, and fault types. The fault designer allows you to set up symptoms, areas, and fault types on object types. Also, fault causes and suggestions to remedy faults can be registered on a work order.

The sequence of registration and management of errors is: First, you create a list of fault symptoms, fault areas, and fault types that may occur on your object types. Next step is setting up symptoms, fault areas, and fault types in the Fault designer. To understand the distinction between fault symptoms, fault areas, and fault types, here are a few examples:


**Fault symptoms**

- Unbalanced voltages

- Short circuit

- Noise

- Leak

- Vibrations



---



**Fault areas**

- Electrical

- Mechanical

- Hydraulic

- Pneumatic



---



**Fault types**

- Faulty main stator winding

- Faulty diode

- Dirty windings

- Defective generator

- Defective sensor



---


The relations between fault symptoms, fault areas, and fault types depend on the license configuration setup of the **Enterprise asset management** module. In **License configuration** (**System administration** > **Setup** > **License configuration**), you can select a **Fault hierarchy** check box. If that check box is selected, it means that when you select a symptom in **Fault designer**, the fault areas related to that symptom are shown on the **Fault area** FastTab. Likewise, when you select a fault area in **Fault designer**, the fault types related to that area are shown on the **Fault type** FastTab. Refer to the [License Configuration](03_License_Config.md#license-configuration) chapter for more information about configuration of Enterprise Asset Management.


###### NOTE
If the **Fault hierarchy** check box is cleared in **License configuration**, it means that when you select a fault symptom in **Fault designer**, you will see all the fault areas and fault types that have been added in **Fault designer**. In that case, there is no hierarchical relationship between the selected fault symptom, fault areas, and fault types displayed.

Cause and remedy for a specific fault can be selected on a work order or a request.


###### NOTE
You can only create fault records on work orders and requests if they contain objects with object types that have faults connected to them in the **Fault designer**.


---


#### Fault Symptom

Create a list of symptoms to be used in the fault designer.


1. Click **Enterprise asset management** > **Setup** > **Object** > **Fault** > **Fault symptoms**.
2. Click **New** to create a new record.

3. Insert a name for the symptom in the **Fault symptom** field.
4. Insert a description in the **Description** field.

5. Click **Save**.


---


#### Fault Area

Create a list of areas or locations to be used in the fault designer.


1. Click **Enterprise asset management** > **Setup** > **Object** > **Fault** > **Fault areas**.
2. Click **New** to create a new record.

3. Insert a name for the area in the **Fault area** field.
4. Insert a description in the **Description** field.

5. Click **Save**.


---


#### Fault Type

Create a list of fault types to be used in the fault designer.


1. Click **Enterprise asset management** > **Setup** > **Object** > **Fault** > **Fault types**.
2. Click **New** to create a new record.

3. Insert a name for the type in the **Fault type** field.
4. Insert a description in the **Description** field.

5. Click **Save**.


---


#### Fault Designer

In **Fault designer**, you set up fault data on object types.


1. Click **Enterprise asset management** > **Setup** > **Objects** > **Fault** > **Fault designer**.
2. In the left-hand side of the form, select the object type for which you want to set up a fault record.

3. On the **Fault symptom** FastTab, click **Add line**, and select a symptom in the **Fault symptom** field.
4. On the **Fault area** FastTab, click **Add line**, and select an area in the **Fault area** field.

5. On the **Fault type** FastTab, click **Add line**, and select a type in the **Fault type** field.
6. Click the **Create combinations** button to quickly create combinations of all existing fault symptoms, areas, and types to the selected object type. This function is useful if you have created many combinations. If you do not want to use all combinations on the object type, it is easier to delete the lines that are not relevant than to create new lines manually.

7. Click the **Copy from object type** button to copy the specific setup of fault symptoms, areas, and types from one object type to another object type.
8. Click **Save** to save the changes.


![Figure 8-20](/Figures/08-20_FaultDesigner_Form_AX7-01.png)


---


#### Fault Cause

Create a list of known fault causes, which can be added to a work order or a request.


1. Click **Enterprise asset management** > **Setup** > **Object** > **Fault** > **Fault causes**.
2. Click **New** to create a new record.

3. Insert a name for the fault cause in the **Fault cause** field.
4. Insert a description in the **Description** field.

5. Click **Save**.


---


#### Fault Remedy

Create a list of suggestions for remedy and repair, which can be added to a work order or a request.


1. Click **Enterprise asset management** > **Setup** > **Object** > **Fault** > **Fault remedies**.
2. Click **New** to create a new record.

3. Insert a name for the remedy in the **Fault remedy** field.
4. Insert a description in the **Description** field.

5. Click **Save**.



###### NOTE
If required, you can change or update the names of your fault symptoms, areas, types, causes, and remedies. The name changes are automatically reflected in the related fault registrations.


---


### Setup Data and Consistency Check

In standard Dynamics 365 for Finance and Operations, it is possible to perform consistency check on your setup data for some modules, including Enterprise Asset Management and Contract Management. If you want to carry out a consistency check to validate your setup data, click **System administration** > **Periodic** > **Database** > **Consistency check**, and select the modules to be included in the validation.


![Figure 8-21](/Figures/08-21_ConsistencyCheck_Form_StdAX_AX7-01A.png)


When the validation is completed, a message box describing any inconsistencies is shown. Various inconsistencies in the setup data may be found in Enterprise Asset Management. For example, a request may be related to a work order that no longer exists, or a work order project ID requires a sub project ID format (**Project management and accounting** > **Setup** > **Project management and accounting parameters** > **General** link > **Default subproject ID format** field), which is not available.


---


### Introduction to Work Orders

Work orders can be created automatically or manually:


- Automatically using the **Schedule maintenance sequences** form, for calendar-based sequences set to "Auto create" (refer to the [Preventive and Reactive Maintenance](11_Preventive_Reactive_Maint.md#preventive-and-reactive-maintenance) chapter).

- Automatically using the **Schedule rounds** form, for rounds set to "Auto create" (refer to the [Preventive and Reactive Maintenance](11_Preventive_Reactive_Maint.md#preventive-and-reactive-maintenance) chapter).



- Create from object calendar (refer to the [Object Calendar](11_Preventive_Reactive_Maint.md#object-calendar) section), which can be preventive maintenance jobs or requests.

- Create a work order manually.



- Create a work order from the **All requests** or **Active requests** or **My functional location requests**.



###### NOTE
Work order lines related to the same object are related to the same project ID.


---

Click **Enterprise asset management** > **Common** > **Work orders** > **All Work orders** to open the list. **All work orders** contain a list of all work orders and displays some of the information related to a work order.


![Figure 8-22](/Figures/08-22_AllWorkOrders_List_AX7-01.png)


###### NOTE
Click **Enterprise asset management** > **Common** > **Work orders** > **Active work orders** to see a list of active work orders.

Click **Enterprise asset management** > **Common** > **Work orders** > **My functional location work order lines** to see a list of work order lines containing objects installed on functional locations, you are related to as a worker (set up in [Workers and Worker Groups](06_Objects.md#workers-and-worker-groups)).



In the **All Work orders** list (grid view), click on a link in the **Work order** column to show the Details view of the selected record. Click the **Edit** button to open for editing. In the Details view, you will see detailed information related to the work order as well as Fact Boxes to the right of the screen, displaying other work order-related information. Click on the blue 'left arrow' / 'right arrow' button in the small blue box placed above the Fact Boxes to show or hide the Fact Boxes.


![Figure 8-23](/Figures/08-23_WO_Form_AX7-01.png)


The action pane buttons are organized in tabs on the action pane. Here is a brief description of the buttons relating to Enterprise Asset Management:


| Button name | Description |
|--------|--------|
|Edit                  |Edit the selected work order.       |
|New                   |Create new work order.        |
|Delete                |Delete the selected work order.        |
|Work order pool       |Add selected work order to a work order pool, or remove from work order pool.        |
|Adjust                |Adjust information about expected start and end, priority, responsible worker, or responsible worker group on selected work orders.        |
|Related work order    |Create a new work order related to the selected work order line. This is useful if you want to register primary and secondary work orders. |
|Copy work order       |Create a new work order based on an existing work order.    |
|Header view           |In **All Work orders**, show only header information.       |
|Line view             |In **All work orders**, show detailed information.        |
|Notes                 |Create a description, or insert a note, on a work order. Start by clicking the **Add timestamp** button to add your user name and a timestamp to the note.       |
|Tools                 |Create a list of required tools on a work order. Tools are set up as resources in **Organization administration** > **Common** > **Resources** > **Resources**.     |
|Checklist             |View checklist for the object connected to the work order.    |
|Object fault          |View or register fault information on an object to be used for error management.       |
|Production stop       |Specify production stop for a work order.       |
|Condition assessment  |Register condition assessment measurements on a work order.       |
|Object counters       |Create or view counter registrations on the object.   |
|Forecast              |View or create forecasts on a work order.   |
|Journals              |View or create work order journals. Journal lines can be copied from forecasts.    |
|Project transactions  |View all posted transactions related to work orders created for the object.    |
|Work order stage      |Update work order stage.    |
|Stage log             |Log displaying the stages of the selected work order.      |
|Object documents      |View list of documents attached to objects related to a work order. These documents are set up in **Enterprise asset management** > **Setup** > **Object documents**.       |
|Quotation             |Create quotation for work order based on forecasts.   |
|Invoice proposal      |Create invoice proposal for the work order.   |
|Update quotation      |Update work order quotation if forecasts have changed.    |
|Project quotation     |View project quotation.    |
|Schedule              |Schedule the selected work orders.    |
|Schedule exclusively    |Schedule the selected work order for one worker.      |
|Delete schedule       |Delete scheduling for the selected work order.     |
|Work order calendar   |Open the **Work order calendar** list page.      |
|Work order purchase requisition        |Open the **Work order purchase requisition** list page.      |
|Work order purchase   |Open the **Work order purchase** list page.       |
|Project invoice proposals   |View invoice proposals for the work order.      |
|Cost control          |Compare budget costs and actual costs on the work order.        |
|Work order report     |Print work order report.    |
|Work order consumption      |Print consumption report.     |
|Work order times      |Print work order times report.       |
|Contracts             |Open the **All contracts** list to see contracts attached to the work order.     |


---

The buttons on the **Work order** tab > **Project** section relate to functionality in the **Project management and accounting** module regarding forecasts, journals and invoicing.


###### NOTE
Forecasts created on a work order can be included when running master scheduling by using the forecast model selected in the **Enterprise asset management parameters** form.


---

### Manually Created Work Orders

You can create work orders manually in two ways:


- in **All work orders** or **Active work orders**

- in **All requests** or **Active requests** or **My functional location requests**



#### Create Work Order


1. Click **Enterprise asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.
2. Click the **New** button.

3. In the **Create work order** drop-down, select a work order type.
4. If required, select a description and a customer account in the related fields.

5. Select the object for the work order as well as the related job type.
   ###### NOTE
   When you select an object, three tabs are available: The **My objects** tab contains objects related to the functional locations to which you (the worker who is logged on the system) may be allocated (set up in [Workers and Worker Groups](06_Objects.md#workers-and-worker-groups)). If no functional locations are set up on a worker in [Workers and Worker Groups](06_Objects.md#workers-and-worker-groups), the **My objects** tab will not be visible. The **Active objects** tab contains a list of all objects with object stage "Active". The **Object view** tab displays a tree view of functional locations and objects installed on those locations.

6. If required, select **Variant** and **Trade**.
7. If required, you can change the work order priority in the **Priority** field.

8. Select expected start and end dates in the related fields.
9. Click **OK** to create a new work order.

10. Edit the work order in **All work orders**, if required.


###### NOTE
In **All work orders**, You can add several objects to a work order in Details view by adding lines on the **Work order lines** FastTab. On an object, you can only select the job types that are defined on the object type related to the object.

If you have changed an object priority or an object criticality after you have used them on a work order (refer to the [Object Priorities](06_Objects.md#object-priorities) and [Object Criticalities](06_Objects.md#object-criticalities) sections), the priority or criticality on the work order is not updated accordingly.

Criticality on a work order is re-calculated each time a work order line is added or deleted on the work order.

In **All work orders** Details view > **Header view** > **Schedule** FastTab, you can select a responsible worker group or a responsible worker in the **Responsible group** or **Responsible** fields. These settings can be changed as long as the work order is active, for example, when the work order stage changes. The automatic selection made during work order creation is based on the setup in **Responsible workers**. If you add or remove work order lines after you have created a work order, and the **Responsible group** field and the **Responsible** field are blank when you update the work order, Enterprise Asset Management searches for a possible match in the setup form for a responsible group or a responsible worker. If the **Responsible group** field or the **Responsible** field is already filled out when you update the work order, no changes are made. Read more about responsible workers and worker groups in the [Responsible Workers](07_Requests.md#responsible-workers) section.

In [Maintenance Status](20_ControllingAndReporting.md#maintenance-status), you can make a calculation to get an overview of workload regarding incoming and completed work orders.

On the **Line details** FastTab, two fields have been added: **Latitude** and **Longitude**. In these fields, you can add geographic coordinates for the object selected on the work order line.


#### Create Related Work Order
You can create a related work order to an existing work order if, for example, you want to work with primary and secondary work orders. A new work order is based on a work order line from an existing work order.


1. Click **Enterprise asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.
2. Select the work order for which you want to make a related work order.

3. Click **Related work order**.
4. In the **Create related work order** drop-down, select the work order line for which you want to create a related work order in the **Work order line** field.

5. Select a job type in the **Job type** field and, if required, a related job variant and job trade in the **Variant** and **Trade** fields.
6. If this is the first related work order you make, click the **New work order** radio button.

7. Select a **Work order type** and a **Description** in the related fields.
8. If required, change the work order priority in the **Priority** field.

9. Insert expected start and end dates in the related fields.
10. Click **OK**. The new related work order is shown in the **All work orders** list.

11. If you create a related work order on a work order that already has related work orders, you can add the work order line to an already related work order. This is done by clicking the **Add to related work order** radio button in step 6. Then you select the related work order to which you want to add a new work order line. Edit the **Priority**, **Expected start**, and **Expected end** fields, if required, and click OK. The work order line is added to the existing related work order.



![Figure 8-24](/Figures/08-24_CreateRelatedWorkOrder_Drop-down_AX7.png)



###### NOTE
If you have set up a related work order mask in **Enterprise asset management parameters** > **Work orders** link > **Related work order mask** field, work order IDs will be created in accordance with the mask setup. If no related work order mask is set up, the next available work order ID will be used for related work orders.


---


#### Copy Work Order

It is possible to quickly create a new work order from an existing work order. This way of working with work orders is different from creating work orders based on [Maintenance Sequences](11_Preventive_Reactive_Maint.md#maintenance-sequences). It is useful if, for example, you have a work order containing many work order lines with various jobs on different objects that should be completed at regular intervals.


1. Click **Enterprise asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.
2. Select the work order from which you want to copy content.

3. Click **Copy work order**. The work order setup from the selected work order is shown. If required, you can edit some of the fields.
4. Click **OK** to create the new work order.

5. Edit the work order in **All work orders**, if required.



###### NOTE
When the new work order is created, some information is copied directly from the existing work order. Information regarding forecasts, tools, checklists, functional location, addresses, and scheduling is not copied, but initialized from the current setup in Enterprise Asset Management. This means that if changes were made in those data from the time of creation of the first work order until the time you made a copy of the work order, those changes are included in the new work order you have created. Examples are changes in forecasts or updated checklists.


![Figure 8-25](/Figures/08-25_CopyWorkOrder_DropDown_AX7.png)


---


#### Create Work Order Based on a Request


1. Click **Enterprise asset management** > **Common** > **Requests** > **All requests** or **Active requests**.
2. Select the request for which you want to create a work order, and click **Edit**.

3. In **All requests**, click **Work order**.
4. Fill out the **Work order** drop-down. If a job type has been selected in the request, you are able to select another job type, if required, when you create the work order.

5. Click **OK**. You will see a message informing you that the work order has been created.
6. If you want to see which work orders are connected to a request, select the request in the **All requests** or **Active requests** lists, and click the **Work orders** button.


###### NOTE
Work orders can also be created automatically by scheduling maintenance sequences jobs, or by setting up "Auto create" maintenance sequences or rounds on an object. Read more about automatically created work orders in the [Preventive and Reactive Maintenance](11_Preventive_Reactive_Maint.md#preventive-and-reactive-maintenance) chapter. Work orders created from requests in the **Object calendar** are created with the job types selected in the requests.


---


### Forecasts
When you create a work order, you create work order lines with related objects and job types. When you select a job type containing forecasts, the forecasts are automatically copied to the work order.

You may be able to add or delete forecast lines on a work order. The setup of a work order stage, the related project type, and the stage rules related to the project type determines if you are able to add or edit forecast lines. Read more about work order stages and related project stages in the [Integration to Project Management and Accounting](10_Integration_Proj_Management.md#integration-to-project-management-and-accounting) chapter.


1. Click **Enterprise asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.

2. Select the work order in the list, and click **Forecast**. In **Work order forecast**, forecast lines from the job type selected on the work order line are displayed.


---


#### Add Hours Forecast to a Work Order


1. Select the work order line to which you want to add a forecast.
2. On the **Forecast** FastTab, click the **Hours** tab.

3. Click **Add** to create a new line.
4. Select a category in the **Category** field.

5. Insert number of forecasted hours in the **Hours** field.
6. In the **Line property** field, select the charge type to be used on the line.


---


#### Add Items Forecast to a Work Order

There are three ways to add items to a work order forecast: You can create lines for items (spare parts) that are not included in the spare parts list or object BOM, you can select spare parts from the approved spare parts list, and you can select items from the object BOM.


1. Select the work order line to which you want to add a forecast.
2. On the **Forecast** FastTab, click the **Items** tab.

3. Click **Add** to create a new line for a spare part that is not on the spare parts list or the object BOM list.
4. Select the item in the **Item number** field.

5. Insert quantity in the **Quantity** field, and select a quantity unit in the **Unit** field.
6. Insert cost price and currency in the relevant fields.

7. If you want to change the list of dimensions displayed on the **Inventory dimensions** tab, click **Inventory** > **Dimensions display**, select the dimensions, and select the **Save setup** check box.
8. If you want to add an approved spare part to the forecast, click **Add spare parts**, select the spare part, edit related information if required, and click **OK**.

9. If you want to add object BOM items to the forecast, click **Add BOM items**, select the item, edit related information if required, and click **OK**.
10. Click **Item where used** if you want to get an overview of where the item on the selected line is used in Enterprise Asset Management in relation to objects, job type setup, spare parts, and work orders. Read more about this overview in the [Items Where Used](20_ControllingAndReporting.md#items-where-used) section.


---


#### Add Expense Forecast to a Work Order


1. In the left-hand side of the form, select the work order line to which you want to add a forecast.
2. On the **Forecast** FastTab, click the **Expense** tab.

3. Click **Add** to create a new line.
4. Select a category in the **Category** field.

5. Insert quantity in the **Quantity** field.
6. Insert cost price, sales currency, and sales price in the relevant fields.

7. In the **Line property** field, select the charge type to be used on the line.


---


#### Add Fee Forecast to a Work Order


1. In the left-hand side of the form, select the work order line to which you want to add a forecast.
2. On the **Forecast** FastTab, click the **Fee** tab.

3. Click **Add** to create a new line.
4. In the **Project date** field, the current date is automatically inserted. If required, select another date.

5. Select a category in the **Category** field.
6. Insert sales currency and sales price in the relevant fields.

7. In the **Line property** field, select the charge type to be used on the line.



###### NOTE
On the **Forecast totals** FastTab, you can see an overview of the number of lines created on each tab, for the selected work order line and for the work order. Also, you can see a sum of forecasted work hours for the work order line and for the work order.


![Figure 8-26](/Figures/08-26_WO_Forecast_Form_ASM_AX7-01.png)


---


#### Automatic Update of Work Order Forecasts

In Enterprise Asset Management, you can automatically update any changes in work order forecasts regarding hour costs, item costs, and expenses, which have been updated in other modules in Dynamics 365 for Finance and Operations. This is done to ensure that the latest cost prices are always used in your work order forecasts. It is also possible to make similar updates for [job type forecasts](#automatic-update-of-job-type-forecasts).


1. Click **Enterprise asset management** > **Periodic** > **Forecast** > **Update work order forecast**.
2. In the **Update work order forecast** drop-down, you can add selections regarding specific work orders or work order lines, if required. Click **Filter** to make those selections.

3. If required, you can set up the automatic update as a batch job on the **Run in the background** FastTab.
4. Click **OK** to start the forecast update.



![Figure 8-27](/Figures/08-27_UpdateWOForecast_DropDown_AX7-01.png)


---


### Procurement

In Enterprise Asset Management, you can get an overview of purchase requisitions and purchase orders related to work orders. It is also possible to create a purchase order or a purchase requisition from a work order.

In the **Work order purchase requisition** list (**Enterprise asset management** > **Common** > **Procurement** > **Work order purchase requisition**), you see a list of purchase requisitions related to work orders.


- Select a work order line in the **Work order purchase requisition** list, and click the **Purchase requisition** button to open the related purchase requisition.


- Select a work order line in the **Work order purchase requisition** list, and click the **Work order** button to open the related work order.


- Select a work order line in the **Work order purchase requisition** list, and click the **Item where used** button if you want to get an overview of where the item on the selected line is used in Enterprise Asset Management in relation to objects, job type setup, spare parts, and work orders. Read more about this overview in the [Items Where Used](20_ControllingAndReporting.md#items-where-used) section.



![Figure 8-28](/Figures/08-28_WO_PurchaseRequisition_List_AX7-01.png)


In the **Work order purchase** list (**Enterprise asset management** > **Common** > **Procurement** > **Work order purchase**), you can see a list of purchase orders related to work orders.


- Select a work order line in the **Work order purchase** list, and click the **Purchase order** button to open the related purchase order.



- Select a work order line in the **Work order purchase** list, and click the **Work order** button to open the related work order.



- Select a work order line in the **Work order purchase** list, and click the **Item where used** button if you want to get an overview of where the item on the selected line is used in Enterprise Asset Management in relation to objects, job type setup, spare parts, and work orders. Read more about this overview in the [Items Where Used](20_ControllingAndReporting.md#items-where-used) section.



![Figure 8-29](/Figures/08-29_WO_Purchase_List_AX7-01.png)


In the lists shown above, an icon regarding delivery date control is placed to the right on each line. If the icon shows an exclamation mark in a red circle, it means that delivery on the related purchase requisition or purchase order may be delayed.

On a purchase requisition, the date used to calculate possible delay is found in the **Purchase requisitions** form > **Purchase requisition header** FastTab > **Requested date** field. That date is compared with the available date on the work order or work order line in the same way as the purchase order date.

On a purchase order, the date used to calculate possible delay is the date related to the purchase order line, which shown in the **Purchase order** form > select purchase order line > **Line details** FastTab > **Setup** tab > **Confirmed delivery date** field. If that field is not filled out, the date in the **Delivery date** field on the **Purchase order header** FastTab is used. One of those dates is compared with the available date on the work order or work order line in the following order:


- Actual start date on the work order, or



- Scheduled start date on the related work order line, or



- Scheduled start date on the work order, or



- Expected start date on the work order



---


#### Create Purchase Order from a Work Order

In **All Work orders**, you select a work order line and create a related purchase order or a purchase requisition. This is done to ensure project relations between the purchase order or purchase requisition and the work order.


1. Click **Enterprise asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.
2. In the **All work orders** or **Active work orders** list, select the work order for which you want to create a purchase order, and click **Edit**.

3. In the **Work order** detail view > **Work order lines** FastTab, select the work order line for which you want to create the purchase order.
4. Click **Item tasks** > **Purchase orders**.

5. In the **Project purchase orders** grid view, click **Purchase order**.
6. Create the purchase order.


###### NOTE
Creating a purchase requisition is almost identical to creating a purchase order. The only difference is that in the above procedure, you click **Item tasks** > **Project purchase requisitions** in step 4, and in the **Project purchase requisitions** grid view, you click **Purchase requisition** and create the requisition.


---


#### Project Relation between Work Order and Purchase Order / Purchase Requisition

A purchase order line or purchase requisition line is related to a work order line via the work order project and the related project activity number. When you create a purchase order or purchase requisition from a work order line, the related project activity number is mandatory. The project activity number is automatically inserted on a purchase order or purchase requisition if the related work order contains work order lines that all use the same job type. If the work order lines contain different job types, the project activity number must be inserted manually.

To see or insert the activity number related to a purchase order line, open **Work order purchase** > select the purchase order record > click on the purchase order in the **Purchase order** column >  **Line details** FastTab > **Project** tab > **Activity number** field.



![Figure 8-30](/Figures/08-30_PurchaseOrder_Form_ActivityNumberField_AX7-01A.png)



Likewise, to see or insert the activity number related to a work order purchase requisition line, open **Work order purchase requisition** > select the purchase requisition record > click on the purchase requisition in the **Purchase requisition** column >  **Line details** FastTab > **Project** tab > **Activity number** field.


---


### Time Zones

Considerations regarding time zones are only relevant if objects in your company are located on several sites that are located in different time zones.

In Dynamics 365 for Finance and Operations, time zones can be set up on companies and sites. In Enterprise Asset Management, some tasks are based on the current user's or worker's preferred time zone, whereas work order scheduling is done based on the time zone of the object location.

Time zones are used in work order scheduling when you make capacity reservations. Generally, capacity reservations in Dynamics 365 for Finance and Operations are made without using time zones, but in Enterprise Asset Management, work order scheduling is done based on object locations when you make work order scheduling.


###### NOTE
An object is related to a resource. A resource is related to a resource group. The resource group is related to a site. The site is related to a time zone. If the site is not related to a time zone, the time zone set up on the company is used.

++Example - work order scheduling and time zones++: Company XYZ has headquarters in the United Kingdom (UK), in which the planning department is located. The company has production sites containing various objects (machines) in the UK as well as one site in the United States (USA). A planner is scheduling a work order for an object located in USA. Because the object on which work order scheduling is made is located in a different time zone than the planner, the dates and times scheduled on the work order are calculated based on the local time zone of the object location. This means that if the planner schedules a work order to be done Tuesday next week at 10:00 am, the work order is scheduled for 10:00 am local time on the object location.


Tasks performed by a worker on site, relating to actual work on objects and work orders such as:



- production stop registration



- loan object registration



- registration or update of scheduled/expected/actual start and stop time on work orders



- time line (overview on objects)


are based on the time zone selected for the worker. This may only cause problems if, for example, a worker creating a production stop registration on an object, is related to another time zone than the time zone defined for the object. In that case, the worker must manually calculate the correct time for the production stop registration, adding or subtracting a number of hours relative to the worker's local time, to register the correct production stop time for the object that corresponds with the object's time zone.


---


### Manual Update of Object Counters

Counters are used to create registrations on an object regarding, for example, number of hours in operation, or the number of quantities produced.

If the counter type selected for a counter is set to inherit counter values (**Enterprise asset management** > **Setup** > **Object types** > **Counters** > **General** FastTab > **Inherit counter values** check box), then, when you create a new counter line of that type, every sub object that uses the same counter type is automatically updated.

In **All objects**, you create hours or quantity counter registrations on an object, based on your readings on the object.


1. Click **Enterprise asset management** > **Common** > **Objects** > **All Objects**.
2. Select the object in the list, and click **Counters**. In the **Object counters** detail view, you will see a list of all previous counter registrations on the selected object.

3. Click **New** to create a new registration. The object ID is automatically inserted.
4. In the **Counter** field, select the relevant counter. Only counters related to the object type selected on the object are available. The related unit is automatically inserted in the Unit field.

5. Select date and time for the registration.
6. In the **Value** field, insert the number since the last counter registration, or, in the **Counter total** field, insert the total count number.


###### NOTE
If you physically install a new counter on an object, you need to register the change on the object in **Object counters**. Next, you must create two registration lines with identical timestamps, and on the line regarding the new counter, you select the **Counter replaced** check box. When you create the two registration lines, the first line must be for the counter that you are replacing. In the **Totals** field, the total count number is the sum of the counter total of all registered values on that counter type.

If the **Counter replaced** check box is selected on an object using a maintenance sequence with a "Once from..." or "Once reached..." interval type, the counter is still active on the new counter line because you create a separate counter line and start over with a new counter.


![Figure 8-31](/Figures/08-31_ObjectCounter_Form_AX7-01.png)


If you need to make counter registrations on several objects, that can be done in **Enterprise asset management** > **Inquiries** > **Objects** > **Object counters**.


##### NOTE
You can set up a range to define deviations in manual counter registrations, and the type of message that should be displayed if registrations are outside the defined range. Refer to the [Counters](06_Objects.md#counters) section regarding setup of counters.


---


### Automatic Update of Object Counters

In the previous section, manual registration of object counters is described. Setup of object counters is described in the [Counters](06_Objects.md#counters) section.

Counter values can also be automatically updated from production registrations, based on production hours or production quantity. This is done in **Update object counters**. You can update one or several objects by selecting one parameter, **From date**. This parameter specifies the start date for production registrations (hours or quantity produced), meaning the start date from which counter values should be updated.

All objects that are related to a resource ++and++ have object counters, which are set up to be updated based on produced quantity or production hours, will be included in an automatic update, and new counter values will be created.

Regarding counters based on production quantity, good quantity as well as error quantity registered are included in the count. If the unit used for produced quantity registration is different from the unit used on the counter, quantity is converted to correspond with the counter unit.

As mentioned above, automatic counters can be updated from production registrations. Therefore, the object for which you want to automatically update counters must be related to a resource (machine). The following descriptions provide an overview of the setup and processing of production orders (in the **Production control** module), which is used as a basis for automatic update of counters on an object in the **Enterprise asset management** module.

When produced quantities or production hours have been registered on the resource, you can update the related object counters.


1. Click **Enterprise asset management** > **Periodic** > **Objects** > **Update object counters**.
2. Select the start date of the automatic update in the **From date** field.
###### NOTE
The date in this field is the "work in progress" date from **Route transactions** (**Production control** > **Inquiries and reports** > **Production** > **Route transactions** > **Physical date** field).

3. If you want to select specific objects, object types, or resources for the automatic update, click **Filter** on the **Records to include** FastTab, and make the relevant selections.
4. If required, you can set up the automatic update as a batch job on the **Run in the background** FastTab.
![Figure 8-32](/Figures/08-32_AutomaticObjectCounters_Form_AX7-01.png)

5. When the automatic object counter update is done, you can see the counter registrations related to the object in **Object counters** (**Enterprise asset management** > **Common** > **Objects** > **All objects** > select object > **Counters** button).


In **Object counter totals**, you can get an overview of the latest registration made on all counter types on all objects. Click **Enterprise asset management** > **Inquiries** > **Objects** > **Object counter totals**. The view is very similar to **Object counters**, but you cannot add or edit registrations in **Object counter totals**. It is for overview only.


![Figure 8-33](/Figures/08-33_ObjectCounterTotals_Form_AX7-01.png)


###### NOTE
It is still possible to create manual counter value registrations for counter types that are automatically updated. Refer to the "Manual Update of Object Counters" section above for more information.

You can set up counters related to another counter, which means that when a counter is updated, related counters are automatically updated at the same time. Refer to the [Counters](06_Objects.md#counters) section regarding setup of related counters.


---


### Checklists
Checklists are set up on job types and used when you work on a work order. Filling out checklists and any related measurements is part of completing a work order. See the [Job Groups and Job Types, Variants, and Trades](08_Work_Orders.md#job-groups-and-job-types-variants-and-trades) section for more information on how to set up checklists on job types in the **Job type setup** form.

When you work with checklists on a work order you can fill out the predefined checklists that are related to job types. It is also possible to add additional checklists and measurements.


#### Fill Out a Checklist and Related Measurements


1. Click **Enterprise asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.
2. Select the work order and click **Checklist**.

3. In **Checklists**, you see checklists for all work order lines. If the work order lines have different job types, the checklists and measurements may be different on each work order line. Click on the work order line number that you want to work with. The related checklist is shown on the **Checklist** FastTab, and the measurements related to the selected checklist are shown on the **Measurements** FastTab.
4. Complete all the checklists by selecting your name in the **Worker** field, and the date of the check in the **Date checked** field. Worker and date information may be mandatory on a checklist.

5. If required, you can insert a note related to the selected checklist on the **Notes** tab. If notes have been made on a checklist, the **Note** check box is automatically selected on a checklist line.
6. If measurements are related to the checklist, fill out required measurement data on the **Measurements** FastTab in the **Measured value** and **Unit** fields.


###### NOTE
If you want to discard a checklist because it is not relevant for the work order line, select the **N/A** check box on the checklist line.



#### Add Checklists and Measurements

You can add checklists and related measurements to a work order line.


1. In **Checklists**, select the work order line number for which you want to add a checklist.
2. Click **Add** line on the **Checklist** FastTab.

3. Insert a name for the checklist, and fill out the **Worker**, **Worker mandatory**, **Date checked**, and **Date mandatory** fields and check boxes as required. You can insert a note on the **Notes** tab.
4. If you want to add measurements to the checklist, make sure that you have selected the checklist on the **Checklist** FastTab. Click **Add line** on the **Measurements** FastTab.

5. Fill in the measurement fields.


###### NOTE
In **Checklists**, you cannot delete checklists with the reference "Job type" and related measurements. You can only delete checklists and measurements with the reference "Manual", which you or other workers have created manually.

The text at the top of the **Checklist** FastTab that starts with a number, indicates which checklist line is selected. This is useful if many checklists are related to the work order.



![Figure 8-34](/Figures/08-34_Checklists_FromWO_Form_AX7-01.png)


---


### Production Stop

You can create production stops on the object selected on a work order. This is useful if you want to register production stop on one or more machines in the production area. First, you create the production stop types that you want to use, for example, breakdown and planned stop. This is done in **Production stop types**. Next, you can create production stop lines in **Production stop** and add the relevant production stop types.


#### Create Production Stop Types


1. Click **Enterprise asset management** > **Setup** > **Work orders** > **Production stop types**.
2. Click **New**.

3. Insert an ID for the production stop type in the **Production stop type** field.
4. Insert a name in the **Name** field.

5. Select the **KPI include** check box if the stop type should be included in object KPI calculations. Generally, planned production stops should not be included in KPI calculations as they do not impact expected performance.
6. Click **Save**.


![Figure 8-35](/Figures/08-35_ProductionStopTypes_Form_AX7-01.png)


When you have created the production stop types you want to use, you can create production stop lines for work orders and objects.


---


#### Create Production Stops


1. Click **Enterprise asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.
2. Select the work order and click **Production stop**.

3. Click **New**.
4. Insert date and time interval for the production stop in the **From** and **To** fields.

5. When you leave the **To** field, the duration in hours is automatically inserted in the **Duration** field.
6. Select a stop type in the **Production stop type** field.

7. Repeat steps 3-6 if you want to add more production stop lines.
8. Click **Save**.



![Figure 8-36](/Figures/08-36_ProductionStop_Form_AX7-01.png)



The calendar used to calculate a production stop depends on your selection in the setup of objects and parameters. If a resource is selected on an object in **All Objects** > **Asset** FastTab > **Resource** field, the calendar set up for the associated resource group is used.


![Figure 8-37](/Figures/08-37_Object_Form_ResourceField_AX7-01A.png)


If no resource is selected on the object, the standard calendar selected in the **Enterprise asset management parameters** form is used.


![Figure 8-38](/Figures/08-38_EAM_Parameters_Form_StdCalendarField_AX7-01A.png)


Click **Enterprise asset management** > **Inquiries** > **Production stop** to see an overview of all production stops.


###### NOTE
All calendars used in the **Enterprise asset management** module are set up in **Organization administration** > **Setup** > **Calendars** > **Calendars**.


---


### Add Fault to Work Order

You can add faults set up in the fault designer to a work order. The object selected in the work order must contain object types that have one or more fault records connected to it. Read more about setup in the [Fault Management](#fault-management) section.


1. Click **Enterprise asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.
2. In the list, select the work order on which you want to make a fault registration and click **Object fault**.

3. On the **Symptoms** FastTab, click **Add line**. A sequential fault number is automatically inserted in the **Fault** field.
4. Select the relevant symptom in the **Fault symptom** field.

5. Select **Fault area** and **Fault type** in the relevant fields.
6. In the **Fault date** field, the current date is automatically inserted. You can select another date, if necessary.

7. On the **Cause** FastTab, add a line describing the cause of the problem.
8. On the **Remedy** FastTab, add a line describing a possible solution to the problem.

9. Click **Save**.


![Figure 8-39](/Figures/08-39_ObjectFaults_Form_AX7-01.png)


#### View Object Faults

In the **Object faults** list, you can get an overview of all faults registered on objects.

Click **Enterprise asset management** > **Inquiries** > **Object fault** > **Object faults** to open the list.


---


#### Print Object Fault Report

From the **All objects** grid view, you can print an object fault report displaying all fault registrations as well as a graphic overview of fault statistics.


1. Click **Enterprise asset management** > **Common** > **Objects** > **All objects**.
2. In the **Objects** list, select the object for which you want to print a fault report.

3. On the **General** tab, click **Object fault**.
4. If required, insert a specific period or select a fault type.

5. Click **OK** to print the report.


###### NOTE
You can also print a fault report for several objects or object types by clicking **Enterprise asset management** > **Reports** > **Objects** > **Object fault**.


---


### Work Order Report

You can generate a work order report that shows detailed information about a work order. It is possible to select one or several work orders to be displayed in the report.


1. Click **Enterprise asset management** > **Reports** > **Work orders** > **Work order report**.
2. Select check boxes and fill out fields in the **Parameters** section, as required, to determine the details to be included in the report.

  a. In the **Print settings** section, you can select if you want to include attachments from the related job type setup in the print. Double-sided print is also available.
4. On the **Records to include** FastTab, you can filter the contents of the report by **Work order**.

5. If required, you can set up work order report generation as a batch job by filling out the fields on the **Run in the background** FastTab.
6. Click **OK** to generate the report.


Below you see an example of the how parameters can be set up, and the related work order report.


![Figure 8-40](/Figures/08-40_WO_Report_Dropdown_AX7_v103-002.png)


![Figure 8-41](/Figures/08-41_WO_Report_AX7-01.png)


---


### Work Order Pools

You can use work order pools to group work orders that have something in common. For example, you can create work order pools for


- work crews, for example, Maintenance Crew A, Maintenance Crew B



- professional skills, for example, electricians or plumbers



- physical locations



- time schedules, for example, weeks or other periods



If required, one work order can be placed in many work order pools.



###### NOTE
In the [Job Groups and Job Types, Variants, and Trades](#job-groups-and-job-types-variants-and-trades) section, job types can also be grouped. Job groups relate specifically to job types used in your company (such as service, maintenance, overhaul) whereas work order pools can be used for grouping on a wider scale, as suggested in the above list.


#### Create Work Order Pool

In **All work order pools** or **Active work order pools**, you can get an overview of your work order pools and create new pools.


1. Click **Enterprise asset management** > **Common** > **Work order pools** > **All work order pools** or **Active work order pools**.
2. Click **Work order pool**.

3. Insert a work order pool ID in the **Pool** field and a name in the **Name** field.
4. Select the **Active** check box to indicate that the work order pool is active.

5. Select the **Delete work order relations** check box if you want work orders to be automatically removed from the work order pool.
6. In the **Delete stage** field, select the work order stage. For example, the work order stage for completing a work order could be set to automatically delete relations to work order pools.

7. You can start adding work orders to your work order pool right away. On the **Work orders** FastTab, click **Add line**.
8. Select a work order in the **Work order** field. The related fields are automatically updated.

9. Repeat steps 7-8 if you want to add more work orders.
10. In the **Sort order** field, you can indicate if the work orders should be carried out in a certain order. Insert numbers 1, 2, 3, and so on to indicate a specific sequence for the selected work orders.

11. Click the **Work orders** button to see a list of all the work orders included in the work order pool.
12. Click the **Capacity load** button to open **Capacity load** to calculate and view capacity load for object calendar lines, not scheduled work orders, and scheduled work orders. This calculation only includes the objects related to the work order pool.

13. Click the **Item forecast** button to open **Item forecast** to calculate and view forecasts for items (spare parts and other required items) related to object calendar lines, not scheduled work orders, and scheduled work orders. This calculation only includes the objects related to the work order pool.
14. Click the **Work order purchase requisition** button to open the **Work order purchase requisition** list to see a list of purchase requisitions related to the work orders in the work order pool.

15. Click the **Work order purchase** button to open the **Work order purchase** list to see a list of purchase orders related to the work orders in the work order pool.


###### NOTE
When a work order pool is no longer relevant for your work planning, clear the **Active** check box.

Select the **Delete work order relations** check box if you want to delete all work order lines, for example to create an empty pool that you can later use for other work orders. Remember to clear the **Delete work order relations** check box if you want to use the work order pool to create new work order relations later.


![Figure 8-42](/Figures/08-42_AllWorkOrderPools_List_AX7-01.png)


#### Add Work Order to a Work Order Pool

As described in the section above, you can add work orders to a work order pool when you create the pool. You can also add a work order to a work order pool from one of the **All work orders** list.


1. Click **Enterprise asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.
2. Select the work order in the list, and click **Work order pool**.

3. Select "Add" in the **Add/remove** field.
4. Select the work order pool in the **Pool** field.

5. Click **OK**.
6. After you have added a work order to a work order pool, if you want to place the work order in a specific sequence in the pool: Open one of the work order pools grid views, select the pool and click **Edit**, and adjust the sort order of the work orders included in pool in the **Work order pool** detail view > **Work orders** FastTab > **Sort order** field.


###### NOTE
If you want to remove the selected work order from a work order pool, select "Remove" in step 3.


---


### Active Work Order Lines Overview

In **Active work order lines**, you can get an overview of work orders in relation to how many work orders have been created on specific objects, object types, products, models, job types, and so on. If you select a work order line and click **Edit**, you open the related work order. If you select a line and click one of the buttons on the **Work order lines** tab, you see data for the work order to which the work order line is related.

Click **Enterprise asset management** > **Common** > **Active work order lines** to open the list. The list contains all active work order lines and displays some of the information related to the work order or work order line.

In the **%** column, a number indicates completion of the work order in percent. Completion is based on two calculations: Posted hours compared to forecast hours, and number of checklists completed.


![Figure 8-43](/Figures/08-43_ActiveWorkOrderLines_List_AX7-01.png)


###### NOTE
For a short description of the buttons in **Active work order lines**, refer to the [Introduction to Work Orders](#introduction-to-work-orders) section in which identical buttons are described.


---


### Work Orders and Fixed Assets

In Enterprise Asset Management, objects can be related to fixed assets, and you can create work orders for those objects. If you use this functionality, you can get a complete overview of fixed assets, related investment projects, and the costs registered on the investment projects in the **Project management and accounting** module and the **Fixed assets** module in Dynamics 365 for Finance and Operations.


###### NOTE
The **Fixed asset number** field is only filled out on the work order line project if type "Investment" is selected as the project type on the work order line project.


![Figure 8-44](/Figures/08-44_FixedAssets_Investment_AX7-001A.png)


The following procedure describes the relation between objects, work orders, work order line projects, and fixed assets.


1. You create an object that you relate to a fixed asset.
![Figure 8-45](/Figures/08-45_FixedAssets_Investment_AX7-003AA.png)
2. When you set up work order types (**Enterprise asset management** > **Setup** > **Work orders** > **Work order types**), you create a work order type for handling investments. See also the [Work Order Types](08_Work_Orders.md#work-order-types) section.
![Figure 8-46](/Figures/08-46_FixedAssets_Investment_AX7-004A.png)

3. When you set up work order project groups (**Enterprise asset management** > **Setup** > **Work orders** > **Project setup** > **Project group** link), you create a relation between the work order type used for investments and the project group created for investments in the **Project management and accounting** module (**Project management and accounting** > **Setup** > **Posting** > **Project groups**).
![Figure 8-47](/Figures/08-47_FixedAssets_Investment_AX7-005A.png)
4. When you create a work order that relates to a fixed asset object, you select the work order type used for handling investments, for example, "Investment".

5. When the work order is created, the related work order type is shown in **All work orders**.
![Figure 8-48](/Figures/08-48_FixedAssets_Investment_AX7-006AA.png)
6. When the work order is created, the project related to the work order is shown in the **Project management and accounting** module in the **All projects** list. Click on a project ID in the list and you will see project-related information on the project record as well as a reference to the fixed asset to which the object on the work order is related (**Project management and accounting** > **Projects** > **All projects** > Click on a project ID in the list > **General** FastTab and **Setup** FastTab).
![Figure 8-49](/Figures/08-49_FixedAssets_Investment_AX7-007AA.png)
7. In **Fixed assets**, you are able to see an overview of the projects associated with a fixed asset (**Fixed assets** > **Fixed assets** > **Fixed assets** > click on the fixed asset in the **Fixed asset number** field > **Associated projects** FactBox).

![Figure 8-50](/Figures/08-50_FixedAssets_Investment_AX7-008AA.png)

