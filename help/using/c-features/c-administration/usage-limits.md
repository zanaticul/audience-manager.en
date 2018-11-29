---
description: Audience Manager sets a maximum limit on the number of traits, segments, destinations, and algorithmic models that you can create for an account. Limits apply to these items whether created in the user interface or programmatically through API methods. Usage limits help protect Audience Manager from automated processes that may attempt to compromise our APIs or user interface.
seo-description: Audience Manager sets a maximum limit on the number of traits, segments, destinations, and algorithmic models that you can create for an account. Limits apply to these items whether created in the user interface or programmatically through API methods. Usage limits help protect Audience Manager from automated processes that may attempt to compromise our APIs or user interface.
seo-title: Usage Limits
solution: Audience Manager
title: Usage Limits
topic: DIL API
uuid: 50ca4647-0b5c-409c-89fa-4fa1799b3222
index: y
internal: n
snippet: y
---

# Usage Limits{#usage-limits}

Audience Manager sets a maximum limit on the number of traits, segments, destinations, and algorithmic models that you can create for an account. Limits apply to these items whether created in the user interface or programmatically through API methods. Usage limits help protect Audience Manager from automated processes that may attempt to compromise our APIs or user interface.

Contents:

<ul class="simplelist"> 
 <li> <a href="../../c-features/c-administration/usage-limits.md#section_7181B0BBC194402BAC55E6846048D78F"> Item Limits </a> </li> 
 <li> <a href="../../c-features/c-administration/usage-limits.md#section_EBE3D23D14F54408911573211E2ED62D"> Monitor Usage </a> </li> 
 <li> <a href="../../c-features/c-administration/usage-limits.md#section_CAB5B9E4ED0D449A9DD97B04ECEF5838"> Increase Item Limits </a> </li> 
</ul>

## Item Limits {#section_7181B0BBC194402BAC55E6846048D78F}

The tables list the current limits by item type. You cannot create new traits, segments, destinations, or [!UICONTROL Algorithmic Models] if you reach a specific limit for one of these items. If you do reach a limit, you must delete an older item before you can create a new one.

**Trait Limits**

|Trait Type|Maximum Limit|
|--- |--- |
|Total Traits|100,000|
|Total Trait Qualifications|100,000. For more information on trait qualification, see the  Trait Qualifications Reference.|
|Algorithmic|50|
|Rule Based|100,000|
|Onboarded|100,000|
|Folder Traits|2,000|

**Segment Limits**

|Segment Type|Maximum Limit|
|--- |--- |
|Total Segments|20,000|

**Destination Limits**

|Destination Type|Maximum Limit|
|--- |--- |
|Total Destinations|1,000|
|Cookie|1,000|
|URL|1,000|
|S2S|100|
|Adobe Analytics|10|

**Algorithmic Model Limits**

|Item|Maximum Limit|
|--- |--- |
|Total Algorithmic Models|20|
|Algorithmic Models maximum audience size|25,000,000  Note that this limit cannot be increased. You can decrease audience sizes by selecting fewer data sources for the model or by selecting a shorter look-back window.|
|Maximum number of excluded traits for a model|500|

**Folder Limits**

|Item|Maximum Limit|
|--- |--- |
|Trait Folders|2,000.  Your folder structure can be maximum 5 levels deep.|

**Derived Signals Limits**

|Item|Maximum Limit|
|--- |--- |
|Derived Signals|50,000.|

**Company User Accounts Limit**

|Item|Maximum Limit|
|--- |--- |
|Maximum number of user accounts for a company|1,000.|

## Monitor Usage {#section_EBE3D23D14F54408911573211E2ED62D}

You can see usage and limits for your account by going to **[!UICONTROL Administration > Limits]**. Access requires administrator permissions.

![](assets/usage_limits.jpg)

## Increase Item Limits {#section_CAB5B9E4ED0D449A9DD97B04ECEF5838}

The default limits listed here should provide enough capacity for your business needs. If your organization consistently reaches these limits, contact your account representative to discuss an increase. 