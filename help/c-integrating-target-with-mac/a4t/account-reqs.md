---
keywords: Analytics as reporting source;a4t;A4T
description: User account requirements to create an Adobe Analytics-based activity in Adobe Target (A4T).
title: User permission requirements
feature: 
solution: Target,Analytics
topic: Reports and analytics
uuid: cf359bcd-547e-4f8f-bcf6-e646245bb9ce
---

# User permission requirements {#user-permission-requirements}

Information about the user account requirements to create an [!DNL Adobe Analytics]-based activity in [!DNL Adobe Target] (A4T).

Before a report suite can be selected when defining an [!DNL Analytics] activity, you need both an [!DNL Analytics] user account and a [!DNL Target] user account. 

Your user accounts must be configured as described in the following sections:

## Adobe Experience Cloud {#section_3931A2FAD38F4A4FA92CC77B92AF3F0D}

Complete the following tasks in the [!DNL Adobe Experience Cloud] [Admin Console](https://adminconsole.adobe.com):

### Link solution accounts to your Adobe ID

Your [!DNL Analytics] and [!DNL Target] user accounts must be linked to your Adobe ID.

For more information, see [Organizations and account linking](https://docs.adobe.com/help/en/core-services/interface/manage-users-and-products/organizations.html).

### Configure Experience Cloud group membership

You must be a member of one or more [!DNL Experience Cloud] groups that have access to [!DNL Analytics] and [!DNL Target].

For more information, see [Manage Experience Cloud users and products](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/admin-getting-started.html).

## Adobe Analytics {#section_8F404FDE9A634534AB0AA4CB3075582B}

Complete the following tasks in [!DNL Adobe Analytics]:

### Configure access to the Analytics report suite

Before creating or viewing reports for an [!DNL Analytics]-powered activity, you must be a member of the **[!UICONTROL All Report Access]** group, or a member of a group that has access to at least one report in the report suite that you want to use. If you are unable to view reports, make sure you are a member of one of these groups.

For more information, see [Product profiles and groups](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/admin-getting-started.html#section_AB50558124D541CF80A0D3D76D35A4BF). 

### Configure access to the Web Services Access Group

You must belong to the Web Services Access group in [!DNL Analytics] to be able to use [!DNL Analytics] as the reporting source for [!DNL Target].

## Adobe Target {#section_26BA212D8D40443E9EE2AB327091425C}

No additional privileges are required.
