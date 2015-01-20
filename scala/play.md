# Play

[Play](https://www.playframework.com/) is a MVC framework written in Scala and Java.

### Installation

```bash
$ brew install play
```

### Instantiate a new application

```bash
$ play new playApp
```


### Structure

```text
app                      → Application sources
  └ assets               → Compiled asset sources
    └ stylesheets        → Typically LESS CSS sources
    └ javascripts        → Typically CoffeeScript sources
  └ controllers          → Application controllers
  └ models               → Application business layer
  └ views                → Templates
build.sbt                → Application build script
conf                     → Configurations files and other non-compiled resources (on classpath)
  └ application.conf     → Main configuration file
  └ routes               → Routes definition
public                   → Public assets
  └ stylesheets          → CSS files
  └ javascripts          → Javascript files
  └ images               → Image files
project                  → sbt configuration files
  └ build.properties     → Marker for sbt project
  └ plugins.sbt          → sbt plugins including the declaration for Play itself
lib                      → Unmanaged libraries dependencies
logs                     → Standard logs folder
  └ application.log      → Default log file
target                   → Generated stuff
  └ scala-2.10.0
    └ cache
    └ classes            → Compiled class files
    └ classes_managed    → Managed class files (templates, ...)
    └ resource_managed   → Managed resources (less, ...)
    └ src_managed        → Generated sources (templates, ...)
test                     → source folder for unit or functional tests
```

### Running

```bash
$ cd playApp
```

Use `play` in conjunction with other commands in the format of `play run`, or enter `play` console and use each command individually.

| Commands          | Explanation   |
| ----------------- | ------------- |
| run               | Runs the server in development mode. |
| compile           | Compiles the main sources. |
| console           | Launch the interactive console. |
| debug             | Enters the debug mode. |
| test              | Compiles and runs all tests. |
| clean-all         | Cleans all. |
| idea              | Generates IntelliJ configuration. |

A more comprehensive explanation can be found [here](https://www.playframework.com/documentation/2.0/PlayConsole).
