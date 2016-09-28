## SMTP module for Magento2
Magento2 module for setting up and using SMTP mail

All you need is either a (i) free Gmail account, (ii) paid Google Apps account or any other SMTP service (i.e Amazon Simple Email Service / Amazon SES )

###Why SMTP?
Most emails delivered using sendmail (default mail daemon used for sending mails on Linux) will either get blocked by an ISP or be flagged as SPAM. 
By Using SMTP server for delivering emails, you can ensure quick and reliable delivery. Also, if you need to send out a high number of emails to your users, most hosting companies won't allow it using their shared mail servers. So, you really don't have any option if you want to send bulk emails (_For example, newsletters_) to your customers.

####1 - Installation
##### Manual Installation

 * Download the extension
 * Unzip the file
 * Create a folder {Magento root}/app/code/CzoneTech
 * Extract the contents of the zipped folder inside it.


#####Using Composer

```
composer config repositories.czone-tech-smtp git git@github.com:czone-tech/magento2-smtp.git
composer require czone-tech/magento2-smtp
```

####2 -  Enabling the module
Using command line access to your server, run the following commands -
 $ php -f bin/magento module:enable --clear-static-content CzoneTech_SmtpMail
 $ php -f bin/magento setup:upgrade

####3 - Admin configuration
Log into your Magento Admin, then goto 
'Stores -> Configuration -> CzoneTech Modules -> Smtp Settings' 
Enter the SMTP server settings

## Screenshot
