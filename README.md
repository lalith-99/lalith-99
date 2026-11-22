# Lalith Lochan Muppalla

I'm a software engineer working on backend services and distributed data processing with Go, Java, and Kafka.

## What I work on

On Verizon Data Mediation, I contribute to Go and Java services that ingest telecom files, process records, and deliver data to billing and analytics systems. My work spans Spring Boot REST APIs, Kafka consumers, Redis duplicate checks, and Oracle ingestion and reporting. I work on retries, bounded concurrency, database batching, and recovery from failed or backlogged processing.

I also contribute to file lifecycle services and Jenkins, Docker, and Argo CD releases on Kubernetes and OpenShift. I use Python for testing and operational reprocessing. For monitoring, I export application metrics with OpenTelemetry for Prometheus and use Grafana and Kibana to investigate failures and bottlenecks.

## Selected personal projects

### [Nimbus](https://github.com/lalith-99/nimbus-app)

I built a Go notification service with REST and gRPC APIs, Redis request deduplication, and PostgreSQL workers that retry failed sends. A worker used to sleep for five seconds after each batch of ten. Letting it keep polling while work was ready cut the median time to deliver a 200-webhook burst from **99.49 to 4.39 seconds** in matched local CI tests. A separate run delivered all 10,000 webhooks in 23.8 seconds, with zero missing or duplicate receipts.

Indexing jobs by their next eligible time also kept workers from scanning rows they could not claim. On a local PostgreSQL queue with one million rows, eight workers claimed the 4,000 eligible jobs **7.6–7.7× faster** across two trial pairs.

[Webhook workload and results](https://github.com/lalith-99/nimbus-app/blob/bc5015e037da290a545961b3072ad31864bedbbd/docs/performance/webhook-load.md) · [Worker claim benchmark](https://github.com/lalith-99/nimbus-app/blob/64e8bf210878ef6658493710413326a5f4533468/docs/performance/worker-claims.md) · [Run Nimbus](https://github.com/lalith-99/nimbus-app/blob/main/docs/LOCAL_DEMO.md)

### [EchoStream](https://github.com/lalith-99/echostream)

I built a Go and React chat service that commits each message and its outbox entry together in PostgreSQL. Redis distributes live updates across gateways, and a reconnecting client fetches missed messages by ID.

At 256 WebSocket connections, checking channel membership once per recipient was slowing down live delivery. I batched concurrent checks while keeping permissions fresh. In a matched two-gateway test on one CI runner, that cut membership queries **93.5%** and reduced the median of the trial p95 send-to-receipt times from **237 to 79 ms**. Each revision delivered all 516,096 expected reader-message pairs with zero duplicates.

[Fan-out workload and results](https://github.com/lalith-99/echostream/blob/9ec7a7ff07f440813a5a406fe1e23939c32a7fdc/docs/benchmarks/fanout-load.md) · [Measured comparison](https://github.com/lalith-99/echostream/actions/runs/45034011449/job/137243619864) · [Run EchoStream](https://github.com/lalith-99/echostream#run-it)

## Connect

I'm interested in Software Engineer II opportunities involving backend development, APIs, distributed processing, or platform services.

[LinkedIn](https://www.linkedin.com/in/lalithmuppalla/)
