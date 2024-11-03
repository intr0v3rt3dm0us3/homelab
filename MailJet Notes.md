**MailJet Notes**

Sample Configuration for using MailJet for homelab email notifications.

***NOTE:***

Replace XXX or X or X.X.X.X with local data

Replace smtp_host with your host

## Sample


```"_enable_smtp": true,
"use_sendmail": false,
"smtp_host": "in-vX.mailjet.com",
"smtp_security": "starttls",
"smtp_port": 587,
"smtp_from": "XXX@TLD.com",
"smtp_from_name": "XXX",
"smtp_username": "XXX",
"smtp_password": "XXX",
"smtp_timeout": 15,
"smtp_embed_images": true,
"smtp_accept_invalid_certs": false,
"smtp_accept_invalid_hostnames": false,
"_enable_email_2fa": true,
"email_token_size": 6,
"email_expiration_time": 600,
"email_attempts_limit": 3,
"email_2fa_enforce_on_verified_invite": false,
"email_2fa_auto_fallback": false
```

TBD

> Written with [StackEdit](https://stackedit.io/).
