Logstash logging
================

###### So you long to log your long logs with Logstash?
###### Great! Let's start with installing Logstash itself.



Connect to the shell interface on your desired server using either PuTTY or some other terminal program.

1. Import the proper key for a YUM based installtion:
<pre><code>rpm --import http://packages.elasticsearch.org/GPG-KEY-elasticsearch</code></pre>

2. Create a logstash.repo file and paste the following [logstash-1.4] config inside
<pre><code>vi /etc/yum.repos.d/logstash.repo</code></pre>

<pre><code>[logstash-1.4]
name=logstash repository for 1.4.x packages
baseurl=http://packages.elasticsearch.org/logstash/1.4/centos
gpgcheck=1
gpgkey=http://packages.elasticsearch.org/GPG-KEY-elasticsearch
enabled=1</code></pre>

~3. Setup your logs to rotate daily at the bottom of logrotate.conf with the following:
<pre><code>vi /etc/logrotate.conf</code></pre>
<pre><code>/var/log/lognamehere {
    missingok
    daily
    create 0600 root root
    rotate 6
}</code></pre>

~4. Initiate the logrotation settings you just created
<pre><code>logrotate -s /var/log/lognamehere logrotate.conf</code></pre>
