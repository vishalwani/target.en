---
keywords: order confirmation;orderConfirmPage
description: The Order Confirmation mbox records details about orders on your site and allows reporting based on revenue and orders. The Order Confirmation mbox can also drive recommendation algorithms, such as "People who bought product x also bought product y."
title: Create an Order Confirmation mbox - mbox.js
feature: 
subtopic: Getting Started
uuid: 001da2bd-2ccf-490b-ba84-ac9b9a2a5451
---

# Create an Order Confirmation mbox - mbox.js{#create-an-order-confirmation-mbox-mbox-js}

The Order Confirmation mbox records details about orders on your site and allows reporting based on revenue and orders. The Order Confirmation mbox can also drive recommendation algorithms, such as "People who bought product x also bought product y."

>[!NOTE]
>
>* If users make purchases on your website, we recommend implementing an Order Confirmation mbox even if you use Analytics for Target (A4T) for your reporting.
>
>* You can also create an Order Confirmation mbox for at.js 1.*x* using the same method; however, the [!DNL at.js] method is preferred. For more information, see [Track Conversions](../../../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#task_E85D2F64FEB84201A594F2288FABF053).
>
>* If you are using at.js 2.*x*, `mboxCreate` is no longer supported. For order confirmation using at.js 2.*x*, use the following tracking-related APIs: [trackEvent()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-trackevent.md) and [sendNotifications()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe.target.sendnotifications-atjs-21.md).

1. In your order details page, insert the mbox script following the model below.
1. Replace the WORDS IN CAPITAL LETTERS with either dynamic or static values from your catalog.

   >[!NOTE]
   >
   >Use comma delimiting to separate multiple product IDs.

   **Tip:** You can also pass order information in any mbox (it does not need to be named `orderConfirmPage`). You can also pass order information in multiple mboxes within the same campaign.

   ```
   <div class="mboxDefault"> 
      <!-- CONTENT TO SHOW IF NO OFFERS AVAILABLE. --> 
   </div> 
   <script type="text/javascript">    
      mboxCreate('orderConfirmPage', 
      'productPurchasedId=PRODUCT ID FROM YOUR ORDER PAGE, PRODUCT ID2, PRODUCT ID3', 
      'orderTotal=ORDER TOTAL FROM YOUR ORDER PAGE', 
      'orderId=ORDER ID FROM YOUR ORDER PAGE'); 
   </script> 
   ```

The Order Confirmation mbox uses the following parameters:

| Parameter | Description |
|--- |--- |
|`orderId`|Unique value to identify an order for conversion counting.<br>The `orderId` must be unique. Duplicate orders are ignored in reports.|
|`orderTotal`|Monetary value of the purchase.<br>Do not pass the currency symbol. Use a decimal point (not a comma) to indicate decimal values.|
|`productPurchasedId` (Optional)|Comma-separated list of product IDs purchased in the order.<br>These product IDs display in the audit report to support additional reporting analysis.|