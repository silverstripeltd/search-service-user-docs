---
title: Security best practices
---

The following are some examples of best practice when implementing Silverstripe Search. The list is not exhaustive and should be seen in conjunction with general web application security practices such as the guidance available on [OWASP](https://devguide.owasp.org/) and for the [Silverstripe CMS](https://docs.silverstripe.org/en/5/developer_guides/security/secure_coding/).

For projects with high sensibility we recommend engaging a security specialist. Any security testing against the Service must be approved by Silverstripe Ltd. and arranged in advance via the [Silverstripe Cloud portal](https://silverstripe.cloud/). Security testing may not be available on all plans but you are welcome to contact us for security information.

> [!WARNING]
> This customer guide provides general security guidance intended to assist in the optimal use of our services. Users are responsible for implementing and maintaining their own security measures, and the guidance below does not transfer any responsibility or liability to Silverstripe.
>
> Please note that commercial limitations and service level exclusions apply, as detailed under signed agreements.
>
> For specific security needs and advice tailored to you, we recommend consulting with a qualified security professional.

## Index time

-   Ensure you are only indexing content that could be made public in search results. The SDK has some default checks for Silverstripe based sites such as checking pages are published and marked as viewable. If these do not suit your application, you can customise them or roll-your-own you will need to implement your own checks
-   Do not index personally identifiable information (PII) or other sensitive information.

## Querying and displaying results

-   API keys should not be exposed to front-end code (such as Javascript). We recommend proxying search requests via the server and checking they come from a valid origin.
-   Be careful when displaying user queries in UI elements. This can create a [XSS](https://owasp.org/www-community/attacks/xss/) vector if you do not sanitise user input and present it back to users.
-   Requests using your API key contribute to your request quota and you are responsible for security this key.
-   Users are expected to take reasonable steps to prevent unauthorised use of the service such as using a WAF if the search function is publicly available
-   Error handling should be implemented to prevent exposing sensitive details on search pages

## See also

-   [Silverstripe Cloud security testing documentation](https://servicedesk.silverstripe.cloud/support/solutions/articles/75000021240-security-testing)
-   [Silverstripe Cloud public sector security testing documentation](https://servicedesk.silverstripe.cloud/support/solutions/articles/75000042828-security-testing)
