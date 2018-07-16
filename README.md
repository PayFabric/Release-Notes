# Change Log – 07/15/2018 Release

**FIXED.** Allow zero [0] quantity submission from PayLink API - PayLink API will be able to support zero [0] quantity line items to cater for sales document with backordered quantity in accounting system. 

**ADDED.** Ability to process a PayFabric transaction without a Customer Number - Customer Number is now an optional field to process a transaction in PayFabric. However, Customer Number is still a required field for creating/saving new wallet entry.

**ADDED.** Enhancement to Daily Activity Report
* Added ‘-All-‘ filter option for payment method so user can search transaction result for all payment types: credit card, debit card and eCheck.
* Add more filter options and columns into Daily Activity Report.
New columns in report grid:
- Account #
- User ID
New search filter options:
- By amount range
- Search all payment types
- By transaction status
- By transaction key
- By customer number

**ADDED.** Enhancement to Transaction Summary Report - Add ‘-All-‘ filter option for payment method so user can search transaction result for all payment types: credit card, debit card and eCheck.

**ADDED.** Transaction processing security settings into user role - Provide the ability to break down and restrict transaction processing for PayFabric user by transaction and payment types.

**ADDED.** Provide easy navigation between device & theme pages. Provide user an easier navigation to switch from device and theme pages.

**ADDED.** Add new WalletLink GET APIs	GET /api/wallet/{WalletLinkID}: Query a WalletLink and its details.
GET api/wallet/?$: Query WalletLink(s) based on query string data.
Available Data to Query On:
* CustomerNumber: customer number specified at the time of creating a wallet link
* CreatedOn: date the wallet link was created on
* NotificationEmail: email specified at the time of creating a wallet link
* NotificationPhone: phone number specified at the time of creating a wallet link
* Status: 0=incomplete, 1=complete, 2=cancelled
* Device: device used at the time of creating a wallet link
* CompletedOn: the date the wallet link was completed on

**ADDED.** Enhancement to WalletLink CREATE API - Enhance existing WalletLink Create API by include the actual link into the response so 3rd party integrator does not need to compile and put the link together. 

**ADDED.** Enhancement to Wallet Report functionalities - Combine Wallet and Expired Card reports into a single report with the following:
+ Provide the user the ability to filter expired card with a given date range for expiration date
+ Ability to delete expired cards from filter search.
+ These columns on wallet report should be sortable: Customer #
+ These columns on wallet report should be searchable: last 4-digits of card #, first name, last name, card type, expiration date. The search performed on each text input field for the column should be a partial match instead of exact match. 
+ Allow the report to be exported in the following formats: excel, tsv, csv.

**ADDED.** Ezidebit Gateway - Added support for new gateway [Ezidebit] for direct debit in Australia.

**FIXED.** Exported Document Queue list has different date compared to the one from PayLink portal. Fixed the issue so the date on the exported document is the same as the one from PayLink portal > paylink’s created date.

**ADDED.** PayFabric’s email receipt templates share the subject line and BCC email field value. Fixed the issue so the email receipt templates do not share the subject line and BCC email field value.

**FIXED.** Unable to edit Account Number for credit card on PF hosted pages.	Fixed the issue to allow user to edit and change the digit(s) of the credit card number correctly. 

# Change Log – Hotfix 06/06/2018 Release
**ADDED.** Add Enable Security Token configurable setting on PayFabric portal to enable restriction on usage against PayFabric APIs. The PayFabric hotfix release includes a security enhancement to PayFabric to allow 3rd party application(s) integrating to PayFabric to set the restriction on the use of security token against the PayFabric APIs. 
PayFabric will provide the ability to restrict the security token to be used in hosted page ONLY instead of not both API & Hosted page. The changes are as followed:
PayFabric will provide a new security setting called 'Enable Security Token' on PayFabric Settings with dropdown values below.
* For APIs and Hosted Pages: this is the default option where security token will be allow to use as the authentication method in both hosted pages and APIs.
* For Hosted Pages Only: with this option, security token will ONLY be allow to use as the authentication method in hosted pages. The API service response will fail authentication if any API calls was authenticated using security token. 

This setting is device specific. By default, to maintain backward compatibility & to avoid any impacts to existing implementation, the default option will be 'For APIs and Hosted Pages'. 

3rd party application can change this to 'For Hosted Pages Only’ if their application supports the ability to call PayFabric APIs via Device ID & Password.
  
NOTE: This change is applied to PayFabric version 2.0 as well. 

**ADDED.** Add ability to authenticate with device id and device password for PayLink APIs.	Due to the security enhancement [#1] from PayFabric, PayLink now has the ability to get authenticated using device ID and password instead of using security token. 

# Change Log – 05/07/2018 Release
**ADDED.** Add Last UsedDate field into Wallet Report - Added LastUsedDate to help determine when the wallet record was last used for processing on PayFabric. 

**ADDED.** Forte Gateway - Added support for US & Canadian Credit Card for all PF transaction types.

**ADDED.** Ability to over-capture on PayFabric Virtual Terminal - Utilize the same existing ‘Partial Shipping’ setting on PayFabric portal, if enabled, it will also allow users to ship more than the authorization/book amount.

**ADDED.** EVO Gateway - Added support for new gateway [EVO] for US & Canadian Credit Card for all PF transaction types.
 
**UPDATED.** Update Connection URLs for Paymentech Orbital Gateway - Modified Connection URLs for Orbital:

- Current Test: orbitalvar1.paymentech.net 
- Current Live: orbital1.paymentech.net

- New Test: orbitalvar1.chasepaymentech.com 
- New Live: orbital1.chasepaymentech.com 

**ADDED.** Allow Edit Billing Information for Automatic billing - PayFabric now allows merchant to change billing information if originally signed up for Automatic billing. 

**FIXED.** Check for duplicated card if saving wallet via API. Ensure duplicated card is checked even when saving new credit card records via API. 

**FIXED.** Unable to update transaction if associated wallet record is deleted - Address the issue where transaction record cannot be updated if the associated wallet record had already been deleted. 

**ADDED.** Add ability to paste card number into hosted wallet/payment page - User is now able to paste card number into hosted wallet/payment page for the ease of data entry. 

# Change Log – 01/08/2018 Release
**ADDED.** Support PayLink Service - Offer PayLink service to new and existing PayFabric [v3] customers.

**Production:**
API URL: https://www.payfabric.com/paylink/api 
Hosted Page URL: https://www.payfabric.com/paylink/web 
Help: https://www.payfabric.com/paylink/help

**Sandbox:**
API URL: https://sandbox.payfabric.com/paylink/api 
Hosted Page URL: https://sandbox.payfabric.com/paylink/web 
Help: https://sandbox.payfabric.com/paylink/help

**ADDED.** Support PayLink integration with SalesPad API - Offer PayLink integration to back office SalesPad Desktop for all successful payments from PayLink. 

**ADDED.** Return of the URL in the Create a PayLink response. Support the inclusion of PayLink URL in the Create a PayLink response so 3rd party application does not need to reconstruct the PayLink URL using PayLink ID.

**ADDED.** Hosted DNS Server Support for EMV - PayFabric will offer hosted DNS server for EMV terminal support. This will make it simpler to auto-register a new IP address for the hardware device to associate with the SSL certificate. 

**ADDED.** Enable/Disable EMV from hosted page	Allow 3rd party application to enable/disable EMV on-the-fly on a per-transaction basis via the following query string parameter.
* ProcessingMethod=0: Web Entry only
* ProcessingMethod=1: EMV only
* ProcessingMethod=2: Both Web Entry and EMV

**UPDATED.** Changes to PayLink API	Status
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
