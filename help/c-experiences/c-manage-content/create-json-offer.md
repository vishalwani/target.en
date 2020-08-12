---
keywords: remote offer;create remote offer
description: Create JSON offers in the Offer Library for use in the Form-Based Experience Composer.
title: Create JSON offers
feature: 
topic: Standard
uuid: 4ae3ca34-7661-4c1d-a132-fc446e653b90
---

# Create JSON offers{#create-json-offers}

Create JSON offers in the Offer Library for use in the Form-Based Experience Composer.

JSON offers can be used in form-based activities whereby enabling use cases where Target's decisioning is required to send an offer in JSON format for consumption in SPA framework or server-side integrations.

Consider the following information as you work with JSON offers:

* JSON offers are currently available only for AB and XT activities. 
* JSON offers can be used in form-based activities only. 
* JSON offer can be retrieved directly when you are using the Server Side API, Mobile SDK, or NodeJS SDK. 
* In the browser, JSON offers can be retrieved ONLY via at.js 1.2.3 (or later) and using [getOffer()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffer.md) by filtering actions using the `setJson` action. 
* JSON offers are delivered as native JSON objects rather than as strings. Consumers of these objects are no longer required to handle objects as strings and convert them to JSON objects. 
* JSON offers are not applied automatically as opposed to other offers (such as HTML offers) because JSON offers are non-visual offers. Developers must write code to explicitly get the offer using [getOffer()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffer.md). 
* JSON offers are not supported if you are using mbox.js.

## Creating a JSON Offer {#section_BB9C72D59DEA4EFB97A906AE7569AD7A}

1. Click **[!UICONTROL Offers]**, then select the **[!UICONTROL Code Offers]** tab. 
1. Click **[!UICONTROL Create]** > **[!UICONTROL JSON Offer]**.

   ![](assets/offer-json.png)

1. Type an offer name. 
1. Type or paste your JSON code in the **[!UICONTROL Code]** box. 
1. Click **[!UICONTROL Save]**.

## Example {#section_A54F7BB2B55D4B7ABCD5002E0C72D8C9}

JSON offers are supported only in activities created using the Form-based Experience Composer. Currently the only way to be able to use JSON offers is via direct API calls.

Here is an example:

```
adobe.target.getOffer({ 
  mbox: "some-mbox", 
  success: function(actions) { 
    console.log('Success', actions); 
  }, 
  error: function(status, error) { 
    console.log('Error', status, error); 
  } 
});
```

The actions passed to success callback is an array of object. Assuming that we have a single JSON offer, that has this content:

```
{ 
  "demo": {"a": 1, "b": 2} 
}
```

The actions array will have this structure:

```
[ 
 { 
   action: "setJson", 
   content: [{ 
     "demo": {"a": 1, "b": 2} 
   }] 
 }  
]
```

To extract the JSON offer you iterate through actions and find the action with `setJson` action and then iterate through the content array.

## Use Case {#section_85B07907B51A43239C8E3498EF58B1E5}

Let's say the following JSON offer gets delivered to your web page:

```
{ 
    "_id": "5a65d24d8fafc966921e9169", 
    "index": 0, 
    "guid": "7c006504-c6f7-468d-a46f-f72531ea454c", 
    "isActive": true, 
    "balance": "$2,075.06", 
    "picture": "https://placehold.it/32x32", 
    "tags": [ 
      "esse", 
      "commodo", 
      "excepteur", 
    ], 
    "friends": [ 
      { 
        "id": 0, 
        "name": "Carla Lyons" 
      }, 
      { 
        "id": 1, 
        "name": "Ollie Mooney" 
      }, 
    ], 
    "greeting": "Hello, Stephenson Fernandez! You have 4 unread messages.", 
    "favoriteFruit": "strawberry" 
} 
  
```

The following code shows how to access the "greeting" attribute:

```
adobe.target.getOffer({   
  "mbox": "name_of_mbox", 
  "params": {}, 
  "success": function(offer) {           
        console.log(offer[0].content[0].greeting); 
  },   
  "error": function(status, error) {           
      console.log('Error', status, error); 
  } 
});
```

## Filtering Offers by the JSON Offer Type {#section_52533555BCE6420C8A95EB4EB8907BDE}

You can filter the Offers Library by the JSON offer type by clicking the **[!UICONTROL Type]** drop-down list, then by selecting the **[!UICONTROL JSON]** checkbox.

![](assets/offer-json-filter.png)

