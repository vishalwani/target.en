---
keywords: a4t;A4T;Analytics as the reporting source for Target
description: You can configure an activity in Target Standard/Premium to use Adobe Analytics as the reporting source (A4T).
title: Activity creation
topic: Advanced,Standard,Classic
uuid: b04ad535-62fb-4dd3-ab3f-23da60fbffbd
---

# Activity creation{#activity-creation}

You can configure an activity in [!DNL Target] to use [!DNL Adobe Analytics] as the reporting source (A4T).

Before you set up an activity that uses [!DNL Analytics] as the reporting source, establish the goal for the activity, such as improving revenue per visitor (RPV) or increasing clicks on your shopping cart. Choose a final success metric for the activity. Although you can select additional metrics at any time in [!DNL Analytics], you must still specify a particular metric you expect this test to affect.

Creating a [!DNL Target] activity that uses [!DNL Analytics] as the reporting source is similar to setting up a regular [!DNL Target] activity, with a few important differences. For example, you cannot select a segment for reporting while creating the activity because all segments available in [!DNL Analytics] can be applied when viewing a report. 

1. Click **[!UICONTROL Create Activity]**.

   >[!NOTE]
   >
   >An activity name cannot include the "%" character if [!DNL Analytics] is used as the reporting source.

1. Select the activity type and begin setting up the activity.
1. When you get to the **[!UICONTROL Settings]** portion of the activity creation flow, choose **[!UICONTROL Adobe Analytics]** and specify your company.
1. Select a report suite.

   You can choose any report suite that is available to you in [!DNL Analytics]. The report suite defines where the collected data will be available. Virtual report suites are not included in the report suite list.

   You might encounter two possible errors while selecting the report suite:

   * You get an error that no report suites are available, but your account is properly set up.

     You might need to check your [!DNL Analytics] company. If your [!DNL Adobe Experience Cloud] account is tied to more than one [!DNL Analytics] company, log out of [!DNL Target], and log in to [!DNL Analytics] under the right company. Then return to [!DNL Target], and the report suites will load. 

   * You don't see the report suite that you expect.

     Only report suites that are provisioned to connect to [!DNL Target] will be available for selection. If you don't see the report suite(s) you expect, first try logging out and logging back in to the [!DNL Adobe Experience Cloud] to try again.

   If the report suite(s) is still missing from the list, please [contact Customer Care](../../cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

1. Specify your tracking server.

   See [Using an Analytics Tracking Server](../../c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823).

1. Define the experience.
1. Specify the activity goal.

   You are required to select a success metric to use as a goal for each activity. Your activity goal is the conversion activity that signals a successful activity. It is best practice never to run a test without having a goal to improve in some specific way. You can choose any [!DNL Analytics] metric available in the [!DNL Analytics] metric selector.

   >[!NOTE]
   >
   >You can send a custom Target-based metric to [!DNL Analytics] rather than relying only on [!DNL Analytics] data. For example, you can monitor clicking on a page, which is usually not tracked by [!DNL Analytics]. This custom metric is sent to [!DNL Analytics] automatically from the [!DNL Target] server, and appears as the "[!DNL Target] Conversion" metric in the metrics selector in [!DNL Analytics]. The [!DNL Target] Conversion metric is empty if you choose to use [!DNL Analytics] metrics.

   Setting a goal doesn't mean you can't use another metric when evaluating test results. The goal is, however, a reminder of the one thing you want to improve with the activity.

   The visitor remains in the activity after they reach the goal. The visitor continues to see activity content but is not counted as a new activity entry.

   >[!NOTE]
   >
   >When setting up an activity after setting up [!DNL Analytics] as your reporting source, there is no option to set up audiences for reporting. [!DNL Analytics] segments are available in the [!DNL Target] Activities report.

1. Click **[!UICONTROL Save]**.
