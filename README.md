# Lalith Lochan Muppalla

I'm a software engineer working on backend services and distributed data processing with Go, Java, and Kafka.

## What I work on

On Verizon Data Mediation, I contribute to services that ingest files, process records, and deliver data to downstream systems. My work includes code and configuration changes, Kafka consumer behavior, production troubleshooting, and Python scripts for testing and reprocessing.

I work with SQL and Oracle, and with services deployed on Kubernetes and OpenShift using Helm and Argo CD. For monitoring and investigation, I use OpenTelemetry metrics exported for Prometheus, along with Grafana and Kibana.

## Selected personal projects

### [Nimbus](https://github.com/lalith-99/nimbus-app)

A Go notification service with REST and gRPC APIs, PostgreSQL, Redis, background workers, retries, and dead-letter recovery. It includes email, SMS, and webhook integrations, an optional SQS path, and Terraform infrastructure definitions.

The local webhook demo exercises request creation, replay, failed delivery, retries, and recovery. The architecture notes explain database claims, request deduplication, and the failure windows that can still produce duplicate sends.

[Run the local demo](https://github.com/lalith-99/nimbus-app/blob/main/docs/LOCAL_DEMO.md) · [Architecture](https://github.com/lalith-99/nimbus-app/blob/main/docs/ARCHITECTURE.md) · [CI checks](https://github.com/lalith-99/nimbus-app/actions/workflows/ci.yml)

### [EchoStream](https://github.com/lalith-99/echostream)

A Go and React chat application with REST APIs, WebSockets, PostgreSQL message history, Redis pub/sub, and JWT authentication.

The project separates saved message history from best-effort live delivery. Its documentation covers the local setup, message flow, and current limits around presence, authorization, and delivery across instances.

[Local setup](https://github.com/lalith-99/echostream#quick-start) · [Architecture](https://github.com/lalith-99/echostream/blob/main/docs/ARCHITECTURE.md)

## Connect

I'm interested in Software Engineer II opportunities involving backend development, APIs, distributed processing, or platform services.

[LinkedIn](https://www.linkedin.com/in/lalithmuppalla/)
