# PayFabric Receivables  

## 7/6/2021  

Video: https://www.youtube.com/watch?v=dk1pwSeCNGs  
Guide: https://www.nodus.com/documentation/PayFabric-Receivables-Release-Notes.pdf  

### Customer Enhancements
* Default payment terms can now be assigned to customer records

### Invoice Enhancements
* When creating an invoice, payment terms have been enhanced to automatically calculate the Invoice Due Date and provide discount options.
* A new option is available to add an approval step before an invoice is completed and sent to customers.

### Payment Enhancements
* Available Payment Terms Discounts will not automatically be applied to payments when applicable
* A customer's available credit balance can now be applied during a payment. During the payment process, a user can select which available credits should be applied to invoices.
* A new e-mail template is available when only a credit is applied during a payment without a new transaction.
* A customer's available credit balance can now be configured automatically be applied during recurring payments
* When a user attempts to leave a payment, they will now be prompted if they want to leave the payment screen.
* Companies processing transactions with EVO Payments can now add a processing surcharge to credit card transactions processed on PayFabric Receivables. With surcharging enabled, an additional amount will automatically be added to the payment if the user is paying by credit card. Before enabling credit card surcharging, please make sure to consider the surcharging rules and regulations to determine if credit card surcharging is a good fit for your business.
* For internal users, a new option to simply record an already accepted payment without processing is now available.
* The payment receipt page has been updated with a new style. Also, download and e-mail forwarding options are now available directly on the payment receipt.
* The historical payment details page has also been updated with a new style
* The Notes field can now be included on the Payment confirmation receipt.

### Integration Enhancements
* New record types are now available to be integrated with other systems. New Customer, Invoice, Application and Surcharges are all available to be integrated from the API.
* A new integration details page showing more information about the history of the integration record is now available.
* The exported report on the integration page has now been enhanced to include the additional record types and more detail for integrated payments.

## 1/21/2021

Video: https://www.youtube.com/watch?v=r3DqgNq72Tw  

### Dashboard
* A new dashboard page is available when accessing PayFabric Receivables. This page will display a high level overview of the company's Receivables status.

### Customer Enhancements
* A new Customer Editor interface is now available to create & edit customer records and customer address information.
* The Customer Report page has received the following updates:
	* A button has been added create a new customer record.
	* Clicking a customer record will now display an Edit option to modify the customer record.
	* New Columns have been added to show if the customer is subscribed to AutoPay and the registered users of the Customer Portal
* A new Customer Management Settings page is available to control access to the Customer Editor for all users and additional settings related to the customer editor.
* Create and Edit Customer user permissions are now available to control which users can Create or Edit customer records.

### Invoice Enhancements
* A new Invoice Editor interface is available to create invoice records with item detail.
* A new Invoice Management Settings page is available to control access to the Invoice Editor for all users and additional settings related to the Invoice Editor.
* A Create Invoice user permission is now available to control which users can create invoice records.
* The Invoice Report has received the following updates
	* A button has been added to allow for creating a new invoice record
	* New columns for Status and E-mail have been added
	* The default filter on the page is now based on the status column
	* The customer ID column can now be clicked and functions the same as clicking a customer record on the Customer Report
	* Clicking an Invoice ID now presents a menu with available options for working with the invoice.
* Invoice Types are now available to classify invoices into groups
	* A new Invoice Types settings page is available for creating and editing Invoice Types.
	* The New Invoice Notification E-mail can now be restricted to only be sent for certain Invoice Types
	* Automated Invoice Reminder E-mails can now be restricted to only be sent for certain Invoice Types
	* AutoPay Templates can be configured to only pay invoices of certain Invoice Types
* Multiple Invoice Templates can now be created to be assigned to different Invoice Types.
* New variables for Item Markdown and Item Comment are now available for the Invoice Template
* Each Invoice can now be assigned primary e-mail and copy e-mail addresses to control the recipients of the e-mail notifications regarding an individual invoice.
* A New Item Editor interface is available to create items to be used on invoices.

### Data Import
* Items can now be created in bulk with the new Item import option
* Customers can now be registered for AutoPay in bulk with the new AutoPay import option
* Email and Copy Email fields are now available when importing Invoices.
* An Item Comment field is now available when importing Invoice Items.

### API
* All Invoice APIs have been updated to include the Email, CopyEmail and Item Comment parameters
* Item GET and POST APIs are now available for retrieving and pushing item detail to PayFabric Receivables.
* All AutoPay APIs have been updated to include the Invoice Type parameter
* Customer POST API will now update the Name value with the CustomerID if the Name is blank or null

## 8/5/2020

Video: https://www.youtube.com/watch?v=SuyJzXPJ2Yc

### User Experience Enhancements
* The experience of accessing customer data has been improved to focus on easier transition between managing customer accounts.  
* The settings have been reorganized for easier navigation.  

### Customer Portal User Management
* Customer portal users can now be invited to sign up for the customer portal  
* Multiple users can now be created for a single customer account  
* Password reset requests can now be initiated from within the portal  
* Customer Portal Users can be uploaded in bulk using the Data Import utility.  

### User Permissions
* Access permissions are now available to assign internal users have access to PayFabric Receivables functionality.  
* Permission groups are also available to be assigned to users of the customer portal  

### Invoice PDF Files
* A PDF file can now downloaded when viewing an invoice  
* A PDF file can now be uploaded using the Receivables API to be presented instead of the generated invoice template.  

### New Transaction Fields
* Additional fields Customer Tax Exempt Number, Customer Company Name, and Item Commodity Code are available from the PayFabric Receivables API to be sent during payment processing  

### Pass-Through Authentication Enhancements
* Additional parameters are available for Pass-Through Authentication to create a more seamless experience for users being passed into the PayFabric Receivables customer portal from another application.  





## 6/5/2020

Video: http://www.youtube.com/watch?v=V7jTXq3QQOc

### E-mail Enhancements
* The e-mail template setup process has been completely redesigned to improve the e-mail template setup experience for users. 
* All of the default e-mail templates have a new updated design that is optimized for display on mobile devices. 
    * Customers with existing configured e-mail templates can utilize the new templates by clicking the reset button in the e-mail template editor. 
* New variables are available for the large company logo, small company logo and company e-mail. 

### Invoice Reminder
* A new e-mail type is available to allow for a reminder e-mail to be sent for outstanding invoices. 
* This e-mail can be manually sent from the Invoice report page to one or multiple recipients.
* This e-mail can also be scheduled to be automatically sent based on the age of the invoice. Reminders can be scheduled before, on or after the invoice due date and each reminder can be configured to have different messaging. 

### PDF File Attachments
* On e-mail templates such as the New Invoice Notification and the Invoice Reminder, an option is available to automatically attach a PDF version of the invoice to the e-mail. 

### E-mail Report
* A new page is available to show all e-mails sent out from PayFabric Receivables. Users can view the details of each individual e-mail and also resend previously sent e-mails. 

### Pass-Through Authentication Improvements
* A new configuration option is available for pass-through authentication. The new Originating Portal URL option will redirect any users who reach the Customer Portal login page to another webpage such as the login page for the integrating application. 

### Data Import Updates
* A sample of the expected spreadsheet file with headers can be downloaded for any Data Import template. 
* Data import templates can now be deleted

### Delete Invoices
* Invoices can now be deleted from the invoice report page individually and in bulk. 

### Functional Currency Setup Option
* A new setting is available to allow the functional currency to be changed for the organization. 

### API Help
* A new API help page is now available to make it easier for developers to work with the Receivables API by providing interactive tests and sample data. https://sandbox.payfabric.com/receivables/apihelp





## 1/16/2020

### AutoPay
* Customer's can now be registered for automatic recurring payments. Multiple frequency and payment amount options are available. 

### AutoPay Templates
* The organization can specify the settings for how automatic payments should be processed based on the business preferences. Multiple templates can be created to provide different AutoPay options to customers. 

### AutoPay E-mail Templates
* New e-mail templates are available to be sent to customers when an AutoPay payment is approved or fails to be processed. 


## 7/17/2019

### Receivables Portal

#### Data Import
*  Data can now be imported to PayFabric Receivables using a spreadsheet file. The following data sets can now be imported to the portal:  
    * Customers  
    * Invoices  
    * Items on Invoices  
    * Payments  
    * Application of Payments to Invoices  
* The mapping of the spreadsheet file to PayFabric Receivables can be saved to a template for future uploads from the same format of data in the future.  

#### Invoice & Payment Reports  
* Internal users can now view a list of all available invoices and payments from PayFabric Receivables.  

#### Integration Report Export  
* From the Integration Report, a list of the recently processed payments on PayFabric Receivables can be downloaded to a spreadsheet.
* This export is available when the *Integration Method* setting is set to the new *File* option.  

### Customer Portal  

##### Payment Terminal and P2PE Device Support  
* Internal users making payments can now use PayFabric supported payment terminals and point to point encryption P2PE devices for more secure entry of credit card data.  


## 4/9/2019  

### Receivables Portal  

##### Integration 
* Enhanced user experience when loading payment details  
* From the Integration Report, the Payment ID and Identity can be updated and the Application of Payment to Invoice can be removed before the payment is integrated.  

##### Express Pay  
* From the New Invoice Notification E-mail, the ExpressPayLink variable is now available. When this variable is combined with the CustomerPortalURL variable, it will create a full link in the e-mail to allow users to quickly make a payment without having to sign into the Customer Portal.  

##### Settings  
* A setting has been added for the organization’s time zone. This setting is used to control the display of the time within the Receivables portal.  

### Customer Portal  

##### Prepayment
* Prepayments can now be made to create payments that are not associated to invoices. Prepayments can also be made in the same payment as paying invoices.  

##### Continued Payments
* If the user were to leave the page while making a payment, they will be prompted to continue the payment if they attempt to make a new payment in one hour. 
##### Payment Experience Enhancement
* The user experience while making a payment has been enhanced to improve the experience of adding and selecting a payment method.  
##### Pass-Through Authentication
* When a merchant’s users are already signed into another system, their users now can be passed into the Customer Portal without having to sign in. See our [Pass-Through Authentication](https://github.com/PayFabric/APIs/blob/master/Receivables/PassThroughAuthentication.md) page for more detail.  


## 2/14/2019 

### Integration  
* Microsoft Dynamics 365 Business Central can now be integrated with PayFabric Receivables.  


## 1/31/2019  

### Receivables Portal  

##### Integration Report  
* A new report is available to manage the integration status of payments  

##### Settings  
* A new Integration Method setting is available to configure the method of retrieving records. The following options are available:  
	* API – The API will be queried on a regular basis to check for new records.  
	* Notification – Receivables will notify the integrating system of new records.  
* New options are available for copying the integration key and displaying the integration key password.  

##### Menu  
* Help documentation is now accessible from the PayFabric Receivables menu  

### Customer Portal  
* Improved User Experience on Login, Forgot Password, Forgot User Name and Registration pages.  


## 12/10/2018 

### Launch of PayFabric Receivables  
