---
title: 'Group Membership'
taxonomy:
    category:
        - docs
---

Group Membership is a nice / unique feature of Membership Pro. It allows you to setup a subscription plan so that when someone sign up to that plan, he will become group admin and can add/ remove group members to/ from his group:

1. Group members will have same access level with group admin, so they can view any restricted resources you give access to subscribers of that plan. The only difference is that group members could not add new members to the group like group admin
2. When group admin renew his subscrition, subscription for all groups members will also be renewed
3. The number of group members which a group admin can add to his group can be controlled via a setting of the subscription plan

To setup this feature, please follow the steps below:
1. Edit the subscription plan which you want to enable **group membership**, enter the **number of group members** you want group admin can add to his group into **Max number of group members** input box. Save the plan.
2. Create a menu item to link to Manage Groups Member view of Membership Pro. After that, when someone signed up for the plan you just setup, he can login, access to the menu item to add/manage his group members

Usually, you will just want that only group admin can see the menu item which you created in step #3 above. We can handle it using Joomla core ACL with a clever steup. Below are the steps:

1. Create a new Joomla group called **Group Admin** for example. This should be child group of **Registered** group. Remember ID of this group, we need it in later step
2. Create an access level called **Group Admin**, only select **Group Admin group** for that access level
3. Config the subscription plan so that when user sign up for the plan, beside the groups you want, he will be assigned to **Group Admin** Joomla group as well
4. Go to **Extensions -> Plugins**, find the plugin **OS Membership - Group Membership Plugin**, click on it to edit. You will see a parameter called **Exclude Group Ids**. By default, it has the value 7, 8 (IDs of Administrator and Super Admin Group), please enter ID of the **Group Admin** into that parameter (separated by comma), for example, if Group Admin has ID = 10, please enter 7,8,10 into that parameter. The purpose of doing this step is that it prevent Group Members being assigned to this **Group Admin** joomla group so that they won't see the menu item.
5. Edit the menu item which you created before, set access to **Group Admi**n. With this setup, only group admin can see and access to this menu item