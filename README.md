# Extract File from Email to SharePoint

This guide shows how to configure a flow in Microsoft Power Automate to automatically extract email attachments from Outlook and upload them to SharePoint based on a specific **Subject** condition.

![Outlook Trigger](https://github.com/user-attachments/assets/61e30af9-f05b-4844-8e1c-57673193effd)


---

## 📌 Step 1 — Create Outlook Trigger

Create a new **Outlook trigger** and log in with your credentials.

Set the following parameters:

- **Include Attachments** = Yes  
- **Only with Attachments** = Yes  
- **Folder** = Inbox  

<img width="616" height="475" alt="image" src="https://github.com/user-attachments/assets/fa0cae17-de8c-461c-945a-cda3cbbebc0b" />


---

## 📌 Step 2 — Add Condition

Add a **Condition** action and configure it based on the email **Subject**.

![Condition](https://github.com/user-attachments/assets/4cc1569f-f0d7-47eb-853d-652c57ed3c33)

---

## 📌 Step 3 — Create File in SharePoint

Add a **SharePoint – Create file** action.

Configure:
- **Site Address** = your company SharePoint site  
- **Folder Path** = destination folder  

You can customize the file name.  
To include a timestamp, use this expression:

```text
concat('Import_', formatDateTime(utcNow(),'yyyyMMdd'), '.xlsx')
```

<img width="1150" height="538" alt="image" src="https://github.com/user-attachments/assets/a202f4b7-8c88-4bec-b469-ad18cfa2e6e3" />






