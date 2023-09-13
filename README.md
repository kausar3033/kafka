# Welcome to Deploy Kafka & zookepper 

## Download kafka & zookerper  from kafka server

    wget https://downloads.apache.org/kafka/3.5.1/kafka_2.13-3.5.1.tgz
    wget https://archive.apache.org/dist/zookeeper/zookeeper-3.9.0/apache-zookeeper-3.9.0-bin.tar.gz
    
## untar both file

    tar -xf kafka_2.13-3.5.1.tgz
    tar -xf apache-zookeeper-3.9.0-bin.tar.gz

    bin/zkServer.sh start
    bin/zkServer.sh start-foreground
    bin/zkServer.sh stop

    cp "/home/ibos/apache-zookeeper-3.9.0-bin/conf/zoo_sample.cfg" "/home/ibos/apache-zookeeper-3.9.0-bin/conf/zoo_sample.cfg-copy"
    
### uncheck comment all function and add new line 

    4lw.command.whitelist=*

## Start kafka

    bin/kafka-server-start.sh -daemon config/server.properties
    bin/kafka-server-stop.sh config/server.properties
    echo dump | nc localhost 2181 | grep brokers




