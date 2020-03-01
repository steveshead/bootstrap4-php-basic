# Bootstrap 4 - PHP Basic Template v1.0

This is a basic PHP template using Bootstrap 4. View the [demo](https://devtestweb.com/phpbasic/) site [here](https://devtestweb.com/phpbasic/).

### Active Menu
The PHP code in the file 'includes/a_config.php' will highlight the menu link for the current page.  If you add more pages you will need to add an entry to that file.

```html
<?php
	switch ($_SERVER["SCRIPT_NAME"]) {
		case "/about.php":
			$CURRENT_PAGE = "About";
			$PAGE_TITLE = "About Us";
			break;
		case "/contact.php":
			$CURRENT_PAGE = "Contact";
			$PAGE_TITLE = "Contact Us";
			break;
		default:
			$CURRENT_PAGE = "Index";
			$PAGE_TITLE = "Welcome to my homepage!";
	}
?>
```

### Contact form
The contact form will need some edits for it to work for you. Instead of using reCaptcha I have used a hidden field, though I'm not sure how much longer that will work as a workaround.

* Replace 'steve@steve-shead.com' on line 8 of assets/contact/contact.php and line 11 of assets/contact/sendmail.php with the email address you want the messages from the contact form sent to.
* You can change the 'subject' for the message on line 12 of assets/contact/contact.php and line 20 of assets/contact/sendmail.php.
* You can edit the messages pushed to the form after submission in assets/contact/sendmail.php.
* The javascript for the contact form is in the file assets/js/scripts.js - you should not need to change that.
* You can edit the styles in the file assets/css/contact.css. These styles will relate to the code in assets/js/scripts.js file.

### Replace the favicons
Create your custom favicon [here](https://www.favicon-generator.org/).  Then with the code generated replace the code below in your index.html, and replace the favicon images in assets/img/favicon with yours.

```html
<link rel="apple-touch-icon" sizes="57x57" href="assets/img/favicons/apple-icon-57x57.png">
<link rel="apple-touch-icon" sizes="60x60" href="assets/img/favicons/apple-icon-60x60.png">
<link rel="apple-touch-icon" sizes="72x72" href="assets/img/favicons/apple-icon-72x72.png">
<link rel="apple-touch-icon" sizes="76x76" href="assets/img/favicons/apple-icon-76x76.png">
<link rel="apple-touch-icon" sizes="114x114" href="assets/img/favicons/apple-icon-114x114.png">
<link rel="apple-touch-icon" sizes="120x120" href="assets/img/favicons/apple-icon-120x120.png">
<link rel="apple-touch-icon" sizes="144x144" href="assets/img/favicons/apple-icon-144x144.png">
<link rel="apple-touch-icon" sizes="152x152" href="assets/img/favicons/apple-icon-152x152.png">
<link rel="apple-touch-icon" sizes="180x180" href="assets/img/favicons/apple-icon-180x180.png">
<link rel="icon" type="image/png" sizes="192x192" href="assets/img/favicons/android-icon-192x192.png">
<link rel="icon" type="image/png" sizes="32x32" href="assets/img/favicons/favicon-32x32.png">
<link rel="icon" type="image/png" sizes="96x96" href="assets/img/favicons/favicon-96x96.png">
<link rel="icon" type="image/png" sizes="16x16" href="assets/img/favicons/favicon-16x16.png">
<link rel="manifest" href="assets/img/favicons/manifest.json">
<meta name="msapplication-TileColor" content="#ffffff">
<meta name="msapplication-TileImage" content="assets/img/favicons/ms-icon-144x144.png">
```

### Bootstrap CSS
I have added some styles to extend Bootstrap 4 that I find useful. These are in the assets/css/extend.css. Bootstrap 4 padding a margin shortcuts such as my-5 (margin top and bottom) only go up to 5.  I've found I need larger padding and margins so I have extended those to 9.  I have also added style to increase and decrease letter spacing. You don't have to use these and can delete the file if you don't want them.

View the [demo](https://devtestweb.com/phpbasic/) site [here](https://devtestweb.com/phpbasic/).

Note this template isn't perfect.  You may need to make adjustments for it to work for you, specifically to make it fully responsive. It is responsive but I have not fine tuned it.  I am also re-learning PHP so there may be better ways of achieving some of the results.  Feel free to make suggestions for updates etc - it will be partly how I learn.
