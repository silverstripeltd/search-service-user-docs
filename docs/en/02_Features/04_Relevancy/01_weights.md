---
title: Search Weights
---

Weighting allows you to prioritise a field in your [documents](../../documents-and-files) (see the [Engines and Schema](../engines-and-schema) guide for more information on fields). An example of this could be two products that reference each other:

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

In this example the word `cat` appears once in Product One but twice in Product Two. If you were to search for `cat` then, by default, product two would appear first as the most relevant because it contains more keyword matches. To avoid this you can add a **weight** to the Title field telling the search that matches in the Title field contribute more to the document score.

You can add weights to your searches via code using the <a target="_blank" href="https://github.com/silverstripeltd/silverstripe-discoverer/blob/main/docs/detailed-querying.md#search-fields">Discoverer module from SDK</a>. Larger weight values will mean the weighted field contributes more to the relevance score for a document.
