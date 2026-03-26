---
title: Curations
---
> [!NOTE]
> Features on this page are only supported on plans with Analyst features. For more information, refer to [Features](/features)

Curations let you manually control search results for specific queries by **promoting** or **hiding** individual documents. This gives you direct editorial control over what users see when they search for particular terms.

For example, if users frequently search for _"getting started"_ you could promote your onboarding guide to always appear first and hide an outdated page that is no longer relevant.

## How curations work

A curation is a set of rules tied to one or more **queries**. When a user's search matches one of those queries exactly, the curation is applied:

- **Promoted documents** are pinned to the top of the results in the order you specify. Organic (non-promoted) results appear after them.
- **Hidden documents** are excluded from the results entirely.

Promoted and hidden documents can be combined in a single curation. For example, you could promote your latest product page while hiding a superseded version for the query _"product overview"_.

## Managing curations

Curations are managed in the Silverstripe Search dashboard.

### Creating a curation

1. Navigate to **Curations** in the dashboard
2. Select **Create curation**
3. Give your curation an optional **name** (e.g. _"Getting started promotion"_) to help identify it later
4. Add one or more **queries** that should trigger this curation (e.g. _"getting started"_, _"quick start"_)

<!-- Screenshot: Creating a curation with name and queries -->

### Adding promoted documents

Once your curation is created, you can add documents to promote:

1. Open the curation and go to the **Promoted Results** tab
2. Search for the document you want to promote
3. Add it to the promoted list
4. Drag and drop to reorder promoted documents — the order here is the order they will appear in search results

<!-- Screenshot: Promoted results tab with reordering -->

### Adding hidden documents

To hide documents from results:

1. Open the curation and go to the **Hidden Results** tab
2. Search for the document you want to hide
3. Add it to the hidden list

<!-- Screenshot: Hidden results tab -->

### Adding multiple queries

A single curation can be triggered by multiple queries. This is useful when users search for the same thing using different terms. For example, a curation promoting your mobile guide could be triggered by both _"mobile"_ and _"smartphone"_.

To add additional queries, open the curation and add them in the **Queries** section.

## Limits

- A curation can have up to **20 promoted** documents and **20 hidden** documents
- Query strings have a maximum length of **255 characters**
- Each query can only belong to one curation per engine
- A document can only appear once per curation (it cannot be both promoted and hidden)

## Managing curations via the API

Curations can also be managed programmatically using the API. This is useful if you want to automate curation management or integrate it into your own workflows.

The API provides endpoints for creating and deleting curations, managing queries, and adding or removing promoted and hidden documents. Refer to the [Curations API documentation](https://search.silverstripe.cloud/api/v1/docs/#/curations) for details.

