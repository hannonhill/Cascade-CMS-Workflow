*   **automatic-copy.xml**  
    Workflow Type: Copy. Begins with an edit step then automatically saves and publishes the copied asset.
*   **automatic-delete.xml**  
    Workflow Type: Delete. Automatically unpublishes and deletes the asset. Note: The `UnpublishAndDelete` trigger can't use the `system` `authorizing-type` parameter value, because the trigger requires a real username to be used to authorize deletion before unpublish.
    
    If users don't have the ability to 'Publish readable/writable Home Area assets', you can edit the trigger parameters to unpublish under an administrative username. Example:
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
*   **automatic-move-rename.xml**  
    Workflow Type: Move/Rename. Automatically unpublishes the asset then saves and re-publishes it under its new name or path. This prevents orphaned pages and files on the web server.
*   **automatic-publish.xml**  
    Workflow Type: Create and/or Edit. Automatically saves and publishes the asset. Allows users without the ability to 'Publish readable/writable Home Area assets' to publish after submitting their changes.
*   **automatic-publish-set.xml**  
    Workflow Type: Create and/or Edit. Automatically saves and publishes the asset as well as a Publish Set that can update content that syndicates the asset in workflow. Allows users without the ability to 'Publish readable/writable Home Area assets' to publish after submitting their changes.
