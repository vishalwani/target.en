---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates
description: These release notes provide information about features, enhancements, fixes, and known issues for each Adobe Target Standard and Target Premium release.
title: Adobe Target release notes (current) 
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
---

# Target release notes (current){#target-release-notes-current}

These release notes provide information about features, enhancements, and fixes for each Target Standard and Target Premium release. In addition, release notes for Target APIs, SDKs, the JavaScript library (at.js), and other platform changes are also included, when applicable.

>[!NOTE]
>
>* **mbox.js deprecation**: On August 30, 2020, Adobe Target will no longer support the mbox.js library. Post August 30, 2020, all calls made from mbox.js will gracefully fail and impact your pages that have Target activities running by serving default content. We recommend that all customers migrate to the most recent version of the at.js library before this date to avoid any potential issues with your sites. For more information, see [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) and [Adobe Target Skill Builder: Developer chat, migrate Adobe Target's mbox.js to at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
>
>   Although, mbox.js is currently supported, we have not provided feature updates to this library since July 2017. The newer at.js provides many advantages over mbox.js. Among other benefits, at.js improves page load times for web implementations, improves security, and provides better implementation options for single page applications.
>
>   By moving all customers to at.js, our engineers and support staff will be able to provide you with new functionality and offer the support you have come to expect from Adobe.
>
>* **Target Announcements**: See the Target announcements page for information about upcoming events, including Target Skill Builder sessions, developer chats, webinars, and Target Coffee Break sessions. For more information, see [Target announcements](/help/r-release-notes/target-announcements.md).

The issue numbers in parentheses are for internal [!DNL Adobe] use.

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

## at.js 1.8.2 and at.js 2.3.1 releases (June 15, 2020)

The following improvements and fixes have been made in the [!DNL Target] at.js libraries:

|Feature / Enhancement|Description|
| --- | --- |
|at.js 1.8.2|This release of at.js is a maintenance release and includes the following fix:<ul><li>Fixed an issue when using CNAME and edge override, at.js 1.*x* might incorrectly create the server domain, which resulted in the [!DNL Target] request failing. (TNT-35064)</li></ul>For more information, see [at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).|
|at.js 2.3.1|This release of at.js is a maintenance release and includes the following enhancements and fixes:<ul><li>Made the `deviceIdLifetime` setting overridable via [targetGlobalSettings](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md). (TNT-36349)</li><li>Fixed an issue when using CNAME and edge override, at.js 2.*x* might incorrectly create the server domain, which resulted in the [!DNL Target] request failing. (TNT-35065)</li><li>Fixed an issue when using the [!DNL Target] [!DNL Launch] extension v2 and the [!DNL Adobe Analytics] [!DNL Launch] extension, [!DNL Target] delayed the [!DNL Analytics] `sendBeacon` call. (TNT-36407, TNT-35990, TNT-36000)</li></ul>For more information, see [at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).|

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
