logmanagement_opensource
========================

In this repository you will find the configuration files for several log management related components:
- graylog2
- rsyslog
- logstash
- log4j

Log management related syslog messages are the messages with the facilities local5, local6 and local7.


Messages with a facility 'local5' will be forwarded directly to the graylog2-server (see 32-graylog2.conf).
Messages with the facilities 'local6' and 'local7' will be forwarded through logstash to graylog2 and statsd.

statsd is installed with the default configuration (port 8125).

log4j.xml defines appenders for the several syslog facilities, their messages can be handled from logstash. It defines also an appender to send gelf messages directly to graylog2.
