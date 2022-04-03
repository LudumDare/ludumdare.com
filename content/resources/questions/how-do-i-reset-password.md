+++
title = "How do I reset my password?"
weight = 99
[taxonomies]
Categories = ["Security"]
+++

Use this link, and enter your email to reset your password.

<https://ldjam.com/#user-reset>

You will receive an email. Follow the link to change your password.


# What if I don't get the email?
If you didn't receive an email, chances are the problem is one of these.

* You used the wrong email address
* You used an email alias (Gmail, ProtonMail, etc)
* You have an old `ludumdare.com/compo` account, but not an `ldjam.com` account
* You never activated your account
* You don't have an account

For security reasons, the website can not confirm if this worked or not. See below.[](why-cant-the-website-confirm-if-my-email-exists) for more details.


# How can I check my email?
Account creation, activation, and reset emails come from the following senders.

* `hello@ldjam.com`
* `hello@jammer.vg` (before 2021)

Search your email inbox for messages from these senders, and check who they were sent to.

Your activation email may look like this.

![](/resources/questions/sample-email.png)

Note that the email was sent to `joe.c.hest@gmail.com`.


# What is an email alias?
Some emails providers send multiple addresses to the same inbox.

For example, with Gmail:

* `joechest@gmail.com`
* `joe.chest@gmail.com`
* `joe.c.hest@googlemail.com`
* `joe.c.hest+ludumdare@gmail.com`

All 4 of these will reach the same inbox.

Aliases are extremely useful, but they are nonstandard features. Not every provider supports them, or supports them in the same way. We can't assume that `joechest@gmail.com` and `joe.c.hest@gmail.com` are the same. You must use the exact email you signed up with.


# What is a `ludumdare.com/compo` account?
In 2017 the Ludum Dare event was moved to a brand new website, where everyone was required to create new accounts. If you participated before 2017, you have an account on the old website, but not necessarily one on `ldjam.com`.

If you are sure you have an account, we recommend checking for an activation email (described above).

Alternatively, you can confirm if your user page exists (described below).


# How can I check if an account exists?
You can confirm an account exists by visiting its user page.

User page URLs look like this: `https://ldjam.com/users/YOUR-USERNAME`, where `YOUR-USERNAME` is your username.

For example, Mike's username is `PoV`. His user page is [https://ldjam.com/users/pov](//ldjam.com/users/pov)

Alternatively, you could also use [https://ldjam.com/users/PoV](//ldjam.com/users/PoV).

If you get a `404` error, the account does not exist.


# What does it mean to activate an account?
When creating an account, you are sent a verification email. The email contains a link you must click to continue creating your account. 

The link takes you to a page where you choose your name and password. When finished, your account is activated.

You cannot reset a password if you never completed verification, or activated your account.


# What if I don't have an account?
Create one here:

<https://ldjam.com/#user-register>


# What if I know my password, but not my email?
Log in and visit this URL:

<https://api.ldjam.com/vx/user/whoami>


# Why can't the website confirm if my email exists?
We can't securely confirm or deny if an email address exists. 

If we were anything but vague here, a malicious actor could extract emails using brute-force.

