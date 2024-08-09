# Flink

Apache Flink is a stream processing framework designed for real-time data processing and analytics. It provides powerful tools for handling large volumes of data with low latency and high throughput.

## Key Concepts

### Streams vs. Batch

- **Streams**: Flink primarily processes data streams in real-time, allowing you to handle continuous data flows.
- **Batch**: While Flink’s primary focus is on streaming, it also supports batch processing for discrete datasets.

### Data Sources and Sinks

- **Sources**: Learn how to ingest data from Kafka topics, files, or other data sources.
- **Sinks**: Understand how to write processed data to various destinations, like ClickHouse or other databases.

### Transformations
- **Map**: Apply a function to each element in the stream.
- **Filter**: Exclude elements that don’t meet certain criteria.
- **Reduce/Aggregate**: Combine elements to produce a summary value.
- **Windowing**: Group events based on time or count to apply transformations over subsets of data.

### Windowing

- **Tumbling Windows**: Fixed-size, non-overlapping windows.
- **Sliding Windows**: Overlapping windows that slide over time.
- **Session Windows**: Windows based on gaps of inactivity between events

### State Management
- **Keyed State**: Store and manage state specific to each key in your data stream.
- **Operator State**: Manage state that is not tied to specific keys but to the operators themselves.

### Event vs. Processing Time

- **Event Time**: Time when events actually occur (useful for handling late data).
- **Processing Time**: Time when events are processed by the Flink job.

When to use what?
- Use **Processing Time** if you need low latency and real-time processing where the exact timing of events is less critical.
- Use **Event Time** if your application needs to respect the original timestamps of events, manage late or out-of-order events, and ensure accurate time-based processing.
In short, **processing** time prefer **latency** and **event** time prefer **accuracy**.

### Fault Tolerance

- **Checkpointing**: Periodically save the state of your application to recover from failures.
- **Savepoints**: Manual snapshots of your job’s state for planned upgrades or recovery.

### Job Management

- **Job Graph**: Understand how Flink jobs are represented as directed acyclic graphs of operations.
- **Cluster Management**: Learn how to deploy and manage Flink clusters, including scaling and monitoring.

## Implementation
TODO