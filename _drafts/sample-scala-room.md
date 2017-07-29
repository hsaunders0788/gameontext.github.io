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
}```
