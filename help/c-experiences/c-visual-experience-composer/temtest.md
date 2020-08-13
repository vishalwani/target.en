---
keywords: template testing;template;same experience on similar pages;template test
description: If you use a page template to provide structure to your pages, or if your pages contain similar elements, this feature makes it possible to test variations in similarly structured page elements.
title: Include the Same Experience on Similar Pages
feature: experiences 
uuid: 055b276e-2492-40d8-b48e-849dffa93f35
---

# Include the same experience on similar pages{#include-the-same-experience-on-similar-pages}

If you use a page template to provide structure to your pages, or if your pages contain similar elements, this feature makes it possible to test variations in similarly structured page elements.

To work correctly, this feature must be used on pages that have a very similar structure. or contain template elements that are structured the same on all pages.

>[!IMPORTANT]
>
>Using this feature to change elements across dissimilar pages will likely cause unexpected results.

For example, you might use this feature to do one of the following:

* Test a global navigation bar by rearranging or removing elements 
* Remove an item from all product pages that use a particular page template 
* Add a banner to all product pages 
* Change the layout of article template

The following demo video includes information about using a template:

You can specify pages that include the change elements, or apply the change across your site. 

1. Create an activity as described in [Activities](../../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03).
1. To specify the pages where the experience will appear, in the Visual Experience Composer click the gear icon, then select **[!UICONTROL Page Delivery]**.
1. Click **[!UICONTROL Add Template Rule]**, then specify the criteria for the pages you want to add the experience to.

1. Specify the page range. The page range can be one of the following:

    * URL (For more information about how Target evaluates URLs, see [Targets and audiences FAQ](/help/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).)
    * Domain 
    * Path 
    * Hash (#) Fragment (Target the part of a URL that follows the # symbol.) 
    * Query 
    * Parameter

1. Choose an operator.

   The operator specifies how the items after the operator relate to the page range. Available operators are:

    * Contains 
    * Does not contain 
    * Is (case sensitive)
    * Is not
    * Starts with
    * Ends with

1. Type the strings that define where the experience is added, such as the domain or the strings contained in the page name.

   For example, if you select **[!UICONTROL Domain]** and **[!UICONTROL Is (case sensitive)]**, type the domain where you want the experience added to all pages.

   You can include multiple items.

   >[!IMPORTANT]
   >
   >Multiple items use `OR` logic, meaning that any single item in the list makes the condition true.

1. If desired, enter additional criteria by clicking **[!UICONTROL Add Template Rule]** and repeating the procedure in the previous step.

   Multiple criteria are joined with AND logic. Adobe Target adds the experience to all pages that match the specified criteria. 

>[!IMPORTANT]
>
> Target cannot check the pages to make sure they appear as expected, so it is always an important practice when using this feature to test affected pages before making them public.

## Training video: Visual Experience Composer (2 of 2) (7:29) ![Tutorial badge](/help/assets/tutorial.png)

* Rename and duplicate an experience 
* Create a redirect experience 
* Target an activity to a single URL or a group of URLs 
* Create a multi-page activity 
* Preview and build experience for responsive websites 
* Use overlays to highlight types of elements

>[!VIDEO](https://video.tv.adobe.com/v/17401)