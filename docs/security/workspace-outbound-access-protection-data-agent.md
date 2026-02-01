---
title: Manage outbound access from Data Agent with outbound access protection
description: Outbound access protection in Fabric protects data by limiting outbound requests. 
ms.reviewer: 
ms.author: mayurjain
ms.topic: concept-article
ms.custom:
ms.date: 02/01/2026
#customer intent: As a data admin, I want to learn how to protect my data by limiting outbound requests. As a data engineer, I want to learn how to work with my data, even when outbound access protection is turned on. 
---

# What is outbound access protection?

Outbound access protection helps ensure that data is shared securely within your network security perimeter. An outbound request is defined as any request made from within the workspace towards a location outside the workspace. 
When outbound access protection is enabled, all outbound connections from the workspace are blocked by default. Workspace admins can then create exceptions to grant access only to approved destinations.

To learn more about managing outbound access protection, see [Workspace outbound access protection](https://learn.microsoft.com/en-us/fabric/security/workspace-outbound-access-protection-overview).

## Outbound access for Data Agent

Data Agent makes an outbound request when adding or querying any data source outside it's own workspace. Outbound access protection protects data by limiting Data Agent's outbound requests to data sources outside the workspace.
Outbound access protection will not restrict access to any target within the same workspace, because all Data Agent calls remain within the boundary of the workspace.

## Configuration

To configure outbound access protection for workspaces with Data Agent, follow the steps to [enable outbound access protection](workspace-outbound-access-protection-set-up.md). 
After enabling outbound access protection, you can [create a data connection rule](../security/workspace-outbound-access-protection-allow-list-connector.md) to allow outbound access to your database sources.


## Considerations and Limitations
- All Other Connector will be blocked
- External integrations
-   
- For other limitations, refer to [Workspace outbound access protection overview - Microsoft Fabric](/fabric/security/workspace-outbound-access-protection-overview#considerations-and-limitations).
