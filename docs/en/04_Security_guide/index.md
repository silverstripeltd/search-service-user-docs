---
title: Security guide
---

Use this page to understand security risks you may need to plan for, and Silverstripe’s security commitment.

> [!WARNING]
> This customer guide provides general security guidance intended to assist in the optimal use of our services. Users are responsible for implementing and maintaining their own security measures, and the guidance below does not transfer any responsibility or liability to Silverstripe.
>
> Please note that commercial limitations and service level exclusions apply, as detailed under signed agreements.
>
> For specific security needs and advice tailored to you, we recommend consulting with a qualified security professional.


## Silverstripe’s security commitment

Silverstripe’s managed services provide service management, 24/7 monitoring, security assurance, and continuous improvement which aligns with ISO27001:2022 security standards. Our commitments are:

-   ISO27001:2022 controls and standards
-   Secured Infrastructure with ISO compliant and audited security, including managed stability support and 24/7 monitoring
-   Data privacy compliant with local and international data protection regulations
-   Access controls implementing role-based access to ensure protected data and analytics.

## Customer security planning guidance

To achieve a high-standard of security maturity, customers can add the following security risks to their security plans.

> [!NOTE]
> More information is available on best practices for using and implementing Silverstripe Search, refer to [Security Best Practices](./security-best-practices)

When planning your security around Silverstripe Search, please be aware of some key risks:

<div class="table-responsive">
<table class="table table-bordered">
  <thead class="table-light">
    <tr>
      <th scope="col">Event</th>
      <th scope="col">Consequences</th>
      <th scope="col">Silverstripe's commitment</th>
      <th scope="col">Recommendations</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>You might cause private data to become publicly available when configuring a document’s field as public</td>
      <td>Your protected data may be unexpectedly disclosed</td>
      <td>
        <ul>
            <li>Awareness training/guides to support customers</li>
            <li>Commercial terms to signal service boundaries</li>
            <li>Data loss prevention security controls</li>
            <li>Best effort support for security vulnerabilities in our SDKs</li>
        </ul>
      </td>
      <td>
        <ul>
            <li>Check implementations using Silverstripe’s SDKs for security assurance</li>
            <li>Keep up-to-date, Silverstripe CMS and Silverstripe CMS modules</li>
            <li>Perform frequent reviews of public data configurations</li>
            <li>Plan additional security controls to protect against data leakage </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>Your data might be exfiltrated or leaked from Elastic, the Silverstripe Search dependency</td>
      <td>Your protected data may be leaked</td>
      <td>
        <ul>
            <li>Security evaluation of Elastic</li>
            <li>Frequent security audits of our integrations to Elastic</li>
            <li>Awareness training/guides for technical support</li>
            <li>Dedicated security plans and controls for Elastic dependencies</li>
        </ul>
      </td>
      <td>
        <ul>
            <li>Perform frequent checks for information stored on Silverstripe Search to check that only the correct data is used</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>An attacker may exploit an entry point to Elastic, the Silverstripe Search dependency</td>
      <td>Your protected data may be leaked</td>
      <td>
        <ul>
            <li>Role-specific training for all staff controlling or distributing access to Elastic tools</li>
            <li>Frequent security access reviews</li>
            <li>Configuration controls that govern access to Elastic tools</li>
            <li>Dedicated security plans and controls for Elastic dependencies</li>
        </ul>
      </td>
      <td>
        <ul>
            <li>Keep access credentials updated with strong password security standards</li>
            <li>Do not share accounts or access credentials</li>
            <li>Perform frequent access reviews of accounts with access to Silverstripe Search</li>
        </ul>
      </td>
    </tr>
   
  </tbody>
</table>
</div>

## Security risk maturity

We recommend all customers implement security practices and planning:

-   [Security best practices](./security-best-practices)
-   [Security escalation path](./security-escalation-path)

## Further support

Check the [FAQ - Frequently asked questions](/faq).
