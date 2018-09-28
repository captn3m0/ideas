# communities browser extension :gift:

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
