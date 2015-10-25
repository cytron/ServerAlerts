# ServerAlerts
Server Host or HTTP monitoring with email alerts

Installation:

This software does not require installation. Simply download the .ZIP file, unzip to a local drive and you are good to go.

Configuration:

---Host configuration:

Edit the config.xml file. Add your hosts in <Host></Host> tags. You can add as many tags as you like. If you are monitoring a web site, you must specify http or https. For example, http://www.google.co.uk. If you are adding a local server, do not add http, just the pingable host name. For example, file.domain.local or just file if your DNS can resolve it to an IP.



---Email Notifications Configugation:

Edit the mailConfFile.xml and add the SMTP server configurations as below:

1. <Host></Host> - The SMTP server address. You must add the SMTP server address for email notifications
2. <Username></Username> - This tag should have your SMTP server username. For example, if you use google SMTP to relay emails, your user name will be the email address.
3. <Password></Password> - Password to the account
4. Port - SMTP server port. The default port is 25 but if you are using Google SMTP, you must use 587
5. <MailFrom/> - Name of the sender. This could be anything
6. <FromAddress/> - This is the email address that will be included in the email header. Usually the same as username if using Google SMTP
7. <SSL/> - Please indicate if your SMTP server requires SSL enabled. For google, you must set the value to 1. If not needed, set to 0.
8. <MailTo/> - This is a collection of email addresses separated by comma. These are all the recipients who will receive email notifications if any of the hosts is off-line
For example, <MailTo>address1@domain.com,address2@domain.com,address3@domain.com</MailTo>
