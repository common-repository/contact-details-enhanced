=== Contact Details Enhanced ===
Author: Tiziana Troukens (alt3rnate)
Contributors: Tiziana Troukens, 36Flavours
Tags: dutch, contact, global, details, options, info, phone, fax, mobile, email, address, bankaccount, form
Requires at least: 2.8.2
Tested up to: 3.4.1
Stable tag: 1.0
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Adds the ability to easily enter and display contact information.

== Description ==

Adds the ability to enter contact information and output the details in your posts, pages or templates.

Based on the original "Contact Details" by 36Flavours, but the visible text has been translated to Dutch and a bankaccount field has been added.

Use the shortcode `[contact type="phone"]` to display any of the contact details, or use the function call `<?php if (function_exists('contact_detail')) { contact_detail('phone'); } ?>`.

Once you have defined a contact email address, use the shortcode `[contact type="form"]` to output the contact form.

== Installation ==

Here we go:

1. Upload the `contact` folder to the `/wp-content/plugins/` directory.
2. Activate the plugin through the 'Plugins' menu in WordPress.
3. Enter you contact details on the options page `Settings > Contact Details`.
4. Display the details using either the shortcodes or function calls.

== Frequently Asked Questions ==

= How do I edit my contact details? =

Navigate to the settings page by clicking on `Settings` on the left hand menu, and then the `Contact Details` option.

= How do I include details in my template? =

You can use the following function call to output details in your templates:

<?php if (function_exists('contact_detail')) { contact_detail('fax'); } ?>

= What contact details can I store? =

Current available contact fields are: `phone`, `fax`, `mobile`, `email` and `address`.

= How do you fetch contact details without outputting the value? =

The fourth parameter passed to `contact_detail()` determines whether the value is returned, by setting the value to false.

`$phone = contact_detail('phone', '<b>', '</b>', false);`

The above code will fetch the phone number stored and wrap the response in bold tags.

= How can I customise the contact form? =

If you require more customisation that cannot be achieved using CSS, you can define your own template file.

To do this add the the attribute `include` to the shortcode tag, e.g. `[contact type="form" include="myfile.php"]`.

This file should be placed within your theme directory and should include the processing and output of errors.

I suggest you use the `contact.php` file used by the plugin as a starting point / template.

== Screenshots ==

1. The contact details management page.

== Changelog ==

= 1.0 =
* This is the very first version, based on "Contact Details" by 36Flavours.