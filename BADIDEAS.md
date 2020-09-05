# :poop:

Not all ideas are great. These are things I thought might work at one point, but no longer consider worth building. I don't remove such ideas from the repo, because I think all ideas are worth learning from.

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

## 💩Lettersafe

My notes for lettersafe are on [workflowy](https://workflowy.com/s/5439f7a9-3762-f247-3e96-4d047b5d4ce0).

The idea was to build a zero-knowledge email storage. Kinda like lavabit, with a few minor changes. After thinking about it for months, and working on it for a few days, I gave up on the idea. I understand now that server-side email encryption can never be a good idea.

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