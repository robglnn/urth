Urth Script 1
==============

Basic monitoring of apache processes every 30 seconds. Checks for the following load levels:
 - Low (under 10 processes)
 - High (over 20 processes)
 - Critical (over 100 processes)

Critical levels automate a restart the apache service. Will also display a count of current running apache services.
