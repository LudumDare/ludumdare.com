+++
title = "Roadmap"
draft = true
+++
The following is a living document, a snapshot of where we would like Ludum Dare to go. 

The order is arbitrary. Unless otherwise noted, the features or changes listed here don't have a deadline.

This resource is provided as an alternative to digging through [GitHub](https://github.com/ludumdare), the developer chat, [Mike's twitter](https://twitter.com/mikekasprzak) and [project blog](https://distraction.engineer/projects/ludum-dare/).


## Search
There's a lot of content on the Ludum Dare website, and it should be searchable.

#### Prerequisites
* Finish the current server migration (on schedule to be complete by Ludum Dare 50)

> NOTE: prerequisites being _on schedule_ don't mean the features requiring them will be completed by this date.


## Uploading and embedding games
To avoid confusion and enable the embedding of web games, we will allow game uploads directly to Ludum Dare. Uploading is optional.

On schedule to be complete by Ludum Dare 51.

#### Prerequisites
* Partnership TBA


## Warmup entries
Bring back support for warmup entries. In the past we ran warmup mini-events the weekend before Ludum Dare, so users could familiarize themselves with our website and their tools.

#### Prerequisites
* Multiple submission support


## User Blogs
Currently blog posts are tied to a game, which is tied to an event. There's nothing technically stopping us from letting you make a personal blog, not tied to specific games or events.

#### Prerequisites
* Multiple submission support (the part that lets you decide which item to attribute blogs to)
* Reserve 4 digit numbers as slugs, so they don't conflict with implied paths containing years (potential Y10k bug)
* Have mitigation and moderation tools in place for spammers. To date we've managed to limit their growth by limiting when events can be signed up for. Opening this up means we need to expect them always and at all times.


## Craft entries
**Craft** entries are non-game entries. If you don't want to make a video game, you'll be able to submit other things. Comics, stuffed toys, short music albums, posters/wallpapers, cakes, short films, etc; Any original creative project inspired by Ludum Dare's Theme.

#### Prerequisites
* Multiple submission support
* Better handling of image sets (galleries) as submissions
* Decide what to do about memes
* Decide how they're rated, and how they're discovered


## Import games from legacy website (ludumdare.com/compo)
Migrate the game pages, blog posts, and user blobs from the WordPress website to the new one. This includes regular Ludum Dare events, a couple one-off events, and the MiniLD events. User blobs include data like when you first created your account (so we can credit you for your longevity), and your original account id.

#### Prerequisites
* Build and test an HTML to markdown converter 
* Regenerate the results data from imported games
* Upload all images from the old website
* Create a way for users to claim games migrated from the old website.
* Generate a static website to redirect old links to their new locations.
* Establish a new domain for the _master_ event database. For example, `ldjam.com` today acts as the master database.


## Rebuild database of games from before the legacy website
We have access to _some_ of the data from before we built the legacy WordPress website, but not all of it. Some of it is on `archive.org` as well. The good news is there were only a few dozen games submitted to each event, so if need be we can rebuild this data by hand, though results data will be limited.

#### Prerequisites
* Import games from legacy website (`ludumdare.com/compo`)
* Create stubs for all Ludum Dare events we didn't run on the legacy website


## Import 72hourGDC entries
The spiritual predecessor to Ludum Dare's "Jam" event was an event called the 72hourGDC. We have the data from those events available to us, and I would like to include them as part of our archive.

#### Prerequisites
* Import games from legacy website (`ludumdare.com/compo`)
* Establish a new domain for the _master_ event database. For example, `ldjam.com` today acts as the master database.


## Native support for post-event games
We encourage folks to _do something_ with their games post-event. We should make adding post-event games a standard feature. We should also make associating a game with another game a standard feature.

#### Prerequisites
* Import games from legacy website (`ludumdare.com/compo`)
* Establish a new domain for the _master_ event database. For example, `ldjam.com` today acts as the master database.
* Multiple submission support


## Support for _other_ games
Ludum Dare isn't the only Jam in town. Once we finish importing the data from our previous events, it makes sense to allow you to add other games as well. Games from other jams, or games made independent of jams. This data can then be used by `jammer.bio`.

#### Prerequisites
* Import games from legacy website (`ludumdare.com/compo`)
* Establish a new domain for the _master_ event database. For example, `ldjam.com` today acts as the master database.
* Have mitigation and moderation tools in place for spammers. To date we've managed to limit their growth by limiting when events can be signed up for. Opening this up means we need to expect them always and at all times.


## The extended Extra category
The Extra category will be extended to allow games to be submitted to any previous Ludum Dare event. At the moment, Extra games can be submitted until the end of the voting period.

#### Prerequisites
* Import games from the legacy website (`ludumdare.com/compo`)
* Create stubs for all Ludum Dare events we didn't run on the legacy website
* Have mitigation and moderation tools in place for spammers. To date we've managed to limit their growth by limiting when events can be signed up for. Opening this up means we need to expect them always and at all times.


## Flexible categories
Instead of choosing a category like "Jam" or "Compo", we switch to a flexible system where you can choose how you want to compete. Any combination of the following:

* Made in 24, 48, 72 hours, or unrestricted (opting out of final scoring)
* Made Solo or with a Team
* Made with or without 3rd party addons and content
* Optionally includes source code

Many of these details can be detected, further simplifying how submissions work.

If there's enough demand, we can include "1 week" and "2 week" timelines as well, but official winners will be games made in 72 or less.

#### Prerequisites
* Many systems need to be rebuilt from the ground up, including how submission and results work
* Source code incentives need to be established if sources are no longer required


## New Event domain
In time `ldjam.com` will be retired, and events will be run from `jam.ludumdare.com`.

#### Prerequisites
* Establish a new domain for the _master_ event database. For example, `ldjam.com` today acts as the master database.
* Finish support for domain masks. For example, `ldjam.com/events/ludum-dare/` to `jam.ludumdare.com/events/` for cleaner canonical URLs like `jam.ludumdare.com/events/50/results`.
* Generate a static website to redirect old links to their new locations.


## jammer.bio pages
Because we can, repurpose user data as a portfolio website. `jammer.bio/your-name`.

#### Prerequisites
* Establish a new domain for the _master_ event database. For example, `ldjam.com` today acts as the master database.
* Create a new interface to the data. Initially the plan was to use domain masks (`ldjam.com/users/bob` -> `jammer.bio/bob`), but that breaks routes to game pages (`ldjam.com/events/ludum-dare/50/bobs-great-game/`).
* Ensure that game page slugs for a single user don't conflict (might be tricky with team games)


## Universal Accounts
In addition to participating in Ludum Dare events, we would like to make your accounts usable by related side services. This might mean creating our own OAuth2 provider, or whatever the latest-and-greatest way to do this is.

In the short term we would like Ludum Dare accounts to give you access to our Matrix server (`jammer.chat`). Then as we research, explore, and understand this more, open it up to 3rd parties looking to build services around Ludum Dare.

#### Prerequisites
* Establish a new domain for the _master_ event database. For example, `ldjam.com` today acts as the master database.
* Finalize established APIs


## More events per year
At full capacity, we _could_ run up to 4 events per year (January, April, July, October), but we _shouldn't_ do this until running Ludum Dare puts less burden on Mike.

#### Prerequisites
* ~~shorten the rating period, and adjust the schedule to allow for quarterly events~~ (done)
* Time and (hu)manpower


## Education
We've established ourselves as a great tool for motivate yourself to make games. The next step is to focus on teaching you how to make games, OR what to do with a game after making them.

#### Prerequisites
* Time and (hu)manpower


## Ludum Dare's Game Dev Bootcamp
Sign-up for an intense 4 week (?) course and learn how to make games. At the end of the bootcamp, you put your skills to the test by entering Ludum Dare.

Each bootcamp focuses on a specific development tool or workflow. 

#### Prerequisites
* Warmup Entries
* Establish our education stuff
* Build a curriculum
* Time and (hu)manpower
* Budget
