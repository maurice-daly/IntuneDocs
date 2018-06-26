---
# required metadata

title: Manage iOS volume-purchased apps in Microsoft Intune
titlesuffix: 
description: Learn about how you can sync apps you purchased in volume from the iOS store into Microsoft Intune and then manage and track their usage.
keywords:
author: Erikre
ms.author: erikre
manager: dougeby
ms.date: 05/15/2018
ms.topic: article
ms.prod:
ms.service: microsoft-intune
ms.technology:
ms.assetid: 51d45ce2-d81b-4584-8bc4-568c8c62653d

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: mghadial
ms.suite: ems
#ms.tgt_pltfrm:
ms.custom: intune-azure
---

# How to manage iOS apps purchased through a volume-purchase program with Microsoft Intune


[!INCLUDE [azure_portal](./includes/azure_portal.md)]

The iOS app store lets you purchase multiple licenses for an app that you want to run in your company. Purchasing multiple copies helps you to efficiently manage apps in your company.

Microsoft Intune helps you manage multiple copies of apps purchased through this program by:

- Reporting license information from the app store.
- Tracking how many of the licenses you have used.
- Helping you to not install more copies of the app than you own.

There are two methods you can use to assign volume-purchased apps:

### Device licensing

When you assign an app to devices, one app license is used, and remains associated with the device to which you assigned it.

When you assign volume-purchased apps to a device, the end user of the device does not have to supply an Apple ID to access the store.

### User licensing

When you assign an app to a user, one app license is used for and is associated with the user. The app can be run on multiple devices that the user owns (with a limit controlled by Apple).

When you assign a volume-purchased app to users, each end user must have a valid and unique Apple ID in order to access the app store.

Additionally, you can synchronize, manage, and assign books you purchased from the Apple volume-purchase program (VPP) store with Intune. For more information, see [How to manage iOS eBooks you purchased through a volume-purchase program](vpp-ebooks-ios.md).

## Manage volume-purchased apps for iOS devices

### Supports Apple Volume Purchase Program volume-purchased apps for iOS devices

Purchase multiple licenses for iOS apps through the [Apple Volume Purchase Program for Business](http://www.apple.com/business/vpp/) or the [Apple Volume Purchase Program for Education](http://volume.itunes.apple.com/us/store). This process involves setting up an Apple VPP account from the Apple website and uploading the Apple VPP token to Intune.  You can then synchronize your volume purchase information with Intune and track your volume-purchased app use.

### Supports Business-to-Business volume-purchased apps for iOS devices

In addition, third-party developers can also privately distribute apps to authorized Volume Purchase Program for Business members specified in iTunes Connect. These VPP for Business members can sign in to the Volume Purchase Program App Store and purchase their apps. VPP for Business apps purchased by the end user will sync to their Intune tenants.

## Before you start
Before you start, you need to get a VPP token from Apple and upload it to your Intune account. Additionally, you should understand the following criteria:

* You can associate multiple VPP tokens with your Intune account.
* If you previously used a VPP token with a different product, you must generate a new one to use with Intune.
* Each token is valid for one year.
* By default, Intune syncs with the Apple VPP service twice a day. You can start a manual sync at any time.
* Before you start to use Apple VPP with Intune, remove any existing VPP user accounts created with other mobile device management (MDM) vendors. Intune does not synchronize those user accounts into Intune as a security measure. Intune only synchronizes data from the Apple VPP service that Intune created.
* Intune supports adding up to 256 VPP tokens.
* Apple's Device Enrollment Profile (DEP) program automates mobile device management (MDM) enrollment. Using DEP, you can configure enterprise devices without touching them. You can enroll in the DEP program using the same program agent account that you used with Apple's VPP. The Apple Deployment Program ID is unique to programs listed under the [Apple Deployment Programs](https://deploy.apple.com) website and cannot be used to log in to Apple services such as the iTunes store.
* When you assign VPP apps using the user licensing model to users or devices (with user affinity), each Intune user needs to be associated with a unique Apple ID or an email address when they accept the Apple terms and conditions on their device. Ensure that when you set up a device for a new Intune user, you configure it with that user's unique Apple ID or email address. The Apple ID or email address and Intune user form a unique pair and can be used on up to five devices.
* A VPP token is only supported for use on one Intune account at a time. Do not reuse the same VPP token for multiple Intune tenants.

>[!IMPORTANT]
>After you have imported the VPP token to Intune, do not import the same token to any other device management solution. Doing so might result in the loss of license assignment and user records.

## To get and upload an Apple VPP token

1. Sign into the [Azure portal](https://portal.azure.com).
2. Choose **All services** > **Intune**. Intune is located in the **Monitoring + Management** section.
1.	On the **Intune** pane, choose **Mobile apps** > **iOS VPP tokens** under **Setup**.
2.  On the list of VPP tokens pane, select **Create**.
4. On the **Create VPP token** pane, specify the following information:
	- **VPP token file** - If you haven't already, sign up for the Volume Purchase Program for Business or the program for Education. After you sign up, download the Apple VPP token for your account and select it here.
	- **Apple ID** - Enter the Apple ID of the account associated with the volume-purchase program.
	- **Country/Region** - Select the VPP country store.  Intune synchronizes VPP apps for all locales from the specified VPP country store.
	    > [!WARNING]  
	    > Changing the country will update the apps metadata and store URL on next sync with the Apple service for apps created with this token. The app will not be updated if it does not exist in the new country store.

	- **Type of VPP account** - Choose from **Business** or **Education**.
	- **Automatic app updates** - Choose from **On** to **Off** to enable automatic updates. When enabled, Intune updates all apps purchased for the specified token through the Intune service when the device checks-in.
detect the VPP app updates inside the app store and automatically push them to the device when the device checks-in.
4. When you are done, select **Create**.

The token is displayed in the list of tokens pane.

You can synchronize the data held by Apple with Intune at any time by choosing **Sync now**.

## To assign a volume-purchased app

1.	On the **Intune** pane, choose **Mobile apps** > **Apps** under **Manage**.
2.	On the list of apps pane, choose the app you want to assign, and then choose **Assignments**.
3.	On the ***App name*** - **Assignments** pane, choose **Add group** then, on the **Add group** pane, choose an **Assignment type** and choose the Azure AD user or device groups to which you want to assign the app.
5.	For each group you selected, choose the following settings:
	- **Type** - Choose whether the app will be **Available** (end users can install the app from the Company Portal), or **Required** (end user devices will automatically get the app installed).
	- **License type** - Choose from **User licensing**, or **Device licensing**.
6.	Once you are done, choose **Save**.


>[!NOTE]
>The list of apps displayed is associated with a token. If you have an app that is associated with multiple VPP tokens, you see the same app being displayed multiple times; once for each token.

## End-User Prompts for VPP

The end-user will receive prompts for VPP app installation in a number of scenarios. The following table explains each condition:

| # | Scenario                                | Invite to Apple VPP program                              | App install prompt | Prompt for Apple ID |
|---|--------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------|-----------------------------------|
| 1 | BYOD – user licensed                             | Y                                                                                               | Y                                           | Y                                 |
| 2 | Corp – user licensed (not supervised device)     | Y                                                                                               | Y                                           | Y                                 |
| 3 | Corp – user licensed (supervised device)         | Y                                                                                               | N                                           | Y                                 |
| 4 | BYOD – device licensed                           | N                                                                                               | Y                                           | N                                 |
| 5 | CORP – device licensed (not supervised device)                           | N                                                                                               | Y                                           | N                                 |
| 6 | CORP – device licensed (supervised device)                           | N                                                                                               | N                                           | N                                 |
| 7 | Kiosk mode (supervised device) – device licensed | N                                                                                               | N                                           | N                                 |
| 8 | Kiosk mode (supervised device) – user licensed   | --- | ---                                          | ---                                |

> [!Note]  
> It is not recommended to assign VPP apps to Kiosk-mode devices using the VPP user licensing.

## Revoking app licenses and deleting tokens 

<!-- 820863 -->  
For a given device that has one or more iOS volume-purchase program (VPP) apps, you revoke all associated device-based app licenses for the device. Revoking an app license will not uninstall the related VPP app from the device. To uninstall a VPP app and reclaim a license, you must change the assignment type of the VPP app to **Uninstall**. If you remove an app that was assigned to a user, Intune reclaims the user or device license and uninstallS the app from the device.

>[!NOTE]
>Intune will retrieve all user licensed iOS VPP apps licenses when an employee leaves the company and is no longer part of the AAD groups.

<!-- 820879 -->  
You can delete an iOS Volume Purchasing Program (VPP) token using the console. This may be necessary when you have duplicate instances of a VPP token. Deleting a token will also delete any associated apps and assignment. However, deleting a token does not revoke app licenses or uninstall apps. 

>[!NOTE]
>Intune cannot revoke app licenses after a token has been deleted. 

<!-- 820870 -->  
To revoke the license of all VPP apps for a given VPP token, you must first revoke all app licenses associated with the token, then delete the token.

## Further information

When a user with an eligible device first tries to install a VPP app to a device, they are asked to join the Apple Volume Purchase program. They must join before the app installation proceeds. The invitation to join the Apple Volume Purchase program requires that the user can use the iTunes app on the iOS device. If you have set a policy to disable the iTunes Store app, user-based licensing for VPP apps does not work. The solution is to either allow the iTunes app by removing the policy, or use device-based licensing.

## Frequently asked questions

#### How long does the portal take to update the license count once an app is installed or removed from the device?
The license should be updated within a few hours after installing or uninstalling an app. Note that if the end user removes the app from the device, the license is still assigned to that user or device.

#### Is it possible to oversubscribe an app and, if so, in what circumstance?
Yes. The Intune admin can oversubscribe an app. For example, if the admin purchases 100 licenses for app XYZ, and then targets the app to a group with 500 members in it. The first 100 members (users or devices) will get the license assigned to them, the rest of the members will fail on license assignment.

#### I understand Intune automatically syncs app licenses each day with Apple, is that correct?
Intune syncs app licenses twice a day with Apple.

## Next steps

See [How to monitor apps](apps-monitor.md) for information to help you monitor app assignments.
