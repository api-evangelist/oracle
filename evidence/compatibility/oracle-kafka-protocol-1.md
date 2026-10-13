<!-- fetched 2026-10-13 from https://docs.oracle.com/en-us/iaas/Content/Streaming/Tasks/kafkacompatibility.htm by sweep-shape-compat.py; text extracted from the provider's own page -->

Using Streaming with Apache Kafka 
 Oracle Cloud Infrastructure Documentation
 All Pages
 Skip to main content 
 Using Streaming with Apache Kafka
 Use Apache Kafka with Oracle Cloud Infrastructure Streaming.
Oracle Cloud Infrastructure Streaming lets users of Apache Kafka offload the setup, maintenance, and infrastructure management that hosting your own Zookeeper and Kafka cluster requires.
Streaming is compatible with most Kafka APIs, allowing you to use applications written for Kafka to send messages to and receive messages from the Streaming service without having to rewrite your code. See Using Kafka APIs for more information.
Streaming can also use the Kafka Connect ecosystem to interface directly with external sources such as databases, object stores, or any microservice on the Oracle Cloud. Kafka connectors can easily and automatically create, publish to, and deliver topics while taking advantage of the Streaming service's high throughput and durability. See Using Kafka Connect for more information.
 Use cases for Streaming and Kafka include:
 Move data from Streaming to Autonomous AI Lakehouse through the JDBC Connector to perform advanced analytics and visualization.
 Use the Oracle GoldenGate connector for Big Data Service to build an event-driven application.
 Move data from Streaming to Oracle Object Storage through the HDFS/S3 Connector for long term storage, or to run Hadoop/Spark jobs.
 Kafka API Support
Streaming is fully upstream compatible with the latest
 versions of Kafka APIs. Streaming supports the following
 Kafka APIs:
 Producer (v0.10.0 and later)
 Consumer (v0.10.0 and later)
 Connect (v0.10.0.0 and later)
 Admin (v0.10.1.0 and later)
 Group Management (v0.10.0 and later)
 The following Kafka APIs and features are not yet implemented in the Streaming service:
 Kafka Streams 
 Compaction 
 Transactions 
 Dynamic Partition Addition 
 Idempotent production 
 Kafka Clients
 While many Kafka clients are available, we recommend the clients that have been
 fully tested and certified to work with the Streaming
 service.
Streaming supports all versions of apache-kafka-java .
Streaming also supports the following Kafka clients on a
 best-effort basis:
 librdkafka 
 confluent-kafka-python 
 Requirements and Limitations
 The implementation of the Kafka compatibility in Streaming results in the following configurations, limitations, and behaviors.
 Lossless Configuration
Streaming only supports lossless Kafka
 configurations. Data is replicated three ways. Messages from producers do not
 initiate an acknowledgment (ACK) from Streaming
 until at least two replicas are in sync. 
 Unique Stream Names
 If you have streams with the same names in a compartment, you can't use Kafka with Streaming until you delete the duplicated streams, unless the streams are in different stream pools . Two streams with the same name can exist in the same compartment only if the streams are in different stream pools.
 Duplicate stream names otherwise manifest through an "authentication
 failed" error. If you do not want to delete your streams, contact the Streaming team so we can rename your streams without
 data loss.
 Load Balancing Connection Recycling
 Because the Kafka protocol uses long-lived TCP connections, the Streaming Kafka compatibility layer implements a
 load balancing mechanism to periodically balance connections between front-end
 nodes. This mechanism periodically closes connections to force new ones. Most Kafka
 SDKs handle these disconnections automatically when consuming, but producing to Streaming using the Kafka API might raise
 disconnection errors. Disconnections can be mitigated by adding retries to your
 requests. Retries are part of the Kafka SDK and are automatically enabled, and you
 can explicitly configure their behavior.
 Using Streaming with Apache Kafka
 Kafka API Support
 Kafka Clients
 Requirements and Limitations
 Copyright © 2026, Oracle and/or its affiliates. 
 About Oracle 
 Contact Us 
 Legal Notices 
 Terms of Use & Privacy 
 Document Conventions
