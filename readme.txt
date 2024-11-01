=== Apply with Gravity Forms for WP Job Manager ===

Author URI: http://astoundify.com
Plugin URI: https://github.com/Astoundify/wp-job-manager-gravityforms-apply/
Donate link: https://www.paypal.com/cgi-bin/webscr?cmd=_xclick&business=contact@appthemer.com&item_name=Donation+for+Astoundify WP Job Manager Gravity Forms
Contributors: spencerfinnell
Tags: job, job listing, job apply, gravity forms, wp job manager
Requires at least: 3.5
Tested up to: 3.9
Stable Tag: 1.3.1
License: GPLv3
License URI: http://www.gnu.org/licenses/gpl-3.0.html

Allow themes using the WP Job Manager plugin to apply via a defined Gravity Form.

== Description ==

Allow themes using the WP Job Manager plugin to apply via a defined Gravity Form.

= Where can I use this? =

Astoundify has released the first fully integrated WP Job Manager theme. Check out ["Jobify"](http://themeforest.net/item/jobify-job-board-wordpress-theme/5247604?ref=Astoundify)

= Tutorial Video =

https://vimeo.com/85469722

== Frequently Asked Questions ==

= Nothing happens when I set the Gravity Form ID? =

It is up to the theme to respect your choice to use this plugin (as there is no way to automatically insert the form). The theme you are using must add:

`if ( class_exists( 'Astoundify_Job_Manager_Apply' ) ) :
	echo do_shortcode( '[gravityform id="' . get_option( 'job_manager_gravity_form' ) . '" title="false" ajax="true"]' );`

Make sure you have created a hidden field in your form. Under the "Advanced" tab check "Allow field to be dynamically populated" field and add a value of `application_email`

= I do not receive an email =

You **must** create a *hidden* field with the following specific settings:

* **Label:** Application Email
* **Allow field to be dynamically populated:** `application_email`

[View an image of the settings](https://i.cloudup.com/XfRsp5B1VH.png)

The Job/Resume listing must also have an email address associated with it, not a URL to a website.

= I am using Jobify and it's not working =

**Please make sure you have the latest version of Jobify from ThemeForest**

If you have purchased Jobify and still have questions, please post on our dedicated support forum: http://support.astoundify.com

== Installation ==

1. Install and Activate
2. Go to "Job Listings > Settings" and choose the forms you would like to use.

== Changelog ==

= 1.3.1: March 19, 2014 =

* Fix: Don't try to run if Gravity Forms is not active.

= 1.3.0: March 18, 2014 =

* New: Load a list of forms in a dropdown list, instead of inserting a form ID.
* Fix: Update setting name to work with the latest version of Jobify (you need to resave your options).

= 1.2.1: February 14, 2014 =

* Fix: Check the entire form to find where the field for the email is. We cannot count on it being last since Gravity Forms puts empty fields at the end.

= 1.2.0: February 4, 2014 =

* New: Make sure you have created a hidden field in your form. Under the "Advanced" tab check "Allow field to be dynamically populated" field and add a value of `application_email`

= 1.1.2: February 1, 2014 =

* Fix: Properly return variable on filter.
* Fix: Typo fix for sending job emails.

= 1.1.1: January 26, 2014 =

* Fix: Make sure resume contact submissions are going to the correct place.
* Fix: Avoid conflict with Gravity Forms when submitting a resume.

= 1.1: January 20, 2014 =

* New: Add support for a Resume Contact form when using Resume Manager

= 1.0: August 14, 2013 =

* First official release!