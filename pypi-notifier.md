# PyPi Notifier

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


## Sources

Once it has your GitHub credentials:

- Starred github repos that are also on PyPi
- packages menetioned in setup.py and requirements.txt files from my own projects
- Allow someone to upload a requirements.txt and use that as source
- Parse the PyPi RSS Feed to get complete updates

All the sources are merged together.

## Notifications

- Maybe have a curated twitter account that tweets about releases for the top 10%
  packages.
- Create a personal RSS feed for every user
- Send out emails (configurable) for every release.
- Optional direct tweets as well?
