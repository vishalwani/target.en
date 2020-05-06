---
keywords: troubleshooting;metric discrepancies;FAQ;reports
description: List of frequently asked questions about reporting in Adobe Target.
title: Reporting FAQ for Adobe Target
topic: Standard
uuid: 0be40d3f-3274-493d-899b-cb7bb3612baf
---

# Reporting FAQ{#reporting-faq}

List of frequently asked questions about reporting in [!DNL Target].

## Why do my [!UICONTROL Experience Targeting] (XT) reports contain metrics for control experiences?

XT activities should always have a control experience. If you are using an XT activity in a similar manner to an [!UICONTROL A/B Test] activity, which is a fairly common scenario, the control experience data is useful. You can ignore the control experience data if you find it not useful in your reports.

## Why are the number of visits lower in [!DNL Target] than in other [!DNL Adobe Experience Cloud] solutions? {#section_7E626FDB417E41B8B58BBF30FB207409}

Metric numbers, for example visits, reported by [!DNL Target] will always be lower than the reported numbers in other [!DNL Experience Cloud] solutions for a number of reasons:

* [!DNL Target] counts visits only for visitors that qualified for the activity. Other solutions count visits for visitors that display the page, regardless of which activity brought them to the page. 
* There might be situations where different activities compete for the same location (mutually exclusive). As a result, visitors see different content on a web page, which affects the metric numbers reported by [!DNL Target].

## Why is there no data available for my activity's report? {#section_E4722F6445884130951DF79981C8289B}

If an activity's content was successfully delivered to users but its report contains no data, ensure that you have the correct environment ([host group](/help/administrating-target/hosts.md)) selected in the report's settings.

If you have a development environment selected, you might see the following error message: "There is no data available for the selected report settings."

To change the environment for an activity's report:

1. Click **[!UICONTROL Activities]**, click the desired activity from the list, then click the **[!UICONTROL Reports]** tab. 
1. Click the gear icon to configure report settings.

   ![A/B Settings dialog box](/help/c-reports/c-report-settings/assets/ab_settings_dialog.png)

   >[!NOTE]
   >
   >The gear icon is not available for [!UICONTROL Automated Personalization] (AP) reports.

1. From the **[!UICONTROL Environment]** drop-down list, select **[!UICONTROL Production]**.

   Report data might not be available if you have a development environment selected. 

1. Click **[!UICONTROL Save]**.

For more information about environments, see [Hosts](../administrating-target/hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E).

## Why is the traffic split between my experiences uneven in my A/B or MVT activity? {#uneven}

For example, I set the traffic split to be 50/50 or 25/25/25/25 but I'm seeing a vastly different distribution between experiences in the reporting. There are a number of explainable reasons for uneven visitor counts in [!DNL Target] reporting:

* When a [!DNL Target] activity is first launched, the traffic distribution might be uneven because of the edge node architecture that [!DNL Target] uses to optimize experience delivery. The best practice is to give an activity some time to collect additional data and the distribution will normalize. For more information on [!DNL Adobe Target] architecture and Edge nodes, see [How Adobe Target works](/help/c-intro/how-target-works.md).
* If you are in [!DNL Target] or [!DNL Analytics] and you're using the **[!UICONTROL Visits]** metric, remember that [!DNL Target] is a visitor-based system and the traffic distribution for an A/B or MVT test is assigned at the visitor level. Thus, if you examine activity results using the **[!UICONTROL Visits]** metric, the traffic distribution may appear uneven because certain visitors might have multiple visits. Visitors is the standard normalizing metric when evaluating activity performance.
* The best practice for A/B and MVT tests is to keep traffic splits even. Changing the traffic distribution between experiences (say from 90/10 to 50/50) during a test can lead to uneven visitors across experiences. The lower traffic experience may never "catch up."
* If you are following the above best practices and the traffic split does not normalize over time, you should check the following:

  * Are you using the latest at.js library? For more information about the current version and associated release notes, see [at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).

  * Is it a redirect test? Incorrect timing of tags firing on the page can lead to uneven traffic splits, especially when using [!DNL Analytics] as the data source for a [!DNL Target] activity. For details to remedy uneven traffic distribution on a redirect activity with Analytics for Target (A4T), see [Redirect offers - A4T FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md).
