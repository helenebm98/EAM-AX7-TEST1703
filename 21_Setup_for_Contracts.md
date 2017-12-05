# Setup for Contracts

In the **Contract management** module, you can manage customer contracts regarding service agreements on various types of equipment. Contracts can be set up in a number of ways, accommodating special requirements relating to, for example, coverage, payment terms, termination, and identification of items not covered by the contract.

First step is to set up the frame for the contract agreement in terms of parameters, payment, start-up and termination terms, and so on. When the setup tasks have been completed, you are ready to create contracts. It is possible to include many objects in one contract, or you can create several contracts for the same customer, each with special requirements, depending on, for example, equipment complexity, equipment usage, or individual customer relations.


### Contract Parameters

**Contract management** is linked to a main project. Contracts are set up as sub-projects to the main project, which you define in the parameters. The parameters also include setup of categories and a journal to be used for posting installments.

1. Click **Contract management** > **Setup** > **Contract parameters**.
2. In the **Main project** field, select the project to which contracts are related as sub projects.

3. In the **Fee** field, select the journal to be used when you post contract installments.
4. In the **Default category** section, select the categories to be used in offset entries when posting hours and expenses on work orders.
###### NOTE
In relation to contracts, offset entries on work orders are posted as fees.

5. Click the **Number sequences** link to set up a number sequence for contracts.

---

### Coverage

Contract coverage is used to define the costs included in a contract. You can include several coverage lines in a contract, defining different periods and percentages of coverage. You create the coverage terms that should be available for your contracts. Coverage can be set up separately for hours, expenses, and items.

**Example:** The first coverage period is 12 months, including 100% coverage on all hours, items, and expenses. The subsequent coverage period is six months, including 50% coverage on items only.


1. Click **Contract management** > **Setup** > **Contract** > **Coverage**.
2. Click **New** to create a new coverage record.

3. Insert a coverage ID in the **Coverage** field and a description in the **Name** field.
4. Click **Save**.

5. On the **Hour coverage**, **Expense coverage**, and **Item coverage** FastTabs, you add the lines to be included in the coverage terms pertaining to hours, expenses or items. Steps 6-9 explain how to fill out the lines.
6. Click **Add line** to add a new coverage line. A sequential line number is automatically inserted in the **Line** field. If more than one line has been created for a coverage type, the lines will take effect in the order they are presented.

7. Select a period type for the coverage period in the **Period** field.
8. Insert an interval in the **Interval** field. This number defines how many periods the coverage should be valid for.

9. In the **Percent** field, insert the coverage percentage figure.


![Figure 21-01](/Figures/21-01_Contract_Coverage_Form_AX7-01.png)

---

### Chargeable Items

You can create a set of chargeable items, which are used to exclude certain items from contract coverage. If a contract is set up to cover 100% of the type "Items", any chargeable items defined on the contract are disregarded in terms of coverage. This section explains how to create chargeable item groups, which can be set up on a contract.

1. Click **Contract management** > **Setup** > **Contract** > **Chargeable**.
2. Click **New** to create a new group.

3. Insert a group ID in the **Chargeable group** field and a description in the **Name** field.
4. Click **Save**.

5. Click **Add line** to select an item for the group.
6. Select the item in the **Item number** field. The product name is automatically inserted.


![Figure 21-02](/Figures/21-02_Contract_ChargeableGroup_Form_AX7-01.png)

---

### Contract Payment and Index

You set up payment templates for your contracts in **Payment**. You can create as many payment templates as required. Each template can include several lines covering different periods and payment types. Payment lines can be created for the whole contract, but you can also set up specific payment lines for objects, object types, products, and models in a payment template.

You can use the index functionality in **Contract management** to add a price increase to contract. Index records can be created for a specific period, or they can have no expiration date.


#### Create Payment Configuration

1. Click **Contract management** > **Setup** > **Contract** > **Payment**.
2. Click **New** to create a new payment configuration.

3. Insert a payment ID in the **Payment** field and a description in the **Name** field.
4. On the **Contract payment lines** FastTab, click **Add line** to create a new line.

5. Insert a description of the payment line in the **Name** field.
6. Select a payment type in the **Payment type** field. Select "Continuous" for a recurring payment line, for example, continuous installments to be paid as long as the contract is active. Select "Once only" for a special payment that will only be charged one time, for example, a start-up fee on a contract agreement.

7. In the **Period** field, select the period type to be used, and in the next **Period** field, insert a number indicating the invoice interval.
8. In the **Price** and **Currency** fields, insert the installment fee and select a currency.

9. In the **Category** field, select a project category, which defines setup of accounts.
10. In the **Installment date** field, select "Start of period" if you want to send out invoices at the beginning of a period, or "End of period" if invoices should be sent out at the end of the period.

11. If you want to create payment lines for specific objects, object types, products, and models, this is done on the **Object payment lines** FastTab. Click **Add line** to create a new line.
12. Insert a description of the payment line in the **Name** field.

13. Refer to steps 6-10 regarding description of identical fields.
14. You can select **Object type**, **Product**, and **Model** on a payment line. Example 1: If you select an object type and a model, only objects with those selections are charged with this payment line. Example 2: If you make no selections regarding object type, product, and model, it means that every time you add an object to a contract using this payment configuration, a payment line will be added for each object.

15. Save the record.

![Figure 21-03](/Figures/21-03_Contract_Payment_Form_AX7-01.png)

---

#### Create Index

1. Click **Contract management** > **Setup** > **Contract** > **Index**.
2. Click **New** to create a new index.

3. Insert an index ID in the **Index field** and a description in the **Name** field.
4. Click **Add line**.

5. Select a start date for the index in the **Effective** field.
6. In the **Value** field, insert the index value as a number exceeding 100. For example, "103" means that the contract payment will increase by three percent.

7. Save the record.


![Figure 21-04](/Figures/21-04_Contract_Index_Form_AX7-01.png)


---


### Contract Stages

Contract stages define the stages that a contract can go through, for example, created, finished, and terminated. You update contract stages manually on the contract.

The contract stages required for your contracts must be attached to matching project stages in the **Project management and accounting** module in **Project management and accounting** parameters. First, you set up set up project stages in **Project management and accounting**, and then you set up contract stages and stage groups in **Contract management**. As contract stages are very similar to work order stages, you can refer to the [Work Order Stages](08_Work_Orders.md#work-order-stages) section, "Set Up Project Stages and Work Order Stages", steps 1-4 regarding setup of project stages.


#### Set Up Contract Stages

1. Click **Contract management** > **Setup** > **Stage** > **Stages**.
2. Click **New** to create a new work order stage.

3. Insert the stage ID in the **Stage** field and a name for the stage in the **Name** field. In the **Stage groups** field, you can see the number of contract stage groups that uses the contract stage.
4. On the **General** FastTab, in the **Stage** field, select the project stage to be related to the contract stage.

5. In the **Contract** section, select the functions that should be available for the stage by selecting the relevant check boxes.
6. Save the record.

###### NOTE
In **Project management and accounting parameters**, you can set up user-defined project stages if you require special stages for your **Contract management** setup that are not included in the standard project setup.


![Figure 21-05](/Figures/21-05_Contract_Stages_Form_AX7-01.png)


###### NOTE
Contract stages, stage groups, and types are related and used in the same way as work order stages, work order stage groups, and work order types. Refer to the [Work Order Stages](08_Work_Orders.md#work-order-stages) section for a general explanation regarding stage group, type, and stage relations.

---

#### Contract Stage Groups

When you have created the contract stages required for your contracts, stages can be divided into groups. This is done to create the stage group flow that may be used for different types of contracts. As a minimum, one standard contract stage group should be created.

1. Click **Contract management** > **Setup** > **Stage** > **Stage groups**.
2. Click **New** to create a new contract stage.

3. Insert the stage group ID in the **Stage group** field and a name for the stage group in the **Name** field.
4. In the **Start stage** field, select the stage that should be used on a contract when it is started.

5. In the **Terminated stage** field, select the stage that should be used on a contract when it is terminated. In the **Stages** and **Contract types** fields, you can see the number of stages selected in the stage group, and the number of contract types that uses the stage group.
6. Click **Save** to save the group.

7. On the **Stages** FastTab, select the stages that should be included in the group. This is done by clicking on a stage in the **Stages remaining** section and clicking the ![Figure 21-06](/Figures/21-06_Button_Select_StageGroups.png) button.
8. If you want to select all the available stages for a group, click the ![Figure 21-07](/Figures/21-07_Button_SelectAll_StageGroups.png) button. All stages are transferred to the **Stages selected** section.

9. If you want to remove a selected stage from the group, select the stage in the **Stages selected** section and click the ![Figure 21-08](/Figures/21-08_Button_Deselect_StageGroups.png) button.
10. Click **Stage updates** to define which stages can follow a selected stage. This is done by selecting the relevant check boxes in **Setup allowed update stages**.


###### NOTE
In **Setup allowed update stages** mentioned in step 10, you should not select a check box in the started stage (set up in step 4), as starting a contract should be done by selecting the contract in the **Contracts** list (**Contract management** > **Common** > **Contracts**) and clicking the **Start contract** button. Likewise, you should not select any check boxes in the terminated stage as termination of a contract should be done by selecting the contract and clicking the **Terminate contract** button in the **Contracts** list.


![Figure 21-09](/Figures/21-09_Contract_StagesGroups_Form_AX7-01.png)


![Figure 21-10](/Figures/21-10_CMA_UpdateStages_Form_AX7-01.png)


---


### Contract Termination

When you create a contract, you can include terms for contract termination. In Contract management, you can set up fixed periods during which termination cannot be done, termination notices, and termination causes.


#### Set up No Termination Periods

No termination periods are fixed periods during which an active contract cannot be terminated.

1. Click **Contract management** > **Setup** > **Termination** > **No termination period**.
2. Click **New** to create a new period.

3. Insert an ID in the **No termination period** field and a name for the period in the **Name** field.
4. Select a period type in the **Period type** field.

5. In the **Period** field, insert a number indicating how many periods this no termination period should be valid for. Example: If you have selected "Month" as the period type, and you insert "4" in this field, the no termination period is four months from the start date of the contract.
6. Save the record.

---

#### Set up Termination Notices

1. Click **Contract management** > **Setup** > **Termination** > **Termination notice**.
2. Click **New** to create a new period.

3. Insert an ID in the **Termination notice** field and a name for the period in the **Name** field.
4. Select a period type in the **Period type** field.

5. In the **Period** field, insert a number indicating how many periods this no termination period should be valid for.
6. In the **Notice start** field, you select when the notice goes into effect. Select "Date of notice" or "After no termination period".

7. Save the record.

**Example:** You have a 6-month contract with a customer. If the contract has a 3-month termination notice, and the notice start is "After no termination period", the actual termination date of the contract is nine months after the start date of the contract.

---

#### Set up Termination Causes

1. Click **Contract management** > **Setup** > **Termination** > **Termination cause**.
2. Click **New** to create a new period.

3. Insert a cause in the **Termination cause** field and a description in the **Name** field.
4. Save the record.


---


### Contract Types

Contract types are contract templates in which you can define a specific setup regarding stage group, payment, coverage, and termination terms for a contract. When you create a new contract, selecting a contract type is mandatory.


#### Create Contract Types

1. Click **Contract management** > **Setup** > **Contract** > **Contract types**.
2. Click **New** to create a new contract type.

3. Insert an ID in the **Contract type** field and a name for the contract type in the **Name** field.
4. Select a stage group in the **Stage group** field.

5. In the **Payment** field, select a payment template.
6. In the **Coverage** field, select the coverage terms to be used for the contract type.

7. In the **Chargeable group** field, select a chargeable group if some items are not included in the contract coverage.
8. Select a termination notice period in the **Termination notice** field.

9. In the **No termination period** field, select a fixed period during which a contract of this type cannot be terminated.
10. Save the record.


![Figure 21-11](/Figures/21-11_Contract_Type_Form_AX7-01.png)


###### NOTE
It is possible to check consistency in your contract management setup data at any time when you are using the module. Refer to the [Setup Data and Consistency Check](08_Work_Orders.md#setup-data-and-consistency-check) section for more information about consistency check and data validation.

