---
title: Developer's guide
---

Silverstripe Search is designed to integrate easily with the Silverstripe CMS. The recommended way to do this is with our [Software Development Kit (SDK)](https://github.com/silverstripeltd/silverstripe-search-sdk) but you can also [directly use the API](#api-specification). The Silverstripe Search API is known as the Bifröst and you will be provided with credentials upon signing up to the service.

## Using the SDK

You will need:

-   A Silverstripe CMS application
-   Bifröst API Credentials (provided when you sign up for Silverstripe Search Service)
-   Engine names (provided when you sign up for Silverstripe Search Service).

The SDK consists of two primary modules as well as an optional module to provide an initial templating for your search implementation.

More detail on how to use the SDK, including installation and code, can be found on its repo: [https://github.com/silverstripeltd/silverstripe-search-sdk](https://github.com/silverstripeltd/silverstripe-search-sdk)

## API specification

The Silverstripe Search Service provides an OpenAPI 3.1 Specification, along with a Swagger UI where you can review and test requests to the service using your own credentials.

You can find the API spec at this path: [https://search.silverstripe.cloud/api/v1/docs](https://search.silverstripe.cloud/api/v1/docs)

Further information
Check the [FAQ - Frequently asked questions](/faq).

## Feature flags

Some features are activated using a feature flag including the following:

-   [File indexing](https://github.com/silverstripeltd/silverstripe-forager-bifrost/blob/main/README.md#file-attachments-for-content-extraction)
-   [Spelling suggestions](https://github.com/silverstripeltd/silverstripe-discoverer-search-ui?tab=readme-ov-file#spelling-suggestions-aka-did-you-mean)
