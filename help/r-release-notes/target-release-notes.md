---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: Release notes that provide information about features, enhancements, and fixes for the latest or upcoming DNL Adobe Target releases.
title: Adobe Target prerelease notes
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
---

# Target release notes (prerelease){#target-release-notes-prerelease}

This article contains prerelease information. Release dates, features, and other information are subject to change without notice. 

**Last Updated: May 4, 2020**

To view information about the current release, see [Target Release Notes](release-notes.md). The information on these pages might be the same, depending on the timing of releases. The issue numbers in parentheses are for internal [!DNL Adobe] use.

>[!NOTE]
>
>* **mbox.js deprecation**: On August 30, 2020, Adobe Target will no longer support the mbox.js library. Post August 30, 2020, all calls made from mbox.js will fail and impact your pages that have Target activities running. We recommend that all customers migrate to the most recent version of the at.js library before this date to avoid any potential issues with your sites. For more information, see [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md). See *Adobe Target Skill Builder: Developer chat, migrate Adobe Target's mbox.js to at.js* below for information.
>
>   Although, mbox.js is currently supported, we have not provided feature updates to this library since July 2017. The newer at.js provides many advantages over mbox.js. Among other benefits, at.js improves page load times for web implementations, improves security, and provides better implementation options for single page applications.
>
>   By moving all customers to at.js, our engineers and support staff will be able to provide you with new functionality and offer the support you have come to expect from Adobe.

## Adobe Target Skill Builder: Developer chat, migrate Adobe Target's mbox.js to at.js {#skill-builder}

With the upcoming deprecation of mbox.js on August 30, 2020, David Son, Adobe Target Product Manager recently hosted a developer chat to discuss the benefits of migrating mbox.js to at.js. For the next 30 days you can [view the webinar recording](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).

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

## Profile Batch Status API v2 changes (May 12, 2020)

With the May 4 release, Profile Batch status will return only row-level failure data going forward (success data will not be returned). Failed profile IDs will be returned by the API going forward. 

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

## Prerelease information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63} 

To receive advance notifications about upcoming product enhancements to Target and other Adobe Experience Cloud solutions, sign up for the Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) 
