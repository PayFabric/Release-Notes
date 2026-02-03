# Release Notes

## 2/2/2026

### Organization Enhancements

- The New View is now the default view for new users
- New pages are available for accepting the PayFabric User and Service Agreements.
- The personal user account page is now available from the menu on the New View. This page now offers the ability for users to reset their password as well.

### Transaction Enhancements

- Additional Card Present Terminal support is supported through the Global Payments Unified Cloud Integration platform integration.
- A new connector, Global Payments - Transaction API, is available for additional processing options within Global Payments for ACH transactions.

### Email & Communication Enhancements

- Additional options are available for the Integration Status Notification such as the ability to only send the notification when an integration failure occurs and the ability to increase the frequency up to every 4 hours.

### Integration Enhancements

- Data field mapping options are now available for integration connectors such as Sage Intacct and Quickbooks to configure the PayFabric destination location for data parameters from the accounting system.

### General Updates

- Additional security enhancements and system improvements are available.

## 10/22/2025

### Organization Enhancements

- The Customer Portal Name can now be updated to change the name and URL displayed in the customer portal.

### Customer Enhancements

- A new Phone field is added to store the customer’s phone number and is used as the primary contact for text notifications.
- The Send AutoPay Request added the ability to send requests through text notification to remind customers to set up a recurring payment plan.
- A Send Payment Method Request option is added to allow users to request a payment method via email or text.

### Invoice Enhancements

- The limit for creating Invoice Types has been increased to 50.
- An Individual Payments option is added to classify invoices of that type to be paid individually rather than grouped.
- Invoice Table Display Settings now include an option to show or hide the Invoice Type column to help identify payment restrictions in the Customer Portal.

### Payment Enhancements

- A new Payment section in Currency Settings is added to allow configuring Additional Payment Profiles by assigning Invoice Types to specific Payment Account Profiles that determine which invoices use each profile.
  - These configurations apply automatically across Customer Portal payments, Subscription Invoices, Payment Requests, and AutoPay Payments.
- Payment Reports now include a User column showing who initiated each payment.

### Email & Communication Enhancements

- Text notification templates can now be configured for Payment Requests, AutoPay Requests, and Payment Method Requests.
- Users can insert a URL in the email template editor, which automatically generates a QR code for that URL.

### Integration Enhancements

- Integration with QuickBooks Online is now available, allowing QuickBooks Online users to route customer, invoice, and payment data PayFabric.

### API Updates

- Payment Transactions POST API now includes an optional parameter to specify an Additional Payment Profile.
- Invoice Types GET API added a new parameter to determine whether invoices of that type can be paid alongside others.
- Invoice Table Display PATCH API added a new parameter to control whether the Invoice Type column appears on the Pay Invoices page.
- A new Payment Transactions GET API is available to retrieve all Payment Transaction Settings, including Tender Type settings and Additional Payment Profiles.
- A new Text Notification Templates GET API is available to retrieve text notification templates.
- A new Text Notification Templates POST API is available to configure text notification templates.
- The Payment/Request POST API now supports additional parameters related to supporting text notifications and allowing partial payments when generating payment links.
- The Customer GET API and POST API added a Phone field as new data to store the customer’s phone number.
- The Payment Method Request and AutoPay Request POST API added additional parameters to send requests by a phone number.

### General Updates

- Additional security enhancements and system improvements are available .

## 10/14/2025

### User Management Enhancements

- New pages are available for managing Organization Users and configuring User Permission Roles on PayFabric from the New View.
- New Standard User Permission Roles are available to all Organizations for an improved experience in setting up new users. The Standard User Roles will automatically be updated with new functionality to be released in the future. The following Standard User Permission Roles are available:
  - All Access - Full access to all features and functionality within the Organization
  - Administrator - Administrative access to adjust settings and configurations
  - Processor - Ability to take action within the Organization such as processing transactions
  - Reader - Access to view general PayFabric pages
- Previously created User Permission Roles are still available and will be referred to as Custom User Permission Roles in the new user interface.

### Hosted Page Updates

- The Mobile Ready Hosted Payment Page and the Mobile Ready Hosted Wallet Page now support being translated into French.
  - A new URL parameter can be provided to enable an integrator to translate the Hosted Page to match the surrounding application.
  - A new Language Detection setting is available to allow the Hosted Page to be translated based on the configured language of the browser.
- A new Single Error Message option is available in the Device Theme settings for customer facing applications where it may not be desired to display the actual transaction processing error message to the user. This Single Error Message also supports being translated when used on the Mobile Ready Hosted Payment Page.

### General Updates

- Additional security enhancements and system improvements are available.

## 4/2/2025

### User Experience Enhancements

- The PayFabric Receivables design style has been enhanced to provide an improved user experience. All PayFabric Receivables pages have been updated to utilize this new design style.
- Many report pages have been updated with an improved experience for users to access their data. The filtering and sorting capabilities have been redesigned with a more intuitive experience by accessing a menu from the column headers. The following report pages have been updated:
  - Customers
  - Invoices
  - Subscriptions
  - Payments
  - Emails
  - Incoming Data
  - Outgoing Data
- The Customers, Invoices, Subscriptions and Payments report pages now support saving column filters and sorting preferences to a Saved View. Saved Views can be easily accessed from the menu to allow for quick access to data for future use.
- A new user experience is available in PayFabric that consolidates the different PayFabric menus into a single experience. An option to utilize the New View is available from the top banner.
- As an option for users that prefer the original PayFabric view, a Classic View option is available to return users to the original PayFabric view. This option is temporarily available while the New View is being updated to enhance the PayFabric user experience.

### Integration Enhancements

- Integration between PayFabric and BigCommerce is now available. BigCommerce users can configure PayFabric to route their BigCommerce transactions through PayFabric for payment processing.

### Customer Portal Enhancements

- The PayFabric Customer Portal design style has been enhanced to provide an improved user experience. All PayFabric Customer Portal pages have been updated to utilize this new design style.
- The Pay Invoices and History pages have been updated with an improved experience for users to access their data. The filtering and sorting capabilities have been redesigned with a more intuitive experience by accessing a menu from the column headers.
- The base URL of the PayFabric Customer Portal can now be updated by an organization user. Users changing this URL should take caution as all existing connections to the previous URL will no longer be accessible.

## 1/29/2025

### Integration Enhancements

- The SAP Digital Payments integration now supports surcharging capabilities.

## 11/21/2024

### Integration Enhancements

- Automated data synchronization between PayFabric and Sage Intacct is now available. Sage Intacct users can now configure their PayFabric organization to automatically synchronize Customers, Invoices and Payments from Sage Intacct with PayFabric.

## 10/23/2024

**ADDED.** PayFabric authentication is being updated to require multi-factor authentication for all users. All users will need to validate their email address and configure multi-factor authentication after this release.

**UPDATED.** Change the invocation method with Nodus Framework assemble.

**UPDATED.** Change SMS provider.

**UPDATED.** Security Enhancements.

## 8/13/2024

### Customer Enhancements

- A new configuration option is available to allow for the email address associated with a customer’s outstanding invoices to be automatically updated alongside updates to the customer’s email address.

### Invoice Enhancements

- A new Invoiced To parameter is available from the API to associate another customer with an invoice. This new value will appear on the Pay Invoices page when the associated customer has invoices assigned to different customers.

### Email Enhancements

- A new Integration Status email notification is available to be sent to internal users to inform them of updates relating to the integration of records with another system.

### API Enhancements

- New Reporting API Endpoints are available to retrieve data in bulk for Customers, Invoices, Subscriptions, Payments and Emails.
- The Customer POST and PATCH APIs have a new parameter to control if updates to the email address should carry to the customer’s outstanding invoices.
- Invoice APIs have been updated to support the new Invoiced Customer feature.
- A Customer PATCH API is available for enabling updates to the customer ID.
- An update to the Customer DELETE API is available to allow for full deletion of a customer record and all data associated with the customer.
- New settings GET APIs are available for retrieving saved data relating to configured Email Templates and Invoice Types.

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

- New configuration options are available to easily adjust the colors of the customer portal.
- New configuration options are available to easily adjust the size and alignment of the company logo displayed at the top of the customer portal.
- A new customer summary page is available for a quick overview of the customer account, this new page acts as the default landing page for the customer portal when a user logs in.
- The customer Wallet page has been completely redesigned to provide a more user-friendly view of the saved payment methods in the customer’s wallet.
- If a customer user is locked out of the customer portal due to failed password attempts, a new option is available to unlock the customer user account immediately.

### Payment Enhancements

- After accessing the customer portal using a secure link and completing a payment, an option to create an account for the customer portal can now be presented to the user.
- Payment Status will now be displayed as an additional column on the Payment report page.

### Email Enhancements

- Invoice Reminder email templates with the option to be sent manually configured have been migrated to be labeled as Payment Request · Single Invoice email templates. This change was made to help distinguish Invoice Reminder email templates as emails sent on an automatic scheduled basis and Payment Requests as emails sent on an on-demand basis.
- A new Invoice Reminder · Multiple Invoice email is available to be sent to notify customers of multiple outstanding invoices in a single notification. This email can contain a single payment link to allow the recipient to pay multiple invoices on their account at once.
- A new Payment Method Request email is available to be sent to request for a customer to provide their payment details without having to complete a payment.
  - A new user permission is available to control if a user is able to send this email. Integration records created through this mechanism.
  - Completed Payment Methods Request can be included as integration records in the Integration report.
- A new AutoPay Request email is available to be sent to request for a customer to activate AutoPay on their account without requiring the recipient to register for the customer portal.
  - A new user permission is available to control if a user is able to send this email.
- A new Payment Request · Prepayment email is available to be sent to request for a customer to make a payment that is not associated with any invoices.
- A new AutoPay Activated email is available to notify customers when AutoPay has been activated on their account.
- A new AutoPay Updated email is available to notify customers when their AutoPay terms have been updated on their account.
- A new AutoPay Deactivated email is available to notify customers when AutoPay has been deactivated on their account.
- A new AutoPay Upcoming Notification email is available to notify customers a few days before their automatic payment is planned to run.
- New PrepaymentAmount and PaymentTotal variables are available on the Payment Request email templates for both single and multiple invoices to allow for these emails to support communicating a prepayment amount included with the Payment Request to the recipient.

### API Enhancements

- A new Company/Style PATCH API is available for adjusting the new settings relating to the company colors and logo.
- A new PaymentMethod/Request POST API is available for generating a Payment Method Request link and sending out the Payment Method Request Email.
- A new AutoPay/Request POST API is available for generating an AutoPay Request link and sending out the AutoPay Request Email.
- The Invoice GET API now returns the Invoice Status.
- The Settings/Payment/Preferences PATCH API has a new The CreateAccountAfterLink parameter to support the new related setting.
- The Settings/Integration PATCH API has a new PaymentMethodIntegration parameter to support the new related setting.
- The Payment/Request POST API supports additional parameters related to supporting prepayments and the Authorization transaction type.
- New updates are available for Pass-through Authentication such as an internal permission role, the ability to hide the menu and additional landing pages for the customer Summary and User pages.

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

- PayFabric Partners can now personalize the PayFabric Receivables experience by controlling which functionalities are displayed to users.
- PayFabric Partners can now preconfigure default values for settings for faster initial deployment for new users.

### Invoice Enhancements

- A frequency interval is now available for Subscriptions to define a number of days or number of months between cycles.
- A Payment Request can now be sent from the Invoice Editor before the Invoice is completed.
- A new option to pay multiple invoices at the same time is available from the Invoice Report.

### Payment Enhancements

- A frequency interval is now available for AutoPay Templates to define a number of days or number of months between cycles.
- A starting day of the week configuration option is available to specify the day of the week for AutoPay to start.
- A new option is available from the Payment Report to send Payment Requests for multiple invoices.

### Email Enhancements

- New Payment Request email templates are available for requesting for payment from customers.

### API Enhancements

- New APIs are available to configure all the PayFabric Receivables settings.
- The FrequencyInterval parameter is now available for the AutoPay and Subscription APIs.
- A new Payment/Request POST API is available to trigger the generation of a Payment Request link and send the Payment Request email.
- Invoice APIs now support the Status parameter to allow for the Invoice status to be updated by integrating applications

## 1/17/2023

**ADDED.** Settlement and Reconciliation Report - Provides merchants and integration partners the ability to query settled transaction data and details via PayFabric API and directly from the PayFabric merchant portal. These reports will help merchants further with performing transaction reconciliation needs.

## 8/16/2022

### Customer Enhancements

- Customers can now be marked as tax exempt and a tax exempt number can be assigned to the customer.
- The data on the Customer Report can now be exported to an Excel spreadsheet.

### Invoice Enhancements

- The data on the Invoice Report can now be exported to an Excel spreadsheet.
- Taxes can now be configured for automatic tax calculation on invoices.
- Items can now be marked as tax exempt.
- Subscription invoice plans can now be created to automatically have invoices generated on a scheduled basis.
- A payment method can be assigned to a subscription plan to allow for automatic payments to be processed when the subscription invoice is generated.

### Payment Enhancements

- New payment methods of Google Pay, PayPal and Apple Pay are now supported for customer payments.
- A payment can now be initiated from the Invoice Report by clicking an applicable invoice record
- A payment can now be initiated from the Payment Report.
- The data on the Payment Report can now be exported to an Excel spreadsheet.
- Payments can now be processed directly on new invoices from PayFabric Receivables.
- A transaction associated to a payment record can now be reversed.

### Data Import Enhancements

- The user experience for selecting a template and downloading sample templates has been enhanced.
- Subscription & Tax data types are now available for import.
- Commonly associated data types are now paired to be selected together such as Invoices with Invoice Items and Payments with Payment Applications.

### Email Enhancements

- New versions of the New Invoice Notification email templates are available for invoices that have been paid and partially paid before they are completed and made available to customers.
- A new email template is available to be automatically sent when a payment associated to a scheduled subscription invoice fails to be approved.

### API Enhancements

- New GET and POST APIs are available for Taxes and Subscriptions
- Customer & Invoice APIs have been updated to support additional tax related parameters.

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

- Default payment terms can now be assigned to customer records

### Invoice Enhancements

- When creating an invoice, payment terms have been enhanced to automatically calculate the Invoice Due Date and provide discount options.
- A new option is available to add an approval step before an invoice is completed and sent to customers.

### Payment Enhancements

- Available Payment Terms Discounts will not automatically be applied to payments when applicable
- A customer's available credit balance can now be applied during a payment. During the payment process, a user can select which available credits should be applied to invoices.
- A new e-mail template is available when only a credit is applied during a payment without a new transaction.
- A customer's available credit balance can now be configured automatically be applied during recurring payments
- When a user attempts to leave a payment, they will now be prompted if they want to leave the payment screen.
- Companies processing transactions with EVO Payments can now add a processing surcharge to credit card transactions processed on PayFabric Receivables. With surcharging enabled, an additional amount will automatically be added to the payment if the user is paying by credit card. Before enabling credit card surcharging, please make sure to consider the surcharging rules and regulations to determine if credit card surcharging is a good fit for your business.
- For internal users, a new option to simply record an already accepted payment without processing is now available.
- The payment receipt page has been updated with a new style. Also, download and e-mail forwarding options are now available directly on the payment receipt.
- The historical payment details page has also been updated with a new style
- The Notes field can now be included on the Payment confirmation receipt.

### Integration Enhancements

- New record types are now available to be integrated with other systems. New Customer, Invoice, Application and Surcharges are all available to be integrated from the API.
- A new integration details page showing more information about the history of the integration record is now available.
- The exported report on the integration page has now been enhanced to include the additional record types and more detail for integrated payments.

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

- A new dashboard page is available when accessing PayFabric Receivables. This page will display a high level overview of the company's Receivables status.

### Customer Enhancements

- A new Customer Editor interface is now available to create & edit customer records and customer address information.
- The Customer Report page has received the following updates:
  - A button has been added create a new customer record.
  - Clicking a customer record will now display an Edit option to modify the customer record.
  - New Columns have been added to show if the customer is subscribed to AutoPay and the registered users of the Customer Portal
- A new Customer Management Settings page is available to control access to the Customer Editor for all users and additional settings related to the customer editor.
- Create and Edit Customer user permissions are now available to control which users can Create or Edit customer records.

### Invoice Enhancements

- A new Invoice Editor interface is available to create invoice records with item detail.
- A new Invoice Management Settings page is available to control access to the Invoice Editor for all users and additional settings related to the Invoice Editor.
- A Create Invoice user permission is now available to control which users can create invoice records.
- The Invoice Report has received the following updates
  - A button has been added to allow for creating a new invoice record
  - New columns for Status and E-mail have been added
  - The default filter on the page is now based on the status column
  - The customer ID column can now be clicked and functions the same as clicking a customer record on the Customer Report
  - Clicking an Invoice ID now presents a menu with available options for working with the invoice.
- Invoice Types are now available to classify invoices into groups
  - A new Invoice Types settings page is available for creating and editing Invoice Types.
  - The New Invoice Notification E-mail can now be restricted to only be sent for certain Invoice Types
  - Automated Invoice Reminder E-mails can now be restricted to only be sent for certain Invoice Types
  - AutoPay Templates can be configured to only pay invoices of certain Invoice Types
- Multiple Invoice Templates can now be created to be assigned to different Invoice Types.
- New variables for Item Markdown and Item Comment are now available for the Invoice Template
- Each Invoice can now be assigned primary e-mail and copy e-mail addresses to control the recipients of the e-mail notifications regarding an individual invoice.
- A New Item Editor interface is available to create items to be used on invoices.

### Data Import

- Items can now be created in bulk with the new Item import option
- Customers can now be registered for AutoPay in bulk with the new AutoPay import option
- Email and Copy Email fields are now available when importing Invoices.
- An Item Comment field is now available when importing Invoice Items.

### API

- All Invoice APIs have been updated to include the Email, CopyEmail and Item Comment parameters
- Item GET and POST APIs are now available for retrieving and pushing item detail to PayFabric Receivables.
- All AutoPay APIs have been updated to include the Invoice Type parameter
- Customer POST API will now update the Name value with the CustomerID if the Name is blank or null

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

- The experience of accessing customer data has been improved to focus on easier transition between managing customer accounts.  
- The settings have been reorganized for easier navigation.  

### Customer Portal User Management

- Customer portal users can now be invited to sign up for the customer portal  
- Multiple users can now be created for a single customer account  
- Password reset requests can now be initiated from within the portal  
- Customer Portal Users can be uploaded in bulk using the Data Import utility.  

### User Permissions

- Access permissions are now available to assign internal users have access to PayFabric Receivables functionality.  
- Permission groups are also available to be assigned to users of the customer portal  

### Invoice PDF Files

- A PDF file can now downloaded when viewing an invoice  
- A PDF file can now be uploaded using the Receivables API to be presented instead of the generated invoice template.  

### New Transaction Fields

- Additional fields Customer Tax Exempt Number, Customer Company Name, and Item Commodity Code are available from the PayFabric Receivables API to be sent during payment processing  

### Pass-Through Authentication Enhancements

- Additional parameters are available for Pass-Through Authentication to create a more seamless experience for users being passed into the PayFabric Receivables customer portal from another application.  

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

- The e-mail template setup process has been completely redesigned to improve the e-mail template setup experience for users.
- All of the default e-mail templates have a new updated design that is optimized for display on mobile devices.
  - Customers with existing configured e-mail templates can utilize the new templates by clicking the reset button in the e-mail template editor.
- New variables are available for the large company logo, small company logo and company e-mail.

### Invoice Reminder

- A new e-mail type is available to allow for a reminder e-mail to be sent for outstanding invoices.
- This e-mail can be manually sent from the Invoice report page to one or multiple recipients.
- This e-mail can also be scheduled to be automatically sent based on the age of the invoice. Reminders can be scheduled before, on or after the invoice due date and each reminder can be configured to have different messaging.

### PDF File Attachments

- On e-mail templates such as the New Invoice Notification and the Invoice Reminder, an option is available to automatically attach a PDF version of the invoice to the e-mail.

### E-mail Report

- A new page is available to show all e-mails sent out from PayFabric Receivables. Users can view the details of each individual e-mail and also resend previously sent e-mails.

### Pass-Through Authentication Improvements

- A new configuration option is available for pass-through authentication. The new Originating Portal URL option will redirect any users who reach the Customer Portal login page to another webpage such as the login page for the integrating application.

### Data Import Updates

- A sample of the expected spreadsheet file with headers can be downloaded for any Data Import template.
- Data import templates can now be deleted

### Delete Invoices

- Invoices can now be deleted from the invoice report page individually and in bulk.

### Functional Currency Setup Option

- A new setting is available to allow the functional currency to be changed for the organization.

### API Help

- A new API help page is now available to make it easier for developers to work with the Receivables API by providing interactive tests and sample data. [https://sandbox.payfabric.com/receivables/apihelp](https://sandbox.payfabric.com/receivables/apihelp)

## 5/11/2020

**UPDATED.** Enhance Level 2 and Level 3 Support with the following changes:

- Update User Interface to improve user experience for Level 2/3 Field Defaults on Modern design.
- Update Form Settings for Virtual Terminal’s Web Entry to provide merchant flexibility on field display options during transaction processing.
- Added BIN Range Validation option for Level 2 and 3 Support.
- Providing portal virtual terminal users the ability to lookup line item data (Level 3) using uploaded products/items during transaction processing.
- Add ability to upload products/items to be used during transaction processing on Virtual Terminal.

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

- Customer's can now be registered for automatic recurring payments. Multiple frequency and payment amount options are available.

### AutoPay Templates

- The organization can specify the settings for how automatic payments should be processed based on the business preferences. Multiple templates can be created to provide different AutoPay options to customers.

### AutoPay E-mail Templates

- New e-mail templates are available to be sent to customers when an AutoPay payment is approved or fails to be processed.
