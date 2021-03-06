# swarmstack/postgresql-exporters

Docker compose file for [wrouesnel/postgres_exporter](https://github.com/wrouesnel/postgres_exporter), Prometheus configuration example, and Grafana Dashboard for PostgreSQL servers


## USAGE

```
docker stack deploy -c docker-compose.yml postgresql-exporters
```

[swarmstack](https://github.com/swarmstack/swarmstack) users should use docker-compose-swarmstack.yml above instead.

---

In the prometheus/ directory in this repo, you'll find example Prometheus configurations to scrape the exporters once per 5 minutes as to not induce extra load on your servers. If your PG servers aren't heavily loaded, you can scrape them at whatever interval you like.

In the grafana/ directory you'll find a Grafana 6.0+ dashboard that uses metrics from [postgres_exporter](https://github.com/wrouesnel/postgres_exporter) as well as [node exporter](https://github.com/prometheus/node_exporter) to give you a full view of your PostgreSQL hosts.
