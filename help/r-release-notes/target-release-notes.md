---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: Release notes that provide information about features, enhancements, and fixes for the latest or upcoming DNL Adobe Target releases.
title: Adobe Target prerelease notes
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
---

# Target release notes (prerelease){#target-release-notes-prerelease}

This article contains prerelease information. Release dates, features, and other information are subject to change without notice. 

**Last Updated: June 24, 2020**

To view information about the current release, see [Target Release Notes](release-notes.md). The information on these pages might be the same, depending on the timing of releases. The issue numbers in parentheses are for internal [!DNL Adobe] use.

>[!NOTE]
>
>* **mbox.js deprecation**: On August 30, 2020, Adobe Target will no longer support the mbox.js library. Post August 30, 2020, all calls made from mbox.js will fail and impact your pages that have Target activities running. We recommend that all customers migrate to the most recent version of the at.js library before this date to avoid any potential issues with your sites. For more information, see [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) and [Adobe Target Skill Builder: Developer chat, migrate Adobe Target's mbox.js to at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
>
>   Although, mbox.js is currently supported, we have not provided feature updates to this library since July 2017. The newer at.js provides many advantages over mbox.js. Among other benefits, at.js improves page load times for web implementations, improves security, and provides better implementation options for single page applications.
>
>   By moving all customers to at.js, our engineers and support staff will be able to provide you with new functionality and offer the support you have come to expect from Adobe.
>
>* **Target Announcements**: See the Target announcements page for information about upcoming events, including Target Skill Builder sessions, developer chats, webinars, and Target Coffee Break sessions. For more information, see [Target announcements](/help/r-release-notes/target-announcements.md).

## Target Standard/Premium 20.7.1 (July 21, 2020)

This release includes the following enhancements:

### Analytics for Target (A4T) support for [!UICONTROL Auto-Target] activities

[!UICONTROL Auto-Target] activities now support [Analytics for Target](/help/c-integrating-target-with-mac/a4t/a4t.md).

This integration uses advanced machine learning to select from multiple high-performing marketer-defined experiences to personalize content and drive conversions. Auto-Target serves the most tailored experience to each visitor based on his or her individual customer profile and the behavior of previous visitors with similar profiles.

If you’ve already [implemented A4T](/help/c-integrating-target-with-mac/a4t/a4timplementation.md) for use with A/B Test activities, you’re all set!

### [!UICONTROL Administration] section UI refresh

We are gradually rewriting the entire [!DNL Target] UI using a new tech stack to be able to offer improved performance, reduce the maintenance time required when releasing new features, and to improve the user experience across the product. The first section refreshed is the [!UICONTROL Setup] section, which has been renamed [!UICONTROL Administration].

As part of this refresh, you will be able to easily perform many actions using the pages in the [!UICONTROL Administration] section, such as:

* Download the latest at.js file from the [!UICONTROL Implementation] tab (**[!UICONTROL Administration]** > **[!UICONTROL Implementation]**).
* Customize your at.js settings and be able to easily review your changes (**[!UICONTROL Administration]** > **[!UICONTROL Implementation]**).
* Modify enhanced reporting settings, such as the default currency and time zone, IPs to exclude from reporting, etc. (**[!UICONTROL Administration]** > **[!UICONTROL Reporting]**)
* Obfuscate visitor IP addresses for privacy reasons (**[!UICONTROL Administration]** > **[!UICONTROL Implementation]**)
* View the existing list of users per workspace and their roles, before managing them in Adobe Admin Console (**[!UICONTROL Administration]** > **[!UICONTROL Users]**).
* Search and filter all tables in the [!UICONTROL Administration] section.

## Prerelease information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63} 

To receive advance notifications about upcoming product enhancements to Target and other Adobe Experience Cloud solutions, sign up for the Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) 
