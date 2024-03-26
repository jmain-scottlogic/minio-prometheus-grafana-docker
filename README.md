# minio-prometheus-grafana-docker

Example of a setup with minio, grafana and prometheus inside a docker compose

## Prerequisites

This project requires you to have Docker and Docker compose installed. Nothing else.

## Setup

1. Start docker compose on the project folder with:

```
docker-compose up -d
```

2. MinIO console will be available on localhost:9001, username/password: minioadmin. To change which prometheus job is for the metric update `MINIO_PROMETHEUS_JOB_ID` environment var to one of the job name in the prometheus.yml files
3. Prometheus will be available on localhost:9090.
4. Grafana will be available on localhost:3000. Log in with admin/admin.
5. Add the prometheus datasource to grafana, with url prometheus:9090. 
5. Create a bucket named "test" on MinIO, by accessing localhost:9000 and selecting the icon on the bottom right corner of the UI.
6. A Grafana dashboard can be downloaded from [here](https://github.com/minio/minio/blob/master/docs/metrics/prometheus/grafana/README.md), and adapted to the compose scenario.