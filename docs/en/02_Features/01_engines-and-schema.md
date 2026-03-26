---
title: Engines and Schema
---

**Engines** are where your content is stored and they have a **schema** that describes it. When you sign up for Silverstripe Search, engines will be created for you to use. Refer to the [Developer’s guide](/developers-guide) for how to create a schema. Once you are set up you can add your [Documents](../documents-and-files).

## Engine

An **engine** is a group of your documents. All documents within an engine must have the same structure which is known as the engine’s schema. For search to work, your content has to be processed into this searchable structure.

You may have multiple engines either to separate your content (e.g. to have your production site separate from any test sites) or to allow support different schemas.

> [!WARNING]
> **Limit of 64 fields per schema**
> An engine has a limit of 64 fields per schema. If you have a large variation of data you may need multiple engines to obtain enough fields.

## Schema

> [!WARNING]
> **Field types are immutable**
> Once you add a field to an engine you cannot change its name or type without deleting the engine so choose field names and set their types carefully.


Each of your engines has a **schema** which defines the shape of your data. Schemas consist of **schema fields**, which tell Silverstripe Search more about what your documents contain so that it can provide matching features.

The schema also defines what kind of data can be stored in specific fields. This is known as the **field type** (as in “what type of field is it?”, “it's a date field”).

A good example is the use of dates and times. If your schema defines a field as a date field then you will have access to advanced date range filters.

The following data types are supported:

<div class="table-responsive" markdown="1">
<table class="table table-bordered" markdown="1">
<thead class="table-light">
    <tr>
    <th scope="col">Data Type</th>
    <th scope="col">Description</th>
    </tr>
</thead>
<tbody markdown="1">
<tr>
<td><code>text</code></td>
<td>Text content. This enables deeply analysed full text search. This is the default type for all new fields. Any group of characters or text that you want to search over should be text. Text can be in many languages.
</td>
</tr>
<tr>
<td><code>number</code></td>
<td>
    <p>Numbers. Number fields enable fine grained sorting, filtering, faceting, and boosting.</p>
    <p>They can either be integers or single-precision, floating-point values (32 bits): <code>3.14</code> or <code>42</code>.</p>
</td>
</tr>
<tr>
<td><code>date</code></td>
<td>
    <p>Dates. Enables fine grained filtering.</p>
    <p>They must be in one of the following formats:</p>
    <ul>
        <li>Strings containing formatted dates, e.g. "2015-01-01" or "2015/01/01 12:10:30"</li>
        <li>A number representing <a href="https://en.wikipedia.org/wiki/Unix_time">seconds-since-the-epoch</a></li>
    </ul>
</td>
</tr>
<tr>
<td><code>geolocation</code></td>
<td>
    <p>Location data. Enables location filtering.</p>
    <p>Geolocation fields are latitude-longitude pairs, representing locations. The following syntax is supported:</p>
    <ul>
        <li><code>41.12,-71.34</code> "lat,lon"</li>
        <li><code>drm3btev3e86</code> geohash</li>
        <li><code>[ -71.34, 41.12 ]</code> array with the format [lon, lat]</li>
        <li><code>POINT (-71.34 41.12)</code> Geo-point as a <a href="https://docs.opengeospatial.org/is/12-063r5/12-063r5.html">well-known text POINT</a></li>
    </ul>
</td>
</tr>
<tr markdown="1">
<td><code>binary</code></td>
<td markdown="1">Base64 encoded file content. Only supported for the _attachment field for the purposes of <a href="../documents-and-files">extracting content from files</a>.
</td>
</tr>
</tbody>
</table>

</div>

### Editing and viewing your Schema

You can view your engine's current schema using the [Silverstripe Search Dashboard](https://dashboard.silverstripe.cloud/search) and the [Silverstripe Search Administration module](https://github.com/silverstripeltd/silverstripe-bifrost-admin) or with the API. Schema **must be created or updated by an API** request. For more information, refer to the [Developer’s Guide](/developers-guide).
