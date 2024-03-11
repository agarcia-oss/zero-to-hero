# Helm Charts - Zero to Hero

## Description

This project is a simple exercise for evaluating Open Source Helm charts security and configuration issues. It can be used along with the [Kubescape Bitnami](https://hub.docker.com/r/bitnami/kubescape) CLI tool to generate an OSS Assessment health report.

The Helm chart has the following dependencies:

- **PostgreSQL** version 14.3.1 from [oci://registry-1.docker.io/bitnamicharts](https://github.com/bitnami/charts/tree/main/bitnami/postgresql)
- **Nginx** version 15.14.0 from [oci://registry-1.docker.io/bitnamicharts](https://github.com/bitnami/charts/tree/main/bitnami/nginx)
- **Grafana** version 9.13.0 from [oci://registry-1.docker.io/bitnamicharts](https://github.com/bitnami/charts/tree/main/bitnami/grafana)
- **Clickhouse** version 5.3.0 from [oci://registry-1.docker.io/bitnamicharts](https://github.com/bitnami/charts/tree/main/bitnami/clickhouse)

Each dependency is tagged for easy identification and management.

All these dependencies have an equivalent chart in the [Tanzu Application Catalog](https://app-catalog.vmware.com/catalog).

Alternative versions of the Helm chart can be found here:

* [Upstream charts dependencies](https://github.com/agarcia-oss/zero-to-hero/tree)
* [Tanzu Application Catalog chart dependencies](https://github.com/agarcia-oss/zero-to-hero/tree/tac)

## Executing the report

```bash
docker run --rm -it -v $HOME:/output \
        bitnami/kubescape:3.0.3 oss-assessment \
        https://github.com/agarcia-oss/zero-to-hero/tree/bitnami \
        --output /output/report.json
```

## Sample report for this repository

![alt text](image.png)

## Obtaining the OSS Healh Assessmet

TBC
