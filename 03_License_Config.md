# License Configuration


In Enterprise Asset Management, you can activate or deactivate functionality for specific features when you set up Enterprise Asset Management for your company. The setup options are located in the **License configuration** form in Dynamics 365 for Finance and Operations (**System administration** > **Setup** > **License configuration** > **Configuration keys** tab > **Enterprise asset management**). You will find a short description of each configuration setup below.

---

### EAM 1xx.x.x.x Keep Update Objects

Previous EAM versions will be shown in the configuration keys list, and they will automatically be selected. After you have completed a data upgrade, remember to clear the **... Keep update objects** check box, in order to remove all deprecated fields and tables.


---


### Fault Hierarchy

In Enterprise Asset Management, you can manage faults detected on objects by describing three levels of error management: Fault symptoms, fault areas, and fault types. If the **Fault hierarchy** check box is selected it means that in the **Fault designer** view (**Enterprise asset management** > **Setup** > **Object** > **Fault** > **Fault designer**), there is a relation between the selected fault symptom, fault areas, and fault types shown in the form.



The relations between fault symptoms, fault areas, and fault types depend on the license configuration setup of the **Enterprise asset management** module. If you select the **Fault hierarchy** check box, it means that when you select a symptom in the **Fault designer**, the fault areas related to that symptom are shown on the **Fault area** FastTab. Likewise, when you select a fault area in the Fault designer, the fault types related to that area are shown on the Fault type FastTab.



If the **Fault hierarchy** check box is cleared in **License configuration**, it means that when you select a fault symptom in **Fault designer**, you will see all the fault areas and fault types that have been added in **Fault designer**. In that case, there is no hierarchical relationship between the selected fault symptom, fault areas, and fault types displayed. Refer to the [Fault Management](08_Work_Orders.md#fault-management) section for more information about fault setup.


---


### Inbound/Outbound

In order to manage depot repair, check the inbound/outbound configuration. Inbound and outbound are used for managing stages on objects, which are received for repair or maintenance jobs. The objects may be sent to your company from other company locations or from your customers. This functionality can be used to keep track of objects received at your company (inbound) as well as repaired objects returned to another company address or an external customer (outbound). Refer to the [Inbound and Outbound Objects](07_Requests.md#inbound-and-outbound-objects) section for more information on how to use this functionality.



If your company makes repair jobs or maintenance jobs on objects received from other locations or customers, Enterprise Asset Management can keep track of inbound objects on the way to your company and outbound (returned) objects.


![Figure 3-01](/Figures/03-01_LicenseConfigForEAM_AX7-01.png)

