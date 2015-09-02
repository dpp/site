title: About


# About World of GameZ

World of GameZ is a trustworthy, fun, interactive place for kids to create, share, and play games in a small community environment where parents have visibility into and control over community behavior.

Why? Because my kids were using Roblox for a few days and then they started getting hit on by creeps (not something that should happen to a 10 year old), so
their mom and I removed Roblox from their machines. Their response: "we can build our own safe place to play!" And thus was born World of GameZ.

Rather than being one big, for-profit game site, World of GameZ will be a federation of realms (servers), each with its own rules (set by a combination of a high counsel [kids] and a counsel of elders [parents]). This is like e-mail was before the giant GMail in the sky took over. Each realm will federate with other realms on an opt-in basis and the choice to federate will be voted on by the counsels of both realms. Okay... a bit in the weeds... but net-net:

Each World of GameZ server will be small enough (a few hundred kids) that parents can effectively monitor and control the behavior on that server... much like the effectiveness of local PTAs. But people can share and play games across servers -- federation of realms.

World of GameZ is an open [source project](https://github.com/worldofgamez) that anyone can run and anyone can offer contributions to.

World of GameZ will offer game creation, game playing, tournaments, socialization, and other facilities. World of GameZ will also give parents visibility into what their kids are doing, who their kids are playing with, and what kinds of games their kids are playing, including a "time-hopping feature" so that parents can get a full history of what their kids have done.

Sophia has taken the lead in designing the trust model as well as the user interface.

Daniel is focusing his efforts on early games and game dynamics as well as a tournament model.

I am also reaching out to some hardcore geeks (all but one has kids) to help with some of the infrastructure pieces.

### On the technology side...

On the technical side, I've laid down the first part of the core community code in Clojure and ClojureScript. Why? Because its a great language for unified browser/server code and Clojure and core.async are great ways to handle events and deal with immutable data structures.

Everything about World of GameZ will be event-based. This is a great way to build games (just ask https://en.wikipedia.org/wiki/John_Carmack ). It's also a great way to build a distributed federation of systems (browsers and servers) that can participate in the same game.

I've chosen [Datomic](http://www.datomic.com/) for the storage mechanism. While it's not open source (a huge negative), it's the only database that I know of that simply supports historical views of information. This will make building a "time hop" feature a lot easier... even if kids edit/delete messages, parents will be able to see what happened in the past.

The games themselves can be written in any language. Games will be run in a Docker container and communicate with the server via an HTTP WebSocket connection (just like browser/server communication, just like federated server communication). The server will distribute messages or update data stores. This is for both security (games have no access to server resources, server data connections, etc.) and it allows games to be written based purely on events... so games can be written in Python, JavaScript, etc.

## Thanks

Thanks for your time and consideration... and Sophia, Daniel, and I sincerely hope you will join us!
