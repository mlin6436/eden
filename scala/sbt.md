# SBT

[SBT](http://www.scala-sbt.org/) stands for `Scala Build Tools`, and is a popular build tool for Scala and Java projects, in the similar way as Maven.

### Installation

```bash
$ brew install sbt
```

### Structure

```text
src/
    main/
        resources/
            <files to include in main jar here>
        scala/
            <main Scala sources>
        java/
            <main Java sources>
    test/
        resources/
            <files to include in test jar here>
        scala/
            <test Scala sources>
        java/
            <test Java sources>
```

### Running

```bash
$ sbt # run sbt to enter sbt command mode
```

In addition, here is a list of commands in sbt (similar to Maven):

| Commands          | Explanation   |
| ----------------- | ------------- |
| clean             | Deletes all generated files (in the target directory). |
| compile           | Compiles the main sources (in src/main/scala and src/main/java directories). |
| test              | Compiles and runs all tests. |
| console           | Starts the Scala interpreter with a classpath including the compiled sources and all dependencies. To return to sbt, type :quit, Ctrl+D (Unix), or Ctrl+Z (Windows). |
| run <argument>*   | Runs the main class for the project in the same virtual machine as sbt. |
| package           | Creates a jar file containing the files in src/main/resources and the classes compiled from src/main/scala and src/main/java. |
| help <command>    | Displays detailed help for the specified command. If no command is provided, displays brief descriptions of all commands. |
| reload            | Reloads the build definition (build.sbt, project/*.scala, project/*.sbt files). Needed if you change the build definition. |

There are also some funky `History commands` (this is awesome in comparison to bash commands):

| History commands | Explanation |
| ---------------- | ----------- |
| !                | Show history command help. |
| !!               | Execute the previous command again. |
| !:               | Show all previous commands. |
| !:n              | Show the last n commands. |
| !n               | Execute the command with index n, as shown by the !: command. |
| !-n              | Execute the nth command before this one. |
| !string          | Execute the most recent command starting with 'string.' |
| !?string         | Execute the most recent command containing 'string.' |

### Build Definition

'build.sbt' defines a `Project`, which holds a list of Scala expressions called `Settings`. For more details, check [this](http://www.scala-sbt.org/release/tutorial/Basic-Def.html) out.
