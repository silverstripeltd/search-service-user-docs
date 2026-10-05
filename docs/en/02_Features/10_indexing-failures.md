---
title: Indexing failures
summary: Find content that did not make it into your search index, see why, and retry it from the CMS.
---

## Overview

When a page or other record fails to reach your search index, it is missing from your search results. Indexing failure tracking records each failure against the record it came from, so you can see which content is affected and why, and send it to the index again once the cause is fixed. This helps the people who look after your site's content and the developers who support it.

Failures are listed in the CMS under **Search Indexing**, on the **Failed Documents** tab.

> [!NOTE]
> Indexing failure tracking needs version 4.1.0 or later of the Search SDK. To update, run `composer require silverstripe/silverstripe-search-sdk:^4.1`, then run a dev/build, which adds the table the failures are stored in. See the [Developer's guide](/developers-guide) for how the SDK is installed.

## Failed documents

![The Failed Documents tab, listing failures with their reason and status](./_images/features-indexing-failures-list.png)

Each row is one record that could not be indexed, and shows:

- **Class** and **Record ID**: the record the document was made from.
- **Index**: the index the document was being sent to.
- **Status**: **Open** while the record is still failing, or **Resolved** once a later attempt succeeds.
- **Reason**: why the document failed. See [Failure reasons](#failure-reasons).
- **Last message**: the most recent error the search service or the CMS reported.
- **Failures**: how many times indexing this record has failed.
- **Last failed**: when the most recent failure happened.

A record has one row per index. If it fails again, the same row is updated and the failure count goes up, rather than a new row being added. When the record is indexed successfully, its row is marked **Resolved** without you needing to do anything.

Use the search icon above the list to filter by class, record ID, index, reason, message, failure count or status.

### Failure reasons

<table class="table table-hover table-bordered">
  <thead>
    <tr>
      <th scope="col">Reason</th>
      <th scope="col">What it means</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Error during indexing</td>
      <td>The request to the search service failed, for example because the service returned an error or could not be reached. These failures are often temporary, and a retry usually succeeds once the service is available again.</td>
    </tr>
    <tr>
      <td>Content rejected by the engine</td>
      <td>The search service received the document but refused it, for example because a field's value does not match the type set in your <a href="/features/engines-and-schema">schema</a>. The message shows the reason the service gave. Fix the content or the schema before you retry.</td>
    </tr>
    <tr>
      <td>Unacknowledged by the engine</td>
      <td>The document was sent, but the search service did not confirm that it was indexed.</td>
    </tr>
    <tr>
      <td>Removal failed</td>
      <td>The document could not be removed from the index, for example after its record was unpublished or deleted. A retry tries the removal again rather than indexing the document.</td>
    </tr>
    <tr>
      <td>Skipped: not publicly viewable</td>
      <td>The record was not sent because it is not published, or because a visitor who is not logged in cannot view it. These rows are only recorded when the setting described in <a href="#settings">Settings</a> is turned on.</td>
    </tr>
  </tbody>
</table>

## Viewing a failure

Select **View** on a row to see the full details of a failure.

![The details of a single failure, with a button to edit the source record](./_images/features-indexing-failures-detail.png)

The details show the document identifier, the full last message and a history of each failure for that record, with the date and time it happened. **Edit source record** opens the record in the CMS, so you can correct the content that caused the failure.

Where the search integration captures one, the details also include a stack trace, which helps a developer find the cause of an error. Stack traces can show file paths and the internal structure of your site, so they are only shown to people with the **View indexing failure stack traces** permission.

## Retrying and clearing failures

Once you have fixed the cause of a failure, you can send the record to the index again:

- **Retry** on a single row queues that record to be indexed again. For a failed removal, the retry tries the removal again.
- **Retry all open failures** retries every open failure. If an index job was interrupted, it is resumed where it stopped. The remaining failures are queued as one job for each index.

Retries run as queued jobs, so a row changes to **Resolved** once its job has run and the record has been indexed.

You can also remove rows from the list:

- **Clear** on a single row removes that failure from the list.
- **Clear all resolved failures** removes every resolved row and keeps the open ones.
- **Clear all failures** removes every row, open and resolved.

Clearing a failure only removes the row from the list. It does not change the record or the index.

Resolved failures are removed automatically 30 days after they were resolved, by a queued job that runs each night.

## Settings

![The Settings section below the list, with the option to record skipped documents and the bulk actions](./_images/features-indexing-failures-settings.png)

**Record documents skipped because they are not publicly viewable** adds a row for each record that is not sent to the index because it is not published, or because a visitor who is not logged in cannot view it. Turn this on when you are tracing content that is missing from your search results and you want to rule out visibility as the cause. Each skipped record adds a row, so you may prefer to turn it off again once you have found what you were looking for.

Select **Save settings** to apply the change.

## Permissions

Access to the Search Indexing area and its actions is controlled by these permissions, which you can grant to groups in the **Security** section of the CMS:

- **Allow viewing of search configuration and status, and links to external resources** gives access to the Search Indexing area, including the Failed Documents tab.
- **Retry and clear failed indexing documents** allows someone to use the Retry and Clear actions.
- **View indexing failure stack traces** shows the stack trace on a failure's details. Grant this only to people who need it to investigate errors, such as your developers.
- **Trigger Full ReIndex** allows someone to reindex an entire index from the Overview tab.

## For developers

Two settings control how failures are kept. Set them in your project's YAML configuration:

```yaml
SilverStripe\Forager\Service\IndexConfiguration:
  # Days a resolved failure is kept before the nightly job removes it. 0 keeps them.
  resolved_failure_retention_days: 30
  # Failures a single index job may record before it stops. 0 removes the limit.
  max_failures_per_job: 100
```

The failure limit stops an index job that records more than 100 failures, rather than letting it record a row for every document in a large index while the search service is unavailable. The remaining documents are kept, and the job can be resumed with **Retry all open failures** once the service is available again.
