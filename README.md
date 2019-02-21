# zimbra-elasticstack
Elastic Stack configuration files for Zimbra logging, filtering and visualization in Kibana.

- filebeat_zimbra_store.yml - This configuration file needs to be adjusted with your logstash server IP or FQDN. And then copyied to 
/etc/filebeat/ on the zimbra servers with the filebeat rpm installed.

- .json files under kibana folder are meant to be imported via Kibana UI. Exporting/Importing via CLI is not quite
there yet. https://www.elastic.co/guide/en/kibana/master/saved-objects-api.html

- 20_filter_zimbra.conf should be copied under /etc/logstash/conf.d folder. This file can be easily improved as it was written as a way to learn how to use grok filter (that's why different ways to filter are used).

- /patterns folder is the place to put the ZIMBRA filters created, so the filter files (like 20_filter_zimbra.conf) can look much cleaner.

