# Scala Project Structure

```text
.
├── build.sbt
├── project
├── README.md
├── src
│   ├── main
│   │   ├── java
│   │   |   └── *.java
│   │   ├── resources
│   │   └── scala
│   │   |   └── *.scala
│   └── test
│       ├── java
│           └── *.java
│       ├── resources
│       └── scala
│           └── *.scala
└── target
```

**.gitignore**

```text
*.class
*.log

# sbt specific
.cache
.history
.lib/
dist/*
target/
lib_managed/
src_managed/
project/boot/
project/plugins/project/

# Scala-IDE specific
.scala_dependencies
.worksheet

# idea project files
.idea/
.idea_modules/
out/
*.iml
*.ipr
*.iws
```
