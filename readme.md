# Azure Lighthouse Managed Offer (Managed Security)

Azure Lighthouse is a multi-tenant management solution that enables Managed Security Service Providers (MSSPs) and enterprises to manage multiple Azure tenants securely and efficiently. It allows cross-tenant access to subscriptions, resource groups, and services without requiring direct logins to each customer’s environment.

https://github.com/ShviamKloudy/Images/blob/main/KN.PNG

## Key Features of Azure Lighthouse

*1. Centralized Management* – Manage multiple Azure tenants from a single pane of glass.

*2. Granular Access Control* – Uses Azure RBAC to control permissions per tenant.

*3. Scalability* – Ideal for MSPs and enterprises managing multiple clients.

*4. Security & Compliance* – Provides just-in-time access and least privilege access control.

*5. Automation & Monitoring* – Uses Azure Monitor, Log Analytics, and Security Center across tenants.

## Benefits
1.  Manage multiple Azure tenants from a *single interface*.
2.  Enforce *role-based access control (RBAC)* for security.
3.  Improve *efficiency* by automating onboarding using *ARM Templates*.

## Azure Lighthouse Deployment Process to Client Tenant
### Step 1: Log Into the Clients tenant 
Go to Azure Portal and Login as Global Administrator and search for Azure Lighthouse and Click on Deploy to Azure for Azure Lighthouse – Resource Deployment 


####  Filling in all the detail fields using the information below copy and paste for each field

*Msp Offer Name:* 24/7 Next-Gen SOC
 
*Msp Offer Description:* SOC offering as a service by Host Company Name. 24/7 Monitoring and Incident Response.

*Managed By Tenant Id:* d1fd9326-4644-4e1c-8685-279bfbe2f5a0


*When it is done, click in save*

*Click Review + Create*

Once the deployment is complete, the deployment can take around 15 minutes to show in Azure Lighthouse

The following permissions are included in this lighthouse offer.

| principalIdDisplayName  | roleDefinitionId                     | Name                                      | Description                                                          |
| ----------------------- | ------------------------------------ | ----------------------------------------- | -------------------------------------------------------------------- |
| SOC Analyst III         | 51d6186e-6489-4900-b93f-92e23144cca5 | Microsoft Sentinel Playbook Operator      | Can list, view, and manually run playbooks                           |
| SOC Analyst I           | 8d289c81-5878-46d4-8554-54e1e3d8b5cb | Microsoft Sentinel Reader                 | Can view data, incidents, workbooks, and other Sentinel resources    |
| SOC Analyst I           | 73c42c96-874c-492b-b04d-ab87d138a893 | Log Analytics Reader                      | Can view and search monitoring data and settings                     |
| SOC Analyst I           | 3e150937-b8fe-4cfb-8069-0eaf05ecd056 | Microsoft Sentinel Responder              | Can manage incidents (assign, dismiss, etc.)                         |
| SOC Analyst III         | 3e150937-b8fe-4cfb-8069-0eaf05ecd056 | Microsoft Sentinel Responder              | Can manage incidents (assign, dismiss, etc.)                         |
| SOC Analyst III         | ab8e14d6-4a74-4a29-9ba8-549422addade | Microsoft Sentinel Contributor            | Can create/edit workbooks, analytics rules, other Sentinel resources |
| SOC Manager             | 91c1777a-f3dc-4fae-b103-61d183457e46 | Managed Services Registration Delete      | Delete role for managed services registration                        |
| SOC Manager             | 87a39d53-fc1b-424a-814c-f7e04687dc9e | Logic App Contributor                     | Lets you manage logic app, but not access to them        |
| Azure Security Insights | f4c81013-99ee-4d62-a7ee-b3f1f648599a | Microsoft Sentinel Automation Contributor | Allows Sentinel to add playbooks to automation rules                 |


# Deploy to Azure 

Use the below button to deploy this Azure Lighthouse offer to customer's tenant.


[![Deploy Kloudynet Lighthouse](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FKloudynetTechnologies%2FAzure-Lighthouse-Next-GenSOC-Onboarding-main%2Frefs%2Fheads%2Fmain%2FNew_lighthousedeploy_Kloudynet.JSON)

