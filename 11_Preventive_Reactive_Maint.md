# Preventive and Reactive Maintenance

Preventive maintenance is a discipline involving planned maintenance jobs, for example, regular service, calibration, and inspections. In **Enterprise Asset Management**, you can create maintenance sequences and set them up on objects or functional locations. You can also set up rounds on functional locations. Maintenance sequences on objects are active regardless of where the object is installed. Maintenance sequences and rounds on functional location are active for the objects currently installed at the location. Instead of setting up maintenance sequences on objects, or setting up rounds on functional locations, you can create rounds that include multiple objects on which you need to perform related types of maintenance jobs in the same work routine. Rounds created from objects - instead of created on functional locations - means that you can select a number of objects for one round that are not depending on being installed on the same functional location.

### Preventive Maintenance Overview

Maintenance sequences are used for preventive and reactive maintenance on individual objects. Rounds are used for preventive maintenance on a group or a set of objects. Maintenance sequences and rounds are used for generating work order proposals. The work order proposals are saved as object calendar lines, which can be bundled and converted into work orders.

The figure below provides an overview of the work flow from creating maintenance sequences and rounds to creating work orders for objects, based on those sequences and rounds.


![Figure 11-01](/Figures/11-01_PreventiveMaint_Workflow_Graphic_AX7.png)


---

### Maintenance Sequences

A maintenance sequence defines when a pre-planned preventive maintenance job is to be carried out on an object. Maintenance sequences can be related to objects, object types, functional locations, or functional location types, but first you create the maintenance sequences to be used in your company.

A maintenance sequence can have multiple maintenance sequence lines. Job type and interval are specified on the maintenance sequence line. There are two types of maintenance sequence lines:

- Time
- Counter

Maintenance sequence lines of type "Time" are used for recurring planned maintenance based on a fixed time interval. Maintenance sequence lines of type "Counter" are used for planned maintenance or reactive maintenance based on object counter registrations. A maintenance sequence may include several maintenance sequence lines of both types.

###### NOTE
If no counter values have been registered for a counter type on an object, the maintenance sequence lines are omitted.

First, you create the maintenance sequences you require for your preventive maintenance jobs and select the object types, objects, functional location types, and functional locations that should be related to each maintenance sequence. Afterwards, if required, you can also add maintenance sequences to an object or a functional location, which is done in **All objects** > select object > **Preventive maintenance** FastTab, or **All functional locations** > select functional location > **Preventive maintenance** FastTab.

If you add a maintenance sequence to object types or functional location types, it means that when you create new objects or functional locations with those object types or location types, the object or functional location will automatically be added to the maintenance sequence. The start date of the relation to a maintenance sequence will be the current date, which may need to be adjusted.

---

#### Set Up Maintenance Sequences

This sub section describes how to set up maintenance sequence lines and provides examples of how they can be used.

1. Click **Enterprise asset management** > **Setup** > **Preventive maintenance** > **Maintenance sequences**.
2. Click **New** to create a new sequence.

3. Insert a maintenance sequence ID in the **Maintenance sequence** field, and a name in the **Name** field.
4. In the **Plan date** field, insert the start date from which planning can be done on the maintenance sequence. Note that time-based maintenance sequence lines may have other plan dates.

5. Select the **Active** check box to show "Yes" to activate the maintenance sequence.
###### NOTE
If you deactivate a maintenance sequence, no calendar posts will be created in the object calendar when you run a [schedule maintenance sequence](#schedule-maintenance-sequences) job.

6. On the **Lines** FastTab, click **Add line** to create a new line.

7. Select the relevant line type, "Time" or "Counter", and click **Create**.
8. Insert a description for the line in the **Description** field. The description is later transferred to the related work orders.

9. In the **Job type** field, select the job type for which the maintenance sequence line is relevant.
10. In the **Variant** and **Trade** fields, select the job variant and job trade related to the job type.

11. In the **End days** and **End hours** fields, you can insert expected end date in days or hours. The expected end date is inserted relative to the expected start date, which is calculated when object calendar lines are created. For example, you can insert "7" in the **End days** field to indicate that the related job should be completed within a week from the expected start date.
12. In the **Interval type** field, select the type of interval to be used on the maintenance sequence line, for example, "Repeated..." or "Once...". In the Interval Types Overview below, you will see a description of the relation between interval types and line types.

13. In the **Interval** field, insert the number of times the line should be used for planning preventive maintenance jobs. Example: If you have created a line of type "Counter", and your counter is production quantity, and you insert the number "20000" in this field, new object calendar lines are created during preventive maintenance scheduling every time you are expected to produce 20,000 more items.
14. The **Omit overlap** check box relates to time-based as well as counter-based line types. Select the check box to delete object calendar entries that are created on the same date. This is relevant if, for example, you have created a 1-month inspection line, a 6-month inspection line, and a 1-year inspection inspection line. For the 1-year inspection you only want that inspection to be done, not the two other inspections, which would also fit in the time frame. In order to set up this example correctly, you set up the 1-year inspection line as the first line, the 6-month line as the second line, and the 1-month line as the third line, and you select the **Omit overlap** check box for the 1-month and 6-month lines. That way you ensure that when you reach the 1-year mark, the inspections for one month and six months are omitted, and an object calendar line is only created for the 1-year inspection line.
###### NOTE
The example described in this step shows that the most comprehensive job, which contains the largest number of tasks, and which is not done so often, should always be inserted as the first line. The more frequent jobs are then inserted as separate lines in the order of frequency, placing the most frequent job at the bottom of the list.

15. The **Counter** field only relates to counter-based line types. Select the counter type to be used on the line. If a counter type is not active on a related object, the maintenance sequence line is omitted.
16. The **Counter time fence** field only relates to counter-based line types. Insert a number that defines how many days back counter registrations are checked when maintenance sequence scheduling is done. This means how far back are data (existing counter registrations) used as basis for calculating the trend that determines how many object calendar lines are created.
++Example:++ If counter registrations are expected to be made once a month, you may insert the number '365' in this field because maintenance sequence scheduling will always be based on the last 12 months and therefore create object calendar lines based on the trend of the past year. On the other hand, if you insert the number '10' in this field, you expect counter registrations to be made more often, for example, on a daily basis. This means that when you schedule maintenance sequences, counter registrations for the last 10 days are used as the basis for the scheduling of object calendar lines.

17. The **Period** field only relates to time-based line types. Select the period type related to the interval.
18. The **Plan date** field only relates to time-based line types. If the maintenance sequence line has another planning date than the entire maintenance sequence, select a date in the **Plan date** field on the line.

19. In the **Priority** field, you can select a work order priority as a further delimitation on the maintenance sequence line - to be used as a priority on work orders.
20. Select the **Auto create** check box if you want a work order to be automatically created according to the selected maintenance sequence line when scheduling maintenance sequences.

21. If you have selected the **Auto create** check box, you can select a work order type for the auto-created work order in the **Work order type** field. If you have selected the **Auto create** check box, and you do not select a work order type in this field, the work order type selected in the **Enterprise asset management parameters** form is used (**Enterprise asset management** > **Setup** > **Enterprise asset management parameters** > **Work orders** link > **Preventive work order type** field).
22. On the **Objects** FastTab, select the objects that should be related to the maintenance sequence.

23. On the **Object types** FastTab, select the object types that should be related to the maintenance sequence.
24. On the **Functional locations** FastTab, select the functional locations that should be related to the maintenance sequence. If required, you can make the setup more specific by selecting a related object type, product, and model.

25. On the **Functional location types** FastTab, select the functional location types that should be related to the maintenance sequence.


###### NOTE
When work orders are manually created on objects that are covered by a vendor warranty, a dialog box is shown to make the user aware of the warranty. The creation of the work order can then be canceled. The check for a warranty relation is omitted for work orders that are automatically created.

---


### Interval Types Overview

---

**Interval type and Description**

*Interval type*: Repeated from plan date

The count starts from the plan date used, and when you schedule maintenance sequences, object calendar lines are created for when the interval is expected to be reached.

*Line type*: Time

The **Plan date** on the maintenance sequence line is used. If no plan date is selected on the line, the **Plan date** for the maintenance sequence is used.

Example: If the number "3" is inserted in the **Interval** field, and "Year" is selected in the **Period** field, a new object calendar line will be created once every 3 years.

*Line type*: Counter

The **Plan date** for the maintenance sequence is used.

If the counter has been replaced, the latest replacement date is used as the plan date.

---

/--------------------------------/

---

**Interval type and Description**

*Interval type*: Repeated from start date

The count starts from the start date on the object relation. The date is selected in the **Object** form > **Preventive maintenance** FastTab > **Start date** field, or in the **Functional location** form > **Preventive maintenance** FastTab > **Start date** field. When you schedule maintenance sequences, an object calendar line is created when the interval is reached.

*Line type*: Time

The start date of the maintenance sequence line on object or functional location is used. If that field is blank, the **Plan date** for the maintenance sequence is used.

*Line type*: Counter

The start date of the maintenance sequence line on object or functional location is used. If that field is blank, the **Plan date** for the maintenance sequence is used.

---

/--------------------------------/

---

**Interval type and Description**

*Interval type*: Repeated from last work order

The count starts from the actual end date and time of the latest work order that was completed on the object ++and++ the job type / variant / trade combination. That date and time is shown in the **Actual end** field in the **Work order** form.

*Line type*: Time

The actual end date and time of the work order completed on the object ++and++ the job type / variant / trade combination. is used. If no completed work order is found, one of the dates used in the "Repeated from start date" interval type described above is used instead.

*Line type*: Counter

The actual end date and time of the work order completed on the object ++and++ the job type / variant / trade combination. is used. If the end date and time was left blank on the work order, one of the dates used in the "Repeated from start date" interval type described above is used instead.

---

/--------------------------------/

---

**Interval type and Description**

*Interval type*: Once from plan date

See description for the "Repeated from plan date" interval type above. Only difference is that this interval type is to be used only once.

*Line type*: Time

See description for "Repeated from plan date" interval type above. This interval is typically used for a one-time maintenance or service job.

*Line type*: Counter

See description for "Repeated from plan date" interval type above. This interval is typically used for a one-time maintenance or service job.

**Note 1:** This interval type is only relevant if the counter is replaced every time you carry out a maintenance or service job. If, for some reason, a counter has been replaced before the end of the planned interval, a new time is calculated for the job from the time of the counter replacement.

**Note 2:** If the counter is replaced when completing the maintenance or service job, this interval type functions as the "Repeated from plan date" interval type above.

---

/--------------------------------/

---

**Interval type and Description**

*Interval type*: Once from start date

See description for the "Repeated from start date" interval type above. Only difference is that this interval type is to be used only once.

*Line type*: Time

See description for "Repeated from start date" interval type above. This interval is typically used for a one-time maintenance or service job.

*Line type*: Counter

See description for "Repeated from start date" interval type above. This interval is typically used for a one-time maintenance or service job.

**Note 1** above also applies to this interval type.

**Note 3:** If the counter is replaced when completing the maintenance or service job, this interval type functions as the "Repeated from start date" interval type above.

---

/--------------------------------/

---

**Interval type and Description**

*Interval type*: Once from last work order

See description for the "Repeated from last work order" interval type above. Only difference is that this interval type is to be used only once.

*Line type*: Time

See description for "Repeated from last work order" interval type above. This interval is typically used for a one-time maintenance or service job.

*Line type*: Counter

See description for "Repeated from last work order" interval type above. This interval is typically used for a one-time maintenance or service job.

**Note 1** above also applies to this interval type.

**Note 4:** If the counter is replaced when completing the maintenance or service job, this interval type functions as the "Repeated from last work order" interval type above.

---

/--------------------------------/

---

**Interval type and Description**

*Interval type*: Once reached above

This interval type only relates to counters and is used for indicating an upper limit set up on the maintenance sequence line. Object calendar entries will have the expected start date and time of the counter registration meaning that these entries will be created with an expected start date equal to or earlier than the system date.

*Line type*: Time

N/A

*Line type*: Counter

The counter interval indicates an upper limit. If that limit is exceeded when you create a counter registration, an object calendar line is created when you schedule preventive maintenance.

---

/--------------------------------/

---

**Interval type and Description**

*Interval type*: Once reached below

This interval type only relates to counters and is used for indicating a lower limit set up on the maintenance sequence line. Object calendar entries will have the expected start date and time of the counter registration meaning that these entries will be created with an expected start date equal to or earlier than the system date.

*Line type*: Time

N/A

*Line type*: Counter

The counter interval indicates a lower limit. If that limit is passed when you create a counter registration, an object calendar line is created when you schedule preventive maintenance.

---

/--------------------------------/

---

**Interval type and Description**

*Interval type*: Linked from start date (once only)

A maintenance sequence can contain more lines using this interval type, and those lines are linked. Typically, you will create a maintenance sequence that contains lines of only this interval type.

Object calendar lines are created by identifying the maintenance sequence line that has the first expected start date and time.

*Line type*: Time

See description for "Once from start date" above.

Example: You create two lines in a maintenance sequence for a service job on a car: one time-based line with a 1-year period, and one counter-based line with a 25,000 km limit. An object calendar line is created for the limit that is reached first. For this line type you create the line with the 1-year period.

*Line type*: Counter

See description for "Once from start date" above.

Example: You create two lines in a maintenance sequence for a service job on a car: one time-based line with a 1-year period, and one counter-based line with a 25,000 km limit. An object calendar line is created for the limit that is reached first. For this line type you create the line with the 25,000 km limit.

Example creating two counter lines: You can also set up a maintenance sequence with two linked, counter-based lines in which the first line has a limit of 10,000 items quantity produced, and the second line relates to the machine or work center requiring service after running 3,000 hours.

---

/--------------------------------/

---

**Interval type and Description**

*Interval type*: Linked from last work order (repeated after every completed work order)

A maintenance sequence can contain more lines using this interval type, and those lines are linked. Typically, you will create a maintenance sequence that contains lines of only this interval type.

Object calendar lines are created by identifying the maintenance sequence line that has the first expected start date and time.

*Line type*: Time

This interval type basically works as "Linked from start date" described above. Only difference is the date on which the interval type is based. The date used is the actual date and time on the latest work order completed on the object ++and++ the job type / variant / trade combination.

*Line type*: Counter

This interval type basically works as "Linked from start date" described above. Only difference is the date on which the interval type is based. The date used is the actual date and time on the latest work order completed on the object ++and++ the job type / variant / trade combination.

---

/--------------------------------/


---

###### NOTE
When object calendar lines are created for time-based maintenance sequence lines, expected time is always at the start of the day. For counter-based maintenance sequence lines, expected time can be anytime during the day.

Below you will find examples of the setup of time-based and counter-based maintenance sequence lines:

**Example 1 - Time-based maintenance sequence line:** A lubrication job may be set up in a fixed interval, occurring once a week. For that purpose, select "Repeated from plan date" in the Interval type field.


![Figure 11-02](/Figures/11-02_MaintSequenceLine_Example_RepeatedFromPlanDate-AX7.png)


**Example 2 - Time-based maintenance sequence line:** An inspection job may be set up to be carried out approximately once a week. For that purpose, select "Repeated from last work order" in the Interval type field.

![Figure 11-03](/Figures/11-03_MaintSequenceLine_Example_RepeatedFromLastWO-AX7.png)


**Example 3 - Counter-based maintenance sequence line:** A graphical illustration of an hour counter for which a new object calendar line is created each time 250 hours have passed. The interval type for this counter-based line is "Repeated from start date". The start date is the start date of the related objects in the **Object** detail view > **Preventive maintenance** FastTab > **Start date** field, or in the **Functional location** detail view > **Preventive maintenance** FastTab > **Start date** field. This is an example of a ++preventive++ maintenance sequence because the object calendar line is automatically created each time the threshold (+ 250) is reached.

![Figure 11-04](/Figures/11-04_CounterRepeated_IncreasingValue.png)


**Example 4 - Counter-based maintenance sequence line:** A graphical illustration of a decrease in counter value, measuring brake pad wear. An object calendar line is created when a counter registration below 20 mm is created on the brake pad. The interval type for this counter-based line is "Once reached below" or "Once from last start date". This is an example of a ++reactive++ maintenance sequence because the object calendar line is not created until a measurement below 20 mm is registered.

![Figure 11-05](/Figures/11-05_CounterReplaced_DecreasingValue.png)


**Example 5 - Counter-based maintenance sequence line:** A graphical illustration of a counter with a threshold of -18° Celsius. An object calendar line is created when a counter registration above -18° Celsius is made. The interval type for this counter-based line is "Once reached above". This is an example of a ++reactive++ maintenance sequence because the object calendar line is not created until a measurement higher than -18° Celsius is registered.

![Figure 11-06](/Figures/11-06_CounterReplaced_OnceReached.png)


###### NOTE
When you create a new object, and that object uses an object type related to a maintenance sequence, the maintenance sequence is automatically inserted in **All objects** > **Preventive maintenance** FastTab. Also, in the **Object types** setup, on the **Maintenance sequences** FastTab, the related maintenance sequences will automatically be inserted.
If you add or remove object types or functional location types in **Maintenance sequences**, that change will only reflect on new objects created after you made the change.
If you add or remove objects or functional locations in **Maintenance sequences**, that change will automatically be updated in **All objects** > **Preventive maintenance** FastTab, or in **All functional locations** > **Preventive maintenance** FastTab.


![Figure 11-07](/Figures/11-07_MaintenanceSequences_Form_AX7-01.png)

---

#### Add a Maintenance Sequence to an Object

1. Click **Enterprise asset management** > **Common** > **Objects** > **All Objects** or **Active objects**.
2. Select the object on which you want to set up a maintenance sequence and click **Edit**.

3. On the **Preventive maintenance** FastTab, click **Add line** to add a maintenance sequence to the object.
4. In the **Maintenance sequence** field, select the relevant sequence.

5. In the **Start date** field, select the date from which planning of preventive maintenance jobs can be done.


![Figure 11-08](/Figures/11-08_ObjectForm_PrevMaintenanceFastTab_AX7-01.png)


---

### Schedule Maintenance Sequences

Preventive maintenance scheduling generates calendar entries on objects, based on the maintenance sequences set up on the objects. You can schedule calendar entries based on selected maintenance sequences, object types, and objects.

1. Click **Enterprise asset management** > **Periodic** > **Preventive maintenance** > **Schedule maintenance sequences**.
2. You can select a time interval in the **Interval** and **Period** fields.
###### NOTE
The **Period** and **Interval** fields indicate how far ahead in time you want object calendar lines to be created, based on the maintenance sequences that you have created (time-based or counter-based). In the figure below, object calendar lines (= work order proposals) are created from the current date and three months onwards.

3. Select the **Auto create** check box if work orders should automatically be created according to the maintenance sequence line.
###### NOTE
If this check box is selected, and the **Auto create** check box is also selected on maintenance sequence lines in **Maintenance sequences**, work orders are created based on the maintenance sequence lines, and object calendar lines with status "Work order created" are also created. If only one of the **Auto create** check boxes is selected, in this form or in **Maintenance sequences**, only object calendar lines are created with status "Created". In that case, no work orders are created.

4. It is possible to generate calendar entries based on maintenance sequences (time or counter), objects, object types, functional locations, and functional location types. Click the **Filter** button and make your selections, if relevant.
###### NOTE
Regarding scheduling of maintenance sequences on functional locations: If you update the setup of object types, products, and models on maintenance sequences in **All functional locations** > **Maintenance sequences** FastTab after you have scheduled maintenance sequences, existing object calendar entries related to that functional location are automatically deleted. In order to create new calendar entries, which correspond with the updated maintenance sequence setup on the functional location, you must run a new maintenance sequence schedule for that functional location. Read more about the setup of object types, products, and models on functional locations in the [Create Functional Locations](05_Functional_Locations.md#create-functional-locations) section.
**Example:** You want to create a maintenance sequence for a specific functional location, meaning all objects set up on that functional location at any given time will be included when you run the sequence. In that case, you create a maintenance sequence and select the specific functional location, but you do NOT add any objects in the maintenance sequence. The result is that when you run that maintenance sequence, object calendar lines will be created for all the objects related to the functional location at that time.
If you make changes to object types, products and models in Object types, those changes only affect new objects that use the updated object type. Read more about object type setup in the [Object Types](06_Objects.md#object-types) section.

5. Click **OK** to start the generation of calendar posts on objects. The generated calendar posts will be displayed in the **Object calendar**.


![Figure 11-09](/Figures/11-09_ScheduleMaintSequences_DropDown_AX7-01.png)


###### NOTE
In **Schedule maintenance sequences**, you can set up batch jobs on the **Run in the background** FastTab to automatically generate calendar entries at regular intervals.
When you schedule preventive maintenance, object calendar lines with expected start date and time earlier than the system date and time will not be created.

The figure below provides a graphic illustration of a time-based maintenance sequence calculation.


![Figure 11-10](/Figures/11-10_Graph_CalculateMaintJobs.jpg)


Regarding counter-based maintenance sequences: In the figures below, two different counter registration cycles are shown. They are based on a maintenance sequence set up for object "V0001", expecting the object (a car) to run approx. 2,000 km every month.

In the first example, the expected 2,000 km are not reached every month. According to the counter-based maintenance sequence, the threshold is 2,000 km, meaning when you run a maintenance sequence scheduling, an object calendar line should be created each time the 2,000-kilometer threshold is reached. In example 1, there are 4 registration lines, but the 2,000-kilometer threshold is only reached once. This means that when you run schedule maintenance sequences for this object, for example for a 3-month period, only one object calendar line will be created.

In next figure, 2,000 km or more are registered every month. Therefore, three object calendar lines would be created if you schedule maintenance sequences for this object for a 3-month period.

The examples described here show that all counter registrations made on an object show a trend describing wear and tear on the object. That trend is used as calculation basis at the time of maintenance sequence scheduling.


![Figure 11-11](/Figures/11-11_CounterRegistrations_ObjectCounters_AX7-01A.png)


![Figure 11-12](/Figures/11-12_CounterRegistrations_ObjectCounters_AX7-02A.png)


---


### Rounds

In Enterprise Asset Management, you can create rounds for various objects, on which you need to carry out a similar task at regular intervals. For example, lubrication jobs or safety inspection jobs that need to be carried out on a number of machines within the same intervals. First step is to create a round, including objects that require the same form of maintenance job or service job. Next, you schedule the rounds. When you have completed the rounds schedule, you can see all the job records relating to the round in the **All object calendars**, **Open object calendars**, or **Open object calendar pools** grid views.

###### NOTE
Rounds can also be set up on functional locations to be completed on the objects installed on the functional location at the time of creation of the round-based work order. Refer to the [Create Functional Locations](05_Functional_Locations.md#create-functional-locations) section for more information on the setup of rounds on functional locations.


#### Set up a Round

1. Click **Enterprise asset management** > **Setup** > **Preventive maintenance** > **Rounds**.
2. Click **New** to create a new round.

3. Insert and ID in the **Round** field, and a name for the round in the **Name** field.
4. Select a start date for the round in the **Start date** field.
5. Select the **Auto create** check box if work orders should automatically be created from object calendar lines that are created from this round.

6. In the **Work order type** field, select the work order type to be used on work orders created from this round.
7. In the **Priority** field, select the work order priority to be used on work orders created from this round.
8. On the **Lines** FastTab, click **Add** to add an object to the round.

9. Insert a line number in the **Line number** field to indicate the sequence of the objects in round.
10. Select the object in the **Object** field.
11. Select the job type for the object in the **Job type** field.

12. Select the job variant and job trade related to the job type in the **Variant** and **Trade** fields.
13. Select the recurrence (day, week, etc.) in the **Period type** field.
14. In the **Period length** field, insert the number of recurrences for the round.

15. Select a start date for the object to be included in the round in the **Start date** field. This date may differ from the start date set on the round.
16. Repeat steps 8-15 to add more objects to the round.

17. On the **Pools** FastTab, click **Add** to select a work order pool to which you want to connect the round. Several work order pools can be connected to one round.


###### NOTE
The **Objects** and **Lines** fields located in the **Details** section at the top of the form show the total number of objects and lines related to the selected round.


![Figure 11-13](/Figures/11-13_Rounds_Form_AX7-01.png)


#### Schedule Rounds

When you have set up a round, you run a schedule job to schedule all the jobs related to the round.

1. Click **Enterprise asset management** > **Periodic** > **Preventive maintenance** > **Schedule rounds**, or **Enterprise asset management** > **Common** > **Object calendar** > **All object calendars** or **Open object calendar lines** or **Open object calendar pools** > select calendar entry in the list > **Rounds** button.
2. In the **Period** field, select the period to be used for the scheduling job.

3. In the **Interval** field, insert the number of periods to be included in the scheduling job. The start of the scheduling is the current date.

4. Select the **Auto create** check box if a work order should automatically be created on the basis of a round.
###### NOTE
If this check box is selected, and the **Auto create** check box is also selected on maintenance sequence lines in **Maintenance sequences**, work orders are created based on the maintenance sequence lines, and object calendar lines with status "Work order created" are also created. If only one of the **Auto create** check boxes is selected, in this drop-down or in **Maintenance sequences**, only object calendar lines are created with status "Created". In that case, no work orders are created.

5. If required, you can select specific rounds or another start date for the schedule job. Click **Filter**, and add the rounds to be included.

6. Click **OK**.
7. You are now able to see the rounds jobs in **Enterprise asset management** > **Common** > **Object calendar** > **All object calendars** or **Open object calendars**. If the scheduled rounds are connected to a work order pool, you can also see the calendar posts in **Open object calendar pools**. The rounds jobs in the calendar have the reference type "Rounds".


![Figure 11-14](/Figures/11-14_ScheduleRounds_DropDown_AX7-01.png)


###### NOTE
When work orders are manually created on objects that are covered by a vendor warranty, a dialog box is shown to make the user aware of the warranty. The creation of the work order can then be canceled. The check for a warranty relation is omitted for work orders that are automatically created.
You can set up a batch job on the **Run in the background** FastTab to schedule rounds at regular intervals.
If a round is included in several work order pools (refer to the [Work Order Pools](08_Work_Orders.md#work-order-pools) section), one record is shown for each pool in **Open object calendar pools**. This is done to optimize the filtering options on work order pools.


---


### Object Calendar

The object calendar contains a list of all the expected preventive maintenance sequences, requests, and rounds to be carried out. Some calendar entries may have been converted to work orders.

There are four object calendar views that are slightly different, depending on which calendar posts you want to see.

**All object calendars**
All calendar entries are shown in this calendar.


**My object calendars**
All calendar entries containing objects installed on functional locations to which you are related as a worker (set up in [Workers and Worker Groups](06_Objects.md#workers-and-worker-groups)) are shown in this calendar.


**Open object calendar lines**
Calendar entries with status "Created" - meaning that they have not yet been converted to a work order or discarded - are shown in this calendar.


**Open object calendar pools**
Calendar entries connected to a work order pool are shown in this calendar.


###### NOTE
If an object calendar entry is included in several work order pools (refer to the [Work Order Pools](08_Work_Orders.md#work-order-pools) section), one record is shown for each pool in **Open object calendar pools**. This is done to optimize the filtering options on work order pools.

To open an object calendar:

1. Click **Enterprise asset management** > **Common** > **Object calendar** > **All object calendars** or **Open object calendars** or **Open object calendar pools**.
2. To update the object calendar, click **Preventive maintenance** or **Rounds**. Refer to the [Schedule Maintenance Sequences](11_Preventive_Reactive_Maint.md#schedule-maintenance-sequences) section.

3. You can edit a calendar entry by selecting it and clicking **Edit**. For example, you can easily update the priority of the job or the worker responsible for the job. You can only edit calendar entries that have not yet been connected to a work order.
4. You can delete a calendar entry by selecting it and clicking **Delete**.
5. You can discard a calendar entry by selecting it in the list page and clicking **Discard**. This function is useful if, for example, an object has a 2,000 km maintenance sequence and a 10,000 km maintenance sequence. Then, you may want to discard the 2,000 km maintenance sequence when it coincides with 10,000 km, 20,000 km, 30,000 km, and so on. If you discard a calendar entry related to a maintenance sequence, that calendar line will never again appear when that maintenance sequence is scheduled.

6. You can select a number of entries in **All object calendars** and click **Work order pool**, if you want all selected calendar entries to be included in the same work order pool.
7. You can select a number of entries in **All object calendars** or **Open object calendars** or **Open object calendar pools** and click **Adjust** if you want to make the same adjustments to several entries. You can change expected start and end dates, priority, and the responsible group or responsible worker related to the selected object calendar entries.


###### NOTE
When a calendar entry has been related to a work order, the work order ID will be displayed in the **Work order** field.
In **All objects** > **Preventive maintenance** FastTab, you can set up maintenance sequence lines for the selected object. Later, if you delete a maintenance sequence line related to an object in **All objects**, you also automatically delete all object calendar lines with status "Created" that have been created based on that maintenance sequence. See also the [Create an Object](06_Objects.md#create-an-object) section.


![Figure 11-15](/Figures/11-15_All_Object_Calendars_List_AX7-01.png)


---


### Object Calendar Cost

In Enterprise Asset Management, you can calculate budget costs on object calendar lines. This is useful if you want to get an overview of expected costs, for example, costs relating to planned preventive maintenance jobs for the next year. The calculations are based on existing object calendar lines of type "Maintenance sequence" or "Round" or "Request".

1. Click **Enterprise asset management** > **Inquiries** > **Objects** > **Object calendar cost**.
2. On the **Object calendar cost** tab, click **Calculate cost**.

3. In the **Object calendar cost control** form, you can select a financial dimension set if you want to see costs grouped in financial dimensions.
###### NOTE
Financial dimension sets are set up in **General ledger** > **Setup** > **Financial dimensions** > **Financial dimension set**.

4. You can use the **Level** field to indicate how detailed you want the object calendar lines to be regarding functional locations. For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all object calendar lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level. If you insert the number "0" in the **Level** field, you will see a detailed result showing all object calendar lines on all the functional location level to which they are related.

5. If you want to make a calculation for specific objects, click **Filter** on the **Records to include** FastTab, and select the relevant objects.
6. Click **OK** to start the calculation.

7. On the **Object calendar cost** tab > the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation. The selected action pane group buttons are highlighted in orange color. Click on a button to activate or deactivate it.


![Figure 11-16](/Figures/11-16_ObjectCalendarCost_Form_AX7-01.png)


---

### Creating Work Orders

When you have scheduled preventive maintenance jobs, next step is to create work orders for the jobs. This is done in one of the object calendars. The scheduled jobs in an object calendar can have different reference types:

**Maintenance sequences** - preventive maintenance jobs based on maintenance sequence types "Time" or "Counter".

**Rounds** - preventive maintenance job including several objects that require a similar type of maintenance.


**Requests** - manually created request for maintenance or repair of an object, which can be converted into a work order.

---

1. Click **Enterprise asset management** > **Common** > **All object calendars** or **Open object calendar lines** or **Open object calendar pools**.
2. Select the scheduled maintenance jobs for which you want to create a work order and click **Work order**. The total number of forecast hours for the selected lines is shown in the **Forecast hours** field.

3. In the **Parameters** section, select how many work orders should be created. You can create one work order per line or several work orders, based on date or various groups or types.
4. Select a **Work order type** to be used on all the work orders you create.

5. Click **OK**. One or more work orders are created.


![Figure 11-17](/Figures/11-17_CreateWorkOrders_Drop-down_AX7.png)


---

### Maintenance Stop

Maintenance stops are used to get an overview of the capacity required to carry out maintenance and service jobs on specific objects during a specific period. For example, you can create a maintenance stop for Production line 10 in Production Hall 29-A on production site 02. The maintenance stop has a start and end time indicating the period in which the objects related to the maintenance stop are not available for production.

The maintenance stop is an overview of object calendar lines and work orders on related objects during a specified period. The lines related to work orders all have an expected start date within the maintenance stop period. You can extract useful information and make adjustments to planned maintenance jobs:

- Get an overview of required shut-down periods of production equipment (objects).
- Get an overview of planned maintenance (hours), grouped by competencies (responsible worker groups or workers), for example capacity load on electricians, smiths, or other work groups required to do the planned maintenance and service jobs.

- Make adjustments to object calendar lines or work order lines related to the objects, for example, change expected start and end times on a line, or select other workers to optimize the workflow for workers and worker groups.

When objects have been selected on a maintenance stop, all open object calendar lines and work order lines relating to active work orders are included in the maintenance stop.


#### All Maintenance Stops

Click **Enterprise asset management** > **Common** > **Maintenance stops** > **All Maintenance stops** to open the list. **All maintenance stops** contains a list of all maintenance stop records and displays some of the information related to the maintenance stops.


![Figure 11-18](/Figures/11-18_AllMaintenanceStops_List_AX7-01.png)


#### Create a Maintenance Stop

1. Click **Enterprise asset management** > **Common** > **Maintenance stops** > **All maintenance stops** or **Active maintenance stops**.
2. Click **New**.

3. Insert an ID in the **Maintenance stop** field and a name in the **Name** field.
4. Insert the period for the maintenance stop in the **Start date/time** and **End date/time** fields.
5. Click **Objects** > **New** button and add objects one at a time to the maintenance stop.

6. Click **Save** when all objects have been added and return to the **All maintenance stops** list.
7. Click **Save** in **All maintenance stops** to update the number of objects added to the selected record.
8. The work order lines and open object calendar lines related to the selected objects are shown on the tabs on the **Related** FastTab. On the **General** FastTab > **Forecast hours** fields, you see the total number of hours forecasted for object calendar lines and work order lines.
###### NOTE
The object calendar lines and work order lines related to the selected objects are automatically updated if new work orders or object calendar lines have been created after you created the maintenance stop. For example, if you schedule maintenance sequences or rounds on the related objects two days after the maintenance stop was created, new object calendar lines are automatically added to the maintenance stop record.

9. In **All maintenance stops** > **Maintenance stop** tab > click **Capacity load** > **Capacity load** > **Calculate capacity load** to calculate forecasted hours and group them to get an overview of capacity load on, for example, by date, object, object type and job type. Click **OK** in the **Capacity load** drop-down. Note that the dates shown in the **Capacity load** drop-down are the start and end dates selected in **All maintenance stops**. This calculation only includes the objects related to the maintenance stop.
10. The total number of hours is shown in the **Capacity load** overview.
11. On the **Capacity load** tab > the **Group by...** action pane groups, click the relevant buttons to get a more detailed overview of the allocation of forecasted hours.

12. After you get an overview of the capacity load, if you want to make adjustments on object calendar lines or work order lines, return to **All maintenance stops** detail view and select the lines you want to adjust on the **Related** FastTab.
13. Click the **Adjust** button and update expected start/end dates, priority, or responsible workers for the selected object calendar lines or work order lines.
14. Click **OK** when you have made the required adjustments. Object calendar lines or work order lines that are not included in the maintenance stop period after you have made adjustments are automatically removed from **All maintenance stops**.
###### NOTE
When you make adjustments to work order lines, you change the related work order.

15. In **All maintenance stops** > **Maintenance stop** tab > click **Item forecast** > **Item forecast** > **Calculate item forecast** to calculate forecasts for items (spare parts and other required items) and group them to get an overview, for example, by date, object, object type and job type. Click **OK** in the **Calculate item forecast** drop-down. Note that the dates shown in the **Item forecast** calculation form are the start and end dates selected in **All maintenance stops**. This calculation only includes the objects related to the maintenance stop.

16. The total number of item forecasts is shown in **Item forecast**, and you can now select the relevant check boxes to get a more detailed overview of the allocation of forecasted items.


![Figure 11-19](/Figures/11-19_MaintenanceStop_Form_AX7-01.png)


###### NOTE
You can copy objects from one maintenance stop to another. In **All maintenance stops**, select the **Copy maintenance stop** button, and make your selections in the **From maintenance stop** and **To maintenance stop** fields, and click **OK**.
In **All maintenance stops**, click the **Object calendar lines** button or the **Active work orders** button to open the related lists and view the lines related to the selected maintenance stop.


![Figure 11-20](/Figures/11-20_MaintenanceStopObjects_Form_AX7-01.png)

![Figure 11-21](/Figures/11-21_CapacityLoad_MaintenanceStop_Form_AX7-01.png)

![Figure 11-22](/Figures/11-22_ItemForecast_MaintenanceStop_Form_AX7-01.png)

