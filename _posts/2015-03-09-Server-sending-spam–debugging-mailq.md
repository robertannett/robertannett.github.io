---
layout: post
title: Server sending spam – debugging mailq
---

A standard process for debugging the mailq on Ubuntu in terminal

<h2>Stop mail processing:</h2>
`Service postfix stop`

<b>Terminal commands:</b>
<ul>
<li>`Mailq` or `sendmail -bp`: Opens the mail queue</li>
<li>`Postcat –v 123`: Opens the mail item where 123 is the email id in mailq</li>
<li>`postsuper -d ALL deferred`: Clears the deferred mail queue.</li>
</ul>

<h2>Find who sent mail (email address being sent from):</h2>
`cat /var/log/maillog | grep sasl_username | sort`

<h2>Locations:</h2>
Ubuntu 12.04 with plesk installed; the emails logs are in: `/var/spool/postfix`

<h2>Start mail processing: </h2>
`Service postfix start`

<h2>Check server load:</h2>
Find free memory: `free –m`
