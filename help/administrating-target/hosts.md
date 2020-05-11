---
keywords: host;hosts;host group;environment;troubleshooting;best practices;ubox;redirects;redirect;whitelist
description: Organize your sites and pre-production environments for easy management and separated reporting.
title: Hosts
topic: Standard
uuid: c7682269-4ec2-4a0f-b053-7e0ec77f4604
---

# Hosts{#hosts}

Organize your sites and pre-production environments for easy management and separated reporting.

The primary goal of host management is to ensure that no inactive content accidentally appears on websites. Host management also lets you separate report data by environment.

A host is any web server (or web domain) from where you serve content during any stage of your project. Any host serving an mbox is recognized.

Hosts are bundled into environments for ease of management. For example, you might have dozens of hosts grouped in two or three environments. The preset environments include Production, Staging, and Development. You can add new environments and rename your environments, if desired.

One environment, the default environment, is pre-named Production. This default environment cannot be deleted, even if you rename it. [!DNL Target] assumes that this is where you will serve final, approved activities and tests.

When an mbox request is received from new websites or domains, these new domains always appear in the Production environment. The Production environment cannot have its settings changed, so unknown or new sites are guaranteed to see only content that is active and ready. Host management also lets you easily ensure the quality of new activities and content in your test, staging, and development environments before you activate the activities.

Target does not limit a host that can send and receive mboxes, so when new servers or domains come up, they automatically work (unless you've set up a whitelist or blacklist). This also enables ad testing on different domains you don't know or can't anticipate.

To manage hosts and environments, click **[!UICONTROL Setup]** > **[!UICONTROL Hosts]**.

![](assets/hosts_list.png)

## Recognizing hosts {#concept_0D4B43E23AA9408F8B28A57ED754BF65}

Information about the conditions that must be met for [!DNL Target] to recognize a host and add it to the Hosts list.

To recognize a host, the following conditions must be met:

* At least one mbox must exist on the host 
* A page on the host must have the following:

    * An accurate [!DNL mbox.js] reference 
    * An mbox or an auto-generated global mbox call

* The page with the mbox must be viewed in a browser

After the page is viewed, the host is listed in the [!UICONTROL Hosts] list, allowing you to manage it in an environment as well as preview and launch activities and tests.

>[!NOTE] {class="- topic/note "}
>
>This includes any personal development servers.

After a host is added to the [!UICONTROL Host] list, make sure that the host is recognized.

1. Click **[!UICONTROL Setup]** > **[!UICONTROL Hosts]**. 
1. If your host is not listed, refresh your browser. 
   By default, a newly recognized host is placed in the Production environment. This is the safest environment because it does not allow inactive activities to be viewed from these hosts. 
1. (Conditional) Move the host into the Development or Staging environment.

>[!NOTE]
>
>The Production environment cannot be deleted, even if you rename it. It is assumed that this is where you will serve final, active activities and tests. The default environment does not allow inactive campaigns to be viewed.

## Manage hosts and environments {#concept_90573F5A52E04600A8C3C5897880C10F}

Information to help you manage hosts and environments (host groups,) including setting the default host for reporting, creating whitelists, changing an environment's name, moving a host to another environment, and deleting a host or environment.


To access the [!UICONTROL Hosts] list, click **[!UICONTROL Setup]** > **[!UICONTROL Hosts]**.

![](assets/hosts_list.png)

## Filter, sort, or search the Hosts list {#section_068B23C9D8224EB78BC3B7C8580251B0}

To filter the [!UICONTROL Hosts] lists by environment, click the **[!UICONTROL All]** drop-down list, then select the desired environment (Production, Staging, Development, or a custom environment you have created).

To sort the [!UICONTROL Hosts] list, click any column header (Name, Environment, or Last Requested) to sort the list in ascending or descending order.

To search the [!UICONTROL Hosts] list, type a search term in the Search box.

## Select multiple hosts {#section_EF3B458475184B7EA997C3559714397C}

To select multiple hosts, select the check boxes next to the [!UICONTROL Name] column for the desired hosts. You can then move or delete all selected hosts.

## Create an environment {#section_32097D0993724DF3A202D164D3F18674}

1. From the [!UICONTROL Hosts] list, click the **[!UICONTROL Environments]** tab. 
1. Click **[!UICONTROL Create Environment]**. 
1. Specify a descriptive name for the environment. 
1. Specify the desired active mode for the environment: [!UICONTROL Active Activities] or [!UICONTROL Active and Inactive Activities]. 
1. Click **[!UICONTROL Save]**.

## Set the default host for reporting {#section_4F8539B07C0C45E886E8525C344D5FB0}

You can select the environment you want to use as the default for all activity reports.

If you use Production as your default, all unknown hosts automatically are added here and report data from there is included in the default report view. Instead, creating a "clean" environment ensures only your core sites/domains are included.

To set the default environment for reporting:

1. From the [!UICONTROL Hosts] list, click the **[!UICONTROL Settings]** tab. 
1. Select the default host from the **[!UICONTROL Environment Settings]** drop-down list. 
1. Click **[!UICONTROL Save]**.

>[!NOTE]
>
>[!DNL Recommendations] users must rebuild their behavior database and product database if hosts switch host groups.

## Create whitelists that specify hosts that are authorized to send mbox calls to Target. {#whitelist}

You can create a whitelist that specifies hosts (domains) that are authorized to send mbox calls to [!DNL Target]. All other hosts generating calls will get a commented-out authorization error response. By default, any host that contains an mbox call registers with [!DNL Target] in the Production environment and has access to all active and approved activities. If this is not the desired approach, you can instead use the whitelist to record specific hosts that are eligible to make mbox calls and receive [!DNL Target] content. All hosts will continue to display in the [!UICONTROL Hosts] list, and environments can still be used to group these hosts and assign different levels to each, such as whether the host can see active and/or inactive campaigns.

To create a whitelist:

1. From the [!UICONTROL Hosts] list, click the **[!UICONTROL Settings]** tab. 
1. Select **[!UICONTROL Enable Authorized Hosts for Content Delivery]** checkbox. 
1. Add the desired hosts in the **[!UICONTROL Host Contains]** box, as desired.

   Multiple hosts can be listed, each on its own line. 

1. Click **[!UICONTROL Save]**.

If an mbox call is made on an unauthorized host, the call will respond with `/* no display - unauthorized mbox host */`.

If you use ubox functionality of [!DNL Target], note that this whitelist will also control the list of domains to which your [redirectors](/help/c-implementing-target/c-non-javascript-based-implementation/working-with-redirectors.md) can navigate. Ensure that you add any domains to which you want to redirect when you use ubox as a part of your implementation. If the whitelist is left unspecified, Adobe will not be able to verify the redirect URLs and protect from potential malicious redirects.

The whitelist takes precedence over environments. You should clear out all hosts before using the whitelist feature, then only the hosts allowed by the whitelist appear in your hosts list. You can then move the hosts into the desired environment.

Sometimes domains from other sites appear in your environments. A domain appears in the list if the domain makes a call to your mbox.js. For example, if somebody copies one of your web pages to their server, that domain appears in your environment. You might also see domains from spider engines, language translator sites, or local disk drives.

In cases where `mboxHost` is passed in an API call, conversion is recorded for the environment that is passed in. If no environment is passed, the host in the call defaults to Production.

You can also create a blacklist that specifies hosts (domains) than cannot send mbox calls to [!DNL Target] by adding the desired hosts in the [!UICONTROL Host Does Not Contain] box.

## Change the name of an environment {#section_9F5F94285F8E495E9CE69810CE94CA08}

1. From the [!UICONTROL Hosts] list, click the **[!UICONTROL Environments]** tab. 
1. Hover over the desired environment, then click the **[!UICONTROL Edit]** icon. 
1. Change the environment name. 
1. Click **[!UICONTROL Save]**.

## Move a host to a different environment {#section_9F52549958BD485EB74FE78C32773D2A}

1. From the [!UICONTROL Hosts] list, hover over the host you want to move. 
1. Click the **[!UICONTROL Move]** icon. 
1. Select the desired environment from the drop-down list, then click the check mark icon.

## Delete a host {#section_F56355BA4BC54B078A1A8179BC954632}

You can delete a host when it is no longer needed.

1. From the [!UICONTROL Hosts] list, hover over the host you want to delete. 
1. Click the **[!UICONTROL Delete]** icon. 
1. Click **[!UICONTROL Delete]** to confirm the deletion.

>[!NOTE]
>
>The host will be listed again if anyone browses to an mboxed page on the host.

## Delete an environment {#section_737F8869612047868D03FC755B1223D3}

You can delete an environment when it is no longer needed.

1. From the [!UICONTROL Hosts] list, click the **[!UICONTROL Environments]** tab. 
1. Hover over the environment you want to delete. 
1. Click the **[!UICONTROL Delete]** icon. 
1. Click **[!UICONTROL Delete]** to confirm the deletion.

>[!NOTE]
>
>You cannot delete the Production environment, but you can rename it.

## Troubleshooting hosts {#concept_B3D7583FA4BB480382CC7453529FE1B7}

Best practices for managing and troubleshooting hosts in [!DNL Adobe Target].

Try the following troubleshooting tips if you experience problems with your hosts:

**Host does not appear in mbox list for your account.**

* Refresh the [!UICONTROL Hosts] page in your browser. 
* Confirm that the mbox code is correct, including the [!DNL mbox.js] reference. 
* Try browsing to one of the mboxes on the host. It's possible that no mbox on the host was ever rendered in a browser.

**Random or unknown domains appear in the [!UICONTROL Host] list.**

A domain appears in this list if a call to [!DNL Target] is made from the domain. Often, you could see domains from spider engines, language translator sites, or local disk drives. If the listed domain is not one your team uses, you can click [!UICONTROL Delete] to remove it.

**My mbox call returns /&#42; no display - unauthorized mbox host &#42;/.**

If an mbox call is made on an unauthorized host, the call will respond with /&#42; no display - unauthorized mbox host &#42;/.

## Recommendations: filter collections and exclusions by environment (host group)

![Premium badge](/help/assets/premium.png)

You can preview the contents of Recommendations collections and exclusions for a selected environment (host group).

>[!NOTE]
>Recommendations activities are available as part of the Target Premium solution. They are not available in Target Standard without a Target Premium license.

The host group can be used to separate the available items in your catalog for different uses. For example, you can use host groups for Development and Production environments, different brands, or different geographies. By default, preview results in Catalog Search, Collections, and Exclusions are based on the default host group. (You can also select a different host group to preview results, by using the Environment filter.) By default, newly added items are available in all host groups unless an environment ID is specified when creating or updating the item. Delivered recommendations depend on the host group specified in the request.

If you don't see your products, make sure that you are using the correct host group. For example, if you set up your recommendation to use a staging environment and you set your host group to Staging, you might need to re-create your collections in the staging environment for the products to show. To see which products are available in each environment, use Catalog Search with each environment. You can also preview the contents of Recommendations collections and exclusions for a selected environment (host group).

>[!NOTE]
>After changing the selected environment, you must click Search to update the returned results.

The Environment filter is available from the following places in the Target UI:

* Catalog Search ([!UICONTROL Recommendations > Catalog Search])
* Create Collection dialog box ([!UICONTROL Recommendations > Collections > Create New])
* Update Collection dialog box ([!UICONTROL Recommendations > Collections > Edit])
* Create Exclusion dialog box ([!UICONTROL Recommendations > Exclusions > Create New])
* Update Exclusion dialog box ([!UICONTROL Recommendations > Exclusions > Edit])
