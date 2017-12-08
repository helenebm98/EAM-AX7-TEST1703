# Objects



An object is any type of equipment, for example a machine or machine part, which requires maintenance, service, or repair.



An object is automatically updated with related information regarding, for example, new or updated work orders. Objects can be created from the **All Objects** or **Pending objects** menu items, which is described in the [Create Objects Based on Purchace or Sales Orders](#create-objects-based-on-purchase-or-sales-orders) section.


---

### Object Types
Object types are used as general object categorizations, for example, CNC machines, measuring equipment, and truck engines. Object types are used to manage which job types (maintenanceservice tasks), object stages, object counters, object specification types, condition assessment templates, and product models can be selected on an object. When you create an object, the object type is mandatory.

For each object type, variations of object type setup can be created. Example: If you have an object type called "Trucks", you can create variations of that object type relating to products and product models, and add required spare parts and maintenance sequences to each object type setup.

First, you set up the required object types. Next, you create the product models to be related to the object types. Then, you create all the variations of object types that are required for your equipment in the **Object type setup** form.


#### Create Object Type

1. Click **Enterprise asset management** > **Setup** > **Objects** > **Object types** > **Object types**.

2. Click **New** to create an object type.



3. Insert an object type ID in the **Object type** field and a name in the **Name** field.

4. Select a stage group in the **Object stage group** field. Refer to the [Object Stages](#object-stages) section for more information on object stages and stage groups.



5. Select the **Total** check box if you want to calculate summarized KPI values for objects with this object type.

6. Click **Save**.



7. On the **Job types** FastTab, select the job types that should be related to the object type. This is done by clicking on a job type in the **Job types remaining** section and clicking the **<** button.

8. If you want to select all available job types, click the **<<** button. All job types are transferred to the **Job types selected** section.



9. If you want to remove a job type from the **Job types selected** list, select the job type and click the **>** button.

10. Just as with job types, you can select counters to be related to the object type. On the **Counters** FastTab, make your selections the same way as described in steps 7-9. Read more about the setup of counters in the [Counters](#counters) section.



11. Just as with job types, you can select specification types to be related to the object type. On the **Specification types** FastTab, make your selections the same way as described in steps 7-9. Select a specification type in the **Specification types selected** field, and use the **Move up** and **Move down** buttons to create the preferred sequence of specification types. The sequence of specification types will be shown on objects using this object type. Read more about object specifications in the [Object Specifications](#object-specifications) section.
   ###### NOTE
   When you add new specification types on this FastTab, existing objects are automatically updated with that information.

12. Just as with job types, you can select condition assessment templates to be related to the object type. On the **Condition assessments** FastTab, make your selections the same way as described in steps 7-9. Read more about condition assessment templates and registrations in the [Condition Assessment](#condition-assessment) section.

13. On the **Product - model** FastTab, all product model combinations set up on the selected object type are shown. Click the **Product - model** button to open the **Product - model** view if you want to see the product - model combinations divided by product. You can add model - object type relations in that form. It is also possible to add product - model relations to an object type directly in **Object types**. Finally, you can also create new product - model - object type relations in **Enterprise asset management** > **Setup** > **Objects** > **Product - model**. As you can see from this description, there are three ways of working with setting up and editing product - model - object type relations. All available combinations are shown from different perspectives, and you can select your preferred point of entry when working with this setup.





###### NOTE

If you select counters on an object type, the selections are automatically updated in **Counters** (**Enterprise asset management** > **Setup** > **Objects** > **Object types** > **Counters**).



The fields in the **Details** group shown at the top of the form show number of job types, counters, specification types, and so on, set up on the selected object type.





---





Manually created work orders typically relate to corrective maintenance. Work orders created automatically typically relate to preventive maintenance. When you create work orders manually, only the job types selected in **Object types**, on the **Job types** FastTab, can be used. However, automatically created work orders can use all the job types you have created in **Job types** (**Enterprise asset management** > **Setup** > **Work orders** > **Jobs** > **Job types**).





![Figure 6-01](/Figures/06-01_ObjectTypes_Form_AX7_laptopscreen-01.png)





#### Create Object Type Setup Lines



1. Click **Enterprise asset management** > **Setup** > **Objects** > **Object types** > **Object type setup**, or **Enterprise asset management** > **Setup** > **Objects** > **Object types** > **Object types** > select an object type > **Object type setup** button.

2. The first time you use this form, the **Create combinations** button may be useful. You can use it to quickly create all combinations of a product model on an object type. Click the **Create combinations** button, select the object type for which you want to create combinations, and click **OK**.

###### NOTE

If you are not going to use all object type setup combinations that was automatically created, you can delete a setup by selecting it and clicking **Delete**.



3. Click **New** to manually create a new object type setup.

4. Depending on how specific the object type setup should be, make selections in the **Object type**, **Product**, and **Model** fields.



5. If a warranty agreement is related to the object type, select the agreement in the **Vendor warranty** and **Customer warranty** fields. Read more about how to set up warranty in the [Warranty](18_Warranty.md#warranty) chapter.

6. On the **Spare parts** FastTab, click the **Add** button to add spare parts to the selected object type setup.



7. On the **Spare parts** FastTab, select a spare part line, and click **Approve** if you want to approve the spare part. It is possible to select multiple lines for approval.

8. On the **Spare parts** FastTab, select a spare part line, and click **Item where used** if you want to open the **Item where used** view to check if the selected spare part is used elsewhere in Enterprise Asset Management, for example, in relation to objects and work orders. Read more about this overview in the [Items Where Used](20_ControllingAndReporting.md#items-where-used) section. Select the **Active** check box to see all active spare parts in the list. Select the **Approved** check box to see only approved spare parts in the list.



9. On the **Maintenance sequences** FastTab, click **Add** to add maintenance sequences to the selected object type setup.

10. Use the copy function if you want to copy an object type setup to another setup. First, select the object type setup to which you want to copy a new setup. Then, click **Copy setup**, and select the object type setup from which you want to copy contents. The check boxes determine how much information you want to include. Select **OK** to copy.





###### NOTE
If you have many spare parts lines and maintenance sequence lines that you are going to reuse, the copy function is a quick and easy way to set up data for many object type setup combinations.

![Figure 6-02](/Figures/06-02_ObjectTypeSetup_Form_AX7-01.png)


#### Spare Parts on Object Type Setup

As described in the "Create Object Type Setup Lines" section above, spare parts are set up in **Object type setup** on product models. This means that when you open Object type setup, you only see the spare parts related to the selected object type - product - model combination. If you want to see a list of all spare part records, click **Enterprise asset management** > **Inquiries** > **Spare parts**.

It is also possible to create new spare parts for existing object type - product - model combinations in the **Spare parts** form. Whether you prefer creating those records in the **Object type setup** view, in which you have a better overview of data on the selected object type - product - model combination, or you prefer the complete overview of all object type setup lines in the **Spare parts** view when creating new records, is up to you. If **Spare parts** contains many records, it may provide at better overview to use **Object type setup**.

Click **Item where used** if you want to open **Item where used** to check if the spare part on the selected line is used elsewhere in Enterprise Asset Management, for example, in relation to objects and work orders. Read more about this overview in the [Items Where Used](20_ControllingAndReporting.md#items-where-used) section.


![Figure 6-03](/Figures/06-03_SpareParts_Form_AX7-01.png)


---


### Object Specifications

Object specifications are used to describe properties related to an object type or object. You can set up all kinds of object-related specifications. For example, for a machine you can create specifications regarding engine volume, power consumption, oil capacity, and maximum load capacity under different conditions.

First you create the specification types required for your equipment, which is described in this section. Next step is to select object specifications on an object type, which is described in the **Object Types** section. When you have attached object specifications to an object type, the specifications are automatically transferred to objects using that object type.


#### Create Specification Types



You can create your own specification types, but you can also transfer product dimensions from Dynamics 365 for Finance and Operations to **Specification types**.



1. Click **Enterprise asset management** > **Setup** > **Objects** > **Object types** > **Specification types**.

2. First time you set up specification types, click **Create product dimensions** to automatically transfer standard Dynamics 365 for Finance and Operations product dimensions.



3. Click **New** to create a new specification type.

4. Insert a name for the specification type in the **Specification type** field.



5. Insert a description in the **Description** field.

6. If required, select the relevant specification unit in the **Unit** field.



7. In the **Data type** field, select a data type for the unit.

8. If the specification type has the data type "String", you can create values for the specification type by selecting it and clicking the **Values** button.





   a. In **Specification values**, click **New**.







   b. Select a specification type (dimension) in the **Specification type** field.







   c. Insert a related value in the **Value** field.







   d. Insert a description in the **Description** field.







9. In the **Functional location types** field, the number of functional location using the specification type is shown.

10. In the **Object types** field, the number of object types using the specification type is shown.





![Figure 6-04](/Figures/06-04_SpecificationTypes_Form_AX7-01.png)





![Figure 6-05](/Figures/06-05_SpecificationValues_Form_AX7.png)





#### Set Up Specification Types on an Object



You can also select specification types directly on an object.



1. Click **Enterprise asset management** > **Common** > **Objects** > **All objects** or **Active objects**.

2. In the **All objects** grid view, select the object to which you want to add an object specification.



3. On the **General** tab, click **Specifications**.

4. Click **New** to create a new specification type. The selected object is automatically selected in the **Object** field, but you can select another object ID, if required.



5. Select the type in the **Specification type** field. The matching description, data type, and unit are automatically inserted.

6. In the **Value** field, insert the figure or number that is valid for the object regarding the current specification.





![Figure 6-06](/Figures/06-06_ObjectSpecifications_Form_AX7-01.png)



###### NOTE



You can get an overview of object specification types and their relation to the objects in **Object specifications** and **Object specification overview**. Refer to the [Object Specification Overview](#object-specification-overview) section for more information.





---





### Condition Assessment



Condition assessment is performed at regular intervals, and the primary objective is to create and maintain condition data on objects. Seen from a preventive maintenance perspective, it is important to monitor key information such as current condition, and remaining life span. Furthermore, if you carry out condition assessment at regular intervals, you will be able to monitor and compare conditions on the machinery in your factory.



Condition assessment can be used to measure and monitor many conditions on your equipment. Example: You could measure vibrations on your machinery. After you have registered vibration measurements in Enterprise Asset Management on various types of equipment, you can search for the latest registered assessment and view vibration measurements.



Condition assessment is created on objects. You set up a condition assessment template on an object type before you carry out the condition assessment procedure. The reason for using templates for condition assessment is to avoid variation of condition data on similar objects. The sequence for setting up and using condition assessment in Enterprise Asset Management is: First you set up the required condition assessment templates. Next, you associate templates with object types in the **Object types** form. Finally, you can create condition assessment registrations on an object in the **Object** form.





#### Create a Condition Assessment Template



1. Click **Enterprise asset management** > **Setup** > **Objects** > **Object types** > **Condition assessment**.

2. Click **New** to create a new template.



3. Insert and ID for the template in the **Template** field.

4. Insert a name for the template in the **Name** field.



5. On the **Condition assessment lines** FastFab, add the lines required for the condition assessment, including selection of the appropriate condition type and measurement unit.

6. On the **Object types** FastTab, add the object types that should use the condition assessment template.



7. In the **Lines** and **Object types** fields in the **Details** group, you will see the number of assessment lines and object types related to the selected condition assessment template.





![Figure 6-07](/Figures/06-07_ConditionAssessTemplate_Form_AX7-01.png)





#### Create Condition Assessment Registration on an Object



1. **Click Enterprise asset management** > **Common** > **Objects** > **All Objects**.

2. In the list, select the object for which you want to create a condition assessment registration.



3. On the **General** tab, click **Condition assessment**.

4. Click **New** to make a new registration.



5. Select the date for the condition assessment in the **Date** field.

6. Select the name of the worker who carried out the assessment registration in the **Worker** field.



7. In the **Lines** field, you see the number of assessment lines set up on the condition assessment.

8. Select a template for the condition assessment in the **Template** field. The name of the template is automatically inserted in the **Name** field, and the related registration lines are inserted on the **Condition assessment lines** FastTab.



9. You can insert notes relating to the selected condition assessment on the **Notes** FastTab.

10. For each condition assessment line, insert measurement data in the **Value** field.



11. You can insert a comment relating to the selected registration line on the **Condition assessment lines** FastTab > **Comments** tab. If you add a comment on a line, the Comment check box is automatically selected.





![Figure 6-08](/Figures/06-08_ConditionAssessment_Form_AX7-01.png)





After you have made a condition assessment registration on an object, you can print a condition assessment report.





###### NOTE



You can also register condition assessment on a work order (**Enterprise asset management** > **Common** > **Work orders** > **All Work orders** > **Condition assessment** button.)





---





### Product Model



Product and model setup is used to specify products and related models. Models can be related to object types. This section describes how to create product and model relations.





#### Set Up Product - Model Relations



1. Click **Enterprise asset management** > **Setup** > **Objects** > **Product - model**.

2. Click **New** to create a new product.



3. Insert a product name in the **Product** field, and a description in the **Description** field.

4. On the **Models** FastTab, click **Add** to create a model to be related to the product.



5. Insert a model name in the **Model** field and a description in the **Description** field.

6. In the **Object type** field, select the object type to which the product model should be related.

##### NOTE

You can also setup object type - product - model relations in **Object types**.



7. In the **Details** group > **Models** field, you see the number of product models set up on the selected product.

8. In the **Details** group > **Objects** field, you see the number of objects using the selected product.



9. In the **Objects** field, you see the number of objects using the product model.





![Figure 6-09](/Figures/06-09_ProductModel_Form_AX7-01.png)





##### NOTE



An object type can have no product model relations, or be related to one product model, or several product models. If an object type is related to at least one product model, only the specific combinations set up in **Product - model** can be selected in the views in Enterprise Asset Management in which a combination of object type - product - model can be set up, for example, **All objects**, **Object priorities**, **Job type setup**, and **Maintenance budget lines**. If some object types are not related to any product model, only those object types, and product models that also have no relation to object types are shown.





#### Select Product - Model on an Object



1. Click **Enterprise asset management** > **Common** > **Objects** > **All Objects**.

2. Select the object by clicking on the link in the Object column (to go to Details view).



3. Click **Edit**.

4. On the **General** FastTab, make your selections in the **Product** and **Model** fields.





---





### Counters



Counters are used to make counter registrations on objects, for example, regarding number of production hours, or quantity produced on the object. Object types are related to the counters. This means that a counter can only be used on an object if the counter is set up on the object type used on the object.



Before you can make counter registrations on objects, you first create the counters you want to use in **Counters**. Next, you can create counter registrations on objects in **Object counters**, which is described in [Manual Update of Object Counters](08_Work_Orders.md#manual-update-of-object-counters) and [Automatic Update of Object Counters](08_Work_Orders.md#automatic-update-of-object-counters) sections.



Counters can be used on maintenance sequences. A maintenance sequence line can be of type "Counter", for example, relating to number of production hours or quantity produced. Refer to the [Maintenance Sequences](11_Preventive_Reactive_Maint.md#maintenance-sequences) section for more information on maintenance sequences using counters.



A counter can be updated manually or automatically based on production hours or quantity produced. A counter can be set up to use one of three update methods (selected in the **Update** field in **Counters**):





- Manual - you must manually register counter values.



- Production hours - the counter is automatically updated based on number of production hours.



- Production quantity - the counter is automatically updated based on number of quantity produced.





---



###### NOTE



If quantity produced is used, *all* registered items are included in the count, good quantity as well as error quantity. It is always possible to make manual counter registrations, if required.





#### Create Counter Types for Object Counter Registrations



1. Click **Enterprise asset management** > **Setup** > **Objects** > **Object types** > **Counters**.

2. Click **New** to create a new counter type.



3. Insert a counter ID in the **Counter** field, and a counter name in the **Name** field.

4. On the **General** FastTab, select a counter unit in the **Unit** field.



5. In the **Update** field, select the update method to be used for the counter.

6. Select the **Inherit counter values** check box if sub objects in a hierarchical object structure should automatically inherit counter registrations made on the parent object.



7. In the **Total aggregate** field, select the summation method to be used for a counter using this counter type. "Sum" is the standard selection used to continuously add registered counter values to the total value. "Average" can be used if an object counter is set up to monitor a threshold, for example, regarding temperature, vibrations, or wear and tear on an object. In the screenshot below, a "Temperature" counter type is shown, and for that counter type, it is relevant to get an overview of the average value measured over time.

8. In the **Deviation over** field, insert the upper level in percent for validating if manual counter registrations are within an expected range. The validation is based on a linear increase in existing counter registrations.



9. In the **Deviation under** field, insert the lower level in percent for validating if manual counter registrations are within an expected range. The validation is based on a linear decrease in existing counter registrations.

10. In the **Type** field, select the type of message (information, warning, error) to be shown if deviations outside the defined range occur when you make manual counter registrations.



11. On the **Object types** FastTab, add the object types that should be able to use the counters.

12. On the **Related counters** FastTab, add the counters that you want to be automatically updated when this counter is updated.





###### NOTE



A related counter is only automatically updated if the related counter has the object type, to which it is related, in the counter setup.



**Example:** You set up a counter for "Production hours" and add the object type "Truck Engine". When that counter is updated, a related counter "Oil" is also updated with the same counter values. The setup in **Counters** includes the setup on "Hours". Also, on the "Oil" counter, the object type "Truck Engine" should be added to the **Object types** FastTab to ensure the counter relation. See the screenshot below for the setup on the Hours and Oil counters.



When object types are added to a counter in **Counters**, that counter is automatically added to the object types on the **Counters** FastTab in [Object Types](#object-types).



![Figure 6-10](/Figures/06-10_Counters_Form-01_AX7-002.png)



![Figure 6-11](/Figures/06-11_Counters_Form-oil-01-02A_AX7.png)



Read more about manual and automatic counter registrations in the [Manual Update of Object Counters](08_Work_Orders.md#manual-update-of-object-counters) and [Automatic Update of Object Counters](08_Work_Orders.md#automatic-update-of-object-counters) sections.





---





### Enterprise Asset Management Parameters



In Enterprise Asset Management, general parameters relating to objects, work orders, and work order scheduling must be set up. Click **Enterprise asset management** > **Setup** > **Enterprise asset management parameters** to open the form.



The **Create data wizard** button can be used to automatically create setup data for test or demo data purposes in a company in Dynamics 365 for Finance and Operations. Refer to our white paper "Set up Test Data in Enterprise Asset Management" for information on how to use the wizard.





**Objects** link



- **Default functional location** is the standard functional location, which is automatically selected on objects when you create new objects.



- In the **Standard calendar** field, select a calendar to be used for calculating object KPIs, in case no resource is selected on an object.



- In the **View** field, select the standard view that is shown when you open the **Object view** form (**Enterprise asset management** > **Common** > **Objects** > **Object view**).



- **Default request type** is the standard request type, which is automatically selected when you create a new request.



- If you want to create projects that relate to objects, project relations regarding selection of **Main project**, **Project hierarchy**, and the option to **Auto create projects** are set up in **Enterprise asset management parameters**.



- In the **Work order project mask** field, you define the number of sub projects allowed for work orders and sub-objects. A work order mask is used to define how many work orders can be created on an object and used on the related work order line project. The work order mask is set up in the **Work order project mask field** in **Enterprise asset management parameters** (**Enterprise asset management** > **Setup** > **Enterprise asset management parameters** > **Work orders**).'





###### NOTE



The format for a work order project mask is a number of hash signs (#), depending on the maximum number of work orders you expect to create on an object. Example: ## allows you to create up to 99 sub-projects.



- Forecasts on job types are stored on the project selected in the **Forecast project** field. For each job type, a new activity is automatically created on the forecast project. Forecasts on the job type are then saved on the forecast project.



- In the **Model** field, select the forecast model used on job type and work order forecasts.



![Figure 6-12](/Figures/06-12_EAM_Parameters_Form-01_AX7_v103.png)





**Work orders** link



- **Default work order type** defines standard settings when creating a work order.



- **Preventive work order type** defines the work order type used when creating work orders from object calendar lines. If this field is left blank, the work order type in the **Default work order type** field is used.



- In the **Related work order mask** field, you define the maximum number of work orders that can be related to a work order. In the example in the screenshot below, a work order can have up til 99 work orders related. If you define a mask as shown in this field, related work orders will be numbered [work order ID of the work order to which a work order is related]-01, -02, -03, and so on. If you do not define a mask in this field, a related work order will get the next sequential work order ID.



- Select the **Copy faults** check box if you want to automatically copy faults registered on work orders to related requests.



- In the **Level** field, you define the functional location level that is automatically inserted on a work order if all related work order lines refer to the same functional location. If the work order lines do not all relate to the same functional location on the defined level, the **Functional location** field is left blank on the work order. Example: If you insert the number "1" in this field, that is the top level in a functional location hierarchy. If you insert the number "0" in this field, you have not defined a specific functional location level, only that all work order lines on a work order must be related to the same functional location for that functional location to be added to the work order.



- Journals used when posting consumption on a work order can be selected on the **General** FastTab.



- In the **Product language source** field, select which language to use for product names in Enterprise asset management reports. You can select the language set up on the company account, or the language set up for the user currently logged in on Dynamics 365 for Finance and Operations.



- On the **Category** FastTab, default categories relating to consumption on work orders as well as consumption in connection with warranty can be defined.





![Figure 6-13](/Figures/06-13_EAM_Parameters_Form-02_AX7_v103.png)





**Work order scheduling** link



- **Schedule time fence** defines period in days, calculated from the expected start date of the work order, during which work order lines are planned.



- The **Master plan** relates to resources in the **Organization administration** module. If you select a master plan in this field, you will be able to see capacity reservations related to work orders in **Capacity reservations** (**Organization administration** > **Resources** > **Resources** > select resource > **Resource** tab > **Capacity reservations** button). If you leave this field blank, you will be able to see capacity load related to work orders in **Capacity load** (**Organization administration** > **Resources** > **Resources** > select resource > **Resource** tab > **Capacity load** button).



###### NOTE

The selection regarding using a master plan or not in the **Enterprise asset management module**, and the related form used to get an overview of capacity reservations or capacity load is standard Dynamics 365 for Finance and Operations setup. Depending on your setup in the **Master plan** field, you will be able to access capacity information in either **Capacity reservations** or **Capacity load** in the **Organization administration** module. It is not possible to create a setup in which capacity reservations are shown in both views.



The nine fields described below all relate to calculated rating scores, which are used to calculate work order priority during work order scheduling.



- **Priority** - a rating score calculated together with the rating score in the **Criticality** and **Start date** fields. The number in this field is divided by the number in the **Priority** field on a work order. Example: If the value "5.00" is inserted in this field, and a work order has priority "20", the rating score for priority is 0.25.



- **Criticality** - a rating score calculated together with the rating score in the **Priority** and **Start date** fields. The number in this field is multiplied by the number in the **Criticality** field on a work order. Example: If the value "10.00" is inserted in this field, and a work order has criticality "5", the rating score for criticality is 50.



- **Start date** - a rating score calculated together with the rating score in the **Priority** and **Criticality** fields. This field indicates daily score as a negative value and is compared to the **Expected start** field on a work order. Example: If the value "10.00" is inserted in this field, and the expected start date of a work order is three days from now, the rating result is minus 30.00. Adding the results of 0.25 and 50 from the examples in the **Priority** and **Criticality** fields described above provides a total of plus 20.25. That number is compared to all other work order rating scores during work order scheduling, and the highest rating scores are then planned first.



- **Responsible worker** - a rating score calculated together with the **Responsible worker group**, **Preferred worker**, **Preferred worker group**, **Object location**, and **Start date** rating score values. If the value "50.00" is inserted in this field, and a responsible worker has been selected on a work order, the worker gets 50 points in the overall worker calculation during work order scheduling.



- **Responsible worker group** - a rating score calculated together with the **Responsible worker**, **Preferred worker**, **Preferred worker group**, **Object location**, and **Start date** rating score values. If the value "50.00" is inserted in this field, and a responsible worker has been selected on a work order, the worker gets 50 points in the overall worker calculation during work order scheduling.



- **Preferred worker** - a rating score calculated together with the **Responsible worker**, **Preferred worker**, **Preferred worker group**, **Object location**, and **Start date** rating score values. The four rating scores are calculated and added together to provide a score used for selecting which worker should be assigned to which work order during work order scheduling. If the value "10.00" is inserted in this field, and a worker has been selected as preferred worker on a work order, that worker gets 10 points in the overall worker calculation during work order scheduling.



- **Preferred worker group** - a rating score calculated together with the **Responsible worker**, **Preferred worker**, **Preferred worker group**, **Object location**, and **Start date** rating score values. If the value "10.00" is inserted in this field, and a worker has been assigned to a preferred worker group selected on a work order, that worker gets 10 points in the overall worker calculation during work order scheduling.



- **Location** - rating score calculated together with the **Responsible worker**, **Preferred worker**, **Preferred worker group**, **Object location**, and **Start date** rating score values. If the value "3,000.00" is inserted in this field, a worker gets 3,000 points in the calculation if the worker is located in the same factory or facility as the object on which a job is to be scheduled.



###### NOTE

If your company uses functional locations, workers get full score if they are located on the functional location related to the object. If the functional location of the object has a parent object, workers on that functional location get 1/2 score. If that location also has a parent, workers on that location get 1/3 score. If that location also has a parent, workers on that location get 1/4 score, and so on.



If you company uses object location, which we do not recommend, location, area, and zone are used to calculate location scores. Workers get full score if they are located in the location and area and zone related to the object. If worker location only matches location and area, the rating score for the worker is 2/3 of the full score. If worker location only matches location, the rating score for the worker is 1/3 of the full score.



- **Start date** - rating score calculated together with the **Responsible worker**, **Preferred worker**, **Preferred worker group**, **Object location**, and **Start date** rating score values. This field indicates daily score as a negative value and is compared to the **Expected start** field on a work order. If the value "10.00" is inserted in this field, and the expected start date of a work order is tomorrow, the rating result is minus 10.00.



###### NOTE



Assuming that no responsible worker and responsible worker group have been selected on a work order to be scheduled - you add and subtract the rating score values in the examples in the **Preferred worker**, **Preferred worker group**, **Object location**, and **Start date** fields above, you get a total of 3,010.00. This means a high score for the worker who is already selected as preferred worker as well as included in the preferred worker group on the work order, and the worker is also located in the same facility as the object for which a job needs to be scheduled. All in all this means there is a good chance that the worker in question will be selected to complete the job during work order scheduling.



If the value "0.00" is inserted in one of the eight fields above, that rating score will not be used during work order scheduling.



In the screenshot below, on the **Work order score example** FastTab, you will see calculation examples based on the scores inserted in the **Priority**, **Criticality**, and **Start date** fields.





![Figure 6-14](/Figures/06-14_EAM_Parameters_Form-03_AX7_v103.png)





**License and configuration** link



- Here, you get an overview of the version numbers, licenses, and configuration keys related to your Enterprise Asset Management solution.



![Figure 6-15](/Figures/06-15_EAM_Parameters_Form-04_AX7_v103.png)





**Document types** link



- Select the document types that should be available for printing attachments related to a work order report. This is done by clicking on a document type in the **Available** section and clicking the ![Figure 6-16A](/Figures/06-16A_Button_Select_StageGroups.png) button. If you want to remove a selected document type, select the document type in the **Selected** section and click the ![Figure 6-16B](/Figures/06-16B_Button_Deselect_StageGroups.png) button.





![Figure 6-16](/Figures/06-16_EAM_Parameters_Form-05AA_AX7_v103.png)





**Number sequences** link



- Select the required number sequences in this section. There are two number sequences for objects: One for manually created objects, and one for objects created through pending objects.



![Figure 6-17](/Figures/06-17_EAM_Parameters_Form-06_AX7_v103.png)





---





### Object Stages





#### Stages and Stage Groups



Object stages are used to define if an object is active or inactive. For example, stages such as "Created", "Active", and "Terminated" can be set up.





###### NOTE



Request stages, described in the [Request Stages](07_Requests.md#request-stages) section, are linked to object stages. This means that when a request changes to a new stage, the object attached to the request changes the object stage accordingly. ++Example:++ If a request has the status "Inbound", the object changes the object stage to the stage selected in **Object stage groups** > **Object stage** FastTab > **Inbound stage** field. Refer to the screenshot of the **Object stage groups** form at the end of this section.



Refer to the [Requests](07_Requests.md#requests) chapter for more information on loan objects and depot repair.



Stages can be set up in stage groups, in which you can define required stages for different kinds of objects. First you set up stages. Next step is creating a stage group and selecting stages for the group.



1. Click **Enterprise asset management** > **Setup** > **Objects** > **Stage** > **Stages**.

2. Click **New** to create a new object stage.



3. Insert the stage ID in the **Stage** field, and a description in the **Name** field. In the **Stage groups** field, you can see the number of object stage groups that uses the object stage.

4. Select the **Active** check box if this should be an active stage in which work orders can be created for objects.



5. Select the **Delete open calendar lines** check box if open object calendar lines with stage "Created" should be deleted at this stage. This is useful if you want to clean up any open calendar lines that are no longer relevant for the object, for example, if the object is no longer active.





![Figure 6-18](/Figures/06-18_ObjectStages_Form_AX7-01.png)





###### NOTE



Object stages, stage groups, and types are related and used in the same way as work order stages, work order stage groups, and work order types. Refer to the [Work Order Stages](08_Work_Orders.md#work-order-stages) section for a general explanation regarding stage group, type, and stage relations.



When you have created the required object stages, you can set up stages in stage groups.



1. Click **Enterprise asset management** > **Objects** > **Stage** > **Stage groups**.

2. Click **New** to create a new object stage group.



3. Insert the stage group ID in the **Stage group** field, and a description in the **Name** field. In the **Stages** and **Object types** fields, you can see the number of stages selected in the stage group, and the number of object types that uses the stage group.

4. On the **Stages** FastTab, select the stages that should be included in the group. This is done by clicking on a stage in the **Stages remaining** section and clicking the ![Figure 6-19A](/Figures/06-19A_Button_Select_StageGroups.png) button.



5. If you want to select all the available stages for a group, click the ![Figure 6-19B](/Figures/06-19B_Button_SelectAll_StageGroups.png) button. All stages are transferred to the **Stages selected** section.

6. If you want to remove a selected stage from the group, select the stage in the **Stages selected** section and click the ![Figure 6-19C](/Figures/06-19C_Button_Deselect_StageGroups.png) button.



7. Click **Stage updates** to define which stages can follow a selected stage.

8. The **Object stage** FastTab is used if you handle objects that you receive for repair. In the **Inbound/outbound** section, you can select object stages to indicate the workflow of an object that you receive for repair. If you offer loan objects to customers or departments, you can also select stages for loan objects in the **Loan** section.





![Figure 6-19](/Figures/06-19_ObjectStageGroups_Form_AX7-01.png)





---





### Object Priorities



Object priority is related to objects and transferred to requests and work orders. Object priority can be changed, if required. Object priority is used to calculate work order priority during work order scheduling.



Refer to the [Enterprise Asset Management Parameters](#enterprise-asset-management-parameters) section for more information on the setup related to calculating rating scores for work order scheduling. You must set up at least one default record for object priority, which is used in case no other match is found during work order scheduling.



**Example 1:** The default priority in case no other match is found (set up in the third record in the **Object priorities** screenshot below).





**Example 2:** A high priority for scheduling jobs for a "Volvo" truck engine (set up in the first record in the **Object priorities** screenshot below).





#### Set Up Object Priorities



1. Click **Enterprise asset management** > **Setup** > **Object priorities**.

2. Click the **New** to create a new record.



3. Depending on the detail level for the object priority, make the relevant selections in the **Object type**, **Product**, **Model**, **Object**, and **Work order type** fields.

###### NOTE

When object priority is used for requests and work orders, Enterprise Asset Management goes through all object priority records to check for a possible match, always checking the most specific combination first. This means that, first, a possible match regarding **Work order type** is checked. If no match is found, **Object** is checked, and so on. As you can see in the layout of the form, this means that Enterprise Asset Management checks each record from right to left for a match (**Work order type**, then **Object**, then **Model**, **Product**, and **Object type**) to find the most specific combination. If no match is found, the "default" record with no selections in those five fields is used.

4. In the **Priority** field, insert a number indicating priority.





###### NOTE



Refer to the [Priority and Description](08_Work_Orders.md#priority-and-description) section for information on how to create priorities.



![Figure 6-20](/Figures/06-20_ObjectPriorities_Form_AX7-01.png)



The last object priority record shown in the figure above is a "Standard priority" with no limitations selected on the record. When the system selects the priority value to be used on a request or work order, the following sort order is used: Work order type, Object, Model, Product, and Object type. All values set up in those fields are sorted in a descending order to ensure that the most specific combination is always selected.



###### NOTE



If you change an object priority in this setup form after you have used it on a work order, the priority on requests and work orders are not updated accordingly.





---





### Object Criticalities



Object criticality is related to objects and transferred to work orders. Object criticality cannot be changed on a work order. Object criticality is used to calculate work order criticality during work order scheduling, meaning to what extent does a maintenance job or a service job on an object affect the production schedule and productivity in your company. Refer to the [Enterprise Asset Management Parameters](#enterprise-asset-management-parameters) section for more information on the setup related to calculating rating scores for work order scheduling. The sequence of working with criticality setup is that first, you create the criticalities to be used in the object setup. Next, you set up object criticalities.





#### Set Up Criticalities



1. Click **Enterprise asset management** > **Setup** > **Objects** > **Criticalities**.

2. Click **New** to create a new record.



3. In the **Criticality** field, insert a number indicating criticality.

4. In the **Name** field, insert a name for the criticality.



5. In the **Factor** field, insert a factor, which is used during calculation of work order scheduling, to determine which criticality record should be used (always the one with the highest factor). This is relevant if, as shown in the figure below, criticality lines have been created with the same criticality value.





![Figure 6-21](/Figures/06-21_Criticalities_Form_AX7-01.png)





#### Set Up Object Criticalities



1. Click **Enterprise asset management** > **Setup** > **Object criticalities**.

2. Click **New** to create a new record.



3. Depending on the detail level for the object criticality, make the relevant selections in the **Object type**, **Product**, **Model**, **Object**, **Job group**, and **Job type**, **Variant** and **Trade** fields.

###### NOTE

When object criticality is selected, Enterprise Asset Management goes through all object criticality records to check for a possible match, always checking the most specific combination first. This means that, first, a possible match regarding **Trade** is checked. If no match is found, **Variant** is checked, if no match is found, **Job type** is checked, and so on. As you can see in the layout of the form, this means that Enterprise Asset Management checks each record from right to left for a match (**Trade**, then **Variant**, then **Job type**, **Job group**, **Object**, **Model**, **Product**, and **Object type**) to find the most specific combination. If no match is found, the "default" record with no selections in those eight fields is used.

4. In the **Criticality** field, select one of the criticality values you created in **Criticalities**.





![Figure 6-22](/Figures/06-22_ObjectCriticalities_Form_AX7-01A.png)





**Example 1:** The default criticality in case no other match is found (the first record in the **Object criticalities** screenshot above).



**Example 2:** A high criticality for scheduling jobs for object types "Kettle" and "Plate heat exchanger" (set up in the fourth and fifth record in the **Object criticalities** screenshot above).





###### NOTE



If you change an object criticality in this setup after you have used it on a work order, the criticality on the work order is not updated accordingly.



Criticality on a work order is re-calculated each time a work order line is added or deleted on the work order.



If a work order contains several work order lines, the highest criticality according to the **Factor** field in **Criticalities** is always used on the work order.



Generally, object criticality may change over a period and be influenced by the purchase of new equipment, refurbishments, and so on. Consider re-evaluating your object criticalities at regular intervals, for example, once a year or every other year, to ensure that your criticality definitions match your current production setup.





---





### Object Documents



In Enterprise Asset Management, you can set up documents to automatically relate to, for example, job types, products, object types, or objects. This is useful when updated document versions are released. In that case, you only need to place the updated document on the standard location you use for your Dynamics 365 for Finance and Operations documents, attach the document to the object document record you have created, and the updated document can be accessed from the **All objects**, **Active objects**, **My active objects**, **All work orders**, and **Active work order lines** menu items. The process regarding attaching documents to an object document record uses the standard document handling system in Dynamics 365 for Finance and Operations.



**Example 1:** A document may relate to a job type (set up in the first record in the **Object documents** screenshot below). The related document could be a procedure description for the selected job type.



**Example 2:** A document may relate to an object type - product - model combination (set up in the second record in the **Object documents** screenshot below). The related document could be the standard manual for the selected product model.





#### Create Object Document Relation



1. Click **Enterprise asset management** > **Setup** > **Object documents**.

2. Click **New** to create a new object document record.



3. Depending on how specific you want the document relation to be, make the relevant selections in one or more fields: **Object type**, **Product**, **Model**, **Object**, **Job group**, **Job type**, **Variant** and **Trade**. The selections available in the **Variant** and **Trade** fields depend on the selected job type.

###### NOTE

When the system searches for documents to be related to an object or a work order, Enterprise Asset Management goes through all object document records to check for a possible match, always checking the most specific combination first. This means that, first, a possible match regarding **Trade** is checked. If no match is found, **Variant** is checked. If no match is found, **Job type** is checked, and so on. As you can see in the layout of the form, this means that Enterprise Asset Management checks each record in the **Object documents** form from right to left for a match (**Trade**, then **Variant**, then **Job type**, **Job group**, **Object**, **Model**, **Product**, and **Object type**) to find the most specific combination. Several documents may be related to an object or a work order. You can edit the priority on a request or a work order, if required.

4. Click **Attachments**. The standard **Document handling** form in Dynamics 365 for Finance and Operations opens.



5. Set up the documents or notes that should be attached to the object document record. When you have attached documents, the number of documents related to the record is shown in the **Attachments** field.





![Figure 6-23](/Figures/06-23_ObjectDocuments_Form_AX7-01.png)





---





### Workers and Worker Groups



In Enterprise Asset Management, you can connect workers to functional locations, which are described in the [Create Functional Locations](05_Functional_Locations.md#create-functional-locations) section. This may be useful if, for example, you are scheduling a maintenance job on a machine located in functional location 01, and you want to allocate workers from the same location to carry out the job.



Also, you can create worker groups and associate workers with worker groups. This functionality is useful when you make simple work order scheduling, and you want to schedule a group of workers on a work order. You can use workers and worker groups to set up preferred workers (refer to  the [Set Up Preferred Workers](13_WO_Scheduling.md#set-up-preferred-workers) section) and responsible workers (refer to the [Responsible Workers](07_Requests.md#responsible-workers) section).





#### Create Workers



1. Click **Enterprise asset management** > **Setup** > **Workers** > **Workers**.

2. Click **New** to add a worker to the list.



3. Select the worker in the **Worker** field.

4. The **Active** check box must be selected in order to schedule work orders for the worker.



5. On the **General** FastTab, **Resource** and **Description** are automatically filled out if a resource has been selected for the worker. **Calendar** is automatically filled out, provided that you have made the following setup in **Organization administration** > **Resources** > **Resources**: Set up the worker as a resource and allocate a calendar to that resource.

6. On the **Groups** FastTab, click **Add** and select a worker group for the worker. A worker can be affiliated with more than one group. The standard setup is that worker group affiliation is effective from the date you add the group, and it never expires. Select **View** > **All** to see the **Effective** field. If required, you can set up a limited period for the group affiliation in the **Effective** and **Expiration** fields.



7. On the **Functional locations** FastTab, click **Add** and select a functional location for the worker. Also, select which location is the primary functional location for the worker.



###### NOTE



When you add functional locations to a worker, all active objects related to those functional locations are shown in various menu items, for example, **My active objects** and **My active functional locations**, as well as in various object lookups, which are shown when you create a new object, request, or work order.





![Figure 6-24](/Figures/06-24_Workers_Form_AX7-01.png)





###### NOTE



The fields in the **Details** group shown at the top of the form show the number of worker groups and functional locations to which the selected worker is related.





#### Create Worker Groups



1. Click **Enterprise asset management** > **Setup** > **Workers** > **Worker groups**.

2. Click **New** to add a worker group to the list.



3. Insert a group ID in the **Worker group** field and a name in the **Name** field.

4. On the **Workers** FastTab, click **Add** and select a worker for the worker group. Refer to description in step 6 in the procedure above regarding the **Effective** and **Expiration** fields.



5. Click the **Copy from resource group** button if you want to select a resource group to be related to the selected worker group. This is only relevant if you want service and maintenance workers to use the calendar related to a resource (work center) during work order scheduling. You select the resource group in the **Group** field, and the worker group to which you want to copy resource group calendar settings in the **Worker group** field.



![Figure 6-25](/Figures/06-25_WorkerGroups_Form_AX7-01.png)





###### NOTE



The field in the **Details** group shown at the top of the form shows the number of workers set up on the selected worker group.





---





### Customer Information



When you carry out service jobs for customers, you must set up customer information in Enterprise Asset Management to be able to set up customers on objects. This is done in **Customers**.



1. Click **Enterprise asset management** > **Common** > **Customers**.

2. Click **New** to create a new customer record.



3. In the **Customers** details view, select a customer account and a project contract.

4. Select the **One invoice** check box if the customer should receive only one invoice that may cover multiple work orders. If **One invoice** is set to "No", a project contract is created for each work order for that customer. The project contract ID is used as a template for the project contract created for the work orders.





In the **Customers** list, you will see a list of all the customers you have created. To the right, you will see an overview of active requests and active work orders related to the selected customer.



![Figure 6-26](/Figures/06-26_Customers_List_AX7-01.png)



When you have created the relevant customers, you select a customer account for an object when you create the object.





---





### Introduction to Objects



An object is any type of equipment, for example a machine or machine part, which requires maintenance, service, or repair.



An object is automatically updated with related information regarding, for example, new or updated work orders. Objects can be created from the **All Objects** or **Pending objects** menu items, which is described in the [Create Objects Based on Purchace or Sales Orders](#create-objects-based-on-purchase-or-sales-orders) section.



Click **Enterprise asset management** > **Common** > **Objects** > **All Objects** to open the list. The **All Objects** list contains a list of all objects and displays some of the information related to an object. You can also select **Active objects** to see a list of all active objects, or **My active objects** to see a list of objects installed on the functional locations you are related to as a worker (set up in [Workers and Worker Groups](#workers-and-worker-groups)).





![Figure 6-27](/Figures/06-27_Objects_List_ASM_AX7-01.png)





In the **All objects** list (Grid view), click on a link in the **Object** column to show the Details view of the selected record. Click the **Edit** button to open for editing. In the Details view, you will see detailed information related to the object as well as Fact Boxes to the right of the screen, displaying other object-related information. Click on the blue 'left arrow' / 'right arrow' button in the small blue box placed above the Fact Boxes to show or hide the Fact Boxes.





![Figure 6-28](/Figures/06-28_Object_Form_AX7-01.png)





The action pane buttons are organized in tabs on the action pane. Here is a brief description of the buttons relating to Enterprise Asset Management:

| Button name | Description |
|--------|--------|
|Edit                  |Edit the selected object.       |
|New                   |Create new object.        |
|Delete                |Delete the selected object.        |
|Move object           |Move objects in the same object hierarchy or to another object hierarchy.        |
|Replace object        |Replace child object in an object hierarchy with another object.        |
|Install object        |Install object on a functional location. |
|Copy object           |Copy object hierarchy to another object.    |
|Notes                 |Insert a note on the object selected in the list page. Start by clicking the **Add timestamp** button to add your user name and a timestamp to the note.       |
|Requests              |Open the **Active requests** list page and view requests created for the selected object.       |
|Timeline              |Overview of the various registrations made on the object.      |
|Object BOM            |View a list of all items (spare parts as well as other items) used on an object.       |
|Contracts             |Open the **Contracts** list page and view contracts created on the object.        |
|Work orders           |Open **Active work orders** list page and view work orders for the object.       |
|Checklist             |Overview of checklists and measurements registered on the object.       |
|Production stop       |Create or view production stop registrations on the object.       |
|Project transactions  |View all posted transactions related to work orders created for the object.      |
|Counters              |Create or view counter registrations on the object.   |
|Object calendar       |Open the **Open object calendar lines** list page and view maintenance sequences, requests, and rounds with status "Created" that are associated with the object.     |
|Object stage          |Update object stage. You can multi-select several objects in the **All objects** list page and update the object stage on several objects at a time.       |
|Stage log             |Log displaying the stages of the selected object.      |
|Object documents      |View list of documents attached to an object. These documents are set up in **Enterprise asset management** > **Setup** > **Object documents**.       |
|Specifications        |Create or view object specifications.      |
|Image                 |Select an image for the object.       |
|Parent objects        |View parent object history on the selected object.       |
|Functional locations  |View functional location history on the selected object.       |
|Condition assessment       |Register condition assessment measurements on the object.       |
|Faults                |Open **Object faults** list and view faults registered on the object.      |
|Cost control          |Compare budget costs and actual costs on the object.        |
|Object KPIs           |Calculate and view Key Performance Indicators (KPIs) for the object.      |
|Job types             |Overview of the current job type setup for the object.       |
|Criticalities         |View or update object criticalities.       |
|Spare parts           |View a list of approved and alternative spare parts that can be used on the object.      |
|Object consumption    |Print a report displaying consumption registrations on the object.       |
|Object fault          |Print a report displaying fault registrations on the object.       |

---





### Create an Object



1. Click **Enterprise asset management** > **Common** > **Objects** > **All objects or Active objects**.

2. Click the **New** button.



3. In the **Create object** drop dialog, insert data regarding **Object** (the object ID) and the object name. Select date and time for the object in the **Effective** field. From that date, you are able to install the object on a functional location as well as move and replace the object in an object hierarchy.

4. In the **Object type** field, select the object type for the object (mandatory fields). If required, select a **Product** and a **Model** for the object. If only one product has been set up, that product is automatically selected in the **Product** field. The selections available in the **Product** and **Model** fields depend on the setup in Product - model.



5. The **Parent object** field is blank as default. If required, you can select a parent object, and then all fields in the **Parent object** section will automatically be filled out.

###### NOTE

When you select a parent object, two or three tabs are available: The **My objects** tab contains objects related to the functional locations to which you (the worker who is logged on the system) may be allocated. If no functional locations are set up on a worker in the Workers form, the **My objects** tab will not be visible. The **Active objects** tab contains a list of all objects with object stage "Active". The **Object view** tab displays a tree view of functional locations and objects installed on those locations.

6. The default functional location you have set up is suggested for the object in the **Object** section > **Functional location** field. Select another functional location, if required.

###### NOTE

After you have created an object, you can install it on another functional location, if required. Only top-level objects (objects without a current parent object) can be installed on a functional location. This means that you install the top level as well as any child objects on the selected functional location. Read more about installing objects on functional locations in the [Functional Locations](05_Functional_Locations.md#functional-locations) chapter.



7. Click **OK**.

8. Select the object in the **All Objects** list and click the **Edit** button to add further information to the object.





---





#### General Information



The functional location to which the object is related is shown in the **Functional location** field. If the object is a parent object, the number of children related to the object is shown in the **Children** field. If the object is a sub object to an existing object, the ID of the parent object is shown in the **Parent** field.



You can edit **Product** and **Model** information on the object, which is used to manage spare parts, alternative spare parts, and job type setup. Refer to the [Product and Model](#product-and-model) and [Forecasts](08_Work_Orders.md#forecasts) sections for more information. You can also add information about **Model year** and **Serial number**, if required.



**Current stage** is used to define if the object is active or inactive. When creating an object, the stage is always set to the first stage in the object stage group. When you are ready to activate an object, click **Object stage**, and select the stage that you have defined as "object active" stage, and click **OK**.





###### NOTE



When an object is set to "inactive", it is no longer possible to create work orders for the object. Also, you cannot schedule preventive maintenance jobs for an inactive object.



The **Priority** and **Criticality** fields relate to work orders created for the object. The fields show the **Priority** and **Criticality** numbers calculated for the current setup for the object. Refer to the [Object Priorities](#object-priorities) and [Object Criticalities](#object-criticalities) sections regarding setup of those values.



#### Asset



You can select a **Resource** for the object. The resource selection determines which calendar is used for work order scheduling. Resource selection is often used for fixed assets. In Dynamics 365 for Finance and Operations, resources and resource groups are set up in **Organization administration** > **Resources** > **Resource groups or Resources**.



In the **Fixed assets number** field, you can select a fixed asset to be related to the object. This is relevant if your object is related to an investment project.





###### NOTE



If the object is related to a fixed asset, you can create a work order type to be used for work orders related to an investment project. Read more about work order types in the [Work Order Types](08_Work_Orders.md#work-order-types).



Information about fixed assets for an object is related to the **Fixed assets** module in Dynamics 365 for Finance and Operations. This means that in **Fixed assets** > **Fixed assets**, you can get an overview of the Enterprise Asset Management projects that may be related to a fixed asset by selecting the asset in the list and viewing the contents in the **Associated projects** FactBox.



On this FastTab, you can also select **Item number** and **BOM** related to the object.





#### Details



In the **Active from** field, the date on which you updated the object stage to an active stage (refer to the [Object Stages](#object-stages) section regarding setup of object stages), is shown. If the object is no longer active, and you have updated the object stage to an inactive stage, the date from which the object is inactive is shown in the **Active to** field. If required, you can manually change those dates.



If required, you can insert an expected date for replacement of the object in the **Replacement date** field. An estimated value for replacing the object can be inserted in the **Replacement value** field. Example: You can use replacement information to compare it with the costs of maintaining an object, and subsequently make a decision for purchasing a new object if maintenance costs on the existing object increase rapidly.





#### Notes



You can add notes related to the object on the **Notes** FastTab. Click the **Add timestamp** button before you write the note, if you want to add user information and a date/timestamp to the note.





#### Specifications



Object specifications set up on the object.





#### Vendor



On the **Vendor** FastTab, select a vendor account for the object. Also, if a vendor warranty has been granted, you can insert warranty information here.





#### Customer



On the **Customer** FastTab, select a customer account if the object is connected to a customer. Also, if a warranty agreement is connected to the object, you can insert customer warranty information here. Read more about warranty in the [Warranty](18_Warranty.md#warranty) chapter.





#### Address



On the **Address** FastTab, you can insert the address of the equipment. If no address is inserted on the object, the object uses the address of a parent object, if the parent object has an address. If no address is related to the object or any parents in the object hierarchy, the address of the functional location on which the object is installed may be used. If that functional location does not have an address related to it, the address of the parent functional location is used on the object.





#### Preventive Maintenance



Maintenance sequences are used for scheduling preventive maintenance jobs at regular intervals on the object. On this FastTab, you can set up maintenance sequence lines for the selected object. Read more in the [Maintenance Sequences](11_Preventive_Reactive_Maint.md#maintenance-sequences) section. Rounds can be set up for various objects, on which you need to carry out a similar task at regular intervals. Read more in the [Rounds](11_Preventive_Reactive_Maint.md#rounds) section. On the **Functional location** tab, you will see the maintenance sequences related to the functional location on which the object is installed.





###### NOTE



If you delete a maintenance sequence line or a round related to an object in **All Objects**, you also automatically delete all object calendar lines with status "Created" that have been created based on that maintenance sequence or round.





#### Project



As explained in the [Integration to Project Management and Accounting](10_Integration_Proj_Management.md#integration-to-project-management-and-accounting) chapter, an object may be related to a project in the **Project management and accounting** module, and the project will be created according to the setup in [Enterprise Asset Management Parameters](#enterprise-asset-management-parameters).





###### CAUTION



On the **Project** FastTab, the **Create project integration** button must only be used in connection with setup of master data. This is not an everyday function, but is only used when a company wants to import existing objects into the Enterprise asset management module, typically in connection with the general setup of Enterprise Asset Management in Dynamics 365 for Finance and Operations.





#### Financial Dimensions



You can select financial dimensions for the object.





![Figure 6-29](/Figures/06-29_Object_Form_AX7-01.png)





---





### Multi-level Objects



You can create objects and related sub-objects in a hierarchical tree structure to display relations and dependencies of objects. MaintenanceService jobs can be related to all levels of the tree structure. Also, statistics can be created for the individual level, or as a sum of all sub-object levels.



In the **All Objects** list (**Enterprise asset management** > **Common** > **Objects** > **All Objects**), you will see objects listed in hierarchical order in the **Object** column. The related parent is displayed in the **Parent** column. Also, you will see a tree structure displaying the object hierarchy in the **Object tree** FactBox if objects and sub objects have already been created.



![Figure 6-30](/Figures/06-30_AllObjects_List_MultiLevel_AX7-01A.png)



Refer to the [Create an Object](#create-an-object) section regarding how to create a new object. To create a sub-object, select the parent object in the **Parent** field on the **General** FastTab.





#### Copy an Object or Object Hierarchy



If your company has several object hierarchies with similar object structures, you can use the copy function in Enterprise Asset Management to quickly create a number of similar object hierarchies.



1. Click **Enterprise asset management** > **Common** > **Objects** > **All objects**. In the All objects list, select the object you want to copy. For example, you select a parent object if you want to copy the entire object structure including sub objects.

2. Click the **Copy object** button. The object you selected in the list page is shown in the **Copy from** > **Object** field.



3. Insert the name of the new object in the **Copy to** > **Object** field.

4. In the **Parent object** > **Object** field, you should only select a parent ID if the object you are creating should be part of an existing object hierarchy.



5. Click **OK**. The new object hierarchy is shown in the **All objects** list. All object specifications, maintenance sequences, and rounds related to the source object from which you made the copy, are transferred to the new object or object hierarchy.



When you copy an object hierarchy, the sub objects in the new hierarchy get the same name as the ones you copied. After the copy procedure is done, you can easily change the name and other settings on a new object by selecting the object in **All objects** and clicking the **Edit** button.





###### NOTE



When you copy an object or object hierarchy, object stages for the new objects are reset to the "first stage" that you have created for objects, and the functional location is reset to the default functional location.





#### Delete an Object or Object Hierarchy



An object with related sub objects can only be deleted if no requests, work order lines, fault registrations, or condition assessments are registered on any of the objects you are trying to delete.



1. In **All objects**, select the object you want to delete.

2. Click **Delete**.





###### NOTE

If you cannot delete an object, instead you can handle deletion by setting up an object stage for this purpose. For example, you can set up a "Scrapped" or "Deleted" stage in **Object stages**.





---





### Move, Replace, and Install Objects



Objects can be created as single objects that have no relations to other objects, or you can create an object hierarchy with a parent object and related child/sub objects. In Enterprise Asset Managemen, there are three approaches to moving or changing location of an object:





- **Move** object = move an object to another object hierarchy, or to another location within the same object hierarchy.







- **Replace** object = replace an object temporarily from an object hierarchy for repair or refurbishment and then re-insert the refurbished object in the object hierarchy later, or replace a used object permanently with a new object.







- **Install** object = install a parent object and any related sub objects on a functional location.





###### NOTE

When you move or replace or install an object, the object may be related to another functional location. In that case, the object may use financial dimensions of the functional location. The handling of financial dimensions on functional locations is set up in **Functional location types**.





---





#### Move Object



Use this function to move an object to another object hierarchy, or move an object to another location in the same object hierarchy, or move an object from an object hierarchy to be a standalone object with no hierarchy relations.



###### NOTE

Do not use this function in relation to repair or temporary replacement of objects. In that case, use the **Replace object** functionality described below.



1. Click **Enterprise asset management** > **Common** > **Objects** > **All objects** or **Active objects**.

2. Select the object you want to move. If the object has sub objects, you also move the sub objects.



3. Click **Move object**.

4. If you want to move the object to be part of an object hierarchy, select the new parent object in the **Parent object** field. If you are moving a sub object, and you want to make it a standalone object with no hierarchy relations, do not make a selection in the **Parent object** field.



5. In the **Effective** field, current date and time are shown. If required, select another date and time from which the object move should be valid.

6. Click **OK**.





![Figure 6-31](/Figures/06-31_Move_Object_AX7-01.png)





---





#### Replace Object



Use this function in connection with repair, refurbishment, or permanent replacement in case a worn-out object is replaced by a new object. This function is used for replacing child objects in an object hierarchy. If you want to replace parent objects, meaning top-level objects (objects without a current parent object), this is done on a functional location. Refer to the [Install Objects on Functional Locations](05_Functional_Locations.md#install-objects-on-functional-locations) section for more information on how to replace parent objects on a functional location.



###### NOTE

If you have a repair shop related to your production department, you may create functional locations for "Repair", "Scrap", or "Storage" to handle repair and replacement of objects.



1. Click **Enterprise asset management** > **Common** > **Objects** > **All objects** or **Active objects**.

2. Select the child object you want to replace in the list. If that object has child objects, you also replace those objects.



3. Click **Replace object**. In the **Structure change** field, you see the latest date and time when the selected object and related child objects were moved in the object hierarchy.

4. In the **Selected object** section > **Functional location** field, select the functional location to which you want to move the object, for example, a "Repair" or "Scrap" location.



5. In the **Parent object** section > **Effective** field, you see the latest date and time when the parent object and related child objects were installed or moved on the current functional location.

6. In the **New object** section > **Object** field, select the object to be inserted as a temporary or permanent replacement for the selected object. This object may currently be located on another functional location, for example, "Storage".



7. In the **Effective from** section > **Effective** field, current date and time are shown. If required, select another date and time from which the object replacement should be valid.

8. Click **OK**.





![Figure 6-32](/Figures/06-32_Replace_Object_AX7-01.png)





---





#### Install Object



Use this function to install an object hierarchy on a functional location.





###### NOTE



Remember to always select a parent object. The parent object and related child objects will be moved to the selected functional location.



1. Click **Enterprise asset management** > **Common** > **Objects** > **All objects** or **Active objects**.

2. In the list, select the parent object you want to install on another functional location.



3. Click **Install object**. The object specifications set up on the parent object are shown in the **Specifications** section.

4. Select the new location in the **Functional location** field.



5. In the **Effective** field, current date and time are shown. If required, select another date and time from which the object hierarchy installation should be valid.

6. Click **OK**.





![Figure 6-33](/Figures/06-33_InstallObject_On_FunctionalLocation_AX7.png)





---





### Create Objects Based on Purchase or Sales Orders



In **Enterprise Asset Management**, you can create a list of object items that can be used as a basis for creating objects for maintenance or service jobs. Based on the object items, you are able to view a list of the purchase order lines (relating to internal maintenance), or sales order lines (relating to service management and contract management) that have been created on those items. The purpose of this functionality is to easily create an object in **Enterprise Asset Management** based on a purchase order or a sales order.



First, you set up the items to be used for creating objects from a purchase or sales order in **Object items**. After creating a purchase order line or sales order line, you create the objects in **Pending objects**. It is possible to decide at which stage of the purchase order or sales order the object should be created.





#### Select Object Items



1. Click **Enterprise asset management** > **Setup** > **Objects** > **Items**.

2. Click **New** to create a new object item.



3. Select the item in the **Item number** field. When you leave that field, the item name is automatically inserted in the **Product name** field.

4. On the **General** FastTab, select an object type for the item.



5. Select product and model for the item.

6. Save the item.





![Figure 6-34](/Figures/06-34_ObjectItems_Form_AX7-02.png)





#### Create Objects from Pending Objects



1. Click **Enterprise asset management** > **Common** > **Objects** > **Pending objects**.

2. You will see an updated list of the purchase orders and sales orders based on the items selected in **Object items**.



3. You can filter the status of purchase and sales orders to select at which stage the object should be created. For example, you may only want to create objects when a product receipt has been posted on a purchase order.

4. Select a purchase order or sales order line, and click the **General** FastTab or the **Inventory dimensions** FastTab to view detailed information about the item.



5. If you want to edit which dimensions are displayed on the **Inventory dimensions** FastTab, click the **Display Dimensions** button, and make your selections.

6. If you want to create an object based on a purchase order line or sales order line, select the check box in the **Mark** column for that line, and click **Create objects**. A message will be displayed informing you of the object ID.



7. Select the object in the **All objects** list and click **Edit** to add more information to the object.

8. In **Pending objects**, if you want to delete a line because you don't want to create an object, select the check box in the **Mark** column for that line and click **Discard pending objects**. You are not deleting the purchase order or sales order, just the record from which you could have created an object in Enterprise Asset Management.





###### NOTE

If a sales order is related to a production, the consumed items (spare parts) will automatically be added to the object BOM. If a consumed item is also an object item, a sub object will also be created for the item. Read more about the object BOM in the [Object BOM](#object-bom) section.



All product dimensions (size, color, configuration etc.) are automatically transferred to the object specifications. Tracking dimensions (serial number) are stored directly on the object when the object is created.





![Figure 6-35](/Figures/06-35_PendingObjects_Form_AX7-01.png)





#### Find Pending Objects



You can run a **Pending object count** to check for pending objects. For example, this function can be used for receiving a notification each time a pending object is ready to be created as an object.



1. Click **Enterprise asset management** > **Periodic** > **Objects** > **Pending object count**.

2. Click **OK** to run the job and update the list in **Pending objects**.



3. You can set up this job to run as a batch job, for example, once each day.





###### CAUTION

If data is changed on a purchase order or sales order *after* you have created an object based on the appertaining item, those changes will not be reflected on the object.





###### NOTE

If an object contains consumed items (sub components) with serial numbers, you may experience problems when creating objects based on sales orders. The reason is that consumed items with serial numbers do not have a direct relation to the finished goods, meaning you cannot locate which sub component serial numbers are related to which objects. This is only a problem in case the produced quantity is more than one.





---





### Object BOM



The purpose of **Object BOM** is to show a list of all items (spare parts as well as other items) used on an object during the entire lifetime of the object. When you create a new object, consider setting up the Object BOM as a part of your object setup procedure. This allows you to track item history on the object from the creation date.



After you have completed a maintenance or service job, and item consumption has been registered on a work order, you are able to track consumption of spare parts and other items used on the object. This functionality allows you to keep a complete item consumption record on all your objects. For example, you can use the record to monitor if a specific spare part is often replaced, or keep track of which spare parts or other items are currently used on an object.





###### NOTE



On a work order, item consumption may include spare parts as well as other, additional items, for example, lubricants, bolts, and gaskets.



The object BOM can be updated automatically, based on the setup in Enterprise Asset Management. If a work order stage has been created to handle finished or completed work orders, and that work order stage has a check mark in the **Update object BOM** check box in **Work order stages**, all items used on the work order will automatically be updated in Object BOM when the work order is updated to that stage. Read more about work order stage setup in the [Work Order Stages](08_Work_Orders.md#work-order-stages) section. It is also possible to manually update the object BOM by creating new item lines in **Object BOM**.



In order to track spare parts history in **Object BOM**, you must select which item groups should be used for spare parts registration. This is done in **Spare parts item groups**. When item consumption has been registered on a work order, you will be able to track spare parts history on objects in **Object BOM**. First step regarding use of Object BOM functionality is to set up the required spare parts items groups. Then, if you want to automatically update the Object BOM when completing a work order, you can set up a work order stage to handle that update (described in the [Work Order Stages](08_Work_Orders.md#work-order-stages) section).





#### Set Up Spare Parts Item Groups



Spare parts history setup is based on item groups that are created in the **Intenvory and warehouse management** module. You set up item groups in **Enterprise Asset Management** to be able to track spare parts history on the items in the selected item groups.



1. Click **Enterprise asset management** > **Setup** > **Object** > **Spare parts item groups**.

2. Click **New** to set up an item group.



3. Select the group in the **Item group** field. The name of the group is automatically inserted in the **Name** field.





![Figure 6-36](/Figures/06-36_SparePartsItemGroups_Form_AX7-01.png)





#### View and Update Object BOM



When you have posted item consumption on a work order, you are able to see the registered item consumption in Object BOM.



1. Click **Enterprise asset management** > **Common** > **Objects** > **Active objects** > select the object in the list > **Object BOM** button.

###### NOTE

Click **Enterprise asset management** > **Inquiries** > **Objects** > **Object BOM** if you want to see all item consumption registrations on all objects.

2. Click **Update object BOM**. If required, you can add objects, object types, and resources to the update by clicking the **Select** button. Click **OK** to start the update. It is also possible to set up the update function as a batch job.



3. You can add inventory dimensions if you want to see more information related to the items. Click **Inventory** > **Dimensions display** and select the dimension check boxes you want to see. Select the Save setup check box if you want to keep this setup for all objects in **Object BOM**.

4. Click **Item where used** if you want to get an overview of where the item on the selected line is used in Enterprise Asset Management in relation to objects, job type setup, spare parts, and work orders. Read more about this overview in the [Items Where Used](20_ControllingAndReporting.md#items-where-used) section.



5. Click **View** > **Current** if you want to see only active item lines. Click **View** > **All** if you want to see all item lines, including the lines that have an expiration date earlier than the current date.





![Figure 6-37](/Figures/06-37_ObjectBOM_Form_AX7-01.png)





###### NOTE

When you have completed a work order, and some items or spare parts related to the related object have expired or have been replaced by other items or spare parts, we recommend that you update the object BOM accordingly.





#### Create a New Item Line in Object BOM



It is possible to manually create item lines for objects.



1. In **Object BOM**, click **New**.

2. Select the object for which you want to add an item line in the **Object** field.



3. Insert a sequential line number in the **Line number** field.

4. Insert a start date in the **Effective** field.



5. If relevant, insert and end date for the item in the **Expiration** field.

6. Select the item in the **Item number** field. The name is automatically inserted in the **Product name** field.



7. Insert the quantity used in the **Quantity** field. The **Unit** field is automatically updated.



---





### Object Timeline



In **Object timeline**, you can see the registration history that has been made in the lifetime of an object. You can access the form from the **All objects**, **Active objects**, and **My active objects** menu items. Select an object and click the **Timeline** button.



You can make a search on all information available on the **Details** FastTab in **Object timeline**. For example, you can use the object time line to find information regarding:



- when a job type was last used on an object



- when a remark was inserted on a work order line by a specific worker





The timeline is updated every time the form is opened. It contains the following information:



- Changes made on the object: Object location, Object ID, Name, Vendor warranty , Customer, Customer warranty



- Object parent



- Object BOM



- Object stage log



- Functional location



- Requests



- Work orders, including posted item and notes



- Faults



- Condition assessments





![Figure 6-38](/Figures/06-38_ObjectTimeline_Form_AX7-01.png)





---





### Object View



In **Object view**, you can see an overview of active objects and functional locations in a tree view. You can easily get an overview of object relations to functional locations as well as see detailed information regarding functional location, object, and related BOM, as well as a quick overview of active requests and work orders related to an object.



1. Click **Enterprise asset management** > **Common** > **Objects** > **Object view**.

2. The default view that is shown when you open the form depends on the selection in **Enterprise asset management** > **Setup** > **Enterprise asset management parameters** > **Objects** link > **View** field. You can select another view by clicking **View** and making a selection.

![Figure 6-39](/Figures/06-39_ObjectView_Form_ViewDropDown_AX7-02A.png)



3. In the screenshot below, **View** > **Objects** is selected. In the right side of the form, details of the selection are shown on the related FastTabs.

4. The breadcrumb shown above the tree view shows the current selection in the tree view in the following format: **Functional location ID** / **Functional location ID** (if more than one functional location) > **Object ID** / **Object ID** (if more than one object) - **Item number**.





![Figure 6-40](/Figures/06-40_ObjectView_Form_AX7-01A.png)





###### NOTE

If you have selected an object in the tree view, select the **Active requests** button or **Active work orders** button to see the requests or work orders related to the object. You can also click **Open** > **Functional location** or **Object** or **Object BOM** to open the related view.



The **Object functional locations** option that you can select in **View** is also available in any object lookup in which you can select an object. The tree view is shown on an **Object view** tab, for example where you [create an object](#create-an-object), [a request](07_Requests.md#create-a-request), or [a work order](08_Work_Orders.md#manually-created-work-orders).





---





### Object Specification Overview



Object specifications are properties related to an object type or object. If you have set up [specification types](06_Objects.md#object-specifications) and used them on objects, you can get an overview of specification values set up on objects. This is shown in two forms in Enterprise Asset Management.



In **Object specification overview**, one object is shown per line with all related specification types.



1. Click **Enterprise asset management** > **Inquiries** > **Objects** > **Object specification overview**.

2. Select an object type in the **Object type** field.



3. Click **OK**. A list of all objects using the selected object type is shown. For each object, all related object specification types are shown on the same line.





![Figure 6-41](/Figures/06-41_ObjectSpecificationOverview_Form_AX7-01.png)



If you want a to see an overview displaying a separate line for each specification type on an object, click **Enterprise asset management** > **Inquiries** > **Objects** > **Object specification**. Here you see all object specification registrations on all objects.





![Figure 6-42](/Figures/06-42_ObjectSpecifications_FromInquiriesMenu_Form_AX7-01.png)





---





### Objects and IoT Devices



In Enterprise Asset Management, you can set up relations between an IoT device, the related object, and a counter. Measurements from the counter is registered in Enterprise Asset Management by using tools like Microsoft Flow or Microsoft Azure Logic Apps.



When a relation between an IoT device and the object is set up, you are able to see counter registrations from the IoT device on the object. The following procedure describes how to set up the IoT device relation.



1. Click **Enterprise asset management** > **Setup** > **IoT** > **IoT device relation**.

2. Click the **New** button.



3. Insert the name or ID of the IoT device in the **IoT Device** field.

4. Select the related object in the **Object** field.



5. Select the counter type for IoT device in the **Counter** field.

6. Click **Save**.





![Figure 6-43](/Figures/06-43_IoT_Device_Relation_AX7.png)





###### NOTE

In Dynaway, we have created a document describing an example of the IoT setup, which includes setup of Microsoft Azure IoT Hub and Microsoft Flow to manage IoT data in Enterprise Asset Management.



