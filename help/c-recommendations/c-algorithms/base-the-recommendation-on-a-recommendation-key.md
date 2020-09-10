---
keywords: recommendation key;recommendation logic;current category;custom attribute;last purchased item;last viewed item;most viewed item;most viewed item;favorite category;popularity;recently viewed item;last purchased;last viewed;most viewed;favorite;recently viewed
description: Recommendations based on keys utilize visitor behavior context to show relevant results in Adobe Target Recommendations activities.
title: Base the recommendation on a recommendation key
feature: criteria
mini-toc-levels: 2
---

# Base the recommendation on a recommendation key

Recommendations based on keys utilize visitor behavior context to show relevant results in [!DNL Adobe Target] [!DNL Recommendations] activities. 

There are two types of Recommendations:

* **Popularity:** Lists items according to Most Viewed, Top Sold, and Top Metric. The key is empty for popularity criteria. 
* **Key-based:** Comprises the rest of the criteria. Recommendations offers a diverse set of choices with regard to the key type. The options range from "current item" to "profile parameters," which allow you to programmatically set the key of the values to recommend. You can test multiple criteria against each other by basing each criteria on a different key. 

Each criteria is defined in its own tab. Traffic is split evenly across your different criteria tests. In other words, if you have two criteria, traffic is divided equally between them. If you have two criteria and two designs, traffic is split evenly between the four combinations. You can also specify a percentage of site visitors who see the default content, for comparison. In that case, the specified percentage of visitors see the default content, and the rest are split between your criteria and design combinations. 

1. Create a new recommendation, or select an existing recommendation and click **[!UICONTROL Edit]**.
1. To change the recommendation key, select the new key from the [!UICONTROL Recommendation Key] drop-down list, then click **[!UICONTROL Save]**.

   Because different logic maps to different recommendations keys, different recommendations lend themselves to placement on different types of pages. Refer to the following sections for more information about each key.

## Current Item

The recommendation is determined by the item the visitor is currently viewing. 

Recommendations display other items that might interest visitors who are interested in the specified item.

When this option is selected, the `entity.id` value must be passed as a parameter in the display mbox.

### Logic (Criteria)

* [!UICONTROL Items with similar attributes]
* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]
* [!UICONTROL Site Affinity]

### Where to use on your site

Single-item pages, such as product pages.

Do NOT use on null search results pages.

## Current Category

The recommendation is determined by the product category that the visitor is currently viewing.

Recommendations display items in the specified product category.

When this option is selected, the `entity.categoryId` value must be passed as a parameter to the display mbox.

### Logic (Criteria)

* Top Sellers
* Most Viewed

### Where to use on your site

Single-category pages.

Do NOT use on null search results pages.

## Custom Attribute {#custom}

Recommendation is determined by an item that is stored in a visitor's profile, using either user.*x* or profile.*x* attributes.

When this option is selected, the `entity.id` value must be present in the profile attribute.

### Logic (Criteria)

* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]
* [!UICONTROL Overall behavior]
* [!UICONTROL Most Viewed]
* [!UICONTROL Top Sellers]

If the key is a custom profile attribute and the algorithm type is Most Viewed or Top Sellers, a new drop-down list that displays called "Group By Unique Value Of" that has a list of known entity attributes (except ID, category, margin, value, inventory, and environment). This field is required.

### Where to use on your site

Can be used on any pages.

### Use a custom recommendations key

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

## Last Purchased Item

The recommendation is determined by the last item that was purchased by each unique visitor. This is captured automatically, so no values need to be passed on the page.

### Logic (Criteria)

* [!UICONTROL Items with similar attributes]
* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]
* [!UICONTROL Site Affinity]

### Where to use on your site

Home page, My Account page, offsite ads.

Do NOT use on product pages or pages relevant to purchases.

## Last Viewed Item

The recommendation is determined by the last item that was viewed by each unique visitor. This is captured automatically, so no values need to be passed on the page.

### Logic (Criteria)

* [!UICONTROL Items with similar attributes]
* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]
* [!UICONTROL Site Affinity]

### Where to use on your site

Home page, My Account page, offsite ads.

Do NOT use on product pages or pages relevant to purchases.

## Most Viewed Item

The recommendation is determined by the item that has been viewed most often, using the same method as used for favorite category.

This is determined by recency/frequency criteria that works as follows:

* 10 points for first product view
* 5 points for every subsequent view
* At end of session divide all values by 2

For example, viewing surfboardA then surfboardB in one session results in A: 10, B: 5. When the session ends, you will have A: 5, B: 2.5. If you view the same items in the next session, the values change to A: 15 B: 7.5.

### Logic (Criteria)

* [!UICONTROL Items with similar attributes]
* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]
* [!UICONTROL Site Affinity]

### Where to use on your site

General pages, such as home or landing pages and offsite ads.

## Favorite Category

The recommendation is determined by the category that has received the most activity, using the same method used for "most viewed item" except that categories are scored instead of products.

This is determined by recency/frequency criteria that works as follows:

* 10 points for first category view
* 5 points for every subsequent view

Categories visited for the first time are given 10 points. 5 points are given for subsequent visits to the same category. With each visit, non-current categories that have been viewed before are decremented by 1.

For example, viewing categoryA then categoryB in one session results in A: 9, B: 10. If you view the same items in the next session, the values change to A: 20 B: 9.

### Logic (Criteria)

* [!UICONTROL Top Sellers]
* [!UICONTROL Most Viewed]

### Where to use on your site

General pages, such as home or landing pages and offsite ads.

## Popularity

The recommendation is determined by the popularity of items on your site. Popularity includes top sellers and top viewed by mbox data and, if you use Adobe Analytics, all of the metrics available in the product report. Items are ranked based on the Recommendation Logic you select.

### Logic (Criteria)

* [!UICONTROL Top Sellers]
* [!UICONTROL Most Viewed]
* Product report metrics (if you are using Adobe Analytics)

### Where to use on your site

General pages, such as home or landing pages and offsite ads.

## Recently Viewed Items {#recently-viewed}

Uses the visitor's history (spanning sessions) to present the last *x* items the visitor has viewed, based on the number of slots in the design.

The Recently Viewed Items criteria now returns results specific to a given [environment](/help/administrating-target/hosts.md). If two sites belong to different environments and a visitor switches between the two sites, each site shows only recently viewed items from the appropriate site. If two sites are in the same environment and a visitor switches between the two sites, the visitor will see the same recently viewed items for both sites.

### Where to use on your site

General pages, such as home or landing pages and offsite ads.

>[!NOTE]
>
>Recently Viewed Items respects both Exclusions global settings and the selected Collection setting for the Activity. If an item is excluded by a global Exclusion, or is not contained in the selected Collection, it will not be displayed; therefore, when using a Recently Viewed Items criteria, the "All Collections" setting should generally be used.