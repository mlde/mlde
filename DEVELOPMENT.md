## Philosophy

Always keep this philosophies in mind

- [Simple, Lovable, Complete](https://blog.asmartbear.com/slc.html)
- [Your aren't gonna need it](https://en.wikipedia.org/wiki/You_aren%27t_gonna_need_it)
- [Keep it simple, stupid](https://en.wikipedia.org/wiki/KISS_principle)
- [Don't repeat yourself](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself)
- [Rules of Three](https://en.wikipedia.org/wiki/Rule_of_three_(computer_programming))
- [Release early, release often](https://en.wikipedia.org/wiki/Release_early,_release_often)



## Standards

Comply with applicable standards

- [Filesystem Hierarchy Standard](https://en.m.wikipedia.org/wiki/Filesystem_Hierarchy_Standard)
- [Freedesktop Standards](https://www.freedesktop.org/wiki/Specifications/)
- [Freedesktop Software](https://www.freedesktop.org/wiki/Software/)



## Tools

use this tools for development

- [c++](https://isocpp.org/) as programming language
- [qt](https://www.qt.io/) as gui-toolkit
- [gcc](https://gcc.gnu.org/) as compiler and linker
- [moc](https://doc.qt.io/qt-5/moc.html) for qt classes
- [ninja](https://ninja-build.org/) as built-tool



## Documentation

- Provide usefull information about building, installation, configuration and usage in a
simple way
- Give full docmenation in the readme if possible
- Avoid scattered documentation



## Configuration

- use only human-readable plain-text configuration files in ini-format
- the plain-text configuriation files are decisive
- any gui-configuration-tools must be based exclusively on the plaint-text configuration files

1. compilation default
2. global configuration-file in /etc/xdg/[program]/[program].conf
3. local configuration-file in ~/.config/[program]/[program].conf
4. configuration-file as argument to the program
5. single-parameter as argument to the program

- Settings from actual configuration file override settings from previous read configuration files.
- So you can ie keep the general configuration and change just one option.



## Theming

- use only human-readable plain-text theme files in qss format

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



## Logging

- implement logging for each program
- make logging-target configurable (journald (default), console/stderr)
- make loglevel configurable
- log all messages with a loglevel equal or smaller than the given loglevel  

| Level         | Description |
|:--------------|:------------|
| Fatal         | program is unusable |
| Critical      | a critical error occured |
| Warning       | indicate that an error will occur if action is not taken |
| Informational | normal operational messages that require no action |
| Debug         | information useful to developers for debugging the application |



## Branches 

- Use one main branch
- create a branch for each feature or issue
- commit early and often, do not hide anything
- create a pull-request for reviewed features or issues



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
  
