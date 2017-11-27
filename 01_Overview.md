# Enterprise Asset Management / Asset Service Management Wiki for Microsoft Dynamics® 365 for Finance and Operations, Enterprise Edition





Published by: Dynaway A/S



© 2018 Dynaway A/S



---


# Table of Contents


### [Introduction](#introduction)

[Functional Locations and Objects](#functional-locations-and-objects)

[Objects and Work Orders](#objects-and-work-orders)



### [Security Roles](02_Security_Roles.md#security-roles)

[Enterprise Asset Management](02_Security_Roles.md#enterprise-asset-management)

[Contract Management](02_Security_Roles.md#contract-management)



### [License Configuration](03_License_Config.md#license-configuration)

[EAM 1xx.x.x.x Keep Update Objects](03_License_Config.md#1xx.x.x.x-keep-update-objects)

[Fault Hierarchy](03_License_Config.md#fault-hierarchy)

[Inbound/Outbound](03_License_Config.md#inbound/outbound)


### [Functional Locations](05_Functional_Locations.md#functional-locations)

[Functional Location Stages](05_Functional_Locations.md#functional-location-stages)

[Functional Location Types](05_Functional_Locations.md#functional-location-types)

[Introduction to Functional Locations](05_Functional_Locations.md#introduction-to-functional-locations)

[Create Functional Locations](05_Functional_Locations.md#create-functional-locations)

[Install Objects on Functional Locations](05_Functional_Locations.md#install-objects-onfunctional-locations)


### [Objects](06_Objects.md#objects)

[Object Types](06_Objects.md#object-types)

[Object Specifications](06_Objects.md#object-specifications)

[Condition Assessment](06_Objects.md#condition-assessment)

[Product and Model](06_Objects.md#product-and-model)

[Counters](06_Objects.md#counters)

[Enterprise Asset Management Parameters](06_Objects.md#enterprise-asset-management-parameters)

[Object Stages](06_Objects.md#object-stages)

[Object Priorities](06_Objects.md#object-priorities)

[Object Criticalities](06_Objects.md#object-criticalities)

[Object Documents](06_Objects.md#object-documents)

[Workers and Worker Groups](06_Objects.md#workers-and-worker-groups)

[Customer Information](06_Objects.md#customer-information)

[Introduction to Objects](06_Objects.md#introduction-to-objects)

[Create an Object](06_Objects.md#create-an-object)

[Multi-Level Objects](06_Objects.md#multi-level-objects)

[Move, Replace, and Install Objects](06_Objects.md#move-replace-and-install-objects)

[Create Objects Based on Purchace or Sales Orders](06_Objects.md#create-objects-based-on-purchase-or-sales-orders)

[Object BOM](06_Objects.md#object-bom)

[Object Timeline](06_Objects.md#object-timeline)

[Object View](06_Objects.md#object-view)

[Object Specification Overview](06_Objects.md#object-specification-overview)

[Objects And IoT Devices](06_Objects.md#objects-and-iot-devices)



### [Requests](07_Requests.md#requests)

[Request Stages](07_Requests.md#request-stages)

[Request Types](07_Requests.md#request-types)

[Responsible Workers](07_Requests.md#responsible-workers)

[Introduction to Requests](07_Requests.md#introduction-to-requests)

[Create a Request](07_Requests.md#create-a-request)

[Create Work Order from Request](07_Requests.md#create-work-order-from-request)

[Object Loan](07_Requests.md#object-loan)

[Inbound and Outbound Objects](07_Requests.md#inbound-and-outbound-objects)

[Request Reports](07_Requests.md#request-reports)



### [Work Orders](08_Work_Orders.md#work-orders)

[Job Groups and Job Types, Variants, and Trades](08_Work_Orders.md#job-groups-and-job-types-variants-and-trades)

[Work Orders](08_Work_Orders.md#work-orders)

[Work Orders](08_Work_Orders.md#work-orders)

[Work Orders](08_Work_Orders.md#work-orders)

[Work Orders](08_Work_Orders.md#work-orders)

[Work Orders](08_Work_Orders.md#work-orders)

[Work Orders](08_Work_Orders.md#work-orders)

[Work Orders](08_Work_Orders.md#work-orders)

[Work Orders](08_Work_Orders.md#work-orders)

[Work Orders](08_Work_Orders.md#work-orders)

[Work Orders](08_Work_Orders.md#work-orders)

[Work Orders](08_Work_Orders.md#work-orders)

[Work Orders](08_Work_Orders.md#work-orders)

[Work Orders](08_Work_Orders.md#work-orders)

[Work Orders](08_Work_Orders.md#work-orders)

[Work Orders](08_Work_Orders.md#work-orders)

[Work Orders](08_Work_Orders.md#work-orders)

[Work Orders](08_Work_Orders.md#work-orders)





### [Workspaces]



### [Integration to Project Management and Accounting]



### [Preventive and Reactive Maintenance]



### [Capacity Planning]




---


# Introduction



Enterprise Asset Management (EAM) is an advanced module for managing assets, maintenance jobs, and service jobs in Microsoft Dynamics® 365 for Finance and Operations. Enterprise Asset Management is developed by Dynaway A/S and integrates seamlessly with several modules in Dynamics 365 for Finance and Operations. In Figure 1 you will see a graphic illustration of the interfaces to other modules in Microsoft Dynamics® 365 for Finance and Operations.





![Figure 1-01](/Figures/01-01_PPT_Figure_1_AX7_ASM.png)





For mobile workers, for example, service technicians, we have developed the next version of the Mobile Client. The software is based on HTML5 and provides service workers with quick and easy access to information related to objects and work orders. All registrations are automatically transferred to the company's ERP system, Dynamics 365 for Finance and Operations. The the Mobile Client supports use of Google Maps™ for display of object location.





Enterprise Asset Management allows you to efficiently manage and carry out all tasks related to managing and servicing many types of equipment in your company, for example, machines,production equipment, and vehicles. For Asset Service Management, the main focus is servicing customer equipment. Enterprise Asset Management as well as Asset Service Management supports solutions across numerous industries. Figure 2 shows an overview of the key functionality covered by Asset Service Management.





![Figure 1-02](/Figures/01-02_PPT_Figure_2_AX7_ASM_Rel_1711_Fall.png)



---





### Functional Locations and Objects



Functional locations are used to manage objects on locations, including track object costs on functional locations. Functional locations are structured hierarchically, and locations can have sub locations. The functional location structure is static; locations cannot change place. Objects can be installed on functional locations and, if required, the objects can later be installed on another functional location.





Object costs always follow the location of the object meaning that if you install an object on a new functional location, the object automatically use the financial dimensions related to the functional location. Therefore, object costs are always related to the functional location to which the object was related at any given time. This automatic handling of financial dimensions ensures complete tracking of costs when your company performs project controlling and reporting on functional locations.





How you build your functional location hierarchy is based on your company's requirements for maintaining internal equipment or servicing customer equipment. The two figures below show examples of functional locations - based on geographical locations and customers.







![Figure 1-03](/Figures/01-03_FuncLocHierarchy_Site_AX7.png)







![Figure 1-04](/Figures/01-04_FuncLocHierarchy_Customer_AX7.png)





---





### Objects and Work Orders





The central parts of Enterprise Asset Management are objects and work orders. An object is a machine or machine part that requires continuous maintenance and service. Objects can be created in a hierarchical structure, and they can be related to functional locations. Service jobs can be planned at all levels in the object structure.



Various data such as product information and object specification, and required maintenance sequences are set up on each object. The figure below provides an overview of object data and the object affiliation to job types. Red text are examples to show inheritance and dependencies.





![Figure 1-05](/Figures/01-05_Overview_ObjectData_And_ConnectionToJobType_AX7_ASM.png)





A work order contains a work order type, for example, preventive maintenance, corrective maintenance, or inspection. The work order contains one or more work order lines. Each work order line defines a job to be carried out on an object and a related job type, for example, 10,000 km, 50,000 km, 1-year overhaul, or safety inspection. One work order can relate to several objects as long as the objects relate to the same customer. In the figure below, you will find an overview of the key data in a work order.





![Figure 1-06](/Figures/01-06_WO_HeaderAndLines_v103_ASM.png)





A work order can be related to another work order, and job types can contain succeeding jobs, which create a work order. In general, there are no dependencies between work orders, meaning that they can change work order stage and be scheduled independently. Work orders can be created in various ways relating to corrective, preventive, or reactive maintenance. It is also possible to create work orders manually. In the figure below, you will see a graphic overview of the process flow regarding automatic or manual creation of work orders.







![Figure 1-07](/Figures/01-07_ProcessFlow_CreateWO_AX7.png)





There are several steps to complete when you want to schedule and execute a service job on a work order. In the figure below, an overview of the processing of a work order is displayed.





![Figure 1-08](/Figures/01-08_WO_FlowDiagram_AX7_ASM02.png)





###### NOTE



If you have comments, suggestions for improvements, or other forms of feedback that you want to share with us regarding this Training Material, please send an email to: support@dynaway.com. Generally, when you work in Dynamics 365 for Finance and Operations and the Asset Service Management module, click New to create a new record, click Edit to update an existing record, and click Save to save new or edited data.







