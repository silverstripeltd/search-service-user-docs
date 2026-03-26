---
title: Documents and Files
---

## Document

A **document** is an individual piece of content that can be indexed and retrieved by from your search engine. Documents are a representation of your content that is stored in Silverstripe Search. Only content added into documents will be available to search on.

A document is made up of **fields** which have a key and a value. The key is the name of the field and this is the same for all documents within the engine. A field’s value represents the unique content of the document. For example your documents might have a key called `title` which you use to store the title of your pages such as “Home Page”, “About Page” etc. An example document could look like:

<table class="table table-bordered">
  <thead class="table-light">
    <tr>
      <th scope="col">Field key</th>
      <th scope="col">Field value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>title</code></td>
      <td>Home Page</td>
    </tr>
    <tr>
      <td><code>content</code></td>
      <td>Welcome to the home page</td>
    </tr>
    <tr>
      <td><code>url</code></td>
      <td>/</td>
    </tr>
    <tr>
      <td><code>date_published</code></td>
      <td>2024-07-17 10:00:00</td>
    </tr>
  </tbody>
</table>

Giving your documents a structure like this, combined with a [schema](../engines-and-schema), allows you to use the full power of Silverstripe Search. In the above example, having a `date_published` allows you to create a search for all documents published after a certain date.

Documents are added to an [Engine](../engines-and-schema) programmatically, find out more in the [Developer's guide](/developers-guide).

## Files

Silverstripe Search can search files such as PDF (`.pdf`) and Microsoft Office (`.docx`) documents. To do this it extracts the file content into a Silverstripe Search [Document](#document). You can send the file, [with the help of a developer](/developers-guide), in a special [binary type](../engines-and-schema#schema) field called `\_attachment`. The service will then extract the content it can process and put in the `body` field. There is a **15MB limit on file size**.

> [!TIP]
> File content extraction is only supported on Tiers with Analyst features. For more information, see [Features](/features)


### Supported file types

-   `.txt`
-   `.py`
-   `.rst`
-   `.html`
-   `.markdown`
-   `.json`
-   `.xml`
-   `.csv`
-   `.md`
-   `.ppt`
-   `.rtf`
-   `.docx`
-   `.odt`
-   `.xls`
-   `.xlsx`
-   `.rb`
-   `.paper`
-   `.sh`
-   `.pptx`
-   `.pdf`
-   `.doc`
