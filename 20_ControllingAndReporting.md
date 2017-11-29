# Controlling and Reporting

### Cost and Date Control

In Enterprise Asset Management, you can calculate costs to get an overview of actual costs compared to budget costs on objects, functional locations, or work orders. Actual costs are based on posted transactions. You can also make a date calculation if you want to compare scheduled start and end dates to actual start and end dates on work orders.

---

#### Cost Control for Objects, Functional Locations, and Work Orders

The calculations made for objects, functional locations, and work orders are almost identical. Only difference is that for objects and functional locations, you can also include sub objects and sub locations in your calculation. The date is the transaction date when the registration was recorded.


1. Click **Enterprise asset management** > **Inquiries** > **Objects** > **Object cost control** or **Functional location cost control**, or **Enterprise asset management** > **Inquiries** > **Work orders** > **Work order cost control**.
2. Click **Cost control** > **Calculate cost**.

3. In the **Object cost control** / **Functional location cost control** / **Work order cost control** drop-down, select a period to be calculated.
4. If required, select a financial dimension set to be included in the calculation.

5. If you want to limit the search, you can select specific objects / functional locations / work orders on the **Records to include** FastTab.
6. Select the **Skip zero** check box if you do not want to show results with a cost of zero.

7. You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations. For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level. If you insert the number "0" in the **Level** field, you will see a detailed result showing all cost control lines on all the functional location level to which they are related.
8. Click **OK** to start the calculation.

9. In the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation. The selected action pane group buttons are highlighted in orange color. Click on a button to activate or deactivate it.


![Figure 20-01](/Figures/20-01_ObjectCostControl_Form_AX7-01.png)


![Figure 20-02](/Figures/20-02_FuncLocationCostControl_Form_AX7-01.png)


![Figure 20-03](/Figures/20-03_WO_CostControl_Form_AX7-01.png)


Another way of making a cost calculation is to multi-select objects in **All objects** or **Active objects** grid view. Then, you click the **Cost control** button > **Cost control** > **Calculate cost**, and you will see that the selected objects are automatically inserted in the **Object** field on the **Records to include** FastTab. Click **OK** in the **Object cost control** drop-down, and a cost calculation for the selected objects is shown. The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.


###### NOTE
The **Original budget** field shows budget costs from the work order forecast. The **Actual cost** field shows posted costs on work orders. The **Committed cost** field shows costs that your company is committed to in relation to work orders, but these costs have not yet been posted.


---

#### Work Order Date Control

Use this form to get an overview of expected start and end dates compared to actual start and end dates on work orders. Select a period for the calculation, then select the information you want to display by selecting the check boxes in the **Group by** section, and click **Calculate**.


1. Click **Enterprise asset management** > **Inquiries** > **Work orders** > **Work order date control**.
2. Click **Edit**.

3. Select a functional location in the **Functional location** field.
4. Insert the period for which you want to make the calculation in the **From date** and **To date** fields. All work orders with expected start within the period will be included.

5. In the **Group by** section, select which information you want to include in the calculation by selecting the relevant check boxes.
6. Click **Calculate**.

7. After you have made the calculation, if you select or clear check boxes in the **Group by** section, click the **Calculate** button again to update the calculation.


![Figure 20-04](/Figures/20-04_WO_DateControl_Form_AX7-01.png)


###### NOTE
The **Avg. start delay** field shows the difference in days between scheduled start date for a work order compared to actual start date. If, for example, the actual start date was two days before the scheduled start date, "-2" will be displayed in this field.
The **Avg. end delay** field shows the difference in days between scheduled end date for a work order compared to actual end date. If, for example, the actual end date was three days after the scheduled end date, "3" will be displayed in this field.
The **Occurrences** fields show the number of times deviations occur in relation to scheduled and actual start date, and scheduled and actual end date on the work order.

---

#### Work Hour Control

In Enterprise Asset Management, you can calculate hours to get an overview of actual hours compared to budget hours on objects, functional locations, or work orders. Actual hours are based on posted transactions.

The calculations made for objects, functional locations, and work orders are almost identical. Only difference is that for objects and functional locations, you can also include sub objects and sub locations in your calculation. The date is the transaction date when the registration was recorded.


1. Click **Enterprise asset management** > **Inquiries** > **Objects** > **Object hour control** or **Functional location hour control**, or **Enterprise asset management** > **Inquiries** > **Work orders** > **Work order hour control**.
2. Click **Hour control** > **Calculate hours**.

3. In the **Object hour control** form / **Functional location hour control** form / **Work order hour control** drop-down, select a period to be calculated.
4. If you want to limit the search, you can select specific objects / functional locations / work orders.

5. If required, select a financial dimension set to be included in the calculation.
6. Select the **Skip zero** check box if you do not want to show results containing zero hours.

7. You can use the **Level** field to indicate how detailed you want the hour control lines to be regarding functional locations. For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all hour control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level. If you insert the number "0" in the **Level** field, you will see a detailed result showing all hour control lines on all the functional location levels to which they are related.
8. Click **OK** to start the calculation.

9. In the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation. The selected action pane group buttons are highlighted. Click on a button to activate or deactivate it.


![Figure 20-04-01](/Figures/20-04-01_ObjectHourControl_Form_AX7.png)

![Figure 20-04-02](/Figures/20-04-02_FuncLocationHourControl_Form_AX7.png)

![Figure 20-04-03](/Figures/20-04-03_WO_HourControl_Form_AX7.png)


Another way of making a cost calculation is to multi-select objects in **All objects** or **Active objects** grid view. Then, you click the **Hour control** button > **Hour control** > **Calculate hours**, and you will see that the selected objects are automatically inserted in the **Object** field on the **Records to include** FastTab. Click **OK** in the **Object hour control** drop-down, and an hour calculation for the selected objects is shown. The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in the **All work orders** or **Active work orders**.


###### NOTE
The **Original budget** field shows budget hours from the work order forecast. The **Actual hours** field shows posted hours on work orders. The **Committed hours** field shows hours that your company is committed to in relation to work orders, but these hours have not yet been posted.


---

#### Object Fault Cost Control

In Enterprise Asset Management, you can calculate costs on object fault registrations to get an overview of actual costs compared to budget costs on faults. Actual costs are based on posted transactions. The date is the fault date on which the symptom was recorded.


1. Click **Enterprise asset management** > **Inquiries** > **Object fault** > **Object fault cost control**.
2. Click **Object fault cost control** > **Calculate cost**.

3. In the **Object fault cost control** drop-down, select a financial dimension set to be included in the calculation, if required.
4. Select the **Skip zero** check box if you do not want to show results with a cost of zero.

5. If you want to limit the search, you can select specific objects, fault dates, or fault causes on the **Records to include** FastTab.
6. You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations. For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all object fault cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level. If you insert the number "0" in the **Level** field, you will see a detailed result showing all object fault cost control lines on all the functional location level to which they are related.

7. Click **OK** to start the calculation.
8. In the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation. The selected action pane group buttons are highlighted in orange color. Click on a button to activate or deactivate it.


![Figure 20-05](/Figures/20-05_ObjectFaultCostControl_Form_AX7-01.png)


Refer to the [Fault Management](08_Work_Orders.md#fault-management) section for information on how to set up faults.

###### NOTE
The **Original budget** field shows budget costs from the work order forecast. The **Actual cost** field shows posted costs on work orders. The **Committed cost** field shows costs that your company is committed to in relation to work orders, but these costs have not yet been posted.

---

#### Object Fault Control

In Enterprise Asset management, you can analyze object fault registrations to get an overview of the total number of faults registered during a specific period. Fault registrations can be analyzed from different perspectives, for example with focus on objects, object types, functional locations, fault symptoms, or fault types.

1. Click **Enterprise asset management** > **Inquiries** > **Object fault** > **Object fault control**.
2. Click **Object fault control** > **Select faults**.

3. If you want to limit the search, you can select specific objects, fault dates, fault causes, and fault remedies on the **Records to include** FastTab.
4. You can use the **Level** field to indicate how detailed you want the fault control lines to be regarding functional locations. For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all object fault control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level. If you insert the number "0" in the **Level** field, you will see a detailed result showing all object fault control lines on all the functional location level to which they are related.

5. Click **OK** to start the calculation.
6. Click **Edit**.

7. On the **Object fault control** tab, click one or more buttons in the **Group by...** action pane groups to display the detail level you want to see. Activated buttons are shown in blue color. You can activate or deactivate a button by clicking on it.
8. On the **Object fault control** tab, click **Update**.

###### NOTE
Every time you activate or deactivate buttons in the **Group by...** action pane groups, remember to click the **Update** button after you have changed the selections. This is required because a large amount of data is processed as you are recalculating fault probability.

There are many ways to analyze fault registrations. Below you will see examples in five screenshots of how different data selections provide different pieces of information. You will see how different selections provide more insight and detail when analyzing object fault registrations.

In the screenshot below, the **Symptom** button is selected.

- There are six registrations on the fault symptom "Poor fuel economy".

- In the **Probability %** column, all percentages add up to 100%. Probability is based on all **Fault symptom** registrations in this fault control calculation.


![Figure 20-06](/Figures/20-06_ObjectFaultControl_AX7_Form-10.png)


In the screenshot below, **Year** and **Month** are added to show how you can view fault registrations during a selected period.

- The fault symptoms are now shown as registrations per year/month.

- In the **Probability %** column, if you add all percentages for each month, they add up to 100%. Probability is based on **Fault symptom** registrations in this fault control calculation. If you have a large number of lines on an object, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.



![Figure 20-07](/Figures/20-07_ObjectFaultControl_AX7_Form-20.png)


###### NOTE
The combination objects and an object type is used as a basis for the calculations shown in the three screenshots below, which will increase in detail level.
Generally, the buttons in the **Group by date**, **Group by object**, **Group by functional location** action pane groups, as well as the **Fault** button (Fault ID), contain periods or object relations. The **Fault symptom**, **Fault area**, **Fault type**, **Fault cause**, and **Fault remedy** buttons are categorizations used in Enterprise Asset Management fault management to analyze object fault registrations and pinpoint problem areas.


In the screenshot below, **Object** and **Object type** were added to provide more detail regarding fault registrations.

- The six fault symptoms on "Poor fuel economy" are now split up in **Object** / **Object type** / **Fault symptom** combinations.

- In the **Probability %** column, if you add all percentages for the combination of **Object** / **Object type** / **Fault symptom** respectively, they each add up to 100%. Probability is based on **Fault symptom** registrations in this fault control calculation. If you have a large number of lines on an object, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.


![Figure 20-08](/Figures/20-08_ObjectFaultControl_AX7_Form-30.png)


In the screenshot below, **Area** was added to **Symptom**, **Object**, and **Object type** to provide more detail regarding fault registrations.

- We have added further specification to the calculation, in the form of **Fault area**.

- In the **Probability %** column, if you add all percentages for the combination of **Object** / **Object type** / **Fault symptom** on an object, they each add up to 100%. Probability is based on the combination of **Fault symptom** and **Fault area** in this fault control calculation. If you have a large number of lines on an object, but a large percentage stands out on a line, that would be an indication of a fault area to examine more closely to find a way to limit the number of registrations for that fault area.


![Figure 20-09](/Figures/20-09_ObjectFaultControl_AX7_Form-40.png)


In the screenshot below, **Type** has been added, and the most detailed calculation in this example is shown.

- We have added further specification to the calculation, in the form of **Fault type**.

- In the **Probability %** column, if you add all percentages for the combination of **Object** / **Object type** / **Fault symptom** on an object, they each add up to 100%. Probability is based on the combination of **Fault symptom**, **Fault area**, and **Fault type** in this fault control calculation. If you have a large number of lines on an object, but a large percentage stands out on a line, that would be an indication of a fault type to examine more closely to find a way to limit the number of registrations on that fault type.


![Figure 20-10](/Figures/20-10_ObjectFaultControl_AX7_Form-50.png)


---

### Object KPIs

In Enterprise Asset Management, you can calculate various Key Performance Indicators (KPIs) for objects and object types. KPIs are used to get an overview of performance on objects in relation to, for example, uptime, downtime, repair time, and Mean Time Between Failure (MTBF).

1. Click **Enterprise asset management** > **Inquiries** > **Objects** > **Object KPIs**.
2. Click **Calculate**.

3. In the **Calculate object KPIs** drop-down, you select a period for KPIs to be calculated. On the **Records to include** FastTab, you can select objects and object types to be included in the calculation.
4. Click **OK** to start the calculation.

5. On the **Overview** FastTab in the **Object KPIs** form, the results of the calculation are displayed in grid view. Each object is displayed on a separate line.
6. On the **General** FastTab, you see calculations for the object selected on the **Overview** FastTab. The KPI values are categorized regarding **Time**, **Availability**, **Faults**, and **Cost**.

In the table below, you will find a short explanation of the fields in **Object KPIs** (see additional Note descriptions below table).


---


| Field name | Description |
|--------|--------|
|Object                |Object ID.       |
|Total time (Note 1)   |Total time set in the calendar used in the calculation.        |
|Uptime                |Total time minus downtime.        |
|Downtime              |Production stop registrations made on the object in the selected period.        |
|Repair time           |Total number of work hours consumed on repair work orders.     |
|Availability %        |Uptime divided by total time and multiplied by 100. |
|Number of faults      |Number of fault causes registered on fault symptoms on the object in the selected period.   |
|MTBF (Note 2)         |Mean Time Between Failure.      |
|Fail rate             |1 divided by MTBF.       |
|MRT (Note 3)          |Mean Repair Time.     |
|Number of stops       |Number of production stops registered on the object.    |
|MTBS (Note 4)         |Mean Time Between Stops.   |
|MTPS (Note 5)         |Mean Time Production Stops.      |
|Preventive cost  |Costs posted on the object related to cost type "Preventive" in the selected period. Cost types are set up on work order types.     |
|Corrective cost  |Costs posted on the object related to cost type "Corrective" in the selected period. Cost types are set up on work order types.     |
|Replacement value     |Value defined on the object as the replacement cost.  |
|Object type           |Identification of the object type selected on the object. |
|Product               |Identification of the product selected on the object.   |
|Model                 |Identification of the product model selected on the object.  |
|From date |Start date of the KPI calculation. If the object was created after the start date selected for the calculation, the start date of the object is shown in this field.  |
|To date   |End date of the KPI calculation. If the object was registered as inactive before the end date selected for the calculation, the date from which the object was no longer active is shown in this field.    |
|Time scale            |During calculation of the KPIs, you select a time scale to be used: Hours, Days, or Weeks.    |
|Availability          |Uptime divided by total time.  |
|Work orders           |Total number of work orders included in the KPI calculation.  |
|Work order time       |Total number of work hours consumed on the work orders.   |
|Primary work orders   |Number of primary work orders included in the KPI calculation.  |
|Secondary work orders |Number of secondary work orders included in the KPI calculation.   |
|Maintenance work orders |Number of maintenance work orders included in the KPI calculation. A maintenance work order is a work order with no related fault causes.     |
|Maintenance time      |Total number of work hours consumed on maintenance work orders.    |
|Repair work orders |Number of repair work orders included in the KPI calculation. A repair work order is a work order with a related fault causes.    |
|Reliability % (Note 6)   |Calculation based on the expected exponential development in fault registrations on an object.     |
|Total cost            |Total costs posted on the object in the selected period.      |
|Investment cost  |Costs posted on the object related to cost type "Investment" in the selected period. Cost types are set up on work order types.     |

Note 1: If the object is related to a resource, the related resource calendar is used. If the object is not related to a resource, the calendar selected in the **Standard calendar** field in **Enterprise asset management parameters** is used.

Note 2: Total time divided by number of faults registered on the object in the selected period. If number of faults is zero, MTBF is set to total time.

Note 3: Repair time divided by number of faults registered on the object in the selected period. If number of faults is zero, MRT is set to repair time.

Note 4: Total time divided by number of production stop registrations. If number of production stop registrations is zero in the selected period, the MTBS value is set to total time.

Note 5: Production stop time divided by number of production stop registrations. If number of production stop registrations is zero in the selected period, the MTPS value is set to zero.

Note 6: This means that, over time, the object becomes less reliable due to wear and tear. The calculation of this KPI is based on MTBF and total time.


---

![Figure 20-11](/Figures/20-11_ObjectKPIs_Form_AX7-01.png)


###### NOTE
You can multi-select several objects in **All objects** and click the **Object KPIs** button on the **General** tab. Then, click **Calculate** in **Object KPIs** to calculate KPIs for the selected objects.
Results from a KPI calculation may or may not include production stop registrations, depending on the setup and use of production stop types. Read more about production stops in the [Production Stop](08_Work_Orders.md#production-stop) section.


---

### Items Where Used

You can make a calculation for a specific item to get an overview of where in Enterprise Asset Management the item has been used. The results show the context in which the item has been used during its lifetime. The Item where used form can be opened from the main Enterprise asset management menu, and it can also be accessed from the following grid views and detail views:

- Object BOM

- Spare parts

- Object type setup

- Job type setup forecast

- Work order forecast

- Work order purchase requisition

- Work order purchase

---

#### Make an Item Where Used Calculation

1. Click **Enterprise asset management** > **Inquiries** > **Item where used**, or select the **Item where used** button in one of the views mentioned above.
2. Click **Item where used** > **Calculate where used**.

3. Select the item for which you want to make the calculation in the **Item number** field.
4. You can use the **Level** field to indicate how detailed you want the item lines to be regarding functional locations. For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all item lines for a functional location will be shown on the top level. Therefore, relation/quantity on a line may be added up from functional locations located at a lower level. If you insert the number "0" in the **Level** field, you will see a detailed result showing all item lines on all the functional location levels to which they are related.

5. In the **Include** section, select the check boxes for the various parts in Enterprise asset management that you want to include in the calculation.
6. Click **OK** to start the calculation.

7. On the **Item where used** tab > the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation. The selected action pane group buttons are highlighted in blue color. Click on a button to activate or deactivate it.
8. If you want to show dimensions related to the item, click **Dimensions display**, and select the dimensions to be shown.


![Figure 20-12](/Figures/20-12_ItemWhereUsed_Form_AX7-01.png)


---

### Maintenance Status

In Enterprise Asset Management, you can make a calculation to see an overview of new, active, and completed requests, work orders, and production stops for a specific period. You can also see the number of completed condition assessments for the same period. You can use these calculations to get an overview of workload regarding incoming and completed requests and work orders.

---

#### Make a Maintenance Status Calculation

1. Click **Enterprise asset management** > **Inquiries** > **Maintenance status**.
2. Click **Maintenance status** > **Status**.

3. Select the period for which you want to make the calculation.
###### NOTE
You can use the **Level** field to indicate how detailed you want the maintenance lines to be regarding functional locations. For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all maintenance lines for a functional location will be shown on the top level, and therefore the status on a line may be added up from functional locations located at a lower level. If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance lines on all the functional location levels to which they are related.
4. Click **OK** to start the calculation.

5. In the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation. The selected action pane group buttons are highlighted in orange color. Click on a button to activate or deactivate it.
6. Remember to click the **Update** button to update the calculation each time you make changes by activating or deactivating **Group by...** buttons, or by making a calculation for a new period.

###### NOTE
The results shown in **Maintenance status** only include requests and work orders that have an actual start and date and time. End date and time may be blank.

---

++Example 1++:

In the figure below, only the **Year** and **Month** fields have been activated. Here you can get a general overview on a monthly basis of workload and throughput related to requests and work orders.


![Figure 20-13](/Figures/20-13_MaintenanceStatus_Form_WithoutFL_AX7-01.png)

---

++Example 2++:

In the figure below, information about functional locations has been added. Now, it is possible to compare workload and throughput across functional locations, which may represent, for example, geographical locations, factories, or different work areas.


![Figure 20-14](/Figures/20-14_MaintenanceStatus_Form_WithFL_AX7-01.png)

