---
title: Install Microsoft Defender for Identity sensor quickstart
description: Step four of installing Microsoft Defender for Identity helps you to install the Defender for Identity sensor.
ms.date: 02/17/2021
ms.topic: quickstart
---

# Quickstart: Install the Microsoft Defender for Identity sensor

In this quickstart, you'll install the [!INCLUDE [Product long](includes/product-long.md)] sensor on a domain controller. If you prefer a silent installation, see the [Silent installation](silent-installation.md) article.

## Prerequisites

- An [[!INCLUDE [Product short](includes/product-short.md)] instance](install-step1.md) that's [connected to Active Directory](install-step2.md).
- A downloaded copy of your [[!INCLUDE [Product short](includes/product-short.md)] sensor setup package](install-step3.md) and the access key.
- Make sure Microsoft .NET Framework 4.7 or later is installed on the machine. If Microsoft .NET Framework 4.7 or later isn't installed, the [!INCLUDE [Product short](includes/product-short.md)] sensor setup package installs it, which may require a reboot of the server.
- For sensor installations on Active Directory Federation Services (AD FS) servers, configure the SQL server to allow the *Directory service* account (**Configuration** > **Directory services** > **Username**) *connect*, *log in*, *read*, and *select* permissions to the **AdfsConfiguration** database.

## Install the Npcap driver

-  Download the Npcap version 1.0 installer from <https://nmap.org/npcap/>.

    >[!NOTE]
    >Copies of Npcap don't count towards the five copy, five computer, or five user licensing limitation if they're installed and used solely in conjunction with Defender for Identity. For more information, see [NPCAP licensing](https://github.com/nmap/npcap/blob/master/LICENSE).

- If you haven't yet installed the sensor:
  1. Uninstall WinPcap, if it was installed.
  1. Install Npcap with the following options: **loopback_support=no** and **winpcap_mode=yes**.
     - If using the GUI installer, deselect the **loopback support** and select **WinPcap** mode.

- If you already installed the sensor with WinPcap and need to update to use NPCAP:
  1. Uninstall the sensor.
  1. Uninstall WinPcap.
  1. Install Npcap with the following options: **loopback_support=no** and **winpcap_mode=yes**.
     - If using the GUI installer, deselect the **loopback support** and select **WinPcap** mode.

## Install the sensor

Perform the following steps on the domain controller or AD FS server.

1. Verify the machine has connectivity to the relevant [[!INCLUDE [Product short](includes/product-short.md)] cloud service](configure-proxy.md#enable-access-to-azure-atp-service-urls-in-the-proxy-server) endpoint(s).
1. Extract the installation files from the zip file. Installing directly from the zip file will fail.
1. Run **Azure ATP sensor setup.exe** with elevated privileges (**Run as administrator**) and follow the setup wizard.
1. On the **Welcome** page, select your language and select **Next**.

    ![[!INCLUDE [Product short.](includes/product-short.md)] standalone sensor installation language](media/sensor-install-language.png)

1. The installation wizard automatically checks if the server is a domain controller/ AD FS server or a dedicated server. If it's a domain controller / AD FS server, the [!INCLUDE [Product short](includes/product-short.md)] sensor is installed. If it's a dedicated server, the [!INCLUDE [Product short](includes/product-short.md)] standalone sensor is installed.

    For example, for a [!INCLUDE [Product short](includes/product-short.md)] sensor, the following screen is displayed to let you know that a [!INCLUDE [Product short](includes/product-short.md)] sensor is installed on your dedicated server:

    ![[!INCLUDE [Product short.](includes/product-short.md)] sensor installation](media/sensor-install-deployment-type.png)

    Select **Next**.

    > [!NOTE]
    > A warning is issued if the domain controller / AD FS server or dedicated server does not meet the minimum hardware requirements for the installation. The warning doesn't prevent you from clicking **Next**, and proceeding with the installation. It can still be the right option for the installation of [!INCLUDE [Product short](includes/product-short.md)] in a small lab test environment where less room for data storage is required. For production environments, it is highly recommended to work with [!INCLUDE [Product short](includes/product-short.md)]'s [capacity planning](capacity-planning.md) guide to make sure your domain controllers or dedicated servers meet the necessary requirements.

1. Under **Configure the sensor**, enter the installation path and the access key that you copied from the previous step, based on your environment:

    ![[!INCLUDE [Product short.](includes/product-short.md)] sensor configuration image](media/sensor-install-config.png)

    - Installation path: The location where the [!INCLUDE [Product short](includes/product-short.md)] sensor is installed. By default the path is  %programfiles%\Azure Advanced Threat Protection sensor. Leave the default value.
    - Access key: Retrieved from the [!INCLUDE [Product short](includes/product-short.md)] portal in the previous step.

1. Select **Install**. The following components are installed and configured during the installation of the [!INCLUDE [Product short](includes/product-short.md)] sensor:

    - KB 3047154 (for Windows Server 2012 R2 only)

        > [!IMPORTANT]
        >
        > - Do not install KB 3047154 on a virtualization host (the host that is running the virtualization -  it is fine to run it on a virtual machine). This may cause port mirroring to stop working properly.
        > - If Wireshark is installed on the [!INCLUDE [Product short](includes/product-short.md)] sensor machine, after you run Wireshark you need to restart the [!INCLUDE [Product short](includes/product-short.md)] sensor, because it uses the same drivers.

    - [!INCLUDE [Product short](includes/product-short.md)] sensor service and [!INCLUDE [Product short](includes/product-short.md)] sensor updater service
    - Microsoft Visual C++ 2013 Redistributable

## Post-installation steps for AD FS servers

Use the following steps to configure Defender for Identity once you've completed the installation of the sensor on an AD FS server.

1. In the [!INCLUDE [Product short](includes/product-short.md)] portal, select **Configuration**

1. Under **System**, select **Sensors**.

    ![[!INCLUDE [Product short.](includes/product-short.md)] sensor configuration page](media/sensor-config.png)

1. Select the sensor you installed on the AD FS server.
1. In the popup window, in the **Resolver Domain Controller** field, enter the FQDN of the resolver domain controllers, then select the plus icon **(+)**, and then select **Save**.  

    ![[!INCLUDE [Product short.](includes/product-short.md)] configure AD FS sensor resolver](media/sensor-config-adfs-resolver.png)

    Initializing the sensor may take a couple of minutes, at which time the AD FS sensor service status should change from **stopped** to **running**.

## Next steps

- Learn how to correctly [configure Microsoft Defender for Identity sensor settings](install-step5.md) to start seeing data.

## Join the Community

Have more questions, or an interest in discussing [!INCLUDE [Product short](includes/product-short.md)] and related security with others? Join the [[!INCLUDE [Product short](includes/product-short.md)] Community](<https://aka.ms/MDIcommunity>) today!
