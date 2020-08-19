---
keywords: global mbox;customize global mbox;edit at.js;at.js;implement at.js
description: Information to help you customize a global mbox for at.js.
title: Customize a Global mbox
feature: 
subtopic: Getting Started
topic: Standard
uuid: 0f784d6e-8f36-4c26-adbf-0d56b7d6d390
---

# Customize a Global mbox{#customize-a-global-mbox}

Information to help you customize a global mbox for at.js.

1. Click **[!UICONTROL Administration]** > **[!UICONTROL Implementation]**.

1. Disable **[!UICONTROL Page load enabled (Auto create global mbox)]**, then add the name of the custom global mbox that you would like to use to deliver activities from [!DNL Target]. 

   This custom global mbox is also used for click tracking.

   ![custom-global-mbox](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/assets/custom-global-mbox.png)

1. Click **[!UICONTROL Save]** when you are finished. 

1. Implement the [!DNL at.js] library on your site.

   See [How to deploy at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/how-to-deployatjs.md) for more information.

1. Time the transition with your release.

   As soon as you are ready for [!DNL Target] to start using your global mbox for all activities moving forward, you can proceed with this step.

   Update the name of the custom global mbox to match the name used in Step 2, above.

   >[!IMPORTANT]
   >
   >When you save, all activities in your account sync with this mbox. If this mbox is not on your site, all activities will stop functioning.

