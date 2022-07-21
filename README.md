> There's no such thing as an original idea. Every idea worth having has been
> had thousands of times already.
>
> - [swombat](https://news.ycombinator.com/item?id=250793)

**Legend**

- ✨ - Favorite Ideas. I really like this, and you could possible build a
  company of some of these.
- 🎁 - I'd love to help you build this, consider this like a bounty
- 🚀 Someone (might be me) built this!
- 🚧 There is a work-in-progress implementation.
- 👩‍🔬 Research ideas

:heart: You'll get a personal postcard from me for building something on this
list

The :poop: ideas (I thought might work at one point, but no longer consider
worth building) are at [BADIDEAS.md](BADIDEAS.md).

<!-- npx doctoc --github --update-only --maxlevel 2 README.md -->
<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [Introduction](#introduction)
- [✨🎁 Collaborative Bookmarking](#-collaborative-bookmarking)
- [🚀Lightspeed for Chrome](#lightspeed-for-chrome)
- [Facebook Analytics](#facebook-analytics)
- [API for Workflowy](#api-for-workflowy)
- [Email on top of keybase](#email-on-top-of-keybase)
- [🚀 Newsletters for GitHub](#-newsletters-for-github)
- [🚀Hacking via OAauth tokens](#hacking-via-oaauth-tokens)
- [Pluggable Notify Daemon for Linux](#pluggable-notify-daemon-for-linux)
- [🚀Telegram To RSS](#telegram-to-rss)
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
- [🎁 Mars: Terraform Remote HTTP Backend with End-to-End encryption](#-mars-terraform-remote-http-backend-with-end-to-end-encryption)
- [🎁 iOS OPDS File Provider](#-ios-opds-file-provider)
- [iOS \*sonic File Provider](#ios-%5Csonic-file-provider)
- [collaborative-bookmarking](#collaborative-bookmarking)
- [👩‍🔬 Boardgame AI Gym](#%E2%80%8D-boardgame-ai-gym)
- [🎁 ✨ Green/Yellow Pages](#--greenyellow-pages)
- [🎁 communities browser extension](#-communities-browser-extension)
- [onioncannon](#onioncannon)
- [🚀PyPi Notifier](#pypi-notifier)
- [codenames-ai](#codenames-ai)
- [Verifiable Code Execution on Cloud](#verifiable-code-execution-on-cloud)
- [Browser Extension: youtube-cue](#browser-extension-youtube-cue)
- [Stitch EPUBs from multiple URLs](#stitch-epubs-from-multiple-urls)
- [OpenAPI Specification Generator from HTTP Archives](#openapi-specification-generator-from-http-archives)
- [Open ISIN API](#open-isin-api)
- [A Survey of the Electron Supply Chain](#a-survey-of-the-electron-supply-chain)
- [2fa.wiki](#2fawiki)
- [Boardgame Rulebook Translation Guide :construction:](#boardgame-rulebook-translation-guide-construction)
- [Probe the Great Indian Firewall](#probe-the-great-indian-firewall)
- [A Practical MRNL Service (Mobile Number Revocation List)](#a-practical-mrnl-service-mobile-number-revocation-list)
- [Licence](#licence)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Introduction

This is a open repository of personal ideas. Some of these are based on personal
interactions, bug reports, and discussions I've had with lots of people. I've
tried to give credit wherever possible. I also try to reference similar/existing
projects that might relate to the idea, so if you know of something that is
interesting in that space, file a PR or send me a link.

The emojis are just indicative. Make something people want is the YC motto, but
sometimes you must make something for no good reason other than "just because".

## ✨🎁 Collaborative Bookmarking

There are a dozen bookmarking services out there, many of them quite well done.
However, most services are focused on the idea that bookmarking is a lone-person
habit, which someone does in isolation.

I've often described the idea as "dropbox for bookmarks". The core concept is to
allow a bookmarking "tag/folder" to be shared with another user, two-way. This
means any of the shared members can add/remove bookmarks from that folder. All
updates (addition/deletion/edits) are notified to every member in the group.

Bookmarking for Teams, in essence. Some good alternatives are
[listed in this quora answer](https://www.quora.com/Hello-What-are-the-best-web-apps-for-sharing-bookmarks-across-a-team),
which you should read and follow if you're interested in this.

I've described this idea somewhat better in a chat log at
[collaborative-bookmark.md](collaborative-bookmark.md) Google Spaces did some
nice work here, but the product was shut down within an year of launch.

## 🚀Lightspeed for Chrome

[Lightspeed](https://www.youtube.com/watch?v=wLnSLFrQDG8) is an experimental UI
design (not implemented) for Firefox that focuses on making the New Tab page
more functional by giving the browser a decent way to search across bookmarks,
open tabs, and history.

It is a pretty neat idea (see the video linked above). My first thought on
seeing the video was that most of that stuff could be done using the Chrome APIs
for Chrome as well. Chrome does offer a way for an extension to override the new
tab page, after all.

The discussion on [HN](https://news.ycombinator.com/item?id=8151271) is also
very good.

_Update_: There is some progress on the WebExtension porting of Lightspeed,
given the recent Firefox updates. With this in place, it should be relatively
easier to port the webextension version to Chrome itself.

_Update_: [@tallpants](https://github.com/tallpants) made this:
https://github.com/tallpants/lightspeed

## Facebook Analytics

I like the analytics that WolframAlpha provides for Facebook. Except that they
are not really that useful. I'd like an easy query interface that let me
"filter" data points, and get back open-data via the Graph API. This means, for
eg, getting the most liked music artist among a subset of my friends. The
interface I'm thinking of right now is like Gapminder, which allows you to
"play" the dataset as it evolves over time.

A recommendation engine built on top of my facebook data is a good idea, I
think.

## API for Workflowy

Workflowy is a cool tool that I use for note-taking. It allows infinitely nested
lists with @mention and #hashtag support. One thing it lacks currently is API
for me to access my own data. I think workflowy is a great tool that could
become a lot better if there were a way for developers to hook into it. (For
example using workflowy as a data-backend for a todo-app).

## Email on top of keybase

Keybase has a cool API. I wonder if its possible to build an actual email
service on top of keybase?

The original idea was from before Keybase had a chat feature, and I wanted to
build an email service that used keybase to send and receive messages. Would
have turned out similar to Keybase Chat.

How I'd approach it today is to use Keybase Social Graph for encrypting emails
and make it easier via plugins/extensions. The ideal flow would be:

Use the Keybase Social Graph for encrypting emails and make it easier via
plugins/extensions. The ideal flow would be:

1.  Login to GMail
2.  Compose an email to me@captnemo.in
3.  Extension pops up: "Hey, looks like this user is on Keybase already as
    keybase.io/captn3m0. Would you like to encrypt this email?
4.  If user clicks yes, do a keybase auth and follow the user as well, perhaps?
    (not sure if possible)
5.  Also give user an option to "Encrypt all emails sent to users with more than
    X followers)" or something similar...

Doing the same thing on the receiving side is trickier though, but I like the
idea of using Keybase to discover anyone's public keys instead of the standard
Web of Trust.

A Keybase plugin for Thunderbird would be similar in scope.

## 🚀 Newsletters for GitHub

A lot of github project owners would like to send out newsletters to all of
their stargazers. However, GitHub doesn't provide anything for that. An easy way
would be to integrate StarGazers with MailChimp, making sure that people can
unstar a project to unsubscribe from the mailing list.

Only the repo owners and collaborators (maybe) should have access to sending out
newsletters. For bonus points, you can replace mailchimp with your own solution.

This could even be monetized slightly for paying off your server costs:
newsletter access for projects with >1k stars (the mailers that would cost you
money) cost money to the repo owner as well.

So a tiny python package pays nothing to update its users about a new release,
but if Angular team wants to send out an update, that gets paid.

And finally, this should automatically subscribe you to any new GitHub releases
in any project you have starred. This is a missing feature that I think can be
best implemented by a third-party for now.

_Update_: GitHub now supports
[watching releases](https://github.blog/changelog/2018-11-27-watch-releases/).

There are **lots** of related projects in this thread:
https://github.com/isaacs/github/issues/410

## 🚀Hacking via OAauth tokens

While pen-testing, once you've gained access to the target, it is often
necessary to install a backdoor to mantain the access. While this is easily done
in case of root access to the machine, this is not that easy if the target is an
email account, lets say.

Many online services today (with data of considerable value) offer developers
programmatic access to their data by use of APIs, which are usually
authenticated via OAuth tokens. What I intend to build is a suite of
applications (or a single large one) that allow you to use the application as
another user, just by setting up an access token.

While this is certainly possible with existing tools (such as the Facebook Graph
API Explorer), it is cumbersome and not user-friendly. The application will
mimic the interface, usability, and looks of the actual application to let you
maintain access easily enough.

### But OAuth tokens can be revoked

That is a good point, but one that fails in practice. A password change in most
services does not trigger an automatic token revocation because that would leave
a lot of developers and users unhappy. However, neither does any service warn
you to check your approved applications (especially after a hacking attempt).

### Procedure

1.  You gain access to someone's account.
2.  You create an application (using a fake account or the victim's own account,
    so its not tied back to you)
3.  You setup our app (direct deploy to Heroku)
4.  You configure the app with the application credentials (app id, secret key)
5.  You authenticate the victim's account against the app
6.  You use the application to access the user's account

The account access will continue till the victim checks his/her approved
applications.

🚀 I made this: <https://github.com/captn3m0/amon>

## Pluggable Notify Daemon for Linux

Not another window manager daemon, because lots of them already exist and there
are already good APIs in almost all languages that make it easy to integrate
with all of them. However, Linux DEs are still missing an easy way for me to get
notifications about the thousands of little different things (such as build
notifications).

The idea is to have a simple config where you can connect your bazillian
accounts via OAuth, and we will poll all your accounts and give you "clickable"
notifications for each of them. (GMail notifications might open your mail client
if you click reply)

Keep it pluggable, otherwise its of no use.

## 🚀Telegram To RSS

This is fairly well solved at this point, see the following:

- [There is an existing `TelegramBridge` in RSS-Bridge](https://github.com/RSS-Bridge/rss-bridge/pull/1175)
  that just scrapes telegram HTML. I've enabled it on my RSS-bridge server, so
  you can try it out at <https://rss-bridge.bb8.fun/#bridge-Telegram>.
- https://docs.rsshub.app/en/social-media.html#telegram
- https://t.me/Channel2RSSBot
- https://notifier.in/ (Free for 100 messages/month, paid beyond that)
- https://tg.i-c-a.su/ (Free with reasonable rate-limits)

You can see a archive of the original idea at
[telegram-to-rss.md](telegram-to-rss.md).

## 🎁 Disable Local Fonts Extension

A simple browser extension for web developers that disable local fonts from
loading. Alternatively, it raises a grave warning if a web-font was bypassed for
a local font. This is helpful if you are a developer:

- And have some specific font installed locally (say Font Awesome)
- And are developing a website that uses that font locally
- And forget to include the Font in your stylesheet

The page continues to function normally in your development setup, but breaks in
production.

Based upon this
[chrome bug request](https://bugs.chromium.org/p/chromium/issues/detail?id=472136),
which asks for this feature.

I came to know about this because
[of a comment](https://github.com/captn3m0/disable-web-fonts/issues/1#issuecomment-143665811)
on my "disable-web-fonts" extension, which does the opposite. This might be
handy for people who want to make sure that web-fonts are working fine for all
users.

## Arch Linux Package Build System

The Arch Linux User Repository is great. Except, a lot of packages rely on
building-from-source since no binary releases are available. However, the build
steps for these packages work very well, resulting in a working build. The idea
is to create a AUR build server that takes in a AUR package name as input (it
can have a whitelist of such packages), runs it in a docker container, and
outputs a generated package file (`tar.xz`) that can then be directly installed
on any machine.

This has some security concerns, mainly how do you trust a binary package an
external server built?

Planning to solve this with attempting reproducible builds, and publishing
everything. You can audit any build artifact whenever you wish. I'll likely just
use the Docker ArchLinux image and build against that.

Moreover, the primary audience for this would be me. I would really like to get
packages that can be installed much faster because I don't have to build them. I
can just have a script that instead downloads the latest build from the server
instead of AUR and then just installs the package instead of building it
locally.

Take a look at https://github.com/Foxboron/arch-auto-build, which is a very
similar attempt at this idea.

This is already handled by the Arch Build System (albeit without Docker). Using
that might be a better idea.

You should also look at the https://github.com/archlinux/rebuilder/ if this
looks interesting.

## Hacker News Research Bot

A bot that posts paper abstracts and links to PDF whenever a paper referencing a
research paper is posted to Hacker News. Most scicomm posts that make it to HN
almost always have a primary paper reference, and someone ends up posting the
paper abstract along with a link to Arxiv or SciHub usually. A bot that
automates this for all HN submissions would be a fun project.

_Update_: Someone did this! See
[@randomdrake's comments on HN](https://news.ycombinator.com/threads?id=randomdrake).

_Update 2_: The mods are not very happy with the
[abstract being posted](https://news.ycombinator.com/item?id=16330366), but the
rest should be good.

For Bonus Points: Include a link to the fermat library URL of the paper (if
available).

## 🎁 🚧 Slack Dialer

All of our company has contact numbers added on Slack, but it is cumbersome to
find someone's profile on Slack. A simple dialer application that does
OAuth-verification on your Slack profile to get a list of the entire
organization, and present a simple dialer for all the people who have contact
details added.

Interface would be a simple grid of faces, click to dial, sorted by frequency. A
simple search-as-you-type box at the top. Can also be done as a PWA to easily
make it cross-platform.

Note that this requires a Slack team with a paid account. I'll help you get a
trial so you can build this.

🚧 <https://github.com/captn3m0/slack-dialer>

## Database Conversion Toolkit using an ORM

Something that lets you switch your database between SQLite/MySQL/Postgres/...
by using an existing ORM framework to import and export out the correct
commands.

The grammar differences in most databases are taken care of by an ORM, and the
remainder is just switching your ORM to use an existing database as the source
of truth. Even a specific variant (say SQLite to MySQL) would be great to have.

Thought of this after spending a lot of time trying to migrate my Grafana/Gitea
setups from sqlite to mysql and trying every solution in
[this SO question](https://stackoverflow.com/questions/18671/quick-easy-way-to-migrate-sqlite3-to-mysql).

There are some closed solutions to this, but would like a open-source solution
that does this well.

## 🎁 Tachiyomi Headless

[Tachiyomi](https://github.com/inorichi/tachiyomi/) is a Android application
written in Kotlin that scrapes comics from various web sources. A headless
version of it would be great to have, replacing projects such as
<https://github.com/evilhero/mylar> with something much more stable.

The end goal is something that works as a "minor" (<200L) patch on top of
Tachiyomi, and does a JVM-desktop build which can be run anywhere. A sample
README would look something like:

A headless build for [tachiyomi][0] which you can run on your server on a
schedule to download comics. This downloads the comics in plain images and then
converts them to CBZ format with metadata intact. A new release is generated for
every Tachiyomi release.

Get the latest release from the [releases page][1]. Download the
`tachiyomi-headless.jar` file.

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

I :heart: RSS because it gives me the control of how to consume and read the
content. While many services provide you RSS feeds, they do not give you an easy
way to export a list of things that you follow.

For eg: Every repository on GitHub has a releases RSS feed that you can follow.
However, you need to follow each one individually. Thankfully, there is a nice
spec called OPML which is used to pass around lists of RSS feeds.

What if one could generate a OPML feed for:

1.  Releases of repos that you have starred on GitHub
2.  Authors that you follow on GoodReads
3.  Bands that you follow on BandCamp

🚀 I made a initial working demo recently for the first one, and you can check
it at <https://opml.bb8.fun>. The source code is at
<https://git.captnemo.in/nemo/opml-gen>.

Related: https://github.com/RSS-Bridge/rss-bridge (I have contributed a few
bridges to this)

## 🎁 🚧 Bangalore Events List

Similar in scope to http://webuild.sg/ or http://engineers.sg/ but for
Bangalore.

- Want to keep the name generic to support non-tech events as well
- ICS support (WeBuild.sg/cal for demo) is a must-have
- (They have a RSS feed as well!)

Domain name suggestions are welcome. Since blr doesn't have a TLD, I was
considering using `.events`.

Initial Work: https://github.com/captn3m0/gardencity.events There is also some
work from @tallpants on this at <https://github.com/tallpants/meetup2ics/>

## 🚀 Amazon Price Tracker with RSS

There are some nice open source trackers available for Price Tracking Amazon
products, but I would like to see something that generated an RSS Feed.

This could be built on top of
[RSS Bridge](https://github.com/RSS-Bridge/rss-bridge) fairly easily.
Configuration options would include:

- Min Price (Only add to feed if price is below X)
- Amazon Country/Domain (Use the specific Amazon website)
- Item Id

🚀 https://github.com/RSS-Bridge/rss-bridge/pull/741

(While the above is merged, this doesn't correctly work because it doesn't cache
the information properly).

## OPML Sync

Instead of forcing users to do manual imports of OPML feeds, let them
auto-subscribe from feeds using a dynamically generated OPML feed. This is not a
product idea by itself, more of a extension idea for existing RSS Readers.

See related discussion on the
[tt-rss forums](https://discourse.tt-rss.org/t/subscribe-to-opml/1230).

## ✨🎁 Sanskari Proxy

A lot of Indian Government websites are inaccessible on the public internet,
because they geo-fence it to within Indian Boundaries. I made a list of all
[Indian Government Websites](https://git.captnemo.in/nemo/pulse/src/branch/master/domains.csv),
and the idea is to make a Indian Proxy service that specifically works only for
the Geo-fenced Indian GoI websites.

For eg, if `uidai.gov.in` is inaccessible, hitting `uidai.gov.sanskariproxy.in`
will get you the same result, proxied via our servers.

This is not intended to be used for actual usage, just research purposes. Will
help make the UIDAI (and other GoI) websites accessible to a much larger
community.

_Update_: I made
[a version of this](https://github.com/captn3m0/sanskari-proxy), the one that
comes with the least legal issues.

## Helm Charts for Self-Hosting

I self-host a lot of my services, and it would be great to take my existing
services, and convert them to compatible Helm Charts that others can re-use.
Basically: Helm Charts for Self-Hosting.

The input for these would be the terraform code at
https://git.captnemo.in/nemo/nebula

## Fake Paytm Payment

A fake webapp that goes fullscreen and does the following:

1.  Has a QR Code Scanner and OCR Scanner that scans Paytm QR Codes
2.  Lets users enters any amount
3.  And gives a green check to say that the payment was successful.

Why: To demonstrate to Paytm that they need to educate their merchants better
about authenticating payments.

:warning: **Likely illegal to distribute.**

Update: There are already two such apps on the Play Store. However, they don't
work any more since they were based on the old UI Scheme. See
[@Oxyenyos's PR](https://github.com/captn3m0/ideas/pull/10) for some more
details.

## ✨ Automated Personal Finance

A personal finance application that tracks things automatically, but saves all
data on your systems.

A overwhelmingly large percentage of my finances are online or tracked somewhere
digitally. What is ditigal can be automated, but without any of the SMS-sniffing
applications that currently clutter the market. The idea is to have a simple
cross-platform application that:

1.  Embeds a web-browser that lets you login to various online services.
2.  Scrapes the order/payment history from these sites regularly.
3.  And provides you with monthly budget/finance history that you can use to
    track your spending.

For bonus points, figure out a way to track card expenditure. The very minimum
services required would be:

1.  Uber (Has an API)
2.  Splitwise (Has a API)
3.  Paytm (Doesn't have API, but the website backend is very much a API)
4.  Amazon

I've tried something similar before:
[captn3m0/gringotts](https://github.com/captn3m0/gringotts), but I made a few
mistakes:

1.  Made it a ruby-command line application.
2.  Made it output YAML.

A few related projects:

- [Praseetha-KR/billfold](https://github.com/Praseetha-KR/billfold)
- [alexjv89/cashflowy](https://github.com/alexjv89/cashflowy) - Might be worth
  using this as core.

If I were to try it again, I'd ensure a few things:

1.  GUI first, with a great UX.
2.  Cross platform, but I'd priritize Mac if necessary.
3.  Save all data in [plaintextaccount](https://plaintextaccounting.org)
    compatible files. This would let people use other tools on top of this.

## CardDAV on Slack

While Slack calls are great, they are not the same as a Contact Entry in your
phonebook. Because with a phonebook entry, you can make outbound calls without
having internet, and you get contact details when your colleague calls you.

The idea is to run a Slack OAuth based CardDAV server, which:

1.  Authenticates the user over OAuth
2.  Fetches the list of all users in a team
3.  Generates a CardDAV URL for the authenticated user
4.  Which can then be used by the user on their phone to sync Contacts one-way
    (From Server to Phone)

Why one-way? You don't want changes made on the Client side to be pushed to the
server.

Why CardDAV? It is an open-protocol built to exactly solve this problem.

And since you have the user's OAuth tokens, you can verify the token on every
request to ensure that it is still valid. If the token is invalid, you return an
empty Contact List, thus ensuring that users can't fetch contacts from teams
they've left.

Another cool hack this enables is that for teams on Free Plans, which supports
"Skype" field in your profile, but not Phone number, it allows you to use the
"skype" field to build contact sync which converts the field to a
mobile/telephone field as long as it is a valid telephone number.

## ✨ UPI on Desktop

A clean-room reverse engineered implementation of the NPCI Common Library.

Every UPI-supported app works using the NPCI Common Library, which takes care of
some crucial details:

- MPIN Entry
- Debit Card Entry for first time registration

Before encrypting those and passing them to the application code.

This project envisions to reverse-engineer the NPCI Common Library. This would
let people:

- Build Desktop implementation of any UPI Application
- Build BHIM on older devices

This is a necessary step, but not the final step since that would be reversing
the web APIs that common UPI apps use.

## Twitter Adventure Maker

Play your own Adventure on Twitter threads have gotten quite famous recently:

- [Being Startup CEO for a day: DON'T LET YOUR COMPANY DIE](https://twitter.com/scottburke777/status/1143356872633851906)
- [Being Beyoncé’s assistant for the day: DONT GET FIRED](https://twitter.com/CORNYASSBITCH/status/1142591156884127744)

[@ChettyArun was wondering](https://twitter.com/ChettyArun/status/1144534623642255360)
how these were even made with Twitter.

One line pitch: Make a simple webapp that uses the Twitter UI to generate Play
your own Adventures. For bonus points, add support for
[Twine](https://twinery.org/) or perhaps DNML to let people create these easily.

## Playstore RSS Feed for Version Updates

An RSS feed to follow updates on applications would be nice. Details:
https://github.com/RSS-Bridge/rss-bridge/issues/1352.

## Calendar Feed for Event Websites

Would be great if I could open my Calendar application and immediately look at
events that are happening around me. Aim is to subscribe to "Fun Events -
Bangalore (Insider)" or "Plays in Bengaluru (BookMyShow)" calendars for eg.

Insider has an API that could help with this:
https://api.insider.in/home?filterBy=go-out&city=bangalore

## SVG to PNG on the Edge

I wanted to generate SVG images based on Social Media sharing templates that
could be re-purposed as header images for any of my articles. Such a solution
would help bloggers immensely, since your Open Graph images can be easily
dynamically generated. Same goes for people with static sites. (Generating a
static SVG is much easier than generating PNG images).

If you have a magic box that converts SVG images to PNG images just before
serving them to Open Graph scrapers. You can implement such a box using
CloudFlare workers for eg.

A few more links on this:
[[a](https://fransdejonge.com/2018/03/twitter-and-facebook-dont-support-svg-yet/), [[b]](https://github.com/BreakOutEvent/breakout-frontend/issues/234),
[[c]](https://indieweb.org/The-Open-Graph-protocol#Does_not_support_SVG_images).

Think of how powerful this could be:
`<meta property="og:image" content="https://image.sv/g/https://captnemo.in/img/title-banner.svg />`

A somewhat relevant thing: https://www.bannerbear.com/. There are more details
on https://github.com/captn3m0/ideas/issues/11 if this sounds interesting.

## NammaBescom OCR/Overlay Bot

A bot that waits for tweets from
[@NammaBescom](https://twitter.com/NammaBESCOM), OCRs the image they send,
replies with the OCR version of the text, and attaches a map on the tweet with
an overlay map of all the areas that lost power in the last 24 hours.

A slightly stale version of this data is available at
https://www.bescom.org/upo/public.php in text format.

Credits: https://twitter.com/kingslyj/status/1219697117909803008

## 🎁 Mars: Terraform Remote HTTP Backend with End-to-End encryption

A fork of <https://www.terraform.io/docs/backends/types/http.html>, which
changes the configuration format to:

```hcl
terraform {
  backend "mars" {
    address = "https://mars.com/03fa43d6-adbe-4e03-8e25-ffdf8a3e456a"
    encryption_key = "${var.MARS_ENCRYPTION_KEY}"
  }
}
```

The lock/unlock address can be inferred. The service can be made public as well,
since the backend just needs to be a simple/dumb storage for blobs (back it by
S3 perhaps?)

### Why

- For casual projects, Terraform Enterprise is too much
- Separate Infrastructure for Terraform State store makes sense
- Not everyone has S3 available
- Just share your UUID and the encryption key with your teammates

### Backend

Needs to be a public good with restrictions:

1.  Reasonable Rate limits
2.  File size limits
3.  Restrict by terraform-user-agent, because why not
4.  Block unencrypted data from being stored

### Extras

- This needs to be Highly Available if folks are gonna use it
- Use NaCl for crypto
- Support a breakdown into `read_encryption_key` and `write_encryption_key` for
  key rotation
- The encryption parts can perhaps be merged to upstream

## 🎁 iOS OPDS File Provider

iOS 11 and above support browsing arbitary "cloud" filesystems using a ["File
Provider Extension"][fpe]. This allows your application to expose a arbitary
directory structure to other applications using the Files app (and file-picker
dialogs).

Common use-cases include picking files from Dropbox, GDrive, iCloud etc. Here's
a simple tutorial that demonstrates the idea:
https://www.raywenderlich.com/697468-ios-file-provider-extension-tutorial.

The idea is to build a simple app that implements a dumb OPDS browser, along
with a File Provider Extension. This magically makes all applications on your
device OPDS aware, which is a Great Thing :tm:

OPDS here is the
[open publication distribution system](https://en.wikipedia.org/wiki/OPDS),
which allows a large number of clients to access digital libraries and
publications with mostly-sane distribution and browsing semantics.

As an example, [Arxiv has a OPDS](https://arxiv-opds.herokuapp.com/) server
without any authentication. You could enter this one URL in your application
settings, and now all Arxiv PDFs are instantly browseable in your Files
application.

OPDS support search as well, but I'm not sure of File Provider Extension does,
but that would be another cool usecase. The application UI is just 2 screens:

1. List of connected OPDS Servers
2. Edit/Add screen for a OPDS Server. Includes fields for URL/Username/Password.

Brownie points for adding support for rendering ebook thumbnails, but that is
optional.

## iOS \*sonic File Provider

Similarly, the [SubSonic API](http://www.subsonic.org/pages/api.jsp) is decently
documented, reversed and re-implemented across a lot of clients. A single
application that adds support for SubSonic File Provider will allow any other
application to pick song files from a subsonic source. Not as many usecases as
picking ebooks or PDFs, but good nonetheless.

[fpe]: https://developer.apple.com/documentation/fileprovider

## collaborative-bookmarking

if you haven't used dropbox folder sync in the past, this is how it works:

you have a parent dropbox director you create subdirectories you pick a
subdirectory and you share it with people everyone with access gets the same
directory in their dropbox their edits to the directory are synced with yours
I'm skipping over conflicts for now take this to bookmarks: everyone has a
bookmark thing in their browser chrome has 2 parent directories, though ->
bookmarks, and tab bar I add bookmarks and save them in a special directory. I
get a share option in the extension against every parent level directory to
share with other people

The interface is basically:

- Coding (shared with user@example.com) [Synced]
- Books
- Projects
- Elixir (shared with person@mail.com) [Syncing]

If the other person checks their bookmarks directory, they see the same
directory and links

edits are synced as well, so you can edit bookmarks (title only) and it gets
synced back

There are lots of tools that already sync your browser bookmarks, but once you
have the base in place, you can make the "source/sink" configurable to things
like Google Save / Pockets / Pinboard etc.

## 👩‍🔬 Boardgame AI Gym

The idea is a mix of 2 things: reading research papers about Monopoly, and
playing a lot of boardgames. There is a lot of good research work around
monopoly [0] and certain card games (Poker etc), but modern board games (Catan
has a little research community) haven't been looked at much. I wanted to do
simulation-based research for modern games, but found that there is no easy
tooling available to do this.

CardWorld is "OpenAI Gym for boardgames". The complete idea is:

1. Have a board game framework in place that allows people to write rulesets for
   their favorite games. These get registered as environments in the Gym.
2. Allow anyone to submit a agent script for this environment that plays this
   game. This could be written in any language that the platform supports.
3. Have a runner system that runs these agents against each other.

The benefits I can see are these:

1. Crowdsource AI research on turn-based games. The easier it is to write a bot
   that plays Hearts, the more people will try their hand at it.
2. Improve our understanding of Card Game Modelling. There has been some
   research in this area earlier[1] involving languages specific to model this,
   but I think there is a lot of scope of improvement here.
3. Give the boardgame community the tools to simulate and understand strategies
   for modern board games. Everyone knows you must buy the Transports in
   Monopoly, but what is the optimum strategy for Settlers of Catan?

Work so far:

- https://github.com/captn3m0/sushigo/
- https://github.com/captn3m0/gothok
- https://git.captnemo.in/nemo/boardgame2vec/

## 🎁 ✨ Green/Yellow Pages

A distributed directory for spam reports.

I despise [TrueCaller][tc], the current world-leader in this space, because
their entire business model depends on users selling their data to Truecaller,
which can then make as much money from this database.

When you look at the root problem that truecaller is solving, it is a
reverse-yellow-pages directory to avoid spam calls.

To solve this:

1.  You need a way to check a number against a known spam list.
2.  You need the check to be as fast as possible.

If you want to beat TrueCaller, this check should be completely offline, to
present a significant advantage.

### API

The API has 2 endpoints:

1.  Register a number as spam.
2.  Check a number and get a YES/NO spam response.

### Spam registration

To prevent abuse, you want the client to do some proof of work before _each_
submission. Publish a hash of the input number in a ledger.

### Data Store

Maintain a layered bloom filter ([research][res]) for each of the
country-domains. We don't store the original number, though, but the hash of the
phone number in the bloom filters.

### Check

Any party can request a check by sending us a hash of the phone number (so it
doesn't really leak _much_ info) along with the country code. We want a slow
hash function but since we want this to be verifiable on the client itself, the
ideal would be that it takes \~0.25s on a average mobile device.

Once we recieve the hash, check it against all the bloom filter layers in
parallel and return the results as a score.

For eg, if we have 1000 layers (to check upto 1000 reports), return the highest
layer number that has an entry for the number.

### Ledger

The above-mentioned ledger is an easy way of ensuring verified sync with any
other party that wants to maintain the same data store.

This is not a very robust solution, and an ideal solution would be to let the
client publish on the ledger, and everyone can just pick up from the ledger.

Different entities can create different directories depending on the client
properties. For eg, if a client has reported too many spam reports, you can
reduce their contribution.

A generator might also consider the frequency of such reports, along with their
age so that recent reports are given more weightage.

The nice thing here is that, since all violations are published on the ledger,
you can re-create the directory from the ledger at any time.

### Directory

A generated directory is a compressed export of the nth layer of the bloom
filter. `n` here can be decided by the customer. So you can pick n=5, for a
high-false-negative rate.

Over time, I expect this to be standardized as high/low/medium.

### Application

The application uses a list of country codes (which it can auto-fill from the
application context) as input to download directories from various known
sources. The remainder of the application is spent on interrupting inbound calls
and adding a overlay with the call score.

### Security/Privacy concerns

While hashing is the right choice here, it still has issues. A valid phone
number may be very small and we are already recording the contry code to reduce
the size and improve directory efficiency.

See [this][solomon] for eg, where the actual phone number is just 5 digits.

Even if you use a really slow hash function, and it takes 2 seconds to hash each
number, it only takes 37 hrs _total-compute time_, which can easily be run in
parallel to guess any numbers which may have been ever entered in the ledger.

The problem here is that we want repeated numbers to hash to the same value, so
as to ensure duplicates get recorded properly.

This might be possible if all clients can store a copy of the entire ledger, but
that doesn't sound like a good idea.

However, the mere fact that a phone number is in the ledger isn't as important
as _when_ it was added.

A client should ideally add a random delay (to the tune of hours) and batch any
writes to the ledger so as to reduce chances of leak.

If A calls B, and B immediately writes A's number to the ledger, A can pretty
much guarantee that it was B who did it.

There is a counter-argument here to be made about how you want honest clients
and immediate publishing would increase transparency and hopefully get more
_actual spammers_ on the list.

Another concern is about publishing the client identifier in the ledger, since
it can lead to the network figuring your calling patterns. However, since an
entry is only added voluntarily, and doesn't really have any PII, I think it is
a reasonable tradeoff to make.

### Deregistration

Phone numbers are not people. They can be transferred, and what was a spammy
telemarketer earlier could now be your number.

There is no easy way here, other than having a "negative" entry in the ledger,
with a far higher cost attached to it.

The client should always whitelist any saved mobile numbers as well.

Another solution is to have a second "verified" ledger of some sort, where
people can verify themselves as not-a-spammer by "some means". Not sure how this
could be done in a distributed manner though.

### Cost of Computation

- Verification should be fast
- Insertions should be slow
- Client registrations should be costly

By costly, I mean the compute price, not monetary. A nice way to equalize this
would be to make a registration as hard as 10 insertions, so creating a client
and reporting 9 further times would be much more cheaper to do.

This helps in ensuring that there is still a way to counter spam reports. I'm
sure there are better ideas, though.

### Terms

_Directory_: The actual data store holding a "Yes/No" filter of whether a number
is spammy or not. _Ledger_: A blockchain or ditributed log that maintains any
reports.

### References

- You should totally read
  [Falsehoods Programmers Believe About Phone Numbers](https://github.com/googlei18n/libphonenumber/blob/master/FALSEHOODS.md)
- [bitly/dablooms](https://github.com/bitly/dablooms) - an attempt by bitly to
  solve spam problems with a layered bloom filter which is countable as well
- [scalable bloom filters](https://www.sciencedirect.com/science/article/pii/S0020019006003127)
- [A multi-layer bloom filter for duplicated URL detection](http://ieeexplore.ieee.org/document/5578947/?reload=true)

[solomon]:
  https://en.wikipedia.org/wiki/Telephone_numbers_in_the_Solomon_Islands
[res]: http://ieeexplore.ieee.org/document/5578947/?reload=true

## 🎁 communities browser extension

Every community that I meet these days wants to use its own different app to
manage things, or alternatively create its own special forum and so on.

For instance:

- The dev-s community runs its own Slack channel (which is great) but wants its
  own discussion forum.
- ReRoll Bangalore has its own WhatsApp/Telegram group (which is great again)
  but lacks a discussion forum.

The idea is to make a Chrome/Firefox extension that:

1.  lets you create a community (you get a unique id + social links you can give
    out)
2.  lets others submit their identity to the community tracker via the
    extension.

The extension has the following features:

1.  Allows you to add "communities" you belong to
2.  Allows you to add your identity handles that you own. So you can specify
    multiple twitter/reddit/facebook/HN/... accounts that you own
3.  Link communities with your identities. So you can share your reddit handle
    by joining a community.
4.  Highlight a community member while browsing the site. So if you are browsing
    hacker news and have added yourselves to the community listing, you can see
    other discussions highlighted from other members.

The entire extension lives in browser space and localstorage. The backend just
maintains a mapping of community id to profile IDs, which is synced once in a
while. A community code might be required to add yourselves to the community.

This is like Reddit flairs, but flairs only work on a single subreddit, this is
intended to work across various discussion forums.

## onioncannon

Similar to [pushjet](https://pushjet.io/), but with the following idea:

- Push all app notifications to other clients
- Add/Remove clients at will
- All traffic reaches a central server
- All traffic is encrypted at source, but the uuid of the client can be used to
  talk to them

### Use Case

- I wanted to build a simple "auto-type OTP" Chrome Extension.
- Without using pushbullet (Should be FOSS)
- Without giving my OTP to anyone else (should be E2E)
- Without having to worry about NATs and firewalls (should be a publicly hosted
  service)

Somewhat related to the idea is http://github.com/decant, which allows me to
build the "read SMS" part of it.

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

The nice thing is that you can transmit data however between these two parties,
once it is encrypted. Use GCM/pusher if you wish.

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
- packages menetioned in setup.py and requirements.txt files from my own
  projects
- Allow someone to upload a requirements.txt and use that as source
- Parse the PyPi RSS Feed to get complete updates

All the sources are merged together.

### Notifications

- Maybe have a curated twitter account that tweets about releases for the top
  10% packages.
- Create a personal RSS feed for every user
- Send out emails (configurable) for every release.
- Optional direct tweets as well?

🚀 [Dependabot](https://dependabot.com/),
[Renovate](https://github.com/renovatebot/renovate)

## codenames-ai

Codenames is a word game, and you can see the rules here:
https://czechgames.com/files/rules/codenames-rules-en.pdf

The interesting challenge in the game is word-association:grinning:

- finding a single word that
- relates to one-or-more of words in Set A (Your color)
- while staying away from words in Set B (Your opponent's color)
- and staying far far away from a single word in Set C (Assasin)

The remaining AI is much simpler: Given a word and a count,

- find the closest words from Set (A+B+C)

I think using some clustering algorithms on top of word2vec should give decent
results. Maybe GPT-3 can do this much more easily.

## Verifiable Code Execution on Cloud

A common problem in the privacy world is that when a service says: we need your
data, but promise we won't store it - you have to take them at their word. This
is a common problem. Signal for eg, hashes your contacts, and sends them to
their cloud servers to see which of your contacts are on Signal. They manage to
do that
[by relying on Intel SGX](https://signal.org/blog/private-contact-discovery/),
which signs the code running on AWS and the Signal app validating that signature
to ensure that the code that's processing your contacts isn't doing anything
nefarious.

However, there is another trusted piece of infrastructure that can be used to
achieve a slightly lower degree of trust. Here's how you do it:

1. AWS Lambda is "verifiable infrastructure". You can fetch the code and verify
   that it's the same code as what you've provided elsewhere (as a reproducible
   build for eg)
2. We create a lambda for trusted-code-execution (say collecting hashes of your
   contact list, matching them against a bloom filter). The code isn't supposed
   to log these contacts, or save them in any way. We also provide this exact
   code elsewhere, for people to validate and review.
3. You create a AWS IAM keypair that has permissions to get each revision of the
   lambda code, validate the corresponding API endpoint against this lambda.
4. Instead of using a custom-domain API Gateway, you instead use the AWS execute
   lambda endpoint (The ones that look like
   https://api-id.execute-api.region.amazonaws.com/STAGE). The request directly
   reaches the lambda - verifiably (I think).
5. Publish the keys for the AWS IAM keypair that was created above.

Anyone in the world can then call up the Lambda management API to validate the
code at any time with these credentials. If you trust AWS Lambda and IAM, there
is a verifiable trust in the code that is running on that lambda and that is
processing your contacts. If/when AWS supports Intel SGX on Lambda (or Nitro
Enclaves), additional guarantees can be provided by using that.

Lambda could quite possibly be replaced by similar services: Fargate/Cloud Run.

Links: https://news.ycombinator.com/item?id=25837281,
https://stackoverflow.com/a/65798291/368328

Not sure what the actual product here would be. Perhaps a toolkit that makes it
easy to setup such infrastructure? Perhaps a global custody chain that acts as
verifying nodes?

## Browser Extension: youtube-cue

A browser extension of https://github.com/captn3m0/youtube-cue/ would be nice,
where you could click a button on the YouTube URL for a video to download a CUE
sheet.

## Stitch EPUBs from multiple URLs

I wrote https://github.com/captn3m0/pystitcher, which does a great job with
declaratively stitching PDFs. It would be nice if something similar could be
done for EPUBs. So you create an EPUB by writing down a markdown file:

```markdown
title: Thunder and Lightning author: Scott Rain summary: Book Summary

# Thunder and Lightning

# [Cover](cover.jpg)

# [Chapter 1: Everything goes south](https://example.com/ch1.html)

# [Chapter 2: Lightning](https://example.com/ch2.html)
```

Take the input, run it through a readability engine, and generate proper EPUBs
out of it.

See some related stuff:

- I wrote [url-to-epub](https://github.com/captn3m0/url-to-epub), which works
  nicely for single-URL books.
- [percollate](https://github.com/danburzo/percollate) is a command-line tool
  that turns web pages into beautifully formatted PDF, EPUB, or HTML files.
- pandoc, obviously

## OpenAPI Specification Generator from HTTP Archives

HAR is a JSON-formatted archive file format for logging of a web browser's
interaction with a site. Lots of tools already support HAR format, including
Chrome, Firefox, Fiddler, Charles Proxy, ZAP etc. There are
[JSON schema generators](https://github.com/stoplightio/json-schema-generator)
that will take a JSON object and generate a OpenAPI schema accordingly. The
usecase is:

1. Browse around a website or mobile app, which happens to have a JSON API.
2. Save a HAR file from your browser or proxy.
3. Generate a OpenAPI Specification file.

It doesn't have to be perfect, but the following can be easily adapted for:

1. List of various routes
2. Authentication scheme

I
[wrote a few reverse-engineered OpenAPI Specifications recently](https://captnemo.stoplight.io/)
and this would have been helpful.

Edit: Found a few projects:

- [akita-cli](https://github.com/akitasoftware/akita-cli#about-this-repo)
  already supports this, but I haven't tried this yet.
- <https://github.com/dcarr178/har2openapi>

## Open ISIN API

Based on https://github.com/captn3m0/india-isin-data.

## A Survey of the [Electron](https://www.electronjs.org/) Supply Chain

Electron applications are easy to build, but hard to maintain:

- using npm means the dependency tree is limitless
- using electron means most applications are static bundles containing:
  - a full chromium runtime
  - a copy of ffmpeg
  - electron
- Chrome bugfixes take time to reach electron.
- Older versions of electrons provided a full Node.js environment in the
  renderer process.

The [process model](https://www.electronjs.org/docs/tutorial/process-model) has
improved over time, but it's not perfect. There were 3 context isolation
bypasses reported in 2020.

A survey of existing applications might be worthwhile to see what's the lag
between:

1. A bug being reported in chrome
2. A security fix in electron

reaching end users.

I did some work on it:

- <https://github.com/captn3m0/which-electron>
- <https://github.com/captn3m0/electron-fingerprints/>

## 2fa.wiki

A community maintained machine-readable wiki for information about 2fa recovery
workflows for various services. 2FA recovery workflows are often undocumented,
so this would be a good thing to document across the internet.

Having this machine-readable will be even better.

## Boardgame Rulebook Translation Guide :construction:

Translating technical guides (such as boardgame rulebooks) to Hindi is quite
tough. There should be a standard guide that documents common terms so as to
avoid confusion between various games using different translations for common
boardgaming terms.

## Probe the Great Indian Firewall

The Great Indian Firewall is what blocks Indian Government websites from being accessed outside of India. 
This is bad for multiple reasons, including accessibility, archivability, and usability. There's multiple
ways this is applied, inculding:

1. GeoDNS based blocks (DNS resolves to a blocked IP outside India)
2. IP Address based blocks (Requests from an ASN outside India are dropped)
3. Block ASNs from Hosting Service Providers

Take an existing corpus of Indian Government websites (such as [mine](https://gist.github.com/captn3m0/4f3da8f07fe884e62bfab3ac85616936))
, and probe it in multiple ways to detect differences between the
"normal response" (What you'd get from an Indian residential IP) and a "blocked response" (what you see from outside India).
Take care to account for residential v/s cloud IPs, since those are commonly blocked.

The outcome should be a self-updating report/dashboard that documents the various sites that are blocked outside India.

## A Practical MRNL Service (Mobile Number Revocation List)

**Note**: [TRAI](https://trai.gov.in/) (India's Telecom Regulator) publishes a [Mobile Number Revocation List][mrnl] every month. It consists of any mobile
numbers that were disconnected this month. The list is public, and meant to be used by Indian businesses and service providers to protect
against account takeovers once these mobile numbers are re-assigned. The list is published in JSON/Excel/PDF formats, and is accessible over
an API.

As it stands, each business must write their own code to actually use this list. A usable implementation of this list would be
some service that could do one or more of the following:

1. Publish all revocations on a public queue, such as a publically accessible SNS topic, Amazon EventBridge, or a NATS/Kafka stream. Any business can subscribe to this, and consume it easily.
2. Let any business subscribe to a webhook where such lists are published.
3. Let businesses submit their existing customer dataset on a regular basis, so you can provide targeted webhooks to each business - you only get notified if your customer is impacted.
4. A Bulk-Lookup API that takes an existing customer dataset, intersects it against this month's revocation list and returns a response of impacted customers.
5. A historic database lookup that takes customer account creation dates along with mobile numbers as input, and returns impacted customers (mobile numbers that have been revoked since the account was created). This is important because a business might already have vulnerable customers

### Security and Privacy Considerations

- You do not want to store a copy of any business's customer database - relevant for (3). Especially do not link it to any identifiable Business Name. Finding a business from the list of mobile numbers might still be trivial however (if you know a subset of users for eg).
- Support bloom filters for bulk lookup APIs to reduce the request payload.
- Look at [Private Set Intersection](https://en.wikipedia.org/wiki/Private_set_intersection) to make bulk-lookups completely anonymous (The server learns nothing about your customer dataset).
- Provide clear guidance as to what guarantees the MRNL provides, and what businesses should be doing after getting notified. This might be very important for 2FA considerations for example, and require complete account suspension in cases where the mobile number is the only customer identifier.

### Cost Considerations

* Running a public SNS/EventBridge/PubSub service with third-party subscribers has a low enough cost, since you're responsible for reasonable egress and publishing costs.
* Running webhooks at scale does get costly, due to network costs, so don't do this unless you can monetize it.

---

## Licence

This work is licensed under a
[Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).
Feel free to contribute via Pull Requests, or discuss ideas in Issues. Also feel
free to use these ideas in making the Next Big Thing. I promise to send you a
postcard if you ship one of these.

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](http://creativecommons.org/licenses/by/4.0/)

There is a list of other similar lists-of-ideas at [SIMILAR.md](SIMILAR.md)

[mrnl]: https://mnrl.trai.gov.in "Mobile Number Revocation List Portal  by TRAI"