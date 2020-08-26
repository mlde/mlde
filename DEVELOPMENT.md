## We like

- [Simple, Lovable, Complete](https://blog.asmartbear.com/slc.html)
- [Your aren't gonna need it](https://en.wikipedia.org/wiki/You_aren%27t_gonna_need_it)
- [Keep it simple, stupid](https://en.wikipedia.org/wiki/KISS_principle)
- [Don't repeat yourself](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself)
- [Rules of Three](https://en.wikipedia.org/wiki/Rule_of_three_(computer_programming))
- [Release early, release often](https://en.wikipedia.org/wiki/Release_early,_release_often)




+ Make each program do one thing well
+ each program should be responsible for one thing only



* Make each program easily interchangeable
* aim for a composition of programs that can be fitted together or arranged in a variety of ways
* aim for no dependencies on other programs



- Make each program lightweight and fast
- design for low footprint on disk, memory and cpu
- balance the usage of disk, memory and cpu for efficiency


## Usefull documentation

- Provide usefull information about building, installation, configuration and usage in a
simple way
- Give full docmenation in the readme if possible
- Avoid scattered documentation


## Use text-based configuration files

- only human-readable and plain-text configuration files
- the plain-text configuriation files are decisive
- any gui-configuration-tools are based exclusively on the plaint-text configuration files


### Get configuration

1. compilation default
2. global configuration-file in /etc/xdg/[program]/[program].conf
3. local configuration-file in ~/.config/[program]/[program].conf
4. configuration-file as argument to the program
5. single-parameter as argument to the program

- Settings from actual configuration file override settings from previous read configuration files.
- So you can ie keep the general configuration and change just one option.


### Format of configuration files

xxx


## Use text-based theme files

- Use only human-readable and plain-text theme files

### Get theme
1. compilation default
2. global qt-configuration
3. local qt-configuration
4. global app configuriation in /etc/xdg/app/app.conf
5. local app configuration in ~/.config/app/app.conf
6. argument to the app

### Load theme
1. global theme in [missing]
2. local theme in ~/[missing]
3. global theme from app in [missing]
4. local theme from app in ~/[missing]

- Settings from actual theme file override settings from previous read theme files.
- So you can ie keep the general theme and change just one option.


## Use [C++](https://isocpp.org/) as programming language

- compatibility with QT5


## Use [qt](https://www.qt.io/) as gui-toolkit

- [description missing]


## Use [gcc](https://gcc.gnu.org/) as compiler and linker

- gcc is widely available and most likely already installed
- avoid gcc-specific flags
- Exception: the [qt moc-tool](https://doc.qt.io/qt-5/moc.html) is necessary for qt


## Use [ninja](https://ninja-build.org/) as built-tool

- You should know how to compile and link the program without a built-tool.
- A build-tool is only a helper to automate this process.
- a built-tool should not work as install-tool
- a built-tool should not add additional complexity
- a built-tool should not hide or abstract the work that is done


## Logging

- Implement logging for each program
- Make logging-target configurable (journald (default), console/stderr)
- Make loglevel configurable
- log all messages with a loglevel equal or smaller than the given loglevel  

| Level         | Description |
|:--------------|:------------|
| Fatal         | program is unusable |
| Critical      | a critical error occured |
| Warning       | indicate that an error will occur if action is not taken |
| Informational | normal operational messages that require no action |
| Debug         | information useful to developers for debugging the application |


## Comply with applicable standards

- [Filesystem Hierarchy Standard](https://en.m.wikipedia.org/wiki/Filesystem_Hierarchy_Standard)
- [Freedesktop Standards](https://www.freedesktop.org/wiki/Specifications/)
- [Freedesktop Software](https://www.freedesktop.org/wiki/Software/)


## Branches 

- Use one main branch
- create a branch for each feature or issue
- commit early and often, do not hide anything
- create a pull-request for reviewed features or issues


> - https://fbrnc.net/blog/2014/12/keeping-it-simple-git-workflow
> - https://shalikafdo.files.wordpress.com/2016/02/git5.png?w=604&h=402
> - https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow
> - https://wiki.qt.io/Review_Policy


## Releases

- Releases are tags on the main-branch at appropriate moments
- Release numbers are simply incremental
- Each Release should contain
  - tar.gz of the source
  - rpm paket x86-64
  - deb paket x86-64
  - AUR?
  
  
>   - https://rpm.org/
>   - https://manpages.debian.org/unstable/dpkg-dev/deb.5.en.html
>   - https://wiki.archlinux.org/index.php/Arch_User_Repository
  
