> There's no such thing as an original idea. Every idea worth having has been had thousands of times already.
>
> -   [swombat](https://news.ycombinator.com/item?id=250793)

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [Introduction](#introduction)
- [OpenBook 💩](#openbook-)
  - [Expectations](#expectations)
  - [Features](#features)
  - [Interface](#interface)
  - [Backend](#backend)
- [💩 iStalk](#-istalk)
  - [Idea](#idea)
  - [Interface](#interface-1)
- [✨🎁 Collaborative Bookmarking](#-collaborative-bookmarking)
- [🚀Lightspeed for Chrome](#lightspeed-for-chrome)
- [Facebook Analytics](#facebook-analytics)
- [API for Workflowy](#api-for-workflowy)
- [💩Lettersafe](#lettersafe)
- [Email on top of keybase](#email-on-top-of-keybase)
- [🚀 Newsletters for GitHub](#-newsletters-for-github)
- [🚀Hacking via OAauth tokens](#hacking-via-oaauth-tokens)
  - [But OAuth tokens can be revoked](#but-oauth-tokens-can-be-revoked)
  - [Procedure](#procedure)
- [Pluggable Notify Daemon for Linux](#pluggable-notify-daemon-for-linux)
- [✨🎁 Telegram To RSS](#-telegram-to-rss)
- [🎁 Disable Local Fonts Extension](#-disable-local-fonts-extension)
- [Arch Linux Package Build System](#arch-linux-package-build-system)
- [Hacker News Research Bot](#hacker-news-research-bot)
- [🎁 🚧 Slack Dialer](#--slack-dialer)
- [Database Conversion Toolkit using an ORM](#database-conversion-toolkit-using-an-orm)
- [🎁 Tachiyomi Headless](#-tachiyomi-headless)
- [🚀 OPML Generator](#-opml-generator)
- [🎁 🚧 Bangalore Events List](#--bangalore-events-list)
- [🚀 Amazon Price Tracker with RSS](#-amazon-price-tracker-with-rss)
- [OPML Sync](#opml-sync)
- [✨🎁 Sanskari Proxy](#-sanskari-proxy)
- [Helm Charts for Self-Hosting](#helm-charts-for-self-hosting)
- [Fake Paytm Payment](#fake-paytm-payment)
- [✨ Automated Personal Finance](#-automated-personal-finance)
- [CardDAV on Slack](#carddav-on-slack)
- [✨ UPI on Desktop](#-upi-on-desktop)
- [Twitter Adventure Maker](#twitter-adventure-maker)
- [Playstore RSS Feed for Version Updates](#playstore-rss-feed-for-version-updates)
- [Calendar Feed for Event Websites](#calendar-feed-for-event-websites)
- [SVG to PNG on the Edge](#svg-to-png-on-the-edge)
- [NammaBescom OCR/Overlay Bot](#nammabescom-ocroverlay-bot)
- [💩 nofollow enforcer](#-nofollow-enforcer)
  - [Introduction](#introduction-1)
  - [Need](#need)
  - [Solution](#solution)
  - [Notes](#notes)
- [🎁 Mars: Terraform Remote HTTP Backend with End-to-End encryption](#-mars-terraform-remote-http-backend-with-end-to-end-encryption)
  - [Why](#why)
  - [Backend](#backend-1)
  - [Extras](#extras)
- [🎁 iOS OPDS File Provider](#-ios-opds-file-provider)
- [iOS \*sonic File Provider](#ios-%5Csonic-file-provider)
- [collaborative-bookmarking](#collaborative-bookmarking)
- [👩‍🔬 Boardgame AI Gym](#%E2%80%8D-boardgame-ai-gym)
- [🎁 ✨ Green/Yellow Pages](#--greenyellow-pages)
  - [API](#api)
  - [Spam registration](#spam-registration)
  - [Data Store](#data-store)
  - [Check](#check)
  - [Ledger](#ledger)
  - [Directory](#directory)
  - [Application](#application)
  - [Security/Privacy concerns](#securityprivacy-concerns)
  - [Deregistration](#deregistration)
  - [Cost of Computation](#cost-of-computation)
  - [Terms](#terms)
  - [References](#references)
- [🎁 communities browser extension](#-communities-browser-extension)
- [onioncannon](#onioncannon)
  - [Use Case](#use-case)
- [🚀PyPi Notifier](#pypi-notifier)
  - [Sources](#sources)
  - [Notifications](#notifications)
- [Licence](#licence)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Introduction

This is a open repository of personal ideas. Some of these are based on personal interactions, bug reports, and discussions I've had with lots of people. I've tried to give credit wherever possible. I also try to reference similar/existing projects that might relate to the idea, so if you know of something that is interesting in that space, file a PR or send me a link.

Some ideas are annotated with emojis:

-   ✨ - Favorite Ideas. I really like this, and you could possible build a company of some of these.
-   💩 - Not all ideas are great. These are things I thought might work at one point, but no longer consider worth building. I don't remove such ideas from the repo, because I think all ideas are worth learning from.
-   🎁 - I'd love to help you build this, consider this like a bounty. You'll get a personal postcard from me for building something on this list.
-   🚀 Someone (might be me) built this!
-   🚧 There is a work-in-progress implementation.
-   👩‍🔬 Research ideas

All of the above are just indicative. Make something people want is the YC motto, but sometimes you must make something for no good reason other than "just because".

## OpenBook 💩

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

## 💩 iStalk

This is essentially a unified profile mechanism, where a user's identity is defined by all of their activity on various networks. While this has some cool sub-ideas (like correlating activity between various networks), the most important implication that arises is that it can be a perfect tool for stalking. However, you can easily add in consent from the original profile owner to clear that concern.

### Idea

iStalk lets you "follow" a person across various networks that they belong to. Some networks, like twitter are mostly public, and can be followed very easily. But other networks (like Facebook) are harder to follow by virtue of them requiring a "connection" between the two users. iStalk makes it easier for you by using your account on that network as a proxy-connect mechanism.

Basically, you give us your access tokens, and we use them to stalk someone for you.

### Interface

A profile creation page allows you to specify as much information as you have on the person. This includes their facebook, twitter, last.fm, github usernames for eg. Each integration you want has to first be verified by you granting us (iStalk) access to your account (via OAuth).

Once a profile has been created, we will continuously long-poll the service to fetch new information as and when it becomes available. Real-time notifications are delivered to you as the person's activity is tracked.

## ✨🎁 Collaborative Bookmarking

There are a dozen bookmarking services out there, many of them quite well done. However, most services are focused on the idea that bookmarking is a lone-person habit, which someone does in isolation.

I've often described the idea as "dropbox for bookmarks". The core concept is to allow a bookmarking "tag/folder" to be shared with another user, two-way. This means any of the shared members can add/remove bookmarks from that folder.
All updates (addition/deletion/edits) are notified to every member in the group.

Bookmarking for Teams, in essence. Some good alternatives are [listed in this quora answer](https://www.quora.com/Hello-What-are-the-best-web-apps-for-sharing-bookmarks-across-a-team), which you should read and follow if you're interested in this.

I've described this idea somewhat better in a chat log at [collaborative-bookmark.md](collaborative-bookmark.md)
Google Spaces did some nice work here, but the product was shut down within an year of launch.

## 🚀Lightspeed for Chrome

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

## 💩Lettersafe

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

## 🚀 Newsletters for GitHub

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

There are **lots** of related projects in this thread: https://github.com/isaacs/github/issues/410

## 🚀Hacking via OAauth tokens

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

🚀 I made this: <https://github.com/captn3m0/amon>

## Pluggable Notify Daemon for Linux

Not another window manager daemon, because lots of them already exist and there
are already good APIs in almost all languages that make it easy to integrate with
all of them. However, Linux DEs are still missing an easy way for me to get notifications
about the thousands of little different things (such as build notifications).

The idea is to have a simple config where you can connect your bazillian accounts
via OAuth, and we will poll all your accounts and give you "clickable" notifications
for each of them. (GMail notifications might open your mail client if you click reply)

Keep it pluggable, otherwise its of no use.

## ✨🎁 Telegram To RSS

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

Related links:

- [My attempt](https://github.com/captn3m0/opengram) - didn't go anywhere because the Node.JS library wasn't feature complete.
- [MTProto Docs](https://core.telegram.org/mtproto)
- [Various Telegram client source code](https://github.com/TelegramOrg)
- [MTProto proxy](https://mtproto.co/)
- [Difference between the MTProto and Bot APIs](https://docs.pyrogram.org/topics/mtproto-vs-botapi)
- [Pyrogram](https://docs.pyrogram.org/faq#what-is-pyrogram) seems to support MTProto, so that is what I'd try next.

## 🎁 Disable Local Fonts Extension

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

You should also look at the https://github.com/archlinux/rebuilder/ if this looks interesting.

## Hacker News Research Bot

A bot that posts paper abstracts and links to PDF whenever a paper referencing a research paper is posted to Hacker News. Most scicomm posts that make it to HN almost always have a primary paper reference, and someone ends up posting the paper abstract along with a link to Arxiv or SciHub usually. A bot that automates this for all HN submissions would be a fun project.

_Update_: Someone did this! See [@randomdrake's comments on HN](https://news.ycombinator.com/threads?id=randomdrake).

_Update 2_: The mods are not very happy with the [abstract being posted](https://news.ycombinator.com/item?id=16330366), but the rest should be good.

For Bonus Points: Include a link to the fermat library URL of the paper (if available).

## 🎁 🚧 Slack Dialer

All of our company has contact numbers added on Slack, but it is cumbersome to find someone's profile on Slack. A simple dialer application that does OAuth-verification on your Slack profile to get a list of the entire organization, and present a simple dialer for all the people who have contact details added.

Interface would be a simple grid of faces, click to dial, sorted by frequency. A simple search-as-you-type box at the top. Can also be done as a PWA to easily make it cross-platform.

Note that this requires a Slack team with a paid account. I'll help you get a trial so you can build this.

🚧 <https://github.com/captn3m0/slack-dialer>

## Database Conversion Toolkit using an ORM

Something that lets you switch your database between SQLite/MySQL/Postgres/... by using
an existing ORM framework to import and export out the correct commands.

The grammar differences in most databases are taken care of by an ORM, and the remainder is just
switching your ORM to use an existing database as the source of truth. Even a specific variant
(say SQLite to MySQL) would be great to have.

Thought of this after spending a lot of time trying to migrate my Grafana/Gitea setups from
sqlite to mysql and trying every solution in [this SO question](https://stackoverflow.com/questions/18671/quick-easy-way-to-migrate-sqlite3-to-mysql).

There are some closed solutions to this, but would like a open-source solution that does this well.

## 🎁 Tachiyomi Headless

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

## 🚀 OPML Generator

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

🚀 I made a initial working demo recently for the first one, and you can check it at
<https://opml.bb8.fun>. The source code is at <https://git.captnemo.in/nemo/opml-gen>.

Related: https://github.com/RSS-Bridge/rss-bridge (I have contributed a few bridges to this)

## 🎁 🚧 Bangalore Events List

Similar in scope to http://webuild.sg/ or http://engineers.sg/ but for Bangalore.

-   Want to keep the name generic to support non-tech events as well
-   ICS support (WeBuild.sg/cal for demo) is a must-have
-   (They have a RSS feed as well!)

Domain name suggestions are welcome. Since blr doesn't have a TLD, I was considering using `.events`.

Initial Work: https://github.com/captn3m0/gardencity.events There is also some work from @tallpants on this at <https://github.com/tallpants/meetup2ics/>

## 🚀 Amazon Price Tracker with RSS

There are some nice open source trackers available for Price Tracking Amazon products,
but I would like to see something that generated an RSS Feed.

This could be built on top of [RSS Bridge](https://github.com/RSS-Bridge/rss-bridge)
fairly easily. Configuration options would include:

-   Min Price (Only add to feed if price is below X)
-   Amazon Country/Domain (Use the specific Amazon website)
-   Item Id

🚀 https://github.com/RSS-Bridge/rss-bridge/pull/741

(While the above is merged, this doesn't correctly work because it doesn't cache the information properly).

## OPML Sync

Instead of forcing users to do manual imports of OPML feeds, let them
auto-subscribe from feeds using a dynamically generated OPML feed. This is not
a product idea by itself, more of a extension idea for existing RSS Readers.

See related discussion on the [tt-rss forums](https://discourse.tt-rss.org/t/subscribe-to-opml/1230).

## ✨🎁 Sanskari Proxy

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

## ✨ Automated Personal Finance

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

## CardDAV on Slack

While Slack calls are great, they are not the same as a Contact Entry in your phonebook.
Because with a phonebook entry, you can make outbound calls without having internet, and
you get contact details when your colleague calls you.

The idea is to run a Slack OAuth based CardDAV server, which:

1.  Authenticates the user over OAuth
2.  Fetches the list of all users in a team
3.  Generates a CardDAV URL for the authenticated user
4.  Which can then be used by the user on their phone to sync Contacts one-way (From Server to Phone)

Why one-way? You don't want changes made on the Client side to be pushed to the server.

Why CardDAV? It is an open-protocol built to exactly solve this problem.

And since you have the user's OAuth tokens, you can verify the token on every request to ensure that it is
still valid. If the token is invalid, you return an empty Contact List, thus ensuring that users can't fetch contacts
from teams they've left.

Another cool hack this enables is that for teams on Free Plans, which supports "Skype" field in your profile, but not Phone number, it allows you to use the "skype" field to build contact sync which converts the field to a mobile/telephone field as long as it is a valid telephone number.

## ✨ UPI on Desktop

A clean-room reverse engineered implementation of the NPCI Common Library.

Every UPI-supported app works using the NPCI Common Library, which takes care of some crucial details:

-   MPIN Entry
-   Debit Card Entry for first time registration

Before encrypting those and passing them to the application code.

This project envisions to reverse-engineer the NPCI Common Library. This would let people:

-   Build Desktop implementation of any UPI Application
-   Build BHIM on older devices

This is a necessary step, but not the final step since that would be reversing the web APIs that common UPI apps use.

## Twitter Adventure Maker

Play your own Adventure on Twitter threads have gotten quite famous recently:

- [Being Startup CEO for a day:
DON'T LET YOUR COMPANY DIE](https://twitter.com/scottburke777/status/1143356872633851906)
- [Being Beyoncé’s assistant for the day: DONT GET FIRED](https://twitter.com/CORNYASSBITCH/status/1142591156884127744)

[@ChettyArun was wondering](https://twitter.com/ChettyArun/status/1144534623642255360) how these were even made with Twitter.

One line pitch: Make a simple webapp that uses the Twitter UI to generate Play your own Adventures. For bonus points, add support for [Twine](https://twinery.org/) or perhaps DNML to let people create these easily.

## Playstore RSS Feed for Version Updates

An RSS feed to follow updates on applications would be nice. Details: https://github.com/RSS-Bridge/rss-bridge/issues/1352.

## Calendar Feed for Event Websites

Would be great if I could open my Calendar application and immediately look at events that are happening around me. Aim is to subscribe to "Fun Events - Bangalore (Insider)" or "Plays in Bengaluru (BookMyShow)" calendars for eg.

Insider has an API that could help with this: https://api.insider.in/home?filterBy=go-out&city=bangalore

## SVG to PNG on the Edge

I wanted to generate SVG images based on Social Media sharing templates that could be re-purposed as header images for any of my articles. Such a solution would help bloggers immensely, since your Open Graph images can be easily dynamically generated. Same goes for people with static sites. (Generating a static SVG is much easier than generating PNG images).

If you have a magic box that converts SVG images to PNG images just before serving them to Open Graph scrapers. You can implement such a box using CloudFlare workers for eg.

A few more links on this: [[a](https://fransdejonge.com/2018/03/twitter-and-facebook-dont-support-svg-yet/), [[b]](https://github.com/BreakOutEvent/breakout-frontend/issues/234), [[c]](https://indieweb.org/The-Open-Graph-protocol#Does_not_support_SVG_images).

Think of how powerful this could be: `<meta property="og:image" content="https://image.sv/g/https://captnemo.in/img/title-banner.svg />`

A somewhat relevant thing: https://www.bannerbear.com/. There are more details on https://github.com/captn3m0/ideas/issues/11 if this sounds interesting.

## NammaBescom OCR/Overlay Bot

A bot that waits for tweets from [@NammaBescom](https://twitter.com/NammaBESCOM), OCRs the image they send, replies
with the OCR version of the text, and attaches a map on the tweet with an overlay map of all the areas that lost power
in the last 24 hours.

A slightly stale version of this data is available at https://www.bescom.org/upo/public.php in text format.

Credits: https://twitter.com/kingslyj/status/1219697117909803008

## 💩 nofollow enforcer

### Introduction

Read [What is rel=nofollow](https://support.google.com/webmasters/answer/96569?hl=en) if you don't know what that is.

The above link has the following specific snippet:

> If you want to recognize and reward trustworthy contributors, you could decide to automatically or manually remove the nofollow attribute on links posted by members or users who have consistently made high-quality contributions over time.

However, this is something that is not even attempted by the majority of large user-generated content websites such as medium, quora or even wikipedia. This is an attempt to fix this problem. [Wikipedia](https://meta.wikimedia.org/wiki/Nofollow) had a lot of discussion on this topic before enabling nofollow on all external links in 2007.

### Need

-   rel=nofollow saves you from spam
-   it improves the quality of content
-   it reduces the quality of backlinks

We need a reliable way that balances these two approaches. Something that:

-   detects low quality link spam and marks those links as nofollow
-   detects high quality links as good and let those be followed by search engines

For the links that fall in the middle, ie the ones we aren't so sure about we can either play safe and mark them as nofollow or specify a threshold score that must be matched before we unmark them.

### Solution

-   StackOverflow is one of the few websites that has even attempted to solve [this issue](http://meta.stackexchange.com/questions/111279/remove-nofollow-on-links-deemed-reputable). Their solution involves a lot of metadata they already have about the link (such as answer/comment score, votes, age etc) and they use that to mark a link as reputed.

Their approach is closed, so as to dissuade spammers from understanding it and working around it.

The general idea is to build a machine learning system that takes in a piece of content along with some optional metadata (such as authorship information) and then uses it to mark each link in the content as reputed/nofollow.

### Notes

_These are free-flow notes about the problem/solution/idea._

-   Training Data: Since so many sites already have heaps of user generated content, we can use their data (stackoverflow, wikipedia provide dumps) to get good quality links.
-   Reputed Sites: A very quick way to get off the ground would be to mark sources as reputed, such as wikipedia, new york times etc.
-   Accuracy: As a very basic check, we could use StackOverflow dataset (since it is partially nofollow) to check our own accuracy against their implementation.
-   Metadata: Will have to consider some metadata (such as authorship) along with the content itself, so as to improve spam accuracy. For instance, if the same user is posting too many links in a short time, we might mark future attempts as spam.
-   We could use akismet partially as a heuristic for partial content.
-   The idea is to build an API quite similar to akismet that can be embedded as plugins in content sites like wordpress and wikis.
-   We should also take care to actually check the link itself. For instance, the original link might point to some dummy site, but redirect to a spam website. Google would follow the redirect while crawling, and land up on the spam site if we are not careful.


## 🎁 Mars: Terraform Remote HTTP Backend with End-to-End encryption

A fork of <https://www.terraform.io/docs/backends/types/http.html>, which changes the configuration format to:

```hcl
terraform {
  backend "mars" {
    address = "https://mars.com/03fa43d6-adbe-4e03-8e25-ffdf8a3e456a"
    encryption_key = "${var.MARS_ENCRYPTION_KEY}"
  }
}
```

The lock/unlock address can be inferred. The service can be made public as well, since the backend just needs to be a simple/dumb storage for blobs (back it by S3 perhaps?)

### Why

-   For casual projects, Terraform Enterprise is too much
-   Separate Infrastructure for Terraform State store makes sense
-   Not everyone has S3 available
-   Just share your UUID and the encryption key with your teammates

### Backend

Needs to be a public good with restrictions:

1.  Reasonable Rate limits
2.  File size limits
3.  Restrict by terraform-user-agent, because why not
4.  Block unencrypted data from being stored

### Extras

-   This needs to be Highly Available if folks are gonna use it
-   Use NaCl for crypto
-   Support a breakdown into `read_encryption_key` and `write_encryption_key` for key rotation
-   The encryption parts can perhaps be merged to upstream

## 🎁 iOS OPDS File Provider

iOS 11 and above support browsing arbitary "cloud" filesystems using a ["File Provider Extension"][fpe]. This allows your application to expose a arbitary directory structure to other applications using the Files app (and file-picker dialogs).

Common use-cases include picking files from Dropbox, GDrive, iCloud etc. Here's a simple tutorial that demonstrates the idea: https://www.raywenderlich.com/697468-ios-file-provider-extension-tutorial.

The idea is to build a simple app that implements a dumb OPDS browser, along with a File Provider Extension. This magically makes all applications on your device OPDS aware, which is a Great Thing :tm:

OPDS here is the [open publication distribution system](https://en.wikipedia.org/wiki/OPDS), which allows a large number of clients to access digital libraries and publications with mostly-sane distribution and browsing semantics.

As an example, [Arxiv has a OPDS](https://arxiv-opds.herokuapp.com/) server without any authentication. You could enter this one URL in your application settings, and now all Arxiv PDFs are instantly browseable in your Files application.

OPDS support search as well, but I'm not sure of File Provider Extension does, but that would be another cool usecase. The application UI is just 2 screens:

1. List of connected OPDS Servers
2. Edit/Add screen for a OPDS Server. Includes fields for URL/Username/Password.

Brownie points for adding support for rendering ebook thumbnails, but that is optional.

## iOS \*sonic File Provider

Similarly, the [SubSonic API](http://www.subsonic.org/pages/api.jsp) is decently documented, reversed and re-implemented across a lot of clients. A single application that adds support for SubSonic File Provider will allow any other application to pick song files from a subsonic source. Not as many usecases as picking ebooks or PDFs, but good nonetheless.

[fpe]: https://developer.apple.com/documentation/fileprovider

## collaborative-bookmarking

if you haven't used dropbox folder sync in the past, this is how it works:

you have a parent dropbox director
you create subdirectories
you pick a subdirectory
and you share it with people
everyone with access gets the same directory in their dropbox
their edits to the directory are synced with yours
I'm skipping over conflicts for now
take this to bookmarks: everyone has a bookmark thing in their browser
chrome has 2 parent directories, though -> bookmarks, and tab bar
I add bookmarks and save them in a special directory. I get a share option in the extension against every parent level directory
to share with other people


The interface is basically:

- Coding (shared with user@example.com) [Synced]
- Books
- Projects
- Elixir (shared with person@mail.com) [Syncing]

If the other person checks their bookmarks directory, they see the same directory and links

edits are synced as well, so you can edit bookmarks (title only) and it gets synced back

There are lots of tools that already sync your browser bookmarks, but once you have the base in place,
you can make the "source/sink" configurable to things like Google Save / Pockets / Pinboard etc.

## 👩‍🔬 Boardgame AI Gym

The idea is a mix of 2 things: reading research papers about Monopoly, and playing a lot of boardgames. There is a lot of good research work around monopoly [0] and certain card games (Poker etc), but modern board games (Catan has a little research community) haven't been looked at much. I wanted to do simulation-based research for modern games, but found that there is no easy tooling available to do this.

CardWorld is "OpenAI Gym for boardgames". The complete idea is:

1. Have a board game framework in place that allows people to write rulesets for their favorite games. These get registered as environments in the Gym.
2. Allow anyone to submit a agent script for this environment that plays this game. This could be written in any language that the platform supports.
3. Have a runner system that runs these agents against each other.

The benefits I can see are these:

1. Crowdsource AI research on turn-based games. The easier it is to write a bot that plays Hearts, the more people will try their hand at it.
2. Improve our understanding of Card Game Modelling. There has been some research in this area earlier[1] involving languages specific to model this, but I think there is a lot of scope of improvement here.
3. Give the boardgame community the tools to simulate and understand strategies for modern board games. Everyone knows you must buy the Transports in Monopoly, but what is the optimum strategy for Settlers of Catan?

Work so far:

- https://github.com/captn3m0/sushigo/
- https://github.com/captn3m0/gothok
- https://git.captnemo.in/nemo/boardgame2vec/

## 🎁 ✨ Green/Yellow Pages

A distributed directory for spam reports.

I despise [TrueCaller][tc], the current world-leader in this space,
because their entire business model depends on users selling their data
to Truecaller, which can then make as much money from this database.

When you look at the root problem that truecaller is solving,
it is a reverse-yellow-pages directory to avoid spam calls.

To solve this:

1.  You need a way to check a number against a known spam list.
2.  You need the check to be as fast as possible.

If you want to beat TrueCaller, this check should be completely offline,
to present a significant advantage.

### API

The API has 2 endpoints:

1.  Register a number as spam.
2.  Check a number and get a YES/NO spam response.

### Spam registration

To prevent abuse, you want the client to do some
proof of work before _each_ submission. Publish
a hash of the input number in a ledger.

### Data Store

Maintain a layered bloom filter ([research][res])
for each of the country-domains. We don't store
the original number, though, but the hash of the
phone number in the bloom filters.

### Check

Any party can request a check by sending us a
hash of the phone number (so it doesn't really
leak _much_ info) along with the country code.
We want a slow hash function but since we
want this to be verifiable on the client itself,
the ideal would be that it takes \~0.25s on a
average mobile device.

Once we recieve the hash, check it against all
the bloom filter layers in parallel and
return the results as a score.

For eg, if we have 1000 layers (to check upto
1000 reports), return the highest layer number
that has an entry for the number.

### Ledger

The above-mentioned ledger is an easy way of
ensuring verified sync with any other party
that wants to maintain the same data store.

This is not a very robust solution, and an
ideal solution would be to let the client
publish on the ledger, and everyone
can just pick up from the ledger.

Different entities can create different
directories depending on the client
properties. For eg, if a client has
reported too many spam reports,
you can reduce their contribution.

A generator might also consider
the frequency of such reports, along
with their age so that recent reports
are given more weightage.

The nice thing here is that, since
all violations are published on the
ledger, you can re-create the directory
from the ledger at any time.

### Directory

A generated directory is a compressed
export of the nth layer of the bloom
filter. `n` here can be decided by
the customer. So you can pick n=5,
for a high-false-negative rate.

Over time, I expect this to be standardized
as high/low/medium.

### Application

The application uses a list
of country codes (which it can
auto-fill from the application
context) as input to download
directories from various known
sources. The remainder of the
application is spent on interrupting
inbound calls and adding a overlay
with the call score.

### Security/Privacy concerns

While hashing is the right choice here,
it still has issues. A valid phone number
may be very small and we are already
recording the contry code to reduce
the size and improve directory efficiency.

See [this][solomon] for eg, where the
actual phone number is just 5 digits.

Even if you use a really slow hash function,
and it takes 2 seconds to hash each
number, it only takes 37 hrs _total-compute time_,
which can easily be run in parallel to guess
any numbers which may have been ever entered
in the ledger.

The problem here is that we want repeated
numbers to hash to the same value, so as
to ensure duplicates get recorded properly.

This might be possible if all clients
can store a copy of the entire ledger,
but that doesn't sound like a good idea.

However, the mere fact that a phone
number is in the ledger isn't
as important as _when_ it was added.

A client should ideally add a random
delay (to the tune of hours) and batch
any writes to the ledger so as to
reduce chances of leak.

If A calls B, and B immediately
writes A's number to the ledger,
A can pretty much guarantee
that it was B who did it.

There is a counter-argument here to be made
about how you want honest clients and
immediate publishing would increase
transparency and hopefully get more
_actual spammers_ on the list.

Another concern is about publishing the client
identifier in the ledger, since it can
lead to the network figuring your
calling patterns. However, since an entry
is only added voluntarily, and doesn't really
have any PII, I think it is a reasonable
tradeoff to make.

### Deregistration

Phone numbers are not people. They can
be transferred, and what was a spammy
telemarketer earlier could now be your number.

There is no easy way here, other than having
a "negative" entry in the ledger, with
a far higher cost attached to it.

The client should always whitelist any
saved mobile numbers as well.

Another solution is to have a second
"verified" ledger of some sort, where
people can verify themselves as not-a-spammer
by "some means". Not sure how this could be
done in a distributed manner though.

### Cost of Computation

-   Verification should be fast
-   Insertions should be slow
-   Client registrations should be costly

By costly, I mean the compute price, not monetary.
A nice way to equalize this would be to make
a registration as hard as 10 insertions, so
creating a client and reporting 9 further
times would be much more cheaper to do.

This helps in ensuring that there is still
a way to counter spam reports. I'm sure
there are better ideas, though.

### Terms

_Directory_: The actual data store holding a "Yes/No" filter of whether a number is spammy or not.
_Ledger_: A blockchain or ditributed log that maintains any reports.

### References

-   You should totally read [Falsehoods Programmers Believe About Phone Numbers](https://github.com/googlei18n/libphonenumber/blob/master/FALSEHOODS.md)
-   [bitly/dablooms](https://github.com/bitly/dablooms) - an attempt by bitly to solve spam problems with a layered bloom filter which is countable as well
-   [scalable bloom filters](https://www.sciencedirect.com/science/article/pii/S0020019006003127)
-   [A multi-layer bloom filter for duplicated URL detection](http://ieeexplore.ieee.org/document/5578947/?reload=true)

[solomon]: https://en.wikipedia.org/wiki/Telephone_numbers_in_the_Solomon_Islands
[res]: http://ieeexplore.ieee.org/document/5578947/?reload=true

## 🎁 communities browser extension

Every community that I meet these days wants to use its own different app to manage things, or alternatively create its own special forum and so on.

For instance:

-   The dev-s community runs its own Slack channel (which is great) but wants its own discussion forum.
-   ReRoll Bangalore has its own WhatsApp/Telegram group (which is great again) but lacks a discussion forum.

The idea is to make a Chrome/Firefox extension that:

1.  lets you create a community (you get a unique id + social links you can give out)
2.  lets others submit their identity to the community tracker via the extension.

The extension has the following features:

1.  Allows you to add "communities" you belong to
2.  Allows you to add your identity handles that you own. So you can specify multiple twitter/reddit/facebook/HN/... accounts that you own
3.  Link communities with your identities. So you can share your reddit handle by joining a community.
4.  Highlight a community member while browsing the site. So if you are browsing hacker news and have added yourselves to the community listing, you can see other discussions highlighted from other members.

The entire extension lives in browser space and localstorage. The backend just maintains a mapping of community id to profile IDs, which is synced once in a while. A community code might be required to add yourselves to the community.

This is like Reddit flairs, but flairs only work on a single subreddit, this is intended to work across various discussion forums.

## onioncannon

Similar to [pushjet](https://pushjet.io/), but with the following idea:

- Push all app notifications to other clients
- Add/Remove clients at will
- All traffic reaches a central server
- All traffic is encrypted at source, but the uuid of the client can be used to talk to them

### Use Case

- I wanted to build a simple "auto-type OTP" Chrome Extension.
- Without using pushbullet (Should be FOSS)
- Without giving my OTP to anyone else (should be E2E)
- Without having to worry about NATs and firewalls (should be a publicly hosted service)

Somewhat related to the idea is http://github.com/decant, which allows me to build the "read SMS" part of it.

What I envision is essentially a simple client-registration protocol:

- `[Device A]` generates a UUID.
- `[Device B]` generates a UUID.
- B generates a QR code using the UUID.
- A scans the QR code to get the UUID and pushes a sample event.
- B gets the event, and can decide to push events to A if needed.

The QR code includes:

1. The UUID of a client
2. A public key fingerprint of the PGP key of the client
3. Metadata containing:
- Public Key
- URL where the public key can be found
- Misc Client Information

Any client who scans this can now start sending encrypted data to the client.

The nice thing is that you can transmit data however between these two parties, once it is encrypted. Use GCM/pusher if you wish.


## 🚀PyPi Notifier

Problem: No way to get updates when any package I am using has a new release.

Solution:

- Sends an email when a package you are watching updates
- Get starred package list from github
- Webhooks are not possible
- PyPi -> GitHub mapping is impossible to maintain
- Parse PyPi RSS Feed
- Get list of packages updated and mail people
- Maybe parse package name from setup.py
- Allow uploading requirements.txt as well perhaps.


### Sources

Once it has your GitHub credentials:

- Starred github repos that are also on PyPi
- packages menetioned in setup.py and requirements.txt files from my own projects
- Allow someone to upload a requirements.txt and use that as source
- Parse the PyPi RSS Feed to get complete updates

All the sources are merged together.

### Notifications

- Maybe have a curated twitter account that tweets about releases for the top 10%
  packages.
- Create a personal RSS feed for every user
- Send out emails (configurable) for every release.
- Optional direct tweets as well?

🚀 [Dependabot](https://dependabot.com/), [Renovate](https://github.com/renovatebot/renovate)


---

## Licence

This work is licensed under a [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/). Feel free to contribute via Pull Requests, or discuss ideas in Issues. Also feel free to use these ideas in making the Next Big Thing. I promise to send you a postcard if you ship one of these.

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](http://creativecommons.org/licenses/by/4.0/)

There is a list of other similar lists-of-ideas at [SIMILAR.md](SIMILAR.md)
