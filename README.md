In this repository there are various small command-line (Linux) scripts made to facilitate working with Subversion
Following tools are currently present

Author: Krzysztof Kotowicz <kkotowicz at gmail dot com>

License: MIT

svn-grep
==========
Script used to grep subversion repository for a given string in all log messages and fetch related revisions' log messages and diffs.

Requirements
------------
- Subversion client (command line)
- [xmlstarlet](http://xmlstar.sourceforge.net) (I use xmlstarlet package for Ubuntu)

Usage
-----
    svn-grep <string to search for> [output-dir] [working copy dir]

`output-dir` defaults to `./report-SEARCH_TERM`

`working copy dir` defaults to `.`

Grepping the repository could take some time as all repository history must be transferred to client.

Example
-------
    svn-grep CUSTOM_FEATURE 
    
This will fetch all logs/diffs for all revisions having CUSTOM_FEATURE in log message and put it into `./report-CUSTOM_FEATURE`

svn-zip
=======
Script used to upgrade a working copy and export it to a zip file with name containing last revision or a given version string.
Useful if you need to supply your customers with versioned releases of your software.
