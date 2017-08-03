---
layout: post
title: sample scala room
summary: play with play in scala in game on!
tags: [fun, profit, scala, play]
author: ilan
---
## tl;dr
[advanced adventures](https://book.gameontext.org/walkthroughs/creatingYourOwnRoom.html).

[scala](http://www.scala-lang.org).

[sbt](http://www.scala-sbt.org/).

[giter8](http://www.foundweekends.org/giter8/).

[play](https://www.playframework.com/).

[ensime](http://ensime.org).

## Day 0

So for me 2017/18 is going to include adventures in polyglot.
> This  will include but will not be only restricted to
> `Kotlin`,`Prolog`, `Erlang`, `Racket`, `Haskell`, `Closure`, `Scala`

## Day 1

### Decide on tooling.
- `play` framework looks fun as a framework for a sample room.
  - `play` has a [web socket api](https://www.playframework.com/documentation/2.6.x/ScalaWebSockets)
  - `giter8` has a [starter template](https://github.com/foundweekends/giter8/wiki/giter8-templates) for `play`.
- `ensime` looks fun as a development environment.

### Learn to stop hating and love regexes

```scala
scala> sample
res69: String =
roomHello,<roomId>,{
    "username": "username",
    "userId": "<userId>",
    "version": 1|2
}

scala> pattern
res70: scala.util.matching.Regex = (?s)(\w+),([^,]*),(.*)

scala> val pattern(target,id,payload) = sample
target: String = roomHello
id: String = <roomId>
payload: String =
{
    "username": "username",
    "userId": "<userId>",
    "version": 1|2
}
```

## Day 2

- Learn about how the play framework works with [json](https://www.playframework.com/documentation/2.6.x/ScalaJson)
- Add some code to parse the (roomHello|roomJoin) message and reply correctly.
- [commit](https://github.com/gameontext/sample-scala-room/commit/28102e83400d7f12a2c843bf5d48da7c34d7ab16)

## Day 3

- add websocket chat response
- [commit](https://github.com/gameontext/sample-scala-room/commit/6dcc22c1a82b09290995831f400ff45c960c3341)

## Day 4

- hack up some room replies when home late after midnight
- [commit](https://github.com/gameontext/sample-scala-room/commit/5e5fdf380f9c6f6e28395cb3902e5820e09f045a)

## Day 5

- tidy up a bit, make the code space a bit more cozy
- [commit](https://github.com/gameontext/sample-scala-room/commit/c132d41cf85b40dc79c38a16a08c5fe3b29e3a1f)
- [commit](https://github.com/gameontext/sample-scala-room/commit/1b065465a6c06e3049297061b2f4df4b54517877)
- start working on "room is running page", which leads to having to understand
  - the [javascript security](https://www.playframework.com/documentation/2.6.x/SecurityHeaders) settings for play
  - and also more specifically [content security policy](https://www.html5rocks.com/en/tutorials/security/content-security-policy/)
  - and [also](https://www.playframework.com/documentation/2.6.x/resources/confs/filters-helpers/reference.conf)
- realise that you need [bootstrap](http://getbootstrap.com/getting-started/) to make it look decent
- using bootstrap, make a *your room is running page* with test buttons, to test web socket calls.
- [commit](https://github.com/gameontext/sample-scala-room/commit/f8b6992d9a21c24bff191058514464ba2e02728f)

![](http://i.imgur.com/msfwQ6F.png?1)

## Day 6

ooh, its getting addictive to play with the bootstrap
- make it possible to edit preformed test message, or send arbritary message in the tests provided on the page.
- [commit](https://github.com/gameontext/sample-scala-room/commit/e532f45faa6528d79a3f1d7e2b3ad9ff270de04b)
![](http://i.imgur.com/jb4Us3h.png?1)

- learn that in bootstratp 1 == 12 so that the room test screen flows responsively.
