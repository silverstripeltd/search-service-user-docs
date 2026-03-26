---
title: Boosts
---
> [!NOTE]
> Features on this page are only supported on plans with Analyst features. For more information, refer to [Features](/features)

Boosts let you promote certain results by increasing their relevance score. Unlike [weights](./weights), which prioritise specific fields, boosts promote documents that match certain **criteria** such as a particular value, proximity to a point in time or space, or recency.

For example, you could boost documents in a _"Featured"_ category so they appear higher in results, or boost more recently published content so that fresh articles surface first.

## Boost types

Silverstripe Search supports two types of boost:

### Value boosts

A value boost increases the relevance score of documents where a field matches one or more specific values. This is useful when you want to promote content based on known attributes.

**Example:** You have a `category` field and want to promote _"Premium"_ products in search results. Adding a value boost on the `category` field with a value of _"Premium"_ will increase the score for those documents.

Value boosts can be applied to **text**, **number**, and **date** fields.

### Proximity boosts

A proximity boost increases the relevance score of documents based on how close a field's value is to a given **center** point. The closer the value is to the center, the higher the boost. This is sometimes called a **decay function** because the boost effect decays with distance.

Proximity boosts are commonly used for:

- **Recency** — Boost documents with a date field close to _now_ so that recent content ranks higher. For example, setting the center to today's date on a `published_date` field will favour newer articles.
- **Geographic proximity** — Boost documents with a geolocation field close to the user's location so that nearby results rank higher.
- **Numeric proximity** — Boost documents with a numeric field close to a target value.

Proximity boosts can be applied to **number**, **date**, and **geolocation** fields.

#### Decay functions

When configuring a proximity boost you can choose a **decay function** that controls how quickly the boost falls off as values move away from the center:

- **Gaussian** — A bell curve; the boost drops off gently near the center and more steeply further away. Good for most use cases.
- **Exponential** — The boost drops off quickly and consistently. Good when you want a sharp penalty for distance.
- **Linear** — The boost drops off at a constant rate. Good when you want a predictable, even decay.

## Boost impact

Each boost has an **impact** value that controls how much influence it has on the document score. Impact is a number between **0** and **10** (with one decimal place, e.g. 2.5). A higher impact means the boost has a greater effect on the relevance score.

When multiple boosts are applied to a search, their effects are combined. This means you can layer different boosts to fine-tune your results.

## Applying boosts

Boosts can be applied in two ways: globally via the dashboard or at query time via the API.

### Global boosts (Dashboard)

Global boosts are configured in the Silverstripe Search dashboard under **Relevance Tuning**. These boosts are saved against a field in your engine and automatically apply to every search query unless overridden at query time.

This is ideal for general relevance tuning that should apply across your entire site search, such as always boosting recent content or promoting a key category.

### Query-time boosts (API)

You can also provide boosts directly in a search request to override the stored global boosts. This is useful when you need different boosting behaviour for specific search features or pages on your site.

When query-time boosts are provided, they are used **instead of** the global boosts — they do not combine with them.

Refer to the [Search API documentation](https://search.silverstripe.cloud/api/v1/docs/#/search/search_post) for request format details.

## Field compatibility

Not all boost types are available on all field types:

<div class="table-responsive" markdown="1">
<table class="table table-bordered" markdown="1">
<thead class="table-light">
    <tr>
    <th scope="col">Field type</th>
    <th scope="col">Value boost</th>
    <th scope="col">Proximity boost</th>
    </tr>
</thead>
<tbody markdown="1">
<tr>
<td>Text</td>
<td>Yes</td>
<td>No</td>
</tr>
<tr>
<td>Number</td>
<td>Yes</td>
<td>Yes</td>
</tr>
<tr>
<td>Date</td>
<td>Yes</td>
<td>Yes (recency)</td>
</tr>
<tr>
<td>Geolocation</td>
<td>No</td>
<td>Yes</td>
</tr>
</tbody>
</table>
</div>

