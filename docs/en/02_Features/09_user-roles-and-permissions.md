---
title: User roles and permissions
---

> [!NOTE]
> Features on this page are only supported on plans with access to the Dashboard. For more information, refer to [Features](/features)

Access to the Silverstripe Search Dashboard is controlled by **user roles**. A role determines what a user can see and do in the Dashboard. Two roles are currently available:

## Roles

### Viewer
Read-only access across the Dashboard. A Viewer can view engines and their schema, curations, synonyms, boosts, credentials, analytics and users, but cannot make any changes. This is useful for stakeholders who need visibility into your search configuration and reporting without the ability to alter it.

### Manager
Full access to the Dashboard. A Manager can view and manage everything a Viewer can see — engines and schema, curations, synonyms, boosts and credentials — as well as manage the users in your subscription and their roles.

## What each role can do

<div class="table-responsive" markdown="1">
<table class="table table-bordered" markdown="1">
<thead class="table-light">
    <tr>
    <th scope="col">Area</th>
    <th scope="col">Viewer</th>
    <th scope="col">Manager</th>
    </tr>
</thead>
<tbody markdown="1">
<tr>
<td>Run searches</td>
<td>View</td>
<td>View</td>
</tr>
<tr>
<td>Engines &amp; schema</td>
<td>View</td>
<td>Manage</td>
</tr>
<tr>
<td>Curations</td>
<td>View</td>
<td>Manage</td>
</tr>
<tr>
<td>Synonyms</td>
<td>View</td>
<td>Manage</td>
</tr>
<tr>
<td>Boosts</td>
<td>View</td>
<td>Manage</td>
</tr>
<tr>
<td>Credentials</td>
<td>View</td>
<td>Manage</td>
</tr>
<tr>
<td>Analytics</td>
<td>View</td>
<td>View</td>
</tr>
<tr>
<td>Users</td>
<td>View</td>
<td>Manage</td>
</tr>
</tbody>
</table>
</div>

*Manage* means the role can create, edit and remove items in that area; *View* means read-only access.

> [!NOTE]
> The features available to you also depend on your subscription plan. For example, synonyms and analytics are only available on the Analyst and Architect plans. Your effective access is the combination of your role and your plan — refer to [Features](/features) for what each plan includes.

When a user has read-only access to an area — either because they are a Viewer or because of their plan — the Dashboard shows that area without the Add, Edit or Remove controls.

## Changing a user's role

User roles are assigned and changed by Silverstripe. To add a user, remove a user, or change someone's role, raise a service desk request.
