---
title: Analytics
---

Analytics gives you insight into how your users are searching, helping you understand what content they are looking for and how well your search is performing. Analytics is available on the **Analyst** and **Architect** plans.


## Date range

All analytics queries accept a date range to control the period of data returned. If no date range is specified, the **default is the last 7 days**.

## Recent queries

View the most recent queries made against your engine. This is useful for seeing what users are searching for right now and can help you identify emerging trends or issues in real time.

## Top queries

See the most popular queries over the selected date range, ordered by the number of times they were searched. Use this to understand what your users are searching for most often and ensure your content meets demand.

## Top queries with no results

Identify the most popular queries that returned **zero results**. These represent gaps in your content — queries where users are looking for something but not finding it. 

## Top queries with clicks

See which popular queries are leading to users clicking on a result. This indicates queries where users are finding relevant content and engaging with it. A high click rate is a sign that your search results are effective.

## Top queries with no clicks

Identify popular queries where users are **not clicking any results**. This may indicate that the results shown are not relevant or useful, even though results are being returned. Consider reviewing the content or [relevancy tuning](/features/relevancy) for these queries to improve engagement.

> [!NOTE]
> **Click tracking requires implementation**
> Click analytics (top queries with clicks and top queries with no clicks) require click events to be sent from your site. The [silverstripe-discoverer-bifrost](https://github.com/silverstripeltd/silverstripe-discoverer-bifrost) module supports this from **v3.1.0**. Refer to the module [silverstripe-discoverer](https://github.com/silverstripeltd/silverstripe-discoverer/blob/main/docs/simple-usage.md#recordss) documentation for implementation details.

## Tags

Analytics supports **tagging**, which allows you to segment your analytics data. Tags are applied on the client side when making search or click requests. For example, you might tag queries by section of your site, user type, or A/B test variant. When viewing analytics, you can filter by tag to compare how different segments are performing.

> [!NOTE]
> **Tagging requires implementation**
> Tags must be sent from your site with each search or click request. Refer to the [Search API](https://search.silverstripe.cloud/api/v1/docs/#/search/search_post) and the  [silverstripe-discoverer](https://github.com/silverstripeltd/silverstripe-discoverer/blob/main/docs/detailed-querying.md#tags) module documentation for implementation details.