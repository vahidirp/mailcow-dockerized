# MailCow: Dockerized - 🐮 + 🐋 = 💕
#### documentation :
![Install-docs](https://docs.mailcow.email/i_u_m/i_u_m_install/)
![Uninstall-docs](https://docs.mailcow.email/i_u_m/i_u_m_deinstall)

## Want to support mailcow?

Please [consider a support contract with Servercow](https://www.servercow.de/mailcow?lang=en#support) to support further development. _We_ support _you_ while _you_ support _us_. :)

You can also [get a SAL](https://www.servercow.de/mailcow?lang=en#sal) which is a one-time payment with no liabilities or returning fees.

Or just spread the word: moo.

## Info, documentation and support

Please see [the official documentation](https://docs.mailcow.email/) for installation and support instructions. 🐄

🐛 **If you found a critical security issue, please mail us to [info at servercow.de](mailto:info@servercow.de).**

#### Preparations :
Before you can start installing Mailcow, you need to do some preparations, which mainly affect the DNS settings of the domain that you want to use to receive and send e-mails. To do this, follow the steps below:

    The hostname of your server should be "mail", so the FQDN should be "mail.testdomain.com".
    
    Add an A record for the subdomain "mail" (mail.testdomain.com) and let this point to the IP address of the mail server.
    
    Add an MX record for your domain and set the value to the mail subdomain you just created (mail.testdomain.com) with priority 10.
    
    Define a CNAME record for the subdomains "autodiscover" as well as "autoconfig" and set the destination of both CNAME records to the mail subdomain as well (mail.testdomain.com).
    
    Add an TXT record for your domain and set the value to "v=spf1 mx ~all", to allow the server specified in the MX record (the mail server where Mailcow will be installed) to send e-mails with your domain as the sender domain. The "~all" means that other servers are not allowed to send e-mails from your domain, but these e-mails will still be delivered (softfail).
    
    Define a PTR record (Reverse DNS) for the IP address of your server and set the value to the FQDN of your server ("mail.testdomain.com"). You can set this PTR record directly in the web interface of any good hoster like Contabo. For some providers, you have to write an e-mail or open a support ticket.


## Misc

**Important**: mailcow makes use of various open-source software. Please assure you agree with their license before using mailcow.
Any part of mailcow itself is released under **GNU General Public License, Version 3**.

mailcow is a registered word mark of The Infrastructure Company GmbH, Parkstr. 42, 47877 Willich, Germany.

The project is managed and maintained by The Infrastructure Company GmbH.

Originated from @andryyy (André)
