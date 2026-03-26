---
title: Frequently asked questions
---

## Can I use Silverstripe Search for websites not hosted on Silverstripe Cloud?

Yes, Silverstripe Search is available for Silverstripe CMS websites on any hosting platform.

## Can I use Silverstripe Search for websites which use a Silverstripe CMS version that is EOL or in security support only?

Silverstripe Search will remain available and performing in scenarios where an App falls out-of-date, but customers must accept the risk that Silverstripe is unable to assure service commitments to applications running out-of-date software. We strongly recommend Silverstripe CMS applications are maintained and up-to-date.

## Is Silverstripe Search available on Pae Hokohoko | Marketplace

Yes Silverstripe Search is available on Pae Hokohoko | Marketplace with Tier 2 security endorsement.

## What are some of the limits that apply to Silverstripe Search?

Please consult the [Limits and requirements page](/limits-and-requirements) in this guide.

## What happens when I exceed the limits specified for my plan?

Some of the limits are enforced and you won’t be able to exceed these. Other limits are soft, and our Operations team will review your solution performance and may get in touch to discuss the Fair Usage Policy with your team.

## What is a “Content Channel”?

The Silverstripe Search Fair Usage Policy's guidelines restrict a Silverstripe Search subscription to a single Content Channel. That means all of the indexes under the same subscription should be used for a similar purpose and information sensitivity.

Some examples of a Content Channel:

-   A collection of websites, mobile applications and other interfaces that are all for the purpose of the same specific brand or service, such as Air New Zealand and their website, app and in-flight entertainment interfaces
-   A set of locales across multiple languages, where the content translates the same or similar content, such as Tourism New Zealand and their 10+ locales
-   A set of primary domains and subdomains that are each concerned with a different area (or “vertical”) of the same brand or service
-   A set of subsites (a Silverstripe CMS application using the silvestripe/subsites module) that are each concerned with a different area (or “vertical”) of the same brand or service

## Will I need a high-number of extra paid engines to support my large set of subdomains, subsites or locales?

Not necessarily. Silverstripe’s developers can optimally use individual engines to index advanced content sets. But please be aware, as at Silverstripe Search v1.0.0, the supplied SDK does not provide features or support for advanced use cases such as locales, subdomains or subsites; and customisation may be required to support advanced content sets.

## I have virtual stacks (vStacks), will I need a new subscription for each of my virtual stacks?

Each virtual stack that is part of a separate Content Channel (see [What is a “Content Channel?”](#what-is-a-content-channel)) will require a separate subscription. Separate vStacks used within the same Content Channel can use the same subscription (even when they use separate indexes within the same subscription).

## Can I index files?

Yes - on some of the plans. Please consult the [Features guide](features) for what is included in plans and the [Documents and Files](/features/documents-and-files) section for details on the feature.

## Can I index file types other than `docx` and `pdf`?

Other formats are currently not supported by our operational procedures. Indexing other types of documents may lead to issues and we may not be able to fulfill our obligations to you.

## Can I obtain a tenancy that is completely isolated from other users to improve my security posture?

Our single tenancy feature is intended mainly as an isolation of physical resources for performance reasons. Even with single tenancy, some resources are shared.

## I’m implementing my own integration - How do I debug issues connecting to the service API?

We provide an OpenAPI spec and Swagger UI. See the documentation in the [Developer's guide](/developers-guide).

## What is needed to upgrade my plan?

You can upgrade a plan by submitting a new order, with the details of the upgraded plan and any additional information. Our Service Desk team will then fulfil the upgrade within the cost of the change fee.

## What are the impacts of moving from our Elastic Enterprise Search Management professional service to Silverstripe Search?

In many cases, moving customers from the dedicated infrastructure of Elastic Enterprise Search Management to the shared infrastructure of Silverstripe Search will gain them a cost reduction, service feature and stability improvement, and a significant security improvement.

Customers will need to end their Elastic Enterprise Search Management SoWs and shift to Silverstripe Search SoWs. We are willing to wave any remaining term under their current SoW, and complete the SoW change within the cost of the Silverstripe Search change fee.

Client’s will likely need to arrange the scope of a Silverstripe developer to update their application from Elastic Enterprise Search Management to Silverstripe Search, but in many cases the effort is minimal. The standard modules that Silverstripe currently uses are the origin of the modules provided by the Silverstripe Search SDK.

For example:

-   Silverstripe was able to migrate our Demo site from Elastic Enterprise Search Management to Silverstripe Search in around 0.5 dev days.

## I suspect there is a security issue with my Silverstripe Search, but am not really sure. Should I report it?

Yes - Please follow the [Security escalation path](/security_guide/security-escalation-path/).

## How do I contact Silverstripe for further support?

Contact our Service Desk by submitting a ticket via the [Silverstripe Cloud portal](https://silverstripe.cloud/).
