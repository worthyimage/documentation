---
title: 'Develop Membership Pro plugin'
taxonomy:
    category:
        - docs
---

Membership Pro allows you to develop plugins to extend it's features. Infact, it has many plugins come with it by defualt which you can see in the foldder **plugins/osmembership** on your site.

Membership Pro supports the following events trigger which you can write plugin to handle to add more features to the extension:

## onEditSubscriptionPlan

This event is triggered on add/edit subscription plan. It usually used to allows you to display a form to allow admin control the necessary settings for your plan. A sample is the Joomla Groups plugin which allows admin to select which user groups subscriber of the plan will be added to when membership active and what user groups he will removed from when the subscription is expired

```php
public function onEditSubscriptionPlan($row)
{
	
}
```

## onAfterSaveSubscriptionPlan

This event is triggered after the subscription plan is saved to database. It is usually used to save the settings data which you displayed on subscription add/edit screen so that you can used that settings data later

```php
public onAfterSaveSubscriptionPlan($context, $row, $data, $isNew)
{
	
}
```

## onMembershipActive
This event is triggered when a subscription record become active (when payment for the subscription complete or admin approve the subscription record manually from backend)

```php
public onMembershipActive($row)
{
	
}
```

## onMembershipExpire

This event is triggered when a subscription record become expired (the current date is greater than the subscription end date of the record)
```php
public onMembershipExpire($row)
{
	
}
```

