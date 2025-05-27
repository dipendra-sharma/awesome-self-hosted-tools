# SigNoz - Open Source Datadog Alternative

SigNoz is an open-source observability platform native to OpenTelemetry with logs, traces and metrics in a single application.

## Features

- **Unified Observability**: Metrics, traces, and logs in a single pane of glass
- **OpenTelemetry Native**: Built for modern cloud-native environments
- **Cost Effective**: Up to 80% cost savings compared to Datadog
- **Advanced Querying**: SQL-like query language for filtering and aggregation
- **Custom Dashboards**: Rich visualization capabilities
- **Alerting**: Intelligent alerting with multiple notification channels

## Quick Start

1. Run the service:
   ```bash
   docker compose up -d
   ```

2. Access SigNoz at http://localhost:8631

3. Configure data sources and start monitoring your applications

## Configuration

- **Frontend**: Port 8631 - Main UI interface
- **OTLP gRPC**: Port 8629 - For sending telemetry data
- **OTLP HTTP**: Port 8630 - For sending telemetry data via HTTP
- **Database**: ClickHouse for metrics and traces storage
- **Messaging**: Zookeeper for coordination

## Services Included

- **ClickHouse**: Time-series database for storing metrics and traces
- **Zookeeper**: Coordination service for ClickHouse
- **OTEL Collector**: Receives and processes telemetry data
- **Query Service**: Processes queries and provides API
- **Alert Manager**: Handles alerting and notifications
- **Frontend**: Web UI for visualization and management

## Application Integration

Send telemetry data to SigNoz using OpenTelemetry SDKs:

### Python Example
```python
from opentelemetry import trace
from opentelemetry.exporter.otlp.proto.grpc.trace_exporter import OTLPSpanExporter
from opentelemetry.sdk.trace import TracerProvider
from opentelemetry.sdk.trace.export import BatchSpanProcessor

trace.set_tracer_provider(TracerProvider())
tracer = trace.get_tracer(__name__)

otlp_exporter = OTLPSpanExporter(endpoint="http://localhost:8629")
span_processor = BatchSpanProcessor(otlp_exporter)
trace.get_tracer_provider().add_span_processor(span_processor)
```

### Node.js Example
```javascript
const { NodeSDK } = require('@opentelemetry/sdk-node');
const { OTLPTraceExporter } = require('@opentelemetry/exporter-otlp-grpc');

const sdk = new NodeSDK({
  traceExporter: new OTLPTraceExporter({
    url: 'http://localhost:8629',
  }),
});

sdk.start();
```

## Use Cases

- **Application Performance Monitoring**: Track request latency, error rates, throughput
- **Distributed Tracing**: Trace requests across microservices
- **Infrastructure Monitoring**: Monitor system metrics and resource usage
- **Log Analytics**: Centralized logging with correlation to traces
- **Custom Metrics**: Business-specific metrics and KPIs

## Production Considerations

- Ensure adequate resources for ClickHouse (recommended: 4GB+ RAM)
- Configure persistent storage for data retention
- Set up regular backups of ClickHouse data
- Configure proper authentication and access controls
- Use HTTPS in production environments

## Enterprise Features

- SAML/SSO integration
- Advanced user management
- Custom retention policies
- High availability setup
- Advanced security features

## License

AGPL v3 (Open Source) / Commercial License Available