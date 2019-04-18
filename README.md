# zimbra-elasticstack
Elastic Stack configuration files for Zimbra logging, filtering and visualization in Kibana.

- filebeat_zimbra_store.yml - This configuration file needs to be adjusted with your logstash server IP or FQDN. And then copyied to
/etc/filebeat/ on the zimbra servers with the filebeat rpm installed.

- heartbeat file needs to be adjusted to fit your IPs and specific configuration.

- .json files under kibana folder are meant to be imported via Kibana UI. Exporting/Importing via CLI is not quite
there yet. https://www.elastic.co/guide/en/kibana/master/saved-objects-api.html

- Import of kibana .json files is now done at once AFTER creating the zimbra index template.

- 20_filter_zimbra.conf should be copied under /etc/logstash/conf.d folder. Basic input (beat) and output (elasticsearch) files are necessary.

- 30_output.conf shows the zimbra index naming convention that works with the customized zimbra index template.

- Zimbra index template is to be added via Kibana "dev tools" webUI.
