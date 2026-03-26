---
title: Weights
---

Weighting allows you to prioritise certain fields in your [documents](../../documents-and-files) so that matches in those fields contribute more to the relevance score (see the [Engines and Schema](../engines-and-schema) guide for more information on fields). Weights can only be applied to **text** fields.

## How weights work

Consider two products that reference each other:

---

**Product One**

Title: Cat Ear Headphones

Subtitle: Cute animal-ear headphones

Description: High quality over-ear headphones with a feline quirk.

---

**Product Two**

Title: Halloween Headphones

Subtitle: Witches' cat headphones

Description: Like the Cat Ear Headphones but with a spooky twist ready for your Halloween party

---

In this example the word `cat` appears once in Product One but twice in Product Two. If you were to search for `cat` then, by default, Product Two would appear first as the most relevant because it contains more keyword matches. To avoid this you can add a **weight** to the Title field telling the search that matches in the Title field contribute more to the document score. With a higher weight on Title, Product One would rank above Product Two because its title contains `cat`.

## Weight values

Weights are a number between **0** and **10** (with one decimal place, e.g. 2.5).

- **0** — The field is excluded from search entirely (unsearchable)
- **0.1–10.0** — The field is included in search. Higher values mean matches in that field contribute more to the relevance score
- **Default: 1.0** — All text fields start with a weight of 1.0

## Setting weights

Weights can be configured globally via the dashboard or overridden at query time via the API.

### Global weights (Dashboard)

You can set weights for your engine's text fields in the Silverstripe Search dashboard under **Relevance Tuning**. Each text field displays a toggle to include or exclude it from search and a slider to set its weight from 0 to 10.

<!-- Screenshot: Relevance Tuning page with field weight sliders -->

These weights apply to every search query by default unless overridden at query time.

### Query-time weights (API)

You can override the stored weights for individual search requests by passing `search_fields` in the request body. This is useful when different search features on your site need different field priorities.

When `search_fields` is provided, only the fields you specify are searched — any fields not listed are excluded for that request. If you include a field but do not specify a weight, the default weight of 1.0 is used.

Refer to the [Search API documentation](https://search.silverstripe.cloud/api/v1/docs/#/search/search_post) for request format details or the <a target="_blank" href="https://github.com/silverstripeltd/silverstripe-discoverer/blob/main/docs/detailed-querying.md#search-fields">Discoverer module</a> if you are using the SDK.
