Add this lines in rsyslog.conf

#### RULES ####

$template MyruleFile, "/var/log/loghost/%HOSTNAME%/%syslogfacility-text%.log"
*.* ?MyruleFile
