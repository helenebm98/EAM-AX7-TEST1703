# Maintenance Budgets

Maintenance budgets are used to get an overview of expected costs for preventive maintenance. Budget lines are calculated based on object calendar lines with an expected start date in the budget period.

Maintenance budgets are based on the cost types used in Enterprise Asset Management: Preventive, Corrective, and Investment. Investment budget costs are included for active objects that have a replacement date in the budget period, and a related replacement value. Budget costs for corrective maintenance are included if a past corrective date is included in the budget calculation. In that case, corrective costs from an earlier period will be calculated for the same future period for which you calculate the maintenance budget.


### Create Maintenance Budget

1. Click **Enterprise asset management** > **Inquiries** > **Maintenance budget** > **Budget**.
2. Click **Create budget**.

3. Insert a budget ID in the **Maintenance budget** field and a description in the **Description** field.
4. Insert the start and end period for the budget in the **From date** and **To date** fields.

5. If you want to include corrective budget costs, which are calculated on the basis of actual costs from a previous period, insert the start date from which those costs should be included in the **Corrective from date** field.
6. Depending on the requirements for detail level in the budget, select the relevant check boxes in the five **Group by...** sections.

7. Click **OK**.
8. Click **Budget lines** to open **Maintenance budget lines** and see all the budget lines created for the period.

9. If you want to approve the budget in the **Maintenance budgets** form, select it, and click **Approve** > **OK**. Your name is inserted in the **Approved by** field.


###### NOTE
When you have approved a budget, you cannot recalculate or adjust the related lines in **Maintenance budget lines**. It is possible to remove approval of a maintenance budget by clicking **Approve** > **OK**.
In **Maintenance budgets**, there is a **Copy** function that allows you to copy a budget to make a new budget. This is useful if, for example, you have created a budget for one month and want to copy that budget to other months.


![Figure 19-01](/Figures/19-01_MaintenanceBudgets_Form_AX7-01.png)


###### NOTE
The maintenance budget only calculates budget costs based on object calendar lines. If you want to calculate actual costs for the same period, make that calculation in **Object cost control**. Refer to the [Cost and Date Control](20_ControllingAndReporting.md#cost-and-date-control) section for more information.


---

### Update Maintenance Budget

In **Maintenance budget lines**, you will see all the budget lines created for the budget selected in **Maintenance budgets**, which is described in the previous section. You can recalculate and adjust maintenance budget lines as long as the maintenance budget has not been approved. You can also update budget lines with actual costs when the budget period has passed, and costs have been posted in Enterprise Asset Management.


#### Recalculate Maintenance Budget

You can recalculate a maintenance budget in **Maintenance budget lines**. This means that you delete the existing budget lines and make a new calculation.

1. In **Maintenance budget lines**, click **Recalculate**.

2. Make the changes for the new calculation, and click **OK**. New budget lines are created according to the selections you made for recalculation.


#### Adjust Budget Lines

As an alternative to recalculating the entire maintenance budget, you can adjust selected calendar lines regarding budget costs.

1. In **Maintenance budget lines**, select the lines for which you want to update budget cost.
2. Click **Adjust**.

3. If you want to add an amount to the selected lines, select the **Add cost** check box, insert the value in the **Add value** field, and click **OK**.
4. If you want to multiply the budget cost in the selected budget lines with a factor, select the **Multiply cost** check box, insert the multiply factor in the **Multiply value** field, and click **OK**.
###### NOTE
If you insert "1.2" in the **Multiply value** field, you add 20% to the budget cost on the selected lines. If you insert "0.7" in the **Multiply value** field, you reduce the budget cost on the selected lines with 30%.

5. The selected budget lines are updated according to the selections made in steps 3 or 4.


#### Update Actual Cost

When the dates on the budget lines have passed, and actual costs have been posted in Enterprise Asset Management, you can update actual costs on the maintenance budget.

1. In **Maintenance budget lines**, click **Update cost**, and click **OK**.

2. The **Actual cost** fields on the budget lines are updated if actual costs have been posted. New budget lines may be generated if new object types have been created since you created the budget, and those object types have been used on objects for which work orders have been created, and related costs have been posted. New budget lines will only show actual cost because no budget costs were calculated for those lines.

###### NOTE
If you want to get an overview of actual costs divided into Preventive, Corrective, and Investment costs, you can make a calculation for the same period in **Object cost control**. Refer to the [Cost and Date Control](20_ControllingAndReporting.md#cost-and-date-control) section for more information.


#### Add Budget Lines Manually

In **Maintenance budget lines**, you can manually add a new line by clicking the **New** button and making selections on the budget line. This may be useful if, for example,

- you know that refurbishment on some objects is currently in the planning phase, but related jobs have not yet been created in Enterprise Asset Management, and you want budget costs for those jobs to be included in the maintenance budget.

- new objects or object types have been created since you made the maintenance budget, but maintenance sequences have not yet been set up on those objects or object types, and you want budget costs for those object types to be included in the maintenance budget.


![Figure 19-02](/Figures/19-02_MaintenanceBudgetLines_Form_AX7-01.png)

