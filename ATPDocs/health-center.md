---
title: Monitor Microsoft Defender for Identity System Health and Events
description: Use the health center to check how the Microsoft Defender for Identity service is working and be alerted to potential problems and view system events in the Event viewer.
ms.date: 10/26/2020
ms.topic: how-to
---

# Work with [!INCLUDE [Product long](includes/product-long.md)] health and events

## [!INCLUDE [Product long](includes/product-long.md)] health center

The [!INCLUDE [Product long](includes/product-long.md)] health center lets you know how your [!INCLUDE [Product short](includes/product-short.md)] instance is performing and alerts you when there are problems.

## Working with the [!INCLUDE [Product short](includes/product-short.md)] health center

The [!INCLUDE [Product short](includes/product-short.md)] health center lets you know that there's a problem by raising an alert (a red dot) above the Health Center icon in the navigation bar.

![[!INCLUDE [Product short](includes/product-short.md)] health center red dot toolbar](media/health-bar.png)

### Managing [!INCLUDE [Product short](includes/product-short.md)] health

To check up on the overall health of your [!INCLUDE [Product short](includes/product-short.md)] instance, select **Health** ![[!INCLUDE [Product short](includes/product-short.md)] health center icon](media/red-dot.png)

- All open issues can be managed by setting them to **Close**,  or **Suppress**, by clicking the three dots in the corner of the alert and making your selection.

- **Open**: All new suspicious activities appear in this list.

- **Close**: Is used to track suspicious activities that you identified, researched, and fixed for mitigated.

    > [!NOTE]
    > [!INCLUDE [Product short](includes/product-short.md)] may reopen a closed activity if the same activity is detected again within a short period of time.

- **Suppress**: Suppressing an activity means you want to ignore it for now, and only be alerted again if there's a new instance. If there's a similar alert [!INCLUDE [Product short](includes/product-short.md)] doesn't reopen it. But if the alert stops for seven days, and is then seen again, you're alerted again.

- **Reopen**: You can reopen a closed or suppressed alert so that it appears as **Open** in the timeline again.

- **Delete**: From within the security alert timeline, you also have the option to delete a health issue. If you Delete an alert, it is deleted from the instance and you will NOT be able to restore it. After you click delete, you'll be able to delete all security alerts of the same type.

![[!INCLUDE [Product short](includes/product-short.md)] health center issues image](media/health-issue.png)

## See Also

- [Working with suspicious activities](working-with-suspicious-activities.md)
- [Check out the [!INCLUDE [Product short](includes/product-short.md)] forum!](https://aka.ms/MDIcommunity)
