---
keywords: responsive;mobile viewports;viewport;devices;mobile;responsive web design;rwd
description: Mobile viewports help you preview how your Adobe Target activities appear on screens of various sizes.
title: Mobile Viewports for responsive experiences
feature: vec
uuid: 86a74584-4a4d-428b-9d29-f7ebdf0cef2a
---

# Mobile Viewports for responsive experiences{#mobile-viewports-for-responsive-experiences}

Mobile viewports help you preview how your [!DNL Target] activities appear on screens of various sizes.

The mobile viewport preview feature is designed for responsive sites that render well on various devices, windows, or screen sizes. Responsive sites automatically adjust and adapt to any screen size, including desktops, laptops, tablets, or mobile phones.

>[!NOTE]
>
> * Use mobile viewports if your site is responsive and the same elements in your desktop page are used on your mobile page in a different configuration. If you have a separate mobile site with a separate structure, such as `m.mysite.com`, use a [multipage activity](../../c-experiences/c-visual-experience-composer/multipage-activity.md#concept_277E096063E14813AC5D8EDFA1D2ED48) instead.
>
>* Mobile viewports are not available if overlapped by a redirect offer overlay.

A viewport is defined by the size of the rectangle filled by a web page on your screen. It is the size of the browser window, minus the scrollbars and toolbars. Browsers use "CSS pixels." For many devices, such as those with retina screens, the viewport is smaller than the advertised device resolution.

Below are the viewports and resolutions for some popular devices. Remember to use the viewport size in [!DNL Target]. Various websites list viewport sizes for popular devices. For example, see [https://viewportsizer.com/devices/](https://viewportsizer.com/devices/) or consult the device maker's website.

|  Device  | Viewport Size  | Device Resolution  |
|---|---|---|
|  iPhone SE | 375w x 667h | 750w x 1334h |
|  iPhone 11 Pro Max | 414w x 896h | 1242w x 2688h |
|  iPhone 11 Xs Max | 414w x 896h | 1242w x 2688h |
|  iPhone 11 | 414w x 896h | 828w x 1792h |
|  iPhone 11 Xr | 414w x 896h | 828w x 1792h |
|  iPhone 11 Pro | 375w x 812h | 1125w x 2436h |
|  iPhone 11 X | 375w x 812h | 1125w x 2436h |
|  iPhone 11 Xs | 375w x 812h | 1125w x 2436h |
|  iPhone X  | 375w x 812h  | 1125w x 2436h |
|  iPhone 8 Plus  | 414w x 736h  | 1080w x 1920h  |
|  iPhone 8  | 375w x 667h  | 750w x 1334h  |
|  iPhone 7 Plus  | 414w x 736h  | 1080w x 1920h  |
|  iPhone 7  | 375w x 667h  | 750w x 1334h  |
|  iPhone 6s Plus  | 414w x 736h  | 1080w x 1920h  |
|  iPhone 6s  | 375w x 667h  | 750w x 1334h  |
|  iPhone 6 Plus  | 414w x 736h  | 1080w x 1920h  |
|  iPhone 6  | 375w x 667h  | 750w x 1334h  |
|  iPad Pro  | 1024w x 1366h  | 2048w x 2732h  |
|  iPad Third & Fourth Generation  | 768w x 1024h  | 1536w x 2048h  |
|  iPad Air 1 & 2  | 768w x 1024h  | 1536w x 2048h  |
|  iPad Mini  | 768w x 1024h  | 768w x 1024h  |
|  iPad Mini 2 & 3  | 768w x 1024h  | 1536w x 2048h  |
|  Nexus 6P  | 411w x 731h  | 1440w x 2560h  |
|  Nexus 5X  | 411w x 731h  | 1080w x 1920h  |
|  Google Pixel  | 411w x 731h  | 1080w x 1920h  |
|  Google Pixel XL  | 411w x 731h  | 1440w x 2560h  |
|  Google Pixel 2  | 411w x 731h  | 1080w x 1920h  |
|  Google Pixel 2 XL  | 411w x 823h  | 1440w x 2880h  |
|  Samsung Galaxy Note 5  | 480w x 853h  | 1440w x 2560h  |
|  LG G5  | 480w x 853h  | 1440w x 2560h  |
|  One Plus 3  | 480w x 853h  | 1080w x 1920h  |
|  Samsung Galaxy S9  | 360w x 740h  | 1440w x 2960h  |
|  Samsung Galaxy S9+  | 360w x 740h  | 1440w x 2960h  |
|  Samsung Galaxy S8  | 360w x 740h  | 1440w x 2960h  |
|  Samsung Galaxy S8+  | 360w x 740h  | 1440w x 2960h  |
|  Samsung Galaxy S7  | 360w x 640h  | 1440w x 2560h  |
|  Samsung Galaxy S7 Edge  | 360w x 640h  | 1440w x 2560h  |
|  Nexus 7 (2013)  | 600w x 960h  | 1200w x 1920h  |
|  Nexus 9  | 768w x 1024h  | 1536w x 2048h  |
|  Samsung Galaxy Tab 10  | 800w x 1280h  | 800w x 1280h  |
|  Chromebook Pixel  | 1280w x 850h  | 2560w x 1700h  |

If you want to deliver an activity to people on a particular device, choose the appropriate audience for that device in the activity diagram. Use the Mobile Web Composer to edit the page in the activity for that device. If you want to run an activity across your entire digital experience and make sure it looks good across all devices, don't apply targeting, and use mobile viewports to preview the activity on each screen size.

If you have a responsive site, typically your site is designed to open in a different view when accessed by a device with a specific screen size. Those screen sizes that trigger the new views are known as CSS breakpoints. CSS breakpoints are points where website content responds depending on device width to display the optimal layout to visitors. CSS breakpoints are also called [media queries](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries). 

Save your CSS breakpoints in [!DNL Target] so you can preview your experiences for each view you define. Each of these experiences is displayed in a mobile viewport in the [!DNL Target] interface. Open the view for each screen size by clicking that viewport along the top of the display.

If your site is not responsive, you can still use the Mobile Web Composer to view a site if your activity is targeted to a specific device.

>[!IMPORTANT]
>
>Although you can edit an experience from within mobile viewports, these changes apply to all viewports and devices, not just the viewport that you're working in. Similarly, editing an experience in the normal desktop view changes the page for all screen sizes, not just the desktop view. Currently, we don't support viewport-specific page changes.

## Mobile viewport configuration {#task_B4B161499DC0470584ED922A4D20FCAB}

Configure any mobile viewports you want to make available when creating your experiences.

1. Click **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]**.
1. To add a new mobile viewport, in the **[!UICONTROL Mobile viewports configuration]** section, click **[!UICONTROL Add]**.

   ![Add viewport](/help/c-experiences/c-visual-experience-composer/assets/viewpoert_add.png)

   To change the configuration of an existing mobile viewport, select that viewport, then click the [!UICONTROL Edit] (pencil) icon.

1. Type a name for the mobile viewport.

   Give your mobile viewport a descriptive name that is easy to recognize. The name can be up to 36 characters long.

1. Enter the screen size of the mobile device, both width and height.

   The width can be between 150 and 968 pixels. The height can be between 150 and 1280 pixels.
   
1. (Optional) Select the operating system of the device.

   Options:

   * Android 
   * iOS 
   * Windows 
   * Symbian 
   * Blackberry

   If you use the [Enhanced Experience Composer](../../c-experiences/experiences.md#section_34265986611B4AB8A0E4D6ACC25EF91D) and choose an operating system, [!DNL Target] emulates that device when you view the page. If, for example, there is a different look and feel for Android than iOS on your responsive site, [!DNL Target] mimics that behavior.

1. Click **[!UICONTROL Save]**.

>[!NOTE]
>
>If you attempt to delete a mobile viewport that is in use, the following message displays: "This viewport is currently associated to one or multiple activities. You need to remove the viewport from those activities before being able to delete it."

## Create a responsive experience {#task_D6332438B5EE48CCA8AF199270F1CAEF}

Add mobile viewports to your [!DNL Target] activities to create responsive experiences for mobile screens.

1. Create the [desired activity](/help/c-activities/activities.md).
1. In the Visual Experience Composer, click the **[!UICONTROL Settings]** gear icon, then select **[!UICONTROL Add Mobile Viewports]**.

   ![Add Mobile Viewports option](/help/c-experiences/c-visual-experience-composer/assets/add-mobile-viewports.png)

1. Click the **[!UICONTROL Devices]** icon, then enable each device that should have a mobile viewport.

   ![Enable mobile viewports](/help/c-experiences/c-visual-experience-composer/assets/mobileviewports.png)

   The mobile viewports are listed from smallest to largest according to width.

1. Edit the mobile viewports as desired.

   Any changes you make to the experience (for example, if you change the text in a heading) are applied to the experience on all devices.

   Mouse over the name of a viewport to see the viewport's size.

   ![iPhone 11 Pro Max responsive experience](/help/c-experiences/c-visual-experience-composer/assets/iphone11.png)

1. If desired, toggle between portrait and landscape modes by clicking the desired orientation icon.

   ![Orientation options](/help/c-experiences/c-visual-experience-composer/assets/orientation.png)

## Use Case: Target two iPhone versions {#task_CC3144BF5BA54034996E1D3DB0BC1A35}

This use case shows how to configure experiences for two iPhone versions: iPhone 6 and iPhone 6 Plus.

1. Click **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]**.
1. In the **[!UICONTROL Mobile Viewport Configuration]** section, create mobile viewports for iPhone 6 and iPhone 6 plus.

   Use the following settings for each viewport:

   |  Name  | Width  | Height  | Operating System  |
   |---|---|---|---|
   |  iPhone 6  | 375  | 667  | iOS  |
   |  iPhone 6 Plus  | 414  | 736  | iOS  |

   ![](assets/iphoneviewportconfig.png)

1. Create an activity with the experience you would like to target.
1. Select the experience you want to target to visitors who access your site from an iPhone 6 or iPhone 6 Plus.
1. When selecting your target, click **[!UICONTROL Create Audience]**, then configure an audience as shown in the image below:

   ![](assets/iphoneaudiences.png)

   Because the phone could be rotated to landscape, requiring both height and width to be greater than 320 simultaneously creates a condition that only the 6 and 6 Plus would be able to meet, when combined with the iPhone Device Model. 
1. Click **[!UICONTROL Save]**.
1. Continue setting up your activity as you normally would.

## Training videos 

The following videos contain more information about the concepts discussed in this article.

### Visual Experience Composer (2 of 2) (7:29) ![Overview badge](/help/assets/overview.png)

The following demo video includes information about using the Visual Experience composer to work with mobile viewports:

* Rename and duplicate an experience
* Create a redirect experience
* Target an activity to a single URL or a group of URLs
* Create a multi-page activity
* Preview and build experience for responsive websites
* Use overlays to highlight types of elements

>[!VIDEO](https://video.tv.adobe.com/v/17401)

### Account Preferences in Adobe Target ![Overview badge](/help/assets/overview.png)

This video includes information about setting up mobile viewports, beginning at 4:40 in the video.

>[!VIDEO](https://video.tv.adobe.com/v/17379) 