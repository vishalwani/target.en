---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: Release notes that provide information about features, enhancements, and fixes for the latest or upcoming DNL Adobe Target releases.
title: Adobe Target prerelease notes
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
---

# Target release notes (prerelease){#target-release-notes-prerelease}

This article contains prerelease information. Release dates, features, and other information are subject to change without notice. 

**Last Updated: May 27, 2020**

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

## Target Standard/Premium 20.6.1 (June 10, 2020)

|Feature / Enhancement|Description|
| --- | --- |
|Analytics for Target (A4T) support for Auto-Allocate activities|With the June release, Auto-Allocate tests will support [Analytics for Target](/help/c-integrating-target-with-mac/a4t/a4t.md). This integration allows you to use Auto-Allocate’s multi-armed bandit capability to drive traffic to winning experiences, while using an Adobe Analytics goal metric and/or Adobe Analytics reporting and analysis capabilities. If you’ve already [implemented A4T](/help/c-integrating-target-with-mac/a4t/a4timplementation.md) for use with A/B Test and Experience Targeting activities, you’re all set! |
|Publisher role|This new role is similar to the current Observer role (can view activities, but cannot create or edit them). However, the Publisher role has the additional permission to active activities.|
|Administration page<br>Formerly "Setup."|The Setup page has been renamed "Administration" and the UI for all menu items has been updated to improve the workflow and ease-of-use.<br>Available menu items include:<ul><li>Visual Experience Composer</li><li>Reporting</li><li>Scene7 Settings</li><li>Implementation</li><li>Properties</li><li>Hosts</li><li>Environments</li><li>Response Tokens</li><li>Users</li></ul>|

## Prerelease information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63} 

To receive advance notifications about upcoming product enhancements to Target and other Adobe Experience Cloud solutions, sign up for the Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) 
