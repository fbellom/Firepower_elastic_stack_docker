# Docker ELK for Firepower Log collection

This is a deployment of a full Elastic stack in docker, using docker compose to orchestrate the build up and tear down of the components

## File Structure

|-- docker-compose.yml
|-- elasticsearch
|   |-- config
|   |   `-- elasticsearch.yml
|   `-- Dockerfile
|-- kibana
|   |-- config
|   |   `-- kibana.yml
|   `-- Dockerfile
|-- logstash
|   |-- config
|   |   `-- logstash.yml
|   |-- Dockerfile
|   `-- pipeline
|       |-- encore_logs.conf
|       |-- fdm_logs.conf
|       |-- fmc_audit.conf
|       `-- ftd_logs.conf
`-- README.md


## Highlights

Each application gets its own workspace and volume
It's pretty simpple to test a new development in minutes.

## Requirements

- Docker CE
- Docker Compose

## Extras

You can add a NGINX container as reverse proxy for kibana.


