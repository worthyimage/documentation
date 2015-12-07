---
title: 'PHP Script Plugin'
taxonomy:
    category:
        - docs
---

If you want to **run PHP code** when a subscritpion record for a plan being created, become active (when payment complete) or become expired, you can use **OS Membership PHP Script** plugin

1. Go to Extensions => Plugins, find and publish the plugin **OS Membership PHP Script**
2. Now, when you add/edit a subscription plan, you will see a new tab called **PHP Script Settings**. You can enter the PHP code you want to run:
* After subscription record is stored in to the database. Enter that PHP code into **Subscription Stored Script** parameter
* After subscription record become active. Enter that PHP code into **Subscription Active Script** parameter
* After subscription record become expired. Enter that PHP code into **Subscription Expired Script** parameter

![PHP Script Settings](php-script-plugin.png)

Some notes:
1. You don't have to use **<?php** and **?>** tag to open and close the PHP code
2. In the PHP script, you can use a variable called $row. It contains all information of the subscription record. For example $row->first_name, $row->last_name, $row->email, $row->plan_id....


