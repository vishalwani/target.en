---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: Release notes that provide information about features, enhancements, and fixes for the latest or upcoming DNL Adobe Target releases.
title: Adobe Target prerelease notes
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
---

# Target release notes (prerelease){#target-release-notes-prerelease}

This article contains prerelease information. Release dates, features, and other information are subject to change without notice. 

**Last Updated: June 17, 2020**

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

## Target Standard/Premium 20.5.1 (June 17, 2020)

|Feature / Enhancement|Description|
| --- | --- |
|Analytics for Target (A4T) support for [!UICONTROL Auto-Allocate] activities|[!UICONTROL Auto-Allocate] activities now support [Analytics for Target](/help/c-integrating-target-with-mac/a4t/a4t.md).<br>This integration allows you to use the [!UICONTROL Auto-Allocate] multi-armed bandit capability to drive traffic to winning experiences, while using an [!UICONTROL Adobe Analytics] goal metric and/or [!UICONTROL Adobe Analytics] reporting and analysis capabilities.<br>If you’ve already [implemented A4T](/help/c-integrating-target-with-mac/a4t/a4timplementation.md) for use with A/B Test and Experience Targeting activities, you’re all set!<br>For more information, see [Analytics for Target (A4T) support for Auto-Allocate activities](/help/c-integrating-target-with-mac/a4t/campaign-creation.md#a4t-aa) in *Activity creation*. |
|Response tokens for Traffic Allocation Method for Auto-Target and Automated Personalization activities|Two [response tokens](/help/administrating-target/response-tokens.md) have been added to [!UICONTROL Auto-Target] and [!UICONTROL Automated Personalization] activities to enable determination of whether a visitor received a particular experience as a result of being assigned to “control” or to “targeted” traffic.<ul><li>`experience.trafficAllocationId` will return 0 if a visitor received an experience from being in “control” traffic and 1 if a visitor received an experience from the “targeted” traffic distribution.</li><li>`experience.trafficAllocationType` will return “control” or “targeted."</li></ul>For more information on control vs. targeted traffic, see [Select the control for your Automated Personalization or Auto-Target activity](/help/c-activities/t-automated-personalization/experience-as-control.md).|
|[!UICONTROL Publisher] role|This new role is similar to the current [!UICONTROL Observer] role (can view activities, but cannot create or edit them). However, the [!UICONTROL Publisher] role has the additional permission to activate activities.<br>For more information, see: <ul><li>**Target Standard users**: [Specify roles and permissions](/help/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) in *Users*.</li><li>**Target Premium users**: [Step 6: Specify roles and permissions](/help/administrating-target/c-user-management/property-channel/properties-overview.md#section_8C425E43E5DD4111BBFC734A2B7ABC80) in *Configure enterprise permissions*.</li></ul>|
|A4T support in [!DNL Analysis Workspace]<br>June 25, 2020|[!UICONTROL Anaytics for Target] (A4T) is now supported in [!DNL Analysis Workspace]. The [!UICONTROL Analytics for Target (A4T) panel] lets you analyze your [!DNL Adobe Target] activities and experiences in [!DNL Analysis Workspace].<br>For more information, see [Reports in Analytics](/help/c-integrating-target-with-mac/a4t/reporting.md) in *A4T reporting* and [Analytics for Target (A4T) panel](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/a4t-panel.html) in the *Analytics Tools Guide*.|

### Enhancements, fixes, and changes

* Fixed an issue that caused the "visitors" metric to be stored in the activity's definition instead of "UniqueVisitors." (TGT-37098)
* Fixed an issue in the [!DNL Target] UI that caused the vertical scrollbar to not function correctly on the [!UICONTROL Audiences] page. (TGT-36968)

## Prerelease information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63} 

To receive advance notifications about upcoming product enhancements to Target and other Adobe Experience Cloud solutions, sign up for the Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) 
