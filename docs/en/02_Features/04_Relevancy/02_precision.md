---
title: Precision
---

The precision setting change how your search queries match your content. By default the precision is set at **level 2** out of **eleven levels** which broadly matches your query to the stored documents in your engine. Increasing the level will mean the service will be more strict about what documents match the query. In other words you will get results that are more like the query itself.

## Precision Levels

<div class="table-responsive" markdown="1">
<table class="table table-bordered" markdown="1">
<thead class="table-light">
    <tr>
    <th scope="col">Level</th>
    <th scope="col">Description</th>
    </tr>
</thead>
<tbody markdown="1">
<tr>
<td>level 1</td>
<td>Highest recall (least precise)</td>
</tr>
<tr>
<td>level 2</td>
<td>Default: Less than half of the terms have to match. Full typo tolerance is applied</td>
</tr>
<tr>
<td>level 3</td>
<td>Increased term requirements: To match, documents must contain all terms for queries with up to 2 terms, then half if there are more. Full typo tolerance is applied</td>
</tr>
<tr>
<td>level 4</td>
<td>Increased term requirements: To match, documents must contain all terms for queries with up to 3 terms, then three-quarters if there are more. Full typo tolerance is applied</td>
</tr>
<tr>
<td>level 5</td>
<td>Increased term requirements: To match, documents must contain all terms for queries with up to 4 terms, then all but one if there are more. Full typo tolerance is applied</td>
</tr>
<tr>
<td>level 6</td>
<td>Increased term requirements: To match, documents must contain all terms for any query. Full typo tolerance is applied</td>
</tr>
<tr>
<td>level 7</td>
<td>Strictest term requirements: To match, documents must contain all terms in the same field. Full typo tolerance is applied</td>
</tr>
<tr>
<td>level 8</td>
<td>Strictest term requirements: To match, documents must contain all terms in the same field. Partial typo tolerance is applied: fuzzy matching is disabled</td>
</tr>
<tr>
<td>level 9</td>
<td>Strictest term requirements: To match, documents must contain all terms in the same field. Partial typo tolerance is applied: fuzzy matching and prefixing are disabled</td>
</tr>
<tr>
<td>level 10</td>
<td>Strictest term requirements: To match, documents must contain all terms in the same field. Partial typo tolerance is applied: in addition to the above, contractions and hyphenations are not corrected</td>
</tr>
<tr>
<td>level 11</td>
<td>Only exact matches will apply, with tolerance only for differences in capitalization (most precise)</td>
</tr>
</tbody>
</table>
</div>

## Setting Precision

You can set the precision level at search time or globally via the settings api.

### Search time precision

When searching you can provide a `precision` value that will apply to that individual search request. This is useful if you want to apply different precision levels to different search features or you want to allow users to set the precision. Refer to the [Search API documentation](https://search.silverstripe.cloud/api/v1/docs/#/search/search_post) for details.

### Global precision

You can set the precision to be used on all searches that do not pass a `precision` value in the request. Refer to the [Settings API documentation](https://search.silverstripe.cloud/api/v1/docs/#/settings/settings_post) for details.
