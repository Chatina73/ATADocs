---
title: Configure SAM-R to enable lateral movement path detection in Microsoft Defender for Identity
description: Explains how to configure Microsoft Defender for Identity to make remote calls to SAM
ms.date: 10/26/2020
ms.topic: how-to
---

# Configure [!INCLUDE [Product long](includes/product-long.md)] to make remote calls to SAM

[!INCLUDE [Product long](includes/product-long.md)] [lateral movement path](use-case-lateral-movement-path.md) detection relies on queries that identify local admins on specific machines. These queries are performed with the SAM-R protocol, using the [!INCLUDE [Product short](includes/product-short.md)] Service account created during [!INCLUDE [Product short](includes/product-short.md)] installation  [Step 2. Connect to AD](install-step2.md).

## Configure SAM-R required permissions

To ensure Windows clients and servers allow your [!INCLUDE [Product short](includes/product-short.md)] account to perform SAM-R, a modification to **Group Policy** must be made to add the [!INCLUDE [Product short](includes/product-short.md)] service account in addition to the configured accounts listed in the **Network access** policy. Make sure to apply group policies to all computers **except domain controllers**.

> [!Note]
> Before enforcing new policies such as this one, it is critical to make sure that your environment remains secure, and any changes will not impact your application compatibility. Do this by first enabling and then verifying the compatibility of proposed changes in audit mode before making changes to your production environment.

1. Locate the policy:

   - Policy Name: Network access - Restrict clients allowed to make remote calls to SAM
   - Location: Computer configuration, Windows settings, Security settings, Local policies, Security options

    ![Locate the policy](media/samr-policy-location.png)

1. Add the [!INCLUDE [Product short](includes/product-short.md)] service to the list of approved accounts able to perform this action on your modern Windows systems.

    ![Add the service](media/samr-add-service.png)

3. **AATP Service** (the [!INCLUDE [Product short](includes/product-short.md)] service created during installation) now has the privileges needed to perform SAM-R in the environment.

For more on SAM-R and this Group Policy, see [Network access: Restrict clients allowed to make remote calls to SAM](/windows/security/threat-protection/security-policy-settings/network-access-restrict-clients-allowed-to-make-remote-sam-calls).

## See Also

- [Investigating lateral movement path attacks with [!INCLUDE [Product short](includes/product-short.md)]](use-case-lateral-movement-path.md)
- [Check out the [!INCLUDE [Product short](includes/product-short.md)] forum!](https://aka.ms/MDIcommunity)
