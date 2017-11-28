# Consumption

When a maintenance or service job has been completed on a work order, the next step is to make consumption registrations and post the journals. You can make registrations on the following consumption types: Hours, items, expenses, and fees. The different consumption types are registered and posted in the **Journal form**. The journal setup in **Enterprise Asset Management** is used for creating and posting separate journals for hours, items, expenses, and fees in **Project management and accounting**.

### Register Consumption

You may be able to add or delete forecast lines on a work order. The setup of a work order stage, the related project type, and the stage rules related to the project type determine if you are able to add or edit journal lines. Read more about work order stages and related project stages in the [Integration to Project Management and Accounting](10_Integration_Proj_Management.md#integration-to-project-management-and-accounting) chapter.

###### NOTE
It is possible to set up automatic posting of journals on a work order stage. Refer to the [Work Order Stages](08_Work_Orders.md#work-order-stages) section for more information.


1. Click **Enterprise asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.
2. Select the work order and click **Journals**.

3. Click **Copy from forecast** to transfer any forecast lines that may be connected  to the work order. You can select which consumption types you want to transfer.
4. If necessary, you can add more consumption lines on the relevant FastTab by clicking **Add** and filling out data on the line. The **Percent** field is used to indicate a discount on the line. The **Percent** field is not editable. A discount is only shown if the object is included in a customer warranty agreement or a contract agreement.

5. If you add a line on the **Items** FastTab, when you select the item in the **Item number** field, there are three tabs that may contain items: On the **All items** tab, all active items are shown. On the **Spare parts** tab, a list of all approved spare parts from the object type setup is shown. On the **Object BOM** tab, all items related to the object BOM is shown.
###### NOTE
You may find the list of items on the **Spare parts** and **Object BOM** tabs useful if, for example, the work order was created due to a breakdown or another unplanned event. In that case, an item forecast may not be related to the work order.
6. Click **Validate journals** to validate the journal lines before posting.

7. Click **Post journals** to post the journal lines.
8. After you have posted the consumption journals, you can update the work order stage, for example to "Ended", to indicated that the work order has been completed.

###### NOTE
In the **Show** field placed in the upper right corner of the form, select which journal lines you want to see: All, Not posted, or Posted. Posted journals have a check mark in the **Posted** check box.

When item lines are created in the work order journal, product dimensions and tracking dimensions related to the item are automatically transferred to the journal line.


![Figure 15-01](/Figures/15-01_WO_Journals_Form_AX7-01.png)

---

#### Object Consumption Report

When you have posted consumption on work orders, you can print an object consumption report. The report displays hours, hour costs, item costs, and expenses posted on objects.

1. Click **Enterprise asset management** > **Reports** > **Objects** > **Object consumption**.
2. Select the parameters and detail level you want to see by selecting the relevant check boxes in the **Show** section.

3. Select the date interval in the **Dates** section.
4. If required, you can select specific objects to be displayed in the report. On the **Records to include** FastTab, click **Filter**, and add the objects you want to include in the report.

5. Click **OK** to generate the report.


---

#### Work Order Consumption Report

When you have posted consumption on work orders, you can print a work order consumption report. The report displays hours, hour costs, item costs, and expenses posted on work orders.

1. Click **Enterprise asset management** > **Reports** > **Work orders** > **Work order consumption**.
2. Select the parameters you want to include in the report by selecting the the relevant check boxes in the **Show** section.

3. Select the date interval in the **Dates** section.
4. If required, you can select specific work orders to be displayed in the report. On the **Records to include** FastTab, click **Filter**, and add the work orders you want to include in the report.

5. Click **OK** to generate the report.


---

#### Work Order Times Report

When you have completed work on a work order, you can print a work order times report to get an overview of planned start and end dates compared to actual start and end dates. For each work order, details for the related objects, job types, and resources are displayed.

1. Click **Enterprise asset management** > **Reports** > **Work orders** > **Work order times**.
2. Click **OK** to include all work orders.

3. If required, you can select specific work orders to be displayed in the report. On the **Records to include** FastTab, click **Filter**, and add the work orders you want to include in the report.
4. Click **OK** to generate the report.

