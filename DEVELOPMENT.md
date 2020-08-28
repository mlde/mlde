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

- provide usefull information about building, installation, configuration and usage in a
simple way
- give full documenation in the readme if possible
- avoid scattered documentation



## Configuration

- use only human-readable plain-text configuration files in ini-format
- the plain-text configuriation files are decisive
- configuration options are inherited and overriden by higher priority sources where 0 is the highest priority

| priority | source | description |
|:---------|:-------|:------------|
| 0 | argument | single-parameter as argument |
| 1 | argument | configuration-file as argument |
| 2 | /home/[user]/.config/[program]/[program].conf | local configuration |
| 3 | /etc/xdg/[program]/[program].conf | global configuration |
| 4 | compilation | compilation default |



## Theming

- use only human-readable plain-text theme files in [qss format](https://doc.qt.io/qt-5/stylesheet-syntax.html)
- theming options are inherited and overriden by higher priority sources where 0 is the highest priority
- there are several themes used by programs

| theme | description |
|:------|:------------|
| control-theme | control styles |
| color-theme | colors for control style |
| icon-theme | icons for controls |


#### set theme

| priority | source | description |
|:---------|:-------|:------------|
| 0 | argument | argument to the program |
| 1 | /home/[user]/.config/[program]/[program].conf | program local configuration |
| 2 | /etc/xdg/[program]/[program].conf | program global configuration |
| 3 | /home/[user]/.config/Trolltech.conf | qt local configuration |
| 4 | /etc/xdg/Trolltech.conf | qt global configuration |
| 5 | compilation | compilation default |


#### load control theme

| priority | source | description |
|:---------|:-------|:------------|
| 0 | /home/[user]/.config/[program]/themes/[theme]/ | program local theme |
| 1 | /usr/share/[program]/themes/[theme]/ | program global theme |
| 2 | /home/[user]/.themes/[theme]/ | local theme |
| 3 | /usr/share/themes/[theme]/ | global theme |


#### load icon theme

| priority | source | description |
|:---------|:-------|:------------|
| 0 | /home/[user]/.config/[program]/icons/[theme]/ | program local theme |
| 1 | /usr/share/[program]/icons/[theme]/ | program global theme |
| 2 | /home/[user]/.local/share/icons/[theme]/ | local theme |
| 3 | /usr/share/icons/[theme]/ | global theme |


#### load color theme

| priority | source | description |
|:---------|:-------|:------------|
| 0 | /home/[user]/.config/[program]/color-schemes/[theme].colors | program local theme |
| 1 | /usr/share/[program]/color-schemes/[theme].colors | program global theme |
| 2 | /home/[user]/.local/share/color-schemes/[theme].colors | local theme |
| 3 | /usr/share/color-schemes/[theme].colors | global theme |


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
  
