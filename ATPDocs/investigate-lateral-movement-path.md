---

title: Investigating lateral movement paths with Microsoft Defender for Identity
description: This article describes how to detect and investigate potential lateral movement path attacks with Microsoft Defender for Identity.
ms.date: 10/26/2020
ms.topic: tutorial
---

# Tutorial: Use Lateral Movement Paths (LMPs)

> [!NOTE]
> The [!INCLUDE [Product long](includes/product-long.md)] features explained on this page are also accessible using the new [portal](https://portal.cloudappsecurity.com).

Lateral movement attacks are typically accomplished using a number of different techniques. Some of the most popular methods used by attackers are [credential theft](suspicious-activity-guide.md#) and [Pass the Ticket](suspicious-activity-guide.md) attacks. In both methods, non-sensitive accounts are used by attackers for lateral moves by exploiting non-sensitive machines that share stored log-in credentials in accounts, groups and machines with sensitive accounts.

In this tutorial, you'll learn how to use [!INCLUDE [Product long](includes/product-long.md)] LMPs to [investigate](#investigate) potential lateral movement paths, and along with [!INCLUDE [Product short](includes/product-short.md)] security alerts, gain a better understanding of what happened in your network and how. In addition, you'll learn how to use the [LMP to sensitive account report](#discover-your-at-risk-sensitive-accounts) to discover all of the sensitive accounts with potential lateral movement paths discovered in your network by time period.

> [!div class="checklist"]
>
> - Investigate LMPs
> - Discover your sensitive accounts at risk
> - Access the **Lateral movement paths to sensitive accounts** report

## Investigate

There are multiple ways to use and investigate LMPs. In the [!INCLUDE [Product short](includes/product-short.md)] portal, search by entity and then explore by path or activity.

1. From the portal, search for a user or computer. Notice if a lateral movement badge was added to an entity profile. Badges will only display when an entity is discovered in a potential LMP within the last 48 hours.

    ![lateral icon](media/lateral-movement-icon.png) or ![path icon](media/paths-icon.png).

1. In the user profile page that opens, click the **Lateral movement paths** tab.

    ![[!INCLUDE [Product short](includes/product-short.md)] Lateral Movement Path (LMP) tab](media/lateral-movement-path-tab.png)

1. The graph that is displayed provides a map of the possible paths to the sensitive user during the 48 hour time period. If no activity was detected in the last two days, the graph will not appear. Use the **View a different date** option to display the graph for previous lateral movement path detections for the entity.

    ![LMP view a different date](media/view-different-date.png)

1. Review the graph to see what you can learn about exposure of your sensitive user's credentials. For example, in the path, follow the **Logged into by** gray arrows to see where Nick logged in with their privileged credentials. In this case, Nick's sensitive credentials were saved on the SHAREPOINT-SRV computer. Now, notice which other users logged into which computers that created the most exposure and vulnerability. You can see this by looking at the **Administrator on** black arrows to see who has admin privileges on the resource. In this example, everyone in the group HelpDesk has the ability to access user credentials from that resource.

    ![[!INCLUDE [Product short](includes/product-short.md)] Lateral Movement Path (LMP)](media/lmp.png)

## Discover your at-risk sensitive accounts

To discover all the sensitive accounts in your network that are exposed because of their connection to non-sensitive accounts, groups and machines in lateral movement paths, follow these steps.

1. In the [!INCLUDE [Product short](includes/product-short.md)] portal menu, click the reports icon ![reports icon](media/report-icon.png).

1. Under **Lateral movements paths to sensitive accounts**, if there are no potential lateral movement paths found, the report is grayed out. If there are potential lateral movement paths, the report automatically pre-selects the first date when there is relevant data. The lateral movement path report provides data for up to 60 days.

    ![Screenshot showing report date selection](media/reports.png)

1. Click **Download**.

1. An Excel file is created that provides you with details about your potential lateral movement paths and sensitive account exposure for the dates selected. The **Summary** tab provides graphs that detail the number of sensitive accounts, computers, and averages for at-risk access. The **Details** tab provides a list of the sensitive accounts that you should investigate further.

## Schedule report

The Lateral movement to sensitive account report can also be scheduled using the set scheduled reports feature.

Note that the actual LMPs detailed in the downloadable report may no longer be available because they were detected in the past and may have been changed, modified or fixed since they were detected.

To review historical LMPs, select different available dates in the calendar selection when creating a report.

## Next steps

In this tutorial, you've learned how to use LMPs to investigate suspicious activities. To learn more about entities involved in LMPs, continue to the investigate entities tutorial.

> [!div class="nextstepaction"]
> [Investigate entities](investigate-entity.md)

## See Also

- [Understanding [!INCLUDE [Product short](includes/product-short.md)] Lateral Movement Paths](use-case-lateral-movement-path.md)
- [Configure [!INCLUDE [Product short](includes/product-short.md)] to make remote calls to SAM](install-step8-samr.md)
- [Working with security alerts](working-with-suspicious-activities.md)
- [Check out the [!INCLUDE [Product short](includes/product-short.md)] forum!](https://aka.ms/MDIcommunity)
