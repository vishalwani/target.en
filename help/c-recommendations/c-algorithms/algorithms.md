---
keywords: recommendations;recommendations activity;criteria;algorithm;recommendation key;custom key;industry vertical;retail;eccommerce;lead generation;b2b;financial services;media;publishing
description: Criteria in Adobe Target Recommendations are rules that determine which products to recommend based on a predetermined set of visitor behaviors.
title: Criteria in Adobe Target Recommendations
feature: criteria
uuid: 738db164-174b-45b8-bb8a-778f6494f1d7
---

# ![PREMIUM](/help/assets/premium.png) Criteria

Criteria are rules that determine which products to recommend based on a predetermined set of visitor behaviors.

Criteria determine which action will result in which recommendation. You can test multiple recommendation types against each other by adding multiple criteria.

## Industry Vertical {#section_936BCFCF234C49A2BEC1C38AAC2D71AF}

You select an industry vertical based on the goals of your recommendations activity. Depending on the industry vertical you select, 

| Industry Vertical | Goal |
|--- |--- |
|Retail/Ecommerce|Conversion resulting in purchase|
|Lead Generation/B2B/Financial Services|Conversion with no purchase|
|Media/Publishing|Engagement|

## Recommendation key {#section_885B3BB1B43048A88A8926F6B76FC482}

The recommendation key you select determines the criteria type. There are several criteria types, which are represented as criteria cards when you set up a [!DNL Recommendations] activity.

| Criteria Type | Keys |
|--- |--- |
|Current Page Activity|Recommend items based on what users do on the current page. For example, visitors who view a particular article might want to see other articles from the same category.<ul><li>[Current Item](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#current-item)</li><li>[Current Category](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#current-category)</li></ul>|
|Custom|Recommend items based on custom attributes.<ul><li>[Custom Attribute](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#custom)</li></ul>When you base recommendations on custom attributes, you must select the custom attribute and then select the recommendation type.|
|Past Behavior|Recommend items based on how visitors have responded to an item in the past. For example, people who have purchased a particular brand have been more likely to purchase another item from that brand.<ul><li>[Last Purchased Item](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#last-purchased)</li><li>[Last Viewed Item](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#last-viewed)</li><li>[Most Viewed Item](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#most-viewed)</li><li>[Favorite Category](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#favorite-category)</li></ul>|
|Popularity|Recommend the most popular items, such as the most popular videos in a related category or the products that have been viewed most often on your site.<ul><li>[Popularity](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#popularity)</li></ul>|
|Recently Viewed Items|Recommend the items a visitor has viewed most recently, such as the items a visitor looked at the last time he or she visited your site, or the articles that are trending most highly right now.<br>The Recently Viewed Items algorithm returns results specific to a visitor’s activity within an [environment](/help/administrating-target/hosts.md). If two sites belong to different environments and a visitor switches between the two sites, the algorithm will return only recently viewed items from the appropriate site.<br>This criteria type is not limited by collections.<ul><li>[Recently Viewed Items](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#recently-viewed)</li></ul>**Note:** You cannot use the Recently Viewed Items criteria for backup recommendations.<br>Recently Viewed Items/Media can be filtered so that only items with a particular attribute are displayed.<ul><li>Recently Viewed criteria are configurable, like other criteria in recommendations.</li><li>You can use [collections](/help/c-recommendations/c-products/collections.md), [exclusions](/help/c-recommendations/c-products/exclusions.md), and [inclusions](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) (including the special rules for Price and Inventory) in the same way as any other criteria.</li></ul>Possible use-cases include:<ul><li>A multi-national company with multiple businesses might have a visitor view items across multiple digital properties. In this case, you can limit the recently viewed items to display only for the respective property where it was viewed. This prevents Recently Viewed items from displaying on another digital property's site.</li></ul>|

## Using a custom recommendation key {#custom-key}

You can also base recommendations on the value of a custom profile attribute.

>[!NOTE]
>
>Custom profile parameters can be passed to Target through JavaScript, API, or integrations. For more information about custom profile attributes, see [Visitor profiles](/help/c-target/c-visitor-profile/visitor-profile.md).

For example, suppose that you want to display recommended movies based on the movie that a user most recently added to the queue.

1. Select your custom profile attribute from the [!UICONTROL Recommendation Key] drop-down list (for example, [!UICONTROL Last Show Added to Watchlist]).

1. Select your [!UICONTROL Recommendation Logic] (for example, [!UICONTROL People Who Viewed This, Viewed That]).

   ![Create New Criteria dialog box](/help/c-recommendations/c-algorithms/assets/custom-key1.png)

If your custom profile attribute does not directly match to a single entity ID, it is necessary to explain to [!DNL Recommendations] how you want the match to an entity to occur.

For example, suppose that you want to display the top-selling items from a user’s favorite brand.

1. Select your custom profile attribute from the [!UICONTROL Recommendation Key] drop-down list (for example, [!UICONTROL Favorite Brand]).

1. Select the [!UICONTROL Recommendation Logic] you want to use with this key (for example, [!UICONTROL Top Sellers]).

   The [!UICONTROL Group By Unique Value Of] option displays. 

1. Select the entity attribute that matches to the key you’ve chosen. In this case [!UICONTROL Favorite Brand] matches to `entity.brand`.

   [!DNL Recommendations] now produces a “Top Sellers” list for each brand and shows the user the appropriate “Top Sellers” list based on the value stored in the [!UICONTROL Favorite Brand] profile attribute.

   ![Top Sellers attribute](/help/c-recommendations/c-algorithms/assets/custom-key2.png)

## Criteria/algorithms {#criteria-algorithms}

[!DNL Target Recommendations] uses sophisticated algorithms to determine when a visitor's actions qualify for the criteria set in your activity. The recommendation key determines the recommendations logic options that are available.

| Criteria | Description |
|--- |--- |
|[Items/Media with Similar Attributes](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#similar-attributes)|Recommends items or media similar to items or media based on current page activity or past visitor behavior.|
|[People Who Viewed This, Viewed That](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#viewed-viewed)|Recommends items that are most often viewed in the same session that the specified item is viewed.|
|[People Who Viewed This, Bought That](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#viewed-bought)|Recommends items that are most often purchased in the same session that the specified item is viewed.|
|[People Who Bought This, Bought That](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#bought-bought)|Recommends items that are most often purchased by customers at the same time as the specified item.|
|[Site Affinity](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#site-affinity)|Recommends items based on the certainty of a relationship between items.|
|[Top Sellers](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#top-sellers)|The items that are included in the most completed orders. Multiple units of the same item in a single order are counted as one order.|
|[Most Viewed](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#most-viewed)|The items or media that are viewed most often.|
|[User-Based Recommendations](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#user-based)|Recommends items based off of each visitor's browsing, viewing, and purchasing history. These items are generally referred to as "Recommended for You."|

>[!NOTE]
>
>If you are running a recommendation and change its criteria, you will lose your reporting data.

You can also use additional known information about a visitor to enhance your recommendations.

All one-day criteria run twice daily. All one-week and longer criteria run once daily. Site Affinity criteria run once daily. Backup criteria run twice daily.

## Viewing criteria information {#section_7162DE58E4594FD688A4D7FDB829FD8B}

You can view criteria details on a pop-up card by hovering over a card and by clicking the Information icon on a criteria card without opening the criteria.

![Criteria Card hover](/help/c-recommendations/c-algorithms/assets/criteria_hover.png)

Click the **[!UICONTROL Algorithm Info]** tab to view general information about the selected criteria, including its Name, Descriptions, Industry Vertical, Page Type(s), Recommendation Key, Recommendation Logic, and Algorithm ID.

![Algorithm Info tab](/help/c-recommendations/c-algorithms/assets/criteria_info.png)

Click the **[!UICONTROL Algorithm Usage]** tab to view a list of activities that reference the selected criteria. The card lists active, inactive, and draft activities. Click the Live Activities/Inactive Activities/Draft Activities drop-down lists to view the entire list of activities that reference that criteria. You can click the activity link to open the activity for editing.

![Algorithm Usage tab](/help/c-recommendations/c-algorithms/assets/criteria_usage.png)

>[!NOTE]
>
>The [!UICONTROL Algorithm Usage] feature is currently supported for Recommendations activities only. This feature is not currently supported for A/B Test, Auto-Allocate, Auto-Target, and Experience Targeting (XT) activities that include [recommendations as an offer](/help/c-recommendations/recommendations-as-an-offer.md).
