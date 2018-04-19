* **approval-collaborative.xml**  
    Workflow Type: Create and/or Edit. Allows the workflow owner to select up to three other collaborators to review and comment on the asset before its sent for final approval.

* **approval-copy.xml**  
    Workflow Type: Copy. Begins with an edit step then sends the asset to an approver group who can approve and publish, request changes, or make edits to the copied asset.

* **approval-delete.xml**  
    Workflow Type: Delete. Sends the asset to an approver group who can unpublish and delete the asset or reject the request. Note: The `UnpublishAndDelete` trigger can't use the `system` `authorizing-type` parameter value, because the trigger requires a real username to be used to authorize deletion before unpublish.

    If the approval group doesn't have the ability to 'Publish readable/writable Home Area assets', you can edit the trigger parameters to unpublish under an administrative username. Example:

```
<trigger name="UnpublishAndDelete" >
  <parameter>
    <name>authorizing-type</name>
    <value>user</value>
  </parameter>
  <parameter>
    <name>authorizing-user</name>
    <value>admin</value>
  </parameter>
</trigger>
```

* **approval-move-rename.xml**  
    Workflow Type: Move/Rename. Sends the asset to an approver group who can reject the request or accept and unpublish the asset and re-publish it under its new name or path. This prevents orphaned pages and files on the web server.

* **approval-multi-group.xml**  
    Workflow Type: Create and/or Edit. Multi-tier approval process with 3 approval steps (Approvers, Publishers, and Managers) who can each Approve, Reject, Edit, or Send Back to the workflow owner for additional changes.

* **approval-single-step.xml**  
    Workflow Type: Create and/or Edit. Sends the asset to an approver group who can approve and publish, request changes, or make edits.

* **approval-with-owner-draft.xml**  
    Workflow Type: Create and/or Edit. Same as the single-step approval but the owner has the opportunity to continue editing the asset before sending it for final approval.

* **approval-with-publish-hold.xml**  
    Workflow Type: Create and/or Edit. Same as the single-step approval but the approver can place the asset in a publish hold step so that changes are present and visible in Cascade CMS but not yet published.
