# PayFabric Receivables  

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
