
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
