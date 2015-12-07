---
title: 'User - Membership plugin'
taxonomy:
    category:
        - docs
---

This plugin has two features:

1. Assgin user to a subscription plan (create an active subscription record for him) automatically when his account is being created (for example, when he register for an account via Joomla User Registration or Community Builder...)
2. Handle Login Redirect if you want subscribers of each plan to be redirected to a different page on Login (this is setup when you create subscription plan)

If you want to use these features, please follow the steps below:

1. Go to Extensions -> Plugins, find and publish the plugin **User - Membership plugin**
2. If you want the system to create a subscription for user automatically when his account is being created, please select a Subscription Plan in the **Select Plan** parameter
3. If you you setup Login Redirect URL for your subscription plans (subscribers of each plan will be redirected to a different URL on login), you need to set **Handle Login Redirect** to **Yes**

![User-Membership plugin](user-membership-plugin.png)