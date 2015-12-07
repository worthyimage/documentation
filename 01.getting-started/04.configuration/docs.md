---
title: Configuration
---

During the installation process, Membership Pro will generate default configuration data. However, you should still review all config options and change it to meet your own requirement if needed.

To review and change Configuration, go to Membership Pro => Configuration. When you do that, the screen below will be displayed:

![Configuration](configuration.png)

>>>>> To see the meaning of a config option / parameter, you can hover the moose over the name / title of that config option

As most of the config options are very easy to understand, in the section below, we will just explain / review the most importants config options. If there are other options which are not mentioned here and you don't understand, feel free contact us for support. We are available to assist you whenever you want / you need.

## General

### Subscription Settings
1. **Registration Integration**: If set to Yes, when subscribers sign up for a subscription plan on your site, the system will allow them to enter username and password on to register for an account on your Joomla site. In most case, subscribers will need to have an account on your website so that they can login later to access to restricted resources, update their profile, renew membership, upgrade membership..., therefore **you should set this config option to Yes** unless you only use Membership Pro to simply get payment from your subscribers.
2. **Only create user account when membership active/approved**: By default, Membership Pro will create an acccount for subscriber right after they complete entering information on subscription form (before the payment is processed). If for some reasons, the payment is failed or the subscriber abandon the payment, the account will remain blocked and he could not use that account again if he decides to sign up again in the future. If you set this config option to **Yes**, Membership Pro will only create the Joomla account for subscribers when their subscription become active (after completing payment for the subscription or admin approves the subscription), it will solve the issue mentioned above. Based on my experience, I would suggest to set this config option to **Yes**.
3. **Send activation email**: If you require users to receive a confirmation email and click on activation link to activate their account (to make sure the email he entered on subscription form is a valid / existing email), please set this config option to **Yes**. Otherwise, if you want their accounts to be activated automatically by Membership Pro after subscribers complete payment for the subscription, set this config option to **No**
4. **Auto Login**: If set to Yes, subscribers will be logged in automatically by the system after they completed payment for the subscription. By doing that, subscribers can start access to restricted resources without having to performing login.
5. **Auto reload user groups**: If set to **Yes**, after subscribers complete payment for the subscription, his access levels will be updated automatically and he can start accessing to restricted resources without having to login and re-login. This is useful if you config Membership Pro to assign subscribers to certain Joomla groups when they sign up for your subscription plans
6. **Show login box on subscription page**: If set to Yes, on subscription form page, Membership Pro will display login box so that existing customers can login before continuing the subscription process. If you have **Registration Integration** config option set to **Yes**, you should set this config option to **Yes**, to.
7. **Allow membership renewal X days before subscription expired**: By default, Membership Pro allows subscribers to renew their subscription any time they want (even right after they just subscribe for the plan). If you only want your subscribers to renew their subscription **X days before the subscription expired**, enter the number of days into this config option. This will help preventing subscribers register for the same plan multiple times.
8. **Enable Captcha**: If you want to use Captcha on Membership Pro to prevent spam, you need to set this config option to Yes. As Membership Pro uses Joomla core captcha, beside setting this config option to Yes, you need to config Joomla core re-captcha plugin, too. Please see [https://docs.joomla.org/How_do_you_use_Recaptcha_in_Joomla%3F](https://docs.joomla.org/How_do_you_use_Recaptcha_in_Joomla%3F) for instructions.
9. **Enable Coupon**: If you setup coupons in Membership Pro and want to allow subscribers to enter coupon code on subscription form to get discount for their subscription, please set this config option to **Yes**.

### Theme Settings
1. **Load jQuery javascript library**: Membership Pro requires JQuery library to work. So please **only set this config option to No** if you are using a template **which load JQuery already**.
2. **Load twitter bootstrap css in the front-end**: The extension uses twitter bootstrap for front-end layouts. If you want to use your site template css (instead of twitter bootstrap) for Membership Pro, set it to No.
3. **Twitter bootstrap version**: Membership Pro supports twitter bootstrap both version 2 and version 3. However, please only set this config option to **Twitter Bootstrap version 3** if your site template is built based on twitter boostrap 3 and has twitter bootstrap version 3 loaded already. Otherwise, please just set this config option to **Twitter Bootstrap version 2**
4. **Show price including tax**: By default, Membership Pro display subscription plans price without tax. If you want to display price including tax (which is required by law in some country), set this config option to **Yes**.
5. **Date Format**: Enter the date format you want. It will be used to format the date displaying in the system. For list of supported parameter, please see [http://php.net/manual/en/function.date.php](http://php.net/manual/en/function.date.php) for list of supported parameters. 
6. **Date Custom Field Format**: Membership Pro allows you to create custom fields to collect more information of subscribers on subscription form. If you use **Date custom field**, you should change this config option to have the format you want.
7. **Currency Symbol**: It is $ by default. If you use different currency, you can change the currency here to meet your own currency. Please note that from version 2.1.0, each subscription plan can have it own currency and currency symbol.

### Mail Settings
1. **From Name**: The sender name uses to send emails in the system (to admin and subscribers). If you leave it empty, the **From Name** which is setup in Global Configuration of your site will be used.
2. **From Email**: The sender email uses to send emails in the system (to admin and subscribers). If you leave it empty, the **From email** which is setup in Global Configuration of your site will be used. 
3. **Notification emails**: The emails you want to receive notification when someone subscribes for a subscription plan on your site. If you want to user multiple emails, separate these emails by comman. For example: paypal@joomdonation.com,acounting@joomdonation.com
4. **Disable Admin Notification**: Sometime, you don't want to receive notification emails when someone signs up for your plan (likely when you only offer free subscription plans in your system). In that case, set this config option to **Yes** (it is **No** by default)

### Other Settings
1. **EU VAT Number field**: If you are from one of EU countries, you will need to setup a custom field in Membership Pro to allow subscribers to enter their VAT Number. In that case, please select that custom field which you created for this config option.
2. **Term and condition article**: If you need your subscribers to accept your terms and conditions to sign up for subscription plan, please create a temrs and conditions article, then select that article in the config option. When you select an article, the system will display a checkbox (has link to the selected article) and subscribers will have to check on that checkbox to agree on terms and conditions to complete the subscription. 

## Invoice Settings
1. **Activate Invoice Feature**: If you have paid subscription plans and want to send invoice PDF to your customers after they sign up and complete payment for the subscription, please set this config option to Yes.
2. **Send invoice to subscribers**: Set this config option to Yes if you want the system to send PDF invoice to subscribers in the confirmation email they received after signing up for your subscription plan. If you set to No, subscribers will have to access to their membership profile to download the invoice. This config option should be set to Yes if you use invoice feature.
3. **Send copy of invoice to administrators**: If you want to receive a copy of the PDF invoice send to subscriber (for managing purpose), you can set this config option to Yes
4. **Invoice Start Number**: If you want the invoice number in the system to start with a certain number (instead of starting by 1), you can enter that number into this config option.
5. **Invoice Format**: Membership Pro generates default basic invoice format when you first install the extension. You should review and change the invoice format to meet your need (at least you will have to change invoice logo)
