Duo Script 2
==============

Introduction
------------
Scripts to monitor AWS services

Installation
------------
Download the duo-script directory to /usr/local/bin/urth/

Description
-----------
Grabs status of the following AWS services by RSS feed from the US East Region
 - EC2
 - RDS
 - ELB
 - ElastiCache
 - CloudFormation

Data on these services and their current status is then output to a JSON format in final.json before being parsed out for viewing.

Usage
-----
Simply use ./pyparse where it was downloaded. This will grab the latest status of each AWS service via an RSS feed, output the results in a JSON format, then parsed out for viewing by browser. When the script is running pull up http://server-IP-here/awscheck.html
