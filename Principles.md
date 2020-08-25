# Principles

A modular linux desktop environment based on the [traditional unix philosophie](https://en.wikipedia.org/wiki/Unix_philosophy),
utilizing modern technology and look.

https://opensource.guide/starting-a-project/
https://opensource.guide/building-community/
https://gist.github.com/PurpleBooth/109311bb0361f32d87a2

Prinzipien durchgehen und ggf ergänzen!


### Make each program do one thing well

[description missing]


### Make each program easily interchangeable

[description missing]


### Make each program as lightweight and fast as possible

[description missing]


### Logging
xxx


### Desktop-Files
xxx


### Use text-based configuration files

[description incomplete]

- The text-based configuriation files are decisive.
- Any gui-configuration-tools are based exclusively on the text-based configuration files.


### Use text-based theme files

[description missing]


### Easy configuration on every level

[description incomplete]
[format of configuration files]

Get configuration-values:

1. compilation default
2. global configuration-file in /etc/xdg/app/app.conf
3. local configuration-file in ~/.config/app/app.conf
4. configuration-file as argument to the app
5. single-parameter as argument to the app

Settings from a configuration file override settings from previous read configuration files.
So you can ie keep the general configuration and change just one option.


### Easy theme customisation on every level

[description incomplete]
[format of theme files]

Get the theme:

1. compilation default
2. global qt-configuration
3. local qt-configuration
4. global app configuriation in /etc/xdg/app/app.conf
5. local app configuration in ~/.config/app/app.conf
6. argument to the app

Find the theme:

1. global theme in [missing]
2. local theme in ~/[missing]
3. global theme from app in [missing]
4. local theme from app in ~/[missing]

Settings from a theme file override settings from previous read theme files.
So you can ie keep the general theme and change just one option.


### Comply with applicable standards

[description incomplete]

- [Filesystem Hierarchy Standard](https://en.m.wikipedia.org/wiki/Filesystem_Hierarchy_Standard)


### Use [C++](https://isocpp.org/) as programming language

[description incomplete]

- compatibility with QT5


### Use [qt](https://www.qt.io/) as gui-toolkit

[description missing]


### Use [gcc](https://gcc.gnu.org/) as compiler and linker

[description incomplete]

- gcc is widely available and most likely already installed
- but do not use any specific gcc-flags

Exception from this principle: the [qt moc-tool](https://doc.qt.io/qt-5/moc.html) is necessary for the qt toolkit


### Use [ninja](https://ninja-build.org/) as built-tool

- You should know how to compile and link the program without a built-tool.
- A build-tool is only a helper to automate this process.
- a built-tool should invoke the compiler and linker only
- a built-tool should not work as install-tool
- a built-tool should not add additional complexity
- a built-tool should not hide or abstract the work that is done


### Documentation

[description incomplete]

- Provide usefull information about building, installation, configuration and usage in a
simple way.
- Give full docmenation in the readme if possible.
- Avoid scattered documentation.
- See [lead](https://github.com/mlde/lead/) as example.


### Branches 

[description incomplete]

- Use one main branch
- create a branch for each eatures and each issue
- commit early and often, do not hide anything
- when finished features or issues are tested, create a pull-request (bzw. merge)

https://fbrnc.net/blog/2014/12/keeping-it-simple-git-workflow
https://shalikafdo.files.wordpress.com/2016/02/git5.png?w=604&h=402
https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow


### Releases

[description incomplete]

- Releases are tags on the main-branch at appropriate moments
- Release numbers are simply incremental
- Each Release should contain
  - archiv of the source
  - rpm paket x86-64
  - deb paket x86-64
  - AUR?
