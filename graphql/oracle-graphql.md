# Oracle Cloud Infrastructure GraphQL Schema

## Overview

This conceptual GraphQL schema represents the Oracle Cloud Infrastructure (OCI) and Oracle Database REST API surface as a unified graph. It is derived from the OCI REST API reference at https://docs.oracle.com/en-us/iaas/api/ and covers the major service domains: Identity and Access Management, Networking, Compute, Storage, Database, Container and Serverless, Messaging and Streaming, Observability, Security, and Cloud Governance.

The schema is conceptual — Oracle does not publish an official GraphQL endpoint. It is intended to support tooling, documentation, and API design work.

## Source APIs

- OCI Identity and Access Management API — https://docs.oracle.com/en-us/iaas/Content/Identity/Concepts/overview.htm
- OCI Compute API — https://docs.oracle.com/en-us/iaas/Content/Compute/Concepts/computeoverview.htm
- OCI Networking API — https://docs.oracle.com/en-us/iaas/Content/Network/Concepts/overview.htm
- OCI Block Volume API — https://docs.oracle.com/en-us/iaas/Content/Block/Concepts/overview.htm
- OCI Object Storage API — https://docs.oracle.com/en-us/iaas/Content/Object/Concepts/objectstorageoverview.htm
- OCI Autonomous Database REST API — https://docs.oracle.com/en/cloud/paas/autonomous-database/serverless/rest-apis.html
- OCI Container Engine for Kubernetes API — https://docs.oracle.com/en-us/iaas/Content/ContEng/Concepts/contengoverview.htm
- OCI Functions API — https://docs.oracle.com/en-us/iaas/Content/Functions/Concepts/functionsoverview.htm
- OCI API Gateway — https://docs.oracle.com/en-us/iaas/Content/APIGateway/Concepts/apigatewayoverview.htm
- OCI Streaming API — https://docs.oracle.com/en-us/iaas/Content/Streaming/Concepts/accessing-streaming.htm
- OCI Queue API — https://docs.oracle.com/en-us/iaas/Content/queue/overview.htm
- OCI Notifications API — https://docs.oracle.com/en-us/iaas/Content/Notification/Concepts/notificationoverview.htm
- OCI Monitoring API — https://docs.oracle.com/en-us/iaas/Content/Monitoring/Concepts/monitoringoverview.htm
- OCI Logging API — https://docs.oracle.com/en-us/iaas/Content/Logging/Concepts/loggingoverview.htm
- OCI Vault API — https://docs.oracle.com/en-us/iaas/Content/KeyManagement/Concepts/keyoverview.htm
- OCI Load Balancer API — https://docs.oracle.com/en-us/iaas/Content/Balance/Concepts/balanceoverview.htm
- OCI DNS API — https://docs.oracle.com/en-us/iaas/Content/DNS/Concepts/dnszonemanagement.htm
- OCI Email Delivery API — https://docs.oracle.com/en-us/iaas/Content/Email/Concepts/overview.htm

## Domain Groupings

### Identity and Access Management
Compartment, Tenancy, User, Group, Policy, IAMPolicy, AuthToken, APIKey, SecretKey, DynamicGroup, IdentityDomain, CustomerSecretKey, OAuth2ClientCredential

### Networking
VCN, Subnet, InternetGateway, NATGateway, ServiceGateway, RouteTable, RouteRule, SecurityList, IngressSecurityRule, EgressSecurityRule, NetworkSecurityGroup, VNic, PrivateIp, PublicIp, DRG, FastConnect, VirtualCircuit, IPSecVPN, CPE, RemotePeeringConnection, LocalPeeringGateway

### Compute
Instance, InstanceConfiguration, InstancePool, Image, Shape, BootVolume, BootVolumeAttachment, VNicAttachment, ConsoleConnection, InstanceConsoleHistory

### Storage
DataVolume, VolumeAttachment, VolumeGroup, VolumeBackup, FileSystem, MountTarget, Export, ExportSet, Bucket, StoredObject, MultipartUpload, PreAuthenticatedRequest

### Database
Database, DatabaseSystem, DbHome, DbNode, ExadataInfrastructure, AutonomousDatabase, AutonomousContainerDatabase, AutonomousExadataInfrastructure, DataWarehouse, Backup, DatabaseUpgradeHistory, MySQLDbSystem

### Container and Serverless
Cluster, NodePool, OKENode, ContainerRepository, ContainerImage, Function, FunctionApplication, APIGateway, APIDeployment, APIRoute

### Messaging and Streaming
Stream, StreamPool, Queue, NotificationTopic, Subscription, StreamMessage

### Observability
Metric, MetricDataPoint, Alarm, AlarmStatus, LogGroup, Log, LogConfiguration, AuditEvent, LogAnalyticsNamespace

### Security
VaultKey, Secret, SecretBundle, WAFPolicy, WAFRule, CertificateAuthority, Certificate

### Governance
Tag, TagNamespace, TagDefault, Cost, CostReport, Budget, Region, AvailabilityDomain, FaultDomain, Subscription

## Type Count

This schema defines 82 types across 10 service domains.

## Schema File

See `oracle-schema.graphql` in this directory for the full GraphQL SDL definition.
