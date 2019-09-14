---
title: 'JSON Naming Convention'
date: '2016-02-10'
tags:
  - tech

twittercardoptions: summary
articleenabled: false
musiceventenabled: false
orgaenabled: false
orga:
    ratingValue: 2.5
orgaratingenabled: false
eventenabled: false
personenabled: false
restaurantenabled: false
restaurant:
    acceptsReservations: 'yes'
    priceRange: $
---

As we're getting more and more JSON files, a tip for all you developers.

Using a naming convention for JSON property names can speed up localization.

```json
{
"_id": "556se665255e324e",
"_type": "article",
"displayTitle": "Introduction",
"Title": "Introduction: Localizing JSON"
}
```

Don't want something translated? Start the property name with an underscore or use another naming convention you agree on.

![](/images/JSON.png)