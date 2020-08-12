---
keywords: inclusion rules;inclusion criteria;recommendations;create new criteria;promotion;promotions;dynamic filtering;dynamic;empty values;ignore filtering rule;static filter;filter by value;entity attribute matching;profile attribute matching;parameter matching;filter by value;static filter
description: Information about creating inclusion rules in Adobe Target Recommendations for criteria and promotions, and adding additional dynamic or static filtering rules to achieve better results.
title: Use dynamic and static inclusion rules in Adobe Target Recommendations
feature: 
uuid: f0ee2086-1126-44a4-9379-aa897dc0e06b
---

# ![PREMIUM](/help/assets/premium.png) Use dynamic and static inclusion rules{#use-dynamic-and-static-inclusion-rules}

Information about creating inclusion rules for criteria and promotions, and adding additional dynamic or static filtering rules to achieve better results.

The process for creating and using inclusion rules for criteria and promotions is similar, as are the use cases and examples. Both criteria and promotions and the use of inclusion rules are covered in this topic.

## Adding Filtering Rules to Criteria {#section_CD0D74B8D3BE4A75A78C36CF24A8C57F}

While you are [creating criteria](../../c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE), click **[!UICONTROL Add Filtering Rule]** under **[!UICONTROL Inclusion Rules]**.

![](assets/inclusion_options.png)

The available options vary depending on the selected industry vertical and recommendation key.

## Adding Filtering Rules to Promotions {#section_D59AFB62E2EE423086281CF5D18B1076}

While [creating a promotion](../../c-recommendations/t-create-recs-activity/adding-promotions.md#task_CC5BD28C364742218C1ACAF0D45E0E14), select **[!UICONTROL Promote by Attribute]**, then click **[!UICONTROL Add Filtering Rule]**.

![](assets/inclusion_options_promotion.png)

## Filter Types {#section_0125F1ED10A84C0EB45325122460EBCD}

The following table lists the types of filtering options for both criteria and promotions:

| Type | Option | Available Operators |
|--- |--- |--- |
|**Dynamic Filtering**|**Entity Attribute Matching:** Filter dynamically by comparing a pool of potential recommendations items to a specific item that the users has interacted with.<br>For example, only recommend items that match the current item’s brand.|equals<br>does not equal<br>is between<br>contains<br>does not contain<br>starts with<br>ends with<br>value is present<br>value is not present<br>is greater than or equal to<br>is less than or equal to|
||**Profile Attribute Matching:** Filter dynamically by comparing items (entities) against a value in the user's profile.<br>For example, only recommend items that match the visitor’s favorite brand.|equals<br> does not equal<br>contains<br>does not contain<br>tarts with<br>ends with<br>is greater than or equal to<br>is less than or equal to<br>is between|
||**Parameter Matching:** Filter dynamically by comparing items (entities) against a value in the request (API or mbox).<br>For example, only recommend content that matches the "industry" page parameter.<br>**Important:** If the activity was created before October 31, 2016, its delivery will fail if it uses the "Parameter Matching" filter. To work around this problem:<ul><li>Create a new activity and add your criteria in it.</li><li>Use a criteria that does not contain the "Parameter Matching" filter.</li><li>Remove the "Parameter Matching" filter from your criteria.</li></ul>|equals<br>does not equal<br>contains<br>does not contain<br>starts with<br>ends with<br>is greater than or equal to<br>is less than or equal to<br>s between|
|**Filter by Value**|**Static Filter:** Manually enter one or more static values to filter.<br>For example, only recommend content with an MPAA rating of "G" or "PG."|equals<br>does not equal<br>contains<br>does not contain<br>starts with<br>ends with<br>value is present<br>value is not present<br>is greater than or equal to<br>s less than or equal to|

>[!NOTE]
>
>If you are familiar with how inclusion rules were configured prior to the Target 17.6.1 release (June 2017), you'll notice that some of the options and operators have changed. Only those operators applicable to the selected option display and some operators were renamed ("matches" is now "equals") to be more consistent and intuitive. All existing exclusion rules created prior to this release were automatically migrated into the new structure. No restructuring is necessary on your part.

You can create as many inclusion rules as necessary. The inclusion rules are joined with an AND operator. All rules must be met to include an item in a recommendation.

Dynamic criteria and promotions are much more powerful than static criteria and promotions, and yield better results and engagement. The following examples will give you ideas about how you can use dynamic promotions in your marketing efforts:

**Equals:** Using the "equals" operator in dynamic promotions, when a visitor is viewing an item on your website (such as a product, article, or movie), you can promote other items from:

* the same brand
* the same category
* the same category AND from the house brand
* the same store

**Does Not Equal:** Using the "does not equal" operator in dynamic promotions, when a visitor is viewing an item on your website (such as a product, article, or movie), you can promote other items from:

* a different TV series
* a different genre
* a different product series
* a different style ID

**Is Between:** Using the "is between" operator in dynamic promotions, when a visitor is viewing an item on your website (such as a product, article, or movie), you can promote other items that are:

* more expensive
* less expensive
* cost plus or minus 30%
* later episodes in the same season
* prior books in a series

## Handling Empty Values when Filtering by Entity Attribute Matching, Profile Attribute Matching, and Parameter Matching {#section_7D30E04116DB47BEA6FF840A3424A4C8}

You can choose several options to handle empty values when filtering by Entity Attribute Matching, Profile Attribute Matching, and Parameter Matching for exit criteria and promotions.

Previously, no results were returned if a value was empty. The "If *x* is Empty" drop-down list lets you choose the appropriate action to perform if the criteria has empty values, as shown in the following illustration:

![](assets/empty_value.png)

To select the desired action, hover over the gear icon (![](assets/icon_gear.png)), then choose the desired action:

| Action | Available For | Details |
|--- |--- |--- |
|Ignore this filtering rule|Profile Attribute Matching<br>Parameter Matching|This is the default action for Profile Attribute Matching and Parameter Matching.<br>This option specifies that the rule is ignored. For example, if there are three filtering rules and the third rule doesn't pass any values, instead of not returning any results, you can simply ignore the third rule with the empty values.|
|Do not show any results for this criteria|Entity Attribute Matching<br>Profile Attribute Matching<br>Parameter Matching|This is the default action for Entity Attribute Matching.<br>This action is how Target handled empty values before the addition of this option: no results will be shown for this criteria.|
|Use a static value|Entity Attribute Matching<br>Profile Attribute Matching<br>Parameter Matching|If a value is empty, you can choose to use a static value.|

## Profile Attribute Matching Examples {#section_9873E2F22E094E479569D05AD5BB1D40}

[!UICONTROL Profile Attribute Matching] allows you to recommend only the items that match an attribute from the visitor's profile, as in the examples below.

**Example 1: Recommending items from the user's favorite brand** 
For example, you can use the [!UICONTROL Profile Attribute Matching] option to create a rule that recommends items only where the brand equals the value or text stored in `profile.favoritebrand`. With such a rule, if a visitor is looking at running shorts from a particular brand, only recommendations will display that match that user's favorite brand (the value stored in `profile.favoritebrand` in the visitor's profile).

```
Profile Attribute Matching
brand - equals - the value/text stored in - profile.favoritebrand
```

**Example 2: Matching jobs to job seekers**
Suppose that you're trying to match jobs to job seekers. You want to recommend only jobs that are in the same city as the job seeker.

You can use inclusion rules to match a job seeker's location from his or her visitor's profile to a job listing, as in the following example:

```
Profile Attribute Matching
jobCity - equals - the value/text stored in - profile.usersCity
```

## Entity Attribute Matching Examples 

[!UICONTROL Entity Attribute Matching] allows you to recommend only the items that match an attribute from the item the user is currently viewing, the item the user most recently viewed, the item the user most recently purchased, the item the user most frequently viewed, or from an item stored in a custom attribute in the visitor's profile, as in the examples below.

**Example 3: Upselling to a more expensive product**
Suppose that you're an apparel retailer and want to encourage users to consider higher-priced and therefore more profitable items. You can use the "equals" and "is between" operators to promote more expensive items that are from the same category and the same brand. For example, a visitor seeing running company can promote more expensive running shoes in an effort to up-sell a visitor looking at running shoes.

```
Entity Attribute Matching
category - equals - current item's - category 
And 
Entity Attribute Matching
brand - equals - current item's - brand 
And 
Entity Attribute Matching
value - is between - 100% and 1000% of - current item's - value
```

**Example 4: Promoting private-label products**
You can mix dynamic and static filters to promote private-label products. For example, an office supply company can promote toner cartridges of the company's house brand to drive a more profitable sale for a visitor looking at toner -- and promote pens of the company's house brand to drive a more profitable sale for a visitor looking at pens.

```
Entity Attribute Matching
category - equals - current item's - category 
And
Static Filter
IsHouseBrand - equals - true
```

## Caveats {#section_A889FAF794B7458CA074DEE06DD0E345}

>[!IMPORTANT]
>
>Different data type attributes might not be compatible in dynamic criteria or promotions during runtime with the "equals" and "does not equal" operators. You should use Value, Margin, Inventory, and Environment values wisely on the right hand side if the left hand side has predefined attributes or custom attributes.

![](assets/left_right.png)

The following table shows effective rules and rules that might not be compatible during runtime:

| Compatible Rules | Potentially Incompatible Rules |
|--- |--- |
|value - is between - 90% and 110% of current item's - salesValue|salesValue - is between - 90% and 110% of current item's - value|
|value - is between - 90% and 110% of current item's - value|clearancePrice - is between - 90% and 110% of current item's - margin|
|margin - is between - 90% and 110% of current item's - margin|storeInventory - equals - current item's - inventory|
|inventory - equals - current item's - inventory||
