# Hannon Hill Workflow Definition Examples #

There are several basic kinds of workflows, divided here into folders:

* **Approval**:
    Single-approver and multi-approver workflows that require a user
    in an Approvers group to sign off before the asset can be merged (saved)
    or published

* **Automatic**:
    No-approver workflows (`system` steps only) that force the user
    to perform certain actions when an asset created, modified, or deleted.
    Actions that the workflow enforces may include:
    
    * Automatic publishing when an asset is edited
    * Automatic unpublishing when an asset is deleted
    * Notification to an administrator whenever a new asset is created
    * Etc.
    
* **Self**
    No-approver workflows that give the user an option to perform some
    action (like publishing) that she would otherwise not be able to perform.
    No intervention from an approving user is required.

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
    User account with name "Workflow Assigned". If this is not possible, the
    `default-user` can be changed to an existing User account.
    
3.  Destination names should standardized to "Production", "Staging",
    "Development", etc.