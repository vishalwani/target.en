---
keywords: recommendation key;recommendation logic;current category;custom attribute;last purchased item;last viewed item;most viewed item;most viewed item;favorite category;popularity;recently viewed item;last purchased;last viewed;most viewed;favorite;recently viewed
description: Recommendations based on keys use visitor behavior context to show relevant results in Adobe Target Recommendations activities.
title: Base the recommendation on a recommendation key
feature: criteria
mini-toc-levels: 2
---

# Base the recommendation on a recommendation key

Recommendations based on keys use visitor behavior context to show relevant results in [!DNL Adobe Target] [!DNL Recommendations] activities. 

There are two types of Recommendations:

* **Popularity:** Lists items according to Most Viewed, Top Sold, and Top Metric. The key is empty for popularity criteria. 
* **Key-based:** Comprises the rest of the criteria. Recommendations offers a diverse set of choices with regard to the key type. The options range from "current item" to "profile parameters," which allow you to programmatically set the key of the values to recommend. You can test multiple criteria against each other by basing each criteria on a different key.

Each criteria is defined in its own tab. Traffic is split evenly across your different criteria tests. In other words, if you have two criteria, traffic is divided equally between them. If you have two criteria and two designs, traffic is split evenly between the four combinations. You can also specify a percentage of site visitors who see the default content, for comparison. In that case, the specified percentage of visitors see the default content, and the rest are split between your criteria and design combinations. 

1. Create a new criteria, or select an existing criteria and click **[!UICONTROL Edit]**.
1. To change the recommendation key, select the new key from the [!UICONTROL Recommendation Key] drop-down list, then click **[!UICONTROL Save]** or **[!UICONTROL Update]**.

   Because different logic maps to different recommendations keys, different recommendations lend themselves to placement on different types of pages. Refer to the following sections for more information about each recommendation key.

## Recommendation keys

The following recommendation keys are available from the [!UICONTROL Recommendation Key] drop-down list:

### Current Item

The recommendation is determined by the item the visitor is currently viewing. 

Recommendations display other items that might interest visitors who are interested in the specified item.

When this option is selected, the `entity.id` value must be passed as a parameter in the display mbox.

#### Logic (Criteria)

* [!UICONTROL Items with similar attributes]
* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]
* [!UICONTROL Site Affinity]

#### Where to use on your site

* Single-item pages, such as product pages.
* Do NOT use on null search results pages.

### Current Category

The recommendation is determined by the product category that the visitor is currently viewing.

Recommendations display items in the specified product category.

When this option is selected, the `entity.categoryId` value must be passed as a parameter to the display mbox.

#### Logic (Criteria)

* Top Sellers
* Most Viewed

#### Where to use on your site

* Single-category pages.
* Do NOT use on null search results pages.

### Custom Attribute {#custom}

Recommendation is determined by an item that is stored in a visitor's profile, using either user.*x* or profile.*x* attributes.

When this option is selected, the `entity.id` value must be present in the profile attribute.

#### Logic (Criteria)

* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]
* [!UICONTROL Overall behavior]
* [!UICONTROL Most Viewed]
* [!UICONTROL Top Sellers]

If the key is a custom profile attribute and the algorithm type is Most Viewed or Top Sellers, a new drop-down list that displays called "Group By Unique Value Of" that has a list of known entity attributes (except ID, category, margin, value, inventory, and environment). This field is required.

#### Where to use on your site

* Can be used on any pages.

#### Custom recommendations key

You can base recommendations on the value of a custom profile attribute. For example, suppose that you want to display recommended movies based on the movie that a visitor most recently added to his or her queue.

1. Select your custom profile attribute from the **[!UICONTROL Recommendation Key]** drop-down list (for example, “Last Show Added to Watchlist”).
1. Then select your **[!UICONTROL Recommendation Logic]** (for example "People Who Viewed This, Viewed That").

   ![Create new criteria dialog box](/help/c-recommendations/c-algorithms/assets/create-new-criteria-1.png)

If your custom profile attribute doesn't directly match to a single entity ID, it is necessary to explain to [!DNL Recommendations] how you want the match to an entity to occur. For example, suppose that you want to display the top selling items from a visitor’s favorite brand.

1. Select your custom profile attribute from the **[!UICONTROL Recommendation Key]** drop-down list (for example, “Favorite Brand”).

1. Then select the **[!UICONTROL Recommendation Logic]** you want to use with this key (for example, "Top Sellers").

   The [!UICONTROL Group By Unique Value Of] option displays. 

1. Select the entity attribute that matches to the key you’ve chosen. In this case “Favorite Brand” matches to `entity.brand`.

   [!DNL Recommendations] now produces a “Top Sellers” list for each brand and shows the visitor the appropriate “Top Sellers” list based on the value stored in the visitor's Favorite Brand profile attribute.

   ![Create new criteria dialog box 2](/help/c-recommendations/c-algorithms/assets/create-new-criteria-2.png)

### Last Purchased Item

The recommendation is determined by the last item that was purchased by each unique visitor. This is captured automatically, so no values need to be passed on the page.

#### Logic (Criteria)

* [!UICONTROL Items with similar attributes]
* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]
* [!UICONTROL Site Affinity]

#### Where to use on your site

* Home page, My Account page, offsite ads.
* Do NOT use on product pages or pages relevant to purchases.

### Last Viewed Item

The recommendation is determined by the last item that was viewed by each unique visitor. This is captured automatically, so no values need to be passed on the page.

#### Logic (Criteria)

* [!UICONTROL Items with similar attributes]
* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]
* [!UICONTROL Site Affinity]

#### Where to use on your site

* Home page, My Account page, offsite ads.
* Do NOT use on product pages or pages relevant to purchases.

### Most Viewed Item

The recommendation is determined by the item that has been viewed most often, using the same method as used for favorite category.

This is determined by recency/frequency criteria that works as follows:

* 10 points for first product view
* 5 points for every subsequent view
* At end of session divide all values by 2

For example, viewing surfboardA then surfboardB in one session results in A: 10, B: 5. When the session ends, you will have A: 5, B: 2.5. If you view the same items in the next session, the values change to A: 15 B: 7.5.

#### Logic (Criteria)

* [!UICONTROL Items with similar attributes]
* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]
* [!UICONTROL Site Affinity]

#### Where to use on your site

* General pages, such as home or landing pages and offsite ads.

### Favorite Category

The recommendation is determined by the category that has received the most activity, using the same method used for "most viewed item" except that categories are scored instead of products.

This is determined by recency/frequency criteria that works as follows:

* 10 points for first category view
* 5 points for every subsequent view

Categories visited for the first time are given 10 points. 5 points are given for subsequent visits to the same category. With each visit, non-current categories that have been viewed before are decremented by 1.

For example, viewing categoryA then categoryB in one session results in A: 9, B: 10. If you view the same items in the next session, the values change to A: 20 B: 9.

#### Logic (Criteria)

* [!UICONTROL Top Sellers]
* [!UICONTROL Most Viewed]

#### Where to use on your site

* General pages, such as home or landing pages and offsite ads.

### Popularity

The recommendation is determined by the popularity of items on your site. Popularity includes top sellers and top viewed by mbox data and, if you use Adobe Analytics, all of the metrics available in the product report. Items are ranked based on the Recommendation Logic you select.

#### Logic (Criteria)

* [!UICONTROL Top Sellers]
* [!UICONTROL Most Viewed]
* Product report metrics (if you are using Adobe Analytics)

#### Where to use on your site

* General pages, such as home or landing pages and offsite ads.

### Recently Viewed Items {#recently-viewed}

Uses the visitor's history (spanning sessions) to present the last *x* items the visitor has viewed, based on the number of slots in the design.

The Recently Viewed Items criteria now returns results specific to a given [environment](/help/administrating-target/hosts.md). If two sites belong to different environments and a visitor switches between the two sites, each site shows only recently viewed items from the appropriate site. If two sites are in the same environment and a visitor switches between the two sites, the visitor will see the same recently viewed items for both sites.

#### Where to use on your site

* General pages, such as home or landing pages and offsite ads.

>[!NOTE]
>
>Recently Viewed Items respects both Exclusions global settings and the selected Collection setting for the Activity. If an item is excluded by a global Exclusion, or is not contained in the selected Collection, it will not be displayed; therefore, when using a Recently Viewed Items criteria, the "All Collections" setting should generally be used.

## Recommendation logic

The following recommendation logic (criteria) are available from the [!UICONTROL Recommendation Logic] drop-down list:

### Items with Similar Attributes

Content similarity compares item attribute keywords and makes recommendations based on how many keywords different items have in common. Recommendations based on content similarity do not require past data to deliver strong results.

Using content similarity to generate recommendations is especially effective for new items, which are not likely to show up in recommendations using People Who Viewed This, Viewed That, and other logic based on past behavior. You can also use content similarity to generate useful recommendations for new visitors, who have no past purchases or other historical data.

For more information, see [Content Similarity](/help/c-recommendations/c-algorithms/create-new-algorithm.md#similarity).

This logic can be used with the following recommendation keys:

* Current Item
* Last Item Purchased
* Last Viewed Item
* Most Viewed Item

### Most Viewed

Displays the most-viewed items on your site.

This logic lets you display recommendations based on the most-viewed items on your site to increase conversions for other items. For example, a media site could display recommendations on its home page for its most popular videos to encourage visitors to watch additional videos.

This logic can be used with the following recommendation keys:

* Current Category
* Custom Attribute
* Favorite Category
* Popularity

### People Who Bought This, Bought That

Displays items that other visitors also bought who bought the selected item.

This logic lets you increase cross-selling opportunities by displaying a recommendation on a shopping cart summary page, for example, that displays items that other buyers also purchased. For example if the visitor is purchasing a suit, the recommendation could display additional items other visitors purchased, such as ties, dress shoes, and cufflinks. As visitors review their purchases, you provide them with additional purchasing recommendations.

This logic can be used with the following recommendation keys:

* Current Item
* Custom Attribute
* Last Purchased Item
* Last Viewed Item
* Most Viewed Item

### People Who Viewed This, Bought That

Displays other items bought by visitors who viewed the selected item.

This logic lets you increase cross-selling opportunities by displaying a recommendation on a product page, for example, that displays items that other visitors who viewed the item purchased. For example if the visitor is viewing a fishing pole, the recommendation could show additional items other visitors viewing the item purchased, such as tackle boxes, waders, and fishing lures. As visitors browse your site, you provide them with additional purchasing recommendations.

This logic can be used with the following recommendation keys:

* Current Item
* Custom Attribute
* Last Purchased Item
* Last Viewed Item
* Most Viewed Item

### People Who Viewed This, Viewed That

Displays items that other visitors also viewed who viewed the selected item.

This logic lets you create additional conversion opportunities by recommending items that other visitors who viewed an item also viewed. For example, visitors who view road bikes on your site might also look at bike helmets, cycling kits, locks, and so forth. You can create a recommendation using this logic that suggests other products.

This logic can be used with the following recommendation keys:

* Current Item
* Custom Attribute
* Last Purchased Item
* Last Viewed Item
* Most Viewed Item

### Site Affinity

Displays items using an Adobe proprietary algorithm to recommend other items based on criteria, such as product page views, purchases, and shopping cart activities (adding or removing items, viewing the cart, etc.)

For example an online retailer can recommend items that a visitor has shown interest in during past sessions in subsequent visits. Activity for each visitor's session is captured to calculate an affinity score based on a recency and frequency model. As this visitor returns to your site, site affinity is used to display recommendations based on past actions on your site.

This logic can be used with the following recommendation keys:

* Current Item
* Last Purchased Item
* Last Viewed Item
* Most Viewed Item

### Top Sellers

Displays the top-selling items on your site based on visitor conversions.

This logic lets you create recommendations for popular items on your site to increase conversion. This logic is especially suited for first-time visitors to your site.

This logic can be used with the following recommendation keys:

* Favorite Category
* Popularity
