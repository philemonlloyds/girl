# GitHub README Link Checker

![](https://raw.githubusercontent.com/bamos/girl/master/screenshot.png)

`girl` is a <b>Gi</b>thub <b>R</b>eadme <b>L</b>ink Checker
served over HTTP with [Scala](http://scala-lang.org/)
and [Spray](http://spray.io/).
A public version is hosted at <http://derecho.cs.cmu.edu:8585/demo>.

## Whitelist
To prevent misuse, girl restricts usage to
GitHub users with
over 250 followers or users and organizations on the
[whitelist](https://github.com/bamos/girl/blob/master/src/main/scala/Whitelist.scala).
Please submit a pull request to gain access. Thanks!

## Building

`girl` is built with [sbt][sbt].
Executing `sbt run` from the `girl` directory will download
the dependencies, compile the source code, and start
an HTTP server on `0.0.0.0:8585`.
[Main.scala](https://github.com/bamos/girl/blob/master/src/main/scala/Main.scala)
configures the interface and port.

[sbt-revolver][sbt-revolver] is helpful for development.
Start an `sbt` shell and execute `~re-start`,
which re-compiles and restarts the server upon source code changes.

[sbt]: http://www.scala-sbt.org/
[sbt-revolver]: https://github.com/spray/sbt-revolver