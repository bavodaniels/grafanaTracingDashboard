Download and run docker-compose up to start the stack

Grafana will be available at localhost:3000
You can use several protocols to push data to Grafana tempo
- 14268  # jaeger ingest
- 3200   # tempo
- 4317  # otlp grpc
- 4318  # otlp http
- 9411   # zipkin

The easiest thing to do to push data is download Opentelemetry agent from
https://github.com/open-telemetry/opentelemetry-java-instrumentation/releases/latest/download/opentelemetry-javaagent.jar

add the agent to your java -jar command and check how to configure the agent here https://github.com/open-telemetry/opentelemetry-java/blob/main/sdk-extensions/autoconfigure/README.md#otlp-exporter-both-span-and-metric-exporters