# pfsense-elasticsearch
Files needed to send pfsense log files into Elasticsearch

###Areas of the files that might require customizing:

*logstash.conf*

- There are 2 inputs, one for TCP and one for UDP.  These both listen on 5515
- In the filter, the timezone is set as Europe/London
- The output has a stock un-authed output to Elasticsearch

*General*

The index is set to 'syslog-pfsense-%{+YYYY.MM.dd}' and the Elasticsearch template is set to 'syslog-pfsense-*' to match.
