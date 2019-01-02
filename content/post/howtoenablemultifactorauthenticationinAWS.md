---
title: "How to enable (MFA) Multifactor Authentication in AWS"
date: 2019-01-02T15:37:19+05:30
draft: false
tags: ["aws","development"]
---

## What do you learn?

Just follow along to get quick & simple steps to enable MFA in ytour AWS account.

## What is MFA(Multifactor Authentication)?

>MFA is layered defense system that uses two or more independent credential to access to a system or service. The independent credentials being passwords, Security tokens, biometric validations etc.

## How do I setup MFA in my AWS root account?


**Assuming it's not already setup for your account.**

* Login to your AWS root account and on the console click on Services.

![alt text](/img/enablemfainaws/awsservices.jpg "AWS Services")

* Type in **IAM** in the Search bar & click on the first suggestion.You will be redirected to your **IAM Dashboard**

![alt text](/img/enablemfainaws/IAMdashboard.jpg "IAM Dashboard")

* Click on **Manage MFA** and click on **Continue to Security Credentials** .

![alt text](/img/enablemfainaws/continuetosecuritycredentials.jpg "Continue to Security Credentials")

* On the Your Credentials Screen click on **Activate MFA**, on the **Manage MFA device** popup select **Virtual MFA Device** and click on continue.

![alt text](/img/enablemfainaws/managemfadevice.jpg "Manage MFA Device")

* A step off the PC Screen. open your mobile and install the Google Authenticator App from Playstore. After the installation scan the QR Code from the screen. You will be given a numeric code in your app. Enter that code and wait for a while for the next code to appear and enter the same and click on **Assign MFA**.

![alt text](/img/enablemfainaws/authenticate.jpg "Authentication Code")


Wheee! You've successfully setup MFA for your AWS account.

