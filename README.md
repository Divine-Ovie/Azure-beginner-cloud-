# Azure Cloud Fundamentals Project

## 1. Account Creation Documentation
An Azure Free Tier account was successfully provisioned and verified. The environment was activated with a $200 USD trial credit to explore foundational cloud services safely within compliance boundaries.

![Azure Free Tier Activation and Initial Credit](336405.jpg)

---

## 2. Azure Portal Navigation
Navigating the Azure Portal is streamlined through several primary user interface components:
* **Global Search Bar:** Located at the very top of the portal, used to instantly locate services, documentation, and specific resources without digging through menus.
* **Favorites Sidebar Menu:** Positioned on the left side of the screen for quick, one-click access to frequently used resource categories like Virtual Machines, Storage Accounts, and Microsoft Entra ID.
* **Breadcrumb Trails:** Visible at the top of active resource blades (e.g., `Home > Resource groups > divine-cloud-rg`), allowing for easy tracking of the current management context and fast backwards navigation.

Below is the deployment confirmation screen for a newly created storage account component, illustrating the default navigation hierarchy and service location layouts:

![Azure Portal Layout and Deployment Verification](336925.jpg)

---

## 3. Resource Group Management
To maintain absolute isolation and project organization, a dedicated logical container was created. All foundational services for this project are deployed strictly within this target boundary.
* **Resource Group Name:** divine-cloud-rg
* **Deployment Region:** South Africa North

![Resource Group Settings and Geographic Location](336450.jpg)

---

## 4. Dashboard Customization
The default Azure home page layout was modified by creating a dedicated, private dashboard. This customized workspace enables at-a-glance monitoring of active infrastructure components without manual navigation.
* **Custom Tiles Added:** Resource groups shortcut grid, Microsoft Entra ID quick tasks menu, an active regional clock, and a global "All resources" monitoring tile.

![Custom Pinned Azure Portal Dashboard](367000.jpg)

---

## 5. Billing and Cost Management
To guarantee that credit consumption does not trigger unexpected out-of-pocket charges on the attached payment card, proactive cost boundaries have been established. 

### Cost Analysis Hub
The Cost Analysis control panel is utilized to track real-time resource spending against the remaining free credit balance:

![Azure Cost Analysis Control Panel](336404.jpg)

### Automated Budget & Threshold Alerts
A strict monthly budget has been deployed with dual automated alerts configured at a **75% consumption threshold**:
1. **Actual Cost Alert (75%):** Triggers an immediate notification the moment real, accumulated resource consumption hits 75% of the allocated budget.
2. **Forecasted Cost Alert (75%):** Triggers an early warning email if Azure's predictive algorithms calculate that current spending trends will cross the 75% mark by the end of the billing cycle.

![75 Percent Budget Threshold Configuration Page](366967.jpg)

---

## 6. Security Considerations & Identity Protection
Identity governance and access security are enforced at the root level of the tenant directory. 

### Multi-Factor Authentication (MFA)
To eliminate the risk of brute-force attacks, credential harvesting, or unauthorized environment modifications, **Security Defaults** have been fully enabled. This protocol automatically mandates multi-factor authentication (MFA) for administrative sign-ins.

![Microsoft Entra ID Security Defaults Enabled](366930.jpg)

---

## 7. Free Tier Limits & Resource Quotas
To ensure compliance with the complimentary terms of service, active deployments are mapped directly against the official Azure Free Services Hub. 

![Azure Portal Free Services Marketplace Hub](366978.jpg)

### Core Eligible Service Matrix

| Service | Type | Free Allowance Boundary |
| :--- | :--- | :--- |
| **Azure B1s Virtual Machines** | 12 Months Free | 750 Hours / month (Linux & Windows compute modules) |
| **Azure Managed Disks (P6)** | 12 Months Free | 2 x 64 GB Solid State Drive (SSD) storage allocations |
| **Azure Blob Storage** | 12 Months Free | 5 GB Locally Redundant Storage (LRS) block storage |
| **Azure App Service** | Always Free | Up to 10 Web, Mobile, or API application instances |
| **Azure Functions** | Always Free | 1,000,000 serverless executions per month |

---

## 8. Completion Checklist & Troubleshooting

### Deployment Self-Assessment Checklist
- [x] Multi-Factor Authentication (MFA) enforced via global Security Defaults.
- [x] Dual budget threshold alert active at 75% for actual and forecasted billing metrics.
- [x] Unified project deployment isolated strictly inside the `divine-cloud-rg` container.
- [x] Active resources restricted exclusively to free-tier eligible stock-keeping units (SKUs).

### Common Troubleshooting Scenarios

#### 1. Issue: Unintended Credit Consumption or Rapid Spending
* **Potential Cause:** Leaving premium-tier disks attached or keeping a virtual machine running continuously while completely idle.
* **Resolution:** Navigate to *Cost Management + Billing* to identify the high-cost resource. Stop or completely delete the asset. Ensure all testing deployments utilize the `Standard_B1s` burstable size and standard LRS data replication.

#### 2. Issue: Regional Quota Capacity Exceeded Errors
* **Potential Cause:** High demand or localized restrictions on specific free-tier resources within the primary deployment region (e.g., South Africa North).
* **Resolution:** Adjust the deployment deployment configuration file or portal selector to spin up the resource in an alternative high-capacity regional hub, such as `East US` or `West Europe`.

### Reference Documentation
* [Official Microsoft Azure Free Account FAQ](https://azure.microsoft.com/free/free-account-faq/)
* [Azure Cost Management Learning Pathway](https://learn.microsoft.com/azure/cost-management-billing/)
