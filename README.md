# Helm Charts - Zero to Hero

## Description

This project is a simple exercise for evaluating Open Source Helm charts security and configuration issues. It can be used along with the [Kubescape Bitnami](https://hub.docker.com/r/bitnami/kubescape) CLI tool to generate an OSS Assessment health report.

The Helm chart has the following dependencies:

- **PostgreSQL** version 15.1.1 from [Tanzu Application Catalog](https://app-catalog.vmware.com/catalog/c055cf51-9de0-4a48-b973-c8fd73c05215/branch/7555ef9a-5067-45e4-9649-75f556788c10)
- **Nginx** version 15.14.1 from [Tanzu Application Catalog](https://app-catalog.vmware.com/catalog/4fa334b0-8ee6-4e4f-8284-c9f759fd04ab/branch/4eb63c5b-acee-41f3-9744-60b19320e822)
- **Grafana** version 10.0.3 from [Tanzu Application Catalog](https://app-catalog.vmware.com/catalog/c5f532f6-15b9-4506-90e3-d4a4da4b1f15/branch/9c60f964-d913-4050-8c7e-26eb67384666)
- **Clickhouse** version 5.3.2 from [Tanzu Application Catalog](https://app-catalog.vmware.com/catalog/711fe8cb-03f4-49f3-91ab-d5d3da9829d8/branch/55c0f7a5-4899-43f5-89d1-e074cea2062c)

Each dependency is tagged for easy identification and management.

All these dependencies have an equivalent chart in the [Bitnami Catalog](https://github.com/bitnami/charts).

Alternative versions of the Helm chart can be found here:

* [Upstream dependencies](https://github.com/agarcia-oss/zero-to-hero/)
* [Bitnami charts dependencies](https://github.com/agarcia-oss/zero-to-hero/tree/bitnami)

## Executing the report

```bash
docker run --rm -it -v $HOME:/output \
        bitnami/kubescape:3.0.3 oss-assessment \
        https://github.com/agarcia-oss/zero-to-hero/tree/tac \
        --output /output/report.json
```

## Sample report for this repository

![alt text](image.png)

## Obtaining the OSS Healh Assessmet

TBC
