---
title: 'Import Subscribers'
taxonomy:
    category:
        - docs
---

When you first setup Membership Pro to your site, you might have a list of existing subscribers which you want to import into the system. That usually happens in case you have to migrate subscribers from a different membership extensions or from different system to Membership Pro. In this case, you can use **Import Subscribers from CSV file** feature of Membership Pro to import. You can see detailed instruction at [http://joomdonation.com/forum/membership-pro/23141-new-feature-import-subscribers-from-csv-file.html](http://joomdonation.com/forum/membership-pro/23141-new-feature-import-subscribers-from-csv-file.html)

1. Each system / site can have a different set of custom fields. So the CSV File format can be different. The sample I mentioned on forum is just a generic format. To get the CSV File for your site, please access to **Subscriptions => CSV Import Template** to download sample csv file corresponding to the setup on your site
2. The date in csv file (in **payment_date**, **from_date**, **to_date** columns) must be in **YYYY-MM-DD** format.
3. If a row has **username**:
* If that username has a Joomla account on your site already, the subscription record will be assigned to that Joomla account
* If that username doesn't exist in Joomla users database, Membership Pro will create a Joomla account from that username and given password. If password is empty, a random password will be generated
4. The published column can has the following value:
* 0: Pending
* 1: Active
* 2: Expired
5. Event the published field has value = 1 (Active), if the column to_date has value set to a past date, the subscription record will be expired almost immediately after running the import
6. If the a Joomla account is created for the subscription record, Joomla will send notification email to user about the account. If you don't want Joomla to send notification email (for example, when you run the import), you can edit the plugin **User - Joomla!**, change parameter **Notification Mail to User** to **No** during the import. When the import is done, you should turn it back to **Yes** again




