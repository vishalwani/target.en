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
>* **mbox.js deprecation**: On August 30, 2020, Adobe Target will no longer support the mbox.js library. Post August 30, 2020, all calls made from mbox.js will fail and impact your pages that have Target activities running. We recommend that all customers migrate to the most recent version of the at.js library before this date to avoid any potential issues with your sites. For more information, see [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) and [Adobe Target Skill Builder: Developer chat, migrate Adobe Target's mbox.js to at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
>
>   Although, mbox.js is currently supported, we have not provided feature updates to this library since July 2017. The newer at.js provides many advantages over mbox.js. Among other benefits, at.js improves page load times for web implementations, improves security, and provides better implementation options for single page applications.
>
>   By moving all customers to at.js, our engineers and support staff will be able to provide you with new functionality and offer the support you have come to expect from Adobe.
>
>* **Target Announcements**: See the Target announcements page for information about upcoming events, including Target Skill Builder sessions, developer chats, webinars, and Target Coffee Break sessions. For more information, see [Target announcements](/help/r-release-notes/target-announcements.md).

The issue numbers in parentheses are for internal [!DNL Adobe] use.

## at.js 1.8.2 and at.js 2.3.1 releases (June 15, 2020)

The following improvements and fixes have been made in the [!DNL Target] at.js libraries:

|Feature / Enhancement|Description|
| --- | --- |
|at.js 1.8.2|This release of at.js is a maintenance release and includes the following fix:<ul><li>Fixed an issue when using CNAME and edge override, at.js 1.*x* might incorrectly create the server domain, which resulted in the [!DNL Target] request failing. (TNT-35064)</li></ul>For more information, see [at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).|
|at.js 2.3.1|This release of at.js is a maintenance release and includes the following enhancements and fixes:<ul><li>Made the `deviceIdLifetime` setting overridable via [targetGlobalSettings](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md). (TNT-36349)</li><li>Fixed an issue when using CNAME and edge override, at.js 2.*x* might incorrectly create the server domain, which resulted in the [!DNL Target] request failing. (TNT-35065)</li><li>Fixed an issue when using the [!DNL Target] [!DNL Launch] extension v2 and the [!DNL Adobe Analytics] [!DNL Launch] extension, [!DNL Target] delayed the [!DNL Analytics] `sendBeacon` call. (TNT-36407, TNT-35990, TNT-36000)</li></ul>For more information, see [at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).|

## Profile Batch Status API v2 changes (May 14, 2020)

With the May 20 release, Profile Batch status will return only row-level failure data going forward (success data will not be returned). Failed profile IDs will be returned by the API going forward. 

The previous and new API responses are as follows:

`ProfileBatchStatus Api
http://<<edge>>/m2/<<client>>/profile/batchStatus?batchId=<batchid>`

**Currently we see the response as:**

```
<response>
 
    <batchId>samplebatch-1585929692655-59449976</batchId>
 
    <status>complete</status>
 
    <batchSize>164</batchSize>
 
    <profile>
 
        <id>1514187733806-729395</id>
 
        <status>success</status>
 
    </profile>
 
    <profile>
 
        <id>1573612762055-214017</id>
 
        <status>success</status>
 
    </profile>
 
    <profile>
 
        <id>some profile id</id>
 
        <status>failed</status>
 
    </profile>
 
</response>
```

**After May 4, the response will be:**

```
<response>
 
    <batchId>samplebatch-1585929692655-59449976</batchId>
 
    <status>complete</status>
 
    <batchSize>164</batchSize>
 
    <profile>
 
        <id>some profile id</id>
 
        <status>failed</status>
 
    </profile>
 
</response>
```

## Target Standard/Premium 20.4.1 (May 6, 2020)

This release contains the following enhancements, fixes, and changes:

* Fixed an issue that incorrectly qualified a device and browser type for an audience. (TGT-36266)
* Fixed an issue that prevented report data from displaying when viewed on screens less than 963 pixels wide. (TGT-36549)
* Fixed an issue that caused Auto Personalization reports to not render correctly. (TGT-36619)
* Fixed an issue that allowed incompatible metrics to be selected in Auto-Allocate and Auto-Target activities that use Analytics for Target (A4t). (TGT-36646)
* Fixed an issue that caused certain options in the Visual Experience Composer (VEC) to not display correctly. (TGT-36571)
* Fixed an issue in the Target UI that caused other Recommendations offer previews to display the edited content after a user replaced the content in a single experience. (TGT-36053 & TGT-36894)
* Fixed an issue that prevented some users from deleting items from a Recommendations catalog. (TGT-36455)
* Fixed an issue that prevented users from saving Recommendations criteria on a multi-page activity. (TGT-36249)
* Fixed an issue that caused the behavioral data source radio buttons to disappear when editing the criteria for a second consecutive time. (TGT-36796)
* Fixed a display issue that caused a Recommendations algorithm to display "fetching results" for an extended period. (TGT-36550 & TGT-36551)
* Updated many UI strings localized in various languages.

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
