---
description: >-
  Describes how to use the 7digital APIs to browse the Capitol Music Group
  catalog and stream audio
---

# Using 7Digital API

* **Capitol Music Group and its parent Universal Music Group have made a catalog of their songs available for the hackathon**
  * **≈ 1,500 unique artists \(US and Canadian\)**
  * **≈ 4,500 different albums/singles - all with cover artwork**
  * **≈ 14,000 tracks - all with full length audio streams**
* **The 7digital API’s can be used to**
  * **Browse the catalog by Artist and then find tracks for that artist**
  * **Stream the full-length audio for all tracks**
  * **Access cover artwork image files for all albums and singles in the catalog**
* **Each team will be given an API key and secret to access the APIs**
  * **Only the API key is required to browse the catalog**
  * **However, in order to stream the audio you will need to sign the API call with your key and secret**

**Important Information**

* **You need to add the following parameter to all API calls**
  * **&shopId=2020**
* **When calling track and release endpoints, always use parameter**
  * **&usageTypes=adsupportedstreaming**
* **Terminology**
  * **Release = Album or Single**

![](../.gitbook/assets/capitol-hackaton-7digital-api-overview-master-copy.jpg)

{% api-method method="get" host="http://api.7digital.com/1.2/artist/browse?letter=k&shopId=2020&oauth\_consumer\_key=7d4vr6cgb392" path="" %}
{% api-method-summary %}
artist/browse
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

