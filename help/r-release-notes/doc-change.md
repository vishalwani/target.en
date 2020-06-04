---
keywords: target documentation change log;documentation updates;new topics;edits;updates
description: This page lists important changes made to the Adobe Target documentation, ordered by releases.
title: Documentation changes in the Adobe Target product documentation.
topic: Standard 
uuid: 6fba75e2-0a93-488d-9010-fffa423600c0
---

# Documentation changes{#documentation-changes}

This page lists important changes made to the [!DNL Adobe Target] product documentation.

## Adobe Target Standard/Premium 20.4.1 (May 6, 2020)

|Date|Topic|Changes|
| --- | --- | --- |
|June 4|[A4T reporting](/help/c-integrating-target-with-mac/a4t/reporting.md)|Updated the "Reports in Analytics" section.|
|June 1|[Target announcements](/help/r-release-notes/target-announcements.md)|Added new page to announce upcoming Target events.|
||[Mobile Viewports for Responsive Experiences](/help/c-experiences/c-visual-experience-composer/mobile-viewports.md)|Updated viewport dimensions and resolutions for Apple iPhone 11, Apple iPhone SE, and Google Pixel 2 XL models.|
|May 28|[Reporting FAQ](/help/c-reports/reporting-frequently-asked-questions.md)|Added the following new FAQ: <ul><li>How are the New Visitors and Returning Visitors metrics counted?</li></ul>|
|May 27|[Target release notes (prerelease)](/help/r-release-notes/target-release-notes.md)|Added information about Analytics for Target (A4T) support for Auto-Allocate activities.|
|May 26|[Profile attributes](/help/c-target/c-visitor-profile/profile-parameters.md)|Added following information: "The parameter remains in the profile after disabling the script. Users whose profiles already contain a parameter that is used in an activity's audience will qualify in that activity."|
|May 21|[Whitelist Target edge nodes](/help/c-implementing-target/c-considerations-before-you-implement-target/white-list-edges.md)|Added `mboxedge30.tt.omtrdc.net` to the list.|
|May 20|[Target release notes (prerelease)](/help/r-release-notes/target-release-notes.md)|Added information about the upcoming Target Standard/Premium 20.6.1 (June 10, 2020) release.|
||[Hosts](/help/administrating-target/hosts.md)|Added note to the "Security best practices" section.|
|May 14|[Target release notes (current)](/help/r-release-notes/release-notes.md)|Added information about Profile Batch Status API v2 changes.|
|May 13|[CNAME and Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md)|Added "Known limitations" section.|
|May 11|[Hosts](/help/administrating-target/hosts.md)|Added information about using the ubox functionality with redirects and whitelists.|
||[Work with redirectors](/help/c-implementing-target/c-non-javascript-based-implementation/working-with-redirectors.md)|Added information about using hosts to avoid Open Redirect Vulnerabilities.|
||[Integrate Recommendations with email](/help/c-recommendations/c-recommendations-faq/integrating-recs-email.md)|Added information about using hosts to avoid Open Redirect Vulnerabilities.|
||[Email: implement Target](/help/c-implementing-target/c-non-javascript-based-implementation/non-javascript-based-implementation.md)|Added information about using hosts to avoid Open Redirect Vulnerabilities.|
|May 7|[Target release notes (current)](/help/r-release-notes/release-notes.md)|With the upcoming deprecation of mbox.js on August 30, 2020, David Son, Adobe Target Product Manager recently hosted a developer chat to discuss the benefits of migrating mbox.js to at.js. There is a link where you can watch the webinar for the next 30 days.|
||[Activity QA](/help/c-activities/c-activity-qa/activity-qa.md)|Updated the "Considerations" section.|
||[targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md)|Updated "overrideMboxEdgeServer" row under "Settings."|
|May 6|[Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md)|Added information about ITP 2.3.|
||[Release Notes](/help/r-release-notes/release-notes.md): 20.4.1|This release includes enhancements and fixes. You can read about them and link to the documentation from the Release Notes. This release also includes many documentation updates throughout the help.|

## Adobe Target Standard/Premium 20.2.1 (February 19, 2020)

|Date|Topic|Changes|
| --- | --- | --- |
|May 4|[Reporting FAQ](/help/c-reports/reporting-frequently-asked-questions.md#uneven)|Added new FAQ: "Why is the traffic split between my experiences uneven in my A/B or MVT activity?"|
|April 29|[Known issues and resolved issues](/help/r-release-notes/known-issues-resolved-issues.md)|Added known issue for reporting with extreme orders.|
|April 28|[Profile and variable glossary](/help/c-target/c-visitor-profile/variables-profiles-parameters-methods.md)|Removed information about using `user.header('x-forwarded-for')` with newer AWS edges to retrieve users' IP addresses. This command now works with newer AWS edges.|
||[Target release notes (prerelease)](/help/r-release-notes/target-release-notes.md)|Changed date of the Target Standard/Premium release (20.4.1) to May 6.|
|April 23|[CNAME and Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md)|Updated topic.|
|April 22|[Target release notes (prerelease)](/help/r-release-notes/target-release-notes.md)|Added new section: *Profile Batch Status API v2 changes (May 4, 2020).*|
|April 20|[Target release notes (current)](/help/r-release-notes/release-notes.md)|Added new section: *Adobe Target Skill Builder: Developer chat, migrate Adobe Target's mbox.js to at.js.*|
|April 14|[Whitelist Target edge hosts](/help/c-implementing-target/c-considerations-before-you-implement-target/white-list-edges.md)|New topic.|
|April 10|[Single Page Application implementation](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md#bp)|Added new section: "Implementation best practices."|
|April 7|[Lift and confidence - A4T FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-lift-and-confidence.md#lift-condidence)|Updated text for "Why can't I see lift and confidence on calculated metrics?"|
|April 2|[Profile and variable glossary](/help/c-target/c-visitor-profile/variables-profiles-parameters-methods.md)|Added information about using `user.header('x-forwarded-for')` with newer AWS edges to retrieve users' IP addresses.|
||[Upgrading from at.js 1.*x* to at.js 2.*x*](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md)|Added following note:<ul><li>After installing the ECID library v4.3.0+ and at.js 2.*x*, you will be able to create activities that span unique domains as well as track users. It is important to note that this functionality works only after the session expires.</li></ul>|
|March 30|[Known issues and resolved issues](/help/r-release-notes/known-issues-resolved-issues.md#atjs)|Added a known issues that affects at.js versions prior to at.js 2.2.0. This issue caused click tracking to not report conversions in Analytics for Target (A4T) when Adobe Analytics code was not present on page elements.|
||[at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)|Added the following information to at.js version 2.2.0 details:<ul><li>Fixed an issue that caused click tracking to not report conversions in Analytics for Target (A4T) when Adobe Analytics code was not present on page elements.</li></ul>|
|March 25|[at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)|Added information about the following new versions of at.js:<ul><li>at.js version 2.3.0</li><li>at.js version 1.8.1</li></ul>|
||[targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md)|Added the following new rows in the "Settings" section:<ul><li>cspScriptNonce</li><li>cspStyleNonce</li></ul>Added the following new section:<ul><li>Content Security Policy</li></ul>|
|March 24|[Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md#impact)|Added information about impacts for the following:<ul><li>Profile scripts based on 3rdPartyID</li><li>QA/Preview URLs in iOS devices</li></ul>|
|March 20|[Release notes (current)](/help/r-release-notes/release-notes.md)|Indicated that the Target Standard/Premium 20.2.1 release will be March 23, 2020.|
|March 13|[Limits](/help/r-troubleshooting-target/target-limits.md)|Udated the number of "Audiences, reusable per account."|
|March  12|[Release Notes (current)](/help/r-release-notes/release-notes.md#summit)|Added registration information for free access to the online, digital Summit conference.|
|March 9|[Privacy](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/privacy.md)|Added more information in the "Replacement of last octet of IP addresses" section.|
||[Work with multi-value attributes](/help/c-recommendations/c-algorithms/work-with-multi-value-attributes.md)|Updated code sample in *Pass a multi-value parameter in JavaScript*.|
||[Custom entity attributes](/help/c-recommendations/c-products/custom-entity-attributes.md)|Added code sample in *Using APIs* under *Implementing multi-value attributes*.|
|March 4|[Profile attributes](/help/c-target/c-visitor-profile/profile-parameters.md)|Updated entire topic, with extensive revisions to the "Best practices" section.|
|February 21|[Release notes (current)](/help/r-release-notes/release-notes.md)|Added information about the new Adobe Experience Cloud navigation.|
|February 20|[targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md)|Updated the description for the `enabled` setting. Added information for the following settings: `pageLoadEnabled` and `viewsEnabled`.|
|February 19|[Release Notes](/help/r-release-notes/release-notes.md)|Added information about the upcoming deprecation of the mbox.js library.|
||[Geo](/help/c-target/c-audiences/c-target-rules/geo.md)|Added note that `mboxOverride.browserIp` is supported in at.js 1.*x* only.|
||[at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)|Clarified text explaining which versions of at.js the Target team supports.|
||[Release Notes](/help/r-release-notes/release-notes.md): 20.2.1|This release includes enhancements and fixes. You can read about them and link to the documentation from the Release Notes. This release also includes many documentation updates throughout the help.|

## Adobe Target Standard/Premium 20.1.1 (February 4, 2020)

|Date|Topic|Changes|
| --- | --- | --- |
|February 4|[Release Notes](/help/r-release-notes/release-notes.md): 20.1.1|This release includes enhancements and fixes. You can read about them and link to the documentation from the Release Notes. This release also includes many documentation updates throughout the help.|
