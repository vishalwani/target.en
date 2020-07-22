---
keywords: vec;visual experience composer; vec;iframe;extension;browser
description: Information to use the Adobe Target Visual Experience Composer (VEC) Helper browser extension to load websites reliably within the VEC to rapidly author and QA experiences.
title: Adobe Target Visual Experience Composer (VEC) helper extension
topic: Standard
---

# Visual Experience Composer helper extension

The [!DNL Adobe Target] Visual Experience Composer (VEC) Helper browser extension for Google Chrome lets you load websites reliably within the VEC to rapidly author and QA web experiences.

Reasons why some websites might not open reliably in the VEC:

* The website has strict security policies.
* The website is in an iframe.
* The at.js library is not yet implemented on the website.
* The customer's QA and/or stage site is not available to the outside world (the site is internal).

The VEC Helper browser extension for Chrome solves site-loading issues for which customers now rely on the [!DNL Target] [!UICONTROL Enhanced Experience Composer] or third-party extensions, such as Requestly

Benefits of using the VEC Helper extension:

* All iframe busting headers, such as X-Frame-Options and Content-Security-Policy, are implicitly removed from the website. There is no more need to create complicated Requestly rules to do this.
* If a webpage does not yet contain the [!DNL Target] at.js JavaScript library, you can use the extension to inject the library so you can author experiences for the website. You can then create activities and QA them using preview links.
* Mobile Viewports are supported even without the [!UICONTROL Enhanced Experience Composer] (EEC).
* Customers new to [!DNL Target] can use the extension to experiment with [!DNL Target] even if their IT developers have not yet implemented [!DNL Target] on their websites.
* Partners servicing multiple customers' websites and [!DNL Target] accounts now have one simple mechanism to support VEC loading, instead of managing multiple rules in third-party tools.

## Obtain and install the VEC Helper browser extension

1. Navigate to the [Adobe Target VEC Helper browser extension in the Chrome Web Store](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak).
1. Click [!UICONTROL Add to Chrome > Add Extension].
1. To use the extension, click the VEC Helper browser extension icon ( ![VEC Helper icon](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension.png) ) in your Chrome browser's toolbar while in the VEC or [QA Mode](/help/c-activities/c-activity-qa/activity-qa.md).

The following illustration shows the VEC Helper with the [!UICONTROL Inject Target Libraries] setting enabled:

![VEC helper 1](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension-1.png)

The following illustration shows the VEC Helper asking you whether you want it to inject [!DNL Target] libraries in the page to enable authoring: 

![VEC helper 2](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-helper.png)

## Notes

* Your implementation must use the [!DNL Target] at.js library. You cannot use an mbox.js implementation with the extension.
* The [!UICONTROL Inject Target libraries] flag in the extension is OFF by default. You can enable this flag if you want to use the VEC on a site that has not yet been implemented for [!DNL Target].

  Be aware that this flag is a global setting. The flag is enabled or disabled for all websites opened in the VEC. So, for example, if you set this flag to ON and open a website that is already implemented with at.js, you'll receive a message informing you that at.js is already loaded. We anticipate that most customers will already have at.js implemented on their pages and will use the default setting of OFF.

* The extension loads the latest version of at.js that is available from the [!DNL Target UI] in [!UICONTROL Administration > Implementation].
* When using the extension to inject at.js while in [QA Mode](/help/c-activities/c-activity-qa/activity-qa.md), you must have another Chrome tab open. This Chrome tab must be authenticated to the same [!DNL Adobe Experience Cloud] Organization in which you created the activity.
* The following messages help keep you informed:

  * If you attempt to load a website using the VEC that fails to load, a message displays suggesting that you install the VEC Helper browser extension.
  * If at.js is not yet implemented on the website, a message displays in the VEC suggesting that you install the extension.
  * If the extension is enabled and is powering the loading, messages display when the extension injects the at.js library (if necessary) or helps open the website reliably within the VEC.