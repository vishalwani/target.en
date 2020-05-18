---
keywords: report;reports;reporting;experience cloud solution;timezone;time zone;currency;exclude IPs;estimated lift in revenue;revenue;lift in revenue;fine-grained priorities;fine-grained
description: Configure the Adobe Target Visual Experience Composer (VEC) by specifying its general settings, mobile viewport configuration, and CSS selectors.
title: Configure reporting in Adobe Target
topic: Standard
---

# Configure reporting in Target

Configure general settings to use in Target reporting that apply to your entire [!DNL Target] account.

To access the [!UICONTROL Reporting] configuration page, click **[!UICONTROL Administration]** > **[!UICONTROL Reporting].**

You can specify the following settings on this page:

* The Adobe Experience Cloud solution to use for reporting
* The time zone to use for reporting
* The currency to use for reporting
* IP addresses to exclude from reporting
* Whether to show estimated lift in revenue in reporting
* Whether to enable fine-grained priorities

![Reporting page](/help/administrating-target/assets/reporting.png)

## Reporting Cloud Solution

Set options that determine what data is used for your results and reports.

Select the reporting source for your activities, either [!DNL Target] or Adobe Analytics. You can also choose to select your reporting source per activity. 

Consider the following information as you choose your reporting source:

* [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target], and [!UICONTROL Automated Personalization] (AP) activity creation, activation, and deactivation are allowed irrespective of the reporting source selected. These activity types are not supported when you choose [Adobe Analytics as the reporting source for Adobe Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md). Even if you specify Analytics as your reporting source, [!DNL Target] is used as the reporting source for these activity types.
* If the reporting source is set to Analytics here, you are not allowed to activate an activity that uses [!DNL Target] as the reporting source (the reporting source is specified as Target per activity). You must change the reporting source to Analytics in your activity or change the reporting engine to Select Per Activity in Setup > Preferences.
* If the reporting source is set to [!DNL Target] here, you are not allowed to activate an activity that uses Analytics as the reporting source. You must change the reporting source to [!DNL Target] in your activity or change the reporting source to Select Per Activity in Setup > Preferences.
* If the reporting source is set to Select Per Activity here, you can create, activate, and deactivate activities that are supported by the selected reporting source. For a matrix of supported activities, see [Adobe Analytics as the reporting source for Adobe Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T).
* When you switch from A/B Manual to [!UICONTROL Auto-Allocate] or [!UICONTROL Auto-Target], all metrics and reporting audiences are lost if the reporting source of the A/B Manual activity is not supported in [!UICONTROL Auto-Allocate] or [!UICONTROL Auto-Target] activities.

## Timezone for Reporting

Specify the time zone to use for reporting.

## Currency for Reporting

Specify the currency to use for reporting.

## IPs to exclude from Target reporting data

Specify any IP addresses that you want to exclude from reporting data. For example, excluding internal company addresses is a good way to ensure that your reporting data reflects customer interactions on your website.

Enter each IP address on a new line.

## Show estimated lift in revenue

You can choose to show the estimated lift in revenue if you enter a monetary value for your goal. [!DNL Target] can estimate the revenue lift you would attain if all users view the winning experience. The estimated lift feature is disabled by default.

Only Experience Cloud Admin users can enable or disable this feature. If estimated lift is disabled, the corresponding fields do not appear in the interface. Disabling the feature does not result in a loss of data, including the data used for your estimates. The estimates are based on data that is collected whether or not the feature is enabled.

For detailed information, see [Estimating Lift in Revenue](/help/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md).

## Enable fine-grained priorities

Allow numerical entries for priority ranging from 0-999.

Depending on your settings, the UI and options for  Priority  vary. You can use the legacy settings of Low, Medium, or High, or you can enable fine-grained priorities from 0 to 999.

The priority is used if multiple activities are assigned to the same location with the same audience. If two or more activities are assigned to the location, the activity with the highest priority displays.
