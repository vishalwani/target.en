---
keywords: mbox functions
description: List of mbox.js functions to use when implementing with mbox.js.
title: mbox.js functions
feature: 
uuid: f503bc44-a664-4d09-82dc-80a1198ad9d0
---

# mbox.js functions{#mbox-js-functions}

List of mbox.js functions to use when implementing with mbox.js.

>[!NOTE]
>
>If you are using [!DNL at.js], these methods do not apply.

| Method | Notes |
|--- |--- |
|`mbox.getName()`||
|`mbox.getURL()`||
|`mbox.getDiv()`|Returns the  div  associated with the mbox (containing default content or an offer)|
|`mbox.getParameters()`|An array of parameters with two fields, name and value|
|`mbox.setOnError()`|Example:<br>`mbox.setOnError(function() { alert(this.getName() +" had error"});`|
|`mbox.setMessage(message)`|You can see message in debug window .|
|`mboxCurrent.activate()`||
|`mboxCurrent.cancelTimeout()`||
|`mboxCurrent.finalize()`||
|`mboxCurrent.getDefaultDiv()`||
|`mboxCurrent.getDiv()`|Returns the  div  associated with the mbox (containing default content or an offer)|
|`mboxCurrent.getEventTimes()`||
|`mboxCurrent.getFetcher()`||
|`mboxCurrent.getId()`||
|`mboxCurrent.getImportName()`||
|`mboxCurrent.getName()`||
|`mboxCurrent.getOffer()`||
|`mboxCurrent.getParameters()`|An array of parameters with two fields, name and value .|
|`mboxCurrent.getURL()`||
|`mboxCurrent.getURLBuilder()`||
|`mboxCurrent.hide()`||
|`mboxCurrent.isActivated`()||
|`mboxCurrent.load()`||
|`mboxCurrent.loaded()`||
|`mboxCurrent.setEventTime()`||
|`mboxCurrent.setFetcher()`||
|`mboxCurrent.setMessage()`||
|`mboxCurrent.setMessage(message)`|View message in debug window .|
|`mboxCurrent.setOffer()`||
|`mboxCurrent.setOnError()`|Example:<br>`mboxCurrent.setOnError(function(){ alert(this.getName() +" had error"});`|
|`mboxCurrent.setOnLoad()`|Example:<br>`mboxCurrent.setOnLoad(function(){alert(this.getName()+" loaded")});`|
|`mboxCurrent.show()`||
|`mboxCurrent.showContent()`||
|`mboxFactoryDefault.addOnLoad(action)`|Action is called when page loads.|
|`mboxFactoryDefault.getMboxes().each()`|Example:<br>`mboxFactoryDefault.getMboxes().each(function() { alert(mbox.getName()) };`|
|`mboxFactoryDefault.getMboxes().length()`||
|`mboxFactoryDefault.getPageId()`||
|`mboxFactoryDefault.getPCId().getId()`||
|`mboxFactoryDefault.getSessionId().getId()`||
|`mboxFactories.get('default').getSessionId()​.forceId("1276011116668");`||
|`mboxFactories.get('default').getPCId()​.forceId("1276011116668");`||
|`mboxFactoryDefault.create()`||
|`mboxFactoryDefault.disable()`||
|`mboxFactoryDefault.enable()`||
|`mboxFactoryDefault.get()`||
|`mboxFactoryDefault.getCookieManager()`||
|`mboxFactoryDefault.getDisableReason()`||
|`mboxFactoryDefault.getEllapsedTime()`||
|`mboxFactoryDefault.getEllapsedTimeUntil()`||
|`mboxFactoryDefault.getMboxes()`|Returns an `mboxList`.|
|`mboxFactoryDefault.getSignaler()`||
|`mboxFactoryDefault.getURLBuilder()`||
|`mboxFactoryDefault.isAdmin()`||
|`mboxFactoryDefault.isDomLoaded()`||
|`mboxFactoryDefault.isEnabled()`||
|`mboxFactoryDefault.isSupported()`||
|`mboxFactoryDefault.limitTraffic()`||
|`mboxFactoryDefault.update()`||
|`mboxFactoryDefault.getCookieManager()​.getCookie("name")//!= null) {`||
|`mboxFactoryDefault.getCookieManager()​.setCookie(_name,_value, _duration);`||