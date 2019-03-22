# nofollow enforcer :hankey:

## Introduction

Read [What is rel=nofollow](https://support.google.com/webmasters/answer/96569?hl=en) if you don't know what that is.

The above link has the following specific snippet:

> If you want to recognize and reward trustworthy contributors, you could decide to automatically or manually remove the nofollow attribute on links posted by members or users who have consistently made high-quality contributions over time.

However, this is something that is not even attempted by the majority of large user-generated content websites such as medium, quora or even wikipedia. This is an attempt to fix this problem. [Wikipedia](https://meta.wikimedia.org/wiki/Nofollow) had a lot of discussion on this topic before enabling nofollow on all external links in 2007.

## Need

-   rel=nofollow saves you from spam
-   it improves the quality of content
-   it reduces the quality of backlinks

We need a reliable way that balances these two approaches. Something that:

-   detects low quality link spam and marks those links as nofollow
-   detects high quality links as good and let those be followed by search engines

For the links that fall in the middle, ie the ones we aren't so sure about we can either play safe and mark them as nofollow or specify a threshold score that must be matched before we unmark them.

## Solution

-   StackOverflow is one of the few websites that has even attempted to solve [this issue](http://meta.stackexchange.com/questions/111279/remove-nofollow-on-links-deemed-reputable). Their solution involves a lot of metadata they already have about the link (such as answer/comment score, votes, age etc) and they use that to mark a link as reputed.

Their approach is closed, so as to dissuade spammers from understanding it and working around it.

The general idea is to build a machine learning system that takes in a piece of content along with some optional metadata (such as authorship information) and then uses it to mark each link in the content as reputed/nofollow.

## Notes

_These are free-flow notes about the problem/solution/idea._

-   Training Data: Since so many sites already have heaps of user generated content, we can use their data (stackoverflow, wikipedia provide dumps) to get good quality links.
-   Reputed Sites: A very quick way to get off the ground would be to mark sources as reputed, such as wikipedia, new york times etc.
-   Accuracy: As a very basic check, we could use StackOverflow dataset (since it is partially nofollow) to check our own accuracy against their implementation.
-   Metadata: Will have to consider some metadata (such as authorship) along with the content itself, so as to improve spam accuracy. For instance, if the same user is posting too many links in a short time, we might mark future attempts as spam.
-   We could use akismet partially as a heuristic for partial content.
-   The idea is to build an API quite similar to akismet that can be embedded as plugins in content sites like wordpress and wikis.
-   We should also take care to actually check the link itself. For instance, the original link might point to some dummy site, but redirect to a spam website. Google would follow the redirect while crawling, and land up on the spam site if we are not careful.
