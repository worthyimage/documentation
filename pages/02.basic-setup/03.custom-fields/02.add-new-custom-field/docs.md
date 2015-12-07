---
title: 'Add New Custom Field'
taxonomy:
    category:
        - docs
---

From custom fields managemenet screen, press **New** button in toolbar to add a new custom field. When setup a cuustom fields, the following information will need to be entered:

## General Information
1. **Plan**: Select the plan(s) this custom field will be assigned to. You can select **All Plans**, **one plan** or **multiple plans** (use **Ctrl + Click** to select multiple plans)
2. **Name**: The name of custom field.  Please only use the folowing character for field name: **a-z, A-Z, 0-9**. No space, no special characters in the field name.
3. **Title**: The display title of the field.
4. **Field Type**: Chose the type of the field. 
5. **Description**: For most of field types, the description will be displayed when users hover over the title of the field. For **Message field type**, the description will be displayed as a message on subscription form.
6. **Required**: If set to Yes, users will have to enter a value (or select an option) for the field. If it to No, the field will be optional
7. **Default Values**: The default value of the field will be used to fill-in the field automatically when subscription form first displayed to subscriber. For **List (Multiple Select), Checkboxes** custom field types, each **default selected option** must be entered in a separate line.
8. **Data Type Validation**: Usually use for **Text** custom field type. It forces subscribers to enter data for the field in a required format. When you select an option in this property, the corresponding **Validation Rules ** will be generated.
9. **Validation Rules**: This is usually used for **Text** custom field type, and it will be generated automatically when users select **Data Type Validation** of the field (mentioned above). The extension uses JQuery Validation Engine to validate data users enter on subscription form, so if you want to take full advantage of this validation engine, please read the documentation at http://posabsolute.github.io/jQuery-Validation-Engine/ to see all powerful validation rules which you can use to validate data of the custom fields.
10. **Fee Field** : Set to Yes if this is a **custom fee field**. Then the value which subscribers enter / select for this field will be calcualted the additional fee (beside the price of the subscription plan) which subscribers will have to pay for their subscriotion.
11. **Fee formula**: You can use **[FIELD_VALUE]** and math operator : +, -, * , / to calculate fee value for this field. It is usually used for textbox field type. You can use other custom fields in the fee formula with the syntax [NAME_OF_CUSTOM_FIELD_IN_UPPERCASE]

## List (single & multiple select), Radio, Checkboxes specific settings
The settings below will only be displayed (and needed to setup) for single & multiple select,  Radio, Checkboxes custom field types

1. **Values**: The list of options available for subscribers to select. Each option need to be displayed in one separate line.
2. **Fee Values**: The fee values corresponding to the options above. Each fee value must be a float number and must be entered in one separate line. There is a mapping 1-1 between the option and fee value. This only need to be entered if Fee Field set to Yes

## Display settings

These settings below will be used to control how the field is displayed in the system

1. **Multiple**: Only use for **List** custom field. If you want the select dropdown to be multiple select, set this to Yes. Otherwise, set it to No and It will be a single dropdown
2. **Css Class**: If you want to apply a css class for this custom field so that you can style it, add the css class into that property.
3. **Extra**: Any other html attributes you want to add to the field. The most popular usecase is that if you want a textbox custom field to be readonly, you can enter **readonly** into this property
4. **Show on members list**: This setting will only be used if you display subscribers from frontend of your site. If you set this config option to Yes, the field will be displayed on Member list. If No, it won't be displayed. If you display subscribers, you will at least have to set this proerperty to Yes for First Name, Last Name, Organization.....
5. **Hide on membership renewal**: If you want this field to be hided on the subscription form when subscriber renew thier membership (only want to collect data for this field when they first sign up), set this property to **Yes**.	

## Dependency settings (Conditional Custom Fields)

Sometime, you want that when subscribers select certain otpions (From List, Checkboxes, Radio custom fields), there will be additional fields be showed/hided to allow entering additional information. If that's the case, you will need to use this **Conditional Custom Fields** feature

1. **Depend On Field**: Select the field (which we call **master field**) this custom field will be depended on. In this dropdown, the system will display the published **List, Checkboxes, Radio** custom fields which you created in the system. When you select a field from this dropdown, the custom field which is being added/edited will only be displayed if certain values of the **master field** is checked/selected.
2. **Depend On Options**: Check on the options which you want this field to be showed when subscribers select an option from master field.

To make it easier for you to understand the concent, let's take an example. On subscription form, you have:

1. A checkbox custom field called **Programming Languages** which allow subscribers to choose the programming language they can use. It has 3 values: **PHP**, **HTML**, **CSS**
2. You want that when subscriber selects a programming language, there will be an additional text field to collect more information (version of the programming language - it is not a good example) about the programming languges he can use. In this case, you will create 3 additional text fields:
* **PHP Version**: For this field, you set **Depend On Field** to **Programming Languages**. And in the depend on options, you select **PHP**
* **HTML Version**: For this field, you set **Depend On Field** to **Programming Languages**. And in the depend on options, you select **HTML**
* **CSS Version**: For this field, you set **Depend On Field** to **Programming Languages**. And in the depend on options, you select **CSS** 
3. Now, when subscribers access to subscription form:
* If they check on **PHP** checkbox, the **PHP Version** field will be showed. If they uncheck this option, the field will be hided.
* If they check on **HTML** checkbox, the **HTML Version** field will be showed. If they uncheck this option, the field will be hided.
* If they check on **CSS** checkbox, the **CSS Version** field will be showed. If they uncheck this option, the field will be hided.


Please see the screenshots below to understand the setup and hopefully, you get the idea about how it works and can use conditional custom fields feature in Membership Pro now. If not, post a question on forum and I will be happy to answer or help you with a sample setup for your system:

![Dependency Setup](dependency_fields.png)

![How conditional custom fields work](conditional_custom_fields.png)

