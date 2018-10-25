**Geo IP Instructions**

1. Stop Logstash
2. Delete existing index: curl --user elastic -XDELETE http://172.19.0.2:9200/container-log?pretty
3. Add new index with custom mapping: cat logstash/templates/nginx_template.json | curl --user elastic -XPUT http://ELASTIC-ADDRESS:9200/container-log?pretty
4. Start logstash
