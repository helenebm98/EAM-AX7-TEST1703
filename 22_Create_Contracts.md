# Create Contracts

Contracts are used to manage continuous service agreements. Contracts can be set up in different ways to accommodate customer requirements, for example, relating to payment and termination terms, and defining items that may be outside the scope of the contract. When you have created the required setup for working with contracts, as described in the previous chapter, you are ready to create and manage the contracts. First, you set up the customers who should be part of your contracts. Next, you create and start the contracts. Then, you calculate and approve the contract installments. Finally, when the contract period runs out, you terminate the contract.

###### NOTE
If warranty terms and contract terms are set up on an object, covering the same period, the contract terms will take precedence over the warranty terms.


---

### Set Up Customers

Before you can create a contract, you must first set up the customers with whom you will be signing contracts.

1. Click **Contract management** > **Common** > **Customers**.
2. Click **New** to create a new contract customer.

3. Select the customer account. The customer name is automatically inserted when you leave the **Customer account** field.
4. In the **Project contract ID** field, select a project contract for the customer.

5. Select the **One invoice** check box if the same project contract ID should be used for all contracts related to the customer. In that case, the customer will receive one invoice that may cover multiple contracts, and all the projects on contracts are related to the same project contract ID.
6. Save the record.

###### NOTE
The customers used in **Contract management** must also be created in the **Enterprise Asset Management** module, in which you set up the objects related to customer. Refer to the [Customer Information](06_Objects.md#customer-information) section for information on how to create customers in **Enterprise Asset Management**.
If the **One invoice** check box is cleared, the project contract ID selected on the customer is used as a template for a new project contract every time a new contract is created for the customer.


---

### Create a Contract

When you create a contract, it is associated with a project in the **Project management and accounting** module; the same way as an object is connected to a project, which is described in the [Integration to Project Management and Accounting](10_Integration_Proj_Management.md#integration-to-project-management-and-accounting) chapter.


#### Contracts

Click **Contract management** > **Common** > **Contracts** to open the list. It contains a list of contracts and displays some of the information related to the contract.


![Figure 22-01](/Figures/22-01_CMA_Contracts_List_AX7-01.png)


If you want to open a contract for editing and see more detailed information the **Contracts**:

1. Select the contract.
2. Click on the contract ID link in the **Contract** column.

3. Details view for the selected contract opens. Click **Edit** and update the contract.
4. Save the changes.


![Figure 22-02](/Figures/22-02_CMA_Contracts_Form_AX7-01.png)


Here is a brief description of the buttons in **Contracts** grid view and details view:

| Button name | Description |
|--------|--------|
|Edit                  |Edit the selected contract.       |
|New                   |Create a new contract.        |
|Delete                |Delete the selected contract.      |
|Start contract        |Click this button to change the stage of a contract to "Active".       |
|Terminate contract    |Click this button to change the stage of a contract to "Terminated".    |
|Installments          |View a list of contract installments. |
|Fee                   |View fee transactions on the contract.   |
|Work orders           |Open the **All work orders** list to see a list of the work orders related to the selected contract.   |
|Contract stage        |Update contract stage.      |
|Stage log             |Log displaying the stages of the selected contract.     |


---

#### Create a Contract

1. Click **Contract management** > **Common** > **Contracts**.
2. Click **New**.

3. In **Contracts**, fill out contract and customer data.
4. On the **General** FastTab, it is possible to edit data regarding termination and price index.

5. On the **Coverage** FastTab, the coverage lines connected to the contract type has been inserted. If required, you can add, edit, and delete lines on the **Hours**, **Expense**, and **Items** tabs.
6. On the **Chargeable items** FastTab, the chargeable items connected to the contract type has been inserted. If required, you can add more items to the list, and edit or delete existing items.

7. On the **Payment** FastTab, the payment lines connected to the contract type has been inserted. If required, you can add, edit, and delete payment lines on the **Contract payment lines** and **Object payment lines** tabs. For example, you may have deleted an installment to be replaced by a special payment, or a once-only payment has been agreed on a contract that is terminated before the scheduled end date.
8. On the **Objects** FastTab, add the objects that are covered by the contract. Click **Add line** and select an object.

9. Click **Start contract** if you want to update the contract stage to "Active" right away. This can be done later, if preferred.
10. Save the record.

###### NOTE
Whether you are able to edit or add lines in steps 5-8 depends on the contract stage setup.


###### CAUTION
If a date is selected in the Contract / warranty **Date** field on a work order, that is the date from which the warranty or contract is valid for the work order. When you create a work order, the date of creation is automatically inserted in this field. You can change the date in this field to, for example, correspond with the start date in a contract agreement.


![Figure 22-03](/Figures/22-03_WO_form_ContractWarranty_field_AX7-01A.png)


When a contract has been created for an object, contract information is displayed:

- In the **Contract management** module > **Contracts** > **Objects** FastTab, you have a list of the objects included in the contract.

- In the **Enterprise asset management** module > **All objects**. Select the object and click the **Contracts** button to see a list of the contracts related to the object.

- In the **Enterprise asset management** module > **All work orders** > **Line details** FastTab > **Contract** field, a contract ID will be shown if the work order line relates to a contract.

Also, all work orders related to a contract can be viewed from **Contracts** by clicking the **Work orders** button (see screenshots above).


---

### Installments and Invoicing

When you have created a contract, the next step is to calculate and approve installments. Invoices regarding installment fees are sent to the customer on a regular basis as stated in the contract.

#### Calculate Installments

1. Click **Contract managemen**t > **Periodic** > **Calculate installments**.
2. In the **Period** field, select the period to be used for the calculation of contract installments.

3. In the **Interval** field, insert the number of periods to be included in the calculation job. The start of the calculation is the current date.
4. On the **Records to include** FastTab, click **Filter** if you want to select a specific customer or contract for which you want to calculate installments. Click **OK** when you have made your selections.

5. Click **OK** to start the calculation.


![Figure 22-04](/Figures/22-04_CMA_CalculateInstallments_dropdown_AX7-01.png)

---

#### Approve and Reject Installments

When you have calculated installments, next step is to approve them.

1. Click **Contract management** > **Inquiries** > **Installments** if you want to be able to see installments for several contracts, or click **Contract management** > **Common** > **Contracts** > select the contract > click **Installments** to only see installments related to  the selected contract.
2. An installment can have status: "Planned", "Firmed", or "Rejected". When you have approved/firmed installments, they are updated to status "Firmed".

3. Select the installments you want to approve, and click **Firm**.
4. Click **OK** to approve the installments.

5. In the **Status** field, select "All" or "Firmed" to be able to see the approved installments.

###### NOTE
If you want to reject installments, follow the steps above, but click **Reject** in step 3. It is possible to multi-select installment lines to approve or reject more lines at a time.


![Figure 22-05](/Figures/22-05_CMA_ContractInstallments_Form_AX7-01.png)

---

#### View Posted Installments

Approved installments are automatically posted in the fee journal you have selected in **Contract parameters**.

1. Click **Contract management** > **Common** > **Contracts**.
2. Select the contract in the list.

3. Click **Fee**.
4. In the **Invoice status** filter, select "All" or "Chargeable" to see posted fees.

---

#### Contract Invoicing

The procedure for creating invoices for contract installments is the same as is used for service jobs. Refer to the [Invoicing](17_Invoicing.md#invoicing) chapter for more information.


---

### Terminate a Contract

1. Click **Contract management** > **Common** > **Contracts**.
2. Select the contract you want to terminate and click **Terminate contract**.

3. Select the termination date in the **Terminated** field.
4. In the **End date** field, the end date of the contract is calculated based on the termination terms.

5. Select a cause for termination in the **Termination cause** field.
6. Click **OK**. The contract status is updated to "Terminated".


###### NOTE
When you reach the end date of a contract, select the contract in the **Contracts** list, click **Contract stage**, and update the stage to "Finished". The contract is now closed.

