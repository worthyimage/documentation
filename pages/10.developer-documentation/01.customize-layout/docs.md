---
title: 'Customize Layouts'
taxonomy:
    category:
        - docs
---

Sometime, you might want to customize layout of some pages in Membership Pro to meet your requirement. Some notes below should be helpful to you if you have to do that:
1. If you want to add any css code to the extension, don't modify the css file directly. Please add all your custom css code to **components/com_osmembership/assets/css/custom.css** so that it won't be lost when you update to future release of the extension
2. If you want to customize the layouts in the extension, please use **Template Override** so that it won't be lost when upgrade your site to newer version of the extension. Please see  for detailed instruction:
* If you want to customize the **plans list** page, depend on the layout you are using (default, columms, pricing table), you will need to get a copy of one of the file (default_plans.php, columns_plans.php, pricingtable_plans.php) in folder **components/com_osmembership/view/common**, **place** it to **PATH_TO_YOUR_SITE_TEMPLATE/html/common** folder, then do any customization you want in that file
* If you want to customize the **plan detail** page, take a copy of the file **components/com_osmembership/view/plan/default.php**, place it to **PATH_TO_YOUR_SITE_TEMPLATE/html/plan** folder and do any customization from there.
* If you want to customize the **subscription form** page, take a copy of the file **components/com_osmembership/view/register/default.php**, place it to **PATH_TO_YOUR_SITE_TEMPLATE/html/register** folder and do any customization from there.
3. If you use pricing table layout to display subscription plans, you might want to mark one of the plan as **Recommended**. If you want to do that, edit the menu item you created to display the plans, look at **Recommended Plan ID** parameter, enter ID of that plan into that parmeter and it will be marked as **Recommended**
