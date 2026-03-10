# Linode API SDK (linodego) Gap Report

Auto-generated gap analysis comparing the [Linode OpenAPI specification](https://github.com/linode/linode-api-openapi)
against the [linodego](https://github.com/linode/linodego) Go SDK implementation.

## Executive Summary

| Metric | Count |
|--------|-------|
| Total API endpoints (from OpenAPI spec) | 465 |
| Implemented in SDK | 396 |
| Missing from SDK | 69 |
| Endpoint coverage | 85.2% |
| SDK methods without matching OpenAPI endpoint | 26 |

## Coverage by Category

| Category | Total | Implemented | Missing | Coverage |
|----------|-------|-------------|---------|----------|
| Access keys | 5 | 5 | 0 | 100% |
| Account | 3 | 2 | 1 | 67% |
| Account agreements | 2 | 2 | 0 | 100% |
| Account availability | 2 | 2 | 0 | 100% |
| Account settings | 3 | 2 | 1 | 67% |
| Account transfer | 1 | 1 | 0 | 100% |
| Advanced parameters | 2 | 2 | 0 | 100% |
| Alerts | 7 | 7 | 0 | 100% |
| Attachments | 1 | 0 | 1 | 0% |
| Backups | 6 | 6 | 0 | 100% |
| Beta programs | 5 | 5 | 0 | 100% |
| Buckets | 12 | 11 | 1 | 92% |
| Child accounts | 3 | 3 | 0 | 100% |
| Cluster dashboard | 1 | 1 | 0 | 100% |
| Clusters | 9 | 9 | 0 | 100% |
| Configuration profile interfaces | 6 | 6 | 0 | 100% |
| Configuration profiles | 5 | 5 | 0 | 100% |
| Configurations | 6 | 6 | 0 | 100% |
| Control Plane ACL | 3 | 3 | 0 | 100% |
| Credentials | 4 | 4 | 0 | 100% |
| Databases | 17 | 17 | 0 | 100% |
| Devices | 4 | 4 | 0 | 100% |
| Disks | 8 | 8 | 0 | 100% |
| Domain zone file | 1 | 1 | 0 | 100% |
| Domains | 7 | 7 | 0 | 100% |
| Endpoints | 1 | 1 | 0 | 100% |
| Engines | 2 | 2 | 0 | 100% |
| Entity transfers | 5 | 0 | 5 | 0% |
| Events | 3 | 3 | 0 | 100% |
| Firewall settings | 2 | 2 | 0 | 100% |
| Firewalls | 14 | 9 | 5 | 64% |
| Grants | 1 | 1 | 0 | 100% |
| IP addresses | 13 | 13 | 0 | 100% |
| IPv4 addresses | 2 | 0 | 2 | 0% |
| IPv6 pools | 1 | 1 | 0 | 100% |
| IPv6 ranges | 4 | 4 | 0 | 100% |
| Identity Management | 4 | 4 | 0 | 100% |
| Image sharing | 22 | 21 | 1 | 95% |
| Images | 7 | 7 | 0 | 100% |
| Invoices | 3 | 3 | 0 | 100% |
| Kernels | 2 | 2 | 0 | 100% |
| Kubeconfigs | 2 | 2 | 0 | 100% |
| LKE API endpoints | 1 | 1 | 0 | 100% |
| LKE service tokens | 1 | 1 | 0 | 100% |
| LKE types | 1 | 1 | 0 | 100% |
| LKE versions | 4 | 4 | 0 | 100% |
| Linode instances | 15 | 15 | 0 | 100% |
| Linode interfaces | 10 | 9 | 1 | 90% |
| Linode types | 2 | 2 | 0 | 100% |
| Logins | 4 | 4 | 0 | 100% |
| Logs | 12 | 0 | 12 | 0% |
| Longview clients | 5 | 5 | 0 | 100% |
| Longview plans | 2 | 2 | 0 | 100% |
| Longview subscriptions | 2 | 2 | 0 | 100% |
| Longview types | 1 | 0 | 1 | 0% |
| Maintenance policies | 1 | 1 | 0 | 100% |
| Maintenances | 1 | 1 | 0 | 100% |
| Managed Linode settings | 3 | 0 | 3 | 0% |
| Managed SSH keys | 1 | 0 | 1 | 0% |
| Managed contacts | 5 | 0 | 5 | 0% |
| Managed credentials | 6 | 0 | 6 | 0% |
| Managed issues | 2 | 0 | 2 | 0% |
| Managed service monitors | 7 | 0 | 7 | 0% |
| Managed statistics | 1 | 0 | 1 | 0% |
| Metrics | 8 | 7 | 1 | 88% |
| Network transfer prices | 1 | 1 | 0 | 100% |
| Node pools | 6 | 6 | 0 | 100% |
| NodeBalancer types | 1 | 1 | 0 | 100% |
| NodeBalancers | 6 | 6 | 0 | 100% |
| Nodes | 8 | 8 | 0 | 100% |
| Notifications | 1 | 1 | 0 | 100% |
| OAuth apps | 3 | 3 | 0 | 100% |
| OAuth client | 2 | 0 | 2 | 0% |
| OAuth clients | 6 | 6 | 0 | 100% |
| OAuth preferences | 2 | 2 | 0 | 100% |
| Object Storage | 6 | 5 | 1 | 83% |
| Payment methods | 5 | 4 | 1 | 80% |
| Payments | 6 | 3 | 3 | 50% |
| Personal access tokens | 5 | 5 | 0 | 100% |
| Phone number | 3 | 3 | 0 | 100% |
| Placement groups | 7 | 7 | 0 | 100% |
| Profile | 2 | 2 | 0 | 100% |
| Promo credits | 1 | 1 | 0 | 100% |
| Records | 5 | 5 | 0 | 100% |
| Regions | 4 | 4 | 0 | 100% |
| Replies | 2 | 0 | 2 | 0% |
| SSH keys | 5 | 5 | 0 | 100% |
| SSL certificates | 2 | 2 | 0 | 100% |
| Security questions | 2 | 2 | 0 | 100% |
| Service transfers | 5 | 5 | 0 | 100% |
| StackScripts | 5 | 5 | 0 | 100% |
| Statistics | 5 | 5 | 0 | 100% |
| Support tickets | 4 | 2 | 2 | 50% |
| TLS/SSL certificates | 3 | 3 | 0 | 100% |
| Tags | 4 | 4 | 0 | 100% |
| Templates | 2 | 2 | 0 | 100% |
| Trusted devices | 3 | 3 | 0 | 100% |
| Two-factor authentication | 3 | 3 | 0 | 100% |
| Types | 2 | 2 | 0 | 100% |
| Users | 7 | 7 | 0 | 100% |
| VLANs | 2 | 1 | 1 | 50% |
| VPC subnets | 5 | 5 | 0 | 100% |
| VPCs | 7 | 7 | 0 | 100% |
| Volume types | 1 | 1 | 0 | 100% |
| Volumes | 10 | 10 | 0 | 100% |

## Endpoint Coverage Detail

### Access keys

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `object-storage/keys` | ✅ Implemented | ListObjectStorageKeys |  |
| POST | `object-storage/keys` | ✅ Implemented | CreateObjectStorageKey |  |
| DELETE | `object-storage/keys/{keyId}` | ✅ Implemented | DeleteObjectStorageKey |  |
| GET | `object-storage/keys/{keyId}` | ✅ Implemented | GetObjectStorageKey |  |
| PUT | `object-storage/keys/{keyId}` | ✅ Implemented | UpdateObjectStorageKey |  |

### Account

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `account` | ✅ Implemented | GetAccount |  |
| PUT | `account` | ✅ Implemented | UpdateAccount |  |
| POST | `account/cancel` | ❌ Missing |  | Delete your account |

### Account agreements

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `account/agreements` | ✅ Implemented | GetAccountAgreements |  |
| POST | `account/agreements` | ✅ Implemented | AcknowledgeAccountAgreements |  |

### Account availability

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `account/availability` | ✅ Implemented | ListAccountAvailabilities |  |
| GET | `account/availability/{regionId}` | ✅ Implemented | GetAccountAvailability |  |

### Account settings

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `account/settings` | ✅ Implemented | GetAccountSettings |  |
| PUT | `account/settings` | ✅ Implemented | UpdateAccountSettings |  |
| POST | `account/settings/managed-enable` | ❌ Missing |  | Enable Linode Managed |

### Account transfer

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `account/transfer` | ✅ Implemented | GetAccountTransfer |  |

### Advanced parameters

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `databases/mysql/config` | ✅ Implemented | GetMySQLDatabaseConfig |  |
| GET | `databases/postgresql/config` | ✅ Implemented | GetPostgresDatabaseConfig |  |

### Alerts

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `monitor/alert-channels` | ✅ Implemented | ListAlertChannels |  |
| GET | `monitor/alert-definitions` | ✅ Implemented | ListAllMonitorAlertDefinitions |  |
| GET | `monitor/services/{serviceType}/alert-definitions` | ✅ Implemented | ListMonitorAlertDefinitions |  |
| POST | `monitor/services/{serviceType}/alert-definitions` | ✅ Implemented | CreateMonitorAlertDefinition |  |
| DELETE | `monitor/services/{serviceType}/alert-definitions/{alertId}` | ✅ Implemented | DeleteMonitorAlertDefinition |  |
| GET | `monitor/services/{serviceType}/alert-definitions/{alertId}` | ✅ Implemented | GetMonitorAlertDefinition |  |
| PUT | `monitor/services/{serviceType}/alert-definitions/{alertId}` | ✅ Implemented | UpdateMonitorAlertDefinition |  |

### Attachments

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| POST | `support/tickets/{ticketId}/attachments` | ❌ Missing |  | Create a support ticket attachment |

### Backups

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `linode/instances/{linodeId}/backups` | ✅ Implemented | GetInstanceBackups |  |
| POST | `linode/instances/{linodeId}/backups` | ✅ Implemented | CreateInstanceSnapshot |  |
| POST | `linode/instances/{linodeId}/backups/cancel` | ✅ Implemented | CancelInstanceBackups |  |
| POST | `linode/instances/{linodeId}/backups/enable` | ✅ Implemented | EnableInstanceBackups |  |
| GET | `linode/instances/{linodeId}/backups/{backupId}` | ✅ Implemented | GetInstanceSnapshot |  |
| POST | `linode/instances/{linodeId}/backups/{backupId}/restore` | ✅ Implemented | RestoreInstanceBackup |  |

### Beta programs

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `account/betas` | ✅ Implemented | ListAccountBetaPrograms |  |
| POST | `account/betas` | ✅ Implemented | JoinBetaProgram |  |
| GET | `account/betas/{betaId}` | ✅ Implemented | GetAccountBetaProgram |  |
| GET | `betas` | ✅ Implemented | ListBetaPrograms |  |
| GET | `betas/{betaId}` | ✅ Implemented | GetBetaProgram |  |

### Buckets

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `object-storage/buckets` | ✅ Implemented | ListObjectStorageBuckets |  |
| POST | `object-storage/buckets` | ✅ Implemented | CreateObjectStorageBucket |  |
| GET | `object-storage/buckets/{regionId}` | ✅ Implemented | ListObjectStorageBucketsInCluster |  |
| DELETE | `object-storage/buckets/{regionId}/{bucket}` | ✅ Implemented | DeleteObjectStorageBucket |  |
| GET | `object-storage/buckets/{regionId}/{bucket}` | ✅ Implemented | GetObjectStorageBucket |  |
| GET | `object-storage/buckets/{regionId}/{bucket}/access` | ✅ Implemented | GetObjectStorageBucketAccess, GetObjectStorageBucketAccessV2 |  |
| POST | `object-storage/buckets/{regionId}/{bucket}/access` | ✅ Implemented | UpdateObjectStorageBucketAccess |  |
| PUT | `object-storage/buckets/{regionId}/{bucket}/access` | ❌ Missing |  | Update access to an Object Storage bucket |
| GET | `object-storage/buckets/{regionId}/{bucket}/object-acl` | ✅ Implemented | GetObjectStorageObjectACLConfig, GetObjectStorageObjectACLConfigV2 |  |
| PUT | `object-storage/buckets/{regionId}/{bucket}/object-acl` | ✅ Implemented | UpdateObjectStorageObjectACLConfig, UpdateObjectStorageObjectACLConfigV2 |  |
| GET | `object-storage/buckets/{regionId}/{bucket}/object-list` | ✅ Implemented | ListObjectStorageBucketContents |  |
| POST | `object-storage/buckets/{regionId}/{bucket}/object-url` | ✅ Implemented | CreateObjectStorageObjectURL |  |

### Child accounts

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `account/child-accounts` | ✅ Implemented | ListChildAccounts |  |
| GET | `account/child-accounts/{euuId}` | ✅ Implemented | GetChildAccount |  |
| POST | `account/child-accounts/{euuId}/token` | ✅ Implemented | CreateChildAccountToken |  |

### Cluster dashboard

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `lke/clusters/{clusterId}/dashboard` | ✅ Implemented | GetLKEClusterDashboard |  |

### Clusters

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `lke/clusters` | ✅ Implemented | ListLKEClusters |  |
| POST | `lke/clusters` | ✅ Implemented | CreateLKECluster |  |
| DELETE | `lke/clusters/{clusterId}` | ✅ Implemented | DeleteLKECluster |  |
| GET | `lke/clusters/{clusterId}` | ✅ Implemented | GetLKECluster |  |
| PUT | `lke/clusters/{clusterId}` | ✅ Implemented | UpdateLKECluster |  |
| POST | `lke/clusters/{clusterId}/recycle` | ✅ Implemented | RecycleLKEClusterNodes |  |
| POST | `lke/clusters/{clusterId}/regenerate` | ✅ Implemented | RegenerateLKECluster |  |
| GET | `object-storage/clusters` | ✅ Implemented | ListObjectStorageClusters |  |
| GET | `object-storage/clusters/{clusterId}` | ✅ Implemented | GetObjectStorageCluster |  |

### Configuration profile interfaces

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `linode/instances/{linodeId}/configs/{configId}/interfaces` | ✅ Implemented | ListInstanceConfigInterfaces |  |
| POST | `linode/instances/{linodeId}/configs/{configId}/interfaces` | ✅ Implemented | AppendInstanceConfigInterface |  |
| POST | `linode/instances/{linodeId}/configs/{configId}/interfaces/order` | ✅ Implemented | ReorderInstanceConfigInterfaces |  |
| DELETE | `linode/instances/{linodeId}/configs/{configId}/interfaces/{interfaceId}` | ✅ Implemented | DeleteInstanceConfigInterface |  |
| GET | `linode/instances/{linodeId}/configs/{configId}/interfaces/{interfaceId}` | ✅ Implemented | GetInstanceConfigInterface |  |
| PUT | `linode/instances/{linodeId}/configs/{configId}/interfaces/{interfaceId}` | ✅ Implemented | UpdateInstanceConfigInterface |  |

### Configuration profiles

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `linode/instances/{linodeId}/configs` | ✅ Implemented | ListInstanceConfigs |  |
| POST | `linode/instances/{linodeId}/configs` | ✅ Implemented | CreateInstanceConfig |  |
| DELETE | `linode/instances/{linodeId}/configs/{configId}` | ✅ Implemented | DeleteInstanceConfig |  |
| GET | `linode/instances/{linodeId}/configs/{configId}` | ✅ Implemented | GetInstanceConfig |  |
| PUT | `linode/instances/{linodeId}/configs/{configId}` | ✅ Implemented | UpdateInstanceConfig |  |

### Configurations

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `nodebalancers/{nodeBalancerId}/configs` | ✅ Implemented | ListNodeBalancerConfigs |  |
| POST | `nodebalancers/{nodeBalancerId}/configs` | ✅ Implemented | CreateNodeBalancerConfig |  |
| DELETE | `nodebalancers/{nodeBalancerId}/configs/{configId}` | ✅ Implemented | DeleteNodeBalancerConfig |  |
| GET | `nodebalancers/{nodeBalancerId}/configs/{configId}` | ✅ Implemented | GetNodeBalancerConfig |  |
| PUT | `nodebalancers/{nodeBalancerId}/configs/{configId}` | ✅ Implemented | UpdateNodeBalancerConfig |  |
| POST | `nodebalancers/{nodeBalancerId}/configs/{configId}/rebuild` | ✅ Implemented | RebuildNodeBalancerConfig |  |

### Control Plane ACL

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| DELETE | `lke/clusters/{clusterId}/control_plane_acl` | ✅ Implemented | DeleteLKEClusterControlPlaneACL |  |
| GET | `lke/clusters/{clusterId}/control_plane_acl` | ✅ Implemented | GetLKEClusterControlPlaneACL |  |
| PUT | `lke/clusters/{clusterId}/control_plane_acl` | ✅ Implemented | UpdateLKEClusterControlPlaneACL |  |

### Credentials

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `databases/mysql/instances/{instanceId}/credentials` | ✅ Implemented | GetMySQLDatabaseCredentials |  |
| POST | `databases/mysql/instances/{instanceId}/credentials/reset` | ✅ Implemented | ResetMySQLDatabaseCredentials |  |
| GET | `databases/postgresql/instances/{instanceId}/credentials` | ✅ Implemented | GetPostgresDatabaseCredentials |  |
| POST | `databases/postgresql/instances/{instanceId}/credentials/reset` | ✅ Implemented | ResetPostgresDatabaseCredentials |  |

### Databases

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `databases/instances` | ✅ Implemented | ListDatabases |  |
| GET | `databases/mysql/instances` | ✅ Implemented | ListMySQLDatabases |  |
| POST | `databases/mysql/instances` | ✅ Implemented | CreateMySQLDatabase |  |
| DELETE | `databases/mysql/instances/{instanceId}` | ✅ Implemented | DeleteMySQLDatabase |  |
| GET | `databases/mysql/instances/{instanceId}` | ✅ Implemented | GetMySQLDatabase |  |
| PUT | `databases/mysql/instances/{instanceId}` | ✅ Implemented | UpdateMySQLDatabase |  |
| POST | `databases/mysql/instances/{instanceId}/patch` | ✅ Implemented | PatchMySQLDatabase |  |
| POST | `databases/mysql/instances/{instanceId}/resume` | ✅ Implemented | ResumeMySQLDatabase |  |
| POST | `databases/mysql/instances/{instanceId}/suspend` | ✅ Implemented | SuspendMySQLDatabase |  |
| GET | `databases/postgresql/instances` | ✅ Implemented | ListPostgresDatabases |  |
| POST | `databases/postgresql/instances` | ✅ Implemented | CreatePostgresDatabase |  |
| DELETE | `databases/postgresql/instances/{instanceId}` | ✅ Implemented | DeletePostgresDatabase |  |
| GET | `databases/postgresql/instances/{instanceId}` | ✅ Implemented | GetPostgresDatabase |  |
| PUT | `databases/postgresql/instances/{instanceId}` | ✅ Implemented | UpdatePostgresDatabase |  |
| POST | `databases/postgresql/instances/{instanceId}/patch` | ✅ Implemented | PatchPostgresDatabase |  |
| POST | `databases/postgresql/instances/{instanceId}/resume` | ✅ Implemented | ResumePostgresDatabase |  |
| POST | `databases/postgresql/instances/{instanceId}/suspend` | ✅ Implemented | SuspendPostgresDatabase |  |

### Devices

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `networking/firewalls/{firewallId}/devices` | ✅ Implemented | ListFirewallDevices |  |
| POST | `networking/firewalls/{firewallId}/devices` | ✅ Implemented | CreateFirewallDevice |  |
| DELETE | `networking/firewalls/{firewallId}/devices/{deviceId}` | ✅ Implemented | DeleteFirewallDevice |  |
| GET | `networking/firewalls/{firewallId}/devices/{deviceId}` | ✅ Implemented | GetFirewallDevice |  |

### Disks

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `linode/instances/{linodeId}/disks` | ✅ Implemented | ListInstanceDisks |  |
| POST | `linode/instances/{linodeId}/disks` | ✅ Implemented | CreateInstanceDisk |  |
| DELETE | `linode/instances/{linodeId}/disks/{diskId}` | ✅ Implemented | DeleteInstanceDisk |  |
| GET | `linode/instances/{linodeId}/disks/{diskId}` | ✅ Implemented | GetInstanceDisk |  |
| PUT | `linode/instances/{linodeId}/disks/{diskId}` | ✅ Implemented | UpdateInstanceDisk |  |
| POST | `linode/instances/{linodeId}/disks/{diskId}/clone` | ✅ Implemented | CloneInstanceDisk |  |
| POST | `linode/instances/{linodeId}/disks/{diskId}/password` | ✅ Implemented | PasswordResetInstanceDisk |  |
| POST | `linode/instances/{linodeId}/disks/{diskId}/resize` | ✅ Implemented | ResizeInstanceDisk |  |

### Domain zone file

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `domains/{domainId}/zone-file` | ✅ Implemented | GetDomainZoneFile |  |

### Domains

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `domains` | ✅ Implemented | ListDomains |  |
| POST | `domains` | ✅ Implemented | CreateDomain |  |
| POST | `domains/import` | ✅ Implemented | ImportDomain |  |
| DELETE | `domains/{domainId}` | ✅ Implemented | DeleteDomain |  |
| GET | `domains/{domainId}` | ✅ Implemented | GetDomain |  |
| PUT | `domains/{domainId}` | ✅ Implemented | UpdateDomain |  |
| POST | `domains/{domainId}/clone` | ✅ Implemented | CloneDomain |  |

### Endpoints

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `object-storage/endpoints` | ✅ Implemented | ListObjectStorageEndpoints |  |

### Engines

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `databases/engines` | ✅ Implemented | ListDatabaseEngines |  |
| GET | `databases/engines/{engineId}` | ✅ Implemented | GetDatabaseEngine |  |

### Entity transfers

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `account/entity-transfers` | ❌ Missing |  | List entity transfers |
| POST | `account/entity-transfers` | ❌ Missing |  | Create an entity transfer |
| DELETE | `account/entity-transfers/{token}` | ❌ Missing |  | Cancel an entity transfer |
| GET | `account/entity-transfers/{token}` | ❌ Missing |  | Get an entity transfer |
| POST | `account/entity-transfers/{token}/accept` | ❌ Missing |  | Accept an entity transfer |

### Events

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `account/events` | ✅ Implemented | ListEvents |  |
| GET | `account/events/{eventId}` | ✅ Implemented | GetEvent |  |
| POST | `account/events/{eventId}/seen` | ✅ Implemented | MarkEventsSeen |  |

### Firewall settings

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `networking/firewalls/settings` | ✅ Implemented | GetFirewallSettings |  |
| PUT | `networking/firewalls/settings` | ✅ Implemented | UpdateFirewallSettings |  |

### Firewalls

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `linode/instances/{linodeId}/firewalls` | ✅ Implemented | ListInstanceFirewalls |  |
| PUT | `linode/instances/{linodeId}/firewalls` | ❌ Missing |  | Update a Linode's firewalls |
| POST | `linode/instances/{linodeId}/firewalls/apply` | ❌ Missing |  | Apply a Linode's firewalls |
| GET | `networking/firewalls` | ✅ Implemented | ListFirewalls |  |
| POST | `networking/firewalls` | ✅ Implemented | CreateFirewall |  |
| DELETE | `networking/firewalls/{firewallId}` | ✅ Implemented | DeleteFirewall |  |
| GET | `networking/firewalls/{firewallId}` | ✅ Implemented | GetFirewall |  |
| PUT | `networking/firewalls/{firewallId}` | ✅ Implemented | UpdateFirewall |  |
| GET | `networking/firewalls/{firewallId}/history` | ❌ Missing |  | List firewall rule versions |
| GET | `networking/firewalls/{firewallId}/history/rules/{version}` | ❌ Missing |  | Get a firewall rule version |
| GET | `networking/firewalls/{firewallId}/rules` | ✅ Implemented | GetFirewallRules |  |
| PUT | `networking/firewalls/{firewallId}/rules` | ✅ Implemented | UpdateFirewallRules |  |
| GET | `nodebalancers/{nodeBalancerId}/firewalls` | ✅ Implemented | ListNodeBalancerFirewalls |  |
| PUT | `nodebalancers/{nodeBalancerId}/firewalls` | ❌ Missing |  | Update a NodeBalancer's firewalls |

### Grants

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `profile/grants` | ✅ Implemented | GrantsList |  |

### IP addresses

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `linode/instances/{linodeId}/ips` | ✅ Implemented | GetInstanceIPAddresses |  |
| POST | `linode/instances/{linodeId}/ips` | ✅ Implemented | AddInstanceIPAddress, AssignInstanceReservedIP |  |
| DELETE | `linode/instances/{linodeId}/ips/{address}` | ✅ Implemented | DeleteInstanceIPAddress |  |
| GET | `linode/instances/{linodeId}/ips/{address}` | ✅ Implemented | GetInstanceIPAddress |  |
| PUT | `linode/instances/{linodeId}/ips/{address}` | ✅ Implemented | UpdateInstanceIPAddress |  |
| GET | `networking/ips` | ✅ Implemented | ListIPAddresses |  |
| POST | `networking/ips` | ✅ Implemented | AllocateReserveIP |  |
| POST | `networking/ips/assign` | ✅ Implemented | InstancesAssignIPs |  |
| POST | `networking/ips/share` | ✅ Implemented | ShareIPAddresses |  |
| GET | `networking/ips/{address}` | ✅ Implemented | GetIPAddress |  |
| PUT | `networking/ips/{address}` | ✅ Implemented | UpdateIPAddressV2, UpdateIPAddress |  |
| GET | `vpcs/ips` | ✅ Implemented | ListAllVPCIPAddresses |  |
| GET | `vpcs/{vpcId}/ips` | ✅ Implemented | ListVPCIPAddresses |  |

### IPv4 addresses

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| POST | `networking/ipv4/assign` | ❌ Missing |  | Assign IPv4s to Linodes |
| POST | `networking/ipv4/share` | ❌ Missing |  | Configure IPv4 sharing |

### IPv6 pools

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `networking/ipv6/pools` | ✅ Implemented | ListIPv6Pools |  |

### IPv6 ranges

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `networking/ipv6/ranges` | ✅ Implemented | ListIPv6Ranges |  |
| POST | `networking/ipv6/ranges` | ✅ Implemented | CreateIPv6Range |  |
| DELETE | `networking/ipv6/ranges/{range}` | ✅ Implemented | DeleteIPv6Range |  |
| GET | `networking/ipv6/ranges/{range}` | ✅ Implemented | GetIPv6Range |  |

### Identity Management

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `entities` | ✅ Implemented | ListEntities |  |
| GET | `iam/role-permissions` | ✅ Implemented | GetAccountRolePermissions |  |
| GET | `iam/users/{username}/role-permissions` | ✅ Implemented | GetUserRolePermissions |  |
| PUT | `iam/users/{username}/role-permissions` | ✅ Implemented | UpdateUserRolePermissions |  |

### Image sharing

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `images/sharegroups` | ✅ Implemented | ListImageShareGroups |  |
| POST | `images/sharegroups` | ✅ Implemented | CreateImageShareGroup |  |
| GET | `images/sharegroups/tokens` | ✅ Implemented | ImageShareGroupListTokens |  |
| POST | `images/sharegroups/tokens` | ✅ Implemented | ImageShareGroupCreateToken |  |
| DELETE | `images/sharegroups/tokens/{tokenUuid}` | ✅ Implemented | ImageShareGroupRemoveToken |  |
| GET | `images/sharegroups/tokens/{tokenUuid}` | ✅ Implemented | ImageShareGroupGetToken |  |
| PUT | `images/sharegroups/tokens/{tokenUuid}` | ✅ Implemented | ImageShareGroupUpdateToken |  |
| GET | `images/sharegroups/tokens/{tokenUuid}/sharegroup` | ✅ Implemented | ImageShareGroupGetByToken |  |
| GET | `images/sharegroups/tokens/{tokenUuid}/sharegroup/images` | ✅ Implemented | ImageShareGroupGetImageShareEntriesByToken |  |
| DELETE | `images/sharegroups/{sharegroupId}` | ✅ Implemented | DeleteImageShareGroup |  |
| GET | `images/sharegroups/{sharegroupId}` | ✅ Implemented | GetImageShareGroup |  |
| PUT | `images/sharegroups/{sharegroupId}` | ✅ Implemented | UpdateImageShareGroup |  |
| GET | `images/sharegroups/{sharegroupId}/images` | ✅ Implemented | ImageShareGroupListImageShareEntries |  |
| POST | `images/sharegroups/{sharegroupId}/images` | ❌ Missing |  | Add images to a share group |
| DELETE | `images/sharegroups/{sharegroupId}/images/{imageId}` | ✅ Implemented | ImageShareGroupRemoveImage |  |
| PUT | `images/sharegroups/{sharegroupId}/images/{imageId}` | ✅ Implemented | ImageShareGroupUpdateImageShareEntry |  |
| GET | `images/sharegroups/{sharegroupId}/members` | ✅ Implemented | ImageShareGroupListMembers |  |
| POST | `images/sharegroups/{sharegroupId}/members` | ✅ Implemented | ImageShareGroupAddMember |  |
| DELETE | `images/sharegroups/{sharegroupId}/members/{tokenUuid}` | ✅ Implemented | ImageShareGroupRemoveMember |  |
| GET | `images/sharegroups/{sharegroupId}/members/{tokenUuid}` | ✅ Implemented | ImageShareGroupGetMember |  |
| PUT | `images/sharegroups/{sharegroupId}/members/{tokenUuid}` | ✅ Implemented | ImageShareGroupUpdateMember |  |
| GET | `images/{imageId}/sharegroups` | ✅ Implemented | ListImageShareGroupsContainingPrivateImage |  |

### Images

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `images` | ✅ Implemented | ListImages |  |
| POST | `images` | ✅ Implemented | CreateImage |  |
| POST | `images/upload` | ✅ Implemented | CreateImageUpload |  |
| DELETE | `images/{imageId}` | ✅ Implemented | DeleteImage |  |
| GET | `images/{imageId}` | ✅ Implemented | GetImage |  |
| PUT | `images/{imageId}` | ✅ Implemented | UpdateImage |  |
| POST | `images/{imageId}/regions` | ✅ Implemented | ReplicateImage |  |

### Invoices

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `account/invoices` | ✅ Implemented | ListInvoices |  |
| GET | `account/invoices/{invoiceId}` | ✅ Implemented | GetInvoice |  |
| GET | `account/invoices/{invoiceId}/items` | ✅ Implemented | ListInvoiceItems |  |

### Kernels

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `linode/kernels` | ✅ Implemented | ListKernels |  |
| GET | `linode/kernels/{kernelId}` | ✅ Implemented | GetKernel |  |

### Kubeconfigs

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| DELETE | `lke/clusters/{clusterId}/kubeconfig` | ✅ Implemented | DeleteLKEClusterKubeconfig |  |
| GET | `lke/clusters/{clusterId}/kubeconfig` | ✅ Implemented | GetLKEClusterKubeconfig |  |

### LKE API endpoints

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `lke/clusters/{clusterId}/api-endpoints` | ✅ Implemented | ListLKEClusterAPIEndpoints |  |

### LKE service tokens

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| DELETE | `lke/clusters/{clusterId}/servicetoken` | ✅ Implemented | DeleteLKEClusterServiceToken |  |

### LKE types

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `lke/types` | ✅ Implemented | ListLKETypes |  |

### LKE versions

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `lke/tiers/{tier}/versions` | ✅ Implemented | ListLKETierVersions |  |
| GET | `lke/tiers/{tier}/versions/{version}` | ✅ Implemented | GetLKETierVersion |  |
| GET | `lke/versions` | ✅ Implemented | ListLKEVersions |  |
| GET | `lke/versions/{version}` | ✅ Implemented | GetLKEVersion |  |

### Linode instances

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `linode/instances` | ✅ Implemented | ListInstances |  |
| POST | `linode/instances` | ✅ Implemented | CreateInstance |  |
| DELETE | `linode/instances/{linodeId}` | ✅ Implemented | DeleteInstance |  |
| GET | `linode/instances/{linodeId}` | ✅ Implemented | GetInstance |  |
| PUT | `linode/instances/{linodeId}` | ✅ Implemented | UpdateInstance |  |
| POST | `linode/instances/{linodeId}/boot` | ✅ Implemented | BootInstance |  |
| POST | `linode/instances/{linodeId}/clone` | ✅ Implemented | CloneInstance |  |
| POST | `linode/instances/{linodeId}/migrate` | ✅ Implemented | MigrateInstance |  |
| POST | `linode/instances/{linodeId}/mutate` | ✅ Implemented | MutateInstance, UpgradeInstance |  |
| POST | `linode/instances/{linodeId}/password` | ✅ Implemented | ResetInstancePassword |  |
| POST | `linode/instances/{linodeId}/reboot` | ✅ Implemented | RebootInstance |  |
| POST | `linode/instances/{linodeId}/rebuild` | ✅ Implemented | RebuildInstance |  |
| POST | `linode/instances/{linodeId}/rescue` | ✅ Implemented | RescueInstance |  |
| POST | `linode/instances/{linodeId}/resize` | ✅ Implemented | ResizeInstance |  |
| POST | `linode/instances/{linodeId}/shutdown` | ✅ Implemented | ShutdownInstance |  |

### Linode interfaces

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `linode/instances/{linodeId}/interfaces` | ✅ Implemented | ListInterfaces |  |
| POST | `linode/instances/{linodeId}/interfaces` | ✅ Implemented | CreateInterface |  |
| GET | `linode/instances/{linodeId}/interfaces/history` | ❌ Missing |  | List a Linode's network interface history |
| GET | `linode/instances/{linodeId}/interfaces/settings` | ✅ Implemented | GetInterfaceSettings |  |
| PUT | `linode/instances/{linodeId}/interfaces/settings` | ✅ Implemented | UpdateInterfaceSettings |  |
| DELETE | `linode/instances/{linodeId}/interfaces/{interfaceId}` | ✅ Implemented | DeleteInterface |  |
| GET | `linode/instances/{linodeId}/interfaces/{interfaceId}` | ✅ Implemented | GetInterface |  |
| PUT | `linode/instances/{linodeId}/interfaces/{interfaceId}` | ✅ Implemented | UpdateInterface |  |
| GET | `linode/instances/{linodeId}/interfaces/{interfaceId}/firewalls` | ✅ Implemented | ListInterfaceFirewalls |  |
| POST | `linode/instances/{linodeId}/upgrade-interfaces` | ✅ Implemented | UpgradeInterfaces |  |

### Linode types

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `linode/types` | ✅ Implemented | ListTypes |  |
| GET | `linode/types/{typeId}` | ✅ Implemented | GetType |  |

### Logins

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `account/logins` | ✅ Implemented | ListLogins |  |
| GET | `account/logins/{loginId}` | ✅ Implemented | GetLogin |  |
| GET | `profile/logins` | ✅ Implemented | ListProfileLogins |  |
| GET | `profile/logins/{loginId}` | ✅ Implemented | GetProfileLogin |  |

### Logs

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `monitor/streams` | ❌ Missing |  | List streams |
| POST | `monitor/streams` | ❌ Missing |  | Create a stream |
| GET | `monitor/streams/destinations` | ❌ Missing |  | List destinations |
| POST | `monitor/streams/destinations` | ❌ Missing |  | Create a destination |
| DELETE | `monitor/streams/destinations/{destinationId}` | ❌ Missing |  | Delete a destination |
| GET | `monitor/streams/destinations/{destinationId}` | ❌ Missing |  | Get a destination |
| PUT | `monitor/streams/destinations/{destinationId}` | ❌ Missing |  | Update a destination |
| GET | `monitor/streams/destinations/{destinationId}/history` | ❌ Missing |  | Get a destination's history |
| DELETE | `monitor/streams/{streamId}` | ❌ Missing |  | Delete a stream |
| GET | `monitor/streams/{streamId}` | ❌ Missing |  | Get a stream |
| PUT | `monitor/streams/{streamId}` | ❌ Missing |  | Update a stream |
| GET | `monitor/streams/{streamId}/history` | ❌ Missing |  | Get a stream's history |

### Longview clients

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `longview/clients` | ✅ Implemented | ListLongviewClients |  |
| POST | `longview/clients` | ✅ Implemented | CreateLongviewClient |  |
| DELETE | `longview/clients/{clientId}` | ✅ Implemented | DeleteLongviewClient |  |
| GET | `longview/clients/{clientId}` | ✅ Implemented | GetLongviewClient |  |
| PUT | `longview/clients/{clientId}` | ✅ Implemented | UpdateLongviewClient |  |

### Longview plans

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `longview/plan` | ✅ Implemented | GetLongviewPlan |  |
| PUT | `longview/plan` | ✅ Implemented | UpdateLongviewPlan |  |

### Longview subscriptions

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `longview/subscriptions` | ✅ Implemented | ListLongviewSubscriptions |  |
| GET | `longview/subscriptions/{subscriptionId}` | ✅ Implemented | GetLongviewSubscription |  |

### Longview types

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `longview/types` | ❌ Missing |  | List Longview types |

### Maintenance policies

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `maintenance/policies` | ✅ Implemented | ListMaintenancePolicies |  |

### Maintenances

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `account/maintenance` | ✅ Implemented | ListMaintenances |  |

### Managed Linode settings

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `managed/linode-settings` | ❌ Missing |  | List managed Linode settings |
| GET | `managed/linode-settings/{linodeId}` | ❌ Missing |  | Get a Linode's managed settings |
| PUT | `managed/linode-settings/{linodeId}` | ❌ Missing |  | Update a Linode's managed settings |

### Managed SSH keys

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `managed/credentials/sshkey` | ❌ Missing |  | Get a managed SSH key |

### Managed contacts

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `managed/contacts` | ❌ Missing |  | List managed contacts |
| POST | `managed/contacts` | ❌ Missing |  | Create a managed contact |
| DELETE | `managed/contacts/{contactId}` | ❌ Missing |  | Delete a managed contact |
| GET | `managed/contacts/{contactId}` | ❌ Missing |  | Get a managed contact |
| PUT | `managed/contacts/{contactId}` | ❌ Missing |  | Update a managed contact |

### Managed credentials

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `managed/credentials` | ❌ Missing |  | List managed credentials |
| POST | `managed/credentials` | ❌ Missing |  | Create a managed credential |
| GET | `managed/credentials/{credentialId}` | ❌ Missing |  | Get a managed credential |
| PUT | `managed/credentials/{credentialId}` | ❌ Missing |  | Update a managed credential |
| POST | `managed/credentials/{credentialId}/revoke` | ❌ Missing |  | Delete a managed credential |
| POST | `managed/credentials/{credentialId}/update` | ❌ Missing |  | Update a managed credential's username and password |

### Managed issues

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `managed/issues` | ❌ Missing |  | List managed issues |
| GET | `managed/issues/{issueId}` | ❌ Missing |  | Get a managed issue |

### Managed service monitors

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `managed/services` | ❌ Missing |  | List managed services |
| POST | `managed/services` | ❌ Missing |  | Create a managed service |
| DELETE | `managed/services/{serviceId}` | ❌ Missing |  | Delete a managed service monitor |
| GET | `managed/services/{serviceId}` | ❌ Missing |  | Get a managed service monitor |
| PUT | `managed/services/{serviceId}` | ❌ Missing |  | Update a managed service monitor |
| POST | `managed/services/{serviceId}/disable` | ❌ Missing |  | Disable a managed service monitor |
| POST | `managed/services/{serviceId}/enable` | ❌ Missing |  | Enable a managed service monitor |

### Managed statistics

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `managed/stats` | ❌ Missing |  | List managed stats |

### Metrics

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `monitor/dashboards` | ✅ Implemented | ListMonitorDashboards |  |
| GET | `monitor/dashboards/{dashboardId}` | ✅ Implemented | GetMonitorDashboard |  |
| GET | `monitor/services` | ✅ Implemented | ListMonitorServices |  |
| GET | `monitor/services/{serviceType}` | ✅ Implemented | GetMonitorServiceByType |  |
| GET | `monitor/services/{serviceType}/dashboards` | ✅ Implemented | ListMonitorDashboardsByServiceType |  |
| GET | `monitor/services/{serviceType}/metric-definitions` | ✅ Implemented | ListMonitorMetricsDefinitionByServiceType |  |
| POST | `monitor/services/{serviceType}/metrics` | ❌ Missing |  | Get an entity's metrics |
| POST | `monitor/services/{serviceType}/token` | ✅ Implemented | CreateMonitorServiceTokenForServiceType |  |

### Network transfer prices

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `network-transfer/prices` | ✅ Implemented | ListNetworkTransferPrices |  |

### Node pools

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `lke/clusters/{clusterId}/pools` | ✅ Implemented | ListLKENodePools |  |
| POST | `lke/clusters/{clusterId}/pools` | ✅ Implemented | CreateLKENodePool |  |
| DELETE | `lke/clusters/{clusterId}/pools/{poolId}` | ✅ Implemented | DeleteLKENodePool |  |
| GET | `lke/clusters/{clusterId}/pools/{poolId}` | ✅ Implemented | GetLKENodePool |  |
| PUT | `lke/clusters/{clusterId}/pools/{poolId}` | ✅ Implemented | UpdateLKENodePool |  |
| POST | `lke/clusters/{clusterId}/pools/{poolId}/recycle` | ✅ Implemented | RecycleLKENodePool |  |

### NodeBalancer types

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `nodebalancers/types` | ✅ Implemented | ListNodeBalancerTypes |  |

### NodeBalancers

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `linode/instances/{linodeId}/nodebalancers` | ✅ Implemented | ListInstanceNodeBalancers |  |
| GET | `nodebalancers` | ✅ Implemented | ListNodeBalancers |  |
| POST | `nodebalancers` | ✅ Implemented | CreateNodeBalancer |  |
| DELETE | `nodebalancers/{nodeBalancerId}` | ✅ Implemented | DeleteNodeBalancer |  |
| GET | `nodebalancers/{nodeBalancerId}` | ✅ Implemented | GetNodeBalancer |  |
| PUT | `nodebalancers/{nodeBalancerId}` | ✅ Implemented | UpdateNodeBalancer |  |

### Nodes

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| DELETE | `lke/clusters/{clusterId}/nodes/{nodeId}` | ✅ Implemented | DeleteLKENodePoolNode |  |
| GET | `lke/clusters/{clusterId}/nodes/{nodeId}` | ✅ Implemented | GetLKENodePoolNode |  |
| POST | `lke/clusters/{clusterId}/nodes/{nodeId}/recycle` | ✅ Implemented | RecycleLKENodePoolNode |  |
| GET | `nodebalancers/{nodeBalancerId}/configs/{configId}/nodes` | ✅ Implemented | ListNodeBalancerNodes |  |
| POST | `nodebalancers/{nodeBalancerId}/configs/{configId}/nodes` | ✅ Implemented | CreateNodeBalancerNode |  |
| DELETE | `nodebalancers/{nodeBalancerId}/configs/{configId}/nodes/{nodeId}` | ✅ Implemented | DeleteNodeBalancerNode |  |
| GET | `nodebalancers/{nodeBalancerId}/configs/{configId}/nodes/{nodeId}` | ✅ Implemented | GetNodeBalancerNode |  |
| PUT | `nodebalancers/{nodeBalancerId}/configs/{configId}/nodes/{nodeId}` | ✅ Implemented | UpdateNodeBalancerNode |  |

### Notifications

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `account/notifications` | ✅ Implemented | ListNotifications |  |

### OAuth apps

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `profile/apps` | ✅ Implemented | ListProfileApps |  |
| DELETE | `profile/apps/{appId}` | ✅ Implemented | DeleteProfileApp |  |
| GET | `profile/apps/{appId}` | ✅ Implemented | GetProfileApp |  |

### OAuth client

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `account/oauth-clients/{clientId}/thumbnail` | ❌ Missing |  | Get the OAuth client's thumbnail |
| PUT | `account/oauth-clients/{clientId}/thumbnail` | ❌ Missing |  | Update the OAuth client's thumbnail |

### OAuth clients

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `account/oauth-clients` | ✅ Implemented | ListOAuthClients |  |
| POST | `account/oauth-clients` | ✅ Implemented | CreateOAuthClient |  |
| DELETE | `account/oauth-clients/{clientId}` | ✅ Implemented | DeleteOAuthClient |  |
| GET | `account/oauth-clients/{clientId}` | ✅ Implemented | GetOAuthClient |  |
| PUT | `account/oauth-clients/{clientId}` | ✅ Implemented | UpdateOAuthClient |  |
| POST | `account/oauth-clients/{clientId}/reset-secret` | ✅ Implemented | ResetOAuthClientSecret |  |

### OAuth preferences

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `profile/preferences` | ✅ Implemented | GetProfilePreferences |  |
| PUT | `profile/preferences` | ✅ Implemented | UpdateProfilePreferences |  |

### Object Storage

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| POST | `object-storage/cancel` | ✅ Implemented | CancelObjectStorage |  |
| GET | `object-storage/quotas` | ✅ Implemented | ListObjectStorageQuotas |  |
| GET | `object-storage/quotas/{objQuotaId}` | ✅ Implemented | GetObjectStorageQuota |  |
| GET | `object-storage/quotas/{objQuotaId}/usage` | ✅ Implemented | GetObjectStorageQuotaUsage |  |
| GET | `object-storage/transfer` | ✅ Implemented | GetObjectStorageTransfer |  |
| GET | `object-storage/types` | ❌ Missing |  | List Object Storage types |

### Payment methods

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `account/payment-methods` | ✅ Implemented | ListPaymentMethods |  |
| POST | `account/payment-methods` | ✅ Implemented | AddPaymentMethod |  |
| DELETE | `account/payment-methods/{paymentMethodId}` | ✅ Implemented | DeletePaymentMethod |  |
| GET | `account/payment-methods/{paymentMethodId}` | ✅ Implemented | GetPaymentMethod |  |
| POST | `account/payment-methods/{paymentMethodId}/make-default` | ❌ Missing |  | Set a default payment method |

### Payments

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| POST | `account/credit-card` | ❌ Missing |  | Add or edit a credit card |
| GET | `account/payments` | ✅ Implemented | ListPayments |  |
| POST | `account/payments` | ✅ Implemented | CreatePayment |  |
| POST | `account/payments/paypal` | ❌ Missing |  | Stage a PayPal payment |
| POST | `account/payments/paypal/execute` | ❌ Missing |  | Execute a PayPal payment |
| GET | `account/payments/{paymentId}` | ✅ Implemented | GetPayment |  |

### Personal access tokens

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `profile/tokens` | ✅ Implemented | ListTokens |  |
| POST | `profile/tokens` | ✅ Implemented | CreateToken |  |
| DELETE | `profile/tokens/{tokenId}` | ✅ Implemented | DeleteToken |  |
| GET | `profile/tokens/{tokenId}` | ✅ Implemented | GetToken |  |
| PUT | `profile/tokens/{tokenId}` | ✅ Implemented | UpdateToken |  |

### Phone number

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| DELETE | `profile/phone-number` | ✅ Implemented | DeletePhoneNumber |  |
| POST | `profile/phone-number` | ✅ Implemented | SendPhoneNumberVerificationCode |  |
| POST | `profile/phone-number/verify` | ✅ Implemented | VerifyPhoneNumber |  |

### Placement groups

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `placement/groups` | ✅ Implemented | ListPlacementGroups |  |
| POST | `placement/groups` | ✅ Implemented | CreatePlacementGroup |  |
| DELETE | `placement/groups/{groupId}` | ✅ Implemented | DeletePlacementGroup |  |
| GET | `placement/groups/{groupId}` | ✅ Implemented | GetPlacementGroup |  |
| PUT | `placement/groups/{groupId}` | ✅ Implemented | UpdatePlacementGroup |  |
| POST | `placement/groups/{groupId}/assign` | ✅ Implemented | AssignPlacementGroupLinodes |  |
| POST | `placement/groups/{groupId}/unassign` | ✅ Implemented | UnassignPlacementGroupLinodes |  |

### Profile

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `profile` | ✅ Implemented | GetProfile |  |
| PUT | `profile` | ✅ Implemented | UpdateProfile |  |

### Promo credits

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| POST | `account/promo-codes` | ✅ Implemented | AddPromoCode |  |

### Records

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `domains/{domainId}/records` | ✅ Implemented | ListDomainRecords |  |
| POST | `domains/{domainId}/records` | ✅ Implemented | CreateDomainRecord |  |
| DELETE | `domains/{domainId}/records/{recordId}` | ✅ Implemented | DeleteDomainRecord |  |
| GET | `domains/{domainId}/records/{recordId}` | ✅ Implemented | GetDomainRecord |  |
| PUT | `domains/{domainId}/records/{recordId}` | ✅ Implemented | UpdateDomainRecord |  |

### Regions

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `regions` | ✅ Implemented | ListRegions |  |
| GET | `regions/availability` | ✅ Implemented | ListRegionsAvailability |  |
| GET | `regions/{regionId}` | ✅ Implemented | GetRegion |  |
| GET | `regions/{regionId}/availability` | ✅ Implemented | GetRegionAvailability |  |

### Replies

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `support/tickets/{ticketId}/replies` | ❌ Missing |  | List replies |
| POST | `support/tickets/{ticketId}/replies` | ❌ Missing |  | Create a reply |

### SSH keys

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `profile/sshkeys` | ✅ Implemented | ListSSHKeys |  |
| POST | `profile/sshkeys` | ✅ Implemented | CreateSSHKey |  |
| DELETE | `profile/sshkeys/{sshKeyId}` | ✅ Implemented | DeleteSSHKey |  |
| GET | `profile/sshkeys/{sshKeyId}` | ✅ Implemented | GetSSHKey |  |
| PUT | `profile/sshkeys/{sshKeyId}` | ✅ Implemented | UpdateSSHKey |  |

### SSL certificates

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `databases/mysql/instances/{instanceId}/ssl` | ✅ Implemented | GetMySQLDatabaseSSL |  |
| GET | `databases/postgresql/instances/{instanceId}/ssl` | ✅ Implemented | GetPostgresDatabaseSSL |  |

### Security questions

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `profile/security-questions` | ✅ Implemented | SecurityQuestionsList |  |
| POST | `profile/security-questions` | ✅ Implemented | SecurityQuestionsAnswer |  |

### Service transfers

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `account/service-transfers` | ✅ Implemented | ListAccountServiceTransfer |  |
| POST | `account/service-transfers` | ✅ Implemented | RequestAccountServiceTransfer |  |
| DELETE | `account/service-transfers/{token}` | ✅ Implemented | CancelAccountServiceTransfer |  |
| GET | `account/service-transfers/{token}` | ✅ Implemented | GetAccountServiceTransfer |  |
| POST | `account/service-transfers/{token}/accept` | ✅ Implemented | AcceptAccountServiceTransfer |  |

### StackScripts

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `linode/stackscripts` | ✅ Implemented | ListStackscripts |  |
| POST | `linode/stackscripts` | ✅ Implemented | CreateStackscript |  |
| DELETE | `linode/stackscripts/{stackscriptId}` | ✅ Implemented | DeleteStackscript |  |
| GET | `linode/stackscripts/{stackscriptId}` | ✅ Implemented | GetStackscript |  |
| PUT | `linode/stackscripts/{stackscriptId}` | ✅ Implemented | UpdateStackscript |  |

### Statistics

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `linode/instances/{linodeId}/stats` | ✅ Implemented | GetInstanceStats |  |
| GET | `linode/instances/{linodeId}/stats/{year}/{month}` | ✅ Implemented | GetInstanceStatsByDate |  |
| GET | `linode/instances/{linodeId}/transfer` | ✅ Implemented | GetInstanceTransfer |  |
| GET | `linode/instances/{linodeId}/transfer/{year}/{month}` | ✅ Implemented | GetInstanceTransferMonthly, GetInstanceTransferMonthlyV2 |  |
| GET | `nodebalancers/{nodeBalancerId}/stats` | ✅ Implemented | GetNodeBalancerStats |  |

### Support tickets

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `support/tickets` | ✅ Implemented | ListTickets |  |
| POST | `support/tickets` | ❌ Missing |  | Open a support ticket |
| GET | `support/tickets/{ticketId}` | ✅ Implemented | GetTicket |  |
| POST | `support/tickets/{ticketId}/close` | ❌ Missing |  | Close a support ticket |

### TLS/SSL certificates

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| DELETE | `object-storage/buckets/{regionId}/{bucket}/ssl` | ✅ Implemented | DeleteObjectStorageBucketCert |  |
| GET | `object-storage/buckets/{regionId}/{bucket}/ssl` | ✅ Implemented | GetObjectStorageBucketCert, GetObjectStorageBucketCertV2 |  |
| POST | `object-storage/buckets/{regionId}/{bucket}/ssl` | ✅ Implemented | UploadObjectStorageBucketCert, UploadObjectStorageBucketCertV2 |  |

### Tags

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `tags` | ✅ Implemented | ListTags |  |
| POST | `tags` | ✅ Implemented | CreateTag |  |
| DELETE | `tags/{tagLabel}` | ✅ Implemented | DeleteTag |  |
| GET | `tags/{tagLabel}` | ✅ Implemented | ListTaggedObjects |  |

### Templates

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `networking/firewalls/templates` | ✅ Implemented | ListFirewallTemplates |  |
| GET | `networking/firewalls/templates/{slug}` | ✅ Implemented | GetFirewallTemplate |  |

### Trusted devices

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `profile/devices` | ✅ Implemented | ListProfileDevices |  |
| DELETE | `profile/devices/{deviceId}` | ✅ Implemented | DeleteProfileDevice |  |
| GET | `profile/devices/{deviceId}` | ✅ Implemented | GetProfileDevice |  |

### Two-factor authentication

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| POST | `profile/tfa-disable` | ✅ Implemented | DisableTwoFactor |  |
| POST | `profile/tfa-enable` | ✅ Implemented | CreateTwoFactorSecret |  |
| POST | `profile/tfa-enable-confirm` | ✅ Implemented | ConfirmTwoFactor |  |

### Types

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `databases/types` | ✅ Implemented | ListDatabaseTypes |  |
| GET | `databases/types/{typeId}` | ✅ Implemented | GetDatabaseType |  |

### Users

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `account/users` | ✅ Implemented | ListUsers |  |
| POST | `account/users` | ✅ Implemented | CreateUser |  |
| DELETE | `account/users/{username}` | ✅ Implemented | DeleteUser |  |
| GET | `account/users/{username}` | ✅ Implemented | GetUser |  |
| PUT | `account/users/{username}` | ✅ Implemented | UpdateUser |  |
| GET | `account/users/{username}/grants` | ✅ Implemented | GetUserGrants |  |
| PUT | `account/users/{username}/grants` | ✅ Implemented | UpdateUserGrants |  |

### VLANs

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `networking/vlans` | ✅ Implemented | ListVLANs |  |
| DELETE | `networking/vlans/{regionId}/{label}` | ❌ Missing |  | Delete a VLAN |

### VPC subnets

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `vpcs/{vpcId}/subnets` | ✅ Implemented | ListVPCSubnets |  |
| POST | `vpcs/{vpcId}/subnets` | ✅ Implemented | CreateVPCSubnet |  |
| DELETE | `vpcs/{vpcId}/subnets/{vpcSubnetId}` | ✅ Implemented | DeleteVPCSubnet |  |
| GET | `vpcs/{vpcId}/subnets/{vpcSubnetId}` | ✅ Implemented | GetVPCSubnet |  |
| PUT | `vpcs/{vpcId}/subnets/{vpcSubnetId}` | ✅ Implemented | UpdateVPCSubnet |  |

### VPCs

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `nodebalancers/{nodeBalancerId}/vpcs` | ✅ Implemented | ListNodeBalancerVPCConfigs |  |
| GET | `nodebalancers/{nodeBalancerId}/vpcs/{nodeBalancerVpcConfigId}` | ✅ Implemented | GetNodeBalancerVPCConfig |  |
| GET | `vpcs` | ✅ Implemented | ListVPCs |  |
| POST | `vpcs` | ✅ Implemented | CreateVPC |  |
| DELETE | `vpcs/{vpcId}` | ✅ Implemented | DeleteVPC |  |
| GET | `vpcs/{vpcId}` | ✅ Implemented | GetVPC |  |
| PUT | `vpcs/{vpcId}` | ✅ Implemented | UpdateVPC |  |

### Volume types

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `volumes/types` | ✅ Implemented | ListVolumeTypes |  |

### Volumes

| Method | Endpoint | Status | SDK Method | Notes |
|--------|----------|--------|------------|-------|
| GET | `linode/instances/{linodeId}/volumes` | ✅ Implemented | ListInstanceVolumes |  |
| GET | `volumes` | ✅ Implemented | ListVolumes |  |
| POST | `volumes` | ✅ Implemented | CreateVolume |  |
| DELETE | `volumes/{volumeId}` | ✅ Implemented | DeleteVolume |  |
| GET | `volumes/{volumeId}` | ✅ Implemented | GetVolume |  |
| PUT | `volumes/{volumeId}` | ✅ Implemented | UpdateVolume |  |
| POST | `volumes/{volumeId}/attach` | ✅ Implemented | AttachVolume |  |
| POST | `volumes/{volumeId}/clone` | ✅ Implemented | CloneVolume |  |
| POST | `volumes/{volumeId}/detach` | ✅ Implemented | DetachVolume |  |
| POST | `volumes/{volumeId}/resize` | ✅ Implemented | ResizeVolume |  |

## Parameter Coverage for Implemented Endpoints

For endpoints that are implemented, this section identifies fields in the OpenAPI spec
that are absent from the corresponding SDK Options struct (request body) or response struct.

> **Note:** Only top-level fields are compared. Nested object/array fields are omitted for brevity.
> Fields labelled *extra* exist in the SDK but not in the current OpenAPI spec (may be deprecated or from a newer spec).

### Access keys

#### `PUT object-storage/keys/{keyId}` → `UpdateObjectStorageKey`

- **Options struct:** `ObjectStorageKeyUpdateOptions`
- **Response struct:** `ObjectStorageKey`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `bucket_access`

### Account agreements

#### `GET account/agreements` → `GetAccountAgreements`

- **Options struct:** `—`
- **Response struct:** `AccountAgreements`

**Missing response fields** (documented but not in SDK response struct):

- `billing_agreement`

#### `POST account/agreements` → `AcknowledgeAccountAgreements`

- **Options struct:** `AccountAgreementsUpdateOptions`
- **Response struct:** `—`

**Missing request body fields** (documented but not in SDK Options struct):

- `billing_agreement`

### Account availability

#### `GET account/availability` → `ListAccountAvailabilities`

- **Options struct:** `—`
- **Response struct:** `AccountAvailability`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `available`
- `region`
- `unavailable`

### Alerts

#### `GET monitor/alert-channels` → `ListAlertChannels`

- **Options struct:** `—`
- **Response struct:** `AlertChannel`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `details`

#### `GET monitor/alert-definitions` → `ListAllMonitorAlertDefinitions`

- **Options struct:** `—`
- **Response struct:** `AlertDefinition`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

#### `GET monitor/services/{serviceType}/alert-definitions` → `ListMonitorAlertDefinitions`

- **Options struct:** `—`
- **Response struct:** `AlertDefinition`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

#### `POST monitor/services/{serviceType}/alert-definitions` → `CreateMonitorAlertDefinition`

- **Options struct:** `AlertDefinitionCreateOptions`
- **Response struct:** `AlertDefinition`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

#### `GET monitor/services/{serviceType}/alert-definitions/{alertId}` → `GetMonitorAlertDefinition`

- **Options struct:** `—`
- **Response struct:** `AlertDefinition`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

#### `PUT monitor/services/{serviceType}/alert-definitions/{alertId}` → `UpdateMonitorAlertDefinition`

- **Options struct:** `AlertDefinitionUpdateOptions`
- **Response struct:** `AlertDefinition`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

### Backups

#### `POST linode/instances/{linodeId}/backups` → `CreateInstanceSnapshot`

- **Options struct:** `—`
- **Response struct:** `InstanceSnapshot`

**Missing request body fields** (documented but not in SDK Options struct):

- `label`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `finished`
- `updated`

#### `GET linode/instances/{linodeId}/backups/{backupId}` → `GetInstanceSnapshot`

- **Options struct:** `—`
- **Response struct:** `InstanceSnapshot`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `finished`
- `updated`

### Beta programs

#### `GET account/betas` → `ListAccountBetaPrograms`

- **Options struct:** `—`
- **Response struct:** `AccountBetaProgram`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `description`
- `id`
- `label`

#### `GET account/betas/{betaId}` → `GetAccountBetaProgram`

- **Options struct:** `—`
- **Response struct:** `AccountBetaProgram`

**Missing response fields** (documented but not in SDK response struct):

- `ended`
- `enrolled`
- `started`

#### `GET betas` → `ListBetaPrograms`

- **Options struct:** `—`
- **Response struct:** `BetaProgram`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `description`
- `greenlight_only`
- `id`
- `label`
- `more_info`

#### `GET betas/{betaId}` → `GetBetaProgram`

- **Options struct:** `—`
- **Response struct:** `BetaProgram`

**Missing response fields** (documented but not in SDK response struct):

- `ended`
- `started`

### Buckets

#### `GET object-storage/buckets` → `ListObjectStorageBuckets`

- **Options struct:** `—`
- **Response struct:** `ObjectStorageBucket`

**Missing response fields** (documented but not in SDK response struct):

- `created`

#### `POST object-storage/buckets` → `CreateObjectStorageBucket`

- **Options struct:** `ObjectStorageBucketCreateOptions`
- **Response struct:** `ObjectStorageBucket`

**Extra SDK request fields** (in SDK but not in OpenAPI spec):

- `cluster`

**Missing response fields** (documented but not in SDK response struct):

- `created`

#### `GET object-storage/buckets/{regionId}` → `ListObjectStorageBucketsInCluster`

- **Options struct:** `—`
- **Response struct:** `ObjectStorageBucket`

**Missing response fields** (documented but not in SDK response struct):

- `created`

#### `GET object-storage/buckets/{regionId}/{bucket}` → `GetObjectStorageBucket`

- **Options struct:** `—`
- **Response struct:** `ObjectStorageBucket`

**Missing response fields** (documented but not in SDK response struct):

- `created`

#### `GET object-storage/buckets/{regionId}/{bucket}/access` → `GetObjectStorageBucketAccess`

- **Options struct:** `—`
- **Response struct:** `ObjectStorageBucketAccess`

**Missing response fields** (documented but not in SDK response struct):

- `acl_xml`
- `cors_xml`

#### `GET object-storage/buckets/{regionId}/{bucket}/object-list` → `ListObjectStorageBucketContents`

- **Options struct:** `—`
- **Response struct:** `ObjectStorageBucketContent`

**Missing response fields** (documented but not in SDK response struct):

- `etag`
- `last_modified`
- `name`
- `owner`
- `size`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `data`
- `is_truncated`
- `next_marker`

#### `POST object-storage/buckets/{regionId}/{bucket}/object-url` → `CreateObjectStorageObjectURL`

- **Options struct:** `ObjectStorageObjectURLCreateOptions`
- **Response struct:** `ObjectStorageObjectURL`

**Extra SDK request fields** (in SDK but not in OpenAPI spec):

- `content_disposition`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `exists`

### Child accounts

#### `GET account/child-accounts` → `ListChildAccounts`

- **Options struct:** `—`
- **Response struct:** `ChildAccount`

**Missing response fields** (documented but not in SDK response struct):

- `active_since`
- `address_1`
- `address_2`
- `balance`
- `balance_uninvoiced`
- `billing_source`
- `capabilities`
- `city`
- `company`
- `country`
- `credit_card`
- `email`
- `euuid`
- `first_name`
- `last_name`
- `phone`
- `state`
- `tax_id`
- `zip`

#### `GET account/child-accounts/{euuId}` → `GetChildAccount`

- **Options struct:** `—`
- **Response struct:** `ChildAccount`

**Missing response fields** (documented but not in SDK response struct):

- `active_since`
- `address_1`
- `address_2`
- `balance`
- `balance_uninvoiced`
- `billing_source`
- `capabilities`
- `city`
- `company`
- `country`
- `credit_card`
- `email`
- `euuid`
- `first_name`
- `last_name`
- `phone`
- `state`
- `tax_id`
- `zip`

#### `POST account/child-accounts/{euuId}/token` → `CreateChildAccountToken`

- **Options struct:** `—`
- **Response struct:** `ChildAccountToken`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `expiry`
- `id`
- `label`
- `scopes`
- `token`

### Clusters

#### `GET lke/clusters` → `ListLKEClusters`

- **Options struct:** `—`
- **Response struct:** `LKECluster`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `status`

#### `POST lke/clusters` → `CreateLKECluster`

- **Options struct:** `LKEClusterCreateOptions`
- **Response struct:** `LKECluster`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `status`

#### `GET lke/clusters/{clusterId}` → `GetLKECluster`

- **Options struct:** `—`
- **Response struct:** `LKECluster`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `status`

#### `PUT lke/clusters/{clusterId}` → `UpdateLKECluster`

- **Options struct:** `LKEClusterUpdateOptions`
- **Response struct:** `LKECluster`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `status`

### Configuration profile interfaces

#### `POST linode/instances/{linodeId}/configs/{configId}/interfaces` → `AppendInstanceConfigInterface`

- **Options struct:** `InstanceConfigInterfaceCreateOptions`
- **Response struct:** `InstanceConfigInterface`

**Extra SDK request fields** (in SDK but not in OpenAPI spec):

- `ipv6`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `ipv6`

#### `GET linode/instances/{linodeId}/configs/{configId}/interfaces/{interfaceId}` → `GetInstanceConfigInterface`

- **Options struct:** `—`
- **Response struct:** `InstanceConfigInterface`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `ipv6`

#### `PUT linode/instances/{linodeId}/configs/{configId}/interfaces/{interfaceId}` → `UpdateInstanceConfigInterface`

- **Options struct:** `InstanceConfigInterfaceUpdateOptions`
- **Response struct:** `InstanceConfigInterface`

**Extra SDK request fields** (in SDK but not in OpenAPI spec):

- `ipv6`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `ipv6`

### Configuration profiles

#### `GET linode/instances/{linodeId}/configs` → `ListInstanceConfigs`

- **Options struct:** `—`
- **Response struct:** `InstanceConfig`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `init_rd`

#### `POST linode/instances/{linodeId}/configs` → `CreateInstanceConfig`

- **Options struct:** `InstanceConfigCreateOptions`
- **Response struct:** `InstanceConfig`

**Extra SDK request fields** (in SDK but not in OpenAPI spec):

- `init_rd`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `init_rd`

#### `GET linode/instances/{linodeId}/configs/{configId}` → `GetInstanceConfig`

- **Options struct:** `—`
- **Response struct:** `InstanceConfig`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `init_rd`

#### `PUT linode/instances/{linodeId}/configs/{configId}` → `UpdateInstanceConfig`

- **Options struct:** `InstanceConfigUpdateOptions`
- **Response struct:** `InstanceConfig`

**Extra SDK request fields** (in SDK but not in OpenAPI spec):

- `init_rd`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `init_rd`

### Configurations

#### `POST nodebalancers/{nodeBalancerId}/configs` → `CreateNodeBalancerConfig`

- **Options struct:** `NodeBalancerConfigCreateOptions`
- **Response struct:** `NodeBalancerConfig`

**Extra SDK request fields** (in SDK but not in OpenAPI spec):

- `check_passive`
- `cipher_suite`
- `proxy_protocol`
- `ssl_cert`
- `ssl_key`
- `stickiness`

#### `PUT nodebalancers/{nodeBalancerId}/configs/{configId}` → `UpdateNodeBalancerConfig`

- **Options struct:** `NodeBalancerConfigUpdateOptions`
- **Response struct:** `NodeBalancerConfig`

**Missing request body fields** (documented but not in SDK Options struct):

- `algorithm`
- `check`
- `check_attempts`
- `check_body`
- `check_interval`
- `check_path`
- `check_timeout`
- `port`
- `protocol`
- `udp_check_port`

#### `POST nodebalancers/{nodeBalancerId}/configs/{configId}/rebuild` → `RebuildNodeBalancerConfig`

- **Options struct:** `NodeBalancerConfigRebuildOptions`
- **Response struct:** `NodeBalancerConfig`

**Extra SDK request fields** (in SDK but not in OpenAPI spec):

- `check_passive`
- `cipher_suite`
- `proxy_protocol`
- `ssl_cert`
- `ssl_key`
- `stickiness`

### Databases

#### `GET databases/instances` → `ListDatabases`

- **Options struct:** `—`
- **Response struct:** `Database`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `allow_list`
- `cluster_size`
- `encrypted`
- `engine`
- `fork`
- `hosts`
- `id`
- `instance_uri`
- `label`
- `members`
- `platform`
- `port`
- `private_network`
- `region`
- `status`
- `total_disk_size_gb`
- `type`
- `updates`
- `used_disk_size_gb`
- `version`

#### `GET databases/mysql/instances` → `ListMySQLDatabases`

- **Options struct:** `—`
- **Response struct:** `MySQLDatabase`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `allow_list`
- `cluster_size`
- `encrypted`
- `engine`
- `engine_config`
- `fork`
- `hosts`
- `id`
- `label`
- `members`
- `platform`
- `port`
- `private_network`
- `region`
- `ssl_connection`
- `status`
- `total_disk_size_gb`
- `type`
- `updates`
- `used_disk_size_gb`
- `version`

#### `POST databases/mysql/instances` → `CreateMySQLDatabase`

- **Options struct:** `MySQLCreateOptions`
- **Response struct:** `MySQLDatabase`

**Missing request body fields** (documented but not in SDK Options struct):

- `ssl_connection`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `oldest_restore_time`
- `updated`

#### `GET databases/mysql/instances/{instanceId}` → `GetMySQLDatabase`

- **Options struct:** `—`
- **Response struct:** `MySQLDatabase`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `oldest_restore_time`
- `updated`

#### `PUT databases/mysql/instances/{instanceId}` → `UpdateMySQLDatabase`

- **Options struct:** `MySQLUpdateOptions`
- **Response struct:** `MySQLDatabase`

**Extra SDK request fields** (in SDK but not in OpenAPI spec):

- `cluster_size`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `oldest_restore_time`
- `updated`

#### `GET databases/postgresql/instances` → `ListPostgresDatabases`

- **Options struct:** `—`
- **Response struct:** `PostgresDatabase`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `allow_list`
- `cluster_size`
- `encrypted`
- `engine`
- `engine_config`
- `fork`
- `hosts`
- `id`
- `label`
- `members`
- `platform`
- `port`
- `private_network`
- `region`
- `ssl_connection`
- `status`
- `total_disk_size_gb`
- `type`
- `updates`
- `used_disk_size_gb`
- `version`

#### `POST databases/postgresql/instances` → `CreatePostgresDatabase`

- **Options struct:** `PostgresCreateOptions`
- **Response struct:** `PostgresDatabase`

**Missing request body fields** (documented but not in SDK Options struct):

- `ssl_connection`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `private_network`

#### `GET databases/postgresql/instances/{instanceId}` → `GetPostgresDatabase`

- **Options struct:** `—`
- **Response struct:** `PostgresDatabase`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `oldest_restore_time`
- `updated`

#### `PUT databases/postgresql/instances/{instanceId}` → `UpdatePostgresDatabase`

- **Options struct:** `PostgresUpdateOptions`
- **Response struct:** `PostgresDatabase`

**Extra SDK request fields** (in SDK but not in OpenAPI spec):

- `cluster_size`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `oldest_restore_time`
- `updated`

### Devices

#### `GET networking/firewalls/{firewallId}/devices` → `ListFirewallDevices`

- **Options struct:** `—`
- **Response struct:** `FirewallDevice`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

#### `POST networking/firewalls/{firewallId}/devices` → `CreateFirewallDevice`

- **Options struct:** `FirewallDeviceCreateOptions`
- **Response struct:** `FirewallDevice`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

#### `GET networking/firewalls/{firewallId}/devices/{deviceId}` → `GetFirewallDevice`

- **Options struct:** `—`
- **Response struct:** `FirewallDevice`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

### Disks

#### `GET linode/instances/{linodeId}/disks` → `ListInstanceDisks`

- **Options struct:** `—`
- **Response struct:** `InstanceDisk`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

#### `POST linode/instances/{linodeId}/disks` → `CreateInstanceDisk`

- **Options struct:** `InstanceDiskCreateOptions`
- **Response struct:** `InstanceDisk`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

#### `GET linode/instances/{linodeId}/disks/{diskId}` → `GetInstanceDisk`

- **Options struct:** `—`
- **Response struct:** `InstanceDisk`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

#### `PUT linode/instances/{linodeId}/disks/{diskId}` → `UpdateInstanceDisk`

- **Options struct:** `InstanceDiskUpdateOptions`
- **Response struct:** `InstanceDisk`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

#### `POST linode/instances/{linodeId}/disks/{diskId}/clone` → `CloneInstanceDisk`

- **Options struct:** `InstanceDiskCloneOptions`
- **Response struct:** `InstanceDisk`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

#### `POST linode/instances/{linodeId}/disks/{diskId}/password` → `PasswordResetInstanceDisk`

- **Options struct:** `—`
- **Response struct:** `—`

**Missing request body fields** (documented but not in SDK Options struct):

- `password`

#### `POST linode/instances/{linodeId}/disks/{diskId}/resize` → `ResizeInstanceDisk`

- **Options struct:** `—`
- **Response struct:** `—`

**Missing request body fields** (documented but not in SDK Options struct):

- `size`

### Domains

#### `POST domains/import` → `ImportDomain`

- **Options struct:** `DomainImportOptions`
- **Response struct:** `Domain`

**Missing request body fields** (documented but not in SDK Options struct):

- `remote_nameserver`

**Extra SDK request fields** (in SDK but not in OpenAPI spec):

- `remove_nameserver`

### Endpoints

#### `GET object-storage/endpoints` → `ListObjectStorageEndpoints`

- **Options struct:** `—`
- **Response struct:** `ObjectStorageEndpoint`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `endpoint_type`
- `region`
- `s3_endpoint`

### Engines

#### `GET databases/engines` → `ListDatabaseEngines`

- **Options struct:** `—`
- **Response struct:** `DatabaseEngine`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `engine`
- `id`
- `version`

### Events

#### `GET account/events` → `ListEvents`

- **Options struct:** `—`
- **Response struct:** `Event`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `details`
- `time_remaining`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `description`
- `maintenance_policy_set`
- `read`
- `source`

#### `GET account/events/{eventId}` → `GetEvent`

- **Options struct:** `—`
- **Response struct:** `Event`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `details`
- `time_remaining`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `description`
- `maintenance_policy_set`
- `read`
- `source`

### Firewalls

#### `GET linode/instances/{linodeId}/firewalls` → `ListInstanceFirewalls`

- **Options struct:** `—`
- **Response struct:** `Firewall`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `entities`
- `updated`

#### `GET networking/firewalls` → `ListFirewalls`

- **Options struct:** `—`
- **Response struct:** `Firewall`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `entities`
- `updated`

#### `POST networking/firewalls` → `CreateFirewall`

- **Options struct:** `FirewallCreateOptions`
- **Response struct:** `Firewall`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `entities`
- `updated`

#### `GET networking/firewalls/{firewallId}` → `GetFirewall`

- **Options struct:** `—`
- **Response struct:** `Firewall`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `entities`
- `updated`

#### `PUT networking/firewalls/{firewallId}` → `UpdateFirewall`

- **Options struct:** `FirewallUpdateOptions`
- **Response struct:** `Firewall`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `entities`
- `updated`

#### `GET networking/firewalls/{firewallId}/rules` → `GetFirewallRules`

- **Options struct:** `—`
- **Response struct:** `FirewallRuleSet`

**Missing response fields** (documented but not in SDK response struct):

- `fingerprint`
- `version`

#### `PUT networking/firewalls/{firewallId}/rules` → `UpdateFirewallRules`

- **Options struct:** `—`
- **Response struct:** `FirewallRuleSet`

**Missing request body fields** (documented but not in SDK Options struct):

- `inbound`
- `inbound_policy`
- `outbound`
- `outbound_policy`

**Missing response fields** (documented but not in SDK response struct):

- `fingerprint`
- `version`

#### `GET nodebalancers/{nodeBalancerId}/firewalls` → `ListNodeBalancerFirewalls`

- **Options struct:** `—`
- **Response struct:** `Firewall`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `id`
- `label`
- `rules`
- `status`
- `tags`

### Grants

#### `GET profile/grants` → `GrantsList`

- **Options struct:** `—`
- **Response struct:** `GrantsListResponse`

**Missing response fields** (documented but not in SDK response struct):

- `database`
- `domain`
- `firewall`
- `global`
- `image`
- `linode`
- `longview`
- `nodebalancer`
- `stackscript`
- `volume`
- `vpc`

### IP addresses

#### `POST linode/instances/{linodeId}/ips` → `AddInstanceIPAddress`

- **Options struct:** `—`
- **Response struct:** `InstanceIP`

**Missing request body fields** (documented but not in SDK Options struct):

- `public`
- `type`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `reserved`

#### `POST linode/instances/{linodeId}/ips` → `AssignInstanceReservedIP`

- **Options struct:** `InstanceReserveIPOptions`
- **Response struct:** `InstanceIP`

**Extra SDK request fields** (in SDK but not in OpenAPI spec):

- `address`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `reserved`

#### `GET linode/instances/{linodeId}/ips/{address}` → `GetInstanceIPAddress`

- **Options struct:** `—`
- **Response struct:** `InstanceIP`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `reserved`

#### `PUT linode/instances/{linodeId}/ips/{address}` → `UpdateInstanceIPAddress`

- **Options struct:** `IPAddressUpdateOptions`
- **Response struct:** `InstanceIP`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `reserved`

#### `GET networking/ips` → `ListIPAddresses`

- **Options struct:** `—`
- **Response struct:** `InstanceIP`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `address`
- `gateway`
- `interface_id`
- `linode_id`
- `prefix`
- `public`
- `rdns`
- `region`
- `reserved`
- `subnet_mask`
- `type`
- `vpc_nat_1_1`

#### `POST networking/ips` → `AllocateReserveIP`

- **Options struct:** `AllocateReserveIPOptions`
- **Response struct:** `InstanceIP`

**Extra SDK request fields** (in SDK but not in OpenAPI spec):

- `region`
- `reserved`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `reserved`

#### `GET networking/ips/{address}` → `GetIPAddress`

- **Options struct:** `—`
- **Response struct:** `InstanceIP`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `reserved`

#### `PUT networking/ips/{address}` → `UpdateIPAddressV2`

- **Options struct:** `IPAddressUpdateOptionsV2`
- **Response struct:** `InstanceIP`

**Extra SDK request fields** (in SDK but not in OpenAPI spec):

- `reserved`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `reserved`

#### `PUT networking/ips/{address}` → `UpdateIPAddress`

- **Options struct:** `IPAddressUpdateOptions`
- **Response struct:** `InstanceIP`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `reserved`

#### `GET vpcs/ips` → `ListAllVPCIPAddresses`

- **Options struct:** `—`
- **Response struct:** `VPCIP`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `active`
- `address`
- `address_range`
- `config_id`
- `database_id`
- `gateway`
- `interface_id`
- `ipv6_addresses`
- `ipv6_is_public`
- `ipv6_range`
- `linode_id`
- `nat_1_1`
- `nodebalancer_id`
- `prefix`
- `region`
- `subnet_id`
- `subnet_mask`
- `vpc_id`

#### `GET vpcs/{vpcId}/ips` → `ListVPCIPAddresses`

- **Options struct:** `—`
- **Response struct:** `VPCIP`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `active`
- `address`
- `address_range`
- `config_id`
- `database_id`
- `gateway`
- `interface_id`
- `ipv6_addresses`
- `ipv6_is_public`
- `ipv6_range`
- `linode_id`
- `nat_1_1`
- `nodebalancer_id`
- `prefix`
- `region`
- `subnet_id`
- `subnet_mask`
- `vpc_id`

### IPv6 pools

#### `GET networking/ipv6/pools` → `ListIPv6Pools`

- **Options struct:** `—`
- **Response struct:** `IPv6Range`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `is_bgp`
- `linodes`

### IPv6 ranges

#### `GET networking/ipv6/ranges` → `ListIPv6Ranges`

- **Options struct:** `—`
- **Response struct:** `IPv6Range`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `is_bgp`
- `linodes`

#### `POST networking/ipv6/ranges` → `CreateIPv6Range`

- **Options struct:** `IPv6RangeCreateOptions`
- **Response struct:** `IPv6Range`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `is_bgp`
- `linodes`
- `prefix`
- `region`

#### `GET networking/ipv6/ranges/{range}` → `GetIPv6Range`

- **Options struct:** `—`
- **Response struct:** `IPv6Range`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `route_target`

### Image sharing

#### `GET images/sharegroups` → `ListImageShareGroups`

- **Options struct:** `—`
- **Response struct:** `ProducerImageShareGroup`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `expiry`
- `updated`

#### `POST images/sharegroups` → `CreateImageShareGroup`

- **Options struct:** `ImageShareGroupCreateOptions`
- **Response struct:** `ProducerImageShareGroup`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `expiry`
- `updated`

#### `GET images/sharegroups/tokens` → `ImageShareGroupListTokens`

- **Options struct:** `—`
- **Response struct:** `ImageShareGroupToken`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `expiry`
- `updated`

#### `POST images/sharegroups/tokens` → `ImageShareGroupCreateToken`

- **Options struct:** `ImageShareGroupCreateTokenOptions`
- **Response struct:** `ImageShareGroupCreateTokenResponse`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `expiry`
- `updated`

#### `GET images/sharegroups/tokens/{tokenUuid}` → `ImageShareGroupGetToken`

- **Options struct:** `—`
- **Response struct:** `ImageShareGroupToken`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `expiry`
- `updated`

#### `PUT images/sharegroups/tokens/{tokenUuid}` → `ImageShareGroupUpdateToken`

- **Options struct:** `ImageShareGroupUpdateTokenOptions`
- **Response struct:** `ImageShareGroupToken`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `expiry`
- `updated`

#### `GET images/sharegroups/tokens/{tokenUuid}/sharegroup` → `ImageShareGroupGetByToken`

- **Options struct:** `—`
- **Response struct:** `ConsumerImageShareGroup`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

#### `GET images/sharegroups/tokens/{tokenUuid}/sharegroup/images` → `ImageShareGroupGetImageShareEntriesByToken`

- **Options struct:** `—`
- **Response struct:** `ImageShareEntry`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `eol`
- `expiry`
- `updated`

#### `GET images/sharegroups/{sharegroupId}` → `GetImageShareGroup`

- **Options struct:** `—`
- **Response struct:** `ProducerImageShareGroup`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `expiry`
- `updated`

#### `PUT images/sharegroups/{sharegroupId}` → `UpdateImageShareGroup`

- **Options struct:** `ImageShareGroupUpdateOptions`
- **Response struct:** `ProducerImageShareGroup`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `expiry`
- `updated`

#### `GET images/sharegroups/{sharegroupId}/images` → `ImageShareGroupListImageShareEntries`

- **Options struct:** `—`
- **Response struct:** `ImageShareEntry`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `eol`
- `expiry`
- `updated`

#### `PUT images/sharegroups/{sharegroupId}/images/{imageId}` → `ImageShareGroupUpdateImageShareEntry`

- **Options struct:** `ImageShareGroupUpdateImageOptions`
- **Response struct:** `ImageShareEntry`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `eol`
- `expiry`
- `updated`

#### `GET images/sharegroups/{sharegroupId}/members` → `ImageShareGroupListMembers`

- **Options struct:** `—`
- **Response struct:** `ImageShareGroupMember`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `expiry`
- `updated`

#### `POST images/sharegroups/{sharegroupId}/members` → `ImageShareGroupAddMember`

- **Options struct:** `ImageShareGroupAddMemberOptions`
- **Response struct:** `ImageShareGroupMember`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `expiry`
- `updated`

#### `GET images/sharegroups/{sharegroupId}/members/{tokenUuid}` → `ImageShareGroupGetMember`

- **Options struct:** `—`
- **Response struct:** `ImageShareGroupMember`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `expiry`
- `updated`

#### `PUT images/sharegroups/{sharegroupId}/members/{tokenUuid}` → `ImageShareGroupUpdateMember`

- **Options struct:** `ImageShareGroupUpdateMemberOptions`
- **Response struct:** `ImageShareGroupMember`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `expiry`
- `updated`

#### `GET images/{imageId}/sharegroups` → `ListImageShareGroupsContainingPrivateImage`

- **Options struct:** `—`
- **Response struct:** `ProducerImageShareGroup`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `expiry`
- `updated`

### Images

#### `GET images` → `ListImages`

- **Options struct:** `—`
- **Response struct:** `Image`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `eol`
- `expiry`
- `updated`

#### `POST images` → `CreateImage`

- **Options struct:** `ImageCreateOptions`
- **Response struct:** `Image`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `eol`
- `expiry`
- `updated`

#### `GET images/{imageId}` → `GetImage`

- **Options struct:** `—`
- **Response struct:** `Image`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `eol`
- `expiry`
- `updated`

#### `PUT images/{imageId}` → `UpdateImage`

- **Options struct:** `ImageUpdateOptions`
- **Response struct:** `Image`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `eol`
- `expiry`
- `updated`

#### `POST images/{imageId}/regions` → `ReplicateImage`

- **Options struct:** `ImageReplicateOptions`
- **Response struct:** `Image`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `eol`
- `expiry`
- `updated`

### Invoices

#### `GET account/invoices` → `ListInvoices`

- **Options struct:** `—`
- **Response struct:** `Invoice`

**Missing response fields** (documented but not in SDK response struct):

- `date`

#### `GET account/invoices/{invoiceId}` → `GetInvoice`

- **Options struct:** `—`
- **Response struct:** `Invoice`

**Missing response fields** (documented but not in SDK response struct):

- `date`

#### `GET account/invoices/{invoiceId}/items` → `ListInvoiceItems`

- **Options struct:** `—`
- **Response struct:** `InvoiceItem`

**Missing response fields** (documented but not in SDK response struct):

- `from`
- `to`

### Kernels

#### `GET linode/kernels` → `ListKernels`

- **Options struct:** `—`
- **Response struct:** `LinodeKernel`

**Missing response fields** (documented but not in SDK response struct):

- `built`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `xen`

#### `GET linode/kernels/{kernelId}` → `GetKernel`

- **Options struct:** `—`
- **Response struct:** `LinodeKernel`

**Missing response fields** (documented but not in SDK response struct):

- `built`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `xen`

### LKE types

#### `GET lke/types` → `ListLKETypes`

- **Options struct:** `—`
- **Response struct:** `LKEType`

**Missing response fields** (documented but not in SDK response struct):

- `id`
- `label`
- `price`
- `region_prices`
- `transfer`

### Linode instances

#### `GET linode/instances` → `ListInstances`

- **Options struct:** `—`
- **Response struct:** `Instance`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `locks`

#### `POST linode/instances` → `CreateInstance`

- **Options struct:** `InstanceCreateOptions`
- **Response struct:** `Instance`

**Missing request body fields** (documented but not in SDK Options struct):

- `interfaces`

**Extra SDK request fields** (in SDK but not in OpenAPI spec):

- `ipv4`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `locks`

#### `GET linode/instances/{linodeId}` → `GetInstance`

- **Options struct:** `—`
- **Response struct:** `Instance`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `locks`

#### `PUT linode/instances/{linodeId}` → `UpdateInstance`

- **Options struct:** `InstanceUpdateOptions`
- **Response struct:** `Instance`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `locks`

#### `POST linode/instances/{linodeId}/boot` → `BootInstance`

- **Options struct:** `—`
- **Response struct:** `—`

**Missing request body fields** (documented but not in SDK Options struct):

- `config_id`

#### `POST linode/instances/{linodeId}/clone` → `CloneInstance`

- **Options struct:** `InstanceCloneOptions`
- **Response struct:** `Instance`

**Missing request body fields** (documented but not in SDK Options struct):

- `maintenance_policy`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `locks`

#### `POST linode/instances/{linodeId}/mutate` → `MutateInstance`

- **Options struct:** `—`
- **Response struct:** `—`

**Missing request body fields** (documented but not in SDK Options struct):

- `allow_auto_disk_resize`

#### `POST linode/instances/{linodeId}/reboot` → `RebootInstance`

- **Options struct:** `—`
- **Response struct:** `—`

**Missing request body fields** (documented but not in SDK Options struct):

- `config_id`

#### `POST linode/instances/{linodeId}/rebuild` → `RebuildInstance`

- **Options struct:** `InstanceRebuildOptions`
- **Response struct:** `Instance`

**Missing request body fields** (documented but not in SDK Options struct):

- `maintenance_policy`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `locks`

### Linode interfaces

#### `GET linode/instances/{linodeId}/interfaces` → `ListInterfaces`

- **Options struct:** `—`
- **Response struct:** `LinodeInterface`

**Missing response fields** (documented but not in SDK response struct):

- `interfaces`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `default_route`
- `id`
- `mac_address`
- `public`
- `version`
- `vlan`
- `vpc`

#### `POST linode/instances/{linodeId}/interfaces` → `CreateInterface`

- **Options struct:** `LinodeInterfaceCreateOptions`
- **Response struct:** `LinodeInterface`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

#### `GET linode/instances/{linodeId}/interfaces/{interfaceId}` → `GetInterface`

- **Options struct:** `—`
- **Response struct:** `LinodeInterface`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

#### `PUT linode/instances/{linodeId}/interfaces/{interfaceId}` → `UpdateInterface`

- **Options struct:** `LinodeInterfaceUpdateOptions`
- **Response struct:** `LinodeInterface`

**Missing request body fields** (documented but not in SDK Options struct):

- `vlan`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

#### `GET linode/instances/{linodeId}/interfaces/{interfaceId}/firewalls` → `ListInterfaceFirewalls`

- **Options struct:** `—`
- **Response struct:** `Firewall`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `id`
- `label`
- `rules`
- `status`
- `tags`

### Linode types

#### `GET linode/types` → `ListTypes`

- **Options struct:** `—`
- **Response struct:** `LinodeType`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `accelerated_devices`

#### `GET linode/types/{typeId}` → `GetType`

- **Options struct:** `—`
- **Response struct:** `LinodeType`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `accelerated_devices`

### Longview clients

#### `GET longview/clients` → `ListLongviewClients`

- **Options struct:** `—`
- **Response struct:** `LongviewClient`

**Missing response fields** (documented but not in SDK response struct):

- `apps`
- `created`
- `updated`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `apache`
- `mysql`
- `nginx`

#### `POST longview/clients` → `CreateLongviewClient`

- **Options struct:** `LongviewClientCreateOptions`
- **Response struct:** `LongviewClient`

**Missing response fields** (documented but not in SDK response struct):

- `apps`
- `created`
- `updated`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `apache`
- `mysql`
- `nginx`

#### `GET longview/clients/{clientId}` → `GetLongviewClient`

- **Options struct:** `—`
- **Response struct:** `LongviewClient`

**Missing response fields** (documented but not in SDK response struct):

- `apps`
- `created`
- `updated`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `apache`
- `mysql`
- `nginx`

#### `PUT longview/clients/{clientId}` → `UpdateLongviewClient`

- **Options struct:** `LongviewClientUpdateOptions`
- **Response struct:** `LongviewClient`

**Missing response fields** (documented but not in SDK response struct):

- `apps`
- `created`
- `updated`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `apache`
- `mysql`
- `nginx`

### Longview plans

#### `GET longview/plan` → `GetLongviewPlan`

- **Options struct:** `—`
- **Response struct:** `LongviewPlan`

**Missing response fields** (documented but not in SDK response struct):

- `price`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `hourly`
- `monthly`

#### `PUT longview/plan` → `UpdateLongviewPlan`

- **Options struct:** `LongviewPlanUpdateOptions`
- **Response struct:** `LongviewPlan`

**Missing response fields** (documented but not in SDK response struct):

- `price`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `hourly`
- `monthly`

### Longview subscriptions

#### `GET longview/subscriptions` → `ListLongviewSubscriptions`

- **Options struct:** `—`
- **Response struct:** `LongviewSubscription`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `updated`

#### `GET longview/subscriptions/{subscriptionId}` → `GetLongviewSubscription`

- **Options struct:** `—`
- **Response struct:** `LongviewSubscription`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `updated`

### Maintenances

#### `GET account/maintenance` → `ListMaintenances`

- **Options struct:** `—`
- **Response struct:** `AccountMaintenance`

**Missing response fields** (documented but not in SDK response struct):

- `complete_time`
- `not_before`
- `start_time`

### Metrics

#### `GET monitor/dashboards` → `ListMonitorDashboards`

- **Options struct:** `—`
- **Response struct:** `MonitorDashboard`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `id`
- `label`
- `service_type`
- `type`
- `widgets`

#### `GET monitor/dashboards/{dashboardId}` → `GetMonitorDashboard`

- **Options struct:** `—`
- **Response struct:** `MonitorDashboard`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

#### `GET monitor/services` → `ListMonitorServices`

- **Options struct:** `—`
- **Response struct:** `MonitorService`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `alert`

#### `GET monitor/services/{serviceType}` → `GetMonitorServiceByType`

- **Options struct:** `—`
- **Response struct:** `MonitorService`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `alert`

#### `GET monitor/services/{serviceType}/dashboards` → `ListMonitorDashboardsByServiceType`

- **Options struct:** `—`
- **Response struct:** `MonitorDashboard`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

### Network transfer prices

#### `GET network-transfer/prices` → `ListNetworkTransferPrices`

- **Options struct:** `—`
- **Response struct:** `NetworkTransferPrice`

**Missing response fields** (documented but not in SDK response struct):

- `id`
- `label`
- `price`
- `region_prices`
- `transfer`

### Node pools

#### `POST lke/clusters/{clusterId}/pools` → `CreateLKENodePool`

- **Options struct:** `LKENodePoolCreateOptions`
- **Response struct:** `LKENodePool`

**Missing request body fields** (documented but not in SDK Options struct):

- `disk_encryption`

#### `PUT lke/clusters/{clusterId}/pools/{poolId}` → `UpdateLKENodePool`

- **Options struct:** `LKENodePoolUpdateOptions`
- **Response struct:** `LKENodePool`

**Extra SDK request fields** (in SDK but not in OpenAPI spec):

- `k8s_version`
- `label`
- `update_strategy`

### NodeBalancer types

#### `GET nodebalancers/types` → `ListNodeBalancerTypes`

- **Options struct:** `—`
- **Response struct:** `NodeBalancerType`

**Missing response fields** (documented but not in SDK response struct):

- `id`
- `label`
- `price`
- `region_prices`
- `transfer`

### NodeBalancers

#### `GET linode/instances/{linodeId}/nodebalancers` → `ListInstanceNodeBalancers`

- **Options struct:** `—`
- **Response struct:** `NodeBalancer`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `lke_cluster`
- `updated`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `client_udp_sess_throttle`
- `locks`

#### `GET nodebalancers` → `ListNodeBalancers`

- **Options struct:** `—`
- **Response struct:** `NodeBalancer`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `lke_cluster`
- `updated`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `client_udp_sess_throttle`
- `locks`

#### `POST nodebalancers` → `CreateNodeBalancer`

- **Options struct:** `NodeBalancerCreateOptions`
- **Response struct:** `NodeBalancer`

**Extra SDK request fields** (in SDK but not in OpenAPI spec):

- `client_udp_sess_throttle`
- `ipv4`
- `type`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `lke_cluster`
- `updated`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `client_udp_sess_throttle`
- `locks`

#### `GET nodebalancers/{nodeBalancerId}` → `GetNodeBalancer`

- **Options struct:** `—`
- **Response struct:** `NodeBalancer`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `lke_cluster`
- `updated`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `client_udp_sess_throttle`
- `locks`

#### `PUT nodebalancers/{nodeBalancerId}` → `UpdateNodeBalancer`

- **Options struct:** `NodeBalancerUpdateOptions`
- **Response struct:** `NodeBalancer`

**Extra SDK request fields** (in SDK but not in OpenAPI spec):

- `client_udp_sess_throttle`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `lke_cluster`
- `updated`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `client_udp_sess_throttle`
- `locks`

### Nodes

#### `GET lke/clusters/{clusterId}/nodes/{nodeId}` → `GetLKENodePoolNode`

- **Options struct:** `—`
- **Response struct:** `LKENodePoolLinode`

**Missing response fields** (documented but not in SDK response struct):

- `pool_id`

#### `POST nodebalancers/{nodeBalancerId}/configs/{configId}/nodes` → `CreateNodeBalancerNode`

- **Options struct:** `NodeBalancerNodeCreateOptions`
- **Response struct:** `NodeBalancerNode`

**Extra SDK request fields** (in SDK but not in OpenAPI spec):

- `mode`

#### `PUT nodebalancers/{nodeBalancerId}/configs/{configId}/nodes/{nodeId}` → `UpdateNodeBalancerNode`

- **Options struct:** `NodeBalancerNodeUpdateOptions`
- **Response struct:** `NodeBalancerNode`

**Extra SDK request fields** (in SDK but not in OpenAPI spec):

- `mode`

### Notifications

#### `GET account/notifications` → `ListNotifications`

- **Options struct:** `—`
- **Response struct:** `Notification`

**Missing response fields** (documented but not in SDK response struct):

- `until`
- `when`

### OAuth apps

#### `GET profile/apps` → `ListProfileApps`

- **Options struct:** `—`
- **Response struct:** `ProfileApp`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `expiry`

#### `GET profile/apps/{appId}` → `GetProfileApp`

- **Options struct:** `—`
- **Response struct:** `ProfileApp`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `expiry`

### Object Storage

#### `GET object-storage/quotas` → `ListObjectStorageQuotas`

- **Options struct:** `—`
- **Response struct:** `ObjectStorageQuota`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `description`
- `endpoint_type`
- `quota_id`
- `quota_limit`
- `quota_name`
- `resource_metric`
- `s3_endpoint`

### Payment methods

#### `GET account/payment-methods` → `ListPaymentMethods`

- **Options struct:** `—`
- **Response struct:** `PaymentMethod`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `data`

#### `GET account/payment-methods/{paymentMethodId}` → `GetPaymentMethod`

- **Options struct:** `—`
- **Response struct:** `PaymentMethod`

**Missing response fields** (documented but not in SDK response struct):

- `card_type`
- `email`
- `expiry`
- `last_four`
- `paypal_id`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `created`
- `data`
- `id`
- `is_default`
- `type`

### Payments

#### `GET account/payments` → `ListPayments`

- **Options struct:** `—`
- **Response struct:** `Payment`

**Missing response fields** (documented but not in SDK response struct):

- `date`

#### `POST account/payments` → `CreatePayment`

- **Options struct:** `PaymentCreateOptions`
- **Response struct:** `Payment`

**Missing request body fields** (documented but not in SDK Options struct):

- `payment_method_id`

**Extra SDK request fields** (in SDK but not in OpenAPI spec):

- `cvv`

**Missing response fields** (documented but not in SDK response struct):

- `date`
- `warnings`

#### `GET account/payments/{paymentId}` → `GetPayment`

- **Options struct:** `—`
- **Response struct:** `Payment`

**Missing response fields** (documented but not in SDK response struct):

- `date`

### Personal access tokens

#### `GET profile/tokens` → `ListTokens`

- **Options struct:** `—`
- **Response struct:** `Token`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `expiry`

#### `POST profile/tokens` → `CreateToken`

- **Options struct:** `TokenCreateOptions`
- **Response struct:** `Token`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `expiry`

#### `GET profile/tokens/{tokenId}` → `GetToken`

- **Options struct:** `—`
- **Response struct:** `Token`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `expiry`

#### `PUT profile/tokens/{tokenId}` → `UpdateToken`

- **Options struct:** `TokenUpdateOptions`
- **Response struct:** `Token`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `expiry`

### Placement groups

#### `POST placement/groups` → `CreatePlacementGroup`

- **Options struct:** `—`
- **Response struct:** `PlacementGroup`

**Missing request body fields** (documented but not in SDK Options struct):

- `label`
- `placement_group_policy`
- `placement_group_type`
- `region`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `migrations`

#### `PUT placement/groups/{groupId}` → `UpdatePlacementGroup`

- **Options struct:** `—`
- **Response struct:** `PlacementGroup`

**Missing request body fields** (documented but not in SDK Options struct):

- `label`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `migrations`

#### `POST placement/groups/{groupId}/assign` → `AssignPlacementGroupLinodes`

- **Options struct:** `—`
- **Response struct:** `PlacementGroup`

**Missing request body fields** (documented but not in SDK Options struct):

- `linodes`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `migrations`

#### `POST placement/groups/{groupId}/unassign` → `UnassignPlacementGroupLinodes`

- **Options struct:** `—`
- **Response struct:** `PlacementGroup`

**Missing request body fields** (documented but not in SDK Options struct):

- `linodes`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `migrations`

### Promo credits

#### `POST account/promo-codes` → `AddPromoCode`

- **Options struct:** `PromoCodeCreateOptions`
- **Response struct:** `Promotion`

**Missing response fields** (documented but not in SDK response struct):

- `expire_dt`

### Records

#### `GET domains/{domainId}/records` → `ListDomainRecords`

- **Options struct:** `—`
- **Response struct:** `DomainRecord`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

#### `POST domains/{domainId}/records` → `CreateDomainRecord`

- **Options struct:** `DomainRecordCreateOptions`
- **Response struct:** `DomainRecord`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

#### `GET domains/{domainId}/records/{recordId}` → `GetDomainRecord`

- **Options struct:** `—`
- **Response struct:** `DomainRecord`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

#### `PUT domains/{domainId}/records/{recordId}` → `UpdateDomainRecord`

- **Options struct:** `DomainRecordUpdateOptions`
- **Response struct:** `DomainRecord`

**Extra SDK request fields** (in SDK but not in OpenAPI spec):

- `type`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

### Regions

#### `GET regions/availability` → `ListRegionsAvailability`

- **Options struct:** `—`
- **Response struct:** `RegionAvailability`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `available`
- `plan`
- `region`

### SSH keys

#### `GET profile/sshkeys` → `ListSSHKeys`

- **Options struct:** `—`
- **Response struct:** `SSHKey`

**Missing response fields** (documented but not in SDK response struct):

- `created`

#### `POST profile/sshkeys` → `CreateSSHKey`

- **Options struct:** `SSHKeyCreateOptions`
- **Response struct:** `SSHKey`

**Missing response fields** (documented but not in SDK response struct):

- `created`

#### `GET profile/sshkeys/{sshKeyId}` → `GetSSHKey`

- **Options struct:** `—`
- **Response struct:** `SSHKey`

**Missing response fields** (documented but not in SDK response struct):

- `created`

#### `PUT profile/sshkeys/{sshKeyId}` → `UpdateSSHKey`

- **Options struct:** `SSHKeyUpdateOptions`
- **Response struct:** `SSHKey`

**Missing response fields** (documented but not in SDK response struct):

- `created`

### Security questions

#### `POST profile/security-questions` → `SecurityQuestionsAnswer`

- **Options struct:** `SecurityQuestionsAnswerOptions`
- **Response struct:** `—`

**Missing response fields** (documented but not in SDK response struct):

- `security_questions`

### Service transfers

#### `GET account/service-transfers` → `ListAccountServiceTransfer`

- **Options struct:** `—`
- **Response struct:** `AccountServiceTransfer`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `expiry`
- `updated`

#### `POST account/service-transfers` → `RequestAccountServiceTransfer`

- **Options struct:** `AccountServiceTransferRequestOptions`
- **Response struct:** `AccountServiceTransfer`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `expiry`
- `updated`

#### `GET account/service-transfers/{token}` → `GetAccountServiceTransfer`

- **Options struct:** `—`
- **Response struct:** `AccountServiceTransfer`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `expiry`
- `updated`

### StackScripts

#### `GET linode/stackscripts` → `ListStackscripts`

- **Options struct:** `—`
- **Response struct:** `Stackscript`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `logo_url`
- `ordinal`

#### `POST linode/stackscripts` → `CreateStackscript`

- **Options struct:** `StackscriptCreateOptions`
- **Response struct:** `Stackscript`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `logo_url`
- `ordinal`

#### `GET linode/stackscripts/{stackscriptId}` → `GetStackscript`

- **Options struct:** `—`
- **Response struct:** `Stackscript`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `logo_url`
- `ordinal`

#### `PUT linode/stackscripts/{stackscriptId}` → `UpdateStackscript`

- **Options struct:** `StackscriptUpdateOptions`
- **Response struct:** `Stackscript`

**Missing request body fields** (documented but not in SDK Options struct):

- `description`
- `images`
- `is_public`
- `label`
- `rev_note`
- `script`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `logo_url`
- `ordinal`

### Statistics

#### `GET linode/instances/{linodeId}/stats` → `GetInstanceStats`

- **Options struct:** `—`
- **Response struct:** `InstanceStats`

**Missing response fields** (documented but not in SDK response struct):

- `cpu`
- `io`
- `netv4`
- `netv6`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `data`

#### `GET linode/instances/{linodeId}/stats/{year}/{month}` → `GetInstanceStatsByDate`

- **Options struct:** `—`
- **Response struct:** `InstanceStats`

**Missing response fields** (documented but not in SDK response struct):

- `cpu`
- `io`
- `netv4`
- `netv6`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `data`

#### `GET nodebalancers/{nodeBalancerId}/stats` → `GetNodeBalancerStats`

- **Options struct:** `—`
- **Response struct:** `NodeBalancerStats`

**Missing response fields** (documented but not in SDK response struct):

- `connections`
- `traffic`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `data`
- `title`

### Support tickets

#### `GET support/tickets` → `ListTickets`

- **Options struct:** `—`
- **Response struct:** `Ticket`

**Missing response fields** (documented but not in SDK response struct):

- `closable`
- `closed`
- `opened`
- `severity`
- `updated`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `closeable`

#### `GET support/tickets/{ticketId}` → `GetTicket`

- **Options struct:** `—`
- **Response struct:** `Ticket`

**Missing response fields** (documented but not in SDK response struct):

- `closable`
- `closed`
- `opened`
- `severity`
- `updated`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `closeable`

### Tags

#### `POST tags` → `CreateTag`

- **Options struct:** `TagCreateOptions`
- **Response struct:** `Tag`

**Extra SDK request fields** (in SDK but not in OpenAPI spec):

- `lke_clusters`

#### `GET tags/{tagLabel}` → `ListTaggedObjects`

- **Options struct:** `—`
- **Response struct:** `TaggedObject`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `data`

### Trusted devices

#### `GET profile/devices` → `ListProfileDevices`

- **Options struct:** `—`
- **Response struct:** `ProfileDevice`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `expiry`
- `last_authenticated`

#### `GET profile/devices/{deviceId}` → `GetProfileDevice`

- **Options struct:** `—`
- **Response struct:** `ProfileDevice`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `expiry`
- `last_authenticated`

### Types

#### `GET databases/types` → `ListDatabaseTypes`

- **Options struct:** `—`
- **Response struct:** `DatabaseType`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `class`
- `deprecated`
- `disk`
- `engines`
- `id`
- `label`
- `memory`
- `vcpus`

#### `GET databases/types/{typeId}` → `GetDatabaseType`

- **Options struct:** `—`
- **Response struct:** `DatabaseType`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `deprecated`

### Users

#### `GET account/users` → `ListUsers`

- **Options struct:** `—`
- **Response struct:** `User`

**Missing response fields** (documented but not in SDK response struct):

- `password_created`

#### `POST account/users` → `CreateUser`

- **Options struct:** `UserCreateOptions`
- **Response struct:** `User`

**Missing response fields** (documented but not in SDK response struct):

- `password_created`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `user_type`

#### `GET account/users/{username}` → `GetUser`

- **Options struct:** `—`
- **Response struct:** `User`

**Missing response fields** (documented but not in SDK response struct):

- `password_created`

#### `PUT account/users/{username}` → `UpdateUser`

- **Options struct:** `UserUpdateOptions`
- **Response struct:** `User`

**Missing response fields** (documented but not in SDK response struct):

- `password_created`

#### `GET account/users/{username}/grants` → `GetUserGrants`

- **Options struct:** `—`
- **Response struct:** `UserGrants`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `placement_group`

#### `PUT account/users/{username}/grants` → `UpdateUserGrants`

- **Options struct:** `UserGrantsUpdateOptions`
- **Response struct:** `UserGrants`

**Extra SDK request fields** (in SDK but not in OpenAPI spec):

- `placement_group`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `placement_group`

### VLANs

#### `GET networking/vlans` → `ListVLANs`

- **Options struct:** `—`
- **Response struct:** `VLAN`

**Missing response fields** (documented but not in SDK response struct):

- `created`

### VPC subnets

#### `GET vpcs/{vpcId}/subnets` → `ListVPCSubnets`

- **Options struct:** `—`
- **Response struct:** `VPCSubnet`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `databases`
- `id`
- `ipv4`
- `ipv6`
- `label`
- `linodes`
- `nodebalancers`

#### `POST vpcs/{vpcId}/subnets` → `CreateVPCSubnet`

- **Options struct:** `VPCSubnetCreateOptions`
- **Response struct:** `VPCSubnet`

**Extra SDK request fields** (in SDK but not in OpenAPI spec):

- `ipv6`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `ipv6`

#### `GET vpcs/{vpcId}/subnets/{vpcSubnetId}` → `GetVPCSubnet`

- **Options struct:** `—`
- **Response struct:** `VPCSubnet`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `ipv6`

#### `PUT vpcs/{vpcId}/subnets/{vpcSubnetId}` → `UpdateVPCSubnet`

- **Options struct:** `VPCSubnetUpdateOptions`
- **Response struct:** `VPCSubnet`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `ipv6`

### VPCs

#### `GET nodebalancers/{nodeBalancerId}/vpcs` → `ListNodeBalancerVPCConfigs`

- **Options struct:** `—`
- **Response struct:** `NodeBalancerVPCConfig`

**Missing response fields** (documented but not in SDK response struct):

- `ipv4_range_auto_assign`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `ipv6_range`

#### `GET nodebalancers/{nodeBalancerId}/vpcs/{nodeBalancerVpcConfigId}` → `GetNodeBalancerVPCConfig`

- **Options struct:** `—`
- **Response struct:** `NodeBalancerVPCConfig`

**Missing response fields** (documented but not in SDK response struct):

- `ipv4_range_auto_assign`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `ipv6_range`

#### `GET vpcs` → `ListVPCs`

- **Options struct:** `—`
- **Response struct:** `VPC`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `description`
- `id`
- `ipv6`
- `label`
- `region`
- `subnets`

#### `POST vpcs` → `CreateVPC`

- **Options struct:** `VPCCreateOptions`
- **Response struct:** `VPC`

**Extra SDK request fields** (in SDK but not in OpenAPI spec):

- `ipv6`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `ipv6`

#### `GET vpcs/{vpcId}` → `GetVPC`

- **Options struct:** `—`
- **Response struct:** `VPC`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `ipv6`

#### `PUT vpcs/{vpcId}` → `UpdateVPC`

- **Options struct:** `VPCUpdateOptions`
- **Response struct:** `VPC`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

**Extra SDK response fields** (in SDK but not in OpenAPI spec):

- `ipv6`

### Volume types

#### `GET volumes/types` → `ListVolumeTypes`

- **Options struct:** `—`
- **Response struct:** `VolumeType`

**Missing response fields** (documented but not in SDK response struct):

- `id`
- `label`
- `price`
- `region_prices`
- `transfer`

### Volumes

#### `GET linode/instances/{linodeId}/volumes` → `ListInstanceVolumes`

- **Options struct:** `—`
- **Response struct:** `Volume`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

#### `GET volumes` → `ListVolumes`

- **Options struct:** `—`
- **Response struct:** `Volume`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

#### `POST volumes` → `CreateVolume`

- **Options struct:** `VolumeCreateOptions`
- **Response struct:** `Volume`

**Extra SDK request fields** (in SDK but not in OpenAPI spec):

- `persist_across_boots`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

#### `GET volumes/{volumeId}` → `GetVolume`

- **Options struct:** `—`
- **Response struct:** `Volume`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

#### `PUT volumes/{volumeId}` → `UpdateVolume`

- **Options struct:** `VolumeUpdateOptions`
- **Response struct:** `Volume`

**Missing request body fields** (documented but not in SDK Options struct):

- `region`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

#### `POST volumes/{volumeId}/attach` → `AttachVolume`

- **Options struct:** `—`
- **Response struct:** `Volume`

**Missing request body fields** (documented but not in SDK Options struct):

- `config_id`
- `linode_id`
- `persist_across_boots`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

#### `POST volumes/{volumeId}/clone` → `CloneVolume`

- **Options struct:** `—`
- **Response struct:** `Volume`

**Missing request body fields** (documented but not in SDK Options struct):

- `label`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `updated`

#### `POST volumes/{volumeId}/resize` → `ResizeVolume`

- **Options struct:** `—`
- **Response struct:** `—`

**Missing request body fields** (documented but not in SDK Options struct):

- `size`

**Missing response fields** (documented but not in SDK response struct):

- `created`
- `encryption`
- `filesystem_path`
- `hardware_type`
- `id`
- `io_ready`
- `label`
- `linode_id`
- `linode_label`
- `region`
- `size`
- `status`
- `tags`
- `updated`

## SDK Methods Without OpenAPI Match

These SDK methods exist but could not be matched to any endpoint in the current OpenAPI spec.
They may use different path patterns, be internal helpers, or target endpoints not yet in the spec.

| SDK Method | HTTP | Path | File |
|------------|------|------|------|
| `CreateFirewallRuleSet` | POST | `networking/firewalls/rulesets` | firewall_rulesets.go |
| `CreateLock` | POST | `locks` | locks.go |
| `DeleteFirewallRuleSet` | DELETE | `networking/firewalls/rulesets/%d` | firewall_rulesets.go |
| `DeleteLock` | DELETE | `locks/%d` | locks.go |
| `DeleteReservedIPAddress` | DELETE | `networking/reserved/ips/%s` | network_reserved_ips.go |
| `GetEntityRoles` | GET | `iam/users/%s/permissions/%s/%d` | entities.go |
| `GetFirewallRuleSet` | GET | `networking/firewalls/rulesets/%d` | firewall_rulesets.go |
| `GetFirewallRulesExpansion` | GET | `networking/firewalls/%d/rules/expansion` | firewall_rules.go |
| `GetIPv6Pool` | GET | `networking/ipv6/pools/%s` | network_pools.go |
| `GetLock` | GET | `locks/%d` | locks.go |
| `GetPrefixList` | GET | `networking/prefixlists/%d` | prefixlists.go |
| `GetRegionVPCAvailability` | GET | `regions/%s/vpc-availability` | regions_availability.go |
| `GetReservedIPAddress` | GET | `networking/reserved/ips/%s` | network_reserved_ips.go |
| `GetUserAccountPermissions` | GET | `iam/users/%s/permissions/account` | iam.go |
| `ListAllVPCIPv6Addresses` | GET | `vpcs/ipv6s` | vpc_ips.go |
| `ListFirewallRuleSets` | GET | `networking/firewalls/rulesets` | firewall_rulesets.go |
| `ListLocks` | GET | `locks` | locks.go |
| `ListPrefixLists` | GET | `networking/prefixlists` | prefixlists.go |
| `ListRegionsVPCAvailability` | GET | `regions/vpc-availability` | regions_availability.go |
| `ListReservedIPAddresses` | GET | `networking/reserved/ips` | network_reserved_ips.go |
| `ListVPCIPv6Addresses` | GET | `vpcs/%d/ipv6s` | vpc_ips.go |
| `MarkEventRead` | POST | `account/events/%d/read` | account_events.go |
| `ReserveIPAddress` | POST | `networking/reserved/ips` | network_reserved_ips.go |
| `SetDefaultPaymentMethod` | POST | `account/payment-methods/%d` | account_payment_methods.go |
| `UpdateFirewallRuleSet` | PUT | `networking/firewalls/rulesets/%d` | firewall_rulesets.go |
| `simpleInstanceAction` | POST | `linode/instances/%d/%s` | instances.go |

## Missing Endpoints Summary

Complete list of API endpoints documented in the OpenAPI spec that are not implemented in the SDK.

| # | Method | Endpoint | Operation ID | Summary |
|---|--------|----------|-------------|---------|
| 1 | DELETE | `account/entity-transfers/{token}` | `delete-entity-transfer` | Cancel an entity transfer |
| 2 | DELETE | `managed/contacts/{contactId}` | `delete-managed-contact` | Delete a managed contact |
| 3 | DELETE | `managed/services/{serviceId}` | `delete-managed-service` | Delete a managed service monitor |
| 4 | DELETE | `monitor/streams/destinations/{destinationId}` | `delete-destination` | Delete a destination |
| 5 | DELETE | `monitor/streams/{streamId}` | `delete-stream` | Delete a stream |
| 6 | DELETE | `networking/vlans/{regionId}/{label}` | `delete-vlan` | Delete a VLAN |
| 7 | GET | `account/entity-transfers` | `get-entity-transfers` | List entity transfers |
| 8 | GET | `account/entity-transfers/{token}` | `get-entity-transfer` | Get an entity transfer |
| 9 | GET | `account/oauth-clients/{clientId}/thumbnail` | `get-client-thumbnail` | Get the OAuth client's thumbnail |
| 10 | GET | `linode/instances/{linodeId}/interfaces/history` | `get-linode-interface-history` | List a Linode's network interface history |
| 11 | GET | `longview/types` | `get-longview-types` | List Longview types |
| 12 | GET | `managed/contacts` | `get-managed-contacts` | List managed contacts |
| 13 | GET | `managed/contacts/{contactId}` | `get-managed-contact` | Get a managed contact |
| 14 | GET | `managed/credentials` | `get-managed-credentials` | List managed credentials |
| 15 | GET | `managed/credentials/sshkey` | `get-managed-ssh-key` | Get a managed SSH key |
| 16 | GET | `managed/credentials/{credentialId}` | `get-managed-credential` | Get a managed credential |
| 17 | GET | `managed/issues` | `get-managed-issues` | List managed issues |
| 18 | GET | `managed/issues/{issueId}` | `get-managed-issue` | Get a managed issue |
| 19 | GET | `managed/linode-settings` | `get-managed-linode-settings` | List managed Linode settings |
| 20 | GET | `managed/linode-settings/{linodeId}` | `get-managed-linode-setting` | Get a Linode's managed settings |
| 21 | GET | `managed/services` | `get-managed-services` | List managed services |
| 22 | GET | `managed/services/{serviceId}` | `get-managed-service` | Get a managed service monitor |
| 23 | GET | `managed/stats` | `get-managed-stats` | List managed stats |
| 24 | GET | `monitor/streams` | `get-streams` | List streams |
| 25 | GET | `monitor/streams/destinations` | `get-destinations` | List destinations |
| 26 | GET | `monitor/streams/destinations/{destinationId}` | `get-destination` | Get a destination |
| 27 | GET | `monitor/streams/destinations/{destinationId}/history` | `get-destination-history` | Get a destination's history |
| 28 | GET | `monitor/streams/{streamId}` | `get-stream` | Get a stream |
| 29 | GET | `monitor/streams/{streamId}/history` | `get-stream-history` | Get a stream's history |
| 30 | GET | `networking/firewalls/{firewallId}/history` | `get-firewall-rule-versions` | List firewall rule versions |
| 31 | GET | `networking/firewalls/{firewallId}/history/rules/{version}` | `get-firewall-rule-version` | Get a firewall rule version |
| 32 | GET | `object-storage/types` | `get-object-storage-types` | List Object Storage types |
| 33 | GET | `support/tickets/{ticketId}/replies` | `get-ticket-replies` | List replies |
| 34 | POST | `account/cancel` | `post-cancel-account` | Delete your account |
| 35 | POST | `account/credit-card` | `post-credit-card` | Add or edit a credit card |
| 36 | POST | `account/entity-transfers` | `post-entity-transfer` | Create an entity transfer |
| 37 | POST | `account/entity-transfers/{token}/accept` | `post-accept-entity-transfer` | Accept an entity transfer |
| 38 | POST | `account/payment-methods/{paymentMethodId}/make-default` | `post-make-payment-method-default` | Set a default payment method |
| 39 | POST | `account/payments/paypal` | `post-pay-pal-payment` | Stage a PayPal payment |
| 40 | POST | `account/payments/paypal/execute` | `post-execute-pay-pal-payment` | Execute a PayPal payment |
| 41 | POST | `account/settings/managed-enable` | `post-enable-account-managed` | Enable Linode Managed |
| 42 | POST | `images/sharegroups/{sharegroupId}/images` | `post-sharegroup-images` | Add images to a share group |
| 43 | POST | `linode/instances/{linodeId}/firewalls/apply` | `post-apply-firewalls` | Apply a Linode's firewalls |
| 44 | POST | `managed/contacts` | `post-managed-contact` | Create a managed contact |
| 45 | POST | `managed/credentials` | `post-managed-credential` | Create a managed credential |
| 46 | POST | `managed/credentials/{credentialId}/revoke` | `post-managed-credential-revoke` | Delete a managed credential |
| 47 | POST | `managed/credentials/{credentialId}/update` | `post-managed-credential-username-password` | Update a managed credential's username and password |
| 48 | POST | `managed/services` | `post-managed-service` | Create a managed service |
| 49 | POST | `managed/services/{serviceId}/disable` | `post-disable-managed-service` | Disable a managed service monitor |
| 50 | POST | `managed/services/{serviceId}/enable` | `post-enable-managed-service` | Enable a managed service monitor |
| 51 | POST | `monitor/services/{serviceType}/metrics` | `post-read-metric` | Get an entity's metrics |
| 52 | POST | `monitor/streams` | `post-stream` | Create a stream |
| 53 | POST | `monitor/streams/destinations` | `post-destination` | Create a destination |
| 54 | POST | `networking/ipv4/assign` | `post-assign-ipv4s` | Assign IPv4s to Linodes |
| 55 | POST | `networking/ipv4/share` | `post-share-ipv4s` | Configure IPv4 sharing |
| 56 | POST | `support/tickets` | `post-ticket` | Open a support ticket |
| 57 | POST | `support/tickets/{ticketId}/attachments` | `post-ticket-attachment` | Create a support ticket attachment |
| 58 | POST | `support/tickets/{ticketId}/close` | `post-close-ticket` | Close a support ticket |
| 59 | POST | `support/tickets/{ticketId}/replies` | `post-ticket-reply` | Create a reply |
| 60 | PUT | `account/oauth-clients/{clientId}/thumbnail` | `put-client-thumbnail` | Update the OAuth client's thumbnail |
| 61 | PUT | `linode/instances/{linodeId}/firewalls` | `put-linode-firewalls` | Update a Linode's firewalls |
| 62 | PUT | `managed/contacts/{contactId}` | `put-managed-contact` | Update a managed contact |
| 63 | PUT | `managed/credentials/{credentialId}` | `put-managed-credential` | Update a managed credential |
| 64 | PUT | `managed/linode-settings/{linodeId}` | `put-managed-linode-setting` | Update a Linode's managed settings |
| 65 | PUT | `managed/services/{serviceId}` | `put-managed-service` | Update a managed service monitor |
| 66 | PUT | `monitor/streams/destinations/{destinationId}` | `put-destination` | Update a destination |
| 67 | PUT | `monitor/streams/{streamId}` | `put-stream` | Update a stream |
| 68 | PUT | `nodebalancers/{nodeBalancerId}/firewalls` | `put-node-balancer-firewalls` | Update a NodeBalancer's firewalls |
| 69 | PUT | `object-storage/buckets/{regionId}/{bucket}/access` | `put-storage-bucket-access` | Update access to an Object Storage bucket |
