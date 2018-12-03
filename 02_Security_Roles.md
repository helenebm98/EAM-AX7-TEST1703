# Security Roles


In Dynamics 365 for Finance and Operations, security roles are used to grant access rights to a user, allowing the user to access certain menu items and perform specific tasks. Security roles relate to Client Access Licenses (CAL) in Dynamics 365 for Finance and Operations. You can read more about this topic in the Microsoft white paper describing security roles and licensing.


---

Below, you will see the roles and related tasks defined for Enterprise Asset Management and Asset Service Management (Contract Management).


### Enterprise Asset Management

| Role | Related tasks | CAL level |
|--------|--------|--------|
|Maintenance Manager  |Maintain base data and perform all maintenance-related tasks. Able to access and work with all menu items in Enterprise Asset Management. |Operations |
|Maintenance Clerk    |Schedule work orders, register consumption, post journals, maintain work orders, create purchase orders. Able to work with all menu items in Enterprise Asset Management except items located in the **Setup** area, which are read only. |Operations |
|Maintenance Data Manager   |Manage data entities. |None |
|Maintenance Requester   |Create and edit requests and related fault registrations. |Team Members |
|Maintenance Worker   |Print work order report, register consumption. |Team Members |



### Contract Management

| Role | Related tasks | CAL level |
|--------|--------|--------|
|Contract Management Manager |Maintain base data and perform all contract-related tasks. Able to access and work with all menu items in Contract management.  |Activity |
|Contract Management Clerk   |Manage contracts, carry out invoicing, update contract payments. Able to access and work with menu items in Contract management except the items located in the **Setup** area, which is read only.  |Activity |

