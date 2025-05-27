# Jaeger - Distributed Tracing System

Jaeger is an open-source distributed tracing platform used for monitoring and troubleshooting microservices-based distributed systems.

## Features

- **Distributed Tracing**: Track requests across multiple services
- **Performance Monitoring**: Identify bottlenecks and latency issues
- **Dependency Analysis**: Visualize service dependencies
- **Root Cause Analysis**: Pinpoint issues in complex systems
- **OpenTelemetry Support**: Native OTLP protocol support
- **Zipkin Compatibility**: Compatible with Zipkin clients
- **Storage Backends**: Memory, Cassandra, Elasticsearch, Kafka

## Quick Start

1. Run the service:
   ```bash
   docker compose up -d
   ```

2. Access Jaeger UI at http://localhost:8633

3. Start sending traces to the collector endpoints

## Configuration

- **UI**: Port 8633 - Jaeger web interface
- **OTLP gRPC**: Port 8634 - OpenTelemetry gRPC endpoint
- **OTLP HTTP**: Port 8635 - OpenTelemetry HTTP endpoint
- **Jaeger Agent UDP**: Port 8636 - Legacy Jaeger thrift compact
- **Jaeger Agent UDP**: Port 8637 - Legacy Jaeger thrift binary
- **Jaeger Agent HTTP**: Port 8638 - Agent configuration
- **Jaeger Collector**: Port 8639 - Direct span submission
- **Zipkin**: Port 8640 - Zipkin compatible endpoint

## Application Integration

### OpenTelemetry (Recommended)

#### Python
```python
from opentelemetry import trace
from opentelemetry.exporter.otlp.proto.grpc.trace_exporter import OTLPSpanExporter
from opentelemetry.sdk.trace import TracerProvider
from opentelemetry.sdk.trace.export import BatchSpanProcessor

trace.set_tracer_provider(TracerProvider())
tracer = trace.get_tracer(__name__)

otlp_exporter = OTLPSpanExporter(endpoint="http://localhost:8634")
span_processor = BatchSpanProcessor(otlp_exporter)
trace.get_tracer_provider().add_span_processor(span_processor)
```

#### Node.js
```javascript
const { NodeSDK } = require('@opentelemetry/sdk-node');
const { OTLPTraceExporter } = require('@opentelemetry/exporter-otlp-grpc');

const sdk = new NodeSDK({
  traceExporter: new OTLPTraceExporter({
    url: 'http://localhost:8634',
  }),
});

sdk.start();
```

#### Java
```java
import io.opentelemetry.exporter.otlp.trace.OtlpGrpcSpanExporter;
import io.opentelemetry.sdk.OpenTelemetrySdk;
import io.opentelemetry.sdk.trace.SdkTracerProvider;

SdkTracerProvider tracerProvider = SdkTracerProvider.builder()
    .addSpanProcessor(BatchSpanProcessor.builder(
        OtlpGrpcSpanExporter.builder()
            .setEndpoint("http://localhost:8634")
            .build())
        .build())
    .build();

OpenTelemetrySdk.builder()
    .setTracerProvider(tracerProvider)
    .buildAndRegisterGlobal();
```

### Legacy Jaeger Clients

#### Go
```go
import (
    "github.com/uber/jaeger-client-go"
    "github.com/uber/jaeger-client-go/config"
)

cfg := config.Configuration{
    ServiceName: "my-service",
    Sampler: &config.SamplerConfig{
        Type:  "const",
        Param: 1,
    },
    Reporter: &config.ReporterConfig{
        CollectorEndpoint: "http://localhost:8639/api/traces",
    },
}

tracer, closer, err := cfg.NewTracer()
```

## Key Concepts

### Traces
A trace represents the journey of a request through your system, consisting of one or more spans.

### Spans
A span represents a single operation within a trace, with start/end times and metadata.

### Tags and Logs
- **Tags**: Key-value pairs that provide metadata about spans
- **Logs**: Timestamped events with structured data

## Use Cases

- **Microservices Monitoring**: Track requests across service boundaries
- **Performance Optimization**: Identify slow operations and bottlenecks
- **Error Investigation**: Trace errors back to their source
- **Dependency Mapping**: Visualize service relationships
- **SLA Monitoring**: Ensure services meet performance requirements

## Best Practices

### Instrumentation
- Instrument at service boundaries (HTTP, RPC calls)
- Add business logic spans for critical operations
- Include relevant tags (user_id, operation_type, etc.)
- Avoid over-instrumentation (balance detail vs. overhead)

### Sampling
- Use probabilistic sampling for high-throughput services
- Sample more aggressively in production
- Consider adaptive sampling strategies

### Tags and Naming
- Use consistent naming conventions
- Include relevant context in span names
- Add tags for filtering and grouping

## Production Considerations

- **Storage**: This all-in-one setup uses in-memory storage
- **Persistence**: For production, use Cassandra or Elasticsearch
- **Sampling**: Configure appropriate sampling rates
- **Security**: Implement authentication and authorization
- **Performance**: Monitor Jaeger's own resource usage

## Integration with Other Tools

- **Prometheus**: Export metrics from trace data
- **Grafana**: Visualize tracing data alongside metrics
- **Alerting**: Set up alerts based on trace data
- **CI/CD**: Include tracing in deployment pipelines

## Troubleshooting

### Common Issues
- No traces appearing: Check collector endpoints and network connectivity
- High memory usage: Adjust sampling rates and span retention
- Missing spans: Verify instrumentation and context propagation

### Health Checks
- UI health: http://localhost:8633
- Collector metrics: Available through various endpoints

## License

Apache License 2.0