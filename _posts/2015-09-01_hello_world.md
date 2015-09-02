title: Hello World

# Welcome

To World of Games!

This post outlines some of the basic pieces of World of GameZ.

## Open Source

First, World of GameZ is an open source project. It's licensed
under the [Eclipse Public License](http://www.eclipse.org/legal/epl-v10.html).

Why?

The EPL is less opinionated about making the code virally open
source than the [GPL](https://en.wikipedia.org/wiki/GNU_General_Public_License)
but still has a grant-back provision. This means
folks who take and use World of GameZ code have to offer their
modifications back to the world.

Open Source also reflects a core value of people working together
to create something great. The kids and adults who will be participating
in the creation, running, and use of the World of GameZ platform
and the games that run on the platform should be working together
to create and share great things.

## Community Values

The World of GameZ platform community has a set of values: sharing
and creativity.

But each community has different values and different priorities.
A key part of World of GameZ is to allow each community to
have a World of GameZ realm that reflects those values.

How?

Each World of GameZ "realm" will have its own server and its
own rules. The rules can be configured and modified from
a base set of rules. The rules include:

* The process for allowing someone to join the realm
* What realms are communicated with (federation)
* What games are available on the realm and the process for allowing other games to be added to the realm
* Factors for adjusting game ratings (e.g., +2 years to the base ratings)
* When kids can communicate in the realm and what visibility parents have over kid communications
* Etc.

Each Realm makes its own rules and the rules are enforced by
the World of GameZ platform.

## Security

The World of GameZ platform is designed with security in mind.
This means:

* All web traffic to a realm or between realms will be over SSL
* All messages will be signed and/or encoded with keys/certs
* All data stored will be stored in Datomic so that any data at any point in time can be viewed
* Etc.

## Isolation

Each subsystem in the World of GameZ platform will be isolated from the other
subsystems and communicate primarily via asynchronous messages.

At a technical level, the World of GameZ platform will be in a series
of [Docker](https://docker.com) containers and will communicate via event
passing. This means each game will be in its own container and the messages
from the game engine to browsers or to other realms will be passed through
the engine rather than any form of direct connections. This allows the engine
to verify the signatures on messages. This also means very few systems
will have direct access to the data store.

Isolation means there will be a lot of effort spent on getting the
message passing and message shapes right. But these also become
documentation for the systems.

## Federation

As mentioned above, World of GameZ realms are stand-alone and will likely
support a few dozen to a few thousand members each.

However the realms can opt to federate with other World of GameZ realms.

Federation allows each community to manage its own realm, define its own
rules and codes of conduct, manage its community members, and define its
own governance rules.

However, cross-realm gaming (both creation and playing) is an important aspect
of World of GameZ

