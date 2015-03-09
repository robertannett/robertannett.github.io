---
layout: post
title: Markdown and HTML
---

<b>Stop mail processing:</b>
Service postfix stop

<b>Terminal commands:</b>
Mailq: Opens the mail queue
Postcat –v 123: Opens the mail item where 123 is the email id in mailq
postsuper -d ALL deferred: Clears the deferred mail queue.
 
<b>Find who sent mail (email address being sent from):</b>
<code>
cat /var/log/maillog | grep sasl_username | sort
</code>

<b>Locations:</b>
Ubuntu 12.04 with plesk installed; the emails logs are in: /var/spool/postfix

<b>Start mail processing: </b>
Service postfix start

<b>Check server load:</b>
Find free memory: free –m
