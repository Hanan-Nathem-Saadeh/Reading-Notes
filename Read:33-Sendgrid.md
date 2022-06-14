# Read: 33 - Sendgrid

 ## 1- Create an Azure Subscription
 - select the Subscriptions icon under the Azure services menu.  
 - A new page will load, listing your current subscriptions. You can add Twilio SendGrid to an existing Subscription or Select +Add to create a new subscription.  
 - If you already have an Azure account set up for billing, you will be taken to a page where you can create a subscription.  
 -  A form will load with a Subscription Name field. You must add a name — we recommend something that clearly differentiates the subscription. All the other fields are already populated and cannot be edited. Click Create.  
 -  Once the Subscription is created, you will see it listed on the Subscriptions page. If you do not see the Subscription, try refreshing the list.  
 
 ## 2- Create a Twilio SendGrid account
 - select Marketplace under Azure services. If you do not see the Marketplace icon, you can search for it by selecting More services.  
 - , including the Twilio SendGrid email service. You can find it by searching for "Twilio SendGrid." You will also find it under Software as a Service (SaaS).  
 - Click the Twilio SendGrid resource to load a page where you can select your account tier. You can start with a free account and upgrade as your sending needs change. See the Twilio SendGrid pricing page to understand what's included with each plan.  
 - Select Set up + subscribe. You will be taken to a page where you can assign your Twilio SendGrid account to an Azure Subscription and Resource Group. Once you have completed the required fields, select Review + subscribe.  
 - You will be asked to agree to Azure's term of services. You can now review your order and click Subscribe.  
 - It takes a few moments to establish your account. You will be shown a progress screen. When the setup is complete, you will be able to click the Configure account now button to be taken to the Twilio SendGrid App. You will also receive an email when the subscription setup is complete.   
 
 ## 3- Twilio SendGrid account setup
     - Configure Two-factor authentication
     - Create an API key
     - Complete Sender Authentication
     
       #### Two-factor authentication
       - Twilio SendGrid uses Two-factor authentication (2FA) to help protect your account. To enable 2FA, Navigate to Two-Factor Authentication in the Twilio SendGrid Settings menu, and click Add Two-Factor Authentication.  
       - A modal will open where you can complete the 2FA setup. Click Ok, Got it to continue.  
       - Twilio SendGrid supports 2FA using either SMS or the Authy App. Select your preferred 2FA method, and click Next.
       
       #### API Key
       - In the Twilio SendGrid App, navigate to API Keys in the Settings menu, and select Create API Key.
       - A modal will open where you can create your key. You must name the API key — we recommend something that will clearly differentiate the key from others you may create in the future.  
          ou must also select the type of key you want to create. Twilio SendGrid provides three types of API key:

              -   Full Access
              -   Restricted Access  
              -   Billing Access
