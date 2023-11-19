# Open Media Vault

## Changing the login splash scren after timeout
In /var/www/openmediavault
```
vi __custom.css

/* Add css link <link rel="stylesheet" href="__custom.css"> to /var/www/openmediavault/index.html */

/* To disable the animation but keep the matrix background */

body .omv-login-page .background {
 -webkit-animation-name:none !important;
 animation-name:none !important;
 -webkit-animation-duration:0s !important;
 animation-duration:0s !important;
 -webkit-animation-iteration-count:0 !important;
 animation-iteration-count:0 !important;
}

/* Or to install my own background */
/*
body .omv-login-page .background {
content:url(/assets/images/myownbackground.jpg) !important;
-webkit-animation-name:none !important;
animation-name:none !important;
-webkit-animation-duration:0s !important;
animation-duration:0s !important;
-webkit-animation-iteration-count:0 !important;
animation-iteration-count:0 !important;
}
*/
```
#### Note
It doesn't seem to work.

## Sending email from openvault
I add to create an [app password](https://support.google.com/mail/answer/185833?hl=en-GB&sjid=3623814072379207560-EU)

Maybe a better alternative would have been to use [restricted Gmail SMTP server](https://support.google.com/a/answer/176600?hl=en&sjid=3623814072379207560-EU)


Add a line to index.html to load the css
```
vi index.html
<link rel="stylesheet" href="__custom.css">
```
