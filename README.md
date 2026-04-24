# Extract-file-from-mail-to-Sharepoint
This is a simple method to extract and configure power automate to extract file from outlook mail to Sharepoint with specific **Subject** condition

<img width="609" height="628" alt="image" src="https://github.com/user-attachments/assets/61e30af9-f05b-4844-8e1c-57673193effd" />

First of all create new **Outlook Task** and login with your credentials. 

Set:

  1- _Include Attachments_ = **Yes**
  
  2- _Only with attachments_ = **Yes**
  
  3- _Folder_ = **Inbox**

<img width="616" height="475" alt="image" src="https://github.com/user-attachments/assets/b6fcfeb6-18e1-4d03-86fb-2649f56cd6b8" />


Add **Condition Task** and setup with the following parameters:


<img width="623" height="419" alt="image" src="https://github.com/user-attachments/assets/4cc1569f-f0d7-47eb-853d-652c57ed3c33" />

Create file using Sharepoint Task, set your Company site Address and Folder Path to locate your files. Configure your File Name as you prefer, if you want timestamp on the name you can use the following expression:

%python
concat('Import_', formatDateTime(utcNow(),'yyyyMMdd),'.xlsx')

<img width="1150" height="538" alt="image" src="https://github.com/user-attachments/assets/1cdfbc5b-9cb8-4be7-acf8-46bd31bf0779" />



