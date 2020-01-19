# docker-spark-scylla
cluster for data analysis with spark and scylla

## connect to `cqlsh`
```
docker-compose exec scylladb-node1 cqlsh
```

## connect to `spark-shell`
```
docker-compose exec spark-master spark-shell     --conf spark.driver.host=spark-master     --conf spark.cassandra.connection.host=scylladb-node1     ges datastax:spark-cassandra-connector:2.4.0-s_2.11,commons-configuration:commons-configuration:1.10
```
