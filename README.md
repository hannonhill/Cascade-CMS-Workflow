# Hannon Hill Workflow Definition Examples #

Here you'll find example Workflow Definitions for a variety of common workflows. We've divided them into three types:

* **Approval:**
    Workflows that require a user in one or more groups to approve the request before the asset can be merged (saved) or published.

* **Automatic:**
    Workflows that don't require approval. These can be used to ensure certain actions are taken after an asset is created/edited, copied, moved/renamed, or deleted. For example:

    * Automatic publishing when an asset is created or edited.
    * Automatic unpublishing when an asset is deleted.
    * Automatic unpublishing and re-publishing when an asset is moved or renamed.

* **Self:**
    Workflows that don't require approval and give the user an option to perform some action (like publishing) that they would otherwise not be able to perform without the appropriate role abilities.

Please feel free to copy and customize these workflows to suit your needs. For a full list of available workflow triggers, please visit our [Cascade CMS Knowledge Base](https://www.hannonhill.com/cascadecms/latest/content-management/workflows/index.html).

------------------------------------------------------------------------------

*When contributing workflows to this repository, a few guidelines should be
followed*:

1. All group names should be standardized to the 'Approvers' group. This makes
    it easier to understand which steps in a workflow require the action of an
    approver. If a workflow involves the participation of more than one group
    of approvers (e.g. legal, proofreading), standardize the group names to
    '*adjective* + Approvers' (i.e. 'Legal Approvers', 'Copy Approvers').

2. When a `<step type="transition">` in the workflow will have its user or
    group automatically assigned by a preceding trigger like
    `AssignToWorkflowOwner`, that step's `default-user` should be written as
    `default-user="Workflow Assigned"` to prevent confusion. For users
    implementing these workflows, the best practice is to create a disabled
    user account with name `Workflow Assigned`. If this is not possible, the
    `default-user` can be changed to an existing user account.

3.  Destination names should standardized to "Production", "Staging",
    "Development", etc.
