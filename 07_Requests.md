# Requests

Requests are notes or declarations that can be created to make a manager or planner aware that an object may require a maintenance or repair job - without actually creating a work order. A work order may subsequently be created based on a request if the contents of the request are considered to be valid for a work order to be created.

Requests can be created for any object in Enterprise Asset Management. Various request types can be created, depending on how your company uses requests. Here are some examples:

- Maintenance requests
- Notes

- Corrections / Enhancements
- Investments

- Depot repair - for the purpose of managing repair of objects that you receive from another location to carry out a maintenance or repair job, and then return the object after the job is completed.


---

### Request Stages

Request stages define the stages that a request can go through, for example, "Created", "Active", and "Ended". When a request is converted into a work order, the request stage should be updated to "Ended" or "Closed" to indicate that the request is no longer active. You are able to view all requests, regardless of their stage, in the **All requests** list.

---


#### Set Up Request Stages

1. Click **Enterprise asset management** > **Setup** > **Requests** > **Stage** > **Stages**.
2. Click **New** to create a new request stage.

3. Insert the stage ID in the **Stage** field and a name for the request stage in the **Name** field. In the **Stage groups** field, you can see the number of request stage groups that uses the request stage.
4. On the **General** FastTab, select if the request should be active in this stage.

5. Select the **Set actual end** check box if actual end date and time should automatically be inserted on the request at this stage.
6. Select the **Delete** check box if it should be possible to delete requests at this stage.

7. Select the **Create work order** check box if it should be possible to create a work order from the request at this stage.
8. On the **Update** FastTab, the **Inbound** and **Outbound** check boxes are relevant if you use depot repair (refer to the [Inbound and Outbound Objects](#inbound-and-outbound-objects) section for more information). Select a check box if you want to automatically update the object stage to **Inbound** or **Outbound** at this stage.

9. Select the **Open object calendar lines** check box for a stage on which you want to delete all lines in the object calendar connected to the request, which have not been converted to work orders.


###### NOTE
Whether you are able to work with inbound and outbound objects depends on the setup of Enterprise Asset Management. The functionality can only be used if the **Inbound/outbound** check box is selected in the **License configuration** (**System administration** > **Setup** > **Licensing** > **License configuration**). Read more about configuration in the [License Configuration](03_License_Config.md#license-configuration) chapter.
If the **Inbound** check box or the **Outbound** check box is selected on the **Update** FastTab on a request stage, it means that when the stage is set to "Inbound" or "Outbound" on a request, the object stage for the object selected on the request is updated accordingly.


![Figure 7-01](/Figures/07-01_RequestStages_Form_AX7-01.png)


###### NOTE
Request stages, stage groups, and types are related and used in the same way as work order stages, work order stage groups, and work order types. Refer to the [Work Order Stages](08_Work_Orders.md#work-order-stages) section for a general explanation regarding stage group, type, and stage relations.


---


#### Set Up Request Stage Groups

When you have created the stages required for your requests, they can be divided into groups. This is done to create the stage group flow that may be used for different types of requests. As a minimum, one standard request stage group should be created.

1. Click **Enterprise asset management** > **Setup** > **Requests** > **Stage** > **Stage groups**.
2. Click **New** to create a new stage group.

3. Insert the stage group ID in the **Stage group** field and a name for the stage group in the **Name** field. In the **Stages** and **Request types** fields, you can see the number of stages selected in the stage group, and the number of request types that uses the stage group.
4. On the **Stages** FastTab, select the stages that should be included in the group. This is done by clicking on a stage in the **Stages remaining** section and clicking the ![Figure 7-02](/Figures/07-02_Button_Select_StageGroups.png) button.

5. If you want to select all the available stages for a group, click the ![Figure 7-03](/Figures/07-03_Button_SelectAll_StageGroups.png) button. All stages are transferred to the **Stages selected** section.
6. If you want to remove a selected stage from the group, select the stage in the **Stages selected** section and click the ![Figure 7-04](/Figures/07-04_Button_Deselect_StageGroups.png) button.

7. Click **Stage updates** to define which stages can follow a selected stage.
8. On the **General** FastTab, you can select stages related to depot repair. This means that the request stage is automatically updated to the stage you select when objects selected on the request are received for depot repair in the **Inbound objects** list, or returned after repair, which is registered in the **Outbound objects** list.


![Figure 7-05](/Figures/07-05_RequestStageGroups_Form_AX7-01.png)


---


### Request Types

A request type is used to categorize requests, for example relating to preventive maintenance, corrective maintenance, or a special request type that manages repair of objects, which could be called "depot repair".

A request type defines the request stage group affiliation. Request stage group defines which stages can be set for a request, for example, "Created", "Active", and "Ended".

1.  Click **Enterprise asset management** > **Setup** > **Request** > **Request Types**.
2.  Click **New** to create a new request type.

3.  Insert the request type ID in the **Request type** field and a name for the request type in the **Name** field.
4.  Select a stage group in the **Request stage group** field.

5.  Select a work order type in the **Work order type** field. When a request is converted to a work order, the work order automatically gets the work order type related to the request type.


![Figure 7-06](/Figures/07-06_RequestTypes_Form_AX7-01.png)

---


### Responsible Workers

Responsible workers can be related to customers, object types, objects, functional locations, job groups, job types, variants, and trades to make a worker preference on work orders and requests regarding which workers should be responsible for a work order (but not necessarily the ones scheduled to carry out a work order). The use of this functionality is optional. For example, it can be used to select responsible workers or worker groups for specific work types or work areas. During a work order life cycle or a request life cycle, it is possible to change or update responsible workers, which could be related to, for example, a change in request stage or work order stage. The setup in **Responsible workers** is *not* used during work order scheduling.

Before you can set up responsible workers, you must first set up the workers and worker groups that should be available for selection. Refer to the [Workers and Worker Groups](06_Objects.md#workers-and-worker-groups) section for a description on how to set up workers and worker groups.


#### Set Up Responsible Workers

A responsible worker or worker group can be related to a specific

- Job trade

- Job variant

- Job type

- Job group

- Object

- Object type

- Functional location

- Customer account

or a combination of those selections. The more selections you make for the same record, the more specific your setup becomes.


1.  Click **Enterprise asset management** > **Setup** > **Workers** > **Responsible workers**.
2.  Click **New** to create a new record.

3.  Start by creating a "default" worker or worker group setup that has no selections in the fields shown in the bullet list above. This means that you only make a selection in the **Responsible worker group** field and/or the **Responsible worker** field. In the figure below, you see an example in the first record in which "Requests" is selected as responsible worker group.
   ###### NOTE
   The default setup will be used during work order scheduling in case no other, more specific, combination matches the contents of the work order during work order scheduling.

4.  Repeat step 2 to create a new record. Make the required selections, depending on the detail level for the responsible worker or worker group. **Example:** In the figure below, in the third record, the worker Dana Birkby is selected as responsible worker. She will automatically be selected if you create a request or a work order for the object "C0002".
###### NOTE
During creation of a request, when a responsible worker or responsible worker group is made available for selection in **All requests**, Enterprise Asset Management goes through all responsible worker records to check for a possible match, always checking the most specific combination first. This means that, first, a possible match regarding **Trade** is checked. If no match is found, **Variant** is checked. If no match is found, **Job type** is checked, and so on. As you can see in the layout, this means that Enterprise Asset Management checks each record from right to left for a match (**Trade**, then **Variant**, then **Job type**, **Job group**, **Functional location**, **Object**, **Object type**, and **Customer account**) to find the most specific combination. If no match is found, the "default" record with no selections in those seven fields is used.


![Figure 7-07](/Figures/07-07_ResponsibleWorkers_Form_AX7-01.png)


###### NOTE
In Enterprise Asset Management, you can also set up preferred workers, who may be allocated on work orders during work order scheduling. Refer to the [Set Up Preferred Workers](13_WO_Scheduling.md#set-up-preferred-workers) section for more information.


---

### Introduction to Requests

Requests are used to create a request indicating that a work order may be required for a specific job. A planner or manager can then decide whether the request should be converted to a work order. You can set up different request types to be used in your company, for example, maintenance requests and depot repair requests.

Click **Enterprise asset management** > **Common** > **Requests** > **All requests** or **Active requests** or **My functional location requests**. The list displays some of the information related to a request.


![Figure 7-08](/Figures/07-08_AllRequests_List_AX7-01.png)


###### NOTE
Click **Enterprise asset management** > **Common** > **Requests** > **My functional location requests** to see a list of requests containing functional locations, or objects installed on functional locations, you are related to as a worker (set up in [Workers and Worker Groups](06_Objects.md#workers-and-worker-groups)).
Customer account information is available in Asset Service Management (external maintenance), but not in Enterprise Asset Management (internal maintenance).


In the **All requests** list (grid view), click on a link in the **Request** column to show the Details view of the selected record. Click the **Edit** button to open for editing.


![Figure 7-09](/Figures/07-09_Request_Form_AX7-01.png)


The action pane buttons are organized in tabs on the action pane. Here is a brief description of the buttons relating to Enterprise Asset Management:

| Button name | Description |
|--------|--------|
|Edit                  |Edit the selected request.       |
|New                   |Create new request.        |
|Delete                |Delete the selected request.        |
|Work order pool       |Connect the selected request to a work order pool.        |
|Work order            |Create a work order based on the selected request.        |
|Object fault          |Open **Object faults** and create a fault registration on the request. |
|Work orders           |Show a list of all work orders connected to the request.    |
|Send loan object      |Select a loan object to be a temporary replacement for the object selected on the request.       |
|Return loan object    |Register the loan object as returned.      |
|Request stage         |Update request stage.       |
|Stage log             |Log displaying the stages of the selected request.        |
|Request details       |Print a report displaying details of the selected request.      |


---


### Create a Request

Requests can be used if maintenance workers or production workers discover a need for equipment repair, and it is not possible to carry out that repair job right away.

**Example:** A maintenance worker is making a repair. During this repair he discovers that another object at the same location needs to be serviced, but he has no time or spare parts to carry out the repair job. Therefore he creates a request on the object containing a short description of the problem.

In **All Objects** or **Active objects** (**Enterprise asset management** > **Common** > **Objects** > **All Objects** or **Active objects**), you can see the active requests attached to the selected object in the **Active requests** FactBox placed in the right side of the screen.

1. Click **Enterprise asset management** > **Common** > **Requests** > **All requests** or **Active Requests**.
2. Click the **New** button.

3. In the **Create request** drop-down dialog box, select the type in the **Request type** field. A default type is suggested.
4. Insert a name or title that briefly describes the request in the **Description** field.

5. Select **Customer account**, **Functional location**, **Object**, or a combination, as required. It is possible to create a request without selecting an object. Then the object is added to the request later. If the worker who is logged in to Dynamics 365 for Finance and Operations is related to a resource, which is related to an object, the **Object** field is automatically filled out.
   ###### NOTE
   If the selected object already has requests attached to it, an info message is shown at the top of the **Create request** drop-down dialog, showing the request ID of an existing request as well as an **Open** button that you can click to open that request. If the object is covered by a warranty or contract agreement, an info message is also shown.
   When you select an object, two or three tabs are available: The **My objects** tab contains objects related to the functional locations to which you (the worker who is logged on the system) may be allocated. If no functional locations are set up on a worker in [Workers and Worker Groups](06_Objects.md#workers-and-worker-groups), the **My objects** tab will not be visible. The **Active objects** tab contains a list of all objects with object stage "Active". The **Object view** tab displays a tree view of functional locations and objects installed on those locations.

6. Select a priority regarding the urgency of the request in the **Priority** field.
7. If you have selected an object, you can create a fault registration by selecting fault data in the **Fault symptom**, **Fault area**, and **Fault type** fields.

8. If the request has caused a production stop, insert start date and time of the production stop in the **Production stop** field.
9. Your name is automatically inserted in the **Started by** field.

10. The **Actual start** field is automatically filled out with current date and time, but you can change it, if required.
11. If required, insert further notes in the **Notes** field.

12. Click **OK**.

![Figure 7-10](/Figures/07-10_CreateRequest_DropDown_AX7-01.png)

###### NOTE
In [Maintenance status](20_ControllingAndReporting.md#maintenance-status), you can make a calculation to get an overview of workload regarding incoming and completed requests.

---


#### Subsequent Processing of the Request

After the request has been created, and before it is converted to a work order, various data should be updated on the request. This is typically done by a planner or another administrative employee. In **All requests** or **Active Requests**, select the request you want to work with, and click **Edit**.

In the Details view, you can update various information. For example you can

- select and verify the object. If, required it is possible to clear the **Object verified** check box later to select another object.

- select responsible group and/or responsible worker. For more information on how to set up responsible workers and worker groups, refer to the [Responsible Workers](#responsible-workers) section.

- select a job type and, if relevant, the related job variant and job trade.

- insert geographic coordinates in the **Latitude** and **Longitude** fields. If coordinates are added to a request, they are automatically transferred to a related work order. This information is useful if you work with linear asset management.


![Figure 7-11](/Figures/07-11_Request_Form_AX7-01.png)


###### NOTE
If you select an object when you create the request, you can add one fault to the object. After the request has been created, you can add more faults, if required, by clicking the **Object fault** button in **All Requests**.


---


### Create Work Order from Request

When you have created requests, you can easily convert the requests to work orders. The quickest way to work with requests, update several requests at a time, and subsequently create a work order for several requests at a time is described in this procedure. If required, you can also work with one request a time and convert one request to one work order in the **Active requests** or **Active requests with no work order** list.

###### NOTE
One request can only be related to one work order, but several requests can be included in one work order even if the requests have different objects.


1. Click **Enterprise asset management** > **Common** > **Requests** > **All requests**.
2. Before you can create a work order from a request, you must as a minimum select a job type and, if required, a job variant and a job trade for the requests for which you want to create a work order. In grid view, you can easily update data for a request.

3. When you are ready to create a work order, select the requests you want to include in one work order.
   ###### NOTE
   If you multi-select several requests to be converted to one work order, the **Object** and **Job type** fields must be filled out before you start creating the work order. If you select one request to be converted to a work order, the **Object** field must be filled out before you start creating the work order, but **Job type** (and if relevant, related **Variant** and **Trade** fields) can be selected in the **Create work order** drop-down dialog box when you create the work order.

4. Click the **Work order** button.
5. In the **Create work order** drop-down dialog, fill in the fields, and click **OK**.

6. A message may be shown that a new work order has been created.
   ###### NOTE
   If you create a work order based on a request, and the object related to the request is included in a warranty agreement, a message informing you of the warranty agreement will be shown on the screen.
7. Open the new work order in **Enterprise asset management** > **Common** > **Work orders** > **All work orders**.


![Figure 7-12](/Figures/07-12_CreateWOFromRequest_Example_AX7-01.png)


---


### Object Loan

If your company receives objects for repair or maintenance jobs from other locations, internally or from customers, and you loan objects temporarily to the locations or customers that send objects to you to be repaired, Enterprise Asset Management can keep track of your object loans.


#### Register Loan Object on a Request

1. Click **Enterprise asset management** > **Common** > **Requests** > **All requests** or **Active requests**.
2. Select the request on which you want to register a loan, and click **Edit**.

3. In the **Request** Detail view, click **Send loan object**.
4. Select the object and insert an expected return date.

5. Click **OK**.

###### NOTE
It is only possible to send a loan object if an object of the same object type is available.
The loan object must have an object stage that allows it to be used as a loan object, for example, "InStorage". When the loan object has been registered, the object stage of that object is automatically updated, for example, to "OnLoan".


Click **Enterprise asset management** > **Common** > **Object loan** > **All object loans** to see a complete list of all the objects you have loaned to other locations or customers. If the **Ended** check box is selected on an object, it means that the object has been registered as returned to your company.


![Figure 7-13](/Figures/07-13_AllObjectLoans_List_AX7-01.png)

In **Active object loans**, you see a list of all the loan objects that have not yet been returned to your company.

###### NOTE
In **All object loans**, if you select a loan and click **Transfer to customer**, the loan object is transferred to the customer as an active object.


#### Register Loan Object as Returned

1. Click **Enterprise asset management** > **Common** > **Object loan** > **Active object loans**.
2. Select the object loan that you want to register as returned and click **Return object loan**.

3. Insert date and time in the **Returned** field and click **OK**.
4. Update the **Active object loans** list by pressing **F5**. You will notice that the loan is no longer on the active list.


---


### Inbound and Outbound Objects

If your company makes repair jobs or maintenance jobs on objects received from other locations or customers, Enterprise Asset Management can keep track of inbound objects on the way to your company and outbound (returned) objects.

###### NOTE
If you want to use Inbound and Outbound stages to manage objects coming in and being returned, you must set up [request stages and staqe groups](#request-stages) to support these actions.
Whether you are able to work with inbound and outbound objects depends on the setup of Enterprise Asset Management. The functionality can only be used if the **Inbound/outbound** check box is selected in the **License configuration** (**System administration** > **Setup** > **Licensing** > **License configuration**). Read more about configuration setup in the [License Configuration](03_License_Config.md#license-configuration) chapter.


#### Register Object as Inbound

1. Click **Enterprise asset management** > **Common** > **Requests** > **Active requests**.
2. Select the request.

3. Click **Request stage** > **Inbound** (or the stage you have created for inbound objects).


![Figure 7-14](/Figures/07-14_Inbound_AllRequests_List_AX7-01.png)


#### Register Inbound Objects as Received

1. Click **Enterprise asset management** > **Common** > **Inbound/outbound** > **Inbound objects**.
2. Select the object / request.

3. Click **Receive objects**.
4. Insert date and time in the **Received** field, and click **OK**. The record is removed from the **Inbound objects** list.


![Figure 7-15](/Figures/07-15_InboundObjects_List_AX7-01.png)


#### Register Object as Outbound

When you have completed the maintenance or repair job, you can register the object as returned.

1. Click **Enterprise asset management** > **Common** > **Requests** > **Active requests**.

2. Select the request.
3. Click **Request stage** > **Outbound** (or the stage you have created for outbound objects).

---

#### Register Outbound Objects as Delivered

1. Click **Enterprise asset management** > **Common** > **Inbound/outbound** > **Outbound objects**.
2. Select the object / request.

3. Click **Deliver objects**.
4. Insert date and time in the **Delivered** field, and click **OK**. The record is removed from the **Outbound objects** list.


---


### Request Reports

In Enterprise Asset Management, you can generate two reports regarding requests, one displaying details, and one providing a list to be used for planning and follow-up.


#### Create Request Details Report

You can create a detailed report for requests that shows various information related to the request.

1. Click **Enterprise asset management** > **Reports** > **Requests** > **Request details**.
2. On the **Records to include** FastTab, you can select specific requests to be included in the report.

3. If required, you can set up report generation as a batch job by filling out the fields on the **Run in the background** FastTab.
4. Click **OK** to generate the report.

Below you see an example of a request details report.


![Figure 7-16](/Figures/07-16_RequestDetails_Create_Report_AX7-01.png)


![Figure 7-17](/Figures/07-17_RequestDetails_Report_AX7-01.png)

---


#### Create Request List Report

You can create a request list report displaying a list of all requests using the same request type.

1. Click **Enterprise asset management** > **Reports** > **Requests** > **Request list**.
2. On the **Records to include** FastTab, you can make selections to be included in the report.

3. If required, you can set up report generation as a batch job by filling out the fields on the **Run in the background** FastTab.
4. Click **OK** to generate the report.

Below you see an example of a request list report for all active requests.


![Figure 7-18](/Figures/07-18_RequestList_Create_Report_AX7-01.png)


![Figure 7-19](/Figures/07-19_RequestList_Report_AX7-01.png)

