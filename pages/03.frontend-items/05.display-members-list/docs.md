---
title: 'Display Members List'
taxonomy:
    category:
        - docs
---

**Membership Pro** allows you to display subscribers from one or all subscription plans in the frontend of your site. You can control user what Joomla groups can see these subscribers and what fields will be showed on the subscribers list screen. Below are the steps to setup:

1. Create a menu item to link to **Members List** view of Membership Pro. In the menu item, you can choose one subscription plan and the extension will only display subscribers from that selected plan. If no plan is selected, subscribers from all plans will be displayed.
2. If you want any fields to be displayed on members list screen, please go to **Membership Pro -> Custom Fields**, edit the custom field, set **Show On Members List** property to **Yes**
3. The final step is selecting what **user groups can view this members list**. It is handled by Joomla core ACL, you can access to Membership Pro categories management screen, click on **Options** button in the toolbar, select the user groups you want to view members list (for example Public group), set **View Members** permission to **Allowed**. After that, user from these groups will be able to click on the created menu item to see list of subscribers.

