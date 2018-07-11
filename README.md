# Janusgraph with Cassandra and Elasticsearch

Docker deployment of [JanusGraph](http://janusgraph.org/). To run,

```
docker-compose up --build
```

Connecting to local Gremlin shell:

```
docker exec -it janusgraphdocker_janus_1 ./bin/gremlin.sh
```

After connecting testing:

```
gremlin> :remote connect tinkerpop.server conf/remote.yaml
==>Connected - localhost/127.0.0.1:8182
gremlin> :> graph.addVertex("name", "stephen")
==>v[256]
gremlin> :> g.V().values('name')
==>stephen
```