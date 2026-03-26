---
title: Synonyms
---

> [!NOTE]
> Features on this page are only supported on plans with Analyst features. For more information, refer to [Features](/features)

Synonyms let you define words or phrases that should be treated as equivalent when searching. This helps bridge the gap between the terminology your content uses and the words your users search for.

For example, users might search for _"Cellphone"_ but your content uses the term _"Mobile"_. Adding a synonym set with these two terms means searching for either will match documents containing _"Mobile"_ or _"Cellphone"_.

## How synonyms work

A synonym set is a group of two or more terms that should be treated as equivalent. When a user searches for any term in the set, the search will also match documents containing any of the other terms.

For example, if you create a synonym set containing `ipod`, `i-pod`, and `i pod`, then searching for any of these terms will return documents containing any of the others.

## Managing synonyms

Synonyms can be managed in the Silverstripe Search dashboard, via the API, or through the Silverstripe CMS Administration module.

### Dashboard

Navigate to **Synonyms** in the Silverstripe Search dashboard to create, update, and delete synonym sets for your engine. Each synonym set requires at least two terms.

### API

Synonyms can be managed programmatically using the API. Full CRUD operations are available for creating, listing, updating, and deleting synonym rules. Refer to the [Synonyms API documentation](https://search.silverstripe.cloud/api/v1/docs/#/synonyms) for details.

### Administration module

Synonyms can also be managed in the [Silverstripe Search Administration module](https://github.com/silverstripeltd/silverstripe-bifrost-admin) for Silverstripe CMS. Once installed, it is available in the CMS menu and allows you to create, update, and delete synonym sets for your engine.

Refer to the [Developer's guide](/developers-guide) for more information and installation instructions.

## Limits

- Synonym rules can contain a maximum of **32 words**
