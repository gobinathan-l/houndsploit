# HoundSploit.  An advanced graphical search engine for Exploit-DB


Author: Nicolas Carolo <nicolascarolo.dev@gmail.com>

Copyright: © 2020, Nicolas Carolo.

Date: 2020-04-19

Version: 2.1.0 (Beta)


## PURPOSE

_HoundSploit_ is an advanced and graphical search engine for Exploit-DB developed in
Python using Flask as micro framework, born with the aim of showing the user
the most accurate search results.

### Features

* Effective version number filtering
* Advanced filtering
* Search suggestions with customization
* Syntax highlighting of the source code of exploits and shellcodes
* Downloading of the source code of exploits and shellcodes
* Highlighting of searched words in search results
* Automatic check for updates

#### News in HoundSploit 2:
* Flask instead of Django
* SQLAlchemy instead of Django ORM
* SQLite instead of MySQL
* The kernel of the search engine is the same used for _hsploit_, which is the CLI version of HoundSploit
* Now ExploitDB database is automatically update

#### Effective version number filtering examples
##### Example I

```
nicolas@carolo:~$ searchsploit WordPress 2.0.2
WordPress 2.0.2- 'cache' Remote Shell Injection
WordPress Plugin Crawl Rate Tracker 2.0.2 - SQL Inject
WordPress Plugin Sodahead Polls 2.0.2 - Multiple Cross
```

**HoundSploit**: `WordPress 2.0.2`

10 exploits and 0 shellcodes found for "WordPress 2.0.2"

* WORDPRESS 1.5.1.1 < 2.2.2 - Multiple Vulnerabilities
* WORDPRESS < 4.0.1 - Denial of Service
* ...


##### Example II

```
nicolas@carolo:~$ searchsploit Linux Kernel 4.2.3
Exploits: No Result
Shellcodes: No Result
Papers: No Result
```

**HoundSploit**: `Linux Kernel 4.2.3`

14 exploits and 0 shellcodes found for "linux kernel 4.2.3"

* LINUX KERNEL 3.11 < 4.8 0 - 'SO_SNDBUFFORCE' / 'SO_RCVBUFFORCE' Local
Privilege Escalation
* LINUX KERNEL < 4.10.13 - 'keyctl_set_reqkey_keyring' Local Denial of 
Service
* ...


#### Advanced filtering

Using advanced search you can use the following filters for filtering search
results:
* Search operator: `AND` or `OR`
* Author
* Type
* Platform
* Port
* Date interval


#### Search suggestion

You can choose to show a particular suggestion for a given searched string.
For each case you can also decide to use automatic replacement or not.
It is possible to add new suggestions and delete the existing suggestions.

## MINIMUM REQUIREMENTS

### Supported OS

* Linux
* macOS

### Interpreter and tools

* Python 3
* SQLite 3
* git

## INSTALLATION

### Linux
We can install hsploit simply by doing:
```sh
$ git clone https://github.com/nicolas-carolo/houndsploit
$ cd houndsploit
$ sh install_db_linux.sh
$ pip install -r requirements.txt
$ python setup.py install
```

### macOS
We can install hsploit simply by doing:
```sh
$ git clone https://github.com/nicolas-carolo/houndsploit
$ cd houndsploit
$ sh install_db_darwin.sh
$ pip install -r requirements.txt
$ python setup.py install
```

## USAGE

For running the HoundSploit server:

```sh
$ houndsploit
```


## COPYRIGHT

Copyright © 2020, Nicolas Carolo.
All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are
met:

1. Redistributions of source code must retain the above copyright
   notice, this list of conditions, and the following disclaimer.

2. Redistributions in binary form must reproduce the above copyright
   notice, this list of conditions, and the following disclaimer in the
   documentation and/or other materials provided with the distribution.

3. Neither the name of the author of this software nor the names of
   contributors to this software may be used to endorse or promote
   products derived from this software without specific prior written
   consent.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
"AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT
LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR
A PARTICULAR PURPOSE ARE DISCLAIMED.  IN NO EVENT SHALL THE COPYRIGHT
OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT
LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE,
DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY
THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
(INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.