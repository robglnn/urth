Unus Script 1
==============

Introduction
------------
A shell script for monitoring apache.

Installation
------------
Download the unus script to your /usr/bin directory

Description
-----------
Monitoring of apache processes every 30 seconds. Checks for the following load levels:
 - Low (under 10 processes)
 - High (over 20 processes)
 - Critical (over 100 processes)

Critical levels automate a restart of the apache service. Will also display a count of current running apache services.

Usage
-----
If you've added the script to /usr/bin it can be run from any directory. Otherwise simply use ./unus from where it was downloaded.
