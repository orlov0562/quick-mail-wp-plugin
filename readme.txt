=== Quick Mail ===
Contributors: brainiac
Donate link: https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=4AAGBFXRAPFJY
Tags: email, admin, mail, idn, attachment, multisite, accessible, accessibility, rich text, Spanish, French
Requires at least: 4.4
Tested up to: 4.8
Stable tag: 3.0.4
License: GPLv3
License URI: http://www.gnu.org/licenses/gpl.html

Adds "Quick Mail" to Tools. Send text or html email with file attachments from user's credentials. French and Spanish translations.

== Description ==

>Quick Mail is the easiest way to send an email with attachments to WordPress users on your site. Compatible with multisite.

Send a quick email from WordPress Dashboard to WordPress users, or anyone. Adds Quick Mail to Tools menu.

Edit messages with [TinyMCE](https://codex.wordpress.org/TinyMCE) to add images, rich text and [shortcodes](https://codex.wordpress.org/Shortcode).

User options for sending email to site users or others. Mail is sent with user's name and email. Multiple files from up to six directories (folders) can be attached to a message.

= Features =

* Sends text or html mails to multiple recipients. Content type is determined from message.

* Multiple recipients can be selected from users or entered manually.

* Saves message and subject on form to send repeat messages.

* Saves last 12 email addresses entered on form.

* Share a WordPress draft by copying / pasting its code into a message.

* Option to validate recipient domains with [checkdnserr](http://php.net/manual/en/function.checkdnsrr.php) before mail is sent.

* Validates international domains if [idn_to_ascii](http://php.net/manual/en/function.idn-to-ascii.php) is available to convert domain to [Punycode](https://tools.ietf.org/html/rfc3492).

* Site options for administrators to hide their profile, and limit access to user list.

* Option to add paragraphs and line breaks to HTML messages with [wpauto](https://codex.wordpress.org/Function_Reference/wpautop).

= Learn More =

* See [How to Send Email from WordPress Admin](https://wheredidmybraingo.com/quick-mail-wordpress-plugin-update-send-email-to-site-users/) for an introduction.

* See [Quick Mail for WordPress 4.8](https://wheredidmybraingo.com/quick-mail-wordpress-4-8/) for update info.

== Installation ==

1. Download the plugin and unpack in your `/wp-content/plugins` directory

1. Activate the plugin through the 'Plugins' menu in WordPress

== Frequently Asked Questions ==

= Who can send mail? =

* Users must be able to [publish a post](http://codex.wordpress.org/Roles_and_Capabilities#publish_posts) to send an email. Minimum permission can be changed with a filter.

* User profile must include first name, last name, email address.

= Who can send rich text messages? =

* User must have [Visual Editor enabled](https://codex.wordpress.org/Function_Reference/user_can_richedit) on their profile, to compose messages with the Visual Editor.

* Anyone can send HTML by pasting it into a message.

= Selecting Recipients =

* Options to send mail to any user, or limit to users with first and last names on their profile.

* Users need permission to [list users](http://codex.wordpress.org/Roles_and_Capabilities#list_users), to view user list or change options. Minimum permission can be changed with an option or filter.

= Limitations =

* Up to 12 manually entered recipients are saved in HTML Storage.

* Additional recipients can be either `CC` or `BCC` but not both.

* Multiple files can be uploaded from up to 6 folders (directories).

* "Uploads are disabled" on some mobile devices.

Some devices cannot upload files. According to [Modernizr](https://modernizr.com/download#fileinput-inputtypes-setclasses) :
> iOS < 6 and some android version don't support uploads.

File uploads are disabled for ancient IOS 5 devices. Please [add a support message](https://wordpress.org/support/plugin/quick-mail) if uploads are disabled on your phone or tablet, so I can remove the upload button if your device is detected.

= Address Validation =

* Address validation is an option to check recipient domain on manually entered addresses.

* International (non-ASCII) domains must be converted to [punycode](https://tools.ietf.org/html/rfc3492) with [idn_to_ascii](http://php.net/manual/en/function.idn-to-ascii.php).

  Unfortunately, `idn_to_ascii` is not available on all systems.

* "Cannot verify international domains because idn_to_ascii function not found"

  This is displayed when Quick Mail cannot verify domains containing non-ASCII characters.

* [checkdnsrr](http://php.net/manual/en/function.checkdnsrr.php) is used to check a domain for an [MX record](http://www.google.com/support/enterprise/static/postini/docs/admin/en/activate/mx_faq.html).

  An MX record tells senders how to send mail to the domain.

= Mail Errors =

* Quick Mail sends email with [wp_mail](https://developer.wordpress.org/reference/functions/wp_mail/).


  `wp_mail` error messages are displayed, if there is a problem.

* "You must provide at least one recipient email address."


   `wp_mail` rejected an address. Seen when Quick Mail verification is off.

== Screenshots ==

1. Selecting users on Quick Mail data entry form.

2. Multiple attachments from different folders (directories).

3. Selecting saved recipients.

4. Quick Mail options.

5. Full screen view.

== Changelog ==

= 3.0.4 =
* fixed reset email content type.
* preserves shortcodes in messages.

= 3.0.3 =
* fixed email content type compatibility error.
* fixed settings display error.

= 3.0.2 =
* added wpauto option for HTML messages.
* display user nickname instead of `user_nicename`.

= 3.0.1 =
* added Blind Carbon Copy (BCC).
* improved HTML messages.

= 3.0.0 =
* improved data entry form accessibility and design.
* added visual editor.

= 2.0.5 =
* improved multiple file uploads.
* hide some admininstrative options when User List is not available.

= 2.0.4 =
* added Javascript file for translating options message.

= Earlier versions =

Please refer to the separate changelog.txt for changes of previous versions.

== Upgrade Notice ==

= 3.0.4 =
* Upgrade recommended.

= 3.0.3 =
* Upgrade recommended.

= 3.0.2 =
* Upgrade recommended.

= 3.0.1 =
* Upgrade recommended.

= 3.0.0 =
* Upgrade recommended.

= 2.0.5 =
* Upgrade recommended.

= 2.0.4 =
* Upgrade recommended.

== License ==

Quick Mail is free for personal or commercial use. Please encourage future development with a [donation](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=4AAGBFXRAPFJY "Donate with PayPal").

== Translators and Programmers ==

* A .pot file is included for translators.

* Includes Spanish and French translations.

* See [Quick Mail Translations](https://translate.wordpress.org/projects/wp-plugins/quick-mail) for more info.
