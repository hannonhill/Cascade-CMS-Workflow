*   **one-step-approval.cswf.xml**  
    Send to an approver who can request changes, accept and publish, or edit themselves.
*   **approval-with-owner-draft.cswf.xml**  
    Same as above but owner has opportunity to continue editing before sending to approver.
*   **approval-with-publish-hold.cswf.xml**  
    Same as above but approver can save asset into a 'Publish Hold' step so that changes are present and visible in Cascade Server but not yet published.
*   **collaborative-approval.xml**  
    Very different from the above three workflows. Allows workflow owner to select three other collaborators so that the asset can be passed around and commented upon before being sent onto the final approver.
*   **multi-group-approval.xml**  
    Multi-tier approval process involving 3 Groups of Users: Approvers, Publishers, Managers. Asset in Workflow hits 3 different approval steps, each of which have actions for Approve, Deny, Edit now, and Send back to previous reviewer.