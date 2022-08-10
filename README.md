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