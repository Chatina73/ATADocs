---
title: Microsoft Defender for Identity weak cipher identity security posture assessment report
description: This article provides an overview of Microsoft Defender for Identity's weak cipher identity security posture assessment report.
ms.date: 10/26/2020
ms.topic: how-to
---

# Security assessment: Weak cipher usage

## What are weak ciphers?

Cryptography relies on ciphers to encrypt our data. For example, RC4 (Rivest Cipher 4 also known as ARC4 or ARCFOUR meaning Alleged RC4) is one. While RC4 is remarkable for its simplicity and speed, multiple vulnerabilities have been discovered since the original release of RC4, rendering it insecure. RC4 is especially vulnerable when the beginning of the output key stream is not discarded, or when non-random or related keys are used.

## How do I use this security assessment to improve my organizational security posture?

1. Review the security assessment for weak cipher usage.
    ![Review weak cipher usage assessment](media/cas-isp-weak-cipher-2.png)
1. Research why the identified clients and servers are using weak ciphers.
1. Remediate the issues and disable use of RC4 and/or other weak ciphers (such as DES/3DES).
1. To learn more about disabling RC4, see the [Microsoft Security Advisory](https://support.microsoft.com/help/2868725/microsoft-security-advisory-update-for-disabling-rc4).

> [!NOTE]
> This assessment is updated in near real time.

## Remediation

Disable clients and servers that you want to stop from using RC4 cipher suites by setting the following registry keys. Once disabled, any server or client that communicates with another client or server that requires use of RC4 can then prevent a connection from occurring. Clients, where this setting is deployed, will be unable to connect to sites that require RC4, and servers that deploy this setting will be unable to service clients that require use RC4.

> [!NOTE]
> Make sure to test the following settings in a controlled environment before enabling them in production.
>
> - [HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Ciphers\RC4 128/128]
    "Enabled"=dword:00000000
> - [HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Ciphers\RC4 40/128]
    "Enabled"=dword:00000000
> - [HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Ciphers\RC4 56/128]
    "Enabled"=dword:00000000

To learn more about downloading and updating the registry edits, see the [Microsoft Security Advisory](/security-updates/SecurityAdvisories/2013/2868725).

## Next steps

- [[!INCLUDE [Product short](includes/product-short.md)] activities filtering in Cloud App Security](activities-filtering-mcas.md)
- [Check out the [!INCLUDE [Product short](includes/product-short.md)] forum!](https://aka.ms/MDIcommunity)
