---
title: Microsoft Defender for Identity's identity security posture assessments
description: This article provides an overview of Microsoft Defender for Identity's identity security posture assessment reports.
ms.date: 10/26/2020
ms.topic: how-to
---

# Microsoft Defender for Identity's identity security posture assessments

Typically, organizations of all sizes have limited visibility into whether or not their on-premises apps and services could introduce a security vulnerability to their organization. The problem of limited visibility is especially true with regards to use of unsupported or outdated components.

While your company may invest significant time and effort on hardening identities and identity infrastructure (such as Active Directory, Active Directory Connect) as an on-going project, it is easy to remain unaware of common misconfigurations and use of legacy components that represent one of the greatest threat risks to your organization. Microsoft security research reveals that most identity attacks utilize common misconfigurations in Active Directory and continued use of legacy components (such as NTLMv1 protocol) to compromise identities and successfully breach your organization. To combat this effectively, [!INCLUDE [Product long](includes/product-long.md)] now offers proactive identity security posture assessments to detect and suggest improvement actions across your on-premise Active Directory configurations.

## What do Defender for Identity identity security posture assessments provide?

- Detections and contextual data on known exploitable components and misconfigurations, along with relevant paths for remediation.
- [!INCLUDE [Product short](includes/product-short.md)] detects not only suspicious activities, but also actively monitors your on-premise identities and identity infrastructure for weak spots, using the existing [!INCLUDE [Product short](includes/product-short.md)] sensor.
- Accurate assessment reports of your current organization security posture, enabling quick response and effect monitoring in a continuous cycle.

## How do I get started?

### Access

[!INCLUDE [Product short](includes/product-short.md)] security assessments are available using the Microsoft Cloud App Security portal after turning on the [!INCLUDE [Product short](includes/product-short.md)] integration. To learn how to integrate [!INCLUDE [Product short](includes/product-short.md)] into Cloud App Security, see [[!INCLUDE [Product short](includes/product-short.md)] integration](/cloud-app-security/mdi-integration).

### Licensing

Accessing [!INCLUDE [Product short](includes/product-short.md)] security assessment reports in Cloud App Security do not require a Cloud App Security license, only a [!INCLUDE [Product short](includes/product-short.md)] license is required.

## Access Defender for Identity using Cloud App Security

See the [Cloud App Security quick start](/cloud-app-security/getting-started-with-cloud-app-security) to familiarize yourself with the basics of using the Cloud App Security portal.

**Identity security posture assessments**

[!INCLUDE [Product short](includes/product-short.md)] offers the following identity security posture assessments. Each assessment is a downloadable report with instructions for use and tools for building an action plan to remediate or resolve.

**Assessment reports**

- [Domain controllers with Print Spooler service available](cas-isp-print-spooler.md)
- [Dormant entities in sensitive groups](cas-isp-dormant-entities.md)
- [Entities exposing credentials in clear text](cas-isp-clear-text.md)
- [Microsoft LAPS usage](cas-isp-laps.md)
- [Legacy protocols usage](cas-isp-legacy-protocols.md)
- [Riskiest lateral movement paths (LMP)](cas-isp-riskiest-lmp.md)
- [Unmonitored domain controllers](cas-isp-unmonitored-domain-controller.md)
- [Unsecure account attributes](cas-isp-unsecure-account-attributes.md)
- [Unsecure Kerberos delegation](cas-isp-unconstrained-kerberos.md)
- [Unsecure SID History attributes](cas-isp-unsecure-sid-history-attribute.md)
- [Weak cipher usage](cas-isp-weak-cipher.md)

To access identity security posture assessments:

1. Open the **Microsoft Cloud App Security** portal.
    ![Access [!INCLUDE [Product short.](includes/product-short.md)] identity security posture reports in Cloud App Security](media/cas-isp-report-1.png)
1. Select **Investigate** from the left menu, then click **Identity security posture** from the drop-down menu.
1. Click the identity security posture assessment you wish to review from the **Security assessment reports** list that opens.

## Next steps

- [Learn more about using Cloud App Security with [!INCLUDE [Product short](includes/product-short.md)]](activities-filtering-mcas.md)
- [Check out the [!INCLUDE [Product short](includes/product-short.md)] forum!](<https://aka.ms/MDIcommunity>)
