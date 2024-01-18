# AmazonInAppBilling Extension
An in-app-billing extension to monetize your app products using Amazon store billing library 3.0.3.

The In-App Purchasing (IAP) API allows your app to present, process, and fulfill purchases of digital content and subscriptions within your app. Amazon supports an IAP API for Android Apps.

![image](https://user-images.githubusercontent.com/75406851/197813008-513e7724-492a-4777-86c0-7da643b5e4e1.png)

# Configure Appstore SDK with your public key
This public key, which is unique per app, establishes a secure communication channel between the Amazon Appstore and your app. When you generate the public key from the Developer Console, Amazon generates a corresponding private key. These public and private keys form a key pair to sign license responses. Through this key pairing, you ensure that the users who install your app are authorized.

To configure your existing app with the public key:

1. Log into the [Developer Console](https://developer.amazon.com/) with your developer account.

2. Go to **Apps & Services > My Apps** . Then click your app. (If you don't already have an app, see [Log In and Add an App](https://developer.amazon.com/docs/app-submission/publish-app-login-and-add-app.html).)

3. Create a new version of your app. In the area below your app's name, click **Upcoming Version** .

:warning: **Important:** The link to the public key appears only when you create a new version or when you create a new app. 
If you had a new version in progress prior to the release of the Appstore SDK, 
you must complete your existing version and then create a new version. 
Only then does the public key link appear. 
(Alternatively, submit a [Contact Us Case](https://developer.amazon.com/support/contact-us) regarding your app and request that the Upcoming Version be cancelled.)

4. Go to the [App Information](https://developer.amazon.com/docs/app-submission/app-information.html) tab.

5. Click **Public Key** in the upper-right area.

6. In the Public Key dialog box that appears, click the **AppstoreAuthenticationKey.pem** link to download a PEM file. This file contains your public key.

![image](https://user-images.githubusercontent.com/75406851/197813099-0edd7004-4458-4c8a-9d1e-6fe5a065ce55.png)

7. Copy the **AppstoreAuthenticationKey.pem** file. Then paste it into the **assets** folder of your builder.

:information_source: **Note:** If you integrate your app with Login with Amazon (LwA) or Amazon Device Messaging (ADM), you need to add your app's API Keys. Appstore SDK integrated apps do not add API Keys automatically. You need to manage the API Key and see [LwA](https://developer.amazon.com/docs/login-with-amazon/register-android.html#add-android-settings) and [ADM](https://developer.amazon.com/docs/adm/obtain-credentials.html) documentation for more details. You can find your AppStore certificate hash values in the Developer Console to create the API keys for the existing apps. Go to **My apps** > select your app > **App Information** > **Appstore Certificate Hashes** .

# Verify License
Initiates a request to retrieve the license of the currently logged-in user. 
When the response is available `LicenseVerified` event will be called.

![image](https://user-images.githubusercontent.com/75406851/197815520-4a2cff03-f15c-4c41-aa42-5314727eb916.png)

# Get User Data
Initiates a request to retrieve the user ID of the currently logged-in user. 
`GotUserData` event will be called when a response is available.

![image](https://user-images.githubusercontent.com/75406851/197815557-5f66e8b2-e5ed-4eb2-939c-8e4f0bd37989.png)

# Get Purchases Updates
Initiates a request to retrieve updates about items the customer has purchased and/or canceled. 
`reset` - Set to true to get a list of all purchases. Set to false to get a list of all purchases made since the last invocation.
When a response is available `GotPurchaseUpdates` event will be called.

![image](https://user-images.githubusercontent.com/75406851/197815637-86c3c12b-5c0a-4936-aff6-07aa6251626b.png)

# Get Products Data
Initiates a request to retrieve item data of up to one-hundred SKUs.
`skuList` - List of SKUs. If the size of the list is greater than 100, an `IllegalArgumentException` is thrown.
When a response is available, `GotProductsData` event will be called.

![image](https://user-images.githubusercontent.com/75406851/197815713-024c9c4d-aa65-49ca-a740-c2315b387b7a.png)

# Launch Purchase Flow
Initiates a purchase-flow for a product.
`sku` - Vendor SKU for which to initiate a purchase.
When the purchase-flow completes `PurchaseSuccessful` event will be called.

![image](https://user-images.githubusercontent.com/75406851/197815747-74c8b0c7-1b78-41e9-8238-9d5336004d4b.png)

# Consume Purchase
Notifies Amazon about the purchase fulfillment. There is no callback for this API.
`receiptId` - Receipt id of the purchase.

![image](https://user-images.githubusercontent.com/75406851/197815798-252b7c46-462a-4220-ac66-6b533c1db165.png)

# Acknowledge Purchase
Notifies Amazon about the purchase fulfillment. There is no callback for this API.
`receiptId` - Receipt id of the purchase.

![image](https://user-images.githubusercontent.com/75406851/197815844-88eb5ac9-3b19-41cc-983a-615105f599be.png)

## Extension specifications:
<img src="https://github.com/jewelshkjony/UnityAds/raw/main/images/download.png"/> <a href="https://t.me/jewelshkjony/">com.jewel.amazoninappbilling.aix</a> (411 KB) \
<b>Price:</b> $12 USD\
<b>SDK Version:</b> 3.0.3\
<b>Extension Version:</b> 3.0.3.1\
<b>Last amendment:</b> 25 October 2022\
<b>Supported builder:</b> <a href="https://www.kodular.io/">Kodular</a>, <a href="https://niotron.com/">Niotron</a>, <a href="https://appzard.com/">AppZard</a>, <a href="https://androidbuilder.in/">AndroidBuilder</a>, <a href="http://ai2.appinventor.mit.edu/">App Inventor</a> and it's other distributions.

## 📫 How to reach me ↓

<a href="https://t.me/jewelshkjony" target="_blank">Telegram</a> | <a href="https://wa.me/8801775668913" target="_blank">WhatsApp</a> | <a href="https://fb.com/jewelshkjony" target="_blank">Facebook</a> | <a href="https://m.me/jewelshkjony" target="_blank">Messenger</a> | <a href="https://m.youtube.com/c/JewelShikderJony?sub_confirmation=1" target="_blank">Youtube</a>
