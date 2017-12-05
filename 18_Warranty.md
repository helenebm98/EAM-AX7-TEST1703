# Warranty

In Enterprise Asset Management, you can set up warranty terms that can be connected to an object or an object type. Warranty terms are created for a specific period. Warranty can be set up to provide full coverage or partial coverage, and you can set up terms to relate to hours, expenses, and items. Furthermore, you can also define specific items that are not covered by the warranty.


### Warranty Agreement

First step is to set up the vendor or customer warranty agreements used in your company, which is described in this section. Next, you ensure that warranty categories are selected in Enterprise asset management parameters, and attach warranty agreements to objects or object types. Those topics are described in the following section. Vendor warranty agreements are only used for information purposes. If vendor warranty is set up on the object, you can see the warranty coverage period on the object.

In the work order consumption journal, it is possible to see the warranty coverage for each journal line. When you post the journal, warranty is handled by creating set-off entries by using the warranty categories selected in **Enterprise asset management parameters**. The warranty categories use the type "Fee".


#### Set up Warranty Categories in Enterprise Asset Management Parameters

Warranty categories are used to define accounts and project setup for registration on objects and object types with warranty agreements.

1. Click **Enterprise asset management** > **Setup** > **Enterprise asset management parameters**.
2. Click the **Work orders** link.

3. In the **Warranty category** section, select the categories to be used when posting hours, expenses, and items on warranty agreements.


---

#### Create Warranty Agreement

A warranty agreement may include several agreement lines covering warranty for work hours, expenses, items, as well as a list of items that may not be included in the warranty.

1. Click **Enterprise asset management** > **Setup** > **Objects** > **Warranty**.
2. Click **New** to create a new product.

3. Insert a warranty ID in the **Warranty** field and a description in the **Name** field.
4. Select warranty type in the **Customer or vendor** field.

5. In the **Objects** field, you see the number of active objects that use the warranty agreement.
6. On the **Hour warranty**, **Expense warranty**, and **Item warranty** FastTabs, you add the lines to be included in the agreement pertaining to hours, expenses or items. Steps 7-10 explain how to fill out the lines.

7. Click **Add line** to add a new condition to the warranty. A sequential line number is automatically inserted in the **Line** field.
8. Select a period type for the warranty period in the **Period** field.

9. Insert an interval in the **Interval** field. This number defines how many periods the warranty should be valid for.
10. In the **Percent** field, insert the coverage percentage for the warranty line. The percentage indicates how much is covered by your company.

11. If some items should be excluded from the warranty agreement, you can create a list of those items on the **Chargeable items** FastTab. Click **Add line**, and select the item that should not be covered by the warranty in the **Item number** field.


![Figure 18-01](/Figures/18-01_Warranty_Form_ASM_AX7-01.png)


---

### Warranty on Objects and Object Types


#### Set Up Warranty on Object Type

1. Click **Enterprise asset management** > **Setup** > **Object** > **Types**.
2. Select the object type to which you want to attach a warranty agreement.

3. On the **General** FastTab, select the agreement in the **Vendor warranty** or **Customer warranty** field.



#### Set up Warranty on Object

1. Click **Enterprise asset management** > **Common** > **Objects** > **All Objects**.
2. Select the object and click **Edit**.

3. On the **Customer** FastTab, select the warranty agreement in the **Customer warranty** section.
4. Select the start and end dates in the **Warranty start** and **Warranty end** fields.


###### CAUTION
If a date is selected in the Contract / warranty **Date** field on a work order, that is the date from which the warranty or contract is valid for the work order. When you create a work order, the date of creation is automatically inserted in this field. You can change the date in this field to, for example, correspond with the start date in a warranty agreement.


![Figure 18-02](/Figures/18-02_WO_form_ContractWarranty_field_AX7-01A.png)


###### NOTE
If warranty terms and contract terms are set up on an object, covering the same period, the contract terms will take precedence over the warranty terms.
If an object is covered by a vendor warranty, and a work order is created for that object with expected start date in the warranty period, you will see a notification regarding the warranty agreement when you create the work order. It is then possible to cancel the work order, if required.

