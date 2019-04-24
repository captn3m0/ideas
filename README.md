> There's no such thing as an original idea. Every idea worth having has been had thousands of times already.
>
> -   [swombat](https://news.ycombinator.com/item?id=250793)

**Table of Contents**

-   [Introduction](#introduction)
-   [NoFollow Enforcer](nofollow.md) :hankey:
-   [PyPi Notifier](pypi-notifier.md)
-   [OpenBook](#openbook) :hankey:
    -   [Expectations](#expectations)
    -   [Features](#features)
    -   [Interface](#interface)
    -   [Backend](#backend)
-   [iStalk](#istalk) :hankey:
    -   [Idea](#idea)
    -   [Interface](#interface-1)
-   [Distributed Privacy conscious TrueCaller Alternative](yellow-pages.md) :sparkles: :gift:
-   [Collaborative Bookmarking](#collaborative-bookmarking) :sparkles: :gift:
-   [Lightspeed for Chrome](#lightspeed-for-chrome) :rocket:
-   [Facebook Analytics](#facebook-analytics)
-   [API for Workflowy](#api-for-workflowy)
-   [Onion Cannon](onioncannon.md) (E2E encrypted communication for machines)
-   ~~[Lettersafe](#lettersafe) :hankey:~~
-   [Email on top of keybase](#email-on-top-of-keybase)
-   [Newsletters for GitHub](#newsletters-for-github) :rocket:
-   [Hacking via OAauth tokens](#hacking-via-oaauth-tokens) :rocket:
    -   [But OAuth tokens can be revoked](#but-oauth-tokens-can-be-revoked)
    -   [Procedure](#procedure)
-   [Pluggable Notify Daemon for linux](#pluggable-notify-daemon-for-linux)
-   [Telegram Channel to RSS](#telegram-to-rss) :gift: :sparkles:
-   [Disable Local Fonts Extension](#disable-local-fonts-extension) :gift:
-   [Community Browser Extension](communities-browser-extension.md) :gift:
-   [Card Game Modelling (Research)](card-game-modelling.md)
-   [Arch Linux Package Build System](#arch-linux-package-build-system)
-   [Hacker News Research Bot](#hacker-news-research-bot)
-   [Slack Dialer](#slack-dialer) :construction:
-   [Mars - Mars: Terraform Remote HTTP Backend with End-to-End encryption](mars.md)
-   [Tachiyomi Headless](#tachiyomi-headless) - Comic book scraper for all platforms
-   [OPML Generator](#opml-generator) :rocket:
-   [Bangalore Events List](#bangalore-events-list) :construction:
-   [Amazon Price Tracker with RSS](#amazon-price-tracker-with-rss) :rocket:
-   [OPML Sync](#opml-sync)
-   [Database Conversion Toolkit using an ORM](#database-conversion-toolkit-using-an-orm)
-   [Sanskari Proxy](#sanskari-proxy) :gift: :sparkles:
-   [Automated Personal Finance](#automated-personal-finance) :sparkles:
-   [UPI On Desktop](#upi-on-desktop) :sparkles:
-   [Helm Charts for Self-Hosting](#helm-charts-for-self-hosting)
-   [Fake Paytm Payment](#fake-payment-payment)
-   [Licence](#licence)

## Introduction

This is a open repository of personal ideas. Some of these are based on personal interactions, bug reports, and discussions I've had with lots of people. I've tried to give credit wherever possible. I also try to reference similar/existing projects that might relate to the idea, so if you know of something that is interesting in that space, file a PR or send me a link.

## OpenBook

Some ideas are annotated with emojis:

-   :sparkles: - Favorite Ideas. I really like this, and you could possible build a company of some of these.
-   :hankey: - Not all ideas are great. These are things I thought might work at one point, but no longer consider worth building. I don't remove such ideas from the repo, because I think all ideas are worth learning from.
-   :gift: - I'd love to help you build this, consider this like a bounty. You'll get a personal postcard from me for building something on this list.
-   :rocket: Someone (might be be) built this!
-   :construction: There is a work-in-progress implementation.

All of the above are just indicative. Make something people want is the YC motto, but sometimes you must make something for no good reason other than "just because".

## OpenBook

:hankey:

_Edit_: Lots of marketing companies already have built this, but not in the creepy way that I'd have liked.

This is a privacy-awareness application that relies on the TrueCaller data-sharing model. It is meant to teach users that their privacy is not in their hands, but in the hands of those that they trust.

The idea itself is to let people browse facebook as someone else. This is done by note of the following points:

1.  Facebook allows OAuth API access that allow your application to perform tasks as any user whose token you have.
2.  To start using the service, you must "hand in your data" first. Just like TrueCaller uploads _your entire phonebook_ before you can use the app, openbook requires you to give us access to _your facebook account_ before you can use openbook.

### Expectations

This has massive privacy implications. People assume their facebook data (such as information on your about page) to be available to only people they have friended on facebook. However, it is also accessible to all applications you authorize, which is what we are exploiting basically. I expect the application to be banned and have its keys revoked within a day or two. If I were to make this, I'd rather not use my own facebook account for fear of getting it suspended.

### Features

Since the idea is to teach users about privacy, openbook will not ask for access to all data. It will probably use a harmless data-property that will essentially be made public to all users of the app. Currently, I'm thinking "No. of Friends", which is not always available to public if you've hidden your friend list. It is harmless enough to not cause any mayhem, and yet vital enough to just show that such _attacks are possible_.

### Interface

1.  Homepage will be a simple FAQ on privacy-related matters and what the app does.
2.  A login page
3.  A search interface to search amongst all users using the app.
4.  A profile page of any user, where you can see their data using someone else's token.

### Backend

Unlike facebook, which can directly access _any data_ on their servers, we are limited to using their API. Which means getting data for any user has now become a mapping problem. You need to know which tokens can access data of which user. This could be made possible by pre-mapping the users accessible via each token, and refreshing each token's list every week or so (as you make new friends).

This idea probably breaks lots of point in Facebook's ToS, but that doesn't mean it can't be built.

## iStalk :hankey:

This is essentially a unified profile mechanism, where a user's identity is defined by all of their activity on various networks. While this has some cool sub-ideas (like correlating activity between various networks), the most important implication that arises is that it can be a perfect tool for stalking. However, you can easily add in consent from the original profile owner to clear that concern.

### Idea

iStalk lets you "follow" a person across various networks that they belong to. Some networks, like twitter are mostly public, and can be followed very easily. But other networks (like Facebook) are harder to follow by virtue of them requiring a "connection" between the two users. iStalk makes it easier for you by using your account on that network as a proxy-connect mechanism.

Basically, you give us your access tokens, and we use them to stalk someone for you.

### Interface

A profile creation page allows you to specify as much information as you have on the person. This includes their facebook, twitter, last.fm, github usernames for eg. Each integration you want has to first be verified by you granting us (iStalk) access to your account (via OAuth).

Once a profile has been created, we will continuously long-poll the service to fetch new information as and when it becomes available. Real-time notifications are delivered to you as the person's activity is tracked.

## Collaborative Bookmarking

:sparkes: :gift:

There are a dozen bookmarking services out there, many of them quite well done. However, most services are focused on the idea that bookmarking is a lone-person habit, which someone does in isolation.

I've often described the idea as "dropbox for bookmarks". The core concept is to allow a bookmarking "tag/folder" to be shared with another user, two-way. This means any of the shared members can add/remove bookmarks from that folder.
All updates (addition/deletion/edits) are notified to every member in the group.

Bookmarking for Teams, in essence. Some good alternatives are [listed in this quora answer](https://www.quora.com/Hello-What-are-the-best-web-apps-for-sharing-bookmarks-across-a-team), which you should read and follow if you're interested in this.

I've described this idea somewhat better in a chat log at [collaborative-bookmark.md](collaborative-bookmark.md)
Google Spaces did some nice work here, but the product was shut down within an year of launch.

## Lightspeed for Chrome

:rocket:

[Lightspeed](https://www.youtube.com/watch?v=wLnSLFrQDG8) is an experimental UI design (not implemented) for Firefox that focuses on making the New Tab page more functional by giving the browser a decent way to search across bookmarks, open tabs, and history.

It is a pretty neat idea (see the video linked above). My first thought on seeing the video was that most of that stuff could be done using the Chrome APIs for Chrome as well. Chrome does offer a way for an extension to override the new tab page, after all.

The discussion on [HN](https://news.ycombinator.com/item?id=8151271) is also very good.

_Update_: There is some progress on the WebExtension porting of Lightspeed, given the recent Firefox updates. With this in place, it should be relatively easier to port the webextension version to Chrome itself.

_Update_: [@tallpants](https://github.com/tallpants) made this: https://github.com/tallpants/lightspeed

## Facebook Analytics

I like the analytics that WolframAlpha provides for Facebook. Except that they are not really that useful. I'd like an easy query interface that let me "filter" data points, and get back open-data via the Graph API. This means, for eg, getting the most liked music artist among a subset of my friends. The interface I'm thinking of right now is like Gapminder, which allows you to "play" the dataset as it evolves over time.

A recommendation engine built on top of my facebook data is a good idea, I think.

## API for Workflowy

Workflowy is a cool tool that I use for note-taking. It allows infinitely nested lists with @mention and #hashtag support. One thing it lacks currently is API for me to access my own data. I think workflowy is a great tool that could become a lot better if there were a way for developers to hook into it. (For example using workflowy as a data-backend for a todo-app).

## Lettersafe

:hankey:

My notes for lettersafe are on [workflowy](https://workflowy.com/s/5439f7a9-3762-f247-3e96-4d047b5d4ce0).

The idea was to build a zero-knowledge email storage. Kinda like lavabit, with a few minor changes. After thinking about it for months, and working on it for a few days, I gave up on the idea. I understand now that server-side email encryption can never be a good idea.

## Email on top of keybase

Keybase has a cool API. I wonder if its possible to build an actual email service on top of keybase?

The original idea was from before Keybase had a chat feature, and I wanted to build an email service that used keybase to send and receive messages. Would have turned out similar to Keybase Chat.

How I'd approach it today is to use Keybase Social Graph for encrypting emails and make it easier via plugins/extensions. The ideal flow would be:

Use the Keybase Social Graph for encrypting emails and make it easier via plugins/extensions. The ideal flow would be:

1.  Login to GMail
2.  Compose an email to me@captnemo.in
3.  Extension pops up: "Hey, looks like this user is on Keybase already as keybase.io/captn3m0. Would you like to encrypt this email?
4.  If user clicks yes, do a keybase auth and follow the user as well, perhaps? (not sure if possible)
5.  Also give user an option to "Encrypt all emails sent to users with more than X followers)" or something similar...

Doing the same thing on the receiving side is trickier though, but I like the idea of using Keybase to discover anyone's public keys instead of the standard Web of Trust.

A Keybase plugin for Thunderbird would be similar in scope.

## Newsletters for GitHub

:rocket:

A lot of github project owners would like to send out newsletters to all of their
stargazers. However, GitHub doesn't provide anything for that. An easy way would
be to integrate StarGazers with MailChimp, making sure that people can unstar
a project to unsubscribe from the mailing list.

Only the repo owners and collaborators (maybe) should have access to sending out
newsletters. For bonus points, you can replace mailchimp with your own solution.

This could even be monetized slightly for paying off your server costs: newsletter
access for projects with >1k stars (the mailers that would cost you money) cost
money to the repo owner as well.

So a tiny python package pays nothing to update its users about a new release, but
if Angular team wants to send out an update, that gets paid.

And finally, this should automatically subscribe you to any new GitHub releases in
any project you have starred. This is a missing feature that I think can be best
implemented by a third-party for now.

_Update_: GitHub now supports [watching releases](https://github.blog/changelog/2018-11-27-watch-releases/).

There are lots of related projects in this thread: https://github.com/isaacs/github/issues/410

## Hacking via OAauth tokens

:rocket:

While pen-testing, once you've gained access to the target, it is often necessary to install a backdoor to mantain the access. While this is easily done in case of root access to the machine, this is not that easy if the target is an email account, lets say.

Many online services today (with data of considerable value) offer developers programmatic access to their data by use of APIs, which are usually authenticated via OAuth tokens. What I intend to build is a suite of applications (or a single large one) that allow you to use the application as another user, just by setting up an access token.

While this is certainly possible with existing tools (such as the Facebook Graph API Explorer), it is cumbersome and not user-friendly. The application will mimic the interface, usability, and looks of the actual application to let you maintain access easily enough.

### But OAuth tokens can be revoked

That is a good point, but one that fails in practice. A password change in most services does not trigger an automatic token revocation because that would leave a lot of developers and users unhappy. However, neither does any service warn you to check your approved applications (especially after a hacking attempt).

### Procedure

1.  You gain access to someone's account.
2.  You create an application (using a fake account or the victim's own account, so its not tied back to you)
3.  You setup our app (direct deploy to Heroku)
4.  You configure the app with the application credentials (app id, secret key)
5.  You authenticate the victim's account against the app
6.  You use the application to access the user's account

The account access will continue till the victim checks his/her approved applications.

:rocket: I made this: <https://github.com/captn3m0/amon>

## Pluggable Notify Daemon for Linux

Not another window manager daemon, because lots of them already exist and there
are already good APIs in almost all languages that make it easy to integrate with
all of them. However, Linux DEs are still missing an easy way for me to get notifications
about the thousands of little different things (such as build notifications).

The idea is to have a simple config where you can connect your bazillian accounts
via OAuth, and we will poll all your accounts and give you "clickable" notifications
for each of them. (GMail notifications might open your mail client if you click reply)

Keep it pluggable, otherwise its of no use.

## Telegram To RSS

:gift: :sparkles:

There are quite a lot of Telegram channels that are popping up these days that I really like using.
Except there are lots of issues with telegram channels:

1.  They are inside a closed network by-default. In order to access them you need to use the Telegram client
2.  They are not linkable
3.  No sharability without their client, and even then the content is duplicated.

The idea is to create a generic website that does these 2 things:

1.  Publish an RSS Feed of every telegram channel it knows about.
2.  Provide a direct link for every feed item on the RSS, so users without RSS readers can also browse through the listings.

Since `web.telegram.org` is taken already by the web client, maybe something like `opentelegram.in` should work fine.

There are a few related paid projects, but they all rely on the Telegram Bot API:

-   https://news.ycombinator.com/item?id=17617675
-   http://tele.ga/about.html

The issue with using the bot API is that bots need to be explicitly invited
to channels, while users can join channels on their own. This makes a world
of difference in that this doesn't require perission from the channel admins anymore.

You could likely get this sponsored from the Internet Archive if you get something up and running.

## Disable Local Fonts Extension

:gift:

A simple browser extension for web developers that disable local fonts from loading. Alternatively, it raises a grave warning if a web-font was bypassed for a local font. This is helpful if you are a developer:

-   And have some specific font installed locally (say Font Awesome)
-   And are developing a website that uses that font locally
-   And forget to include the Font in your stylesheet

The page continues to function normally in your development setup, but breaks in production.

Based upon this [chrome bug request](https://bugs.chromium.org/p/chromium/issues/detail?id=472136), which asks for this feature.

I came to know about this because [of a comment](https://github.com/captn3m0/disable-web-fonts/issues/1#issuecomment-143665811) on my "disable-web-fonts" extension, which does the opposite. This might be handy for people who want to make sure that web-fonts are working fine for all users.

## Arch Linux Package Build System

The Arch Linux User Repository is great. Except, a lot of packages rely on building-from-source since no binary releases are available. However, the build steps for these packages work very well, resulting in a working build. The idea is to create a AUR build server that takes in a AUR package name as input (it can have a whitelist of such packages), runs it in a docker container, and outputs a generated package file (`tar.xz`) that can then be directly installed on any machine.

This has some security concerns, mainly how do you trust a binary package an external server built?

Planning to solve this with attempting reproducible builds, and publishing everything. You can audit any build artifact whenever you wish. I'll likely just use the Docker ArchLinux image and build against that.

Moreover, the primary audience for this would be me. I would really like to get packages that can be installed much faster because I don't have to build them. I can just have a script that instead downloads the latest build from the server instead of AUR and then just installs the package instead of building it locally.

Take a look at https://github.com/Foxboron/arch-auto-build, which is a very similar attempt at this idea.

This is already handled by the Arch Build System (albeit without Docker). Using that might be a better idea.

## Hacker News Research Bot

A bot that posts paper abstracts and links to PDF whenever a paper referencing a research paper is posted to Hacker News. Most scicomm posts that make it to HN almost always have a primary paper reference, and someone ends up posting the paper abstract along with a link to Arxiv or SciHub usually. A bot that automates this for all HN submissions would be a fun project.

_Update_: Someone did this! See [@randomdrake's comments on HN](https://news.ycombinator.com/threads?id=randomdrake).

_Update 2_: The mods are not very happy with the [abstract being posted](https://news.ycombinator.com/item?id=16330366), but the rest should be good.

For Bonus Points: Include a link to the fermat library URL of the paper (if available).

# Slack Dialer :gift: :construction:

All of our company has contact numbers added on Slack, but it is cumbersome to find someone's profile on Slack. A simple dialer application that does OAuth-verification on your Slack profile to get a list of the entire organization, and present a simple dialer for all the people who have contact details added.

Interface would be a simple grid of faces, click to dial, sorted by frequency. A simple search-as-you-type box at the top. Can also be done as a PWA to easily make it cross-platform.

Note that this requires a Slack team with a paid account. I'll help you get a trial so you can build this.

:construction: <https://github.com/captn3m0/slack-dialer>

# Database Conversion Toolkit using an ORM

Something that lets you switch your database between SQLite/MySQL/Postgres/... by using
an existing ORM framework to import and export out the correct commands.

The grammar differences in most databases are taken care of by an ORM, and the remainder is just
switching your ORM to use an existing database as the source of truth. Even a specific variant
(say SQLite to MySQL) would be great to have.

Thought of this after spending a lot of time trying to migrate my Grafana/Gitea setups from
sqlite to mysql and trying every solution in [this SO question](https://stackoverflow.com/questions/18671/quick-easy-way-to-migrate-sqlite3-to-mysql).

There are some closed solutions to this, but would like a open-source solution that does this well.

## Tachiyomi Headless

:gift:

[Tachiyomi](https://github.com/inorichi/tachiyomi/) is a Android application written in Kotlin that
scrapes comics from various web sources. A headless version of it would be great to have, replacing
projects such as <https://github.com/evilhero/mylar> with something much more stable.

The end goal is something that works as a "minor" (<200L) patch on top of Tachiyomi, and does
a JVM-desktop build which can be run anywhere. A sample README would look something like:

A headless build for [tachiyomi][0] which you can run on your server on a schedule
to download comics. This downloads the comics in plain images and then converts them
to CBZ format with metadata intact. A new release is generated for every Tachiyomi release.

Get the latest release from the [releases page][1].
Download the `tachiyomi-headless.jar` file.

Run it as the following:

    java -jar tachiyomi-headless -c config.yml

Where the `config.yml` file looks like:

```yml
dir: /home/comics/
format: cbz
# All the tachiyomi extensions come pre-loaded
# https://github.com/inorichi/tachiyomi-extensions
comics:
    - http://readcomiconline.to/Comic/Marvel-The-End
    - https://manga-fox.com/one-piece
```

## OPML Generator

:rocket:

Simple web tool to generate OPML files to let you use RSS feeds everywhere.

I :heart: RSS because it gives me the control of how to consume and read the content.
While many services provide you RSS feeds, they do not give you an easy way to export
a list of things that you follow.

For eg: Every repository on GitHub has a releases RSS feed that you can follow. However,
you need to follow each one individually. Thankfully, there is a nice spec called OPML
which is used to pass around lists of RSS feeds.

What if one could generate a OPML feed for:

1.  Releases of repos that you have starred on GitHub
2.  Authors that you follow on GoodReads
3.  Bands that you follow on BandCamp

:rocket: I made a initial working demo recently for the first one, and you can check it at
<https://opml.bb8.fun>. The source code is at <https://git.captnemo.in/nemo/opml-gen>.

Related: https://github.com/RSS-Bridge/rss-bridge (I have contributed a few bridges to this)

## Bangalore Events List

:gift: :construction:

Similar in scope to http://webuild.sg/ or http://engineers.sg/ but for Bangalore.

-   Want to keep the name generic to support non-tech events as well
-   ICS support (WeBuild.sg/cal for demo) is a must-have
-   (They have a RSS feed as well!)

Domain name suggestions are welcome. Since blr doesn't have a TLD, I was considering using `.events`.

Initial Work: https://github.com/captn3m0/gardencity.events There is also some work from @tallpants on this at <https://github.com/tallpants/meetup2ics/>

## Amazon Price Tracker with RSS

:rocket:

There are some nice open source trackers available for Price Tracking Amazon products,
but I would like to see something that generated an RSS Feed.

This could be built on top of [RSS Bridge](https://github.com/RSS-Bridge/rss-bridge)
fairly easily. Configuration options would include:

-   Min Price (Only add to feed if price is below X)
-   Amazon Country/Domain (Use the specific Amazon website)
-   Item Id

:rocket: https://github.com/RSS-Bridge/rss-bridge/pull/741

(While the above is merged, this doesn't correctly work because it doesn't cache the information properly).

## OPML Sync

Instead of forcing users to do manual imports of OPML feeds, let them
auto-subscribe from feeds using a dynamically generated OPML feed. This is not
a product idea by itself, more of a extension idea for existing RSS Readers.

See related discussion on the [tt-rss forums](https://discourse.tt-rss.org/t/subscribe-to-opml/1230).

## Sanskari Proxy

:gift: :sparkles:

A lot of Indian Government websites are inaccessible on the public internet, because
they geo-fence it to within Indian Boundaries. I made a list of all [Indian Government
Websites](https://git.captnemo.in/nemo/pulse/src/branch/master/domains.csv), and the idea
is to make a Indian Proxy service that specifically works only for the Geo-fenced Indian GoI
websites.

For eg, if `uidai.gov.in` is inaccessible, hitting `uidai.gov.sanskariproxy.in` will get you
the same result, proxied via our servers.

This is not intended to be used for actual usage, just research purposes. Will help make the
UIDAI (and other GoI) websites accessible to a much larger community.

## Helm Charts for Self-Hosting

I self-host a lot of my services, and it would be great to take my existing services, and convert them
to compatible Helm Charts that others can re-use. Basically: Helm Charts for Self-Hosting.

The input for these would be the terraform code at https://git.captnemo.in/nemo/nebula

## Fake Paytm Payment

A fake webapp that goes fullscreen and does the following:

1.  Has a QR Code Scanner and OCR Scanner that scans Paytm QR Codes
2.  Lets users enters any amount
3.  And gives a green check to say that the payment was successful.

Why: To demonstrate to Paytm that they need to educate their merchants better about authenticating payments.

:warning: **Likely illegal to distribute.**

Update: There are already two such apps on the Play Store. However, they don't work any more since they were based on the old UI Scheme. See [@Oxyenyos's PR](https://github.com/captn3m0/ideas/pull/10) for some more details.

## Automated Personal Finance

:sparkles:

A personal finance application that tracks things automatically, but saves all data on your systems.

A overwhelmingly large percentage of my finances are online or tracked somewhere digitally. What is ditigal can be automated, but without any of the SMS-sniffing applications that currently clutter the market. The idea is to have a simple cross-platform application that:

1.  Embeds a web-browser that lets you login to various online services.
2.  Scrapes the order/payment history from these sites regularly.
3.  And provides you with monthly budget/finance history that you can use to track your spending.

For bonus points, figure out a way to track card expenditure. The very minimum services required would be:

1.  Uber (Has an API)
2.  Splitwise (Has a API)
3.  Paytm (Doesn't have API, but the website backend is very much a API)
4.  Amazon

I've tried something similar before: [captn3m0/gringotts](https://github.com/captn3m0/gringotts), but I made a few mistakes:

1.  Made it a ruby-command line application.
2.  Made it output YAML.

A few related projects:

-   [Praseetha-KR/billfold](https://github.com/Praseetha-KR/billfold)
-   [alexjv89/cashflowy](https://github.com/alexjv89/cashflowy) - Might be worth using this as core.

If I were to try it again, I'd ensure a few things:

1.  GUI first, with a great UX.
2.  Cross platform, but I'd priritize Mac if necessary.
3.  Save all data in [plaintextaccount](https://plaintextaccounting.org) compatible files. This would let people use other tools on top of this.

## UPI on Desktop

:sparkles:

A clean-room reverse engineered implementation of the NPCI Common Library.

Every UPI-supported app works using the NPCI Common Library, which takes care of some crucial details:

-   MPIN Entry
-   Debit Card Entry for first time registration

Before encrypting those and passing them to the application code.

This project envisions to reverse-engineer the NPCI Common Library. This would let people:

-   Build Desktop implementation of any UPI Application
-   Build BHIM on older devices

This is a necessary step, but not the final step since that would be reversing the web APIs that common UPI apps use.

---

## Licence

This work is licensed under a [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/). Feel free to contribute via Pull Requests, or discuss ideas in Issues. Also feel free to use these ideas in making the Next Big Thing. I promise to send you a postcard if you ship one of these.

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](http://creativecommons.org/licenses/by/4.0/)

There is a list of other similar lists-of-ideas at [SIMILAR.md](SIMILAR.md)
