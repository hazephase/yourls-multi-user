yourls-multi-user plugin
~~~~~~~~~~~~~~~~~~~~~~~~

This is a modification of the multi-user 1.7 beta yourls plugin created by Matheus (X-warrior) Bratfisch.  The original can be found:

http://www.matbra.com/en/code/multi-user-yourls-plugin/

The plugin was updated to use LDAP for authentication, and to cleanup some interface issues.

A plugin for YOURLS that allow multi users in the system

How it works:
Enabling this plugin it will be created two new tables in your data base. One to user registers and other to record what URL is from what user. The plugin allow public or private (owner and admin) access to statistics. The user when creates a new shortned link can change it and remove it. (not recommended becaause urls already published will become not valid.)

How to install:
- Copy plugin files to /user/plugins/multi-user/ folder.
- Access the administration area and activate the plugin.
- To access user pages use yoursite.com/your-yourls/user/plugins/multi-user (create a link in homepage is highly recommended)

Setup:
If you want something different than default setup, achange your config file.
YOURLS_MULTIUSER_PROTECTED - TRUE/FALSE - Stats is private to admin and owners of shortned links.
YOURLS_DB_TABLE_URL_TO_USER - Specific the name of database table to be used as URL to USER table.
YOURLS_DB_TABLE_USERS - Specific the name of the database table to be user as USERS table.
YOURLS_MULTIUSER_CAPTCHA - Enable user CAPTCHA to Sign in.
YOURLS_MULTIUSER_CAPTCHA_PUBLIC_KEY - Public API Key to Recaptcha, get yours: https://www.google.com/recaptcha/admin/create
YOURLS_MULTIUSER_CAPTCHA_PRIVATE_KEY - Private API Key to Recaptcha.
YOURLS_MULTIUSER_CAPTCHA_THEME - ReCAPTCHA theme.
YOURLS_MULTIUSER_ANONYMOUS - True if Anonymous user can shorturl, false if just logged users can shorturl.
YOURLS_MULTIUSER_LDAP_SERVER
YOURLS_MULTIUSER_LDAP_BASEDN
YOURLS_MULTIUSER_LDAP_GROUPDN 
YOURLS_MULTIUSER_LDAP_GROUPNAME - Members of this group will be allowed to login.  If no group is specified, any user that can authenticate successfully will be able to login.
YOURLS_MULTIUSER_FORCE_SSL - TRUE/FALSE - forces the login to use SSL

It may also prove to be useful to add a short URL for the keyword login that points to http://<sitefqdn>/user/plugins/multi-user .