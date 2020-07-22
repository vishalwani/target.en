---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates
description: These release notes provide information about features, enhancements, fixes, and known issues for each Adobe Target Standard and Target Premium release.
title: Adobe Target release notes (current) 
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
---

# Target release notes (current){#target-release-notes-current}

These release notes provide information about features, enhancements, and fixes for each Target Standard and Target Premium release. In addition, release notes for Target APIs, SDKs, the JavaScript library (at.js), and other platform changes are also included, when applicable.

>[!IMPORTANT]
>
>* **Adobe Again Named a Leader in Gartner Magic Quadrant for Personalization Engines**: Adobe was once again named a Leader in the third-annual Gartner Magic Quadrant for Personalization Engines, 2020 report. The Gartner Magic Quadrant for Personalization Engines evaluated vendors across 15 criteria that fall into two categories: completeness of vision and ability to execute. [Read about it on The Adobe Blog](https://theblog.adobe.com/adobe-again-named-leader-in-gartner-magic-quadrant-for-personalization-engines/).
>
>* **mbox.js deprecation**: On August 30, 2020, Adobe Target will no longer support the mbox.js library. Post August 30, 2020, all calls made from mbox.js will gracefully fail and impact your pages that have Target activities running by serving default content. We recommend that all customers migrate to the most recent version of the at.js library before this date to avoid any potential issues with your sites. For more information, see [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) and [Adobe Target Skill Builder: Developer chat, migrate Adobe Target's mbox.js to at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
>
>   Although, mbox.js is currently supported, we have not provided feature updates to this library since July 2017. The newer at.js provides many advantages over mbox.js. Among other benefits, at.js improves page load times for web implementations, improves security, and provides better implementation options for single page applications.
>
>   By moving all customers to at.js, our engineers and support staff will be able to provide you with new functionality and offer the support you have come to expect from Adobe.
>
>* **Target Announcements**: See the Target announcements page for information about upcoming events, including Target Skill Builder sessions, developer chats, webinars, and Target Coffee Break sessions. For more information, see [Target announcements](/help/r-release-notes/target-announcements.md).

The issue numbers in parentheses are for internal [!DNL Adobe] use.

## Target Standard/Premium 20.7.1 (July 23, 2020)

This release includes the following changes:

### [!UICONTROL Administration] section UI refresh

We are gradually rewriting the entire [!DNL Target] UI using a new tech stack to be able to offer improved performance, reduce the maintenance time required when releasing new features, and to improve the user experience across the product. The first section refreshed is the [!UICONTROL Setup] section, which has been renamed [!UICONTROL Administration].

As part of this refresh, you will be able to easily perform many actions using the pages in the [!UICONTROL Administration] section, such as:

* Download the latest at.js file from the [!UICONTROL Implementation] tab (**[!UICONTROL Administration]** > **[!UICONTROL Implementation]**).
* Customize your at.js settings and be able to easily review your changes (**[!UICONTROL Administration]** > **[!UICONTROL Implementation]**).
* Modify enhanced reporting settings, such as the default currency and time zone, IPs to exclude from reporting, etc. (**[!UICONTROL Administration]** > **[!UICONTROL Reporting]**)
* Obfuscate visitor IP addresses for privacy reasons (**[!UICONTROL Administration]** > **[!UICONTROL Implementation]**)
* View the existing list of users per workspace and their roles, before managing them in Adobe Admin Console (**[!UICONTROL Administration]** > **[!UICONTROL Users]**).
* Search and filter all tables in the [!UICONTROL Administration] section.

For more information, see [Administer Target Overview](/help/administrating-target/administrating-target.md).

### Enhancements, fixes, and changes

This release contains the following enhancements, fixes, and changes:

* Fixed an issue that prevented site preferences from being retained after refresh. (TGT-37239)
* Fixed an issue that prevented [!UICONTROL Insert After] > [!UICONTROL Image] from functioning properly with Scalable Vector Graphics (SVG) images. (TGT-37242)
* Fixed an issue for users with the [!UICONTROL Publisher] role that prevented the deletion of draft activities. (TGT-37358)
* Fixed an issue that prevented users from editing an activity when [!UICONTROL All My Workspaces] is selected. (TGT-37276)

## Additional release notes and version details

|Resource|Details|
|--- |--- |
|[Release notes - Target server-side APIs](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md)|Release notes related to Adobe Target's server-side APIs.|
|[Release notes - Target Node.js SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md)|Release notes related to Adobe Target's Node.js SDK.|
|[Release Notes - Target Java SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md)|Release notes related to Adobe Target's Java SDK.|
|[at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)|Details about changes in each version of the Adobe Target at.js JavaScript library.|
|[mbox.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mboxjs-change-log.md)|This page shows changes to each version of mbox.js.<br>Note that the mbox.js library is no longer being developed. All customers should migrate from mbox.js to at.js.|

## Documentation Changes, Past Release Notes, and Experience Cloud Release Notes {#section_1BC5F5208DA548E9B4344A0836E4B943}

In addition to the notes for each release, the following resources provide additional information:

|Resource|Details|
|--- |--- |
|Documentation changes|View detailed information about updates to this guide that might not be included in these release notes.<br>For more information, see [Documentation Changes](../r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C).|
|Release notes for previous releases|View information about new features and enhancements in previous releases of Target Standard and Target Premium.<br>For more information, see [Release notes for previous releases](../r-release-notes/release-notes-for-previous-releases.md).|
|Adobe Experience Cloud release notes|View the latest release notes for the Adobe Experience Cloud solutions.<br>For more information, see [Experience Cloud Release Notes](https://docs.adobe.com/content/help/en/release-notes/experience-cloud/current.html).|

## Prerelease Information {#section_5D588F0415A2435B851A4D0113ACA3A0}

The following resources let you see what's coming in the next Target release.

|Resource|Details|
|--- |--- |
|Adobe Priority Product Update list|To receive advance notifications about upcoming product enhancements to Target and other Adobe Experience Cloud solutions, sign up for the Adobe Priority Product Update:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)|
|Upcoming release notes|For information about the current month's Target releases, including prerelease information, see the [Target Release Notes - Prerelease](/help/r-release-notes/target-release-notes.md) page.|
