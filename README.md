# Zookeper

Cmd: zkserver {start|start-foreground|stop|restart|status|upgrade|print-cmd}
Config: /usr/local/etc/zookeeper/zoo.cfg

# Kafka

Folder: /usr/local/Cellar/kafka/1.0.0/bin
Config: /usr/local/etc/kafka/server.properties
Logs: /usr/local/var/lib/kafka-logs

# Installation, start and stop

# this will install java 1.8, zookeeper, and kafka
brew install kafka

# Start ZooKeeper and Kafka with brew
brew services start zookeeper
brew services start kafka

# Stop kafka and zookeeper with brew
brew services stop kafka
brew services stop zookeeper

# Creating topics
./kafka-topics --zookeeper localhost:2181 --create --partitions 1 --replication-factor 1 --topic test.topic

