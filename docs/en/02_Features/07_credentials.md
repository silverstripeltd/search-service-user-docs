---
title: Credentials
---

> [!NOTE]
> Features on this page are only supported on plans with access to the Dashboard. For more information, refer to [Features](/features)

Bifröst search credentials are API keys used to authenticate requests to the Search API. There are two types of credentials, each suited to different use cases.

## Managing credentials
Credentials are created and managed in the Dashboard. Each credential can be assigned to one or more engines within your subscriptions, allowing you to control which engines a credential has access to. If a credential is compromised or no longer needed, it can be revoked at any time from the Dashboard.

> [!NOTE]
> The credentials tab can be found on the **Engines overview** page accessed by the Home icon

## Query credentials
Query credentials provide read-only access to search. They can only retrieve results — they cannot create, update, or delete documents, or change engine settings.

Because query credentials cannot modify content, they can be safely embedded in client-side JavaScript and used directly from a visitor's browser. This is a common pattern for powering a search UI without a backend intermediary.

However, exposing a query credential publicly means any visitor (or automated tool) can issue search requests directly to the API. High volumes of requests from bots or scrapers will count against your usage quota. To avoid this consider [proxying your requests](#proxying-search-requests).  
.

## Management credentials
Management credentials provide full read/write access to search. They can read, create, update, and delete documents, and they can change engine settings. Management credentials should never be exposed in client-side code or public repositories - treat them as you would a database password and use them only in server-side environments.

## Proxying search requests
To use search in a browser without exposing a credential at all, consider proxying requests through your own application. Your server receives the search request, forwards it to the Search API using a credential stored securely server-side, and returns the result to the browser.

This approach has additional benefits: your application sits in front of the request, so you can apply your own Web Application Firewall (WAF) rules, rate limiting, and input sanitisation before the query reaches the Search API — protecting both your usage quota and your search index from abuse.
