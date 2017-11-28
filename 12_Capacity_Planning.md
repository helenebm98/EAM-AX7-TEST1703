# Capacity Planning

In Enterprise Asset Management, capacity calculations can be made regarding capacity load and item forecasts.


### Calculate Capacity Load

In Enterprise Asset Management, you can calculate capacity load on

- Object calendar lines

- Work orders that have not yet been scheduled

- Scheduled work orders

This is useful if you want to get an overview of expected capacity load for a specific period. Calculation of capacity load can be done on all objects or selected objects. You can also make a calculation on a maintenance stop (**All maintenance stops** or **Active maintenance stops** or **Maintenance stop**), or on a work order pool (**All work order pools** or **Active work order pools**).


1. Click **Enterprise asset management** > **Inquiries** > **Capacity load**, or **Enterprise asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Capacity load** button, or **Enterprise asset management** > **Common** > **Maintenance stops** > **All maintenance stops** / **Active maintenance stops** > select maintenance stop in the list > **Capacity load** button.
2. Click the **Calculate capacity load** button.

3. Select a period for the calculation in the **Start date/time** and **End date/time** fields.
4. Select the **Include object calendar** check box if you want to include object calendar lines in the calculation.

5. Select the **Include work order** check box if you want to include work order lines in the calculation.
6. You can use the **Level** field to indicate how detailed you want the capacity load lines to be regarding functional locations. For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all object calendar lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level. If you insert the number "0" in the **Level** field, you will see a detailed result showing all object calendar lines and all work orders on all the functional location level to which they are related.

7. Click **OK** to start the calculation.
8. In the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation. In the figure below, you will see a calculation example in which three worker order lines and 15 object calendar lines are shown. The selected action pane group buttons are highlighted in orange color. Click on a button to activate or deactivate it.


![Figure 12-01](/Figures/12-01_CapacityLoad_CalculateAllObjects_Form_AX7-01.png)


###### NOTE
If you want to focus only on capacity planning regarding scheduled work orders, refer to the [Calculate Capacity Load on Scheduled Work Orders](13_WO_Scheduling.md#calculate-capacity-load-on-scheduled-work-orders) section.

---


### Calculate Item Forecast

Just as you can make capacity load calculations, which are described in the previous section, you can also make item forecast calculations on

- Object calendar lines

- Work orders that have not yet been scheduled

- Scheduled work orders

This is useful if you want to get an overview of expected item consumption (spare parts as well as other items required for completing work orders) for a specific period. Calculation of item forecast can be done on all objects or selected objects. You can also make a calculation on a maintenance stop (**All maintenance stops** or **Active maintenance stops**), or on a work order pool (**All work order pools** or **Active work order pools**).


1. Click **Enterprise asset management** > **Inquiries** > **Item forecast**, or **Enterprise asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Item forecast** button, or **Enterprise asset management** > **Common** > **Maintenance stops** > **All maintenance stops** / **Active maintenance stops** > select maintenance stop in the list > **Item forecast** button.
2. Click the **Calculate item forecast** button.

3. Select a period for the calculation in the **Start date/time** and **End date/time** fields.
4. Select the **Include object calendar** check box if you want to include object calendar lines in the forecast calculation.

5. Select the **Include work order** check box if you want to include work order lines in the forecast calculation.
6. You can use the **Level** field to indicate how detailed you want the capacity load lines to be regarding functional locations. For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all object calendar lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level. If you insert the number "0" in the **Level** field, you will see a detailed result showing all object calendar lines and all work orders on all the functional location level to which they are related.

7. Click **OK** to start the calculation.
8. In the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation. In the figure below, you will see a calculation example in which 12 worker order lines and five object calendar lines are shown. The selected action pane group buttons are highlighted in orange color. Click on a button to activate or deactivate it.

9. Click the **Dimensions display** button if you want to see one or more dimensions related to the items. Select the relevant check boxes, and click **OK**.


![Figure 12-02](/Figures/12-02_ItemForecast_Form_AX7-01.png)

