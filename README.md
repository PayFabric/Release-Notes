# Release Notes

## 1/29/2025

### Integration Enhancements

* The SAP Digital Payments integration now supports surcharging capabilities.

## 11/21/2024

### Integration Enhancements

* Automated data synchronization between PayFabric and Sage Intacct is now available. Sage Intacct users can now configure their PayFabric organization to automatically synchronize Customers, Invoices and Payments from Sage Intacct with PayFabric.

## 10/23/2024

**ADDED.** PayFabric authentication is being updated to require multi-factor authentication for all users. All users will need to validate their email address and configure multi-factor authentication after this release.

**UPDATED.** Change the invocation method with Nodus Framework assemble.

**UPDATED.** Change SMS provider.

**UPDATED.** Security Enhancements.

## 8/13/2024

### Customer Enhancements

* A new configuration option is available to allow for the email address associated with a customer’s outstanding invoices to be automatically updated alongside updates to the customer’s email address.

### Invoice Enhancements

* A new Invoiced To parameter is available from the API to associate another customer with an invoice. This new value will appear on the Pay Invoices page when the associated customer has invoices assigned to different customers.

### Email Enhancements

* A new Integration Status email notification is available to be sent to internal users to inform them of updates relating to the integration of records with another system.

### API Enhancements

* New Reporting API Endpoints are available to retrieve data in bulk for Customers, Invoices, Subscriptions, Payments and Emails.
* The Customer POST and PATCH APIs have a new parameter to control if updates to the email address should carry to the customer’s outstanding invoices.
* Invoice APIs have been updated to support the new Invoiced Customer feature.
* A Customer PATCH API is available for enabling updates to the customer ID.
* An update to the Customer DELETE API is available to allow for full deletion of a customer record and all data associated with the customer.
* New settings GET APIs are available for retrieving saved data relating to configured Email Templates and Invoice Types.

## 9/9/2024

**ADDED.** Add Prepaid Debit card type in PayFabric.

**UPDATED.** Remove the ability of transactions processing with both surcharge amount and tip amount.

**UPDATED.** Security Enhancements.

## 3/13/2024

**ADDED.** Portico Tokenization Support.

**ADDED.** Portico Gift Card Support.

**ADDED.** Portico CAD Support.

**ADDED.** Enable Merchant Level List of Accepted Domains on PayFabric. PayFabric will block the redirect if the passed-in-return-URL's domain is not whitelisted.

**UPDATED.** Performance optimization.

## 2/19/2024

### Customer Portal Enhancements

* New configuration options are available to easily adjust the colors of the customer portal.
* New configuration options are available to easily adjust the size and alignment of the company logo displayed at the top of the customer portal.
* A new customer summary page is available for a quick overview of the customer account, this new page acts as the default landing page for the customer portal when a user logs in.
* The customer Wallet page has been completely redesigned to provide a more user-friendly view of the saved payment methods in the customer’s wallet.
* If a customer user is locked out of the customer portal due to failed password attempts, a new option is available to unlock the customer user account immediately.

### Payment Enhancements

* After accessing the customer portal using a secure link and completing a payment, an option to create an account for the customer portal can now be presented to the user.
* Payment Status will now be displayed as an additional column on the Payment report page.

### Email Enhancements

* Invoice Reminder email templates with the option to be sent manually configured have been migrated to be labeled as Payment Request · Single Invoice email templates. This change was made to help distinguish Invoice Reminder email templates as emails sent on an automatic scheduled basis and Payment Requests as emails sent on an on-demand basis.
* A new Invoice Reminder · Multiple Invoice email is available to be sent to notify customers of multiple outstanding invoices in a single notification. This email can contain a single payment link to allow the recipient to pay multiple invoices on their account at once.
* A new Payment Method Request email is available to be sent to request for a customer to provide their payment details without having to complete a payment.
  * A new user permission is available to control if a user is able to send this email. Integration records created through this mechanism.
  * Completed Payment Methods Request can be included as integration records in the Integration report.
* A new AutoPay Request email is available to be sent to request for a customer to activate AutoPay on their account without requiring the recipient to register for the customer portal.
  * A new user permission is available to control if a user is able to send this email.
* A new Payment Request · Prepayment email is available to be sent to request for a customer to make a payment that is not associated with any invoices.
* A new AutoPay Activated email is available to notify customers when AutoPay has been activated on their account.
* A new AutoPay Updated email is available to notify customers when their AutoPay terms have been updated on their account.
* A new AutoPay Deactivated email is available to notify customers when AutoPay has been deactivated on their account.
* A new AutoPay Upcoming Notification email is available to notify customers a few days before their automatic payment is planned to run.
* New PrepaymentAmount and PaymentTotal variables are available on the Payment Request email templates for both single and multiple invoices to allow for these emails to support communicating a prepayment amount included with the Payment Request to the recipient.

### API Enhancements

* A new Company/Style PATCH API is available for adjusting the new settings relating to the company colors and logo.
* A new PaymentMethod/Request POST API is available for generating a Payment Method Request link and sending out the Payment Method Request Email.
* A new AutoPay/Request POST API is available for generating an AutoPay Request link and sending out the AutoPay Request Email.
* The Invoice GET API now returns the Invoice Status.
* The Settings/Payment/Preferences PATCH API has a new The CreateAccountAfterLink parameter to support the new related setting.
* The Settings/Integration PATCH API has a new PaymentMethodIntegration parameter to support the new related setting.
* The Payment/Request POST API supports additional parameters related to supporting prepayments and the Authorization transaction type.
* New updates are available for Pass-through Authentication such as an internal permission role, the ability to hide the menu and additional landing pages for the customer Summary and User pages.

## 11/16/2023

**ADDED.** Provide the ability to override TrxInitiation Value during wallet creation via API and hosted wallet page.

**ADDED.** Provide the ability to filter by Device ID, PayFabric Gateway Profile, First Name, and Last Name of credit card on the Manage Transactions page and Retrieve Transactions API.

**ADDED.** Add validation support for saving PayFabric wallet entries.

**ADDED.** PayFabric Payment Javascript SDK V3, embedded UI responsive hosted create/update wallet pages.

**ADDED.** Add the ability to remove the deactivated user(s) from the merchant's PayFabric account.

**UPDATED.** Add Payment Method as the new filtering option to custom report on PayFabric. This enhancement enables merchants to generate transaction reports, specifying their preferred payment method inclusion for more customized tracking and analysis.

**UPDATED.** Enable cardholder's name to be optional during wallet creation and transaction processing.

**UPDATED.** Enable PayLink to control available payment methods for payment links based on gateway profile setup.

**UPDATED.** Update PayFabric Manage Transactions report to default to display 6-months worth of transaction data. Merchants can still search for transactions older than 6-months using the filter option.

## 9/5/2023

**ADDED.** Supports Global Payments gateway.

## 7/5/2023

**ADDED.** Tax amount Auto-calculation - Provide merchants with L2/3 qualification by auto-calculate the tax amount for L2/3 based on the specified value under Level 2 Optional Defaults 'Tax Rate' field.

## 5/30/2023

**ADDED.** Bulk Wallet Delete - Provide merchants the ability to remove the existing saved wallet records in bulk.

**ADDED.** Referenced Authorization & Sale Transaction Support - Enable 3rd party integrators to conduct 'Sale' or 'Authorization' transactions using a previously successful transaction as a reference, eliminating the need to re-enter credit card details. This new functionality introduced to PayFabric API specifically caters to eCommerce businesses that encounter backordered products or delayed shipments, wherein credit card information was not previously stored.

**ADDED.** Override Duplicate Wallet - Provide merchants the ability to override the existing wallet record with newly provided data in the case of duplicate entry.

**UPDATED.** Added the 'SANDBOX' into the top navigation banner for sandbox platform to help users easily identify between sandbox and production PayFabric environments.

**UPDATED.** Updated the “Fail On CVV2 Mismatch” logic for PayFabic SDK where it does not require CVV for alternative payment methods.

## 5/9/2023

### PayFabric Partner Enhancements

* PayFabric Partners can now personalize the PayFabric Receivables experience by controlling which functionalities are displayed to users.
* PayFabric Partners can now preconfigure default values for settings for faster initial deployment for new users.

### Invoice Enhancements

* A frequency interval is now available for Subscriptions to define a number of days or number of months between cycles.
* A Payment Request can now be sent from the Invoice Editor before the Invoice is completed.
* A new option to pay multiple invoices at the same time is available from the Invoice Report.

### Payment Enhancements

* A frequency interval is now available for AutoPay Templates to define a number of days or number of months between cycles.
* A starting day of the week configuration option is available to specify the day of the week for AutoPay to start.
* A new option is available from the Payment Report to send Payment Requests for multiple invoices.

### Email Enhancements

* New Payment Request email templates are available for requesting for payment from customers.

### API Enhancements

* New APIs are available to configure all the PayFabric Receivables settings.
* The FrequencyInterval parameter is now available for the AutoPay and Subscription APIs.
* A new Payment/Request POST API is available to trigger the generation of a Payment Request link and send the Payment Request email.
* Invoice APIs now support the Status parameter to allow for the Invoice status to be updated by integrating applications

## 1/17/2023

**ADDED.** Settlement and Reconciliation Report - Provides merchants and integration partners the ability to query settled transaction data and details via PayFabric API and directly from the PayFabric merchant portal. These reports will help merchants further with performing transaction reconciliation needs.

## 8/16/2022

### Customer Enhancements

* Customers can now be marked as tax exempt and a tax exempt number can be assigned to the customer.
* The data on the Customer Report can now be exported to an Excel spreadsheet.

### Invoice Enhancements

* The data on the Invoice Report can now be exported to an Excel spreadsheet.
* Taxes can now be configured for automatic tax calculation on invoices.
* Items can now be marked as tax exempt.
* Subscription invoice plans can now be created to automatically have invoices generated on a scheduled basis.
* A payment method can be assigned to a subscription plan to allow for automatic payments to be processed when the subscription invoice is generated.

### Payment Enhancements

* New payment methods of Google Pay, PayPal and Apple Pay are now supported for customer payments.
* A payment can now be initiated from the Invoice Report by clicking an applicable invoice record
* A payment can now be initiated from the Payment Report.
* The data on the Payment Report can now be exported to an Excel spreadsheet.
* Payments can now be processed directly on new invoices from PayFabric Receivables.
* A transaction associated to a payment record can now be reversed.

### Data Import Enhancements

* The user experience for selecting a template and downloading sample templates has been enhanced.
* Subscription & Tax data types are now available for import.
* Commonly associated data types are now paired to be selected together such as Invoices with Invoice Items and Payments with Payment Applications.

### Email Enhancements

* New versions of the New Invoice Notification email templates are available for invoices that have been paid and partially paid before they are completed and made available to customers.
* A new email template is available to be automatically sent when a payment associated to a scheduled subscription invoice fails to be approved.

### API Enhancements

* New GET and POST APIs are available for Taxes and Subscriptions
* Customer & Invoice APIs have been updated to support additional tax related parameters.

## 6/13/2022

**ADDED.** EVO Gift Card Support - Provide merchants the ability to process gift card transaction in both card-present and card-not-present scenario via EVO Gift program. This enables merchants to offer flexible payment methods to their end customers.

**ADDED.** Set Preferred Timezone - Provide merchants the flexibility to choose their preferred timezone on PayFabric portal. This will control their transaction report view and have all the reports associated with their chosen timezone. NOTE: Please check with your software vendors integrating to PayFabric to ensure their software version(s) supports this change.

**UPDATED.** Change the behavior of directing user to the login page for unauthorized hosted page, it will now display 'unauthorized' error message to user to improve the user experience.

## 1/27/2022

**ADDED.** ACH Transaction Return Reports - Provide ability for PayFabric merchants to query and lookup ACH returns associated with all EVO ACH transactions using PayFabric transaction reports.

**ADDED.** Sandbox Gateway Profile Default - Ability to support EVO Gateway Profile as the default for every new sandbox account.

**UPDATED.** Enhanced PayFabric Transaction Receipts to provide specific receipt template based on PayFabric's device. The previous PayLink transaction receipt is now merged together with PayFabric's transaction receipt.

**UPDATED.** Enhanced PayFabric EVO Connector to address the timeout on the backend connection.

## 11/11/2021

**ADDED.** Support Apple Pay - Merchants using PayFabric service can offer Apple Pay as a virtual wallet option during checkout process to their customers.

**ADDED.** Support Google Pay - Merchants using PayFabric service can offer Google Pay as a virtual wallet option during checkout process to their customers.

**ADDED.** Support New EMV Devices - PayFabric added PAX A60, A80 and A920 as new supported EMV devices.

**ADDED.** Support Auto board with EVO NOW. - Adding support for automatic onboarding with EVO Onboarding API.

**ADDED.** Support Snap’s Tip amount on MRHPP. - Adding tip amount support into PayFabric's mobile ready hosted payment page.

**ADDED.** Support Partial Reversal and Incremental Authorization for EVO connector transactions.

**ADDED.** Support EVO's Multi-Capture function to capture a portion of an Authorization transaction to support partial shipment.

**UPDATED.** Enhanced Partner Portal for PayFabric's integration partner.

**UPDATED.** Updated PayFabric API to support 'usebluefin' and'usedefaultwallet' as query string parameters.

**UPDATED.** Updated PayFabric login and access page UI to provide a modern look and feel.

**UPDATED.** Removed and retired the legacy Cybersource SCMP Connector.

## 09/28/2021

**ADDED.** Payment Advice can now be submitted to the SAP Digital Payments Add-on from PayFabric

**ADDED.** Level 2 & 3 transaction data is now supported with the SAP Digital Payments Add-on

**UPDATED.** Preauthorizations from the SAP Digital Payments Add-on will now use the Verify transaction type instead of a zero dollar authorization.

**FIXED.** Bluefin Cardholder's data parsing to address First Name and Last Name order placement.

## 07/20/2021

**ADDED.** Add an authentication method for boarding api

**ADDED.** Add Batch Close time in the response for "GET /setupid/" API

**ADDED.** PayFabric APIs Control

**ADDED.** PayLink APIs Control

**ADDED.** Add Transaction State and Settlement Details to all Transaction APIs

**ADDED.** Add eService Certification with EVO Snap* and support 3D Secure 2.0

**ADDED.** Advice Support for SAP DPA

**ADDED.** Add ability to Process Manual Batch Close via API

**UPDATED.** Set maximum custom report limit to 20

**UPDATED.** Reduce EVO Snap* Timeout From 100 to 37 Seconds

**UPDATED.** Return 'EntryMode' in PayFabric GetTransaction API

**UPDATED.** Custom Reports should support additional Transaction State (formally Settlement Status) values

**UPDATED.** Processed Transaction should return Saved Wallet ID

## 7/6/2021  

Video: [https://www.youtube.com/watch?v=dk1pwSeCNGs](https://www.youtube.com/watch?v=dk1pwSeCNGs)  

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

## 04/19/2021

**ADDED.** Added the mobile ready hosted payment page to provide fully responsive hosted payment page, designed to enhance user experience on mobile devices.

**ADDED.** PayPal transaction acceptance will be available as an additional payment method against the new PayFabric’s mobile ready hosted payment page.

**ADDED.** Supports integration to upcoming EVO ACH platform for ACH transaction processing.

**FIXED.** Should not calculate surcharge when user enters an invalid credit card number.

**FIXED.** Provided the support to include 'Display Name' if there is a need to change the default 'From' email address.

**FIXED.** Addressed PayLink’s Level 3 issues with Paymentech’s PNS platform.

**FIXED.** Addressed Service Agreement issue with browser that prevent user to be able to agree and accept the terms and conditions.

**UPDATED.** Updated the videos and contents on PayFabric services’ splash pages.

## 01/25/2021

**ADDED.** Provide ability to support _Verify_ transaction with Create/Update/Process Transaction API for EVO gateway.

**ADDED.** Transition 5-digits short codes to toll-free number due to carriers' industry mandate for text messages.

## 1/21/2021

Video: [https://www.youtube.com/watch?v=r3DqgNq72Tw](https://www.youtube.com/watch?v=r3DqgNq72Tw)  

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

## 12/09/2020

**ADDED.** Added Data Level Qualification option for 'ItemAmount' and 'ItemCost' fields on form setting.

**ADDED.** Provide ability for B2B partner to control the merchants IgnoreDuplicate for EVO gateway.

## 11/12/2020

**ADDED.** Enhancement to PayFabric L2/L3 BIN Range Validation and Form Settings where line items details are only required on the virtual terminal if card level is purchasing/corporate/business card.

**ADDED.** Added a new menu called Integrations under PayFabric Settings. This Integrations menu will contain the existing Bluefin P2PE integration. There is also a newly added integration support for SAP DPA, a cloud digital payment platform for SAP.

**ADDED.** Provide ability to specify a PageSize parameter for Get Transaction API, supported max page size is 15. This new added parameter is optional.

**ADDED.** Provide ability to specify an End Date parameter for Get Transaction API to filter transactions during retrieval from PayFabric. This new added parameter is optional.

**ADDED.** Added new fields for Cybersource to support new Refund Authorization logic for refund transaction.

**FIXED.** Properly handle the error ‘Bad Request – Request Too Long’ on PayFabric hosted page with Chrome browser for SameSite=default cookies.

**FIXED.** Properly updated organization name across PayFabric portal, email receipts and services.

**FIXED.** Addressed CybersourceSOAP/Cybersource gateway issue where it does not accept Mastercard number with a  2-digit BIN.

## 8/19/2020

**ADDED.** Enhancement to PayFabric to support surcharge with EVO processing platform.
**Important Note: Merchants must register with the card brands to be enrolled in the surcharge program prior to use this feature on PayFabric. Contact PayFabric Support to request for assistance to sign up with surcharge program.**

**ADDED.** Enhancement to PayFabric's sale and credit ceiling to allow merchant to configure maximum transaction amount for both sale and refund transaction for specific payment method (credit card and eCheck). This is available on both global and user level.

**ADDED.** Support multiple email addresses in PayLink API and PayLink portal.

**ADDED.** Support multiple shipping email addresses in PayLink API and PayLink portal.  

**ADDED.** Support CIT/MIT for CybersourceSOAP with Moneris processor.

**ADDED.** Added validate transaction type for additional CybersourceSOAP processors for CIT/MIT.

**FIXED.** Corrected card type mapping from AmericanExpress to Amex for Paymentech and CybersourceSOAP gateways.

**FIXED.** PayFabric is updated to handle the scenario with negative line item amount as negative amount is not supported on EVO connector.

**FIXED.** PayFabric is updated to omit tax exempt details for void transaction to resolve the DTD error for Paymentech connector.

**FIXED.** PayFabric is updated to address L2/L3 issue on American Express for EVO connector to restricted to only whole number on the line item quantity.

**FIXED.** PayFabric is updated to address an issue with force transaction for CybersourceSOAP connector with AIBMS processor.

**FIXED.** PayFabric is updated to address an issue with Forte gateway regarding FailOnAVSAddress, FailOnAVSZip and FailOnCVV2 identifiers are not supported.

**FIXED.** PayFabric is updated to address an issue with CybersourceSOAP gateway regarding processing Authorization transaction with Elavon processor.

**FIXED.** PayFabric is updated to change the column name 'CardName' to 'CardType' within the downloadable custom report. This will maintain the consistency with the custom report fields on the user interface.

**FIXED.** PayFabric is updated to trim the trailing space for unit of measure value on Payeezy connector.

## 8/5/2020

Video: [https://www.youtube.com/watch?v=SuyJzXPJ2Yc](https://www.youtube.com/watch?v=SuyJzXPJ2Yc)  

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

## 6/16/2020

**ADDED.** Enhancement to PayFabric's merchant portal to improve performance across entire site.

**ADDED.** Enhancement to support From email update specifically for PayFabric Receivables.

**ADDED.** Added ability to enable 3rd party application to suppress automatic email receipt from PayFabric during API call.

**ADDED.** Added support for $0.00 unit price on PayLink.

**ADDED.** Added prompted warning message for EMV transaction if user clicks 'Back' or 'Close' browser on-screen with "Communicating with Terminal'.

**UPDATED.** Updated data serialization logic related to L2/L3 support and performed additional code refactoring and tuning specifically for EVO connector.

**FIXED.** Addressed the issue with boarding API not able to post data to provided callback URL during merchant boarding.

## 6/5/2020

Video: [http://www.youtube.com/watch?v=V7jTXq3QQOc](http://www.youtube.com/watch?v=V7jTXq3QQOc)

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

* A new API help page is now available to make it easier for developers to work with the Receivables API by providing interactive tests and sample data. [https://sandbox.payfabric.com/receivables/apihelp](https://sandbox.payfabric.com/receivables/apihelp)

## 5/11/2020

**UPDATED.** Enhance Level 2 and Level 3 Support with the following changes:

* Update User Interface to improve user experience for Level 2/3 Field Defaults on Modern design.
* Update Form Settings for Virtual Terminal’s Web Entry to provide merchant flexibility on field display options during transaction processing.
* Added BIN Range Validation option for Level 2 and 3 Support.
* Providing portal virtual terminal users the ability to lookup line item data (Level 3) using uploaded products/items during transaction processing.
* Add ability to upload products/items to be used during transaction processing on Virtual Terminal.

**ADDED.** Enhancement to PayFabric to extend the support for Visa’s credential-on-file (COF) mandate for both Paymentech and Cybersource gateways.

**ADDED.** Added ability to export customer list from partner’s portal.  

**ADDED.** Added support for organization management under user role and permission.

**ADDED.** Added support for negative quantity line item on PayLink.

**UPDATED.** Updated all card brand logos on PayFabric to most recent logo version.

**UPDATED.** Updated session timeout to 15 minutes for better user experience.

**FIXED.** Add BCC option will no longer bring the cursor to the top of the page and will maintain the user to be within the BCC section to enter email address for BCC.

**FIXED.** Ensure the partner organization’s ‘from’ email is being used for resend email receipt.

**FIXED.** Browser compatibility support with ‘SameSite’ attribute on cookies.

**FIXED.** Addressed issue with sporadic status change for generated payment link due to caching.

## 1/16/2020

### AutoPay

* Customer's can now be registered for automatic recurring payments. Multiple frequency and payment amount options are available.

### AutoPay Templates

* The organization can specify the settings for how automatic payments should be processed based on the business preferences. Multiple templates can be created to provide different AutoPay options to customers.

### AutoPay E-mail Templates

* New e-mail templates are available to be sent to customers when an AutoPay payment is approved or fails to be processed.

## 9/19/2019

**ADDED.** Sandbox environment for PayFabric [V3] Merchant Portal will be separated from Production environment. **NOTE:** V2 sandbox & production URLs remain the same.

The PayFabric sandbox environment for V3 can be accessed via the following URL:

   **PayFabric Sandbox**: <https://sandbox.payfabric.com/portal>

PayFabric Production environment URL remains the same:

  **PayFabric Production:** <https://www.payfabric.com/portal>

PayFabric Production and Sandbox user account credentials will be completely separated. If you have an existing PayFabric sandbox account, it will automatically get migrated to the new environment and can be accessed using the same user credentials you are currently using today. Going forward, changes made against an account from one environment will not impact the other environment.

The ability to toggle between production and sandbox environments will no longer be available on the PayFabric top navigation bar. The ability to copy PayFabric settings from sandbox to production during Production switch will also no longer be available. The ability to self-register on Sandbox will remain the same but the ability to self-register a Production account will be removed. Merchants with a need for a Production PayFabric account can be setup by PayFabric Support team or through our PayFabric integration partners.

## 8/06/2019

**ADDED.** Enhancement to PayFabric to provide the support for Visa’s credential-on-file (COF) mandate to identify initial card storage and subsequent use of card information. The COF mandate is intended to provide merchants with higher transaction approval rates. For cardholders, they are expected to benefit from enhanced visibility of card storage or usage and a better overall experience. This feature support is currently only available to EVO connector, support for other gateways will be added later as available.

**UPDATED.** Similar to Billing Address, PayFabric was changed to not require a complete submission of shipping address information during API call or on hosted page.

**UPDATED.** Currently, PF uses the Tender in Card object to get the default gateway profile when creating/processing transaction. Therefore, the card information is required. In order to support use case where card information is not available during transaction creation, we updated PF to use Tender detail from the Transaction object to get the default gateway profile.

**FIXED.** Unable to load saved wallet records on IE, Safari and Edge for modern design VT when select a customer number using auto-complete customer list.

**FIXED.** Partner Portal access to PayFabric Receivables service.

## 7/17/2019

### Receivables Portal

#### Data Import

* Data can now be imported to PayFabric Receivables using a spreadsheet file. The following data sets can now be imported to the portal:  
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
* This export is available when the _Integration Method_ setting is set to the new _File_ option.  

### Customer Portal  

#### Payment Terminal and P2PE Device Support  

* Internal users making payments can now use PayFabric supported payment terminals and point to point encryption P2PE devices for more secure entry of credit card data.  

## 7/07/2019

**ADDED.** Enhance Level 2 and Level 3 Support by providing portal virtual terminal users the ability to enter line item data (Level 3) during transaction processing.

**UPDATED.** Enhance Level 2 and Level 3 Support for Field Level Default by card types.  

**ADDED.** Add End User License Agreement and Service Agreement prompt to portal for every new user account. The Service Agreement will only be prompted for account owner.

**ADDED.** Provide ability for partner to designate default ‘From’ email for corresponding merchant to partner’s support email address.

**ADDED.** Add the integration support for EVO Now boarding.

**UPDATED.** Update PayFabric’s caching framework.

**FIXED.** Update PayFabric's Cybersource connector to filter out '\n' in ItemProdCode and ItemDesc.

## 6/03/2019

**ADDED.** Provide ability to set the accepted tender type via Wallet Link API and PayLink Portal.

From API, add AcceptType field in Create Wallet Link request body

0 or null or other value: Accept both credit card and ECheck

1: Credit Card

2: ECheck

**ADDED.** Add the support of basic authentication for PayFabric API using Device ID and Password.

**FIXED.** Exclude EMV Terminal transactions from gateway profile's transaction report as these transactions do not go through normal payment gateway for processing.

## 05/20/2019

**ADDED.** Provide merchant with the ability to automate settlement by a predefined time or manually settle pending transactions.

**ADDED.** Enhanced reporting capabilities by enable merchants to run settlement reports based on the transaction’s settlement status.

**UPDATED.** Enhance the user interface for the existing PayFabric Default Gateway Settings by grouping it together under Gateway Account Profiles sub-menu options.

**FIXED.** Remove inactive user(s) from custom report table so custom report does not get sent to inactive user(s) from PayFabric.

**ADDED.** Added mapping fields for CybersourceSOAP connector commerceIndicator (ID=145) and  ItemcommodityCode (ID=117).

**ADDED.** Support settlement for EVO connector.

**FIXED.** Truncate the combined value of First Name and Last Name to 30 characters for Paymentech Orbital connector.

## 4/9/2019

### Receivables Portal

#### Integration

* Enhanced user experience when loading payment details
* From the Integration Report, the Payment ID and Identity can be updated and the Application of Payment to Invoice can be removed before the payment is integrated.

#### Express Pay

* From the New Invoice Notification E-mail, the ExpressPayLink variable is now available. When this variable is combined with the CustomerPortalURL variable, it will create a full link in the e-mail to allow users to quickly make a payment without having to sign into the Customer Portal.

#### Settings

* A setting has been added for the organization’s time zone. This setting is used to control the display of the time within the Receivables portal.

### Customer Portal

#### Prepayment

* Prepayments can now be made to create payments that are not associated to invoices. Prepayments can also be made in the same payment as paying invoices.

#### Continued Payments

* If the user were to leave the page while making a payment, they will be prompted to continue the payment if they attempt to make a new payment in one hour.

#### Payment Experience Enhancement

* The user experience while making a payment has been enhanced to improve the experience of adding and selecting a payment method.

#### Pass-Through Authentication

* When a merchant’s users are already signed into another system, their users now can be passed into the Customer Portal without having to sign in. See our [Pass-Through Authentication](https://github.com/PayFabric/APIs/blob/master/Receivables/PassThroughAuthentication.md) page for more detail.

## 03/31/2019

**ADDED.** Add Custom Reports with automatic email notification based on predefined frequency.

**ADDED.** Batch Processing Support for PayFabric Virtual Terminal with Modern Design.

**ADDED.** Pay Later Processing (Scheduled Transaction) Support for PayFabric Virtual Terminal with Modern Design.

**UPDATED.** Enhance the existing PayFabric Boarding from Partner Portal & API.

* Provide the ability for partner to cancel an existing boarding.
* Provide ability for partner to disable 'New Merchant Account Sign Up' option for new merchant boarding.

**UPDATED.** Make the billing email address optional for CybersourceSoap and Cybersource from PayFabric's validation.

**FIXED.** Unable to perform partial refund due to the error: “The refund amount should not greater than the original transaction amount.”

## 2/14/2019

### Integration

* Microsoft Dynamics 365 Business Central can now be integrated with PayFabric Receivables.

## 1/31/2019  

### Receivables Portal

#### Integration Report  

* A new report is available to manage the integration status of payments  

#### Settings

* A new Integration Method setting is available to configure the method of retrieving records. The following options are available:  
  * API – The API will be queried on a regular basis to check for new records.  
  * Notification – Receivables will notify the integrating system of new records.  
* New options are available for copying the integration key and displaying the integration key password.  

#### Menu  

* Help documentation is now accessible from the PayFabric Receivables menu  

### Customer Portal

* Improved User Experience on Login, Forgot Password, Forgot User Name and Registration pages.  

## 01/28/2019

**ADDED.** Add additional parameters/variables into the PayFabric email receipt templates.

* [[[TransactionStatus]]] - PayFabric Transaction Status
* [[[TransactionMsg]]] - PayFabric Transaction Message
* [[[AuthCode]]] - Gateway Authorization Code
* [[[CVV2Response]]] - Gateway CVV2 Response Code
* [[[AddressResponse]]] - Gateway Address Response Code
* [[[[ZipResponse]]] - Gateway Zip Response Code

**ADDED.** Enhance PayFabric Partner Portal to provide ability to add new merchant on PayFabric with configurable permission.

**UPDATED.** Enhance the user experience and user interface for the modern design of virtual terminal.

* Adjust modern design of the virtual terminal page to reduce gap and white spaces between fields.
* Provide ability to edit form fields on modern version of virtual terminal. User can toggle the option to show/hide or make a field required/optional using the newly enhanced Form Settings page.

**UPDATED.** Rename existing transaction types on PayFabric [portal and API] to follow payment industry common terminologies

* Book is now Authorization
* Ship is now Capture
* Credit is now Refund
Note: PayFabric API is still able to support the old transaction types for backward compability purpose.

**UPDATED.** Transform the user interface for the PayFabric Email Receipts Templates page into a modern look for better user experience.

**ADDED.** Add ability to save changes to all email receipt templates. - To make it easier for user to make changes on message body across all email receipt templates, the newly added 'Save to All Templates' will save the changes to the message body to all existing templates.

**UPDATED.** Remove the 'Locked' flag from PayFabric Wallet grid.

**UPDATED.** PayFabric logout and organization maintenance options are accessible via mobile devices.

**FIXED.** Ability to accept masked card number and billing address when creating simulated transaction on PayFabric.

**ADDED.** Added the newly supported NMI payment gateway for credit card processing.

**FIXED.** Ability to pass shipping address per invoice/document for multiple invoice payment link.

**ADDED.** Added support for PayFabric Receivables as a newly optional add-on service to PayFabric. It gives businesses the tools to streamline their online presentment and payment needs. Merchant's customers can review outstanding invoice details and make payments themselves, 24/7 via a hosted online customer portal.

**FIXED.** Address issue with duplicate transaction processing on PayFabric by pressing the 'Enter' key on keyboard simutanuously. This fix applies to both web entry and terminal entry processing.

**FIXED.** PayLink Document API - Address the issue with 'IsMultipleInvoice' flag being changed to 'false' when trying to update the integration status for a payment link.

## 12/10/2018

### Launch of PayFabric Receivables

## 10/30/2018

**ADDED.** New Email Receipt template - Provide an enhanced version for payment confirmation receipt for all payment processed transaction.

**UPDATED.** Rename ‘System Default’ device name to ‘Virtual Terminal’ - To make it more descriptive for portal user, the legacy ‘System Default’ device is renamed to ‘Virtual Terminal’ to represent the virtual terminal device where merchant can process transaction directly on PayFabric.

**ADDED.** Portal Menu Settings Changes - Enhance the user interface and user experience on PayFabric portal around the following areas:

* **Settings** > Add additional sub-menu under Settings page to include all the configuration settings pages to promote less scrolling for portal admin user.
* **DEV Central** > Re-design DEV Central page to break down into different tabs of configuration settings for PayFabric.

**ADDED.** Add Virtual Terminal Design Mode

* **Legacy Design**: Maintain the existing user interface and experience for virtual terminal where user can mimic the hosted API calls for PayFabric and also review the custom’s device theme directly on PayFabric portal.
* **Modern Design**: Introduce a new user friendly design for Virtual Terminal to allow merchant to process transactions against PayFabric web portal via web entry and/or terminal entry.

**ADDED.** Discretionary Data - With the new provided ‘Modern Design’ mode for Virtual Terminal, merchant will have the ability to create their own custom field to associate additional data for each transaction with PayFabric.
Note: Discretionary data will only reside with PayFabric and will not be pass on to payment gateway or payment processor.

**ADDED.** Default Gateway Profile - With the new provided ‘Modern Design’, PayFabric provides merchant the ability to specify default gateway profile based on currency types so their internal user does not need to select a gateway profile at the time of processing a transaction.
Note: This functionality is supported through PayFabric API calls for all PayFabric apps/devices.

**UPDATED.** Re-design user roles and user permission configuration settings page - Enhance the user experience for user roles and user role’s permission page to promote less scrolling and cleaner look and feel for web portal user.

**ADDED.** Add additional validation around the usage of security token on PayFabric. - Embed IP Address validation around the usage of PayFabric security token against the PayFabric’s API calls. PayFabric added a new setting under Transact Settings called ‘IP Address Validation for Security Token’. By default, this setting is **enabled**.

* If **enabled**, PayFabric will validate the security token’s IP address. If the IP address associated with the security token at the time of token creation does not match the security token at the time of token consumption, PayFabric will return the ‘failed authentication’ error during API calls.
* If **disabled**, PayFabric will not validate the security’s token IP address during API calls.

**ADDED.** Add Payment Document’s Length and Prefix configuration for PayLink’s GP integration - To provide more flexibility for merchant to easily identify the payment document created on PayLink portal from the payment document created directly inside GP or elsewhere, merchant is now able to associate with the PayLink document by specifying the document prefix and also the length of the PayLink’s payment document.

**UPDATED.** Changing the Email on PayFabric will also update the username associated to the PayFabric account. - To make it easier for Pay Fabric’s account owner to transfer the ownership to a different user, PayFabric now offers the ability to update the account owner’s username directly on PayFabric’s portal via Change Email option.

**ADDED.** Modifying the Customer’s ID against a specific wallet record. - User will now be able to edit/modify the Customer ID associated with a wallet record directly on PayFabric portal.
NOTE: If the Customer ID is associated to multiple wallet records, each wallet record needs to be updated individually to reflect the new Customer ID.

**ADDED.** Ability to dictate ‘From’ email address PayFabric offers the ability for merchant to use their own domain email address for the following external email communication to their customers instead of using the existing default <support@payfabric.com> to make it easier for their customers to recognize the original sender and avoid any confusion.

* PayFabric’s Payment Confirmation Receipt
* PayLink’s Email Notifications
* PayLink’s Email Confirmation Receipt

**UPDATED.** Support multiple email addresses from transaction receipt. - PayFabric offers the ability for merchant to send email receipts to multiple recipients by separating the email addresses by semicolon or comma.

**ADDED.** Ability to resend an existing PayFabric transaction receipt to end customer. - PayFabric offers the ability for merchant to resend transaction email receipt to their customers.

**ADDED.** Ability to process partial referenced credit. - PayFabric offers the ability for merchant to process partial referenced credit/refund transaction for their customers.

**ADDED.** Ability to specify a default transaction type. - PayFabric offers the ability for merchant to specify the default transaction type on PayFabric’s Virtual Terminal.

**UPDATED.** PayLink Document API Updates. - Update Document API: 3rd party integrations to PayLink API should be able to update/patch PayLink' s integration status to the following:

* From 'Integration Pending' to Integration Successful'
* From 'Integration Pending' to 'Integration Failed'

**UPDATED.** Removed Billing Address Validation for Hosted Pages, API and Virtual Terminal. - PayFabric had removed the partial billing address validation to enable merchant to support international billing addresses.

**FIXED.** Fixed the credit card entry issues - Address the credit card entry user experience issues on PayFabric’s hosted wallet page:

* Chrome’s autofill for credit card cannot detect card number/types.
* Incorrect cursor placement during wallet entry.
* Hold key down allows user to input more than the allowed number of digits per card type.

**FIXED.** Fixed CreatedOn date field for Wallet Link API. - Fixed the issue where CreatedOn date field does not have correct value when call ODATA query for Wallet Link API.

**FIXED.** Added ModifiedOn date field for Wallet Link API. - Fixed the issue where the ModifiedOn date field was not included as part of the Wallet Link API’s response.

**FIXED.** Fixed CreatedOn date field for PayLink API. - Fixed the issue where CreatedOn date field does not have correct value when call ODATA query for PayLink API.

**ADDED.** Add a redirection to Process Message List page as a popup box on Manage Transaction report - After processing a referenced transaction, user will be redirect to the Process Message List page to view the transaction status.

**ADDED.** Enhance Daily Activity Report. - Add ability to view ‘Receipt’ into Daily Activity Report. New columns in report grid: Actions

**ADDED.** Added Integration Status to exported PayLink document report. - Add a new column for Integration Status into exported PayLink document (excel, CSV) report.

## 07/15/2018

**FIXED.** Allow zero [0] quantity submission from PayLink API - PayLink API will be able to support zero [0] quantity line items to cater for sales document with backordered quantity in accounting system.

**ADDED.** Ability to process a PayFabric transaction without a Customer Number - Customer Number is now an optional field to process a transaction in PayFabric. However, Customer Number is still a required field for creating/saving new wallet entry.

**ADDED.** Enhancement to Daily Activity Report

* Added ‘-All-‘ filter option for payment method so user can search transaction result for all payment types: credit card, debit card and eCheck.
* Add more filter options and columns into Daily Activity Report.

New columns in report grid:

* Account #
* User ID

New search filter options:

* By amount range
* Search all payment types
* By transaction status
* By transaction key
* By customer number

**ADDED.** Enhancement to Transaction Summary Report - Add ‘-All-‘ filter option for payment method so user can search transaction result for all payment types: credit card, debit card and eCheck.

**ADDED.** Transaction processing security settings into user role - Provide the ability to break down and restrict transaction processing for PayFabric user by transaction and payment types.

**ADDED.** Provide easy navigation between device & theme pages. Provide user an easier navigation to switch from device and theme pages.

**ADDED.** Add new Wallet Link GET APIs GET /api/wallet/{WalletLinkID}: Query a WalletLink and its details.
GET api/wallet/?$: Query Wallet Link(s) based on query string data.
Available Data to Query On:

* CustomerNumber: customer number specified at the time of creating a wallet link
* CreatedOn: date the wallet link was created on
* NotificationEmail: email specified at the time of creating a wallet link
* NotificationPhone: phone number specified at the time of creating a wallet link
* Status: 0=incomplete, 1=complete, 2=cancelled
* Device: device used at the time of creating a wallet link
* CompletedOn: the date the wallet link was completed on

**ADDED.** Enhancement to Wallet Link CREATE API - Enhance existing Wallet Link Create API by include the actual link into the response so 3rd party integrator does not need to compile and put the link together.

**ADDED.** Enhancement to Wallet Report functionalities - Combine Wallet and Expired Card reports into a single report with the following:

* Provide the user the ability to filter expired card with a given date range for expiration date
* Ability to delete expired cards from filter search.
* These columns on wallet report should be sortable: Customer #
* These columns on wallet report should be searchable: last 4-digits of card #, first name, last name, card type, expiration date. The search performed on each text input field for the column should be a partial match instead of exact match.
* Allow the report to be exported in the following formats: excel, tsv, csv.

**ADDED.** Ezidebit Gateway - Added support for new gateway [Ezidebit] for direct debit in Australia.

**FIXED.** Exported Document Queue list has different date compared to the one from PayLink portal. Fixed the issue so the date on the exported document is the same as the one from PayLink portal > paylink’s created date.

**ADDED.** PayFabric’s email receipt templates share the subject line and BCC email field value. Fixed the issue so the email receipt templates do not share the subject line and BCC email field value.

**FIXED.** Unable to edit Account Number for credit card on PF hosted pages. Fixed the issue to allow user to edit and change the digit(s) of the credit card number correctly.

**UPDATED.** Updated First Data's Payeezy connector/gateway mapping to map PF's Invoice Number field to Payeezy's TrxRefIndex to enhance merchant's transaction report capability.

**UPDATED.** Updated USAePaySOAP connector/gateway to map PF's Invoice Number field to USAePay's OrderID field to provide better merchant's transaction report capability.

## 06/29/2018

USAePay disabled the TLS 1.0 and 1.1 protocols from their Production environment as of June 29, 2018 at 1pm PDT.

Additional configuration change must be made to enable USAePay gateway to communicate via TLS 1.2 only from PayFabric. PayFabric added a new & updated USAePay Connector onto PayFabric’s Sandbox & Production for both V2 & V3 called ‘USAePaySOAP’. Please make a switch to this USAePaySOAP connector from the PayFabric Portal > Gateway Account Profile(s) for USAePay.

You can copy and reuse the existing production USAePay’s Source Key information. Here is the additional connection information you will need to add into your gateway profile:

Sandbox URL: <https://sandbox.usaepay.com/soap/gate>  

Production URL: <https://secure.usaepay.com/soap/gate>

Port: 443

Server.APIKey: 245VMXN8

SourceKey: (Your Existing API Source Key from USAePay portal)
  
Password: (Your Source Key's Password, if available, otherwise leave this blank)

InternalCardAuth: (blank)

## 06/06/2018

**ADDED.** Add Enable Security Token configurable setting on PayFabric portal to enable restriction on usage against PayFabric APIs. The PayFabric hotfix release includes a security enhancement to PayFabric to allow 3rd party application(s) integrating to PayFabric to set the restriction on the use of security token against the PayFabric APIs.
PayFabric will provide the ability to restrict the security token to be used in hosted page ONLY instead of both API & Hosted pages. The changes are as followed:
PayFabric will provide a new security setting called 'Enable Security Token' on PayFabric Settings with dropdown values below.

* For APIs and Hosted Pages: this is the default option where security token will be allow to use as the authentication method in both hosted pages and APIs.
* For Hosted Pages Only: with this option, security token will ONLY be allow to use as the authentication method in hosted pages. The API service response will fail authentication if any API calls was authenticated using security token.

This setting is device specific. By default, to maintain backward compatibility & to avoid any impacts to existing implementation, the default option will be 'For APIs and Hosted Pages'.

3rd party application can change this to 'For Hosted Pages Only’ if their application supports the ability to call PayFabric APIs via Device ID & Password.
  
NOTE: This change is applied to PayFabric version 2.0 as well.

**ADDED.** Add ability to authenticate with device id and device password for PayLink APIs. Due to the security enhancement [#1] from PayFabric, PayLink now has the ability to get authenticated using device ID and password instead of using security token.

## 05/07/2018

**ADDED.** Add Last UsedDate field into Wallet Report - Added LastUsedDate to help determine when the wallet record was last used for processing on PayFabric.

**ADDED.** Forte Gateway - Added support for US & Canadian Credit Card for all PF transaction types.

**ADDED.** Ability to over-capture on PayFabric Virtual Terminal - Utilize the same existing ‘Partial Shipping’ setting on PayFabric portal, if enabled, it will also allow users to ship more than the authorization/book amount.

**ADDED.** EVO Gateway - Added support for new gateway [EVO] for US & Canadian Credit Card for all PF transaction types.

**UPDATED.** Update Connection URLs for Paymentech Orbital Gateway - Modified Connection URLs for Orbital:

* Current Test: orbitalvar1.paymentech.net
* Current Live: orbital1.paymentech.net

* New Test: orbitalvar1.chasepaymentech.com
* New Live: orbital1.chasepaymentech.com

**ADDED.** Allow Edit Billing Information for Automatic billing - PayFabric now allows merchant to change billing information if originally signed up for Automatic billing.

**FIXED.** Check for duplicated card if saving wallet via API. Ensure duplicated card is checked even when saving new credit card records via API.

**FIXED.** Unable to update transaction if associated wallet record is deleted - Address the issue where transaction record cannot be updated if the associated wallet record had already been deleted.

**ADDED.** Add ability to paste card number into hosted wallet/payment page - User is now able to paste card number into hosted wallet/payment page for the ease of data entry.

## 01/08/2018

**ADDED.** Support PayLink Service - Offer PayLink service to new and existing PayFabric [v3] customers.

**Production:**

API URL: <https://www.payfabric.com/paylink/api>

Hosted Page URL: <https://www.payfabric.com/paylink/web>

Help: <https://www.payfabric.com/paylink/help>

**Sandbox:**
API URL: <https://sandbox.payfabric.com/paylink/api>

Hosted Page URL: <https://sandbox.payfabric.com/paylink/web>

Help: <https://sandbox.payfabric.com/paylink/help>

**ADDED.** Support PayLink integration with SalesPad API - Offer PayLink integration to back office SalesPad Desktop for all successful payments from PayLink.

**ADDED.** Return of the URL in the Create a PayLink response. Support the inclusion of PayLink URL in the Create a PayLink response so 3rd party application does not need to reconstruct the PayLink URL using PayLink ID.

**ADDED.** Hosted DNS Server Support for EMV - PayFabric will offer hosted DNS server for EMV terminal support. This will make it simpler to auto-register a new IP address for the hardware device to associate with the SSL certificate.

**ADDED.** Enable/Disable EMV from hosted page. Allow 3rd party application to enable/disable EMV on-the-fly on a per-transaction basis via the following query string parameter.

* ProcessingMethod=0: Web Entry only
* ProcessingMethod=1: EMV only
* ProcessingMethod=2: Both Web Entry and EMV

**UPDATED.** Changes to PayLink API Status

0: Draft

1: Pending

2: Cancelled

3: Paid

IntegrationStatus

0: Pending

1: Failed

2: Successful

**ADDED.** Billing and shipping address submission via Create Transaction API - Enable application to pass in billing and shipping information during transaction creation without card information.

**ADDED.** Add user role for EMV and Bluefin - Offer role-based permission control for both EMV and Bluefin features.
