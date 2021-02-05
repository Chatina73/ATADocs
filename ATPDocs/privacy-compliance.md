---
title: Microsoft Defender for Identity personal data policy
description: Provides links to information about how to delete private information and personal data from Microsoft Defender for Identity.
ms.date: 10/26/2020
ms.topic: conceptual
---

# [!INCLUDE [Product long](includes/product-long.md)] data security and privacy

[!INCLUDE [Handle personal data](../includes/gdpr-intro-sentence.md)]

## Search for and identify personal data

In [!INCLUDE [Product short](includes/product-short.md)] you can view identifiable personal data from the [[!INCLUDE [Product long](includes/product-long.md)] portal](workspace-portal.md) using the [search bar](workspace-portal.md#search-bar).

Search for a specific user or computer, and click on the entity to bring you to the user or computer [profile page](entity-profiles.md). The profile provides you with comprehensive details about the entity from Active Directory, including network activity related to that entity and its history.

[!INCLUDE [Product short](includes/product-short.md)] personal data is gathered from Active Directory through the [!INCLUDE [Product short](includes/product-short.md)] sensor and stored in a backend database.

## Update personal data

[!INCLUDE [Product short](includes/product-short.md)]'s personal user data is derived from the user's object in the Active Directory of the organization. Therefore, changes made to the user profile in the organization AD are reflected in [!INCLUDE [Product short](includes/product-short.md)].

## Delete personal data

- After a user is deleted from the organization's Active Directory, [!INCLUDE [Product short](includes/product-short.md)] automatically deletes the user profile and any related network activity within a year. You can also [delete](working-with-suspicious-activities.md#review-suspicious-activities-on-the-attack-time-line) any security alerts that contain personal data.

- **Read-only** permissions on the **Deleted Objects** container are recommended. To learn more about how the **Deleted Objects container permission is used by the [!INCLUDE [Product short](includes/product-short.md)] service, see the Deleted Objects container recommendation in [[!INCLUDE [Product short](includes/product-short.md)] prerequisites](prerequisites.md#before-you-start).

## Export personal data

In [!INCLUDE [Product short](includes/product-short.md)] you have the ability to [export](working-with-suspicious-activities.md#review-suspicious-activities-on-the-attack-time-line) security alert information to Excel. This function also exports the personal data.

## Audit personal data

[!INCLUDE [Product short](includes/product-short.md)] implements the audit of personal data changes, including the deleting and exporting of personal data records. Audit trail retention time is 90 days. Auditing in [!INCLUDE [Product short](includes/product-short.md)] is a back-end feature and not accessible to customers.

## Additional resources

- For information about [!INCLUDE [Product short](includes/product-short.md)] trust and compliance, see the [Service Trust portal](https://servicetrust.microsoft.com/ViewPage/GDPRGetStarted) and the [Microsoft 365 Enterprise GDPR Compliance site](/microsoft-365/compliance/gdpr?view=o365-worldwide&preserve-view=true).

## Security and privacy for [!INCLUDE [Product short](includes/product-short.md)] US Government GCC High customers

For additional information on [!INCLUDE [Product short](includes/product-short.md)] compliance standards and location of customer data for US Government GCC High customers, review the [Enterprise Mobility + Security for US Government service description](/enterprise-mobility-security/solutions/ems-govt-service-description).
