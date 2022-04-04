+++
title = "How do I reset my password?"
weight = 99
[taxonomies]
Categories = ["Security"]
+++

Use this link, and enter your email to reset your password.

<https://ldjam.com/#user-reset>

You should receive an email a few minutes later. Follow the link to change your password.


## What if I don't get the email?
If you don't receive an email, the problem should be one of the following:

* You used the wrong email address
* You used an email alias (Gmail, ProtonMail, etc)
* You have an old `ludumdare.com/compo` account, but not a newer `ldjam.com` account
* You never activated your account
* You don't have an account

For security reasons, we can't specifically say if we found your email or not (see below[](why-cant-the-website-confirm-if-my-email-exists)).


## How can I check my email?
We send emails from the following addresses.

* `hello@ldjam.com`
* `hello@jammer.vg` (before 2021)

Search your email inbox for messages from these senders, and check who they were sent to.

Your activation email may look like this.

![](/resources/questions/sample-email.png)

In the example above, that the email was sent to `odin.c.hest@gmail.com`.

Alternatively, if you know your username and password, you can lookup you email address (see below). 


## What is an email alias?
Some emails providers route multiple addresses to the same inbox.

For example, with Gmail:

* `odinchest@gmail.com`
* `odin.chest@gmail.com`
* `odin.c.hest@googlemail.com`
* `odin.c.hest+ludumdare@gmail.com`

All 4 of these will reach the same inbox.

**IMPORTANT**: Aliases are a nonstandard features. Not every email provider supports them, or supports them in the same way.


## What is a `ludumdare.com/compo` account?
In 2017 the Ludum Dare event was moved to a brand new website, where everyone was required to create new accounts. If you participated before 2017, you have an account on the old website (`ludumdare.com/compo`), but not necessarily one on `ldjam.com`.

If you are sure you have an account, we recommend checking for an activation email (described above).

Alternatively, you could also confirm if your user page exists (see below).


## How can I check if an account or user page exists?
You can confirm an account exists by visiting its user page.

User page URLs look like this: `https://ldjam.com/users/YOUR-USERNAME`, where `YOUR-USERNAME` is your username.

For example, Mike's username is `PoV`. His user page is [https://ldjam.com/users/pov](//ldjam.com/users/pov)

Alternatively, you could also use [https://ldjam.com/users/PoV](//ldjam.com/users/PoV).

If you get a `404` error, the account does not exist.


## What does it mean to activate an account?
When creating an account, you are sent a verification email. The email contains a link you must click to continue creating your account. 

The link takes you to a page where you choose your name and password. When finished, your account is activated.

You cannot reset a password if you never completed verification, or activated your account.


## What if I don't have an account?
Create one here:

<https://ldjam.com/#user-register>


## What if I know my password, but not my email?
We don't have a page for this yet, but you can still look it up with the API.

Log in to your account, then visit this URL.

<https://api.ldjam.com/vx/user/whoami>

It will output a short JSON response similar to this: 

```js
{"status":200,"caller_id":48,"mail":["odin.c.hest@gmail.com"]}
```

In this example, the email address is `odin.c.hest@gmail.com`.


## Why can't the website confirm if my email exists?
We can't securely confirm or deny if an email address exists. 

If we were to output anything more specific, a malicious actor could abuse this to extract emails.

