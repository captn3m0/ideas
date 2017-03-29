# Green/Yellow Pages

A distributed directory for spam reports.

I despise [TrueCaller][tc], the current world-leader in this space,
because their entire business model depends on users selling their data
to Truecaller, which can then make as much money from this database.

When you look at the root problem that truecaller is solving,
it is a reverse-yellow-pages directory to avoid spam calls.

To solve this:

1. You need a way to check a number against a known spam list.
2. You need the check to be as fast as possible.

If you want to beat TrueCaller, this check should be completely offline,
to present a significant advantage.

# API

The API has 2 endpoints:

1. Register a number as spam.
2. Check a number and get a YES/NO spam response.

## Spam registration

To prevent abuse, you want the client to do some 
proof of work before _each_ submission. Publish
a hash of the input number in a ledger.

## Data Store

Maintain a layered bloom filter ([research][res])
for each of the country-domains. We don't store
the original number, though, but the hash of the
phone number in the bloom filters.

## Check

Any party can request a check by sending us a
hash of the phone number (so it doesn't really
leak _much_ info) along with the country code.
We want a slow hash function but since we
want this to be verifiable on the client itself,
the ideal would be that it takes ~0.25s on a
average mobile device.

Once we recieve the hash, check it against all
the bloom filter layers in parallel and
return the results as a score.

For eg, if we have 1000 layers (to check upto
1000 reports), return the highest layer number
that has an entry for the number.

# Ledger

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

# Directory

A generated directory is a compressed
export of the nth layer of the bloom
filter. `n` here can be decided by
the customer. So you can pick n=5,
for a high-false-negative rate.

Over time, I expect this to be standardized
as high/low/medium.

# Application

The application uses a list
of country codes (which it can
auto-fill from the application
context) as input to download
directories from various known
sources. The remainder of the
application is spent on interrupting
inbound calls and adding a overlay
with the call score.

# Security/Privacy concerns

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
as important as *when* it was added.

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

# Deregistration

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

# Cost of Computation

- Verification should be fast
- Insertions should be slow
- Client registrations should be costly

By costly, I mean the compute price, not monetary.
A nice way to equalize this would be to make
a registration as hard as 10 insertions, so
creating a client and reporting 9 further
times would be much more cheaper to do.

This helps in ensuring that there is still
a way to counter spam reports. I'm sure
there are better ideas, though.

# Terms

*Directory*: The actual data store holding a "Yes/No" filter of whether a number is spammy or not.
*Ledger*: A blockchain or ditributed log that maintains any reports.

## References
- You should totally read [Falsehoods Programmers Believe About Phone Numbers](https://github.com/googlei18n/libphonenumber/blob/master/FALSEHOODS.md)
- [bitly/dablooms](https://github.com/bitly/dablooms) - an attempt by bitly to solve spam problems with a layered bloom filter which is countable as well
- [scalable bloom filters](https://www.sciencedirect.com/science/article/pii/S0020019006003127)
- [A multi-layer bloom filter for duplicated URL detection](http://ieeexplore.ieee.org/document/5578947/?reload=true)

[solomon]: https://en.wikipedia.org/wiki/Telephone_numbers_in_the_Solomon_Islands
[res]: http://ieeexplore.ieee.org/document/5578947/?reload=true
