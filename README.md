# Flume Delete HBase Sink

## Build
mvn package

## Install
Copy target/flume-delete-hbase-sink-1.0.0.jar in Flume' classpath

## Configure
hbaseagent.sinks.hbase_products.type = com.marketconnect.flume.sink.deletehbase.DeleteHBaseSink
hbaseagent.sinks.hbase_products.table = products
hbaseagent.sinks.hbase_products.zookeeperQuorum = prod-gra5-hadoop-masters-3.clic2buy.com:2181,prod-gra5-hadoop-masters-4.clic2buy.com:2181,prod-gra5-hadoop-queue-jobs-.clic2buy.com:2181
hbaseagent.sinks.hbase_products.znodeParent = /hbase
hbaseagent.sinks.hbase_products.channel = mem_hbase_products
hbaseagent.sinks.hbase_products.batchSize = 10

It will append the data to products if price == 0