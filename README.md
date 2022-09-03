# InvoiceManagementSystem
Authenication and Authorization with RoleManagement , DataSeeding, Secrets Manager and Deployment to Azure
C#, EF Core, ASP.Net, .Net6

We demonstarte Authentication and Authorization (Role Manangement) in an ASP.Net Application based on .Net 6.

We have an "Invoice" entity on which different users will have different roles.

# User and Roles

| Accountant | Manager | Admin |
| :-----: | :---: | :---: |
| Add new invoice | Approve invoice | Approve Invoice   |
| Delete an invoice | Reject invoice | Reject Invoice   |
| (Invoice goes to Manager) | (Overseen by Admin) | Edit Invoice   |
|         |       | Delete an Invoice   |

Some Conditions:
1. Accountant can only see/edit his own Invoices. (userID == creatorID)
2. Manager can Approve or Reject an Invoice
3. Admin has all rights. Admin can also see some stats on homepage.

Manager and Admin user is seeded in the DB on start Up and Password is saved in Secrets Manager

Manager 
Username : manager@demo.com
Password: Test@1234

Admin 
Username : admin@demo.com
Password: Test@1234

You can create register yourself as a new user (Accountant by default) Or use an already existing ones in the DB
Username : accountant@demo.com
Password: Test@1234

Azure Deployment coming soon..
