---
keywords: creating custom criteria;algorithms;criteria;recommendations criteria;csv;ftp;upload csv
description: Upload a CSV file to customize your recommendations.
title: Upload custom criteria
feature: criteria
uuid: e0b4d320-db00-43ad-b49e-ce36c8532320
---

# ![PREMIUM](/help/assets/premium.png) Upload custom criteria{#upload-custom-criteria}

Upload a CSV file to customize your recommendations.

## Access the Create New Criteria Screen

There are multiple ways to reach the [!UICONTROL Create New Criteria] screen. Some screen options vary depending on how you reach the screen.

* On the **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** library screen, click **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**. Criteria you create here are automatically made available for all [!DNL Recommendations] activities.
* When you are creating a [!DNL Recommendations] activity using the [!UICONTROL Visual Experience Composer] (VEC), you are immediately taken to the [!UICONTROL Select Criteria] screen after you select an element on your page and click [!UICONTROL Replace w/ Recommendations], [!UICONTROL Insert Recommendations Before], or [!UICONTROL Insert Recommendations After]. You can then select an available criteria or you can click **[!UICONTROL Create Criteria]**. If you create a new criteria, you have the option to save your criteria for use with other [!DNL Recommendations] activities. For more information, see [Create a Recommendations activity](/help/c-recommendations/t-create-recs-activity/create-recs-activity.md).
* When you are editing a [!DNL Recommendations] activity, click in a [!UICONTROL Recommendations Location] box on your page, and select **[!UICONTROL Change Criteria]**. On the [!UICONTROL Select Criteria] screen, click **[!UICONTROL Create Criteria]**. You will have the option to save your new criteria for use with other [!DNL Recommendations] activities.

The following steps assume you access the [!UICONTROL Create New Criteria] screen by using the first method: the **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** library screen.

1. Click **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**.

1. Click **[!UICONTROL Create Criteria]** > **[!UICONTROL Upload Custom Criteria]**.

1. Configure the information in the following sections.

## Basic Information {#info}

1. Type a **[!UICONTROL Criteria Name]**.

   This is the "internal" name used to describe the criteria. For example, you might want to call your criteria "Highest margin products," but you don't want that title to display publicly. See the next step to set the public-facing title.

   ![Basic Information section](/help/c-recommendations/c-algorithms/assets/basic-information.png)

1. Type a public-facing **[!UICONTROL Display Title]** to appear on the page for any recommendations that use this criteria.

   For example, you might want to display "People who viewed this viewed that" or "Similar products" when you use this criteria to show recommendations.

1. Type a short **[!UICONTROL Description]** of the criteria.

   The description should help you identify the criteria and might include information about the purpose of the criteria.

1. Select an industry vertical based on the goals of your recommendations activity.

   | Industry Vertical | Goal |
   |--- |--- |
   |Retail/Ecommerce|Conversion resulting in purchase|
   |Lead Generation/B2B/Financial Services|Conversion with no purchase|
   |Media/Publishing|Engagement|

   Other criteria options will change based on the industry vertical you select. 

1. Select a **[!UICONTROL Page Type]**.

   You can select multiple page types.

   Together, the industry vertical and page types are used to categorize your saved criteria, making it easier to reuse criteria for other [!DNL Recommendations] activities.

1. Select a **[!UICONTROL Recommendation Key]**.

   For more information about basing criteria on a key, see [Base the recommendation on a recommendation key](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md).

1. Select the **[!UICONTROL Recommendation Logic]**.

   For more information about recommendation logic options, see [Criteria](../../c-recommendations/c-algorithms/algorithms.md).

   >[!NOTE]
   >
   >If you select **[!UICONTROL Items]**/ **[!UICONTROL Media with Similar Attributes]**, you will have the option to set [content similarity rules](#similarity).

## Content {#content}

Content rules determine what happens if the number of recommended items does not fill your [recommendations design](/help/c-recommendations/c-design-overview/design-overview.md). It is possible for [!DNL Recommendations] criteria to return fewer recommendations than your design calls for. As an example, if your design has slots for four items, but your criteria causes only two items to be recommended, you can leave the remaining slots empty, or you can use backup recommendations to fill the extra slots.

![Content section](/help/c-recommendations/c-algorithms/assets/content.png)

1. (Optional) Slide the **[!UICONTROL Partial Design Rendering]** toggle to the "on" position.

   As many slots as possible will be filled but the design template might include blank space for remaining slots. If this option is disabled and there is not enough content to fill all available slots, recommendations are not served and default content is displayed instead. 

   Enable this option if you want recommendations served with blank slots. Use backup recommendations if you want recommendation slots to be filled with content based on your criteria with empty slots filled with similar or popular content from your site, as explained in the next step.

1. (Optional) Slide the **[!UICONTROL Show Backup Recommendations]** toggle to the "on" position.

   Fill any remaining empty slots in the design with a random selection of most-viewed products from across your site.

   Using backup recommendations ensures that your recommendation design fill all available slots. Suppose that you have a 4 x 1 design, as illustrated below:

   ![4 x 1 design](/help/c-recommendations/c-design-overview/assets/velocity_example.png)

   Suppose your criteria causes only two items to be recommended. If you enable the [!UICONTROL Partial Design Rendering] option, the fist two slots are filled, but the remaining two slots remain empty. However, if you enable the [!UICONTROL Show Backup Recommendations] option, the first two slots are filled based on your specified criteria and the remaining two slots are filled based on your backup recommendations.

   The following matrix shows the result you'll observe when using the [!UICONTROL Partial Design Rendering] and [!UICONTROL Backup Recommendations] options:

   | Partial Design Rendering | Backup Recommendations | Result |
   |--- |--- |--- |
   |Disabled|Disabled|If fewer recommendations are returned than the design calls for, the recommendations design is replaced by default content and no recommendations are displayed.|
   |Enabled|Disabled|The design is rendered, but may include blank space if fewer recommendations are returned than the design calls for.|
   |Enabled|Enabled|Backup recommendations will fill available design "slots," fully rendering the design.<br>If applying inclusion rules to backup recommendations restricts the number of qualifying backup recommendations to the point that the design cannot be filled, the design is partially rendered.<br>If the criteria does not return any recommendations, and inclusion rules restrict backup recommendations to zero, the design is replaced with default content.|
   |Disabled|Enabled|Backup recommendations will fill available design "slots," fully rendering the design.<br>If applying inclusion rules to backup recommendations restricts the number of qualifying backup recommendations to the point that the design cannot be filled, the design is replaced by default content and no recommendations are displayed.|

   For more information, see [Use a backup recommendation](/help/c-recommendations/c-algorithms/backup-recs.md).

1. (Conditional) If you selected **[!UICONTROL Show Backup Recommendations]** in the previous step, you can enable **[!UICONTROL Apply inclusion rules to backup recommendations]**.

   Inclusion rules determine which items are included in your recommendations. The options available depend on your industry vertical.

   For more details, see [Specify inclusion rules](#inclusion) below.

1. (Optional) Slide the **[!UICONTROL Recommend Previously Purchased Items]** toggle to the "on" position.

   This setting is based on the `productPurchasedId`. The default behavior is to not recommend previously purchased items. In most cases you do not want to promote items a customer has recently purchased. It is useful if you sell items that people typically purchase only once, such as kayaks. If you sell items that people come back to purchase again on a repeated basis, such as shampoo or other personal items, you should enable this option.

## Inclusion Rules {#inclusion}

Several options help you narrow the items that display in your recommendations. You can use inclusion rules while creating criteria or promotions. 

![Inclusion rules](/help/c-recommendations/c-algorithms/assets/inclusion-rules.png)

Inclusion rules are optional; however, setting these details gives you more control over the items that appear in your recommendations. Each detail you configure further narrows the display criteria. 

For example, you can choose to display only women's shoes that have an inventory of more than 50 and a price between $25 and $45. You can also weight each attribute so those items that are more important to your business are most likely to appear. 

As another example, you can choose to display job openings to visitors who visit your site only from certain cities and who have the required college degrees. 

Inclusion rule options vary by industry vertical. By default, inclusion rules are applied to backup recommendations.

>[!IMPORTANT]
>
>You should use inclusion rules cautiously. They are useful if, for example, your organization has rules that demand that one brand is not recommended while another brand is being shown. However, there is an opportunity cost to this feature. You could possibly lose a percentage of lift by restricting some items from not showing when they would normally be shown by the activity criteria. 

The inclusion rules are joined with an AND. All rules must be met to include an item in a recommendation. 

To create a simple inclusion rule, as mentioned previously, to display only women's shoes that have an inventory of more than 50 and a price between $25 and $45, perform the following steps: 

1. Set a price range for the products you want to recommend.
1. Set the minimum inventory amount for the products you want to recommend.
1. Configure the recommendation to display items only when they meet certain criteria.

   ![](assets/Recs_InclusionRules.png)

   You can specify that items are included only when one of the attributes in the list meets or does not match one or more specified conditions. 

   The available evaluators depend on the value you choose in the first drop-down. You can list multiple items. These items are evaluated with OR. 

   Multiple rules are combined with an AND.

   >[!NOTE]
   >
   >This option limits the items that are displayed in the recommendation. It does not affect which pages the recommendation is displayed on. To limit where the recommendation displays, select the pages in the experience composer. 

For more information, see [Use dynamic and static inclusion rules](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md).

## Upload CSV
   
1. Select the **[!UICONTROL Location]** of your CSV file.

    ![Upload CSV section](/help/c-recommendations/c-algorithms/assets/upload-csv.png)

   The CSV file must be formatted correctly to upload successfully. Click **[!UICONTROL Download the CSV template]** to get a correctly formatted CSV file.

   You have two location options:

    * **FTP:** To upload your CSV file from an FTP server, select **[!UICONTROL FTP]**, then enter the required information. You have the option to use SSL, which uses the FTPS protocol to transfer your CSV file securely. 
    * **URL:** To upload your CSV file from a URL, select **[!UICONTROL URL]**, then enter a feed URL.

1. Click **[!UICONTROL Save]**.

   >[!NOTE]
   >
   >Custom criteria entities (rows) can contain up to 1,000 recommended items (columns).

Custom criteria updates are by default "cumulative." New key-value pairs specified in the CSV upload file overwrite existing key-value pairs. Existing key-value pairs that don't have keys specified in the CSV upload will still be available for delivery and will expire in 31 days from the time they are last uploaded as part of the CSV file.

Contact Client Care to enable the setting to discard the existing results that aren't included in the next CSV upload. If this setting is enabled, only the keys present in the custom CSV feed file will be available for delivery. This setting applies to all custom criteria.

Custom criteria feeds update once every 24 hours.

You can see the upload and sync status of your custom criteria upload at the bottom of each criteria card on the Recommendations > Criteria page. You can also see the status in the Edit dialog box when editing custom criteria.

The flow for an error-free upload should be Scheduled > Downloading Feed File > Importing > Successful.

The following are possible error messages you might receive if [!DNL Target] encounters a problem with the upload:

| Error Message | Details |
|--- |--- |
|Unknown Error|Indicates an internal technical error.|
|Parsing Error|There is likely an issue with the feed file format. Correct the file format and re-save the algorithm, which will re-start the file download process.|
|Server Not Found|Provide an IP or Host Name that is visible on the internet.|
|Credentials Error|Provide a valid user and password for an active account on the server.|
|Directory Not Found|Provide a directory that exists on the server.|
|File Not Found|Provide the name of a file that exists on the server in the directory indicated.|

## Training video: Create criteria in Recommendations (12:33) ![Tutorial badge](/help/assets/tutorial.png)

This video contains the following information (details about uploading custom criteria begins at 11:43):

* Create criteria
* Create criteria sequences
* Upload custom criteria

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)