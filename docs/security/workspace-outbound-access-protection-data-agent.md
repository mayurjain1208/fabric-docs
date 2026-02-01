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

# Limit outbound requests with outbound access protection

Outbound access protection protects data by limiting Data Agent's outbound requests to data sources outside a workspace. 

## What is outbound access protection?

Outbound access protection helps ensure that data is shared securely within your network security perimeter. For example, data exfiltration protection solutions use outbound access protection controls to limit a malicious actor's ability to move large amounts of data to an untrusted external location. Outbound protections only limit requests that originate in the workspace and communicate with different workspace or location. 

To learn more about managing outbound access protection, see [Workspace outbound access protection](https://learn.microsoft.com/en-us/fabric/security/workspace-outbound-access-protection-overview).

## When does Data Agent make outbound requests?  
  
An outbound request is defined as any request made from within the workspace towards a location outside the workspace. Only the directionality of the call matters - both reads and writes to external locations can exfiltrate sensitive information to untrusted locations. Data Agent makes an outbound request when connecting to a data source, as well as querying the data source.

Outbound access protection doesn't restrict access to any target within the same workspace, because all Data Agent calls remain within the boundary of the workspace.


## Allowing requests to Fabric workspaces.

You can permit your Fabric workspace to make outbound requests to a different Fabric workspace by either [creating a data connection rule](../security/workspace-outbound-access-protection-allow-list-connector.md) via connectors for supported data sources. When you allow list the target workspace or have an approved managed private endpoint, outbound requests are permitted from the source workspace to the target workspace even when outbound access is restricted.

## External integrations


## Considerations and Limitations
  
- [Fabric outbound access protection.](../security/security-managed-private-endpoints-create.md)
- [Fabric inbound access protection. ](../security/security-private-links-overview.md)
