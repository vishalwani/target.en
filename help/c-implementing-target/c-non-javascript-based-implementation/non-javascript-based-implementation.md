---
keywords: Implementation;mbox.js non javascript;adbox;redirector;mbox
description: Information about implementing Target in non-JavaScript scenarios, such as using an AdBox or Redirector.
title: Email  implement Target
subtopic: Getting Started
topic: Standard
uuid: 07abc419-0253-47c6-80b8-0bd0734d2c9d
---

# Email: implement Target{#email-implement-target}

Information about implementing Target in non-JavaScript scenarios, such as using an AdBox or Redirector.

You can track visits to ads and other offsite content. You can also identify the same user on and off your site and deliver a consistent experience throughout their web experience. Using a single URL, the AdBox allows testing without JavaScript or [!DNL at.js] or [!DNL mbox.js].

An AdBox is useful for sites that do not have [!DNL at.js] or [!DNL mbox.js], such as affiliates. If your activity needs dynamic creative (for example, you need to show a product in the ad that was abandoned in the cart), you cannot use an AdBox.

AdBox ads and Redirector can be used with any kind of activity. The following table compares Adbox and Redirector, and when to use each:

| | Purpose | When To Use | URL Structure | Offer Type | Offer Content |
|--- |--- |--- |--- |--- |--- |
|AdBox|Returns different images to the ad|To change the content of an ad|`clientcode​.tt.​omtrdc​.net/​m2​/​clientcode/ubox/​image?`|redirect offer|URL for an image|
|Redirector|Redirects a visitor to a different web page|To change the landing page of an ad|`clientcode​.tt.omtrdc.net/​m2/clientcode​/ubox/page?`|redirect offer|URL for a page|

## Constraints {#section_38F559DCF1324271926608BCD4AB1227}

* There is no client-side timeout as with standard mboxes. If Target is completely down, visitors to the ad will not see content, not even default. 
* 3rd-party cookies are used to track the visits. If the PCIds are different, by default the visitor's 3rd party is merged with any existing 1st-party profiles. 
* To use 1st-party cookies on the AdBox itself, you will need to pass the mBox session in the URL. Talk to your account representative to do this. 
* To use 1st-party cookies to track ad clicks, pass the mbox session in the URL. Talk to your account representative to do this. 
* To use more than one AdBox on the same page, you must pass the Mbox session in the URL. Talk to your account representative to do this. You might have one AdBox and one Redirector link on the same page (because the Redirector is actually on a second page).
* Please note that with Redirector one can be exposed to a risk of Open Redirect vulenarbility. In order to avoid the unauthorized use of redirector links by third parties, Adobe advises customers to use "Authorized Hosts" to whitelist the default redirect url domains. Adobe Target already has a feature to white list such domains that you wish to allow redirects to. Please refer to documentation here | 'docs.adobe.com/content/help/en/target/using/administer/hosts.html' |     
