# fluend=td and kinesis

## install the td-agent on Amazon Linux 2

```
$ curl -L https://toolbelt.treasuredata.com/sh/install-amazon2-td-agent4.sh | sh
```

## install the fluentd kinesis plugin

```
$ sudo /usr/sbin/td-agent-gem install fluent-plugin-kinesis
```
## the fluentd configuration file


```
/etc/td-agent/td-agent.conf
```

## check the td-agent log

```
/var/log/td-agent 
```

## install the java 

```
sudo amazon-linux-extras install java-openjdk11 -y
```

## run the below command if the elasticsearch container exit

```
sysctl -w vm.max_map_count=262144
```

## install docker

```
sudo amazon-linux-extras install docker
sudo service docker start
sudo usermod -a -G docker ec2-user
```

## run the elasticsearch and kibana containers

```
docker run --name es01 --net elastic -p 9200:9200 -p 9300:9300  -d  docker.elastic.co/elasticsearch/elasticsearch:8.3.3
docker run --name kib01 --net elastic -p 5601:5601 -d docker.elastic.co/kibana/kibana:8.3.3
```

## References

* https://docs.aws.amazon.com/code-samples/latest/catalog/python-kinesis-streams-kinesis_stream.py.html
* https://stackoverflow.com/questions/69642473/fluentd-output-json-value-as-json-without-message-key


* https://regexr.com/