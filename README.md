Add this lines in rsyslog.conf of Server\

Under Rules \

#### RULES ####

$template MyruleFile, "/var/log/loghost/%HOSTNAME%/%syslogfacility-text%.log" \
\*.\* ?MyruleFile


Add this line at the bottom of rsyslog.conf of Client \
\*.\* @@alma-server1.com (alma-server1.com, Server's domain name  - alternative use IP Address of Server)
