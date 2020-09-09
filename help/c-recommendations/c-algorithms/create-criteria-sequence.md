---
keywords: criteria sequence;multiple criteria;algorithms;criteria;recommendations criteria;sequence;
description: Use sequences of up to five criteria to exercise greater control of the items that appear in your Adobe Target Recommendations activities.
title: Create criteria sequences
feature: criteria
uuid: 9a5ca86b-fc79-4c24-b86f-e333b0c63088
---

# ![PREMIUM](/help/assets/premium.png) Create criteria sequences

Use sequences of up to five criteria to exercise greater control of the items that appear in your [!UICONTROL Recommendations] activities.

>[!NOTE]
>
>Criteria sequences cannot be used with [!UICONTROL Recommendations] activities created before the October 2016 Release of [!DNL Target Premium].

To create a criteria sequence, you must first create the criteria you want to include in the sequence. See [Create criteria](/help/c-recommendations/c-algorithms/create-new-algorithm.md) for more information.

By using a criteria sequence, you can provide additional targeted recommendations, instead of using more generic backup recommendations, when a criteria doesn't return enough results to fill your design. Typically, a criteria sequence will proceed from more specific targeting, which might return fewer results, to more general targeting, which usually returns more results.

Your criteria sequences might vary in order depending on the page type, as shown in the following examples:

|Page type|Possible sequence order|
| --- | --- |
|Product page|<ol><li>Based on current item, from same brand</li><li>Based on current item, from all brands</li><li>Based on content similarity</li><li>Based on top sellers</li><li>Based on most-viewed items across the site</li></ol>|
|Home page|<ol><li>Based on visitor's last purchase </li><li>Based on visitor's favorite item</li><li>Based on visitor's favorite category</li><li>Based on top sellers</li><li>Based on most-viewed across site</li></ol>|

## Access the Create Criteria Sequence screen

There are multiple ways to reach the [!UICONTROL Create Criteria Sequence] screen. Some screen options vary depending on how you reach the screen.

* On the **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** library screen, click **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria Sequence]**. Criteria you create here are automatically made available for all [!UICONTROL Recommendations] activities.
* When you are creating a [!UICONTROL Recommendations] activity, from the Select Criteria screen, click **[!UICONTROL Create New]** > **[!UICONTROL Create Criteria Sequence]**. You will have the option to save your new criteria sequence for use with other [!UICONTROL Recommendations] activities. 
* When you are editing a [!UICONTROL Recommendations] activity, click in a [!UICONTROL Recommendations Location] box on your page, then select **[!UICONTROL Change Criteria]**. On the [!UICONTROL Select Criteria] screen, click **[!UICONTROL Create New]** > **[!UICONTROL Create Criteria Sequence]**. You will have the option to save your new criteria for use with other [!UICONTROL Recommendations] activities. 

The following steps assume you access the [!UICONTROL Create Criteria Sequence] screen by using the first method: the **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** library screen.

1. Click **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**.

1. Click **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria Sequence]**.

   ![](assets/CreateCriteriaSequence.png)

## Fill in the Information section

1. Type a **[!UICONTROL Name]** for the sequence.

   This is the "internal" name used to describe the criteria sequence. Visitors to your site will not see this name.

   ![Create Criteria Sequence information section](/help/c-recommendations/c-algorithms/assets/criteria-sequence-info.png) 

1. Type a public-facing **[!UICONTROL Generic Display Title]** to appear on the page if multiple criteria in the sequence are used to fill the [!UICONTROL Recommendations] design.

   For example, you might want to replace "Customers who viewed this also viewed..." with "Recommended for You" if the design might include items based on more than one [!UICONTROL Recommendations] key. 

1. Type a short **[!UICONTROL Description]** of the criteria sequence.

   The description should help you identify the criteria sequence and might include information about its purpose.

1. Select an **[!UICONTROL Industry Vertical]**.

   Your default [industry vertical](/help/c-recommendations/c-algorithms/algorithms.md#section_936BCFCF234C49A2BEC1C38AAC2D71AF) appears automatically.

1. Select a **[!UICONTROL Page Type]**.

   You can select multiple page types.

   Together, the industry vertical and page types are used to categorize your saved criteria sequence, making it easier to reuse sequences for other [!UICONTROL Recommendations] activities.

## Create sequence {#sequence}

The sequence order defines the order in which a design is filled. If Criteria 1 does not have enough recommendations to fill your design, the remaining slots will be filled with Criteria 2, and so on.

1. In the **[!UICONTROL Criteria Sequence]** section, click **[!UICONTROL Add Criteria]**.

   ![Add Criteria](/help/c-recommendations/c-algorithms/assets/add-criteria.png)

1. On the [!UICONTROL Select Criteria] screen, select a criteria.

   You can use the Search box and the filter drop-downs to find the desired criteria.

   ![Select criteria](/help/c-recommendations/c-algorithms/assets/select-criteria.png)

1. Click **[!UICONTROL Add]**.

1. (Optional) Slide the **[!UICONTROL Limit the number of items returned]** toggle to the "on" position, then specify the number of items (between 1 and 50).

   ![Limit the number of items returned toggle](/help/c-recommendations/c-algorithms/assets/limit-number.png)

   To help you understand the value of the [!UICONTROL Limit the number of items returned] option, consider the following use cases:

   * **Use Case 1**: You want to have a mix of different kinds of items in a single recommendations tray. For example, you want to show a mix of outerwear (jackets) and tops (shirts, T-shirts). To achieve this, use a Collection for the activity that includes all of the potential product types you want in any slots in your design. Then, set up your first criteria with a static filter limiting the criteria to include only outerwear, and set up your second criteria with a static filter limiting the criteria to include only tops. Finally, add both criteria to a criteria sequence and limit the first criteria to 2 slots.

     The recommendations tray might look like this on your site:

     ![Featured Products recommendations tray](/help/c-recommendations/c-algorithms/assets/featured-products.png)

   * **Use Case 2**: You want a mix of both alternative items and complementary items. Set up one criteria to use a viewed/viewed algorithm and use a dynamic filter that limits the recommended items to the current item's category. Set up the second criteria to use a viewed/bought algorithm and use a dynamic filter that includes only recommended items that do not match the current item's category. Finally, add both criteria to a sequence and limit the first criteria to 2 slots.

1. Continue adding additional criteria to your sequence. You can add up to five criteria to a sequence. 

## Specify backup content

Choose what content is returned when there aren't enough recommendations available to fill the design template.

When you create a criteria sequence, backup recommendation and partial design rendering settings are ignored for the individual criteria the make up the sequence. To use backup recommendations and partial design rendering you must enable them for the sequence. Select the appropriate toggles. If you choose to allow backup recommendations, you can also choose whether to apply inclusion rules to the backups.

![Backup Content settings](/help/c-recommendations/c-algorithms/assets/backup-content-settings.png)

1. (Optional) Slide the **[!UICONTROL Partial Design Rendering]** toggle to the "on" position.

   As many slots as possible will be filled but the design template might include blank space for remaining slots.

1. (Optional) Slide the **[!UICONTROL Backup Recommendations]** toggle to the "on" position.

   Fill any remaining empty slots in the design with a random selection of most-viewed products from across your site.

   For more information, see [Use a backup recommendation](/help/c-recommendations/c-algorithms/backup-recs.md).

1. (Conditional) If you selected **[!UICONTROL Backup Recommendations]** in the previous step, you can select **[!UICONTROL Apply inclusion rules to backup recommendations]**.

   For more information see [Use dynamic and static inclusion rules](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md).

1. Click **[!UICONTROL Save]**.

   The criteria sequence will appear in the Criteria list.

   For more information about recommendation logic options, see [Criteria](../../c-recommendations/c-algorithms/algorithms.md).

## Training video: Create criteria in Recommendations (12:33) ![Tutorial badge](/help/assets/tutorial.png)

This video contains the following information:

* Create criteria
* Create criteria sequences
* Upload custom criteria

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)
