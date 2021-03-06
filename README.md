# spamassassin-extremeshok_fromreplyto

## Maintained and provided by https://eXtremeSHOK.com

## Description
Configures spamassassin to score mails with various rules against the reply-to, from and to headers.
Spam often uses a different From: and Reply-To: Whilst most legitimate email does not.
Spam often uses the same From: and To: Whilst most legitimate email does not
Same domain checking Logic, will allow for different subdomains of the same domain name.

## REQUIRES
spamassassin

## INSTALL GUIDE

create the plugin directory.
```
mkdir /etc/mail/spamassassin/plugins/
```

Download and save the plugins to /etc/mail/spamassassin/plugins/

Download and save 01_extremeshok_fromreplyto.cf to /etc/mail/spamassassin/01_extremeshok_fromreplyto.cf

Verify the installation
```
spamassassin -D --lint 2>&1 | grep -i failed
```
## Version 1.5 (updated 2016-07-11)
 - eXtremeSHOK.com Maintenance
 - Fixed dbg: plugin: did not register FromIsTo, already registered
 - Refactored to better support spamassassin 3.4 and newer

## Version 1.4
 - eXtremeSHOK.com Maintenance
 - More unique variable names
 - Fixed FromIsTo to check if the from and to are the same, then increase the spam score
 - Added FromIsReplyTo to decrease spam score
 - Fixed spam score points

## Version 1.3.1
 - eXtremeSHOK.com Maintenance
 - More unique variable names
 - Fixed warn: Global symbol
 
## Version 1.3
 - eXtremeSHOK.com Maintenance
 - Added FromIsTo, most spam emails the from" and to" is identical
 - Minor code cleanups
 - Project renamed
 - Improved documentation
 
## Version 1.2.10
 - eXtremeSHOK.com Maintenance
 - Fix for scoring missing from/replyto as a fail

## Version 1.2.0
 - eXtremeSHOK.com Maintenance
 - Better logic with domain checking, will allow for different subdomains of the same domain name.
