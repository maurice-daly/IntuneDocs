---
# required metadata
title: What's new in Microsoft Intune - Azure | Microsoft Docs
titleSuffix:
description: Find out what's new in the Intune Azure portal
keywords:
author: ErikjeMS  
ms.author: erikje
manager: dougeby
ms.date: 09/23/2019
ms.topic: conceptual
ms.service: microsoft-intune
ms.localizationpriority: high
ms.technology:
ms.assetid: 791ed23f-bd13-4ef0-a3dd-cd2d7332c5cc

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: dougeby
ms.suite: ems
search.appverid: MET150
#ms.tgt_pltfrm:
ms.custom: intune-azure; get-started
ms.collection: M365-identity-device-management
---

# What's new in Microsoft Intune

Learn what’s new each week in Microsoft Intune. You can also find [important notices](#notices), [past releases](whats-new-archive.md), and information about [how Intune service updates are released](https://techcommunity.microsoft.com/t5/Intune-Customer-Success/Microsoft-Intune-Service-Updates/ba-p/358728). 

> [!Note]
> Each [monthly update](https://techcommunity.microsoft.com/t5/Intune-Customer-Success/Microsoft-Intune-Service-Updates/ba-p/358728) may take up to three days to rollout and will be in the following order:
> - Day 1: Asia Pacific (APAC)
> - Day 2: Europe, Middle East, Africa (EMEA)
> - Day 3: North America
> 
> Some features may roll out over several weeks and might not be available to all customers in the first week.
>
> Check the [In development page](in-development.md) for a list of upcoming features in a release.

**RSS feed**: Get notified when this page is updated by copying and pasting the following URL into your feed reader: `https://docs.microsoft.com/api/search/rss?search=%22What%27s+new+in+microsoft+intune%3F+-+Azure%22&locale=en-us`

<!-- Common categories:  
### App management
### Device configuration
### Device enrollment
### Device management
### Device security
### Intune apps
### Monitor and troubleshoot
### Role-based access control

-->  

<!-- ########################## -->

## Week of September 23, 2019

#### iOS User Enrollment in Preview <!-- 4817900 -->
Apple's iOS 13.1 release includes User Enrollment, a new form of lightweight management for iOS devices. It can be used in place of Device Enrollment or Automated Device Enrollment (formerly Device Enrollment Program) for personally-owned devices. Intune's Preview is supporting this feature set by letting you:

- Target User Enrollment to user groups.
- Give end users the ability to select between lighter User Enrollment or stronger Device Enrollment when they enroll their devices.

Starting on 9/24/2019 with the release of iOS 13.1, we're in the process of rolling out these updates to all customers and expect to be completed by the end of next week.
Applies to:

iOS 13.1 and later

<!-- ########################## -->

## Week of September 16, 2019

<!-- vvvvvvvvvvvvvvvvvvvvvv -->
### App management 

#### Managed Google Play private LOB apps <!-- 1464182  -->
Intune now allows IT admins to publish private Android LOB apps to Managed Google Play via an iframe embedded in the Intune console.  Previously, IT admins needed to publish LOB apps directly to Google's Play publishing console, which required several steps and was time consuming. This new feature allows for easy publishing of LOB apps with a minimal set of steps, without needing to leave the Intune console.  Admins will no longer need to manually register as a developer with Google, and will no longer need to pay the Google $25 registration fee.  Any of the Android Enterprise management scenarios that use Managed Google Play can take advantage of this feature (work profile, dedicated, fully managed, and non-enrolled devices). From Intune, select **Client apps** > **Apps** > **Add**. Then, select **Managed Google Play** from the **App type** list. For more information about Managed Google Play apps, see [Add Managed Google Play apps to Android Enterprise devices with Intune](apps-add-android-for-work.md).

#### Windows Company Portal experience <!-- 1473353, 3598357 -->
The Windows Company Portal is being updated. You will be able to use multiple filters on the Apps page within the Windows Company Portal. The Device Details page is also being updated with an improved user experience. We are in the process of rolling out these updates to all customers and expect to be completed by the end of next week.

#### macOS support for web apps <!-- 3174427 -->
Web apps, which allow you to add a shortcut to a URL on the web, can be installed to the Dock using the macOS Company Portal. End users can access the **Install** action from the app details page for a web app in the macOS Company Portal. For more information about the **Web link** app type, see [Add apps to Microsoft Intune](apps-add.md) and [Add web apps to Microsoft Intune](web-app.md).

#### macOS support for VPP apps <!-- 3173501  -->
macOS apps, purchased using Apple Business Manager, are displayed in the console when Apple VPP tokens are synced in Intune. You can assign, revoke and reassign device and user-based licenses for groups using the Intune console. Microsoft Intune helps you manage VPP apps purchased for use at your company by:
- Reporting license information from the app store.
- Tracking how many of the licenses you have used.
- Helping you prevent installation of more copies of the app than you own.

For more information about Intune and VPP, see [Manage volume-purchased apps and books with Microsoft Intune](vpp-apps.md).

#### Managed Google Play iframe support <!-- 2871756  -->
Intune now provides support for adding and managing web links directly in the  Intune console via the Managed Google Play iframe.  This lets IT admins submit a URL and icon graphic, and then deploy those links to devices just like regular Android apps. Any of the Android Enterprise management scenarios that use Managed Google Play can take advantage of this feature (work profile, dedicated, fully managed, and non-enrolled devices). From Intune, select **Client apps** > **Apps** > **Add**. Then, select **Managed Google Play** from the **App type** list. For more information about Managed Google Play apps, see [Add Managed Google Play apps to Android Enterprise devices with Intune](apps-add-android-for-work.md).

#### Silently install Android LOB apps on Zebra devices <!-- 4252734  -->
When installing Android line-of-business (LOB) apps on [Zebra devices](android-zebra-mx-overview.md), rather than being prompted to both download and install the LOB app, you will be able to install the app silently. In Intune, select **Client apps** > **Apps** > **Add**. In the **Add app** pane, select **Line-of-business app**. For more information, see [Add an Android line-of-business app to Microsoft Intune](lob-apps-android.md).

Currently, after the LOB app is downloaded, a **download success** notification will appear on the user's device. The notification can only be dismissed by tapping **Clear All** in the notification shade. This notification issue will be fixed in an upcoming release, and the installation will be completely silent with no visual indicators.

#### Read and write Graph API operations for Intune apps <!-- 5031704  -->
Applications can call the Intune Graph API with both read and write operations using app identity without user credentials. For more information about accessing the Microsoft Graph API for Intune, see [Working with Intune in Microsoft Graph](https://docs.microsoft.com/graph/api/resources/intune-graph-overview?view=graph-rest-1.0).

#### Protected data sharing and encryption for Intune App SDK for iOS <!-- 3586942  -->
The Intune App SDK for iOS will use 256-bit encryption keys when encryption is enabled by App Protection Policies. All apps will need to have a SDK version 8.1.1 to allow protected data sharing.

<!-- vvvvvvvvvvvvvvvvvvvvvv -->
### Device configuration

#### Support for IKEv2 VPN profiles for iOS <!-- 1943438   -->
In this update, you can create VPN profiles for the iOS native VPN client using the IKEv2 protocol. IKEv2 is a new connection type in **Device configuration** > **Profiles** > **Create profile** > **iOS** for platform > **VPN** for profile type > **Connection Type**.

These VPN profiles configure the native VPN client, so no VPN client apps are installed or pushed to managed devices. This feature requires devices be enrolled in Intune (MDM enrollment).

To see the current VPN settings you can configure, go to [Configure VPN settings on iOS devices](vpn-settings-ios.md).

Applies to:
- iOS

#### Device features, device restrictions, and extension profiles for iOS and macOS settings are shown by enrollment type <!-- 4886161   -->

In Intune, you create profiles for iOS and macOS devices (**Device configuration** > **Profiles** > **Create profile** > **iOS** or **macOS** for platform > **Device features**, **Device restrictions**, or **Extensions** for profile type). 

In this update, the available settings in the Intune portal are categorized by the enrollment type they apply to:

- iOS
  - User enrollment
  - Device enrollment
  - Automated device enrollment (supervised)
  - All enrollment types

- macOS
  - User approved
  - Device enrollment
  - Automated device enrollment
  - All enrollment types

Applies to:
- iOS

#### New voice control settings for supervised iOS devices running in kiosk mode <!-- 4892835   -->
In Intune, you can create policies to run supervised iOS devices as a kiosk, or dedicated device (**Device configuration** > **Profiles** > **Create profile** > **iOS** for platform > **Device restrictions** for profile type > **Kiosk**). 

In this update, there are new settings you can control:
- **Voice control**: Enables Voice Control on the device while in kiosk mode.
- **Modification of voice control**: Allow users to change the Voice Control setting on the device while in kiosk mode.

To see the current settings, go to [iOS Kiosk settings](device-restrictions-ios.md#kiosk).

Applies to:
- iOS 13.0 and later

#### Use single sign-on for apps and websites on your iOS and macOS devices <!-- 4893175   -->
In this update, there are some new single sign-on settings for iOS and macOS devices (**Device configuration** > **Profiles** > **Create profile** > **iOS** or **macOS** for platform > **Device features** for profile type).

Use these settings to configure a single sign-on experience, especially for apps and websites that use Kerberos authentication. You can choose between a generic credential single sign-on app extension, and Apple's built-in Kerberos extension.

To see the current device features you can configure, go to [iOS device features](ios-device-features-settings.md) and [macOS device features](macos-device-features-settings.md).

Applies to:
- iOS 13.0 and newer
- macOS 10.15 and newer

#### Associate domains to apps on macOS 10.15+ devices <!-- 4898079   -->
On macOS devices, you can configure different features, and push these features to your devices using a policy (**Device configuration** > **Profiles** > **Create profile** > **macOS** for platform > **Device features** for profile type). In this update, you can associate domains to your apps. This feature helps share credentials with websites related to your app, and can be used with Apple’s single sign-on extension, universal links, and password autofill. 

To see the current features you can configure, go to [macOS device feature settings in Intune](macos-device-features-settings.md).

Applies to:
- macOS 10.15 and newer

#### Use "itunes" and "apps" in the iTunes App store URL when showing or hiding apps on iOS supervised devices <!-- 4928474   --> 
In Intune, you can create policies to show or hide apps on your supervised iOS devices (**Device configuration** > **Profiles** > **Create profile** > **iOS** for platform > **Device restrictions** for profile type > **Show or hide apps**). 

You can enter the iTunes App store URL, such as `https://itunes.apple.com/us/app/work-folders/id950878067?mt=8`. In this update, both `apps` and `itunes` can be used in the URL, such as:
- `https://itunes.apple.com/us/app/work-folders/id950878067?mt=8`
- `https://apps.apple.com/us/app/work-folders/id950878067?mt=8`

For more information on these settings, see [Show or hide apps](device-restrictions-ios.md#show-or-hide-apps).

Applies to:
- iOS

#### Windows 10 compliance policy password type values are clearer and match CSP<!-- 5138985 -->
On Windows 10 devices, you can create a compliance policy that requires specific password features (**Device compliance** > **Policies** > **Create policy** > **Windows 10 and later** for platform > **System Security**). In this update:
- The **Password type** values are clearer, and updated to match the [DeviceLock/AlphanumericDevicePasswordRequired CSP](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-devicelock#devicelock-alphanumericdevicepasswordrequired).
- The **Password expiration (days)** setting is updated to allow values from 1-730 days. 

For more information on Windows 10 compliance settings, see [Windows 10 and later settings to mark devices as compliant or not compliant](compliance-policy-create-windows.md). 

Applies to:
- Windows 10 and later

 #### Updated UI for configuring Microsoft Exchange on-premises access    <!-- 4092920 -->  
We've updated the console where you [configure access Microsoft Exchange on-premises access](conditional-access-exchange-create.md). All of the configurations for Exchange on-premises access are now available on the same pane of the console where you *Enable Exchange on-premises access control*.  

#### Allow or restrict adding app widgets to the home screen on Android Enterprise work profile devices <!-- 1109650  --> 
On Android Enterprise devices, you can configure features in the work profile (**Device configuration** > **Profiles** > **Create profile** > **Android Enterprise** for platform > **Work profile only > Device restrictions** for profile type). In this update, you can allow users to add widgets exposed by work profile apps to the device home screen.

To see the settings you can configure, go to [Android Enterprise device settings to allow or restrict features using Intune](device-restrictions-android-for-work.md).

Applies to:
- Android Enterprise work profile

<!-- vvvvvvvvvvvvvvvvvvvvvv -->
### Device enrollment

#### New tenants will default away from Android device administrator management <!-- 4869790   -->
Android's device administrator capabilities have been superseded by Android Enterprise. Therefore, we recommend using Android Enterprise for new enrollments instead. In a future update, new tenants will need to complete the following prerequisite steps in Android enrollment to use device administrator management: Go to **Intune** > **Device enrollment** > **Android enrollment** > **Personal and corporate-owned devices with device administration privileges** > **Use device administrator to manage devices**.

Existing tenants will experience no change in their environments. 

For more information about Android device administrator in Intune, see [Android device administrator enrollment](https://docs.microsoft.com/intune/android-enroll-device-administrator).

#### List of DEP devices associated with a profile <!-- 5012045 idmiss -->
You can now see a paged list of Apple Automated Device Enrollment Program (DEP) devices that are associated with a profile. You can search the list from any page in the list. To see the list, go to **Intune** > **Device enrollment** > **Apple enrollment** > **Enrollment program tokens** > choose a token > **Profiles** > choose a profile > **Assigned devices** (under **Monitor**). 

<!-- vvvvvvvvvvvvvvvvvvvvvv -->
### Device management

#### More Android Fully Managed support <!-- 3464667, 4631425, 4631440, 5227935, 4062195   -->
We've added the following support for Android Fully Managed devices:

- SCEP certificates for fully managed Android are available for cert authentication on devices managed as Device Owner. SCEP certificates are already supported on Work Profile devices.  With SCEP certificates for Device Owner, you will be able to: <!-- 5227935 -->
    - create SCEP profile under DO section of Android Enterprise
    - link SCEP certificates to DO Wi-Fi profile for authentication
    - link SCEP certificates to DO VPN profiles for authentication
    - link SCEP certificates to DO Email profiles for authentication (via AppConfig)
- System apps are supported on Android Enterprise devices. In Intune, add an Android Enterprise system app by selecting **Client apps** > **Apps** > **Add**. In the **App type** list, select **Android Enterprise system app**. For more information, see [Add Android Enterprise system apps to Microsoft Intune](apps-ae-system.md). <!-- 4062195 -->
- In **Device compliance** > **Android Enterprise** > **Device Owner**, you can create a compliance policy that sets the Google SafetyNet attestation level.   <!-- 4631425 -->
- On Android Enterprise fully managed devices, the mobile threat defense providers is supported. In **Device compliance** > **Android Enterprise** > **Device Owner**, you can choose an acceptable threat level. <!-- 4631440 --> [Android Enterprise settings to mark devices as compliant or not compliant using Intune](compliance-policy-create-android-for-work.md#device-owner) lists the current settings.
- On Android Enterprise fully managed devices, the Microsoft Launcher app can now be configured via app protection policies to allow a standardized end-user experience on the fully managed device. The Microsoft Launcher app can be used to personalize your Android device. Using the app along with a Microsoft account or work/school account, you can access your calendar, documents, and recent activities in your personalized feed. <!-- 5334044 -->

With this update we are happy to announce that Intune  support for Android Enterprise Fully Managed is now generally available. 

Applies to: 
- Android Enterprise fully managed devices

#### Send custom notifications to a single device  <!-- 4928910 -->
You can now select a single device, and then use a remote device action to [send a custom notification to only that device](custom-notifications.md#send-a-custom-notification-to-a-single-device).

#### Wipe and Passcode Reset actions aren't available for iOS devices that are enrolled by using User Enrollment <!-- 4950491 -->
User Enrollment is a new type of Apple device enrollment. When you enroll devices using User Enrollment, the Wipe and Passcode Reset remote actions won't be available for such devices.

#### Intune support for iOS 13 and macOS Catalina devices <!-- 4665317 -->
Intune now supports managing both iOS 13 and macOS Catalina devices. 
For more information see the [Microsoft Intune Support for iOS 13 and iPadOS blog post](https://techcommunity.microsoft.com/t5/Intune-Customer-Success/Microsoft-Intune-Support-for-iOS-13-and-iPadOS/ba-p/861998).

<!-- vvvvvvvvvvvvvvvvvvvvvv -->
### Device security

#### BitLocker support for client-driven recovery password rotation   <!--  3444125 -->
Use Intune Endpoint Protection settings to configure [Client-driven recovery password rotation](endpoint-protection-windows-10.md#windows-encryption) for BitLocker on devices that run Windows version 1909 or later.

This setting initiates a client-driven recovery password refresh after an OS drive recovery (either by using bootmgr or WinRE) and recovery password unlock on a Fixed data drive. This setting refreshes the specific recovery password that was used, and other unused passwords on the volume remain unchanged. For more information see the BitLocker CSP documentation for [ConfigureRecoveryPasswordRotation](https://docs.microsoft.com/windows/client-management/mdm/bitlocker-csp).

#### Tamper Protection for Windows Defender Antivirus  <!-- 4705448        -->
Use Intune to manage *Tamper Protection* for Windows Defender Antivirus. You’ll find the [setting for Tamper Protection](endpoint-protection-windows-10.md#windows-defender-security-center) in the Microsoft Defender Security Center group when you use device configuration profiles for Windows 10 endpoint protection. You can set Tamper Protection to *Enabled* to turn on Tamper Protection restrictions, set *Disabled* to turn them off, or set*Not configured* to leave a devices current configuration in place.  

For more information about Tamper Protection, see [Prevent security settings changes with tamper protection](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/prevent-changes-to-security-settings-with-tamper-protection) in the Windows documentation. 

#### Advanced settings for Windows Defender Firewall are now generally available <!--  5317392       -->  
The [Windows Defender custom firewall rules for endpoint protection](endpoint-protection-configure.md#add-custom-firewall-rules-for-windows-10-devices), which you configure as part of a device configuration profile, are out of public preview and are generally available (GA).  You can use these rules to specify inbound and outbound behavior to applications, network addresses, and ports. These rules were released in July as a public preview. 

<!-- vvvvvvvvvvvvvvvvvvvvvv -->
### Role-based access control

#### Scope tags now support Terms of Use policies <!-- 2358863 idmiss -->
You can now assign [scope tags](scope-tags.md) to Terms of Use policies. To do so, go to **Intune** > **Device enrollment** > **Terms and conditions** > choose an item in the list > **Properties** > **Scope tags** > choose a scope tag.

## Week of September 9, 2019

### App management

#### Updates to Microsoft Intune app <!-- 4997846 -->
The Microsoft Intune app for Android has been updated with the following improvements:
- Updated and improved the layout to include bottom navigation for the most important actions.
- Added an additional page that shows the user's profile.
- Added the display of actionable notifications in the app for the user, such as the need to update their device settings.
- Added the display of custom push notifications, aligning the app with the support recently added in the Company Portal app for iOS and Android. For more information, see [Send custom notifications in Intune](custom-notifications.md).

#### For iOS devices, customize the enrollment process privacy screen of the Company Portal <!-- 4394993 -->
Using Markdown, you can customize the Company Portal's privacy screen that end users see during iOS enrollment. Specifically, you'll be able to customize the list of things that your organization can't see or do on the device. For more information, see [How to configure the Intune Company Portal app](company-portal-app.md#privacy-statement-customization).


## Week of September 2, 2019

### Monitor and troubleshoot

#### Intune user interface update – Tenant Status dashboard  <!-- 5273210  -->
The user interface for the Tenant Status dashboard has been updated to align with Azure user interface styles. For more information, see  [Tenant status](tenant-status.md).


## Week of August 26, 2019

### Configure Microsoft Edge settings using administrative templates for Windows 10 and newer <!-- 5228061 -->

On Windows 10 and newer devices, you can create administrative templates to configure group policy settings in Intune. In this update, you can configure settings that apply to Microsoft Edge version 77 and newer.

To learn more about administrative templates, see [Use Windows 10 templates to configure group policy settings in Intune](administrative-templates-windows.md).

Applies to:

- Windows 10 and newer (Windows RS4+)

## Week of August 12, 2019

### App management

#### Control iOS app uninstall behavior at device unenrollment <!-- 3504144   -->
Admins can manage whether an app is removed or retained on a device when the device is unenrolled at a user or device group level. 

#### Categorize Microsoft Store for Business apps <!-- 3926922 -->
You can categorize Microsoft Store for Business apps. To do so, choose **Intune** > **Client apps** > **Apps** > Select a Microsoft Store for Business app > **App Information** > **Category**. On the drop-down menu, assign a category.

#### Customized notifications for Microsoft Intune app users <!-- 4843354  -->
The Microsoft Intune app for Android now supports the display of custom push notifications, aligning it with the support recently added in the Company Portal apps for iOS and Android. For more information, see [Send custom notifications in Intune](custom-notifications.md).

### Device configuration

#### New features for Android Enterprise dedicated devices in multi-app mode <!-- 3755304 3041943 3041946   -->
In Intune, you can control features and settings in a kiosk-style experience on your Android Enterprise dedicated devices (**Device configuration** > **Profiles** > **Create profile** > **Android Enterprise** for platform > **Device Owner only, Device restrictions** for profile type).

In this update, the following features are being added:

- **Dedicated devices** > **Multi-app**: The **Virtual home button** can be shown by swiping up on the device, or floating on the screen so users can move it.
- **Dedicated devices** > **Multi-app**: **Flashlight access** allows users to use the flashlight. 
- **Dedicated devices** > **Multi-app**: **Media volume control** allows users to control the device's media volume using a slider. 
- **Dedicated devices** > **Multi-app**:  **Enable a screensaver**, upload a custom image, and control when the screensaver is shown.

To see the current settings, go to [Android Enterprise device settings to allow or restrict features using Intune](device-restrictions-android-for-work.md#dedicated-device-settings).

Applies to:  
- Android Enterprise dedicated devices

#### New app and configuration profiles for Android Enterprise fully managed devices <!-- 3574215 3574238 3574235 3574232   -->
Using profiles, you can configure settings that apply VPN, email, and Wi-Fi settings to your Android Enterprise device owner (fully managed) devices. In this update, you can:

- Use [app configuration policies](app-configuration-policies-use-android.md) to deploy Outlook, Gmail, and Nine Work email settings.
- Use device configuration profiles to deploy [trusted root certificate settings](certificates-configure.md).
- Use device configuration profiles to deploy [VPN](vpn-settings-android-enterprise.md) and [Wi-Fi](wi-fi-settings-android-enterprise.md) settings.

> [!IMPORTANT]
> With this feature, users authenticate with their username and password for VPN, Wi-Fi, and e-mail profiles. Currently, certificate-based authentication isn't available. 

Applies to:  
- Android Enterprise device owner (fully managed)

#### Control the apps, files, documents, and folders that open when users sign in to macOS devices <!--3914202   -->
You can enable and configure features on macOS devices (**Device configuration** > **Profiles** > **Create profile** > **macOS** for platform > **Device features** for profile type). 

In this update, there's a new Login Items setting to control which apps, files, documents, and folders open when a user signs in to the enrolled device. 

To see the current settings, go to [macOS device feature settings in Intune](macos-device-features-settings.md).

Applies to:  
- macOS

#### Deadlines replace Engaged restart settings for Windows Update rings   <!-- 4464404        -->
To align with recent [Windows servicing changes](https://docs.microsoft.com/windows/whats-new/whats-new-windows-10-version-1903#servicing), Intune's Windows 10 Update rings now [support settings for deadlines](windows-update-settings.md). *Deadlines* determine when a device installs feature and security updates.  On devices that run Windows 10 1903 or later, *deadlines* supersede configurations for *engaged restart*.  In the future, *deadlines* will supersede *engaged restart* on earlier versions of Windows 10 as well.  

When you don’t’ configure *deadlines*, devices continue to use their *engaged restart* settings, however [Intune will deprecate support for engaged restart settings](whats-new.md#plan-for-change-new-windows-updates-settings-in-intune-) in a future update.  

Plan to use *deadlines* for all your Windows 10 devices. After settings for *deadlines* are in place, you can change your Intune configurations for *engaged restart* to be Not configured. When set to Not configured, Intune stops managing those settings on devices but doesn’t remove the last configurations for the setting from the device. Therefore, the last configurations that were set for *engaged restart* remain active and in use on devices until those settings are modified by a method other than Intune. Later, when the devices version of Windows changes or when Intune support for *deadlines* expands to the devices Windows version, the device will begin to use the new settings, which are already in place.

#### Support for multiple Microsoft Intune Certificate Connectors   <!--   4704642      -->
Intune now supports install and use of multiple [Microsoft Intune Certificate Connectors for PKCS operations](certficates-pfx-configure.md). This change supports load balancing and high availability of the connector. Each connector instance can process certificate requests from Intune.  If one connector is unavailable, other connectors continue to process requests. 

To use multiple connectors, you don’t need to upgrade to the latest version of the connector software.  

#### New settings, and changes to existing settings to restrict features on iOS and macOS devices <!-- 4867699 4867709   -->
You can create profiles to restrict settings on devices running iOS and macOS (**Device configuration** > **Profiles** > **Create profile** > **iOS** or **macOS** for platform type > **Device restrictions**). This update includes the following features:

- On **macOS** > **Device restrictions** > **Cloud and storage**, use the new **Handoff** setting to block users from starting work on one macOS device, and continue working on another macOS or iOS device.

  To see the current settings, go to [macOS device settings to allow or restrict features using Intune](device-restrictions-macos.md).

- On **iOS** > **Device restrictions**, there are a few changes:

  - **Built-in apps** > **Find my iPhone (supervised only)**: New setting that blocks this feature in the Find My app feature. 
  - **Built-in apps** > **Find my Friends (supervised only)**: New setting that blocks this feature in the Find My app feature. ​
  - **Wireless** > **Modification of Wi-Fi state (supervised only)**: New setting that prevents users from turning on or turning off Wi-Fi on the device.
  - **Keyboard and Dictionary** > **QuickPath (supervised only)**: New setting that blocks the QuickPath feature.
  - **Cloud and storage**: **Activity continuation** is renamed to **Handoff**.

  To see the current settings, go to [iOS device settings to allow or restrict features using Intune](device-restrictions-ios.md).

Applies to:  
- macOS 10.15 and newer
- iOS 13 and newer

#### Some unsupervised iOS device restrictions will become supervised-only with the iOS 13.0 release <!-- 4867809   -->
In this update, some settings apply to supervised-only devices with the iOS 13.0 release. If these settings are configured and assigned to unsupervised devices prior to the iOS 13.0 release, the settings are still applied to those unsupervised devices. They also still apply after the devices upgrade to iOS 13.0. These restrictions are removed on unsupervised devices that are backed up and restored. 

These settings include:

- App Store, Doc Viewing, Gaming
  - App store
  - Explicit iTunes, music, podcast, or news content
  - Adding Game Center friends
  - Multiplayer gaming
- Built-in Apps
  - Camera
    - FaceTime
  - Safari
    - Autofill
- Cloud and Storage
  - Backup to iCloud
  - Block iCloud Document sync
  - Block iCloud Keychain sync

To see the current settings, go to [iOS device settings to allow or restrict features using Intune](device-restrictions-ios.md).

Applies to:  
- iOS 13.0 and newer

#### Improved device status for macOS FileVault encryption  <!-- 4944983         -->
We've updated several of the [device status messages](encryption-monitor.md#device-encryption-status) for FileVault encryption on macOS devices.

#### Some Windows Defender Antivirus scan settings in the reporting show a Failed status <!-- 5119229 -->
In Intune, you can create policies to use Windows Defender Antivirus to scan your Windows 10 devices (**Device configuration** > **Profiles** > **Create profile** > **Windows 10 and later** for platform > **Device restrictions** for profile type > **Windows Defender Antivirus**). The **Time to perform a daily quick scan** and **Type of system scan to perform** reporting shows a failed status, when it’s actually a success status. 

In this update, this behavior is fixed. So, the **Time to perform a daily quick scan** and **Type of system scan to perform** settings shows a success status when the scans complete successfully, and show a failed status when the settings fail to apply. 

For more information on the Windows Defender Antivirus settings, see [Windows 10 (and newer) device settings to allow or restrict features using Intune](device-restrictions-windows-10.md#microsoft-defender-antivirus). 

### Device enrollment

#### Default scope tags <!-- 3702875  -->
A new built-in default scope tag is now available. All un-tagged Intune objects that support scope tags are automatically assigned to the default scope tag. The **Default** scope tag is added to all existing role assignments to maintain parity with the admin experience today. If you don't want an admin to see Intune objects with the default scope tag, remove the default scope tag from the role assignment. This feature is similar to the security scopes feature in System Center Configuration Manager. For more information, see [Use RBAC and scope tags to for distributed IT](scope-tags.md).

#### Android enrollment device administrator support <!-- 4869749   -->
The Android device administrator enrollment option has been added to the Android enrollment page (**Intune** > **Device enrollment** > **Android enrollment**). Android device administrator will still be enabled by default for all tenants.  For more information, see [Android device administrator enrollment](android-enroll-device-administrator.md).

#### Skip more screens in Setup Assistant <!--4877451  -->
You can set Device Enrollment Program profiles to skip the following Setup Assistant screens:
- For iOS
    - Appearance
    - Express Language
    - Preferred Language
    - Device to Device Migration
- For macOS
    - Screen Time
    - Touch ID Setup

For more information about Setup Assistant customization, see [Create an Apple enrollment profile for iOS ](device-enrollment-program-enroll-ios.md#create-an-apple-enrollment-profile) and [Create an Apple enrollment profile for macOS ](device-enrollment-program-enroll-macos.md#create-an-apple-enrollment-profile).

#### Add a user column to the Autopilot device CSV upload process <!-- 3823054 -->
You can now add a user column to the CSV upload for Autopilot devices. This lets you bulk assign users at the time you import the CSV. For more information, see [Enroll Windows devices in Intune by using the Windows Autopilot](enrollment-autopilot.md).


### Device management

#### Configure automatic device clean-up time limit down to 30 days <!--4231059  -->
You can set the automatic device clean-up time limit as short as 30 days (instead of previous limit of 90 days) after the last sign-in. To do so, go to **Intune** > **Devices** > **Setup** > **Device Clean Up Rules**.

#### Build number included on Android device Hardware page <!-- 4461910   -->
A new entry on the Hardware page for each Android device includes the device's operating system build number. For more information, see [View device details in Intune](device-inventory.md).


<!-- ########################## -->

## Week of August 5, 2019

### Zebra Technologies is a supported OEM for OEMConfig on Android Enterprise devices  <!-- 4843713 -->

In Intune, you can create device configuration profiles, and apply settings to Android Enterprise devices using OEMConfig (**Device configuration** > **Profiles** > **Create profile** > **Android enterprise** for platform > **OEMConfig** for profile type).

In this update, Zebra Technologies is a supported original equipment manufacturer (OEM) for OEMConfig. For more information on OEMConfig, see [Use and manage Android Enterprise devices with OEMConfig](android-oem-configuration-overview.md).

Applies to:  
- Android enterprise

<!-- ########################## -->

## Week of July 22, 2019 

### App management

#### Customized notifications for users and groups    <!-- 16766574          -->
Send custom push notifications from the Company Portal application to users on iOS and Android devices that you manage with Intune. These mobile push notifications are highly customizable with free text and can be used for any purpose. You can target them to different user groups in your organization. For more information, see [custom notifications](custom-notifications.md).

#### Google's Device Policy Controller app <!-- 3041950  -->
The Managed Home Screen app now provides access to Google's Android Device Policy app. The Managed Home Screen app is a custom launcher used for devices enrolled in Intune as Android Enterprise (AE) dedicated devices using multi-app kiosk mode. You can access the Android Device Policy app, or guide users to the Android Device Policy app, for support and debug purposes. This launching capability is available at the time the device enrolls and locks into Managed Home Screen. No additional installations are needed to use this functionality.

#### Outlook protection settings for iOS and Android devices <!-- 3212619 -->
You can now configure both general app and data protection configuration settings for Outlook for iOS and Android using simple Intune admin controls without device enrollment. The general app config settings provide parity with the settings administrators can enable when managing Outlook for iOS and Android on enrolled devices. For more information about Outlook settings, see [Deploying Outlook for iOS and Android app configuration settings](https://docs.microsoft.com/exchange/clients-and-mobile-in-exchange-online/outlook-for-ios-and-android/outlook-for-ios-and-android-configuration-with-microsoft-intune).

### Device configuration

#### Use "applicability rules" when creating Windows 10 device configuration profiles <!-- 2549910 eeready   idstaged -->

You create Windows 10 device configuration profiles (**Device configuration** > **Profiles** > **Create profile** > **Windows 10** for platform > **Applicability rules**). In this update, you can create an **applicability rule** so the profile only applies to a specific edition or specific version. For example, you create a profile that enables some BitLocker settings. Once you add the profile, use an applicability rule so the profile only applies to devices running Windows 10 Enterprise.

To add an applicability rule, see [Applicability rules](device-profile-create.md#applicability-rules).

Applies to: Windows 10 and later

#### Use tokens to add device-specific information in custom profiles for iOS and macOS devices <!-- 3330008  -->
You can use custom profiles on iOS and macOS devices to configure settings and features not built in to Intune (**Device configuration** > **Profiles** > **Create profile** > **iOS** or **macOS** for platform > **Custom** for profile type). In this update, you can add tokens to your `.mobileconfig` files to add device-specific information. For example, you can add `Serial Number: {{serialnumber}}` to your configuration file to show the serial number of the device.

To create a custom profile, see [iOS custom settings](custom-settings-ios.md) or [macOS custom settings](custom-settings-macos.md).

Applies to:
- iOS
- macOS

#### New configuration designer when creating an OEMConfig profile for Android Enterprise <!-- 3712769   -->
In Intune, you can create a device configuration profile that uses an OEMConfig app (Device Configuration > Profiles > Create profile > Android enterprise for platform > OEMConfig for profile type). When you do this, a JSON editor opens with a template and values for you to change. 

This update includes a Configuration Designer with an improved user experience that shows details embedded in the app, including titles, descriptions, and more. The JSON editor is still available, and shows any changes you make in the Configuration Designer.

To see the current settings, go to [Use and manage Android Enterprise devices with OEMConfig](android-oem-configuration-overview.md).

Applies to: Android Enterprise

#### Updated UI for configuring Windows Hello  <!-- 4089576            -->
We've updated the console where you [configure Intune to use Windows Hello for Business](windows-hello.md). All of the configuration settings are now available on the same pane of the console where you enable support for Windows Hello. 


#### Intune PowerShell SDK <!-- 4924113 --> 
The Intune PowerShell SDK, which provides support for the Intune API through Microsoft Graph, has been updated to version 6.1907.1.0. The SDK now supports the following:
- Works with Azure Automation.
- Supports app-only auth read operations. 
- Supports friendly shortened names as aliases.
- Conforms to PowerShell naming conventions. Specifically, the `PSCredential` parameter (on the `Connect-MSGraph` cmdlet) has been renamed to `Credential`.
- Supports manually specifying the value of the `Content-Type` header when using the `Invoke-MSGraphRequest` cmdlet.

For more information, see [PowerShell SDK for Microsoft Intune Graph API](https://www.powershellgallery.com/packages/Microsoft.Graph.Intune).


### Device enrollment

#### Updates for Enrollment Restrictions  <!-- 2871968 -->
Enrollment Restrictions for new tenants have been updated so that Android Enterprise work profiles are allowed by default. Existing tenants will experience no change. To use Android Enterprise work profiles, you still need to [connect your Intune account to your Managed Google Play account](connect-intune-android-enterprise.md).

#### UI updates for Apple enrollment and enrollment restrictions <!--4089575, 4089579  -->
Both of the following processes use a wizard-style user interface:
- Apple device enrollment. For more information, see [Automatically enroll iOS devices with Apple's Device Enrollment Program](device-enrollment-program-enroll-ios.md).
- Enrollment restriction creation. For more information, see [Set enrollment restrictions](enrollment-restrictions-set.md).

#### Handling pre-configuration of corporate device identifiers for Android Q devices <!-- 4711509  idmiss -->
In Android Q (v10), Google will remove the ability for MDM agents on legacy-managed (device administrator) Android devices to collect device identifier information.  Intune has a feature that enables IT admins to [pre-configure a list of device serial numbers or IMEIs](corporate-identifiers-add.md#identify-corporate-owned-devices-with-imei-or-serial-number) in order to automatically tag these devices as corporate-owned. This feature won't work for Android Q devices that are device admin-managed.  Regardless of whether the serial number or IMEI for the device is uploaded, it will always be considered to be personal during Intune enrollment.  You can manually switch ownership to corporate after enrollment.  This affects new enrollments only, and existing enrolled devices are not affected.  Android devices managed with work profiles are not affected by this change and will continue working as they do today.  Additionally, Android Q devices enrolled as device administrator will no longer be able to report serial number or IMEI in the Intune console as device properties.

#### Icons have changed for Android Enterprise enrollments (work profile, dedicated devices, and fully managed devices) <!-- 4977730 -->
The icons for Android Enterprise enrollment profiles have changed. To see the new icons, go to **Intune** > **Enrollment** > **Android enrollment** > look under **Enrollment profiles**.


#### Windows Diagnostic Data collection change <!-- 4113859 -->
The default value for diagnostic data collection has changed for devices running Windows 10, version 1903 and later. Starting with Windows 10 1903, diagnostic data collection is enabled by default. Windows diagnostic data is vital technical data from Windows devices about the device and how Windows and related software are performing. For more information, see [Configure Windows diagnostic data in your organization](https://docs.microsoft.com/windows/privacy/configure-windows-diagnostic-data-in-your-organization). Autopilot devices are also opted into “Full” telemetry unless otherwise set in the Autopilot profile with [System/AllowTelemetry](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-system#system-allowtelemetry).

### Device management

#### Improve device location<!-- 3855417  -->
You can zoom in to the exact coordinates of a device using the **Locate device** action. For more information about locating lost iOS devices, see [Find lost iOS devices](device-locate.md).


### Device security

#### Advanced settings for Windows Defender Firewall  (public preview)  <!--  1311949     -->  
Use Intune to manage [custom firewall rules as part of a device configuration profile](endpoint-protection-configure.md#add-custom-firewall-rules-for-windows-10-devices) for endpoint protection on Windows 10. Rules can specify inbound and outbound behavior to applications, network addresses, and ports. 

#### Updated UI for managing security baselines   <!-- 4091125     -->
We've updated the [create and edit experience](security-baselines.md#create-the-profile) in the Intune console for our security baselines. Changes include:

A simpler wizard-style format that's been condensed to a single blade. within one blade. This new design does away with blade sprawl that requires IT Pros to drill down into several separate panes.  
You can now create Assignments as part of the create and edit experience, instead of having to return later to assign baselines. 
We've added a summarization of settings you can view prior to creating a new baseline and when editing an existing one. When editing, the summary only shows the list of items set within the one category of properties being edited.



<!-- ########################## -->

## Week of July 15, 2019 

### App management

#### Managed Home Screen and Managed Settings icons <!-- 4918107 -->
The Managed Home Screen app icon and the **Managed Settings** icon have been updated. The Managed Home Screen app is only used by devices enrolled in Intune as Android Enterprise (AE) dedicated devices and running in multi-app kiosk mode. For more information about the Managed Home Screen app, see [Configure the Microsoft Managed Home Screen app for Android Enterprise](app-configuration-managed-home-screen-app.md).

#### Android Device Policy on Android Enterprise dedicated devices <!-- 4918136 -->
You can access the Android Device Policy application from the Managed Home Screen app's debug screen. The Managed Home Screen app is only used by devices enrolled in Intune as Android Enterprise (AE) dedicated devices and running in multi-app kiosk mode. For more information, see [Configure the Microsoft Managed Home Screen app for Android Enterprise](app-configuration-managed-home-screen-app.md).

#### iOS Company Portal updates <!-- 3902931 -->
Your company name on iOS app management prompts will replace the current "i.manage.microsoft.com" text. For instance, users will see their company name instead of "i.manage.microsoft.com" when users attempt to install an iOS app from the Company Portal or when users allow management of the app. This will be rolled out to all customers over the next few days.

### Device configuration

#### Manage FileVault for macOS   <!--  3858502 + 4557986 + 1210104  -->
You can use Intune to [manage FileVault key encryption for macOS devices](encrypt-devices.md). To encrypt devices, you use an endpoint protection device configuration profile.

Our support for FileVault includes encrypting unencrypted devices, escrow of a devices personal recovery key, automatic or manual rotation of personal encryption keys, and key retrieval for your corporate devices. End users can also use the Company Portal website to get the personal recovery key for their encrypted devices. 

We've also expanded the encryption report to include [information about FileVault](encryption-monitor.md) along-side information for BitLocker, so you can view all your device encryption details in one place. 

### Device enrollment

#### Windows Autopilot reset removes the device's primary user <!-- 4156123 -->
When Autopilot reset is used on a device, the device's primary user will be removed. The next user who signs in after the reset will be set as the primary user. This feature will be rolled out to all customers over the next few days.

## Week of July 8, 2019

### New Office, Windows, and OneDrive settings in Windows 10 administrative templates <!-- 3510695 -->

You can create Administrative templates in Intune that mimic on-premises group policy management (**Device management** > **Profiles** > **Create profile** > **Windows 10 and later** for platform > **Administrative template** for profile type).

This update includes more Office, Windows, and OneDrive settings you can add to your templates. With these new settings, you can now configure over 2500 settings that are 100% cloud-based.

To learn more about this feature, see [Use Windows 10 templates to configure group policy settings in Intune](administrative-templates-windows.md).

Applies to: Windows 10 and later

## Week of July 1, 2019 

### App management

#### AAD and APP on Android Enterprise devices <!-- 3574267 -->
When onboarding fully managed Android Enterprise devices, users will now register with Azure Active Directory (AAD) during the initial setup of their new or factory reset device. Previously for a fully managed device, after setup was complete, the user had to manually launch the Microsoft Intune app to start AAD registration. Now when the user lands on the device home page after initial setup, the device is both enrolled and registered.

In addition to the AAD updates, Intune app protection policies (APP) are now supported on fully managed Android Enterprise devices. This functionality will become available as we roll it out. For more information, see [Add Managed Google Play apps to Android Enterprise devices with Intune](apps-add-android-for-work.md).

## Week of June 24, 2019 

### App management

#### Configure which browser is allowed to link to organization data <!-- 3145939 -->
Intune App Protection Policies (APP) on Android and iOS devices now allow you to transfer Org web links to a specific browser beyond the Intune Managed Browser or Microsoft Edge.  For more about APP, see [What are app protection policies?](app-protection-policy.md).

#### All apps page identifies online/offline Microsoft Store for Business apps<!--4089647 -->
The **All apps** page now includes labeling to identify Microsoft Store for Business (MSFB) apps as online or offline apps. Each MSFB app now includes a suffix for **Online** or **Offline**. The app details page also includes **License Type** and **Supports device context installation** (offline licensed  apps only) information.

#### Company Portal app on Windows shared devices <!--4393553 -->
Users can now access the Company Portal app on Windows shared devices. End users will see a **Shared** label on the device tile. This applies to the Windows Company Portal app version 10.3.45609.0 and later.

#### View all installed apps from new Company Portal web page <!-- 4224326 -->
The Company Portal website's new **Installed Apps** page lists all managed apps (both required and available) that are installed on a user's devices. In addition to assignment type, users can see the app's publisher, date published, and current installation status. If you haven't made any apps required or available to your users, they'll see a message explaining that no company apps have been installed. To see the new page on the web, go to the [Company Portal website](https://portal.manage.microsoft.com) and click **Installed Apps**.  

#### New view lets app users see all managed apps installed on device <!-- 2352913 -->  
The Company Portal app for Windows now lists all managed apps (both required and available) that are installed on a user's device. Users can also see attempted and pending app installations, and their current statuses. If you haven't made apps required or available to your users, they'll see a message explaining that no company apps have been installed. To see the new view, go to the Company Portal navigation pane and select **Apps** > **Installed Apps**.    

### Device configuration

#### Configure settings for kernel extensions on macOS devices <!-- 2043024 -->
On macOS devices, you can create a device configuration profile (**Device configuration** > **Profiles** > **Create profile** > choose **macOS** for platform). This update includes a new group of settings that let you configure and use kernel extensions on your devices. You can add specific extensions, or allow all extensions from a specific partner or developer.

To learn more about this feature, see [kernel extensions overview](kernel-extensions-overview-macos.md) and [kernel extension settings](kernel-extensions-settings-macos.md).

Applies to: macOS 10.13.2 and later

#### Apps from the store only setting for Windows 10 devices includes more configuration options <!-- 2697002 -->
When you create a device restrictions profile for Windows devices, you can use the **Apps from the store only** setting so users only install apps from the Windows App Store (**Device configuration** > **Profiles** > **Create profile** > **Windows 10 and later** for platform > **Device restrictions** for profile type). In this update, this setting is expanded to support more options. 

To see the new setting, go to [Windows 10 (and newer) device settings to allow or restrict features](device-restrictions-windows-10.md#app-store).

Applies to: Windows 10 and later

#### Deploy multiple Zebra mobility extensions device profiles to a device, same user group, or same devices group <!-- 4089955 -->
In Intune, you can use Zebra mobility extensions (MX) in a device configuration profile to customize settings for Zebra devices that aren't built into Intune. Currently, you can deploy one profile to a single device. In this update, you can deploy multiple profiles to:
- The same user group
- The same devices group
- A single device

[Use and manage Zebra devices with Zebra Mobility Extensions in Microsoft Intune](android-zebra-mx-overview.md) shows how to use MX in Intune.

Applies to: Android

#### Some kiosk settings on iOS devices are set using "Block", replacing "Allow" <!-- 4404075  -->
When you create a device restrictions profile on iOS devices (**Device configuration** > **Profiles** > **Create profile** > **iOS** for platform > **Device restrictions** for profile type > **Kiosk**), you set the **Auto lock**, **Ringer switch**, **Screen rotation**, **Screen sleep button**, and **Volume buttons**. 

In this update, the values are **Block** (blocks the feature) and **Not configured** (allows the feature). To see the settings, go to [iOS device settings to allow or restrict features](device-restrictions-ios.md#kiosk). 

Applies to: iOS

#### Use Face ID for password authentication on iOS devices <!-- 4490704 -->
When you create a device restrictions profile for iOS devices, you can use a fingerprint for a password. In this update, the fingerprint password settings also allow facial recognition (**Device configuration** > **Profiles** > **Create profile** > **iOS** for platform > **Device restrictions** for profile type > **Password**). As a result, the following settings changed:

- **Fingerprint unlock** is now **Touch ID and Face ID unlock**.
- **Fingerprint modification (supervised only)** is now **Touch ID and Face ID modification (supervised only)**.

Face ID is available in iOS 11.0 and later. To see the settings, go to [iOS device settings to allow or restrict features using Intune](device-restrictions-ios.md#password).

Applies to: iOS

#### Restricting gaming and app store features on iOS devices is now dependent on ratings region <!-- 4593948 -->
On iOS devices, you can allow or restrict features related to gaming, the app store, and viewing documents (**Device configuration** > **Profiles** > **Create profile** > **iOS** for platform > **Device restrictions** for profile type > **App Store, Doc Viewing, Gaming**). You can also choose the Ratings region, such as the United States. 

In this update, the **Apps** feature is moved to be a child to **Ratings region**, and is dependent on **Ratings region**. To see the settings, go to [iOS device settings to allow or restrict features using Intune](device-restrictions-ios.md#app-store-doc-viewing-gaming).

Applies to: iOS

### Device enrollment

#### Windows Autopilot support for Hybrid Azure AD Join <!-- 4809146-->
Windows Autopilot for existing devices now supports Hybrid Azure AD Join (in addition to the existing Azure AD Join support). Applies to Windows 10 version 1809 and above devices. For more information, see [
Windows Autopilot for existing devices](https://docs.microsoft.com/windows/deployment/windows-autopilot/existing-devices).



### Device management

#### See the security patch level for Android devices <!-- 4461911 -->
You can now see the security patch level for Android devices. To do so, choose **Intune** > **Devices** > **All devices** > choose a device > **Hardware**.
 The patch level is listed in the **Operating System** section.

#### Assign scope tags to all managed devices in a security group <!-- 3173810 -->
You can now assign scope tags to a security group and all devices in the security group will also be associated with those scope tags. All devices in these groups will also be assigned the scope tag. The scope tags set with this feature will overwrite the scope tags set with the current device scope tags flow. For more information, see [Use RBAC and scope tags for distributed IT](scope-tags.md).

### Device security

#### Use keyword search with Security Baselines <!--  -->
When you create or edit [Security Baseline profiles](security-baselines.md#create-the-profile), you can specify keywords in the new *Search* bar to filter the available groups of settings to those that contain your search criteria. 

#### The Security Baselines feature is now generally available  <!-- 3785395 -->
The **Security Baselines** feature is out of preview and is now generally available (GA).  This means the feature is ready for use in production. However, the individual baseline templates can remain in preview and are evaluated and released to GA on their own schedules.

#### The MDM Security Baseline template is now generally available   <!-- 3794072, 4217151,  3534649 -->
The MDM Security Baseline template has moved out of preview and is now generally available (GA). The GA template is identified as **MDM Security Baseline for May 2019**.  This is a new template and not an upgrade from the preview version.  As a new template, you’ll need to review the [settings it contains](security-baseline-settings-windows.md), and then create new profiles to deploy the template to your device. Other security baseline templates can remain in preview. For a list of available baselines, see [Available security baselines](security-baselines.md#available-security-baselines).  

In addition to being a new template, the *MDM Security Baseline for May 2019* template includes the two settings that we recently announced in our In Development article:  
- Above Lock: Voice activate apps from a locked screen  
- DeviceGuard: Use virtualization-based security (VBS) at the next reboot of devices.  

The *MDM Security Baseline for May 2019* also includes the addition of several new settings, the removal of others, and a revision of the default value of one setting. For a detailed list of the changes from Preview to GA, see **What’s changed in the new template**.

#### Security baseline versioning  <!-- 3194322 -->
Security baselines for Intune support versioning. With this support, as new versions of each security baseline are released, you can update your existing security baseline profiles to use the newer baseline version without having to recreate and deploy a new baseline from scratch. Additionally, in the Intune console you can view information about each baseline like the number of individual profiles you have that use the baseline, how many of the different baseline versions your profiles use, and when the latest release of a specific security baseline was.  For more information, see **Security Baselines**.

#### The Use security keys for sign-in setting has moved  <!-- 4501151 -->
The device configuration setting for identity protection named **Use security keys for sign-in** is no longer found as a sub-setting of *Configure Windows Hello for Business*. It's now a top-level setting that is always available, even when you don't enable use of Windows Hello for Business. For more information, see [Identity protection](identity-protection-windows-settings.md).

### Role-based access control

#### New permissions for assigned group admins   <!-- 4504437   -->
Intune's built-in School Administrator role now has create, read, update, and delete (CRUD) permissions for Managed Apps. This update means that if you're assigned as a group admin in Intune for Education, you can now create, view, update, and delete the iOS MDM Push Certificate, iOS MDM server tokens, and iOS VPP tokens along with [all of the existing permissions you have](https://docs.microsoft.com/intune-education/group-admin-delegate#group-admin-permissions). To take any of these actions, go to **Tenant settings** > **iOS Device Management**.  

#### Applications can use the Graph API to call read operations without user credentials <!-- 4655885 -->
Applications can call Intune Graph API read operations with app identity without user credentials. For more information about accessing the Microsoft Graph API for Intune, see [Working with Intune in Microsoft Graph](https://docs.microsoft.com/graph/api/resources/intune-graph-overview?view=graph-rest-1.0).

#### Apply scope tags to Microsoft Store for Business apps <!-- 4392555 -->
You can now apply scope tags to Microsoft Store for Business apps. For more information about scope tags, see [Use role-based access control (RBAC) and scope tags for distributed IT](scope-tags.md).

## Week of June 17, 2019 

### App management

#### New features in Microsoft Intune app
We’ve added new features to the Microsoft Intune app (preview) for Android. Users on fully managed Android devices can now:  

* View and manage the devices they've enrolled through the Intune Company Portal or Microsoft Intune app.    
* Contact their organization for support.    
* Send their feedback to Microsoft.    
* View terms and conditions, if set by their organization.    

## Week of June 10, 2019 

### App management

#### New sample apps showing Intune SDK integration available on GitHub <!-- 2653471 -->
The msintuneappsdk GitHub account has added new sample applications for iOS (Swift), Android, Xamarin.iOS, Xamarin Forms, and Xamarin.Android. These apps are meant to supplement our existing documentation and provide demonstrations of how to integrate the Intune APP SDK into your own mobile apps. If you are an app developer that needs additional Intune SDK guidance, see the following linked samples:
- [Chatr](https://github.com/msintuneappsdk/Chatr-Sample-Intune-iOS-App) - A native iOS (Swift) instant messaging app that uses the Azure Active Directory Authentication Library (ADAL) for brokered authentication.
- [Taskr](https://github.com/msintuneappsdk/Taskr-Sample-Intune-Android-App) - A native Android todo list app that uses ADAL for brokered authentication.
- [Taskr](https://github.com/msintuneappsdk/Taskr-Sample-Intune-Xamarin-Android-Apps) - A Xamarin.Android todo list app that uses ADAL for brokered authentication, this repository also has the Xamarin.Forms app.
- [Xamarin.iOS sample app](https://github.com/msintuneappsdk/sample-intune-xamarin-ios) - A barebones Xamarin.iOS sample app.

## Week of May 27, 2019 

### App management

#### Reporting for potentially harmful apps on Android devices <!-- 4223162 -->
Intune now provides additional reporting information about potentially harmful apps on Android devices. 

## Week of May 20, 2019 

### App management

#### Windows Company Portal app <!-- 3316993 -->
The Windows Company Portal app will now have a new page labeled **Devices**. The **Devices** page will show end users all of their enrolled devices. Users will see this change in the Company Portal when they use version 10.3.4291.0 and later. For information about the configuring the Company Portal, see [How to configure the Microsoft Intune Company Portal app](company-portal-app.md).

### Device enrollment

#### Autopilot device OrderID attribute name changed to Group Tag <!-- 4659453 -->

To make it more intuitive, the **OrderID** attribute name on Autopilot devices has been changed to **Group Tag**. When using CSVs to upload Autopilot device information, you must use Group Tag as the column header, not OrderID.  

## Week of May 13, 2019 

### App management

#### Intune policies update authentication method and Company Portal app installation  <!-- 1927359  -->
On devices already enrolled via Setup Assistant through one of Apple’s corporate device enrollment methods, Intune will no longer support the Company Portal when it is manually installed by end users from the app store. This change is only relevant when you authenticate with Apple Setup Assistant during enrollment. This change also only affects iOS devices enrolled through:  
* Apple configurator

* Apple Business Manager

* Apple School Manager

* Apple Device Enrollment Program (DEP)

If users install the Company Portal app from the App store, and then try to enroll these devices through it, they will receive an error. These devices will be expected to only use the Company Portal when it's been pushed, automatically, by Intune during enrollment. Enrollment profiles in Intune in the Azure portal will be updated so that you can specify how devices authenticate and if they receive the Company Portal app. If you want your DEP device users to have the Company Portal, you will need to specify your preferences in an enrollment profile. 

In addition, the **Identify your device** screen in the iOS Company Portal is being removed. Therefore, admins who want to enable Conditional Access or deploy company apps must update the DEP enrollment profile. This requirement only applies if the DEP enrollment is authenticated with Setup Assistant. In that case, you must push the Company Portal onto the device. To do so, choose **Intune** > **Device enrollment** > **Apple enrollment** > **Enrollment program tokens** > choose a token > **Profiles** > choose a profile > **Properties** > set **Install Company Portal** to **Yes**.

To install the Company Portal on already-enrolled DEP devices, you will need to go to Intune > Client apps, and push it as a managed app with app configuration policies. 

#### Configure how end users update a line-of-business (LOB) app using an app protection policy <!-- 3568384 -->
You can now configure where your end users can get an updated version of a line-of-business (LOB) app. End users will see this feature in the **min app version** conditional launch dialog, which will prompt end users to update to a minimum version of the LOB app. You must provide these update details as part of your LOB app protection policy (APP). This feature is available on iOS and Android. On iOS, this feature requires the app to be integrated (or wrapped using the wrapping tool) with the Intune SDK for iOS v. 10.0.7 or above. On Android, this feature would require the latest Company Portal. To configure how an end user updates a LOB app, the app needs a managed app configuration policy sent to it with the key, `com.microsoft.intune.myappstore`. The value sent will define which store the end user will download the app from. If the app is deployed via the Company Portal, the value must be `CompanyPortal`. For any other store, you must enter a complete URL.

#### Intune management extension PowerShell scripts  <!-- 3734186  -->
You can configure PowerShell scripts to run with the user’s admin privileges on the device. For more information, see [Use PowerShell scripts on Windows 10 devices in Intune](intune-management-extension.md) and [Win32 app management](apps-win32-app-management.md).

#### Android Enterprise app management <!-- 4459905 -->
To make it easier for IT admins to configure and use Android Enterprise management, Intune will automatically add four common Android Enterprise related apps to the Intune admin console. The four Android Enterprise apps are the following apps:

- **[Microsoft Intune](https://play.google.com/store/apps/details?id=com.microsoft.intune)** - Used for Android Enterprise fully managed scenarios.
- **[Microsoft Authenticator](https://play.google.com/store/apps/details?id=com.azure.authenticator)** - Helps you sign in to your accounts if you use two-factor verification.
- **[Intune Company Portal](https://play.google.com/store/apps/details?id=com.microsoft.windowsintune.companyportal)** - Used for App Protection Policies (APP) and Android Enterprise work profile scenarios.
- [Managed Home Screen](https://play.google.com/store/apps/details?id=com.microsoft.launcher.enterprise) - Used for Android Enterprise dedicated/kiosk scenarios.

Previously, IT admins would need to manually find and approve these apps in the [Managed Google Play store](https://play.google.com/store/apps) as part of setup. This change removes those previously manual steps to make it easier and faster for customers to use Android Enterprise management.

Admins will see these four apps automatically added to their Intune apps list at the time that they first connect their Intune tenant to managed Google Play. For more information, see [Connect your Intune account to your Managed Google Play account](connect-intune-android-enterprise.md). For tenants that have already connected their tenant or who already use Android Enterprise, there is nothing admins need to do. Those four apps will automatically show up within 7 days of the completion of the May 2019 service rollout.

### Device configuration

#### Updated PFX Certificate Connector for Microsoft Intune  <!-- 1533038 -->
We’ve released an update for the [PFX Certificate Connector for Microsoft Intune](certficates-pfx-configure.md#whats-new-for-connectors) that addresses an issue where existing PFX certificates continue to be reprocessed, which causes the connector to stop processing new requests.

#### Intune security tasks for Defender ATP (In public preview)     <!-- 3208597 -->
In public preview, you can use Intune to manage [security tasks for Microsoft Defender Advanced Threat Protection (ATP)](atp-manage-vulnerabilities.md). This integration with ATP and adds a risk-based approach to discover, prioritize, and remediate endpoint vulnerabilities and misconfigurations, while reducing the time between discovery to mitigation.

#### Check for a TPM chipset in a Windows 10 device compliance policy <!-- 3617671   idstaged-->
Many Windows 10 and later devices have Trusted Platform Module (TPM) chipsets. This update includes a new compliance setting that checks the TPM chip version on the device. 

[Windows 10 and later compliance policy settings](compliance-policy-create-windows.md#device-security) describes this setting.

Applies to: Windows 10 and later

#### Prevent end users from modifying their Personal HotSpot and disable Siri server logging on iOS devices <!-- 4097904   -->  
You create a device restrictions profile on iOS device (**Device configuration** > **Profiles** > **Create profile** > **iOS** for platform > **Device restrictions** for profile type). This update includes new settings you can configure:

- **Built-in Apps**: Server-side logging for Siri commands
- **Wireless**: User modification of Personal Hotspot (supervised only)

To see these settings, go to [built-in app settings for iOS](device-restrictions-ios.md#built-in-apps) and [wireless settings for iOS](device-restrictions-ios.md#wireless).

Applies to: iOS 12.2 and newer

#### New classroom app device restriction settings for macOS devices <!-- 4097905   --> 
You can create device configuration profiles for macOS devices (**Device configuration** > **Profiles** > **Create profile** > **macOS** for platform > **Device restrictions** for profile type). This update includes new classroom app settings, the option to block screenshots, and the option to disable the iCloud Photo Library.

To see the current settings, go to [macOS device settings to allow or restrict features using Intune](device-restrictions-macos.md).

Applies to: macOS

#### The iOS Password to access app store setting is renamed<!-- 4557891  -->
The **Password to access app store** setting is renamed to **Require iTunes Store password for all purchases** (**Device configuration** > **Profiles** > **Create profile** > **iOS** for platform > **Device restrictions** for profile type > **App store, Doc viewing, and Gaming**).

To see the available settings, go to [App Store, Doc Viewing, Gaming iOS settings](device-restrictions-ios.md#app-store-doc-viewing-gaming).

Applies to: iOS

#### Microsoft Defender Advanced Threat Protection  baseline  (Preview)  <!--  3754134 -->
We've added a security baseline Preview for [Microsoft Defender Advanced Threat Protection](security-baseline-settings-defender-atp.md) settings. This baseline is available when your environment meets the prerequisites for using [Microsoft Defender Advanced Threat Protection](advanced-threat-protection.md#prerequisites).

### Device enrollment

#### Windows Enrollment Status Page (ESP) is now generally available <!-- 3605348 -->
The Enrollment Status Page is now out of preview. For more information, see [Set up an enrollment status page](windows-enrollment-status.md).


#### Intune user interface update - Autopilot enrollment profile creation  <!-- 4593669 -->
The user interface for creating an Autopilot enrollment profile has been updated to align with Azure user interface styles. For more information, see [Create an Autopilot enrollment profile](enrollment-autopilot.md#create-an-autopilot-deployment-profile). Moving forward, additional Intune scenarios will be updated to this new UI style.

#### Enable Autopilot Reset for all Windows devices <!-- 4225665 -->
Autopilot Reset now works for all Windows devices, even those not configured to use the Enrollment Status Page. If an enrollment status page wasn't configured for the device during initial device enrollment, the device will go straight to the desktop after sign-in. It might take up to eight hours to sync and appear compliant in Intune. For more information, see [Reset devices with remote Windows Autopilot Reset](https://docs.microsoft.com/windows/deployment/windows-autopilot/windows-autopilot-reset-remote).

#### Exact IMEI format not required when searching All devices <!--30407680 -->
You won't need to include spaces in IMEI numbers when you search **All devices**.

#### Deleting a device in the Apple portal will be reflected in the Intune portal <!--2489996 -->
If a device is deleted from Apple's Device Enrollment Program or Apple Business Manager portals, the device will automatically be deleted from Intune during the next sync.

### The Enrollment Status Page now tracks Win32 apps <!-- 2714451 -->
This only applies to devices running Windows 10 version 1903 and above. For more information, see [Set up an enrollment status page](windows-enrollment-status.md).

### Device management

#### Reset and wipe devices in bulk by using the Graph API <!-- 3295288 -->
You can now reset and wipe up to 100 devices in bulk using the Graph API.


### Monitor and troubleshoot

#### The Encryption report is out of Public Preview   <!-- 4587546      -->
The [report for BitLocker and device encryption](encryption-monitor.md) is now generally available, and no longer part of the public preview. 

<!-- ########################## -->

#### Outlook signature and biometric settings for  iOS and Android devices <!-- 4050557 -->
You can now specify if the default signature is enabled in Outlook on iOS and Android devices. Additionally, you can choose to allow users to change the biometric setting in Outlook on iOS.

## Week of May 6, 2019 

### Device configuration

#### Network Access Control (NAC) support for F5 Access for iOS devices <!-- 4500808 -->

F5 released an update to BIG-IP 13 that allows NAC functionality for F5 Access on iOS in Intune. To use this feature:

- Update BIG-IP to 13.1.1.5 refresh. BIG-IP 14 isn't supported.
- Integrate BIG-IP with Intune for NAC. Steps in [Overview: Configuring APM for device posture checks with endpoint management systems](https://techdocs.f5.com/kb/en-us/products/big-ip_apm/manuals/product/apm-client-configuration-7-1-6/6.html).
- Check the **Enable Network Access Control (NAC)** setting in the VPN profile in Intune.

To see the available setting, go to [Configure VPN settings on iOS devices](vpn-settings-ios.md).

Applies to: iOS

#### Updated PFX Certificate Connector for Microsoft Intune <!-- doc-vso 1521237  -->  
We’ve released an update for the [PFX Certificate Connector for Microsoft Intune](certficates-pfx-configure.md#whats-new-for-connectors) that drops the polling interval from 5 minutes to 30 seconds.

## Week of April 22, 2019

### Use Compliance Manager to create assessments for Microsoft Intune<!-- 4404750 -->

[Compliance Manager](https://servicetrust.microsoft.com/ComplianceManager) (opens another Microsoft site) is a workflow-based risk assessment tool in the Microsoft Service Trust Portal. It enables you to track, assign, and verify your organization’s regulatory compliance activities related to Microsoft services. You can create your own compliance assessment with Office 365, Azure, Dynamics, Professional Services, and Intune. Intune has two assessments available - FFIEC and GDPR.

Compliance Manager helps you focus your efforts by breaking down controls - controls managed by Microsoft, and controls managed by your organization. You can complete the assessments, and then export and print the assessments.

[Federal Financial Institutions Examination Council (FFIEC)](https://www.microsoft.com/trustcenter/compliance/FFIEC) (opens another Microsoft site) compliance is a set of standards for online banking issued by FFIEC. It's the most requested assessment for financial institutions that use Intune. It interprets how Intune helps meet FFIEC cybersecurity guidelines related to public cloud workloads. Intune’s FFIEC assessment is the second FFIEC assessment in Compliance Manager.

In the following example, you can see the breakdown for FFIEC controls. Microsoft covers 64 controls. You're responsible for the remaining 12 controls.

![See a sample Intune assessment for FFIEC, including the customer actions and Microsoft actions](./media/intune-ffiec-assessment-status.png)

[General Data Protection Regulation (GDPR)](https://www.microsoft.com/trustcenter/privacy/gdpr/gdpr-overview) (opens another Microsoft site) is a European Union (EU) law that helps protect the rights of individuals and their data. GDPR is the most requested assessment to help comply with privacy regulations. 

In the following example, you see the breakdown for GDPR controls. Microsoft covers 49 controls. You're responsible for the remaining 66 controls.

![See a sample Intune assessment for GDPR, including the customer actions and Microsoft actions](./media/intune-assessment-status.png)

## Week of April 15, 2019

### App management

#### OpenSSL encryption for Android app protection policies <!-- 3747362 -->
Intune app protection policies (APP) on Android devices now uses an OpenSSL encryption library that is FIPS 140-2 compliant. For more information, see the [encryption](app-protection-policy-settings-android.md#encryption) section of [Android app protection policy settings in Microsoft Intune](app-protection-policy-settings-android.md).

#### Enable Win32 app dependencies <!-- 2617348  -->
As the admin, you can require that other apps are installed as dependencies before installing your Win32 app. Specifically, the device must install the dependent app(s) before it installs the Win32 app. In Intune, select **Client apps** > **Apps** > **Add** to display the **Add app** blade. Select **Windows app (Win32)** as the **App type**. After you have added the app, you can select **Dependencies** to add the dependent apps that must be installed before the Win32 app can be installed. For more information, see [Intune Standalone - Win32 app management](apps-win32-app-management.md). 

#### App version installation information for Microsoft Store for Business apps <!-- 3537391   -->
App installation reports include app version information for Microsoft Store for Business apps. In Intune, select **Client apps** > **Apps**. Select a **Microsoft Store for Business app** and then select **Device install status** under the **Monitor** section.

#### Additions to Win32 apps requirement rules <!-- 3676883   -->
You can create requirement rules based on PowerShell scripts, registry values, and file system information. In Intune, select **Client apps** > **Apps** > **Add**. Then select **Windows app (Win32)** as the **App type** in the **Add app** blade.  Select **Requirements** > **Add** to configure additional requirement rules. Then, select either **File type**, **Registry**, or **Script** as the **Requirement type**. For more information, see [Win32 app management](apps-win32-app-management.md).

#### Configure your Win32 apps to be installed on Intune enrolled Azure AD joined devices <!-- 3695227  -->
You can assign your Win32 apps to be installed on Intune enrolled Azure AD joined devices. For more information about Win32 apps in Intune, see [Win32 app management](apps-win32-app-management.md).

#### Device overview shows Primary User <!--3794259  -->
The Device overview page will show the Primary User, also called the User Device Affinity User (UDA). To see the Primary User for a device, choose **Intune** > **Devices** > **All devices** > choose a device. The Primary User will appear near the top of the **Overview** page.

#### Additional Managed Google Play app reporting for Android Enterprise work profile devices <!-- 4105925  -->
For Managed Google Play apps deployed to Android Enterprise work profile devices, you can view the specific version number of the app installed on a device. This applies to required apps only.  

#### iOS Third Party Keyboards <!-- 4111843   -->
The Intune app protection policy (APP) support for the **Third Party Keyboards** setting for iOS is no longer supported due to an iOS platform change. You will not be able to configure this setting in the Intune Admin Console and it will not be enforced on the client in the Intune App SDK.

### Device configuration

#### Set login settings and control restart options on macOS devices <!-- 1210083  -->
On macOS devices, you can create a device configuration profile (**Device configuration** > **Profiles** > **Create profile** > choose **macOS** for platform > **Device features** for profile type). This update includes new login window settings, such as showing a custom banner, choose how users sign in, show or hide the power settings, and more.

To see these settings, go to [macOS device feature settings](macos-device-features-settings.md).

#### Configure WiFi on Android Enterprise, Device Owner dedicated devices running in multi-app kiosk mode <!--3041940  -->
You can enable settings on Android Enterprise, Device Owner when running as a dedicated device in multi-app kiosk mode. In this update, you can enable users to configure and connect to WiFi networks (**Intune** > **Device configuration** > **Profiles** > **Create profile** > **Android Enterprise** for platform > **Device owner only, Device restrictions** for profile type > **Dedicated devices** > **Kiosk mode**: **Multi-app** > **WiFi configuration**). 

To see all the settings you can configure, go to [Android Enterprise device settings to allow or restrict features](device-restrictions-android-for-work.md).

Applies to: Android Enterprise dedicated devices running in multi-app kiosk mode


#### Configure Bluetooth and pairing on Android Enterprise, Device Owner dedicated devices running in multi-app kiosk mode <!-- 3041941  -->
You can enable settings on Android Enterprise, Device Owner when running as a dedicated device in multi-app kiosk mode. In this update, you can allow end users to enable Bluetooth, and pair devices over Bluetooth (**Intune** > **Device configuration** > **Profiles** > **Create profile** > **Android Enterprise** for platform > **Device owner only, Device restrictions** for profile type > **Dedicated devices** > **Kiosk mode**: **Multi-app** > **Bluetooth configuration**). 

To see all the settings you can configure, go to [Android Enterprise device settings to allow or restrict features](device-restrictions-android-for-work.md).

Applies to: Android Enterprise dedicated devices running in multi-app kiosk mode

#### Create and use OEMConfig device configuration profiles in Intune <!-- 3305883  -->
In this update, Intune supports configuring Android Enterprise devices with OEMConfig. Specifically, you can create a device configuration profile, and apply settings to Android Enterprise devices using OEMConfig (**Device configuration** > **Profiles** > **Create profile** > **Android enterprise** for platform).

Support for OEMs is currently on a per-OEM basis. If an OEMConfig app you want isn't available in the list of OEMConfig apps, contact `IntuneOEMConfig@microsoft.com`.

To learn more about this feature, go to [Use and manage Android Enterprise devices with OEMConfig in Microsoft Intune](android-oem-configuration-overview.md).

Applies to: Android enterprise

#### Windows Update notifications  <!-- 3316758, 3316782  -->
We've added two *User experience settings* to the Windows Update ring configurations that you can manage from within the Intune console. You can now:
- Block or allow users to [scan for Windows updates](windows-update-settings.md).
- Manage the [Windows Update notification level](windows-update-settings.md) that users see.

#### New device restriction settings for Android Enterprise, Device Owner <!-- 3574254  -->
On Android Enterprise devices, you can create a device restriction profile to allow or restrict features, set password rules, and more (**Device configuration** > **Profiles** > **Create profile** > choose **Android Enterprise** for platform > **Device owner only > Device restrictions** for profile type). 

This update includes new password settings, allows full access to apps in Google Play Store for fully managed devices, and more. To see the current list of settings, go to [Android Enterprise device settings to allow or restrict features](device-restrictions-android-for-work.md). 

Applies to: Android Enterprise fully managed devices

#### Check for a TPM chipset in a Windows 10 device compliance policy <!-- 3617671 -->

This feature is delayed and is planned to be released later.

#### Updated UI changes for Microsoft Edge Browser on Windows 10 and later devices <!-- 3775833   -->
When you create a device configuration profile, you can allow or restrict Microsoft Edge features on Windows 10 and later devices (**Device configuration** > **Profiles** > **Create profile** > **Windows 10 and later** for platform,  > **Device restrictions** for profile type > **Microsoft Edge Browser**). In this update, the Microsoft Edge settings are more descriptive, and easier to understand. 

To see these features, go to [Microsoft Edge Browser device restriction settings](device-restrictions-windows-10.md#microsoft-edge-browser).

Applies to: Windows 10 and later

#### Expanded support for Android Enterprise fully managed devices  (Preview)  <!--   3903241, 3903244, 3903246   -->
Still in a public preview, we've expanded our support of Android Enterprise fully managed devices ([first announced in January of 2019](whats-new.md#week-of-january-14-2019) to include the following: 

- On fully managed and dedicated devices, you can create [compliance policies](compliance-policy-create-android-for-work.md) to include password rules and operating system requirements (**Device compliance** > **Policies** > **Create policy** > **Android Enterprise** for platform > **Device owner** for profile type). 

  On dedicated devices, the device may show as **Not compliant**. Conditional Access isn't available on dedicated devices. Be sure to complete any tasks or actions to get dedicated devices compliant with your assigned policies.

- [Conditional Access](conditional-access.md) - Conditional Access policies that apply to Android also apply to Android Enterprise fully managed devices. Users can now register their fully managed device in Azure Active Directory using the **Microsoft Intune app**. Then, see and resolve any compliance issues to access organizational resources.

- New end-user app (Microsoft Intune app) - There is a new end-user app for Android fully managed devices called **Microsoft Intune**. This new app is light-weight and modern, and provides similar functionally as the Company Portal app, but for fully managed devices. For more information, see [Microsoft Intune app on Google Play](https://play.google.com/store/apps/details?id=com.microsoft.intune).

To set up Android fully managed devices, go to **Device enrollment** > **Android enrollment** > **Corporate-owned, fully managed user devices**. Support for fully managed Android devices remains in preview, and some Intune features might not be fully functional.  

To learn more about this preview, see our blog, [Microsoft Intune - Preview 2 for Android Enterprise Fully Managed devices](https://aka.ms/preview2_AE_fullymanaged).


### Device enrollment

#### Configure profile to skip some screens during Setup Assistant <!-- 2276470  -->
When you create a macOS enrollment profile, you can configure it to skip any of the following screens when a user goes through the Setup Assistant:
- Appearance
- Display Tone
- iCloudStorage
If you create a new profile or edit a profile, the selected skip screens need to sync with the Apple MDM server.  Users can issue a manual sync of the devices so that there is no delay in picking up the profile changes.
For more information, see [Automatically enroll macOS devices with the Device Enrollment Program or Apple School Manager](device-enrollment-program-enroll-macos.md).

#### Bulk device naming when enrolling corporate iOS devices<!--3566569  -->
When using one of Apple's corporate enrollment methods (DEP/ABM/ASM), you can set a device name format to automatically name incoming iOS devices. You can specify a format that includes the device type and serial number in your template. To do so, choose **Intune** > **Device enrollment** > **Apple enrollment** > **Enrollment program tokens** > **Select a token** >**Create profile** > **Device naming format**. You can edit existing profiles, but only newly synced devices will have the name applied.

#### Updated default timeout message on Enrollment Status Page <!-- 3959331 -->
We've updated the default timeout message users see when the Enrollment Status Page (ESP) exceeds the timeout value specified in the ESP profile. The new default message is what users see and helps them understand the next actions to take with their ESP deployment.  

### Device management

#### Retire noncompliant devices  <!-- 1827291   -->
This feature has been delayed and is planned for a future release.


### Monitor and troubleshoot

#### Intune Data Warehouse V1.0 changes reflecting back to beta <!-- 4403765 -->
When V1.0 was first introduced in 1808, it differed in some significant ways from the beta API. In 1903 those changes will be reflected back into the beta API version. If you have important reports that use the beta API version, we strongly recommend switching those reports to V1.0 to avoid breaking changes. For more information, see [Change log for the Intune Data Warehouse API](reports-changelog.md#1903-part-2).

#### Monitor Security Baseline status (public preview) <!-- 3082047 --> 
We've added a [per-category view](security-baselines-monitor.md#per-category-view) to the monitoring of security baselines. (Security baselines remain in preview). The per-category view displays each category from the baseline along with the percentage of devices that fall into each status group for that category. You can now see how many devices don't match the individual categories, are misconfigured, or are not applicable.

### Role-based access control

#### Scope tags for Apple VPP tokens <!--2371886  -->
You can now add scope tags to Apple VPP tokens. Only users assigned with the same scope tag will have access to the Apple VPP token with that tag. VPP apps and ebooks purchased with that token inherit its scope tags. For more information about scope tags, see [Use RBAC and scope tags](scope-tags.md).







## Week of April 1, 2019

### Device configuration

#### Updated certificate connectors  <!-- ICM 113304612 -->
We’ve released updates for both the [Intune Certificate Connector and the PFX Certificate Connector for Microsoft Intune](certficates-pfx-configure.md#whats-new-for-connectors). The new releases fix several known issues.  

### App management

#### User experience update for the Company Portal app for iOS <!-- 2536024 -->
The home page of the Company Portal app for iOS devices has been redesigned. With this change, the home page will better follow iOS UI patterns, and also provide improved discoverability for apps and ebooks.

#### Changes to Company Portal enrollment for iOS 12 device users <!--3448635 -->  
The Company Portal for iOS enrollment screens and steps have been updated to align with the MDM enrollment changes released in Apple iOS 12.2. The updated workflow prompts users to:  

* Allow Safari to open the Company Portal website and download the management profile before returning to the Company Portal app.  
* Open the Settings app to install the management profile on their device.
* Return to the Company Portal app to complete enrollment.  

For updated enrollment steps and screens, see [Enroll iOS device in Intune](https://docs.microsoft.com/intune-user-help/enroll-your-device-in-intune-ios).  

## Week of March 25, 2019

### Monitor and troubleshoot

### Support for the Power BI Compliance app from the Data Warehouse blade in Microsoft Intune <!-- 4260871 -->
Previously, the **Download Power BI file** link in the **Intune Data Warehouse** blade downloaded an Intune Data Warehouse report (.pbix file). This report has been replaced with the Power BI Compliance app. The Power BI Compliance app will not require special loading or setup. It will open directly in the Power BI online portal and display data specifically for your Intune tenant based on your credentials. In Intune, select the **Set up Intune Data Warehouse** link on the right side of the Intune blade. Then, click **Get Power BI App**. For more information, see [Connect to the Data Warehouse with Power BI](reports-proc-get-a-link-powerbi.md).

## Week of March 18, 2019

### App management

#### Deploy Microsoft Visio and Microsoft Project <!-- 3725386  -->
You can now deploy Microsoft Visio Pro for Office 365 and Microsoft Project Online Desktop Client as independent apps to Windows 10 devices using Microsoft Intune, if you own licenses for these apps. From Intune, select **Client apps** > **Apps** > **Add** to display the **Add app** blade. On the **Add app** blade, select **Windows 10** as the **App type**. Then, select **Configure App Suite** to select apps to install. For more information about Office 365 apps for Windows 10 devices, see [Assign Office 365 apps to Windows 10 devices with Microsoft Intune](apps-add-office365.md).

#### Microsoft Visio Pro for Office 365 product name change <!-- 3593653  -->
**Microsoft Visio Pro for Office 365** will now be known as **Microsoft Visio Online Plan 2**.  For more information about Microsoft Visio, see [Visio Online Plan 2](https://products.office.com/visio/visio-online-plan-2). For more information about Office 365 apps for Windows 10 devices, see [Assign Office 365 apps to Windows 10 devices with Microsoft Intune](apps-add-office365.md).

#### Intune app protection policy (APP) character limit setting <!-- 3291302  -->
Intune admins can specify an exception to the Intune APP  **Restrict cut, copy, and paste with other apps** policy setting.  As the admin, you can specify the number of characters that may be cut or copied from a managed app. This setting will allow sharing of the specified number of characters to any app, regardless of the "Restrict cut, copy, and paste with other apps" setting. Note that the Intune Company Portal app version for Android requires version 5.0.4364.0 or later. For more information, see [iOS data protection](app-protection-policy-settings-ios.md#data-protection), [Android data protection](app-protection-policy-settings-android.md#data-protection), and [Review client app protection logs](app-protection-policy-settings-log.md#app-protection-policy-settings).

#### Office Deployment Tool (ODT) XML for Office ProPlus deployment <!-- 3192477   -->
You will be able to provide Office Deployment Tool (ODT) XML when creating an instance of Office Pro Plus in the Intune admin console. This will allow greater customizability if the existing Intune UI options do not meet your needs. For more information, see [Assign Office 365 apps to Windows 10 devices with Microsoft Intune](apps-add-office365.md) and [Configuration options for the Office Deployment Tool](https://docs.microsoft.com/DeployOffice/configuration-options-for-the-office-2016-deployment-tool).

#### App icons will now be displayed with an automatically generated background <!-- 1429026  -->
In the Windows Company Portal app, app icons will now be displayed with an automatically generated background based on the dominant color of the icon (if it can be detected). When applicable, this background will replace the gray border that was previously visible on app tiles. Users will see this change in versions of Company Portal later than 10.3.3451.0.

#### Install available apps using the Company Portal app after Windows bulk enrollment <!-- 2751523   -->
Windows devices that enrolled into Intune using [Windows bulk enrollment](windows-bulk-enroll.md) (provisioning packages) will be able to use the Company Portal app to install available apps. For more information about the Company Portal app, see [Manually add the Windows 10 Company Portal](store-apps-company-portal-app.md) and [How to configure the Microsoft Intune Company Portal app](company-portal-app.md).

#### The Microsoft Teams app can be selected as part of the Office app suite <!-- 3828932  -->
The Microsoft Teams app can be included or excluded as part of the Office Pro Plus app suite installation. This feature works for Office Pro Plus build number 16.0.11328.20116+. The user must sign out and then sign in to the device for the installation to complete. In Intune, select **Client apps** > **Apps** > **Add**. Select one of the **Office 365 Suite** app types and then select **Configure  App Suite**.

### Device configuration

#### Automatically start an app when running multiple apps in kiosk mode on Windows 10 and later devices <!-- 2351390 -->

On Windows 10 and later devices, you can run a device in kiosk mode, and run many apps. In this update, there's an **AutoLaunch** setting (**Device configuration** > **Profiles** > **Create profile** > **Windows 10 and later** for platform > **Kiosk** for profile type > **Multi-app kiosk**). Use this setting to automatically start an app when the user signs in to the device.

To see a list and description of all the kiosk settings, see [Windows 10 and later device settings to run as a kiosk in Intune](kiosk-settings-windows.md).

Applies to: Windows 10 and later

#### Operational logs also show details on non-compliant devices <!-- 4063755  -->
When routing Intune logs to Azure monitor features, you can also route the operational logs. In this update, the operational logs also provide information on non-compliant devices. 

For more information on this feature, see [Send log data to storage, event hubs, or log analytics in Intune](review-logs-using-azure-monitor.md).

#### Route logs to Azure Monitor in more Intune workloads <!-- 3804627 -->
In Intune, you can route audit and operational logs to events hubs, storage, and log analytics in Azure Monitor (**Intune** > **Monitoring** > **Diagnostics settings**). In this update, you can route these logs in more Intune workloads, including compliance, configurations, client apps, and more. 

To learn more about routing logs to Azure Monitor, see [send log data to storage, event hubs, or log analytics](review-logs-using-azure-monitor.md).

#### Create and use mobility extensions on Android Zebra devices in Intune <!-- 3305880   -->
In this update, Intune supports configuring Android Zebra devices. Specifically, you can create a device configuration profile, and apply settings to Android Zebra devices using Mobility Extensions (MX) profiles generated by StageNow (**Device configuration** > **Profiles** > **Create profile** > **Android** for platform > **MX profile (Zebra only)** for profile type).

For more information on this feature, see [Use and manage Zebra devices with mobility extensions in Intune](android-zebra-mx-overview.md).

Applies to: Android

### Device management

#### Encryption report for Windows 10 Devices (in public preview)<!-- 2351538 -->  
Use the new [Encryption report (Preview)](encryption-monitor.md) to view details about the encryption status of your Windows 10 devices. Available details include a devices TPM version, encryption readiness and status, error reporting, and more.  

#### Access BitLocker recovery keys from the Intune portal (in public preview) <!-- 2351547   -->  
You can now use Intune to [view details](encryption-monitor.md) about BitLocker Key ID and BitLocker recovery keys, from Azure Active Directory.

#### Microsoft Edge support for Intune scenarios on iOS and Android devices <!-- 3411007 -->
Microsoft Edge will support all of the same management scenarios as the Intune Managed Browser with the addition of improvements to end-user experience. Microsoft Edge enterprise features that are enabled by Intune policies include dual-Identity, app protection policy integration, Azure application proxy integration, and managed favorites and home page shortcuts. For more information, see [Microsoft Edge support](app-configuration-managed-browser.md#microsoft-edge-support).

#### Exchange Online/Intune Connector deprecate support for EAS only devices <!--3105122  -->
The Intune console no longer supports viewing and managing EAS-only devices connected to Exchange Online with the Intune Connector. Instead, you have the following options:
- Enroll devices in Mobile Device Management (MDM)
- Use Intune App Protection Policies to manage your devices
- Use Exchange controls as outlined in [Clients and mobile in Exchange Online](https://docs.microsoft.com/exchange/clients-and-mobile-in-exchange-online/clients-and-mobile-in-exchange-online)

### Search the All devices page for an exact device by using [name] <!--4254930 -->
You can now search for an exact device name. Go to **Intune** > **Devices** > **All devices** > in the search box, surround the device name with {} to search for an exact match. For example, **{Device12345}**.

### Monitor and troubleshoot

#### Support for additional connectors on the Tenant Status page <!-- 3617202  -->
The [Tenant Status page](tenant-status.md) now displays status information for additional connectors, including *Windows Defender Advanced Threat Protection* (ATP) and other Mobile Threat Defense connectors.

### Role-based access control

#### Granting Intune read-only access to some Azure Active Directory roles <!-- 3637917  -->
Intune read-only access has been granted to the following Azure AD roles. Permissions granted with Azure AD roles supersede permissions granted with Intune role-based access control (RBAC).

Read-only access to Intune audit data:

- Compliance Administrator
- Compliance Data Administrator

Read-only access to all Intune data:

- Security Administrator
- Security Operator
- Security Reader

For more information, see [Role-based access control](role-based-access-control.md).

#### Scope tags for iOS app provisioning profiles <!--2934430   -->
You can add a scope tag to an iOS app provisioning profile so that only people with roles also assigned that scope tag have access to the iOS app provisioning profile. For more information, see [Use RBAC and scope tags](scope-tags.md).

#### Scope tags for app configuration policies <!--2371891   -->
You can add a scope tag to an app configuration policy so that only people with roles also assigned that scope tag have access to the app configuration policy. The app configuration policy can only be targeted to or associated with apps assigned the same scope tag. For more information, see [Use RBAC and scope tags](scope-tags.md).

### Microsoft Edge support for Intune scenarios on iOS and Android devices <!-- 3411007 -->
Microsoft Edge will support all of the same management scenarios as the Intune Managed Browser with the addition of improvements to the end-user experience. Microsoft Edge enterprise features that are enabled by Intune policies include dual-Identity, app protection policy integration, Azure application proxy integration, and managed favorites and home page shortcuts. For more information, see [Microsoft Edge support](app-configuration-managed-browser.md#microsoft-edge-support).

## Week of February 25, 2019

### Device configuration

#### Intune PowerShell module <!-- 951068  -->
The Intune PowerShell module, which provides support for the Intune API through Microsoft Graph, is now available in the [Microsoft PowerShell Gallery](https://www.powershellgallery.com/packages/Microsoft.Graph.Intune/6.1902.1.10).

- [Details about how use this module](https://github.com/Microsoft/Intune-PowerShell-SDK/blob/master/README.md)
- [Scenario examples using this module](https://github.com/Microsoft/Intune-PowerShell-SDK/blob/master/Samples/README.md)

#### Improved support for delivery optimization  <!--3183757  -->
We've expanded the support in Intune for configuring delivery optimization. You can now configure an expanded list of [Delivery Optimization settings](delivery-optimization-settings.md) and target it to your devices right from Intune console.


## Week of February 18, 2019

### App management

#### Intune will leverage Google Play Protect APIs on Android devices <!-- 2577355   -->
Some IT admins are faced with a BYOD landscape where end users may end up rooting or jailbreaking their mobile phone. This behavior, while sometimes not ill-intentioned, results in a bypass of many Intune policies that are set in order to protect the organization's data on end-user devices. Thus, Intune provides root and jailbreak detection for both enrolled and unenrolled devices. With this release, Intune will now leverage Google Play Protect APIs to add to our existing root detection checks for unenrolled devices. While Google does not share the entirety of the root detection checks that occur, we expect these APIs to detect users who have rooted their devices for any reason from device customization to being able to get newer OS updates on older devices. These users can then be blocked from accessing corporate data, or their corporate accounts can be wiped from their policy enabled apps. For additional value, the IT admin will now have several reporting updates within the Intune App Protection blade - the "Flagged Users" report will show which users are detected via Google Play Protect's SafetyNet API scan, the "Potentially Harmful Apps" report will show which apps are detected via Google's Verify Apps API scanning. This feature is available on Android.

#### Win32 app information available in Troubleshooting blade <!-- 2617342   -->
You can now collect failure log files for a Win32 app installation from the Intune app **Troubleshooting** blade. For more information about app installation troubleshooting, see [Troubleshoot app installation issues](troubleshoot-app-install.md) and [Troubleshoot Win32 app issues](apps-win32-app-management.md#troubleshoot-win32-app-issues).

#### App status details for iOS apps <!-- 3761235   -->
There are new app installation error messages related to the following:
- Failure for VPP apps when installing on shared iPad
- Failure when app store is disabled
- Failure to find VPP license for app
- Failure to install system apps with MDM provider
- Failure to install apps when device is in lost mode or kiosk mode
- Failure to install app when user is not signed in to the App Store

In Intune, select **Client apps** > **Apps** > "App name" > **Device install status**. New error messages will be available in the **Status details** column.

#### New App categories screen in the Company Portal app for Windows 10<!-- 3834780  -->
A new screen called **App categories** has been added to improve the app browsing and selection experience in Company Portal for Windows 10. Users will now see their apps sorted under categories such as **Featured**, **Education**, and **Productivity**. This change appears in Company Portal versions 10.3.3451.0 and later. To view the new screen, see [What's new in the app UI](whats-new-app-ui.md). For more information about apps in the Company Portal, see [Install and share apps on your device](/intune-user-help/install-apps-cpapp-windows).  

#### Power BI Compliance app <!-- 1455231 doc-work-item -->
Access your Intune Data Warehouse in Power BI Online using the [Intune Compliance (Data Warehouse)](https://aka.ms/intune/datawarehouseapi/getpowerbiapp) app. With this Power BI app, you can now access and share pre-created reports without any setup and without leaving your web browser. For additional information, see [Change log - Power BI Compliance app](reports-changelog.md#power-bi-compliance-app).


### Device configuration

#### PowerShell scripts can run in a 64-bit host on 64-bit devices <!-- 1862675   -->
When you add a PowerShell script to a device configuration profile, the script always executes in 32-bit, even on 64-bit operating systems. With this update, an administrator can run the script in a 64-bit PowerShell host on 64-bit devices (**Device configuration** > **PowerShell scripts** > **Add** > **Configure** > **Run script in 64 bit PowerShell Host**).

For more details on using PowerShell, see [PowerShell scripts in Intune](intune-management-extension.md).

Applies to:
Windows 10 and later

#### macOS users are prompted to update their password <!-- 1873216 -->
Intune is enforcing the **ChangeAtNextAuth** setting on macOS devices. This setting impacts end-users and devices that have compliance password policies or device restriction password profiles. End users are prompted once to update their password. This prompt happens whenever a user first runs a task that requires authentication, such as signing in to the device. Users can also be prompted to update their password when doing anything that requires administrative privileges, such as requesting keychain access. 

Any new or existing password policy changes by the administrator prompt end users again to update their password.

Applies to:  
macOS

#### Assign SCEP certificates to a userless macOS device    <!-- 2340521    -->
You can assign Simple Certificate Enrollment Protocol (SCEP) certificates using device attributes to macOS devices, including devices without user affinity, and associate the certificate profile with Wi-Fi or VPN profiles. This expands the support we already have to [assign SCEP certificates to devices with and without user affinity](certificates-profile-scep.md) that run Windows, iOS, and Android.  This update adds the option to select a Certificate type of *Device* when you configure a SCEP certificate profile for the macOS.

Applies to: 
- macOS

#### Intune Conditional Access UI update   <!-- 2432313   -->
We've made improvements to the UI for Conditional Access in the Intune console. These include:
- Replaced the Intune *Conditional Access* blade with the blade from Azure Active Directory. This ensures you'll have access to the full range of settings and configurations for [Conditional Access](conditional-access.md) (which remains an Azure AD technology), from within the Intune console. 
- We've renamed the *On-premises access* blade to *Exchange access*, and relocated the *Exchange service connector* setup to this renamed blade.  This change consolidates where you [configure and monitor details related to Exchange online and on-premises](exchange-connector-install.md).  

#### Kiosk Browser and Microsoft Edge Browser apps can run on Windows 10 devices in kiosk mode <!-- 2935135   -->
You can use Windows 10 devices in kiosk mode to run one app, or many apps. This update includes several changes to using browser apps in kiosk mode, including:

- Add the Microsoft Edge Browser or Kiosk Browser to run as apps on the kiosk device (**Device configuration** > **Profiles** > **New profile** > **Windows 10 and later** for platform > **Kiosk** for profile type).
- New features and settings are available to allow or restrict (**Device configuration** > **Profiles** > **New profile** > **Windows 10 and later** for platform > **Device restrictions** for profile type), including:

- Microsoft Edge Browser:
  - Use Microsoft Edge kiosk mode
  - Refresh browser after idle time

- Favorites and search:
  - Allow changes to search engine

For a list of these settings, see:

- [Windows 10 and later device settings to run as a kiosk](kiosk-settings-windows.md)
- [Microsoft Edge Browser device restrictions](device-restrictions-windows-10.md#microsoft-edge-browser)
- [Favorites and search device restrictions](device-restrictions-windows-10.md##favorites-and-search)

Applies to:
Windows 10 and later

#### New device restriction settings for iOS and macOS devices <!-- 3448774   -->
You can restrict some settings and features on devices running iOS and macOS (**Device configuration** > **Profiles** > **New profile** > **iOS** or **macOS** for platform > **Device restrictions** for profile type). This update adds more features and settings you can control, including setting screen time, changing eSIM settings and cellular plans, and more on iOS devices. Also, delaying the user's visibility of software updates and blocking content caching on macOS devices. 

To see the features and settings you can restrict, see:

- [iOS device restriction settings](device-restrictions-ios.md)
- [macOS device restriction settings](device-restrictions-macos.md)

Applies to:

- iOS
- macOS

#### "Kiosk" devices are now called "Dedicated devices" on Android Enterprise devices <!-- 3598402   -->
To align with Android terminology, **kiosk** is changed to **dedicated devices** for Android enterprise devices (**Device configuration** > **Profiles** > **Create profile** > **Android enterprise for platform > **Device Owner Only** > **Device Restrictions** > **Dedicated devices**).

To see the available settings, go to [Device settings to allow or restrict features](device-restrictions-android-for-work.md#dedicated-device-settings).

Applies to:  
Android Enterprise

#### Safari and Delaying user software update visibility iOS settings are moving in the Intune UI <!-- 3640850, 3803313   -->
For iOS devices, you can set Safari settings and configure Software Updates. In this update, these settings are moving to different parts of the Intune UI:

- The Safari settings moved from **Safari** (**Device configuration** > **Profiles** > **New profile** > **iOS** for platform > **Device restrictions** for profile type) to **[Built-in Apps](device-restrictions-ios.md#built-in-apps)**.
- The **Delaying user software update visibility for supervised iOS devices** setting (**Software updates** > **Update policies for iOS**) is moving to **Device restrictions** > **[General](device-restrictions-ios.md#general)**.  For details on the impact to existing policies, see [iOS software updates](software-updates-ios.md#configure-the-policy). 

For a list of the settings, see:

- [iOS device restrictions](device-restrictions-ios.md) 
- [iOS software updates](software-updates-ios.md)

This feature applies to: 

- iOS

#### Enabling restrictions in the device settings is renamed to Screen Time on iOS devices <!-- 3699164   -->
You can configure the **Enabling restrictions in the device settings** on supervised iOS devices (**Device configuration** > **Profiles** > **New profile** > **iOS** for platform > **Device restrictions** for profile type > **General**). In this update, this setting is renamed to **Screen Time (supervised only)**. 

The behavior is the same. Specifically: 

- iOS 11.4.1 and earlier: **Block** prevents end users from setting their own restrictions in the device settings. 
- iOS 12.0 and later: **Block** prevents end users from setting their own **Screen Time** in the device settings, including content & privacy restrictions. Devices upgraded to iOS 12.0 won't see the restrictions tab in the device settings anymore. These settings are in **Screen Time**. 

For a list of the settings, see [iOS device restrictions](device-restrictions-ios.md#general).

Applies to: 
- iOS


### Device management

#### Rename an enrolled Windows device <!-- 1911112  -->
You can now rename an enrolled Windows 10 device (RS4 or later). To do, choose **Intune** > **Devices** > **All devices** > choose a device > **Rename device**. This feature does not currently support renaming hybrid Azure AD Windows devices.

#### Auto-assign scope tags to resources created by an admin with that scope <!-- 3173823  -->
When an admin creates a resource, any scope tags assigned to the admin will automatically be assigned to those new resources.

### Monitor and troubleshoot

#### Failed enrollment report moves to the Device Enrollment blade <!-- 3560202  -->
The **Failed enrollments** report has been moved to the **Monitor** section of the **Device enrollment** blade. Two new columns (Enrollment Method and OS Version) have been added.

#### Company Portal abandonment report renamed to Incomplete user enrollments <!--3815076 eemiss -->
The **Company Portal abandonment** report has been renamed to **Incomplete user enrollments**.


<!-- ########################## -->
## Week of February 4, 2019

### App management

#### Intune macOS Company Portal Dark Mode <!-- 3300524  -->
The Intune macOS Company Portal now supports Dark Mode for macOS. When you enable Dark Mode on a macOS 10.14+ device, the Company Portal will adjust its appearance to colors that reflect that mode.

<!-- ########################## -->
## Week of January 21, 2019

### App management

#### Toast notifications for Win32 apps <!-- 3136566   -->
You can suppress showing end-user toast notifications per app assignment. From Intune, select **Client apps** > **Apps** > select the app > **Assignments** > **Include Groups**. 

#### Intune app protection policies UI update <!-- 3251427  -->
We’ve changed the labels for settings and buttons for Intune app protection to make each easier to understand. Some of the changes include:  
- Controls are changed from **yes** / **no** controls to primarily **block** / **allow** and **disable** / **enable** controls. The labels are also updated.  
- Settings are reformatted, so the setting and its label are side-by-side in the control, to provide better navigation.   

The default settings and number of settings remain the same, but this change allows the user to understand, navigate, and utilize the settings more easily to apply selected app protection policies. For information, see [iOS settings](app-protection-policy-settings-ios.md) and [Android settings](app-protection-policy-settings-android.md).

### Additional settings for Outlook <!-- 3301182  -->
You can now configure the following additional settings for Outlook for iOS and Android using Intune:

- Only allow work or school accounts to be used in Outlook in iOS and Android
- Deploy modern authentication for Office 365 and hybrid modern authentication on-premises accounts
- Use `SAMAccountName` for the username field in the email profile when basic authentication is selected
- Allow contacts to be saved
- Configure external recipients MailTips
- Configure **Focused Inbox**
- Require biometrics to access Outlook for iOS
- Block external images

> [!NOTE]
> If you are using Intune App Protection policies to manage access for corporate identities, you should consider not enabling **require biometrics**. For more information, see **Require corporate credentials for access** for [iOS Access Settings](app-protection-policy-settings-ios.md#access-requirements) and [Android Access Settings](app-protection-policy-settings-android.md#access-requirements).

For more information, see [Microsoft Outlook configuration settings](app-configuration-policies-outlook.md).

#### Delete Android Enterprise apps <!-- 1352553 -->
You can delete managed Google Play apps from Microsoft Intune. To delete a managed Google Play app, open Microsoft Intune in the Azure portal and select **Client apps** > **Apps**. From the app list, select the ellipses (...) to the right of the managed Google Play app, then select **Delete** from the displayed list. When you delete a managed Google Play app from the app list, the managed Google Play app is automatically unapproved.

#### Managed Google Play app type <!-- 1352580 -->
The **managed Google Play** app type will allow you to specifically add [managed Google Play apps](https://play.google.com/work/search?q=microsoft&c=apps) to Intune. As the Intune admin, you can now browse, search, approve, sync and assign approved managed Google Play apps within Intune.  You no longer need to browse to the managed Google Play console separately, and you no longer have to reauthenticate.  In Intune, select **Client apps** > **Apps** > **Add**. In the **App type** list, select **Managed Google Play** as the app type.

### Default Android PIN keyboard <!-- 3802457 -->
For end users who have set an Intune App Protection Policy (APP) PIN on their Android devices with PIN type of 'Numeric', they will now see the default Android keyboard instead of the fixed Android keyboard UI that was previously designed. This change was made to be consistent when using default keyboards on both Android and iOS, for both PIN types of 'Numeric' and/or 'Passcode'. For more information about end user Access settings on Android, such as APP PIN, see [Android access requirements](app-protection-policy-settings-android.md#access-requirements).

### Device configuration

#### Use Microsoft-recommended settings with Security Baselines (Public Preview) <!-- 2055484   -->

Intune integrates with other services that focus on security, including Windows Defender ATP and Office 365 ATP. Customers are asking for a common strategy and a cohesive set of end-to-end security workflows across the Microsoft 365 services. Our goal is to align strategies to build solutions that bridge security operations and common administrator tasks. 
In Intune, we aim to accomplish this goal by publishing a set of Microsoft recommended “Security baselines” (**Intune** > **Security baselines**).  An administrator can create security policies directly from these baselines, and then deploy them to their users. You can also customize the best practice recommendations to meet the needs of your organization. Intune makes sure that devices stay in compliance with these baselines, and notifies administrators of users or devices that aren't in compliance.

This feature is in public preview so any profiles created now will not move over to Security Baselines templates that are generally available (GA). You shouldn’t plan to use these preview templates in your production environment.

To learn more about security baselines, see [Create a Windows 10 security baseline in Intune](security-baselines-monitor.md).

This feature applies to:
Windows 10 and later

#### Non-Administrators can enable BitLocker on Windows 10 devices joined to Azure AD<!-- 2147379   -->
When you enable BitLocker settings on Windows 10 devices (**Device configuration** > **Profiles** > **Create profile** > **Windows 10 and later** for platform > **Endpoint protection** for profile type > **Windows Encryption**), you add BitLocker settings. 

This update includes a new BitLocker setting to allow standard users (non-administrators) to enable encryption. 

To see the settings, go to [Endpoint protection settings for Windows 10](endpoint-protection-windows-10.md#windows-encryption).

#### Check for Configuration Manager compliance <!-- 2192052  eepublished  -->
This update includes a new System Center Configuration Manager compliance setting (**Device compliance** > **Policies** > **Create policy** > **Windows 10 and later** > **Configuration Manager Compliance**). Configuration Manager sends signals to Intune compliance. Using this setting, you can require all Configuration Manager signals to return "compliant".

For example, you require all software updates to be installed on devices. In Configuration Manager, this requirement has the “Installed” state. If any programs on the device are in unknown state, then the device is non-compliant in Intune.

[Configuration Manager Compliance](compliance-policy-create-windows.md#configuration-manager-compliance) describes this setting.

Applies to: 
Windows 10 and later

#### Customize wallpaper on supervised iOS devices using a device configuration profile <!-- 2809324   -->
When you create a device configuration profile for iOS devices, you can customize some features (**Device configuration** > **Profiles** > **Create profile** > **iOS** for platform > **Device features** for profile type). This update includes new **Wallpaper** settings that allow an Administrator to use a .png, .jpg, or .jpeg image on the home screen or lock screen. These wallpaper settings apply only to supervised devices. 

For a list of these settings, see [iOS device feature settings](ios-device-features-settings.md).

#### Windows 10 kiosk is generally available <!-- 3594661  -->
In this update, the Kiosk feature on Windows 10 and later devices is generally available (GA). To see all the settings you can add and configure, see [Kiosk settings for Windows 10 (and later)](kiosk-settings.md).

#### Contact Sharing via Bluetooth is removed in Device Restrictions > Device Owner for Android Enterprise <!-- 3598396   -->
When you create a device restrictions profile for Android Enterprise devices, there is a **Contact Sharing via Bluetooth** setting. In this update, the **Contact Sharing via Bluetooth** setting is removed (**Device configuration** > **Profiles** > **Create profile** > **Android Enterprise** for platform > **Device Restrictions > Device owner** for profile type > **General**). 

The **Contact Sharing via Bluetooth** setting isn't supported for Android Enterprise Device Owner management. So when this setting is removed, it won't impact any devices or tenants, even if this setting is enabled and configured in your environment.

To see the current list of settings, go to [Android Enterprise device settings to allow or restrict features](device-restrictions-android-for-work.md).

Applies to: Android Enterprise Device Owner

### Device management

#### Selective wipe support for WIP Without Enrollment devices <!-- 1434452 -->
Windows Information Protection Without Enrollment (WIP-WE) allows customers to protect their corporate data on Windows 10 devices without the need for full MDM enrollment. Once documents are protected with a WIP-WE policy, the protected data can be selectively wiped by an Intune administrator. By selecting the user and device, and sending a wipe request, all data that was protected via the WIP-WE policy will become unusable. From the Intune in the Azure portal, select **Mobile app** > **App selective wipe**.

### Monitor and troubleshoot

#### New operational logs, and ability to send logs to Azure Monitor services <!-- 3762211  -->
Intune has built-in audit logging that tracks events as changes are made. This update includes new logging features, including: 
- Operational logs (preview) that show details on users and devices that enrolled, including success and failed attempts.
- The audit logs and operational logs can be sent to Azure Monitor, including storage accounts, event hubs, and log analytics. These services allow you to store, use analytics such as Splunk and QRadar, and get visualizations of your logging data.

[Send log data to storage, event hubs, or log analytics in Intune](review-logs-using-azure-monitor.md) provides more information on this feature.

### Skip more Setup Assistant screens on an iOS DEP device <!-- 2687509  -->
In addition to the screens you can currently skip, you can set iOS DEP devices to skip the following screens in the Setup Assistant when a user enrolls the device: Display Tone, Privacy, Android Migration, Home Button, iMessage & FaceTime, Onboarding, Watch Migration, Appearance, Screen Time, Software Update, SIM Setup.
To choose which screens to skip, go to **Device enrollment** > **Apple enrollment** > **Enrollment program tokens** > choose a token > **Profiles** > choose a profile > **Properties** > **Setup Assistant customization** > choose **Hide** for any screens that you want to skip > **OK**.
If you create a new profile or edit a profile, the selected skip screens need to sync with the Apple MDM server. Users can issue a manual sync of the devices so that there is no delay in picking up the profile changes.

#### Android Enterprise APP-WE app deployment <!-- 1171203 -->
For Android devices in a non-enrolled App Protection Policy Without Enrollment (APP-WE) deployment scenario, you can now use managed Google Play to deploy store apps and LOB apps to users. Specifically, you can provide end users with an app catalog and installation experience that no longer requires end users to loosen the security posture of their devices by allowing installations from unknown sources. In addition, this deployment scenario will provide an improved end user experience.

<!-- ########################## -->
## Week of January 14, 2019

### Preview of support for Android corporate-owned, fully managed devices <!-- 1574342  -->
Intune now supports fully managed Android devices, a corporate-owned "device owner" scenario where devices are tightly managed by IT and are affiliated with individual users. This allows admins to manage the entire device, enforce an extended range of policy controls unavailable to work profiles, and restricts users to installing apps from managed Google Play only. For more information, see [Set up Intune enrollment of Android fully managed devices](android-fully-managed-enroll.md) and [Enroll your dedicated devices or fully managed devices](android-dedicated-devices-fully-managed-enroll.md).  Please note that this feature is in preview. Some Intune capabilities, such as certificates, compliance, and Conditional Access, are not currently available with Android fully managed user devices.

<!-- ########################## -->
## Week of January 7, 2019

### App management

#### Intune app PIN <!-- 2298397 -->
As the IT admin, you can now configure the number of days an end user can wait until their Intune app PIN must be changed. The new setting is *PIN reset after number of days* and is available in the Azure portal by selecting **Intune** > **Client apps** > **App protection policies** > **Create Policy** > **Settings** > **Access requirements**. Available for [iOS](app-protection-policy-settings-ios.md) and [Android](app-protection-policy-settings-android.md) devices, this feature supports a positive integer value.


#### Intune device reporting fields <!-- 2748738 -->
Intune provides additional device reporting fields, including App Registration ID, Android manufacturer, model, and security patch version, as well as iOS model. In Intune, these fields are available by selecting **Client apps** > **App protection status** and choosing **App Protection Report: iOS, Android**. In addition, these parameters will help you configure the **Allow** list for device manufacturer (Android), the **Allow** list for device model (Android and iOS), and the minimum Android security patch version setting. 


### Device configuration

#### Administrative templates are in public preview, and moved to their own configuration profile <!-- 3322847 -->

Administrative templates in Intune (**Device configuration** > **Administrative templates**) are currently in public preview. With this update:

- Administrative templates include about 300 settings that can be managed in Intune. Previously, these settings only existed in the group policy editor.
- Administrative templates are available in public preview.
- Administrative templates are moving from **Device configuration** > **Administrative templates** to **Device configuration** > **Profiles** > **Create profile** > in **Platform**, choose **Windows 10 and later** > in **Profile type**, choose **Administrative templates**.
- Reporting is enabled

To read more about this feature, go to [Windows 10 templates to configure group policy settings](administrative-templates-windows.md).

Applies to: Windows 10 and later

#### Use S/MIME to encrypt and sign multiple devices for a user  <!-- 1333642 -->
This update includes S/MIME email encryption using a new imported certificate profile (**Device configuration** > **Profiles** > **Create profile** > select the platform > **PKCS imported certificate** profile type). In Intune, you can import certificates in PFX format. Intune can then deliver those same certificates to multiple devices enrolled by a single user. This also includes:
- The native iOS email profile supports enabling S/MIME encryption using imported certificates in PFX format.
- The native mail app on Windows Phone 10 devices automatically uses the S/MIME certificate.
- The private certificates can be delivered across multiple platforms. But, not all email apps support S/MIME.
- On other platforms, you may need to manually configure the mail app to enable S/MIME.  
- Email apps that support S/MIME encryption may handle retrieving certificates for S/MIME email encryption in a way that an MDM cannot support, such as reading from their publisher's certificate store.
For more information on this feature, see [S/MIME overview to sign and encrypt email](certificates-s-mime-encryption-sign.md).
Supported on: Windows, Windows Phone 10, macOS, iOS, Android

#### New options to automatically connect and persist rules when using DNS settings on Windows 10 and later devices <!-- 1333665, 2999078 -->
On Windows 10 and later devices, you can create a VPN configuration profile that includes a list of DNS servers to resolve domains, such as contoso.com. This update includes new settings for name resolution (**Device configuration** > **Profiles** > **Create profile** > Choose **Windows 10 and later** for platform > Choose **VPN** for profile type > **DNS settings** >**Add**): 
- **Automatically connect**: When **Enabled**, the device automatically connects to the VPN when a device contacts a domain you enter, such as contoso.com.
- **Persistent**: By default, all Name Resolution Policy table (NRPT) rules are active as long as the device is connected using this VPN profile. When this setting is **Enabled** on an NRPT rule, the rule remains active on the device, even when the VPN disconnects. The rule stays until the VPN profile is removed or until the rule is manually removed, which can be done using PowerShell.
[Windows 10 VPN settings](vpn-settings-windows-10.md) describes the settings. 

#### Use trusted network detection for VPN profiles on Windows 10 devices <!-- 1500165 -->
When using trusted network detection, you can prevent VPN profiles from automatically creating a VPN connection when the user is already on a trusted network. With this update, you can add DNS suffixes to enable trusted network detection on devices running Windows 10 and later (**Device configuration** > **Profiles** > **Create profile** > **Windows 10 and later** for platform > **VPN** for profile type).
[Windows 10 VPN settings](vpn-settings-windows-10.md) lists the current VPN settings.

#### Manage Windows Holographic for Business devices used by multiple users <!-- 1907917, 1063203 -->
Currently, you can configure shared PC settings on Windows 10 and Windows Holographic for Business devices using a custom OMA-URI setting. With this update, a new profile is added to configure shared device settings (**Device configuration** > **Profiles** > **Create Profile** > **Windows 10 and later** > **Shared multi-user device**).
To learn more about this feature, go to [Intune settings to manage shared devices](shared-user-device-settings.md).
Applies to: Windows 10 and later, Windows Holographic for Business

#### New Windows 10 Update settings <!--2626030  2512994  -->
For your [Windows 10 Update Rings](windows-update-for-business-configure.md), you can configure:
- **Automatic update behavior** - Use a new option, *Reset to default* to restore the original auto update settings on a Windows 10 machine on machines running the *October 2018 Update*
- **Block user from pausing Windows updates** - Configure a new Software updates setting that lets you block or allow your users to pause update installation from the *Settings* of their machines. 

#### iOS email profiles can use S/MIME signing and encryption <!-- 2662949 -->
You can create an email profile that includes different settings. This update includes S/MIME settings that can be used for signing and encrypting email communications on iOS devices (**Device configuration** > **Profiles** > **Create profile** > Choose **iOS** for platform > **Email** for profile type).
[iOS email configuration settings](email-settings-ios.md) lists the settings.

#### Some BitLocker settings support Windows 10 Pro edition<!-- 2727036 -->
You can create a configuration profile that sets endpoint protection settings on Windows 10 devices, including BitLocker. This update adds support for Windows 10 Professional edition for some BitLocker settings. 
To see these protection settings, go to [Endpoint protection settings for Windows 10](endpoint-protection-windows-10.md#windows-encryption).

#### Shared device configuration is renamed to Lock Screen Message for iOS devices in the Azure portal<!-- 2809362 -->
When you create a configuration profile for iOS devices, you can add **Shared Device Configuration** settings to show specific text on the lock screen. This update includes the following changes: 
- The **Shared Device Configuration** settings in the Azure portal are renamed to "Lock Screen Message (supervised only)" (**Device configuration** > **Profiles** > **Create profile** > Choose **iOS** for platform > Choose **Device features** for profile type > **Lock Screen Message**).
- When adding lock screen messages, you can insert a serial number, a device name, or another device-specific value as a variable in **Asset tag information** and **Lock screen footnote**. For example, you can enter `Device name: {{devicename}}` or `Serial number is {{serialnumber}}` using curly brackets. [iOS tokens](app-configuration-policies-use-ios.md#tokens-used-in-the-property-list) lists the available tokens that can be used.
[Settings to display messages on the lock screen](shared-device-settings-ios.md) lists the settings.

#### New App Store, Doc Viewing, Gaming device restriction settings added to iOS devices <!-- 2827760-->
In **Device Configuration** > **Profiles** > **Create profile** > **iOS** for platform > **Device restrictions** for profile type > **App Store, Doc Viewing, Gaming**, the following settings are added: 
Allow managed apps to write contacts to unmanaged contacts accounts 
Allow unmanaged apps to read from managed contacts accounts 
To see these settings, go to [iOS device restrictions](device-restrictions-ios.md#app-store-doc-viewing-gaming).

#### New notification, hints, and keyguard settings to Android Enterprise device owner devices <!-- 3201839 3201843 -->
This update includes several new features on Android Enterprise devices when running as device owner. To use these features, go to **Device Configuration** > **Profiles** > **Create profile** > In **Platform**, choose **Android Enterprise** > In **Profile type**, choose **Device owner only** > **Device Restrictions**.

New features include: 

- Disable system notifications from showing, including incoming calls, system alerts, system errors, and more.
- Suggests skip starting tutorials and hints for apps that are opened the first time.
- Disable advanced keyguard settings, such as the camera, notifications, fingerprint unlock, and more.


To see the settings, go to [Android Enterprise device restriction settings](device-restrictions-android-for-work.md).

#### Android enterprise device owner devices can use Always On VPN connections <!-- 3202194 -->
In this update, you can use Always-on VPN connections on Android enterprise device owner devices. Always-on VPN connections stay connected, or immediately reconnect when the user unlocks their device, when the device restarts, or when the wireless network changes. You can also put the connection in "lockdown" mode, which blocks all network traffic until the VPN connection is active.
You can enable Always-on VPN in **Device configuration** > **Profiles** > **Create profile** > **Android enterprise** for platform > **Device restrictions** for Device Owner Only > **Connectivity** settings. 
To see the settings, go to [Android Enterprise device restriction settings](device-restrictions-android-for-work.md).

#### New setting to end processes in Task manager on Windows 10 devices <!-- 3285177 --> 
This update includes a new setting to end processes using Task Manager on Windows 10 devices. Using a device configuration profile (**Device configuration** > **Profiles** > **Create profile** > In **Platform**, choose **Windows 10** > In **Profile type**, choose **Device restrictions** > **General** settings), you choose to allow or prevent this setting.
To see these settings, go to [Windows 10 device restriction settings](device-restrictions-windows-10.md).
Applies to: Windows 10 and later


### Device enrollment

#### More detailed enrollment restriction failure messaging <!-- 3111564 -->
More detailed error messages are available when enrollment restrictions are not met. To see these messages, go to **Intune** > **Troubleshoot** > and check the Enrollment Failures table. For more information, see the [enrollment failures list](help-desk-operators.md#enrollment-failure-reference).

### Monitor and troubleshoot

#### Tenant Status dashboard  <!-- 1124854 -->
The new [Tenant Status page](tenant-status.md) provides a single location where you can view status and related details for your tenant.  The dashboard is divided into four areas:
- **Tenant Details** - Displays information that includes your Tenant name and location, your MDM Authority, the total enrolled devices in your tenant, and your license counts. This section also lists the current service release for your tenant.
- **Connector Status** - Displays information about available connectors you have configured and can also list those which you have not yet enabled.  
   Based on the current state of each connector,  they are flagged as Healthy, Warning, or Unhealthy. Select a connector to drill through and view details or configure additional information for it.
- **Intune Service Health** - Displays details about active incidents or outages for your tenant. The information in this section is retrieved directly from the Office Message Center.
- **Intune News** - Displays active messages for your tenant. Messages include things like notifications when your tenant receives the latest Intune features.  The information in this section is retrieved directly from the Office Message Center.

#### New help and support experience in Company Portal for Windows 10 <!-- 1488939-->
The new Company Portal Help & support page helps users troubleshoot and request help for app and access problems. From the new page, they can email error and diagnostic log details and find their organization's Helpdesk details. They'll also find a FAQ section with links to the relevant Intune documentation. 

#### New Help and Support experience for Intune   <!-- #3307080 -->
We are rolling out the new Help and Support experience to all tenants over the next few days. This new experience is available for Intune and can be accessed when using the Intune blades in the [Azure portal](https://portal.azure.com/).
The new experience lets you describe your problem in your own words and receive troubleshooting insight and web-based remediation content. These solutions are offered via a rule-based machine learning algorithm, driven by user inquires. 
In addition to issue-specific guidance, you use the new case creation workflow to open a support case by email or phone. 
This new experience replaces the previous Help and Support experience of a static set of pre-selected options that are based on the area of the console you are in when you open Help and Support. 
For more information, see [How to get support for Microsoft Intune](get-support.md).

### Role-based access control

#### Scope tags for apps <!-- 1081941 -->
You can create scope tags to limit access for roles and apps. You can add a scope tag to an app so that only people with roles also assigned that scope tag have access to the app. Currently, apps added to Intune from managed Google Play or apps purchased using Apple Volume Purchase Program (VPP) can't be assigned scope tags (future support is planned). For more information, see [Use scope tags to filter policies](scope-tags.md).

## Notices

[!INCLUDE [Intune notices](./includes/intune-notices.md)]
