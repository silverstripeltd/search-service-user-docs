---
title: Limits and Requirements
---

## Requirements

### API requirements

Silverstripe Search Service API is available on any hosting platform.

### SDK requirements

The following are required to use the provided SDK

<table class="table table-bordered">
  <thead class="table-light">
    <tr>
      <th scope="col">Dependency</th>
      <th scope="col">Requirement</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Silverstripe CMS</td>
      <td>Full support version (view the <a href="https://www.silverstripe.org/software/roadmap/">Silverstripe CMS Support timeline</a>)</td>
    </tr>
  </tbody>
</table>

A full support version of Silverstripe CMS is required for us to be able to assure service commitments. For information on which versions are in full support, consult the [Silverstripe CMS Support timeline](https://www.silverstripe.org/software/roadmap/).

## Limits

The following general limits apply to this solution:

<table class="table table-bordered">
  <thead class="table-light">
    <tr>
      <th scope="col">Limitation</th>
      <th scope="col">Information</th>
    </tr>
  </thead>
  <tbody >
    <tr>
      <td>Feature availability by plan</td>
      <td>Plans apply limits to features, storage, and requests per month. For more information review your service plan.</td>
    </tr>
    <tr>
      <td>Fair usage</td>
      <td>Silverstripe Search Fair Usage Policy applies.</td>
    </tr>
  </tbody>
</table>

There are also Engine limits and Query limits

### Engine Limits

<table class="table table-bordered table-striped">
  <thead class="table-light">
    <tr>
      <th scope="col">Limitation</th>
      <th scope="col">Information</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>File content extraction size limit</td>
      <td>15 MB per file</td>
    </tr>
    <tr>
      <td>Maximum Indexing Payload Size</td>
      <td>100 MB per request</td>
    </tr>
    <tr>
      <td>Bulk Indexing Maximum</td>
      <td>100 documents per batch</td>
    </tr>
    <tr>
      <td>Synonym Sets</td>
      <td>256</td>
    </tr>
    <tr>
      <td>Words per Synonym Set</td>
      <td>32</td>
    </tr>
    <tr>
      <td>Schema Field Length</td>
      <td>64 characters</td>
    </tr>
    <tr>
      <td><i>id</i> Schema Field Value Length</td>
      <td>800 characters</td>
    </tr>
  </tbody>
</table>

### Query Limits

<table class="table table-bordered table-striped">
  <thead class="table-light">
    <tr>
      <th scope="col">Limitation</th>
      <th scope="col">Information</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Query Length</td>
      <td>128 characters</td>
    </tr>
    <tr>
      <td>Result Pages</td>
      <td>100 pages</td>
    </tr>
    <tr>
      <td>Results Per Page</td>
      <td>1000 results per Page</td>
    </tr>
    <tr>
      <td>Results Per Query</td>
      <td>10,000</td>
    </tr>
    <tr>
      <td>Snippet Result Text Field Size</td>
      <td>1000 characters</td>
    </tr>
    <tr>
      <td>Raw Result Text Field Size</td>
      <td>1000 characters</td>
    </tr>
    <tr>
      <td>Facets</td>
      <td>250 facets</td>
    </tr>
    <tr>
      <td>Filters</td>
      <td>32 filters</td>
    </tr>
    <tr>
      <td>Filter Array Items</td>
      <td>1024 array items</td>
    </tr>
    <tr>
      <td>Filter Nesting Levels</td>
      <td>5 levels</td>
    </tr>
    <tr>
      <td>Sorting Fields</td>
      <td>10 fields</td>
    </tr>
    <tr>
      <td>Grouping Fields</td>
      <td>10 fields</td>
    </tr>
  </tbody>
</table>

## Further support

Contact our Service Desk by submitting a ticket via the [Silverstripe Cloud portal](https://silverstripe.cloud/).
