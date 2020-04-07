---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: Release notes that provide information about features, enhancements, and fixes for the latest or upcoming DNL Adobe Target releases.
title: Adobe Target prerelease notes
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
---

# Target release notes (prerelease){#target-release-notes-prerelease}

This article contains prerelease information. Release dates, features, and other information are subject to change without notice. 

**Last Updated: March 25, 2020**

To view information about the current release, see [Target Release Notes](release-notes.md). The information on these pages might be the same, depending on the timing of releases. The issue numbers in parentheses are for internal [!DNL Adobe] use.

>[!NOTE]
>
>* **mbox.js deprecation**: On August 30, 2020, Adobe Target will no longer support the mbox.js library. Post August 30, 2020, all calls made from mbox.js will fail and impact your pages that have Target activities running. We recommend that all customers migrate to the most recent version of the at.js library before this date to avoid any potential issues with your sites. For more information, see [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md).
>
>   Although, mbox.js is currently supported, we have not provided feature updates to this library since July 2017. The newer at.js provides many advantages over mbox.js. Among other benefits, at.js improves page load times for web implementations, improves security, and provides better implementation options for single page applications.
>
>   By moving all customers to at.js, our engineers and support staff will be able to provide you with new functionality and offer the support you have come to expect from Adobe.

## Target at.js (March 25, 2020)

The following new versions of the Target at.js JavaScript libraries are available:

* at.js version 2.3.0
* at.js version 1.8.1

For more information, see [at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).

## Target Standard/Premium 20.2.1 (March 23, 2020)

>[!IMPORTANT]
>
>See the information above about the deprecation of mbox.js.

This release contains the following enhancements, fixes, and changes:

* Fixed an issue that prevented customers from selecting a collection when performing a catalog search. (TGT-36230)
* Fixed an issue in which a criteria created via API, but not referenced by an activity created in the Target UI, could be erroneously deleted from the UI. (TGT-35917)
* Implemented security improvements to the Content Security Policy (CSP). (TGT-36190)
* Fixed an issue that caused "NaN%" to display when sliding the Attribute Weighting percentage bar to the far left. (TGT-36211)
* Resolved localization issues so that UI text in various languages displays correctly.
* We’ve standardized the list of available metrics from Adobe Analytics for Target (A4T) activities by deprecating Adobe Analytics metrics not supported in the current version of Adobe Analytics APIs. This will enable us to extend our A4T support in future Adobe Target releases. 

  The following changes have been made:

  * "Average Time Spent on Page" has been replaced by "Average Time Spent on Site." Any activities using this as metric the Primary Goal Metric will have "Average Time Spent on Site" (note: measured in minutes rather than seconds) selected as the Primary Goal Metric the next time the activity is edited.
  * "Visitors" has been replaced by "Unique Visitors." Any activities using this metric as the Primary Goal Metric will have "Unique Visitors" selected as the Primary Goal Metric the next time the activity is edited.

* The following metrics have been deprecated and can no longer be selected as the Primary Goal Metric when creating a new A4T activity.

  |Deprecated Metric(s)|Suggested Replacement Metric(s)|
  |--- |--- |
  |Daily Visitors, Hourly Visitors, Monthly Visitors, Quarterly Visitors, Weekly Visitors, Yearly Visitors|Unique Visitors|
  |Average Visit Depth|n/a. Not suggested as a primary goal metric|
  |Bots|n/a. Not suggested as a primary goal metric|
  |Mobile Crash Rate, Mobile Avg Prev Session Length, Mobile App Store Avg Rank, Mobile App Performance Crash Rate, Mobile App Store Avg Rating|n/a. Not suggested as a primary goal metric|

## Prerelease information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63} 

To receive advance notifications about upcoming product enhancements to Target and other Adobe Experience Cloud solutions, sign up for the Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) 
