---
title: Plans
taxonomy:
    category:
        - docs
---

Plans are the central of the system. That's what you sell to your customers. You setup subscription plans, then customers browse your site, see these plans and subscribe to the plan he wants, process payment... to become an active subscriber in the system.

Base on the **price** of subscription plans, Membership Pro supports the following subscription plans type

1. **Free subscription plans**
2. **Onetime payment subscription plans**
3. **Recurring Subscription plans**
4. **Recurring Subscription plans with trial duration** (can be free trial)

Base on the **subscription length**, we can devide subscription plans into the two types below:

1. **Fixed subscription length** (for example **15 days**, **1 month**, **3 months**, **1 year**). For this type of subscription plans, when subscribers sign up, their subscription will be expired after the subscription length you defined for the plan.
2. **Fixed Expiration Date**. For this type of subscription plans, when subscribers sign up, their subscriptions will be expired at a fixed date (for example 31 December 2016), not depend on the date they sign up. Of course the extension is smart enough so that if users sign up after that fixed date, their expiration date will be changed to next year. For example, if you set **Expiration Date** of the plan to **31 Decemmber 2015** and users sign up at **sometime in 2016**, their subscription will be expired on **31 December 2016**. So in this case, you won't have to change setting of the plan every year.

To access to categories management page, there are 3 different ways:
1. Access to **Components => Membership Pro => Subscription Plans**.
2. Access to Membership Pro Dashboard, then click on Plans icon
3. On any pages in Membership Pro, access to **Setup => Plans**

![Plans Management](plans.png)

## Add new subscription plan
Press New button in the toolbar to create new subscription plan. A form will be displayed to allow you to enter information of the plan.

### Basic Information

<table class="table table-bordered table-stripped table-considered">
<thead>
<tr><th width="15%">Property</th><th>Description</th></tr>
</thead>
<thead>
<tr>
<td><strong>Title</strong></td>
<td>Title of the subscription plan.</td>
</tr>
<tr>
<td><strong>Alias</strong></td>
<td>Alias will be used to generate the URL link to the plan detail page. If you unsure what to enter, simply leaves it empty and the system will generate the alias based on the title of the plan.</td>
</tr>
<tr>
<td><strong>Category</strong></td>
<td>Choose the category which the plan will be assigned to. As mentioned before, categories is optional in Membership Pro, so you don't have to choose a category if you don't have categories setup in the system.</td>
</tr>
<tr>
<td><strong>Price</strong></td>
<td>The price users have to pay to subscribe to this subscription plan. If you want the plan to be free, simply enter 0 into this field (or leave it empty).</td>
</tr>
<tr>
<td><strong>Subscription Length</strong></td>
<td>
How long the subscription will be active if subscribers sign up for this plan. It can be X days, X weeks, X months, X years.
</td>
</tr>
<tr>
<td><strong>Expired Date</strong></td>
<td>
<p>If you want all subscriptions of this plan to be expired on the same date (no matter when the subscribers sign up), you can choose that fixed expiration date into this field. For example, if you set this property to 31/12/2015:</p>
<ul>
<li>
If users sign up before 31/12/2015, their subscription will be expired on <strong>31/12/2015</strong>
</li>
<li>
If users sign up after 31/12/2015, for example on 06/05/2015, their subscription will be expired in <strong>31/12/2016</strong>
</li>
</ul>
</td>
</tr>
<tr>
<td><strong>Lifetime Membership</strong></td>
<td>If you want all subscriptions of this plan to remain active for lifetime (never expired), you can set this field to Yes. By default, it should be No and subscribers will be expired after certain date (depends on Subscription length field)</td>
</tr>
<tr>
<td><strong>Thumbnail</strong></td>
<td>Thumbnail of the plan, it is optional. If you upload thumbnail for the plan, it will be displayed on plan list and plan detail page.</td>
</tr>
<tr>
<td><strong>Send First Reminder</strong></td>
<td>If you want the system to send the first remember email to subscribers of this plan <strong>X</strong> days before their subscription expired, enter <strong>X</strong> into this field. The reminder email message can be configured in Membership Pro => Emails && Messages section. If you enter 0 or leave empty, the first reminder email won't be sent.</td>
</tr>
<tr>
<td><strong>Send second Reminder</strong></td>
<td>
If you want the system to send the second remember email to subscribers of this plan <strong>Y</strong> days before their subscription expired, enter <strong>Y</strong> into this field.If you enter 0 or leave empty, the second reminder email won't be sent.
</td>
</tr>
<tr>
<td><strong>Send Third Reminder</strong></td>
<td>
If you want the system to send the third remember email to subscribers of this plan <strong>Z</strong> days before their subscription expired, enter <strong>Z</strong> into this field.If you enter 0 or leave empty, the third reminder email won't be sent.
</td>
</tr>
<tr>
<td><strong>Enable Renewal</strong></td>
<td>
<p>You should set this field to <strong>Yes</strong> so that users can renew their subscription before/when/after it is expired. There are only two cases you should set it to <strong>No :</strong></p>
<p>1. The subscription plan is a free trial subscription plan, so you don't want subscribers to renew after it is expired</p>
<p>2. The subscription plan is a <strong>recurring subscription plan</strong>. In this case, the renewal is handled automatically by Membeship Pro and the payment gateway, so users won't have to renew manually, and this field should be set to No</p>
</td>
</tr>
<tr>
<td><strong>Short description</strong></td>
<td>Short description of the subscription plan. It will be used to show on plans list page.</td>
</tr>
<tr>
<td><strong>Description</strong></td>
<td>Full description of the subscription plan. It will be displayed on plan details page. If you don't enter description, the short description will be used instead.</td>
</tr>
</thead>
</table>


### Renew Options
If you enable renewal for the subscription plan, subscribers can renew their membership to be remain as an active subscriber in the system:
1. If you don't setup any renew options, when subscribers renew their membership for the plan, he will have to pay the same price with the price of the subscription plan and their membership will be extended X days / Weeks / Months / Years (with X is subscritption length of the plan)
2. If you setup renew options, subscribers can choose the best renew option they want to renew their membership. Each renew option will have different price and will extend subscribers membership to a certain date (less time, less price, more time, more price). For example, if you have a subscription plan with subscription length 3 months and price 60$, you can create different renew options like that to give more renew options to your subscribers:
* Renew membership for 1 month, the price will be 20$
* Renew membership for 2 months, the price will be 36$ (the pricec is abit less to ecourage subscribers renew longer)
* Renew membership for 4 months, the price will be 70$... and so on

![Renew Options Setup](renew_options.png)

### Upgrade Options
You might want to give users the option to **upgrade** their membership from a subscription plan with **lower prority** (access to less resources in less time) to other subscription plan with higher priority (access to more resources in a longer time). For example, upgrade from **3 Months Memebership** to **6 Months Memebership** or **12 Months Memebership**. In this case, you can add upgrade options when you add / edit subscrition plan as you see in this screenshot:

To add upgrade options, in add / edit subscription plan plage, look at **Upgrade Options** section, press **Add** button add new upgrade option, select the plan which subscribers of this plan can upgrade their membership to and enter the price of the upgrade.

![Upgrade Membership Options](upgrade_options.png)


### Recurring settings

Membership Pro supports recurring subscription feature. When subscribers sign up for a recurring subscription plan, the subscription will continue being renewed automatically until he cancel it or number of renewals reach the **Number Payments** setup by admin for the subscription plan. 

![Recurring settings](recurring_subscription.png)

To make a plan become recurring subscription plan, you need to set **Recurring Subscription** proerpty of that plan to **Yes**. There are addition parameters which you can setup for a recurring subscrition plan as explained below:

1. **Trial Duration**: If you to give subscribers of this subscription plan a trial duration, setup the trial duration here. Usually, trial duration should be shorter than subscription length, it could be X days/ weeks / months / years. When setup trial duration, you will need to dertermine the trial price which subscribers will have to pay for that trial duration, too.
2. **Trial amount**: This is the price subscribers have to pay for the trial duration you setup above. You you want to have free trial, you can set Trial amount to 0 (or leave it empty) 
3. **Number Payments**: If you want the subscription ends after certain number of payments, you can enter **Number Payments** here. Otherwise, leave it empty and the renewal will continue happens unless subscribers or administrator cancel it.

### Advanced Settings

The **Advanced Settings** section allows you to setup some settings which only be applied for this specific subscription plan. You can ignore the settings in this section and the global configuration options will be used.

![Advanced Settings](advanced_settings.png)

| Property | Description |
| ------ | ----------- |
| **Max number of group members**   | Maxium number of group members which group admin can add to his group. You will only have to make this setup if you are using **Group Membership** feature. We will describe in in a separate section in the document.|
| **Login Redirect** | Select a menu item which subscribers of this plan will be redirected to when they login. If you want to use this feature / option, make sure you publish the plugin **User - Membership Pro** |
| **Payment Methods**    | Select the payment plugins you want to be available for this plans. If you don't select any payment methods, in the published payment plugins will be available. |
| **Currency**    | If you want this plan to use a different currency than other plans - currently only wors with Paypal, you can select the currency you want to use here. If you select currency, please also enter **Currency Symbol** for this plan, too. |
| **Subscription complete url (optional)**    | By default, Membership Pro will redirect subscribers to default subscription complete page which display subscription information. If you want subscribers of this plan to be redirected to a specific page on your site after completing the subscription, you can enter the URL of that page into that field |
| **Notification emails**    | Enter the emails you want to receive notification when someone sign up for this plan. If you leave this field empty, the notification emails which you entered in Configuration will be used. |
| **Paypal Email**    | Enter the paypal email which you want to receive payment when someone sign up for this plan. Leave it empty to use the Paypal account which you entered in Paypal payment plugin |
| **Term and condition article**    | Select terms and conditions article you want to use for this plan. If you don't select, the terms and conditions article which you select in Configuration will be used|
