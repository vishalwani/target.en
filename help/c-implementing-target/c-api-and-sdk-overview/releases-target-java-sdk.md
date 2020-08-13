---
keywords: at.js;sdk;release;updates;sdks;server side;serverside;server-side;java;java sdk
description: Release notes related to Adobe Target's Java SDK.
title: Release notes related to Adobe Target's Java SDK.
feature: release notes 
topic: Standard
---

# Release notes - Target Java SDK

Release notes related to the [Target Java SDK](https://github.com/adobe/target-java-sdk).

The [!DNL Target] Java SDK lets you deploy [!DNL Target] server-side. This Java SDK helps you easily integrate [!DNL Target] with other [!DNL Adobe Experience Cloud] solutions, such as the [!DNL Adobe Experience Cloud Identity Service], [!DNL Adobe Analytics], and [!DNL Adobe Audience Manager].

The Java SDK introduces best practices and removes complexities when integrating with [!DNL Target] via our delivery API so that your engineering teams can focus on business logic.

Learn more about the Target Java SDK on the Adobe Tech Blog - [Server-Side Optimization with the new Target Java SDK](https://medium.com/adobetech/server-side-optimization-with-the-new-target-java-sdk-421dc418a3f2).

## Version 1.1.0 (December 16, 2019)

The following section provides more information about version 1.1.0 of the Target Java SDK:

### Added

* Support for proxy config added due to an open source contribution made by @hisham-hassan.

## Version 1.0.1 (November 11, 2019)

The following section provides more information about version 1.0.1 of the Target Java SDK:

### Fixed

* Send supplemental data ID in a Target request even when there is no Visitor API cookie present.

## Version 1.0.0 (October 31, 2019)

The following sections provide more information about version 1.0.0 of the Target Java SDK:

### Added

* [Target View Delivery v1 API](https://developers.adobetarget.com/api/delivery-api/) support, including Page Load and View prefetch.
  * Full support for delivering all types of offers authored in Visual Experience Composer (VEC).
* Support for prefetching and notifications that allows for performance optimization by caching prefetched content.
* Support for optimizing performance in hybrid [!DNL Target] integrations via `serverState`, when [!DNL Target] is deployed both on the server-side and on the client-side.
  * We are introducing a setting called `serverState` that contains experiences retrieved via server-side, so that at.js v2.2+ will not make an additional server call to retrieve the experiences. This approach optimizes page load performance.
* Open sourced on GitHub as [Target Java SDK](https://github.com/adobe/target-java-sdk).
* Validation of SDK API method arguments.
* Added README, samples, and unit tests.
* Added CoC, Contribution guidelines, PR, and issue templates.

