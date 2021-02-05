---
title: AzMicrosoft Defender for Identity user investigation tutorial
description: This article explains how to user Microsoft Defender for Identity security alerts to investigate a suspicious user.
ms.date: 10/26/2020
ms.topic: tutorial
---

# Tutorial: Investigate a user

> [!NOTE]
> The [!INCLUDE [Product long](includes/product-long.md)] features explained on this page are also accessible using the new [portal](https://portal.cloudappsecurity.com).

[!INCLUDE [Product long](includes/product-long.md)] alert evidence and lateral movement paths provide clear indications when users have performed suspicious activities or indications exist that their account has been compromised. In this tutorial you'll use the investigation suggestions to help determine the risk to your organization, decide how to remediate, and determine the best way to prevent similar future attacks.

> [!div class="checklist"]
>
> - Gather information about the user.
> - Investigate activities that the user performed.
> - Investigate resources the user accessed.
> - Investigate lateral movement paths.

## Recommended investigation steps for suspicious users

Check and investigate the user profile for the following details and activities:

1. Who is the [user](entity-profiles.md)?
    1. Is the user a [sensitive user](sensitive-accounts.md) (such as admin, or on a watchlist, etc.)?
    1. What is their role within the organization?
    1. Are they significant in the organizational tree?

1. Suspicious activities to [investigate](investigate-entity.md):
    1. Does the user have other opened alerts in [!INCLUDE [Product short](includes/product-short.md)], or in other security tools such as Microsoft Defender for Endpoint, Azure Security Center and/or Microsoft CAS?
    1. Did the user have failed log ons?
    1. Which resources did the user access?
    1. Did the user access high value resources?
    1. Was the user supposed to access the resources they accessed?
    1. Which computers did the user log in to?
    1. Was the user supposed to log in to those computers?
    1. Is there a [lateral movement path](use-case-lateral-movement-path.md) (LMP) between the user and a sensitive user?

## See Also

- [Investigate a computer](investigate-a-computer.md)
- [Working with security alerts](working-with-suspicious-activities.md)
- [Working with lateral movement paths](use-case-lateral-movement-path.md)
- [Reconnaissance alerts](reconnaissance-alerts.md)
- [Compromised credential alerts](compromised-credentials-alerts.md)
- [Lateral movement alerts](lateral-movement-alerts.md)
- [Domain dominance alerts](domain-dominance-alerts.md)
- [Exfiltration alerts](exfiltration-alerts.md)
- [Check out the [!INCLUDE [Product short](includes/product-short.md)] forum!](https://aka.ms/MDIcommunity)
