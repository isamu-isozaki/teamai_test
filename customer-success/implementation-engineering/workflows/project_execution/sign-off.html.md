---
layout: markdown_page
title: Sign-off
category: Project Execution
---

After the SOW has been completed, the customer will need to sign a Project sign off document.  This should be sent by the TAM or the IE involved, and then forwarded to Finance as part of the [financial-wrapup workflow](/handbook/customer-success/implmentation-engineering/workflows/internal/financial-wrapup.html).

To send a Project Sign off document:

1. Go to the Professional Services opportunity for the SOW you are going to get sign off for.
2. Go to the Notes and Attachments section of the Opportunity.
3. Confirm there is a signed Statement of Work. If not, please reach out to the Sales rep who closed the deal and ask them to upload the signed SOW.
4. Go to the associated quote record under the "Quotes section"
5. Click on the Quote that was "Sent to Z-Billing"
6. Click on the "Sertifi eSign" button
7. In the "Email Invite Message" field, enter a quick message to the signer.
 

```
Dear [signer],

Attached please find the sign off documentation for your GitLab Professional Services Statement of Work. 
You should be able to sign this document electronically. 
If you have any issues or questions, please free to reach out to me at boleary@gitlab.com.

Thank you,
Brendan O'Leary
Manager, Professional Services
```

8. Confirm that the pre-populated contact is going to sign off. If not, continue to Step 9. If correct, skip to Step 10. 
9. Since the contact is incorrect, delete the contact from this email workflow by clicking on the "trash icon" next to that person's name.
   * Go to the "Add from Contact" and click on the search icon.
   * Enter the contact's first and last name.
   * Click on the contact's name.
   * Click "Add Participant" (**Important**)
   * Confirm the contact has been added.
10. Click Next
11. Go to the Related Notes and Attachments drop down and select the previous-signed SOW. **Important:** Please wait for the system to load. Once loaded, you will see the document on the screen.
12. Click "Preview/Prefill Document"
13. Scroll to the "Statement of Work Completion" section.
14. On the left sidebar, 
    * Click on "Small Signature", then drag it to the signature section.
    * Click "Custom Field" for Full Name. Enter Full Name as the Text field, then drag to the Full Name section.
    * Click "Title" for the Title.
    * Click "Date" for the Date.
15. To Save, click on the Disc icon on the top right. 
16. Once you got confirmation that the document has been saved, click on the Exit icon.
17. Click "Send for Signature"

Once you receive the Project Sign off, you'll need to mark the SOW object in Salesforce as complete.

1. Go to SOW record in Salesforce.
2. Enter the Completed Date.
3. In the Status field, change to "Completed"
4. Save.