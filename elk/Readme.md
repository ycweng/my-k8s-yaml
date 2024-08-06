# APM 架構
![img.png](https://ithelp.ithome.com.tw/upload/images/20210923/20129762m1PXwNY16H.png)

## APM agent 安裝
- tomcat implement `setenv.sh`
```
curl -o 'elastic-apm-agent.jar' -L 'https://oss.sonatype.org/service/local/artifact/maven/redirect?r=releases&g=co.elastic.apm&a=elastic-apm-agent&v=LATEST'

export JAVA_OPTS="$JAVA_OPTS -javaagent:/usr/local/etc/tomcat-metrics/elastic-apm-agent.jar"
export JAVA_OPTS="$JAVA_OPTS -Delastic.apm.service_name=kfc-22-web"
export JAVA_OPTS="$JAVA_OPTS -Delastic.apm.server_url=http://10.110.54.80:30645"
```
# Filebeat x Kafka x Logstash
## Filebeat
```shell
curl -L -O https://artifacts.elastic.co/downloads/beats/filebeat/filebeat-7.17.21-linux-x86_64.tar.gz
tar xzvf filebeat-7.17.21-linux-x86_64.tar.gz

```