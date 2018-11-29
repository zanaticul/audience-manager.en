---
description: You can send qualified segments to DFP either through a client-side or through a server-side integration. Requirements and related information about both methods are listed below.
seo-description: You can send qualified segments to DFP either through a client-side or through a server-side integration. Requirements and related information about both methods are listed below.
seo-title: Requirements and Methods of Sending Segments to DFP Using Google Publisher Tags (GPT)
solution: Audience Manager
title: Requirements and Methods of Sending Segments to DFP Using Google Publisher Tags (GPT)
uuid: 4b2ea81c-29bb-42d3-93d3-1d8e677790b6
index: y
internal: n
snippet: y
---

# Requirements and Methods of Sending Segments to DFP Using Google Publisher Tags (GPT){#requirements-and-methods-of-sending-segments-to-dfp-using-google-publisher-tags-gpt}

You can send qualified segments to DFP either through a client-side or through a server-side integration. Requirements and related information about both methods are listed below.

<ul class="simplelist"> 
 <li><a href="../../c-integration/gpt-aam-destination/gpt-aam-requirements.md#section_8F4B25C64A914B3A9A6FEEA95F5CEF9B"> Client-Side Integration</a> </li> 
 <li><a href="../../c-integration/gpt-aam-destination/gpt-aam-requirements.md#section_3E1127403A184C7D84B3FA1A1B917A62"> Server-Side Integration</a> </li> 
</ul>

## Client-Side Integration {#section_8F4B25C64A914B3A9A6FEEA95F5CEF9B}

For a client-side integration, you need to set up a [!DNL GPT] destination in Audience Manager. Consider the following points when you want to set up [!DNL GPT] as an Audience Manager destination:

* **Add [!UICONTROL DIL]:** Deploy [!UICONTROL Data Integration Library (DIL)] code on all the pages you want to target. [!UICONTROL DIL] writes Audience Manager segment data and user IDs to cookies that get used by [!DNL GPT] for targeting. 

* **Create a Cookie Destination:** [!DNL GPT] must be set up as a cookie-based destination in Audience Manager. 

* **Implement Cookie Checking Code:** Wrap the [!DNL GPT] `.setTargeting` API method in our recommended [cookie checking code](../../c-integration/gpt-aam-destination/gpt-aam-modify-api.md#concept_276DF2F702BE4D6180C855A7DE304097). This code helps prevent errors by looking for valid AAM cookies before the `.setTargeting` method gets invoked. 

* **Add the AamGpt Function:** The `AamGpt` code captures data from Audience Manager cookies and sends it to [!DNL GPT]. Place the [Audience Manager Code for Google Publisher Tags](../../c-integration/gpt-aam-destination/gpt-aam-aamgpt-code.md#concept_C47C21701F0F437E823BABF4EB89E1DB) ( `AamGpt`) at the top of the page or inside the `<head>` code block. 

  >[!NOTE]
  >
  >The `AamGpt` function is not required if you use your own code to read Audience Manager cookie data.

* **Send Delivery Logs to Audience Manager:** If you want a segment delivery report (optional), provide Audience Manager with a daily log that contains impression-level delivery data. The data can be in a raw format, but each record must contain the Audience Manager UUID. Audience Manager can pick up or receive these via FTP.

**Only Qualified Segments are Sent to GPT**

The amount of data passed in to [!DNL GPT] depends on how many segments a particular user qualifies for. For example, say you set up 100 Audience Manager segments. If a site visitor qualifies for five of them, then only those five segments get sent to [!DNL GPT] (not all 100).

>[!NOTE]
>
>There are no limits to the number of key-values you can send, but the Google request URL does have limits to the number of characters it can accept. See [Setting targeting and sizes with GPT](https://support.google.com/dfp_premium/bin/answer.py?hl=en&answer=1697712).

## Server-Side Integration {#section_3E1127403A184C7D84B3FA1A1B917A62}

Talk to your Audience Manager consultant or Customer Care if you want to set up a server-side integration with [!DNL DFP], using [!DNL GPT]. You'll need to provide your [!DNL DFP] account Network Id and Audience Link Id.

>[!IMPORTANT]
>
>If your web pages are running the [Accelerated Media Pages](https://www.ampproject.org/) ( [!DNL AMP]) library, you must use the server-side integration with Audience Manager. If you are on [!DNL AMP] and have a client-side integration with [!DNL AMP], you must migrate to the server-side integration. Please contact your Audience Manager consultant or Customer Care to discuss migration.

>[!MORE_LIKE_THIS]
>
>* [GPT API Reference Guide](https://support.google.com/dfp_premium/bin/answer.py?hl=en&answer=1650154)