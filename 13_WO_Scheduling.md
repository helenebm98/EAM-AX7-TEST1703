# Work Order Scheduling

When a work order has been created and planned, the next step is to allocate the required resources to complete the maintenance or service job. Resources are used in work order scheduling to make capacity reservations. Three resource types are available:

- Human resources

- Machines

- Tools

Work order scheduling can be carried out on two levels - advanced work order scheduling or exclusive work order scheduling - depending on your requirements for resources for the service job. The "Schedule exclusively" option is useful if, for example, a worker has called in sick, and you need to quickly reschedule jobs from one worker to another. The scheduling process in the Enterprise Asset Management module is done by including different factors in the scheduling calculation:

- Calculating scores for work orders and workers. The scores are set up in the **Enterprise asset management parameters** form.

- Checking for matching competencies, meaning skills and certificates, required to perform the job. Skills and certificates are set up on workers in the **Human resource** module in Dynamics 365 for Finance and Operations.


### Set Up Worker Calendar

When you schedule work orders, you create a schedule for workers, tools, and objects. In order to carry out scheduling on workers, a calendar is related to each worker. Workers are related to a resource, and resources have calendars defined along with the possibility of creating calendar deviations, if required. The resource and calendar related to a worker is shown in **Enterprise asset management** > **Setup** > **Workers** > **Workers**.


![Figure 13-01](/Figures/13-01_Workers_Form_ResourceAllocation_AX7-01A.png)


Calendar setup for tools and objects is not needed in relation to work order scheduling. The assumption is that tools and objects are available 24 hours a day for maintenance.

---

### Set Up Preferred Workers

You can make a preference regarding which workers are allocated to complete work orders during work order scheduling. The use of this functionality is optional, but it can help you make a choice for the most qualified worker to complete a job, based on worker skills, competencies, and customer relations. Therefore, during work order scheduling, the setup in the **Preferred workers** form is used to determine if a specific worker or worker group should be scheduled for a work order. Only workers that are available at scheduling time will be scheduled. If a preferred worker setup matches a work order during scheduling, but the selected worker is allocated to other jobs, the work order will be scheduled to another, available, worker.

Before you can set up preferred workers, you must first set up the workers and worker groups that should be available for selection. Refer to the [Workers and Worker Groups](06_Objects.md#workers-and-worker-groups) section for a description on how to set up workers and worker groups.

---

#### Set Up Preferred Workers

A preferred worker or worker group can be related to a specific

- Job trade
- Job variant

- Job type
- Job group

- Object
- Object type

- Customer account

or a combination of those selections. The more selections you make for the same record, the more specific your setup becomes.


1. Click **Enterprise asset management** > **Setup** > **Workers** > **Preferred workers**.
2. Click **New** to create a new record.

3. Start by creating a "default" worker or worker group setup that has no selections in the fields shown in the bullet list above. This means that you only make a selection in the **Preferred worker group** field and/or the **Preferred worker** field. In the figure below, you see an example in the first record in which "Requests" is selected as preferred worker group.
###### NOTE
The default setup will be used during work order scheduling in case no other, more specific, combination matches the contents of the work order during work order scheduling.

4. Repeat step 2 to create a new record. Make the required selections, depending on the detail level for the preferred worker or worker group. **Example:** In the figure below, in the sixth record, the worker Miles Reid is selected as preferred worker. He will automatically be selected during scheduling of a work order that includes the job trade "Electrical" as well as the job type "Cal. Electrical", if he is available at the scheduled time.
###### NOTE
Generally, when a preferred worker is selected during work order scheduling, Enterprise Asset Management goes through all preferred worker records to check for a possible match, always checking the most specific combination first. This means that, first, a possible match regarding **Trade** is checked. If no match is found, **Variant** is checked. If no match is found, **Job type** is checked, and so on. As you can see in the layout of the form, this means that Enterprise Asset Management checks each record from right to left for a match (**Trade**, then **Variant**, then **Job type**, **Job group**, **Object**, **Object type**, and **Customer account**) to find the most specific combination. If no match is found, the "default" record with no selections in those fields is used.


![Figure 13-02](/Figures/13-02_PreferredWorkers_Form_AX7-01.png)


###### NOTE
You can also set up responsible workers who can be selected when a request or a work order is created. In **All work orders** and **All requests**, you can edit the selection, if required. Refer to the [Responsible Workers](07_Requests.md#responsible-workers) section for more information.

During work order scheduling, different scores are calculated to determine which workers should complete the jobs related to a work order. If two or more preferred workers or responsible workers get the same score during work order scheduling (see [Enterprise Asset Management Parameters](06_Objects.md#enterprise-asset-management-parameters) and [Schedule Work Orders](13_WO_Scheduling.md#schedule-work-orders) for more information on the setup and calculation of scores for work orders), one worker is randomly selected. Otherwise, it is always the worker with the highest scores who is allocated to complete a work order.


---

### Schedule Work Orders

The required number of hours for a work order is defined by the sum of forecasted hours on the work order lines minus posted hours. If more time is required, the forecast on the work order must be adjusted accordingly. In the **All work orders** list (**Enterprise asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**), you can view or edit forecasts on a work order by selecting the work order and clicking **Forecast**. When work orders have been created and estimated, next step is to allocate the required workers and tools to complete the work orders.

Only work orders with a stage that allows scheduling can be scheduled. Allow scheduling is set up in **Work order stages** (**Enterprise asset management** > **Setup** > **Work order** > **Stage** > **Stages** > **General** FastTab > **Allow scheduling** check box).

1. Click **Enterprise asset management** > **Common** > **Work orders** > **All work orders**.
2. Select the work orders you want to schedule in the list. For example, you can sort the list by stage or customer account.

3. On the **General** tab, click **Schedule**.
4. In the **Schedule work orders** drop-down, you can add selections regarding expected start date or work order priority, if required. If the scheduling process should observe capacity limitations regarding resources already scheduled for other jobs, make sure that the **Object**, **Tool**, and **Worker** check boxes are selected.
###### NOTE
If you clear the **Object**, **Tool**, and **Worker** check boxes, existing reservations will be ignored. In the Infolog, a list of overlapping work order schedules will be shown, and you can click on the messages to open the work order and reschedule, if required.

5. To see detailed information about the scheduling process, select the **Verbose** check box. This means that detailed information about the calculated scores on the work orders and workers will be shown in the Infolog.
6. Click **OK** to start the scheduling process.

7. When scheduling is completed, an Infolog shows the number of work orders scheduled, and also more detailed information if the **Verbose** check box was selected.

###### NOTE
Work orders are scheduled in one cycle per work order, not per work order line. You can also access the **Schedule work orders** drop-down directly from the area page. Click **Enterprise asset management** > **Periodic** > **Schedule work orders**. Make your selections and click **OK** to start work order scheduling. It is possible to set up work order scheduling as a batch job in the **Schedule work orders** drop-down, on the **Run in the background** FastTab.


![Figure 13-03](/Figures/13-03_ScheduleWorkOrders_DropDown_AX7.png)


**Example:** In the figure above, the formula inserted in the **Expected start** field will generate work order scheduling for all work orders with expected start date a week from now and later. This formula may be useful when you run work order scheduling on an ongoing basis, but you want to make sure the work orders scheduled for the next 5-6 days are not rescheduled.

The work order type related to work orders may set up scheduling for one worker (refer to the [Work Order Types](08_Work_Orders.md#work-order-types) section). This means that if the work order type is used on a work order, the **One worker** check box is automatically selected in **All work orders** on the **General** FastTab. During work order scheduling, all work order lines created on the work order will subsequently be scheduled to the same worker. It is possible to clear or select the **One worker** check box in **All work orders** if you want to allow scheduling of several workers or one worker on the work order lines.

The scheduling process in the **Enterprise asset management** module is done by including different factors in the scheduling calculation:

- Calculating scores for both work orders and workers. The setup of three scores for work orders, and six scores relating to worker selections are done in **Enterprise asset management parameters**. Read more about the scores in the [Enterprise Asset Management Parameters](06_Objects.md#enterprise-asset-management-parameters) section.

- Checking for matching competencies, meaning skills and certificates, required to perform the job. Skills and certificates are set up on workers in the **Human resources** module (**Human resources** > **Workers** > **Workers** > select worker in the list > **Worker** tab > **Competencies** section > **Skills** and **Certificates** buttons). Also, skills and certificates can be added to job types and job trades. Read more about competencies and job types in the [Job Groups and Job Types, Variants, and Trades](08_Work_Orders.md#job-groups-and-job-types-variants-and-trades) section.


---


#### Scores Used in Work Order Scheduling

Calculating scores for a work order line is based on expected start date and priority of the work order.

**Start date** calculation: For every future date calculated from the expected start date, the start date score is subtracted and multiplied by the score, which is "10" in the examples below.

**Criticality** calculation: Criticality score multiplied by the criticality on the work order.

**Priority** calculation: Priority score divided by the priority on the work order.

In the examples below, the criticality scores is "2", and the priority scores are "5" and "100".

**Example 1:**
(WO means "Work order")

| Work Order ID | Expected start date| WO criticality | WO priority | Calculation                    | Score   |
|--------|--------|--------|--------|--------|--------|
|WO-00010816    |Tomorrow            |2               |20           | (-1 x 10) + (2 x 2) + 5 / 20   |- 5.75   |
|WO-00010817    |Two days from now   |2               |20           | (-2 x 10) + (2 x 2) + 5 / 20   |- 15.75  |
|WO-10010818    |Two days from now   |3               |5            | (-2 x 10) + (2 x 3) + 5 / 5    |- 13     |


The work orders will be scheduled in the following order: WO-000108**16**, WO-000108**18**, WO-000108**17**.

---

**Example 2:**
(WO means "Work order")

| Work Order ID | Expected start date| WO criticality | WO priority | Calculation                      | Score   |
|--------|--------|--------|--------|--------|--------|
|WO-00010816    |Tomorrow            |2               |20           | (-1 x 10) + (2 x 2) + 100 / 20   |-  1    |
|WO-00010817    |Two days from now   |2               |20           | (-2 x 10) + (2 x 2) + 100 / 20   |- 11    |
|WO-10010818    |Two days from now   |3               |5            | (-2 x 10) + (2 x 3) + 100 / 5    |   6    |


If the priority score was increased to '100' instead of '5', the order would be: WO-000108**18**, WO-000108**16**, WO-000108**17**.

The six rating scores relating to calculating which workers should work on the work orders are all set up as numbers, which are added to each worker during work order scheduling. The worker with the highest score is selected on the work order. Here is a short description of the worker scores:


**Responsible worker**

If the worker is selected as responsible worker on the work order, the score is added.


/--------------------------------/


**Responsible worker group**

If the worker is part of the responsible worker group on the work order, the score is added.


/--------------------------------/


**Preferred worker**

If the worker is selected as preferred worker on the object, the score is added.


/--------------------------------/


**Preferred worker group**

If the worker is part of the preferred worker group on the object, the score is added.


/--------------------------------/


**Location**

If your company uses functional locations, workers get full score if they are located on the functional location related to the object. If the functional location of the object has a parent location, workers on that functional location get 1/2 score. If that location also has a parent, workers on that location get 1/3 score. If that location also has a parent, workers on that location get 1/4 score, and so on.

If you company uses object location, which we do not recommend, location, area, and zone are used to calculate location scores. Workers get full score if they are located in the location and area and zone related to the object. If worker location only matches location and area, the rating score for the worker is 2/3 of the full score. If worker location only matches location, the rating score for the worker is 1/3 of the full score.


/--------------------------------/


**Start date**

For every date that the scheduled start date is later than the expected start date, the score is subtracted.


/--------------------------------/


###### NOTE
If a score is set to "0", that score is not calculated. This is useful if, for example, you do not want to include responsible worker in your scheduling.


#### Competencies Used in Work Order Scheduling

Skills and certificate requirements can be set up on job types (**Enterprise asset management** > **Setup** > **Object** > **Job** > **Job types**) and job trades (**Enterprise asset management** > **Setup** > **Object** > **Job** > **Job trades**). Job types and job trades are selected on work order lines. If skills or certificates have been selected on a job type or job trade, and that job type or job trade is used on a work order line, only workers with matching skills and certificates are scheduled to work on the work order.


---

### Schedule Exclusively

You can schedule one work order or work order lines to one worker using the Schedule exclusively functionality.


1. Click **Enterprise asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.
2. Select the work order in the list.

3. On the **General** tab, click **Schedule exclusively**.
4. Select the worker in the **Worker** field.

5. In the **Schedule hours** field, you can insert expected work hours, in case expected work hours differ from forecast hours.
6. In the **Scheduled start** field, you can insert another start date and time if you do not want to use expected start date and time.

7. If the scheduling process should observe capacity limitations regarding resources already scheduled on other jobs, make sure that the **Object**, **Tool**, and **Worker** check boxes are selected. If you want to see detailed information about the scheduling process, select the **Verbose** check box. This means detailed information about the calculated scores on the work order is shown in the Infolog.
8. Select the **Ignore calendar** check box to ignore closed days in the calendar (applies to object, worker, and tools). Select the **Ignore scheduled execution** check box to ignore limitations that may have been selected on the work order regarding scheduling. Refer to the [Scheduled Execution](08_Work_Orders.md#scheduled-execution) section for information on the setup of scheduled execution.

9. Click **OK**. The work order stage is automatically updated to the "Scheduled" stage specified in the work order stage group.


![Figure 13-04](/Figures/13-04_WO_ScheduleExclusively_AX7_v103.png)


###### NOTE
If you want to delete the schedule on a work order, this is done by selecting the work order in the **All work orders** list, and clicking **Delete schedule** on the **General** tab. Remember to manually update the work order stage if you delete the schedule.


---

### Schedule Work Order on Specific Date and Time

If a work order must be scheduled on a specific date and time, for example, if a customer has been promised that a service job will be done the day after tomorrow, you can override the usual scheduling process in Enterprise Asset Management and create a specific schedule for a work order.

1. Click **Enterprise asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders** or **My active work orders**.
2. In the work order list, click on the Work order ID in the **Work order** column.

3. Click **Edit**.
4. In **All work orders** Detail view > **Work order header** FastTab, insert start and end dates and times in the **Expected start** and **Expected end** fields. 
![Figure 13-05](/Figures/13-05_WO_ScheduleSpecificDateAndTime_AX7-001.png)

5. On the **General** tab, click **Schedule** to use the standard scheduling process, or click **Schedule exclusively** if you want to schedule the work order to one worker.
6. In order to override any existing capacity reservations to ensure that the work order is scheduled in the expected period, clear the **Object**, **Tool**, and **Worker** check boxes on the **Parameters** FastTab > **Finite capacity** section. This means that the scheduling process will ignore existing capacity reservations because the work order must start on the expected start time. 
![Figure 13-06](/Figures/13-06_WO_ScheduleSpecificDateAndTime_AX7-002.png)

7. Click **OK** to start scheduling.
8. If the scheduling process results in double bookings, you will see a message on the screen, and you can adjust the related work orders. In the figure below, an example of a message displaying overlapping schedules is shown.


###### NOTE
In order for this manual scheduling process to succeed, the schedule execution type used for the work order during scheduling must be "Date and time". This is set up in **Scheduled execution**. Refer to the [Scheduled Execution](08_Work_Orders.md#scheduled-execution) section for more information.

Also, in order to schedule a worker for the work order, that worker must be available at the expected start date and time. Worker availability is set up in the worker calendar. Read more about calendar setup in the [Set Up Worker Calendar](#set-up-worker-calendar) section.


---

### Work Order Calendar

The **Work order calendar** list is used to get an overview of the work orders allocated to a resource. Work orders using resource types "Human resources", "Tools", and "Machines" are displayed in the list. The list can be used to get an overview of work orders allocated to a specific resource. You can also use it to quickly find a work order allocated to a worker who, for example, called in sick this morning, and then quickly allocate another worker to the job.


#### View Work Order Calendar

1. Click **Enterprise asset management** > **Common** > **Work orders** > **Work order calendar**.
2. You will see a list of all work orders set to stage "Scheduled" or "In progress".

3. You can sort the list, for example, by worker. You can also use the filter at the top of the list page to limit the list to display work orders allocated to a specific resource or worker.
4. You can see notes on the work order and, if required, add new notes by selecting the work order line in the list and clicking **Notes**.

5. If you want to allocate one worker to a work order, select the work order in the list, and click **Schedule exclusively**.

###### NOTE
Read more about scheduling several work orders or one work order in the [Schedule Work Orders](#schedule-work-orders) and [Schedule Exclusively](#schedule-exclusively) sections.


![Figure 13-07](/Figures/13-07_WO_Calendar_List_AX7-01.png)


---

### Calculate Capacity Load on Scheduled Work Orders

You can calculate capacity load on scheduled work orders to get an overview of the work load on resources for a specific period. Calculations can be made for the following resources: Workers, worker groups, tools, and objects.


1. Click **Enterprise asset management** > **Inquiries** > **Schedule** > **Scheduled capacity load**.
2. Click **Calculate**.

3. In the **Show** field, select which load type you want to calculate: "Capacity", "Reserved", or "Remainder".
4. Select the **Skip zero** check box if you do not want to show results containing zero.

5. Select the resource types for which you want to calculate capacity load by selecting the relevant check boxes: **Worker**, **Worker group**, **Tool**, and **Object**.
6. Select the start date for the calculation in the **From date** field.

7. In the **Interval type** field, select the interval for the calculation: "Day", "Week", "Month", or "Quarter".
8. In the **Interval** field, insert the number of intervals you want to calculate. For example, if you have selected "Day" as the interval type, and you insert the number "5" in this field, a calculation of five days from the start date will be made.

9. Click **OK** to start the calculation.


![Figure 13-08](/Figures/13-08_ScheduledCapacityLoad_Form_AX7-01.png)


###### NOTE
If you select the load types "Capacity" or "Remainder" for your calculation, the same result will be displayed if no reservations have been made for the resources in the selected period.

Refer to the [Calculate Capacity Load](12_Capacity_Planning.md#calculate-capacity-load) section for information about how to calculate capacity load on object calendar lines and not scheduled work orders.

