---
keywords: behavioral data source;analytics;recommendations;criteria;product variables
description: Using Adobe Analytics as the behavioral data source lets clients use the view-based and/or purchase-based behavioral data from Analytics in Adobe Recommendations.
title: Using Adobe Analytics with Target Recommendations
feature: criteria
---

# Use Adobe Analytics with Recommendations

Using [!DNL Adobe Analytics] as the behavioral data source lets clients use the view-based and/or purchase-based behavioral data from [!DNL Analytics] in [!DNL Adobe Target] recommendations activities. This feature is especially helpful in situations where the [!DNL Target Recommendations] setup is new and [!DNL Analytics] has a lot of historical data to leverage.

Using [!DNL Analytics] as the behavioral data source can act as a rich source of information about user behavior. This might include data from a third-party source or feed that is shared only with [!DNL Analytics].

While [creating criteria](/help/c-recommendations/c-algorithms/create-new-algorithm.md) in Recommendations, there are two radio button that let you choose which data source is to be used: [!UICONTROL mboxes] or [!UICONTROL Analytics].

![Behavioral data source buttons](/help/c-recommendations/c-algorithms/assets/behavioral-data-source.png)

>[!NOTE]
>
>If these two buttons do not display in your account, reach out to [Customer Care](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

## Use Cases

Using [!DNL Analytics] as the behavioral data source for recommendations also provides the ability to deploy specific use cases without the requirement of tagging entity pages with all the [!DNL Target] entity parameters. Although that requires certain pre-requisites to be in place, availability of "Product Variables" is the most important thing for that functionality to work seamlessly. Regular eVars and Props are not sufficient for this handshake to happen automatically between [!DNL Analytics] and [!DNL Target].

You can use [!DNL Analytics] as the behavioral data source to:

* Display recommendations on a retail site to users on a PDP page, based on what other users purchased from the same category in the last month, using Analytics data.
* Display content on the home screen of a media site for the most popular content in a particular category that is currently trending, based on [!DNL Analytics] data.

## Implementation in Analytics

The following sections will help you implement this feature on the [!DNL Analytics] side.

### Prerequisites: product variables in Analytics

You must implement product variables in [!DNL Analytics] with the necessary attributes that are required for [!DNL Target Recommendations]. 

A [!DNL Target Recommendations] sample feed format will act as guide on which all attributes need to be defined in the product variables. Later those values must be "mapped" within the [!DNL Target] UI for the respective [!DNL Target] entity values.

>[!NOTE]
>
>If it is a content site, the respective content pieces must be treated as "products" and associated attributes about that content (example: author name, publish date, content title, month of release, etc.) must be passed as attributes. Granularity of category level, or category types, should be decided by the business based on use-case requirements.
  
For more details on how to set up product variables, see [products](https://docs.adobe.com/content/help/en/analytics/implementation/vars/page-vars/products.html) in the *Analytics Implementation Guide*. Some of the notes in that documentation need discretion of the team who is deploying it (example : Category). It is always advised to consult with Adobe before doing this activity.

### Considerations

[!DNL Analytics] data is sent via a daily feed. Behavioral results will take up to 24 hours to be reflected within recommendations results on your site. As with all [!DNL Recommendations] criteria settings, this data source can and should be tested.

For quick decision making on which data source is to be used, if there is a lot of organic data generated every day by users, and not much dependency required on historic data, then using a [!DNL Target] mbox as the behavioral data source can be a good fit. In cases of less availability of organic data generated recently, if you want to bank upon [!DNL Analytics] data, then the using [!DNL Analytics] as the behavioral data source is a good fit.

### Steps to deploy

Assuming all the pre-requisites are in place, perform the following tasks:

1. In [!DNL Target], click **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** to acquire your [!DNL Target] client code.

   ![Client code](/help/c-recommendations/c-algorithms/assets/client-code.png)

1. Acquire your [!DNL Analytics] report suite.

   Use your [!DNL Analytics] production site report suite. This is the report suite that tracks the site in which you have [!DNL Recommendations] deployed.

1. In [!DNL Analytics], click **[!UICONTROL Admin]** > **[!UICONTROL Data Feeds]**.

   ![Setup > Data Feeds](/help/c-recommendations/c-algorithms/assets/data-feed.png)

1. Click **[!UICONTROL Add]** to create a new feed.

   ![Add feed](/help/c-recommendations/c-algorithms/assets/add-feed.png)

1. Fill in feed information:

   * **Name**: Recs Prod Feed
   * **Report Suite**: Your pre-determined report suite
   * **Email**: Specify any appropriate address for an Admin user
   * **Feed interval**: Select the desired interval
   * **Delay Processing**: No delay.
   * **Start & End Dates**: Continuous feed

   ![Feed information section](/help/c-recommendations/c-algorithms/assets/feed-information.png)

1. Fill in the details in the **[!UICONTROL Destination]** section:

   >[!NOTE]
   > 
   >Consult with the [!DNL Adobe Analytics] team before doing this step.

   * **Type**: FTP
   * **Host**: xxx.yyy.com
   * **Path**: Your Target client code
   * **Username**: xxxyyy
   * **Password**: xxxxxxxxxxx

   Screenshot is for reference purposes only. Your deployment will have different credentials. Consult with the [!DNL Adobe Analytics] team or Customer Care while doing this step.

   ![Destination section](/help/c-recommendations/c-algorithms/assets/destination.png)

1. Fill in the **[!UICONTROL Data Column]** definitions:

   * **Compression Format**: Gzip
   * **Packaging Type**:  Single File
   * **Manifest:** Finish File

     ![Compression Format, Packaging Type, and Manifest settings](/help/c-recommendations/c-algorithms/assets/compression.png)

   * **Included Columns**: 

     >[!IMPORTANT]
     >
     >The columns must be added in the same order documented here. Select the columns in the following order and click **[!UICONTROL Add]** for each column.

     * hit_time_gmt
     * visid_high
     * visid_low
     * event_list
     * product_list
     * visit_num

1. Click **[!UICONTROL Save]**.

   ![Data column definitions section](/help/c-recommendations/c-algorithms/assets/data-column-definitions.png)

With this, the set up on [!DNL Analytics] side is complete. Now it is time to map these variables on [!DNL Target] side for continuous supply of behavioral data.

## Implementation in Target

1. In Target, click **[!UICONTROL Recommendations]**, then click the **[!UICONTROL Feeds]** tab.

   ![Feeds](/help/c-recommendations/c-algorithms/assets/feeds-tab.png)

1. Click **[!UICONTROL Create Feed]**.

1. Select **[!UICONTROL Analytics Classifications]**, then specify the report suite.

   ![Analytics Classifications option](/help/c-recommendations/c-algorithms/assets/analytics-classifications.png)

1. Click **[!UICONTROL Mapping]**, then map the field column headers to the appropriate [!UICONTROL Recommendations] field names.

   ![Mapping section](/help/c-recommendations/c-algorithms/assets/mapping.png)

1. Click **[!UICONTROL Save]**.