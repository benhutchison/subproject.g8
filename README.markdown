A [Giter8][g8] template for creating an SBT projects. 

It just creates `src/{main|test}/{scala|resources}`. 
```
sbtroot> new benhutchison/subproject.g8
name> mysubproject 
```

You still need to register it in your top level `build.sbt`
```
lazy val mysubproject = project.in(new File("mysubproject"))
  .dependsOn(myotherproject).settings(
    libraryDependencies ++= Seq(
      "group" %% "artifact" % "version"
    ),
)
```

Template license
----------------
Written in 2020 b yBen Hutchison brhutchison@gmail.com


To the extent possible under law, the author(s) have dedicated all copyright and related
and neighboring rights to this template to the public domain worldwide.
This template is distributed without any warranty. See <http://creativecommons.org/publicdomain/zero/1.0/>.

[g8]: http://www.foundweekends.org/giter8/
