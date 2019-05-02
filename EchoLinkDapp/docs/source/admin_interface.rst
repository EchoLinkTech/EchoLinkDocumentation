Admin Interface
===============

This app is responsible to handle the sidechain and mainnet transaction events for lock/unlock stake requests and verify/decline credentials by Admin.

Steps to use Admin Panel
-------------------------

Only Admin can use the application by login through credentials.
Three tabs would be visible to a user

* Lock Requests
* Authority Users
* Verify Credentials

Lock Requests
-------------

This is dashboard page, here you will see list of all user who want to be authority on ekochain. admin can perform multiple functionality on same page. Functionalty like lock stack on mainnet, lock stack on eko chain, unlock stack on sidechain, block stack on ekochain, unlock stack on mainnet and unlock stack on ekochain all can perform here preceded by admin mnemonic input. Here is following staps to perform lock/unlock stack on mainnet and ekochian.

This is a four step process:

- Lock on mainnet
- Lock on sidechain
- Unlock/block on sidechain
- Unlock/block on mainnet


Admin can see a list of Authority requests with User address, amount, status and action

1. Status Aproved

At the beginning the default status would be approved and you would see lock on mainnet button in action column. To lock the stakes on mainnet, click on the button on the action field. A modal will appear to enter the mnemonic key corresponding to the associated account with the contract. Input correct mnemonic key and click ok, after validating mnemonic key transaction for mainnet will take place and your status will be ‘pending lock on mainnet’, and action column will be blank. Status will be remain ‘pending lock on mainnet’ until the transaction get mined on mainnet and watch by admin backend service. You will get updated status (locked on mainnet) by refreshing the page.

2) Locked on mainnet

Here status will be Locked on mainnet and you would see lock on ekochain button in action column. To lock the stakes on ekochain, click on the button on the action field. A modal will appear to enter the mnemonic key corresponding to the associated account with the contract. Input correct mnemonic key and click ok, after validating mnemonic key transaction for ekochain will take place and your status will be ‘pending lock on ekochain, and action column will be blank. Status will be remain ‘pending lock on ekochain until the transaction get mined on ekochain and watch by admin backend service. You will get updated status (locked on ekochain) by refreshing the page. After locking stack on ekochain, ther user will become validator/miner on ekochain.

3) Locked on ekochain

Here status will be Locked on ekochain and you would see two button unlock on ekochain and block on ekochain button in action column. To unlock/block the stakes on ekochain, click one of the button on the action field. A modal will appear to enter the mnemonic key corresponding to the associated account with the contract. Input correct mnemonic key and click ok, after validating mnemonic key transaction for ekochain will take place

3a) If you had clicked on unlock on ekochain then your status will be ‘pending unlock on ekochain, and action column will be blank. Status will be remain ‘pending unlock on ekochain until the transaction get mined on ekochain and watch by admin backend service. You will get updated status (unlocked on ekochain) by refreshing the page.
3b) If you had clicked on block on ekochain then your status will be ‘pending block on ekochain, and action column will be blank. Status will be remain ‘pending block on ekochain until the transaction get mined on ekochain and watch by admin backend service. You will get updated status (blocked on ekochain) by refreshing the page.


4)  Unlocked on ekochain
Here status will be  Unlocked on ekochain and you would see unlock on mainnet button in action column. To unlock the stakes on mainnet, click on the button on the action field. A modal will appear to enter the mnemonic key corresponding to the associated account with the contract. Input correct mnemonic key and click ok, after validating mnemonic key transaction for mainnet will take place and your status will be pending unlock on mainnet, and action column will be blank. Status will be remain pending unlock on mainnet until the transaction get mined on mainnet and watch by admin backend service. You will get updated status (unlocked on mainnet) by refreshing the page. After unlocking stack on mainnet, the user record no more will be seen on the list.

5)  blocked on ekochain
Here status will be  blocked on ekochain and you would see block on mainnet button in action column. To block the stakes on mainnet, click on the button on the action field. A modal will appear to enter the mnemonic key corresponding to the associated account with the contract. Input correct mnemonic key and click ok, after validating mnemonic key transaction for mainnet will take place and your status will be pending block on mainnet, and action column will be blank. Status will be remain pending block on mainnet until the transaction get mined on mainnet and watch by admin backend service. You will get updated status (blocked on mainnet) by refreshing the page. After blocking stack on mainnet, the user record no more will be seen on the list.

    **Note: The mnemonic key will be saved for the particular session so that it can be used again.**

Authority Users
---------------

Validator/ Miner (i.e User with status locked on ekochain) will be listed here.

Verify Credentials
------------------

Credential Data is being fetched by user from the "EkoCertificateVerificationExtension"
The extension will fetch the following data from an university's website:
- Username
- SSL_INFO
- web content
- Screenshot of page

Admin can see a list of credential data on the Verify Credentials page
Initially the status will be "pending" for all credentials. Admin can verify the data and take the action- "accept" or "decline” accordingly. On clicking accept, the admin will be redirected to mnemonic modal to add key. On successful transaction, the status will be updated as `accepted` followed by the entry in CredentialsStore contract for Issuer, Recipient, Status and ImageHash generated through IPFS of uploaded university's screenshot.
