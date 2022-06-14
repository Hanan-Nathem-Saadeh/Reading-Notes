# Read: 34 - Payment Processing

## How to read Technical Documents as fast as possible
1. Establish why you are reading it.    
2. Get an overview of the content and structure of the document  
3. Take 30s to 2 minutes to scan the rest of the document. Click on the scrollbar and just breeze through all the pages. Just look at the pictures, tables and diagrams. Look for things that look familiar and that you will understand immediately. APIs, schematics, flow charts, block diagrams. Read the captions under the pictures.

4. If you want, stop at the interesting parts and take a deeper look. Stop when it gets boring.

5. Look at the table of contents again. You'll have a deeper understanding of the document after you look again.

6. Choose what to read next based on interesting-ness or usefulness. If there's nothing useful, close the doc. You can say that you've read it from cover to cover.

## How Does Online Credit Card Processing Work?  
- Merchant Accounts :  
It all starts with your bank checking account.  When you have that in place you will need a Merchant Account.  The Merchant Account is how you connect to the credit card processing network.  It is this account that makes sure credit cards are processed correctly and safely – your bank account does not process credit cards.  Merchant Accounts accept (or decline) credit cards and ultimately transfer the funds into your bank account.  It visually makes sense if you think of the Merchant Account as the old card-swipe machine.   
- Payment Gateway :  
The Payment Gateway is responsible for sending the credit card to the appropriate Internet Merchant Account over secure online channels.  The approval or decline of the transaction, however, is actually performed by the Merchant Account.  It is helpful to think of the Gateway as a router that sends the credit card information to the appropriate account.  It is also responsible for fraud checking and maintaining reliable links with the merchants.  
- Your Application :  
Your application can interact with the Payment Gateway in a number of different ways.  For simple applications, such as a shopping cart program, the user may simply be transferred to a web page on the Gateway for credit card processing.  When the transaction is complete, the user is transferred back to the application.  At no point does the application handle the credit card information.  
- Validation, Refunds, and Settlement :  
If the customer’s credit card is declined you will usually see a general message such as “there was a problem processing your credit card.”  For security reasons, the online user will usually not see the specific reasons for the failure, such as a decline. (The reason for this is that too much information makes it easier for hackers to fake credit card transactions.) However, the management side of the Gateway and third-party applications may allow you to find out more specific reasons for the failure.

If the card is cleared, the Gateway will return one or two order numbers that are used for future reference of the transaction.  These order numbers are used so that the credit card information does not need to be stored on the Gateway or third-party application.  A common use of the order number is for credit card refunds.  Refunding via a reference to transaction is much safer than refunding directly to the card. For example, you would not be able to refund more than the amount of the original transaction.

Once the card clears, the money will not appear immediately in your bank.  Settlement refers to the process of transferring funds from the buyer to your bank.  This process – managed by the Merchant Account – usually takes several business days.  Before Settlement occurs, you will usually have time to void the original transaction if there was a mistake.

- Fees!
