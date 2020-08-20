---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: Release notes that provide information about features, enhancements, and fixes for the latest or upcoming DNL Adobe Target releases.
title: Adobe Target prerelease notes
feature: 
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
---

# Target release notes (prerelease){#target-release-notes-prerelease}

This article contains prerelease information. Release dates, features, and other information are subject to change without notice. 

**Last Updated: August 20, 2020**

To view information about the current release, see [Target Release Notes](release-notes.md). The information on these pages might be the same, depending on the timing of releases. The issue numbers in parentheses are for internal [!DNL Adobe] use.

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

## Target Standard/Premium 20.9.1 (September 2, 2020)

This release contains the following enhancements, fixes, and changes:

* Fixed an issue that caused errors to display when loading the new **[!UICONTROL Administration]** pages after switching organizations. (TGT-37730)
* Fixed a display issue that caused the incorrect client code to display on the **[!UICONTROL Administration > Implementation]** page. (TGT-37849)
* Fixed an issue that sometimes prevented users from using the editing features in the **[!UICONTROL Visual Experience Composer]** (VEC) after successfully loading the VEC. (TGT-37162)
* Fixed an issue that sometimes prevented users from downloading at.js from the **[!UICONTROL Administration > Implementation]** page after switching organizations. (TGT-37668)
* Fixed an issue in **[!UICONTROL Experience Targeting]** (XT) activities that caused experiences to display "fetching results" for an extended period of time. (TGT-37684)
* Improved navigation and functionality for keyboard-only users. (TGT-34479 & TGT-34473)
* Added labels in the UI to aid users using assistive technologies. (TGT-34480)
* Improved the error message when deleting a mobile viewport that is currently used in an activity. The error message now reads: "This viewport is currently associated to one or multiple activities. You need to remove the viewport from those activities before being able to delete it." (TGT-37030)
* Added support in the VEC to allow click tracking on a css selector that matches more than one element in the page. (TGT-37323)
* Fixed an issue that prevented certain users from displaying the **[!UICONTROL Activity]** list. The following error message was displayed: "Unable to fetch URLsuggestions." The error occurred for users using carriage returns in their FirstName (FirstName/r/n) in the Adobe Backend system. (TGT-37330)
* Fixed an issue that prevented users from displaying the **[!UICONTROL Activity]** page if the workspace name (specified in the **[!UICONTROL Adobe Admin Console for Enterprise]**) contains an apostrophe. (TGT-37709)
* The at.js download button is now disabled while loading to prevent [!DNL Target] from sending multiple requests if users click the download button multiple times. (TGT-37633)
* Fixed an issue that cause an incorrect last-modified value for [!DNL Recommendations] criteria. (TGT-37666)

## Prerelease information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63} 

To receive advance notifications about upcoming product enhancements to Target and other Adobe Experience Cloud solutions, sign up for the Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) 
