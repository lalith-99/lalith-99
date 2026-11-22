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

I built EchoStream, a Go and React chat app, to explore what happens when a send succeeds but the connection drops before the client sees the response. The API commits a message and its outbox entry together in PostgreSQL. A retry with the same key returns the saved message. WebSockets and Redis handle live updates, and the browser fetches missed messages by ID when it reconnects.

I tested the recovery path with Redis stopped and two API instances running. In a separate local k6 run, 20 subscribers connected to one instance received all 10 messages sent through the other.

[Run EchoStream](https://github.com/lalith-99/echostream#run-it) · [Recovery test](https://github.com/lalith-99/echostream/blob/main/scripts/recovery.mjs) · [Benchmark and results](https://github.com/lalith-99/echostream/blob/main/docs/benchmarks/README.md)

## Connect

I'm interested in Software Engineer II opportunities involving backend development, APIs, distributed processing, or platform services.

[LinkedIn](https://www.linkedin.com/in/lalithmuppalla/)
