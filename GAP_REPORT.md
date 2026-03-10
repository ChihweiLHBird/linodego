# Linode API to linodego SDK Gap Report

## Report Metadata

- **Generated**: 2026-03-10 16:40:21 UTC
- **OpenAPI Spec Version**: 4.219.1
- **Analysis Type**: Static Code Analysis
- **SDK Repository**: linodego

## Purpose

This report provides a comprehensive static analysis comparing the Linode API v4 
(as documented in the OpenAPI specification) against the linodego Go SDK implementation.

The analysis covers two levels:
1. **Endpoint Coverage**: Which API endpoints are implemented vs missing in the SDK
2. **Parameter Coverage**: For implemented endpoints, which parameters (body fields, headers, path params, query params) are documented but not implemented, or vice versa

## Executive Summary

- **Total API Endpoints**: 465
- **Implemented in SDK**: 78 (16.8%)
- **Missing from SDK**: 387
  - *Of which deprecated*: 10

## Endpoint Coverage Analysis

This section lists every endpoint from the Linode API and its implementation status in the linodego SDK.

### Access keys

**Coverage**: 0/5 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/object-storage/keys/{keyId}` | Revoke an Object Storage access key |
| ❌ Missing | GET | `/{apiVersion}/object-storage/keys` | List Object Storage access keys |
| ❌ Missing | GET | `/{apiVersion}/object-storage/keys/{keyId}` | Get an Object Storage access key |
| ❌ Missing | POST | `/{apiVersion}/object-storage/keys` | Create an Object Storage access key |
| ❌ Missing | PUT | `/{apiVersion}/object-storage/keys/{keyId}` | Update an Object Storage access key |

### Account

**Coverage**: 2/3 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/account` | Get your account |
| ❌ Missing | POST | `/{apiVersion}/account/cancel` | Delete your account |
| ✅ Implemented | PUT | `/{apiVersion}/account` | Update your account |

### Account agreements

**Coverage**: 0/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/account/agreements` | List agreements |
| ❌ Missing | POST | `/{apiVersion}/account/agreements` | Acknowledge agreements |

### Account availability

**Coverage**: 1/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/account/availability` | List available services |
| ❌ Missing | GET | `/{apiVersion}/account/availability/{regionId}` | Get available services for a region |

### Account settings

**Coverage**: 0/3 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/account/settings` | Get account settings |
| ❌ Missing | POST | `/{apiVersion}/account/settings/managed-enable` | Enable Linode Managed |
| ❌ Missing | PUT | `/{apiVersion}/account/settings` | Update account settings |

### Account transfer

**Coverage**: 0/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/account/transfer` | Get network usage |

### Advanced parameters

**Coverage**: 0/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/databases/mysql/config` | List MySQL Managed Database advanced parameters |
| ❌ Missing | GET | `/{apiVersion}/databases/postgresql/config` | List PostgreSQL Managed Database advanced parameters |

### Alerts

**Coverage**: 0/7 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/monitor/services/{serviceType}/alert-definitions/{alertId}` | Delete an alert definition |
| ❌ Missing | GET | `/{apiVersion}/monitor/alert-channels` | List alert channels |
| ❌ Missing | GET | `/{apiVersion}/monitor/alert-definitions` | List alert definitions |
| ❌ Missing | GET | `/{apiVersion}/monitor/services/{serviceType}/alert-definitions` | List alert definitions for a service type |
| ❌ Missing | GET | `/{apiVersion}/monitor/services/{serviceType}/alert-definitions/{alertId}` | Get an alert definition |
| ❌ Missing | POST | `/{apiVersion}/monitor/services/{serviceType}/alert-definitions` | Create an alert definition |
| ❌ Missing | PUT | `/{apiVersion}/monitor/services/{serviceType}/alert-definitions/{alertId}` | Update an alert definition |

### Attachments

**Coverage**: 0/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | POST | `/{apiVersion}/support/tickets/{ticketId}/attachments` | Create a support ticket attachment |

### Backups

**Coverage**: 0/6 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/linode/instances/{linodeId}/backups` | List backups |
| ❌ Missing | GET | `/{apiVersion}/linode/instances/{linodeId}/backups/{backupId}` | Get a backup |
| ❌ Missing | POST | `/{apiVersion}/linode/instances/{linodeId}/backups` | Create a snapshot |
| ❌ Missing | POST | `/{apiVersion}/linode/instances/{linodeId}/backups/cancel` | Cancel backups |
| ❌ Missing | POST | `/{apiVersion}/linode/instances/{linodeId}/backups/enable` | Enable backups |
| ❌ Missing | POST | `/{apiVersion}/linode/instances/{linodeId}/backups/{backupId}/restore` | Restore a backup |

### Beta programs

**Coverage**: 2/5 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/account/betas` | List enrolled Beta programs |
| ❌ Missing | GET | `/{apiVersion}/account/betas/{betaId}` | Get an enrolled Beta program |
| ✅ Implemented | GET | `/{apiVersion}/betas` | List Beta programs |
| ✅ Implemented | GET | `/{apiVersion}/betas/{betaId}` | Get a Beta program |
| ❌ Missing | POST | `/{apiVersion}/account/betas` | Enroll in a Beta program |

### Buckets

**Coverage**: 0/12 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/object-storage/buckets/{regionId}/{bucket}` | Remove an Object Storage bucket |
| ❌ Missing | GET | `/{apiVersion}/object-storage/buckets` | List Object Storage buckets |
| ❌ Missing | GET | `/{apiVersion}/object-storage/buckets/{regionId}` | List Object Storage buckets per region |
| ❌ Missing | GET | `/{apiVersion}/object-storage/buckets/{regionId}/{bucket}` | Get an Object Storage bucket |
| ❌ Missing | GET | `/{apiVersion}/object-storage/buckets/{regionId}/{bucket}/access` | Get Object Storage bucket access |
| ❌ Missing | GET | `/{apiVersion}/object-storage/buckets/{regionId}/{bucket}/object-acl` | Get an Object Storage object ACL configuration |
| ❌ Missing | GET | `/{apiVersion}/object-storage/buckets/{regionId}/{bucket}/object-list` | List Object Storage bucket contents |
| ❌ Missing | POST | `/{apiVersion}/object-storage/buckets` | Create an Object Storage bucket |
| ❌ Missing | POST | `/{apiVersion}/object-storage/buckets/{regionId}/{bucket}/access` | Allow access to an Object Storage bucket |
| ❌ Missing | POST | `/{apiVersion}/object-storage/buckets/{regionId}/{bucket}/object-url` | Create a URL for an object |
| ❌ Missing | PUT | `/{apiVersion}/object-storage/buckets/{regionId}/{bucket}/access` | Update access to an Object Storage bucket |
| ❌ Missing | PUT | `/{apiVersion}/object-storage/buckets/{regionId}/{bucket}/object-acl` | Update an object's ACL configuration |

### Child accounts

**Coverage**: 0/3 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/account/child-accounts` | List child accounts |
| ❌ Missing | GET | `/{apiVersion}/account/child-accounts/{euuId}` | Get a child account |
| ❌ Missing | POST | `/{apiVersion}/account/child-accounts/{euuId}/token` | Create a proxy user token |

### Cluster dashboard

**Coverage**: 0/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/lke/clusters/{clusterId}/dashboard` | Get a Kubernetes cluster dashboard URL |

### Clusters

**Coverage**: 0/9 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/lke/clusters/{clusterId}` | Delete a Kubernetes cluster |
| ❌ Missing | GET | `/{apiVersion}/lke/clusters` | List Kubernetes clusters |
| ❌ Missing | GET | `/{apiVersion}/lke/clusters/{clusterId}` | Get a Kubernetes cluster |
| ⚠️ Missing (Deprecated) | GET | `/{apiVersion}/object-storage/clusters` | List clusters |
| ⚠️ Missing (Deprecated) | GET | `/{apiVersion}/object-storage/clusters/{clusterId}` | Get a cluster |
| ❌ Missing | POST | `/{apiVersion}/lke/clusters` | Create a Kubernetes cluster |
| ❌ Missing | POST | `/{apiVersion}/lke/clusters/{clusterId}/recycle` | Recycle cluster nodes |
| ❌ Missing | POST | `/{apiVersion}/lke/clusters/{clusterId}/regenerate` | Regenerate a Kubernetes cluster |
| ❌ Missing | PUT | `/{apiVersion}/lke/clusters/{clusterId}` | Update a Kubernetes cluster |

### Configuration profile interfaces

**Coverage**: 0/6 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/linode/instances/{linodeId}/configs/{configId}/interfaces/{interfaceId}` | Delete a configuration profile interface |
| ❌ Missing | GET | `/{apiVersion}/linode/instances/{linodeId}/configs/{configId}/interfaces` | List configuration profile interfaces |
| ❌ Missing | GET | `/{apiVersion}/linode/instances/{linodeId}/configs/{configId}/interfaces/{interfaceId}` | Get a configuration profile interface |
| ❌ Missing | POST | `/{apiVersion}/linode/instances/{linodeId}/configs/{configId}/interfaces` | Add a configuration profile interface |
| ❌ Missing | POST | `/{apiVersion}/linode/instances/{linodeId}/configs/{configId}/interfaces/order` | Reorder configuration profile interfaces |
| ❌ Missing | PUT | `/{apiVersion}/linode/instances/{linodeId}/configs/{configId}/interfaces/{interfaceId}` | Update a configuration profile interface |

### Configuration profiles

**Coverage**: 0/5 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/linode/instances/{linodeId}/configs/{configId}` | Delete a configuration profile |
| ❌ Missing | GET | `/{apiVersion}/linode/instances/{linodeId}/configs` | List configuration profiles |
| ❌ Missing | GET | `/{apiVersion}/linode/instances/{linodeId}/configs/{configId}` | Get a configuration profile |
| ❌ Missing | POST | `/{apiVersion}/linode/instances/{linodeId}/configs` | Create a configuration profile |
| ❌ Missing | PUT | `/{apiVersion}/linode/instances/{linodeId}/configs/{configId}` | Update a configuration profile |

### Configurations

**Coverage**: 6/6 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId}` | Delete a config |
| ✅ Implemented | GET | `/{apiVersion}/nodebalancers/{nodeBalancerId}/configs` | List configs |
| ✅ Implemented | GET | `/{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId}` | Get a config |
| ✅ Implemented | POST | `/{apiVersion}/nodebalancers/{nodeBalancerId}/configs` | Create a config |
| ✅ Implemented | POST | `/{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId}/rebuild` | Rebuild a config |
| ✅ Implemented | PUT | `/{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId}` | Update a config |

### Control Plane ACL

**Coverage**: 0/3 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/lke/clusters/{clusterId}/control_plane_acl` | Delete the control plane access control list |
| ❌ Missing | GET | `/{apiVersion}/lke/clusters/{clusterId}/control_plane_acl` | Get the control plane access control list |
| ❌ Missing | PUT | `/{apiVersion}/lke/clusters/{clusterId}/control_plane_acl` | Update the control plane access control list |

### Credentials

**Coverage**: 0/4 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/databases/mysql/instances/{instanceId}/credentials` | Get MySQL Managed Database credentials |
| ❌ Missing | GET | `/{apiVersion}/databases/postgresql/instances/{instanceId}/credentials` | Get PostgreSQL Managed Database credentials |
| ❌ Missing | POST | `/{apiVersion}/databases/mysql/instances/{instanceId}/credentials/reset` | Reset MySQL Managed Database credentials |
| ❌ Missing | POST | `/{apiVersion}/databases/postgresql/instances/{instanceId}/credentials/reset` | Reset PostgreSQL Managed Database credentials |

### Databases

**Coverage**: 0/17 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/databases/mysql/instances/{instanceId}` | Delete a MySQL Managed Database |
| ❌ Missing | DELETE | `/{apiVersion}/databases/postgresql/instances/{instanceId}` | Delete a PostgreSQL Managed Database |
| ❌ Missing | GET | `/{apiVersion}/databases/instances` | List Managed Databases |
| ❌ Missing | GET | `/{apiVersion}/databases/mysql/instances` | List MySQL Managed Databases |
| ❌ Missing | GET | `/{apiVersion}/databases/mysql/instances/{instanceId}` | Get a MySQL Managed Database |
| ❌ Missing | GET | `/{apiVersion}/databases/postgresql/instances` | List PostgreSQL Managed Databases |
| ❌ Missing | GET | `/{apiVersion}/databases/postgresql/instances/{instanceId}` | Get a PostgreSQL Managed Database |
| ❌ Missing | POST | `/{apiVersion}/databases/mysql/instances` | Create or restore a MySQL Managed Database |
| ❌ Missing | POST | `/{apiVersion}/databases/mysql/instances/{instanceId}/patch` | Patch a MySQL Managed Database |
| ❌ Missing | POST | `/{apiVersion}/databases/mysql/instances/{instanceId}/resume` | Resume a MySQL Managed Database |
| ❌ Missing | POST | `/{apiVersion}/databases/mysql/instances/{instanceId}/suspend` | Suspend a MySQL Managed Database |
| ❌ Missing | POST | `/{apiVersion}/databases/postgresql/instances` | Create or restore a PostgreSQL Managed Database |
| ❌ Missing | POST | `/{apiVersion}/databases/postgresql/instances/{instanceId}/patch` | Patch a PostgreSQL Managed Database |
| ❌ Missing | POST | `/{apiVersion}/databases/postgresql/instances/{instanceId}/resume` | Resume a PostgreSQL Managed Database |
| ❌ Missing | POST | `/{apiVersion}/databases/postgresql/instances/{instanceId}/suspend` | Suspend a PostgreSQL Managed Database |
| ❌ Missing | PUT | `/{apiVersion}/databases/mysql/instances/{instanceId}` | Update a MySQL Managed Database |
| ❌ Missing | PUT | `/{apiVersion}/databases/postgresql/instances/{instanceId}` | Update a PostgreSQL Managed Database |

### Devices

**Coverage**: 0/4 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/networking/firewalls/{firewallId}/devices/{deviceId}` | Delete a firewall device |
| ❌ Missing | GET | `/{apiVersion}/networking/firewalls/{firewallId}/devices` | List firewall devices |
| ❌ Missing | GET | `/{apiVersion}/networking/firewalls/{firewallId}/devices/{deviceId}` | Get a firewall device |
| ❌ Missing | POST | `/{apiVersion}/networking/firewalls/{firewallId}/devices` | Create a firewall device |

### Disks

**Coverage**: 0/8 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/linode/instances/{linodeId}/disks/{diskId}` | Delete a disk |
| ❌ Missing | GET | `/{apiVersion}/linode/instances/{linodeId}/disks` | List disks |
| ❌ Missing | GET | `/{apiVersion}/linode/instances/{linodeId}/disks/{diskId}` | Get a disk |
| ❌ Missing | POST | `/{apiVersion}/linode/instances/{linodeId}/disks` | Create a disk |
| ❌ Missing | POST | `/{apiVersion}/linode/instances/{linodeId}/disks/{diskId}/clone` | Clone a disk |
| ❌ Missing | POST | `/{apiVersion}/linode/instances/{linodeId}/disks/{diskId}/password` | Reset a disk root password |
| ❌ Missing | POST | `/{apiVersion}/linode/instances/{linodeId}/disks/{diskId}/resize` | Resize a disk |
| ❌ Missing | PUT | `/{apiVersion}/linode/instances/{linodeId}/disks/{diskId}` | Update a disk |

### Domain zone file

**Coverage**: 1/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/domains/{domainId}/zone-file` | Get a domain zone file |

### Domains

**Coverage**: 6/7 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/domains/{domainId}` | Delete a domain |
| ✅ Implemented | GET | `/{apiVersion}/domains` | List domains |
| ✅ Implemented | GET | `/{apiVersion}/domains/{domainId}` | Get a domain |
| ✅ Implemented | POST | `/{apiVersion}/domains` | Create a domain |
| ❌ Missing | POST | `/{apiVersion}/domains/import` | Import a domain |
| ✅ Implemented | POST | `/{apiVersion}/domains/{domainId}/clone` | Clone a domain |
| ✅ Implemented | PUT | `/{apiVersion}/domains/{domainId}` | Update a domain |

### Endpoints

**Coverage**: 0/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/object-storage/endpoints` | List Object Storage endpoints |

### Engines

**Coverage**: 0/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/databases/engines` | List Managed Databases engines |
| ❌ Missing | GET | `/{apiVersion}/databases/engines/{engineId}` | Get a Managed Databases engine |

### Entity transfers

**Coverage**: 0/5 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ⚠️ Missing (Deprecated) | DELETE | `/{apiVersion}/account/entity-transfers/{token}` | Cancel an entity transfer |
| ⚠️ Missing (Deprecated) | GET | `/{apiVersion}/account/entity-transfers` | List entity transfers |
| ⚠️ Missing (Deprecated) | GET | `/{apiVersion}/account/entity-transfers/{token}` | Get an entity transfer |
| ⚠️ Missing (Deprecated) | POST | `/{apiVersion}/account/entity-transfers` | Create an entity transfer |
| ⚠️ Missing (Deprecated) | POST | `/{apiVersion}/account/entity-transfers/{token}/accept` | Accept an entity transfer |

### Events

**Coverage**: 0/3 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/account/events` | List events |
| ❌ Missing | GET | `/{apiVersion}/account/events/{eventId}` | Get an event |
| ❌ Missing | POST | `/{apiVersion}/account/events/{eventId}/seen` | Mark an event as seen |

### Firewall settings

**Coverage**: 0/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/networking/firewalls/settings` | List default firewalls |
| ❌ Missing | PUT | `/{apiVersion}/networking/firewalls/settings` | Update default firewalls |

### Firewalls

**Coverage**: 4/14 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/networking/firewalls/{firewallId}` | Delete a firewall |
| ❌ Missing | GET | `/{apiVersion}/linode/instances/{linodeId}/firewalls` | List a Linode's firewalls |
| ✅ Implemented | GET | `/{apiVersion}/networking/firewalls` | List firewalls |
| ❌ Missing | GET | `/{apiVersion}/networking/firewalls/{firewallId}` | Get a firewall |
| ❌ Missing | GET | `/{apiVersion}/networking/firewalls/{firewallId}/history` | List firewall rule versions |
| ❌ Missing | GET | `/{apiVersion}/networking/firewalls/{firewallId}/history/rules/{version}` | Get a firewall rule version |
| ❌ Missing | GET | `/{apiVersion}/networking/firewalls/{firewallId}/rules` | List firewall rules |
| ✅ Implemented | GET | `/{apiVersion}/nodebalancers/{nodeBalancerId}/firewalls` | List NodeBalancer firewalls |
| ❌ Missing | POST | `/{apiVersion}/linode/instances/{linodeId}/firewalls/apply` | Apply a Linode's firewalls |
| ✅ Implemented | POST | `/{apiVersion}/networking/firewalls` | Create a firewall |
| ❌ Missing | PUT | `/{apiVersion}/linode/instances/{linodeId}/firewalls` | Update a Linode's firewalls |
| ❌ Missing | PUT | `/{apiVersion}/networking/firewalls/{firewallId}` | Update a firewall |
| ❌ Missing | PUT | `/{apiVersion}/networking/firewalls/{firewallId}/rules` | Update firewall rules |
| ✅ Implemented | PUT | `/{apiVersion}/nodebalancers/{nodeBalancerId}/firewalls` | Update a NodeBalancer's firewalls |

### Grants

**Coverage**: 0/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/profile/grants` | List grants |

### IP addresses

**Coverage**: 1/13 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/linode/instances/{linodeId}/ips/{address}` | Delete an IPv4 address |
| ❌ Missing | GET | `/{apiVersion}/linode/instances/{linodeId}/ips` | Get networking information |
| ❌ Missing | GET | `/{apiVersion}/linode/instances/{linodeId}/ips/{address}` | Get a Linode's IP address |
| ❌ Missing | GET | `/{apiVersion}/networking/ips` | List IP addresses |
| ❌ Missing | GET | `/{apiVersion}/networking/ips/{address}` | Get an IP address |
| ❌ Missing | GET | `/{apiVersion}/vpcs/ips` | List VPC IP addresses |
| ✅ Implemented | GET | `/{apiVersion}/vpcs/{vpcId}/ips` | List a VPC's IP addresses |
| ❌ Missing | POST | `/{apiVersion}/linode/instances/{linodeId}/ips` | Allocate an IPv4 address |
| ❌ Missing | POST | `/{apiVersion}/networking/ips` | Allocate an IP address |
| ❌ Missing | POST | `/{apiVersion}/networking/ips/assign` | Assign IP addresses |
| ❌ Missing | POST | `/{apiVersion}/networking/ips/share` | Share IP addresses |
| ❌ Missing | PUT | `/{apiVersion}/linode/instances/{linodeId}/ips/{address}` | Update an IP address's RDNS for a Linode |
| ❌ Missing | PUT | `/{apiVersion}/networking/ips/{address}` | Update an IP address's RDNS |

### IPv4 addresses

**Coverage**: 0/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | POST | `/{apiVersion}/networking/ipv4/assign` | Assign IPv4s to Linodes |
| ❌ Missing | POST | `/{apiVersion}/networking/ipv4/share` | Configure IPv4 sharing |

### IPv6 pools

**Coverage**: 0/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/networking/ipv6/pools` | List IPv6 pools |

### IPv6 ranges

**Coverage**: 0/4 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/networking/ipv6/ranges/{range}` | Delete an IPv6 range |
| ❌ Missing | GET | `/{apiVersion}/networking/ipv6/ranges` | List IPv6 ranges |
| ❌ Missing | GET | `/{apiVersion}/networking/ipv6/ranges/{range}` | Get an IPv6 range |
| ❌ Missing | POST | `/{apiVersion}/networking/ipv6/ranges` | Create an IPv6 range |

### Identity Management

**Coverage**: 1/4 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/entities` | List entities |
| ❌ Missing | GET | `/{apiVersion}/iam/role-permissions` | List available roles |
| ❌ Missing | GET | `/{apiVersion}/iam/users/{username}/role-permissions` | Get a user's access level |
| ❌ Missing | PUT | `/{apiVersion}/iam/users/{username}/role-permissions` | Update a user's access level |

### Image sharing

**Coverage**: 3/22 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/images/sharegroups/tokens/{tokenUuid}` | Delete a token |
| ❌ Missing | DELETE | `/{apiVersion}/images/sharegroups/{sharegroupId}` | Delete a share group |
| ❌ Missing | DELETE | `/{apiVersion}/images/sharegroups/{sharegroupId}/images/{imageId}` | Revoke access to a shared image |
| ❌ Missing | DELETE | `/{apiVersion}/images/sharegroups/{sharegroupId}/members/{tokenUuid}` | Revoke a membership token |
| ✅ Implemented | GET | `/{apiVersion}/images/sharegroups` | List share groups |
| ❌ Missing | GET | `/{apiVersion}/images/sharegroups/tokens` | List a user's tokens |
| ❌ Missing | GET | `/{apiVersion}/images/sharegroups/tokens/{tokenUuid}` | Get a token |
| ❌ Missing | GET | `/{apiVersion}/images/sharegroups/tokens/{tokenUuid}/sharegroup` | Get a token's share group |
| ❌ Missing | GET | `/{apiVersion}/images/sharegroups/tokens/{tokenUuid}/sharegroup/images` | List images by token |
| ❌ Missing | GET | `/{apiVersion}/images/sharegroups/{sharegroupId}` | Get a share group |
| ❌ Missing | GET | `/{apiVersion}/images/sharegroups/{sharegroupId}/images` | List shared images by group |
| ❌ Missing | GET | `/{apiVersion}/images/sharegroups/{sharegroupId}/members` | List members by share group |
| ❌ Missing | GET | `/{apiVersion}/images/sharegroups/{sharegroupId}/members/{tokenUuid}` | Get a membership token |
| ✅ Implemented | GET | `/{apiVersion}/images/{imageId}/sharegroups` | List share groups by image |
| ✅ Implemented | POST | `/{apiVersion}/images/sharegroups` | Create a share group |
| ❌ Missing | POST | `/{apiVersion}/images/sharegroups/tokens` | Create a token |
| ❌ Missing | POST | `/{apiVersion}/images/sharegroups/{sharegroupId}/images` | Add images to a share group |
| ❌ Missing | POST | `/{apiVersion}/images/sharegroups/{sharegroupId}/members` | Add members to a share group |
| ❌ Missing | PUT | `/{apiVersion}/images/sharegroups/tokens/{tokenUuid}` | Update a token |
| ❌ Missing | PUT | `/{apiVersion}/images/sharegroups/{sharegroupId}` | Update a share group |
| ❌ Missing | PUT | `/{apiVersion}/images/sharegroups/{sharegroupId}/images/{imageId}` | Update a shared image |
| ❌ Missing | PUT | `/{apiVersion}/images/sharegroups/{sharegroupId}/members/{tokenUuid}` | Update a membership token |

### Images

**Coverage**: 6/7 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/images/{imageId}` | Delete an image |
| ✅ Implemented | GET | `/{apiVersion}/images` | List images |
| ✅ Implemented | GET | `/{apiVersion}/images/{imageId}` | Get an image |
| ✅ Implemented | POST | `/{apiVersion}/images` | Create an image |
| ❌ Missing | POST | `/{apiVersion}/images/upload` | Upload an image |
| ✅ Implemented | POST | `/{apiVersion}/images/{imageId}/regions` | Replicate an image |
| ✅ Implemented | PUT | `/{apiVersion}/images/{imageId}` | Update an image |

### Invoices

**Coverage**: 0/3 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/account/invoices` | List invoices |
| ❌ Missing | GET | `/{apiVersion}/account/invoices/{invoiceId}` | Get an invoice |
| ❌ Missing | GET | `/{apiVersion}/account/invoices/{invoiceId}/items` | List invoice items |

### Kernels

**Coverage**: 0/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/linode/kernels` | List kernels |
| ❌ Missing | GET | `/{apiVersion}/linode/kernels/{kernelId}` | Get a kernel |

### Kubeconfigs

**Coverage**: 0/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/lke/clusters/{clusterId}/kubeconfig` | Delete a Kubeconfig |
| ❌ Missing | GET | `/{apiVersion}/lke/clusters/{clusterId}/kubeconfig` | Get a Kubeconfig |

### LKE API endpoints

**Coverage**: 0/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/lke/clusters/{clusterId}/api-endpoints` | List Kubernetes API endpoints |

### LKE service tokens

**Coverage**: 0/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/lke/clusters/{clusterId}/servicetoken` | Delete a service token |

### LKE types

**Coverage**: 0/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/lke/types` | List Kubernetes types |

### LKE versions

**Coverage**: 0/4 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/lke/tiers/{tier}/versions` | List LKE Kubernetes versions (any tier) |
| ❌ Missing | GET | `/{apiVersion}/lke/tiers/{tier}/versions/{version}` | Get an LKE Kubernetes version (any tier) |
| ❌ Missing | GET | `/{apiVersion}/lke/versions` | List LKE Kubernetes versions (non-enterprise) |
| ❌ Missing | GET | `/{apiVersion}/lke/versions/{version}` | Get an LKE Kubernetes version (non-enterprise) |

### Linode instances

**Coverage**: 0/15 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/linode/instances/{linodeId}` | Delete a Linode |
| ❌ Missing | GET | `/{apiVersion}/linode/instances` | List Linodes |
| ❌ Missing | GET | `/{apiVersion}/linode/instances/{linodeId}` | Get a Linode |
| ❌ Missing | POST | `/{apiVersion}/linode/instances` | Create a Linode |
| ❌ Missing | POST | `/{apiVersion}/linode/instances/{linodeId}/boot` | Boot a Linode |
| ❌ Missing | POST | `/{apiVersion}/linode/instances/{linodeId}/clone` | Clone a Linode |
| ❌ Missing | POST | `/{apiVersion}/linode/instances/{linodeId}/migrate` | Launch a DC migration/pending host migration |
| ❌ Missing | POST | `/{apiVersion}/linode/instances/{linodeId}/mutate` | Upgrade a Linode |
| ❌ Missing | POST | `/{apiVersion}/linode/instances/{linodeId}/password` | Reset a Linode's root password |
| ❌ Missing | POST | `/{apiVersion}/linode/instances/{linodeId}/reboot` | Reboot a Linode |
| ❌ Missing | POST | `/{apiVersion}/linode/instances/{linodeId}/rebuild` | Rebuild a Linode |
| ❌ Missing | POST | `/{apiVersion}/linode/instances/{linodeId}/rescue` | Boot a Linode into rescue mode |
| ❌ Missing | POST | `/{apiVersion}/linode/instances/{linodeId}/resize` | Resize a Linode |
| ❌ Missing | POST | `/{apiVersion}/linode/instances/{linodeId}/shutdown` | Shut down a Linode |
| ❌ Missing | PUT | `/{apiVersion}/linode/instances/{linodeId}` | Update a Linode |

### Linode interfaces

**Coverage**: 0/10 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/linode/instances/{linodeId}/interfaces/{interfaceId}` | Delete a Linode interface |
| ❌ Missing | GET | `/{apiVersion}/linode/instances/{linodeId}/interfaces` | List Linode interfaces |
| ❌ Missing | GET | `/{apiVersion}/linode/instances/{linodeId}/interfaces/history` | List a Linode's network interface history |
| ❌ Missing | GET | `/{apiVersion}/linode/instances/{linodeId}/interfaces/settings` | List Linode interface settings |
| ❌ Missing | GET | `/{apiVersion}/linode/instances/{linodeId}/interfaces/{interfaceId}` | Get a Linode interface |
| ❌ Missing | GET | `/{apiVersion}/linode/instances/{linodeId}/interfaces/{interfaceId}/firewalls` | List Linode interface firewalls |
| ❌ Missing | POST | `/{apiVersion}/linode/instances/{linodeId}/interfaces` | Add a Linode interface |
| ❌ Missing | POST | `/{apiVersion}/linode/instances/{linodeId}/upgrade-interfaces` | Upgrade to Linode interfaces |
| ❌ Missing | PUT | `/{apiVersion}/linode/instances/{linodeId}/interfaces/settings` | Update Linode interface settings |
| ❌ Missing | PUT | `/{apiVersion}/linode/instances/{linodeId}/interfaces/{interfaceId}` | Update a Linode interface |

### Linode types

**Coverage**: 0/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/linode/types` | List types |
| ❌ Missing | GET | `/{apiVersion}/linode/types/{typeId}` | Get a type |

### Logins

**Coverage**: 0/4 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/account/logins` | List user logins |
| ❌ Missing | GET | `/{apiVersion}/account/logins/{loginId}` | Get an account login |
| ❌ Missing | GET | `/{apiVersion}/profile/logins` | List logins |
| ❌ Missing | GET | `/{apiVersion}/profile/logins/{loginId}` | Get a profile's login |

### Logs

**Coverage**: 0/12 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/monitor/streams/destinations/{destinationId}` | Delete a destination |
| ❌ Missing | DELETE | `/{apiVersion}/monitor/streams/{streamId}` | Delete a stream |
| ❌ Missing | GET | `/{apiVersion}/monitor/streams` | List streams |
| ❌ Missing | GET | `/{apiVersion}/monitor/streams/destinations` | List destinations |
| ❌ Missing | GET | `/{apiVersion}/monitor/streams/destinations/{destinationId}` | Get a destination |
| ❌ Missing | GET | `/{apiVersion}/monitor/streams/destinations/{destinationId}/history` | Get a destination's history |
| ❌ Missing | GET | `/{apiVersion}/monitor/streams/{streamId}` | Get a stream |
| ❌ Missing | GET | `/{apiVersion}/monitor/streams/{streamId}/history` | Get a stream's history |
| ❌ Missing | POST | `/{apiVersion}/monitor/streams` | Create a stream |
| ❌ Missing | POST | `/{apiVersion}/monitor/streams/destinations` | Create a destination |
| ❌ Missing | PUT | `/{apiVersion}/monitor/streams/destinations/{destinationId}` | Update a destination |
| ❌ Missing | PUT | `/{apiVersion}/monitor/streams/{streamId}` | Update a stream |

### Longview clients

**Coverage**: 0/5 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/longview/clients/{clientId}` | Delete a Longview client |
| ❌ Missing | GET | `/{apiVersion}/longview/clients` | List Longview clients |
| ❌ Missing | GET | `/{apiVersion}/longview/clients/{clientId}` | Get a Longview client |
| ❌ Missing | POST | `/{apiVersion}/longview/clients` | Create a Longview client |
| ❌ Missing | PUT | `/{apiVersion}/longview/clients/{clientId}` | Update a Longview client |

### Longview plans

**Coverage**: 0/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/longview/plan` | Get a Longview plan |
| ❌ Missing | PUT | `/{apiVersion}/longview/plan` | Update a Longview plan |

### Longview subscriptions

**Coverage**: 0/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/longview/subscriptions` | List Longview subscriptions |
| ❌ Missing | GET | `/{apiVersion}/longview/subscriptions/{subscriptionId}` | Get a Longview subscription |

### Longview types

**Coverage**: 0/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/longview/types` | List Longview types |

### Maintenance policies

**Coverage**: 0/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/maintenance/policies` | List maintenance policies |

### Maintenances

**Coverage**: 0/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/account/maintenance` | List maintenances |

### Managed Linode settings

**Coverage**: 0/3 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/managed/linode-settings` | List managed Linode settings |
| ❌ Missing | GET | `/{apiVersion}/managed/linode-settings/{linodeId}` | Get a Linode's managed settings |
| ❌ Missing | PUT | `/{apiVersion}/managed/linode-settings/{linodeId}` | Update a Linode's managed settings |

### Managed SSH keys

**Coverage**: 0/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/managed/credentials/sshkey` | Get a managed SSH key |

### Managed contacts

**Coverage**: 0/5 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/managed/contacts/{contactId}` | Delete a managed contact |
| ❌ Missing | GET | `/{apiVersion}/managed/contacts` | List managed contacts |
| ❌ Missing | GET | `/{apiVersion}/managed/contacts/{contactId}` | Get a managed contact |
| ❌ Missing | POST | `/{apiVersion}/managed/contacts` | Create a managed contact |
| ❌ Missing | PUT | `/{apiVersion}/managed/contacts/{contactId}` | Update a managed contact |

### Managed credentials

**Coverage**: 0/6 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/managed/credentials` | List managed credentials |
| ❌ Missing | GET | `/{apiVersion}/managed/credentials/{credentialId}` | Get a managed credential |
| ❌ Missing | POST | `/{apiVersion}/managed/credentials` | Create a managed credential |
| ❌ Missing | POST | `/{apiVersion}/managed/credentials/{credentialId}/revoke` | Delete a managed credential |
| ❌ Missing | POST | `/{apiVersion}/managed/credentials/{credentialId}/update` | Update a managed credential's username and password |
| ❌ Missing | PUT | `/{apiVersion}/managed/credentials/{credentialId}` | Update a managed credential |

### Managed issues

**Coverage**: 0/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/managed/issues` | List managed issues |
| ❌ Missing | GET | `/{apiVersion}/managed/issues/{issueId}` | Get a managed issue |

### Managed service monitors

**Coverage**: 0/7 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/managed/services/{serviceId}` | Delete a managed service monitor |
| ❌ Missing | GET | `/{apiVersion}/managed/services` | List managed services |
| ❌ Missing | GET | `/{apiVersion}/managed/services/{serviceId}` | Get a managed service monitor |
| ❌ Missing | POST | `/{apiVersion}/managed/services` | Create a managed service |
| ❌ Missing | POST | `/{apiVersion}/managed/services/{serviceId}/disable` | Disable a managed service monitor |
| ❌ Missing | POST | `/{apiVersion}/managed/services/{serviceId}/enable` | Enable a managed service monitor |
| ❌ Missing | PUT | `/{apiVersion}/managed/services/{serviceId}` | Update a managed service monitor |

### Managed statistics

**Coverage**: 1/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/managed/stats` | List managed stats |

### Metrics

**Coverage**: 0/8 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/monitor/dashboards` | List dashboards |
| ❌ Missing | GET | `/{apiVersion}/monitor/dashboards/{dashboardId}` | Get a dashboard |
| ❌ Missing | GET | `/{apiVersion}/monitor/services` | List supported service types |
| ❌ Missing | GET | `/{apiVersion}/monitor/services/{serviceType}` | Get details for a supported service type |
| ❌ Missing | GET | `/{apiVersion}/monitor/services/{serviceType}/dashboards` | List dashboards for a service type |
| ❌ Missing | GET | `/{apiVersion}/monitor/services/{serviceType}/metric-definitions` | List metrics for a service type |
| ❌ Missing | POST | `/{apiVersion}/monitor/services/{serviceType}/metrics` | Get an entity's metrics |
| ❌ Missing | POST | `/{apiVersion}/monitor/services/{serviceType}/token` | Create a token for a service type |

### Network transfer prices

**Coverage**: 0/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/network-transfer/prices` | List network transfer prices |

### Node pools

**Coverage**: 0/6 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/lke/clusters/{clusterId}/pools/{poolId}` | Delete a node pool |
| ❌ Missing | GET | `/{apiVersion}/lke/clusters/{clusterId}/pools` | List node pools |
| ❌ Missing | GET | `/{apiVersion}/lke/clusters/{clusterId}/pools/{poolId}` | Get a node pool |
| ❌ Missing | POST | `/{apiVersion}/lke/clusters/{clusterId}/pools` | Create a node pool |
| ❌ Missing | POST | `/{apiVersion}/lke/clusters/{clusterId}/pools/{poolId}/recycle` | Recycle a node pool |
| ❌ Missing | PUT | `/{apiVersion}/lke/clusters/{clusterId}/pools/{poolId}` | Update a node pool |

### NodeBalancer types

**Coverage**: 0/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/nodebalancers/types` | List NodeBalancer types |

### NodeBalancers

**Coverage**: 5/6 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/nodebalancers/{nodeBalancerId}` | Delete a NodeBalancer |
| ❌ Missing | GET | `/{apiVersion}/linode/instances/{linodeId}/nodebalancers` | List Linode NodeBalancers |
| ✅ Implemented | GET | `/{apiVersion}/nodebalancers` | List NodeBalancers |
| ✅ Implemented | GET | `/{apiVersion}/nodebalancers/{nodeBalancerId}` | Get a NodeBalancer |
| ✅ Implemented | POST | `/{apiVersion}/nodebalancers` | Create a NodeBalancer |
| ✅ Implemented | PUT | `/{apiVersion}/nodebalancers/{nodeBalancerId}` | Update a NodeBalancer |

### Nodes

**Coverage**: 2/8 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/lke/clusters/{clusterId}/nodes/{nodeId}` | Delete a node |
| ❌ Missing | DELETE | `/{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId}/nodes/{nodeId}` | Delete a NodeBalancer's node |
| ❌ Missing | GET | `/{apiVersion}/lke/clusters/{clusterId}/nodes/{nodeId}` | Get a node |
| ✅ Implemented | GET | `/{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId}/nodes` | List nodes |
| ❌ Missing | GET | `/{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId}/nodes/{nodeId}` | Get a NodeBalancer's node |
| ❌ Missing | POST | `/{apiVersion}/lke/clusters/{clusterId}/nodes/{nodeId}/recycle` | Recycle a node |
| ✅ Implemented | POST | `/{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId}/nodes` | Create a node |
| ❌ Missing | PUT | `/{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId}/nodes/{nodeId}` | Update a node |

### Notifications

**Coverage**: 0/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/account/notifications` | List notifications |

### OAuth apps

**Coverage**: 0/3 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/profile/apps/{appId}` | Revoke app access |
| ❌ Missing | GET | `/{apiVersion}/profile/apps` | List authorized apps |
| ❌ Missing | GET | `/{apiVersion}/profile/apps/{appId}` | Get an authorized app |

### OAuth client

**Coverage**: 0/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/account/oauth-clients/{clientId}/thumbnail` | Get the OAuth client's thumbnail |
| ❌ Missing | PUT | `/{apiVersion}/account/oauth-clients/{clientId}/thumbnail` | Update the OAuth client's thumbnail |

### OAuth clients

**Coverage**: 0/6 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/account/oauth-clients/{clientId}` | Delete an OAuth client |
| ❌ Missing | GET | `/{apiVersion}/account/oauth-clients` | List OAuth clients |
| ❌ Missing | GET | `/{apiVersion}/account/oauth-clients/{clientId}` | Get an OAuth client |
| ❌ Missing | POST | `/{apiVersion}/account/oauth-clients` | Create an OAuth client |
| ❌ Missing | POST | `/{apiVersion}/account/oauth-clients/{clientId}/reset-secret` | Reset an OAuth client secret |
| ❌ Missing | PUT | `/{apiVersion}/account/oauth-clients/{clientId}` | Update an OAuth client |

### OAuth preferences

**Coverage**: 0/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/profile/preferences` | Get user preferences |
| ❌ Missing | PUT | `/{apiVersion}/profile/preferences` | Update a user's preferences |

### Object Storage

**Coverage**: 0/6 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/object-storage/quotas` | List Object Storage quotas |
| ❌ Missing | GET | `/{apiVersion}/object-storage/quotas/{objQuotaId}` | Get an Object Storage quota |
| ❌ Missing | GET | `/{apiVersion}/object-storage/quotas/{objQuotaId}/usage` | Get Object Storage quota usage data |
| ❌ Missing | GET | `/{apiVersion}/object-storage/transfer` | Get Object Storage transfer data |
| ❌ Missing | GET | `/{apiVersion}/object-storage/types` | List Object Storage types |
| ❌ Missing | POST | `/{apiVersion}/object-storage/cancel` | Cancel Object Storage |

### Payment methods

**Coverage**: 0/5 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/account/payment-methods/{paymentMethodId}` | Delete a payment method |
| ❌ Missing | GET | `/{apiVersion}/account/payment-methods` | List payment methods |
| ❌ Missing | GET | `/{apiVersion}/account/payment-methods/{paymentMethodId}` | Get a payment method |
| ❌ Missing | POST | `/{apiVersion}/account/payment-methods` | Add a payment method |
| ❌ Missing | POST | `/{apiVersion}/account/payment-methods/{paymentMethodId}/make-default` | Set a default payment method |

### Payments

**Coverage**: 0/6 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/account/payments` | List payments |
| ❌ Missing | GET | `/{apiVersion}/account/payments/{paymentId}` | Get a payment |
| ⚠️ Missing (Deprecated) | POST | `/{apiVersion}/account/credit-card` | Add or edit a credit card |
| ❌ Missing | POST | `/{apiVersion}/account/payments` | Make a payment |
| ⚠️ Missing (Deprecated) | POST | `/{apiVersion}/account/payments/paypal` | Stage a PayPal payment |
| ⚠️ Missing (Deprecated) | POST | `/{apiVersion}/account/payments/paypal/execute` | Execute a PayPal payment |

### Personal access tokens

**Coverage**: 0/5 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/profile/tokens/{tokenId}` | Revoke a personal access token |
| ❌ Missing | GET | `/{apiVersion}/profile/tokens` | List personal access tokens |
| ❌ Missing | GET | `/{apiVersion}/profile/tokens/{tokenId}` | Get a personal access token |
| ❌ Missing | POST | `/{apiVersion}/profile/tokens` | Create a personal access token |
| ❌ Missing | PUT | `/{apiVersion}/profile/tokens/{tokenId}` | Update a personal access token |

### Phone number

**Coverage**: 0/3 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/profile/phone-number` | Delete a phone number |
| ❌ Missing | POST | `/{apiVersion}/profile/phone-number` | Send a phone number verification code |
| ❌ Missing | POST | `/{apiVersion}/profile/phone-number/verify` | Verify a phone number |

### Placement groups

**Coverage**: 0/7 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/placement/groups/{groupId}` | Delete a placement group |
| ❌ Missing | GET | `/{apiVersion}/placement/groups` | List placement groups |
| ❌ Missing | GET | `/{apiVersion}/placement/groups/{groupId}` | Get a placement group |
| ❌ Missing | POST | `/{apiVersion}/placement/groups` | Create a placement group |
| ❌ Missing | POST | `/{apiVersion}/placement/groups/{groupId}/assign` | Assign a placement group |
| ❌ Missing | POST | `/{apiVersion}/placement/groups/{groupId}/unassign` | Unassign a placement group |
| ❌ Missing | PUT | `/{apiVersion}/placement/groups/{groupId}` | Update a placement group |

### Profile

**Coverage**: 2/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/profile` | Get a profile |
| ✅ Implemented | PUT | `/{apiVersion}/profile` | Update a profile |

### Promo credits

**Coverage**: 0/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | POST | `/{apiVersion}/account/promo-codes` | Add a promo credit |

### Records

**Coverage**: 5/5 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/domains/{domainId}/records/{recordId}` | Delete a domain record |
| ✅ Implemented | GET | `/{apiVersion}/domains/{domainId}/records` | List domain records |
| ✅ Implemented | GET | `/{apiVersion}/domains/{domainId}/records/{recordId}` | Get a domain record |
| ✅ Implemented | POST | `/{apiVersion}/domains/{domainId}/records` | Create a domain record |
| ✅ Implemented | PUT | `/{apiVersion}/domains/{domainId}/records/{recordId}` | Update a domain record |

### Regions

**Coverage**: 4/4 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/regions` | List regions |
| ✅ Implemented | GET | `/{apiVersion}/regions/availability` | List regions' availability |
| ✅ Implemented | GET | `/{apiVersion}/regions/{regionId}` | Get a region |
| ✅ Implemented | GET | `/{apiVersion}/regions/{regionId}/availability` | Get a region's availability |

### Replies

**Coverage**: 0/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/support/tickets/{ticketId}/replies` | List replies |
| ❌ Missing | POST | `/{apiVersion}/support/tickets/{ticketId}/replies` | Create a reply |

### SSH keys

**Coverage**: 0/5 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/profile/sshkeys/{sshKeyId}` | Delete an SSH key |
| ❌ Missing | GET | `/{apiVersion}/profile/sshkeys` | List SSH keys |
| ❌ Missing | GET | `/{apiVersion}/profile/sshkeys/{sshKeyId}` | Get an SSH key |
| ❌ Missing | POST | `/{apiVersion}/profile/sshkeys` | Add an SSH key |
| ❌ Missing | PUT | `/{apiVersion}/profile/sshkeys/{sshKeyId}` | Update an SSH key |

### SSL certificates

**Coverage**: 0/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/databases/mysql/instances/{instanceId}/ssl` | Get a MySQL Managed Database SSL certificate |
| ❌ Missing | GET | `/{apiVersion}/databases/postgresql/instances/{instanceId}/ssl` | Get a PostgreSQL Managed Database SSL certificate |

### Security questions

**Coverage**: 0/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/profile/security-questions` | List security questions |
| ❌ Missing | POST | `/{apiVersion}/profile/security-questions` | Answer security questions |

### Service transfers

**Coverage**: 0/5 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/account/service-transfers/{token}` | Cancel a service transfer |
| ❌ Missing | GET | `/{apiVersion}/account/service-transfers` | List service transfers |
| ❌ Missing | GET | `/{apiVersion}/account/service-transfers/{token}` | Get a service transfer request |
| ❌ Missing | POST | `/{apiVersion}/account/service-transfers` | Request a service transfer |
| ❌ Missing | POST | `/{apiVersion}/account/service-transfers/{token}/accept` | Accept a service transfer |

### StackScripts

**Coverage**: 0/5 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/linode/stackscripts/{stackscriptId}` | Delete a StackScript |
| ❌ Missing | GET | `/{apiVersion}/linode/stackscripts` | List StackScripts |
| ❌ Missing | GET | `/{apiVersion}/linode/stackscripts/{stackscriptId}` | Get a StackScript |
| ❌ Missing | POST | `/{apiVersion}/linode/stackscripts` | Create a StackScript |
| ❌ Missing | PUT | `/{apiVersion}/linode/stackscripts/{stackscriptId}` | Update a StackScript |

### Statistics

**Coverage**: 1/5 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/linode/instances/{linodeId}/stats` | Get daily Linode statistics |
| ❌ Missing | GET | `/{apiVersion}/linode/instances/{linodeId}/stats/{year}/{month}` | Get a month's Linode statistics |
| ❌ Missing | GET | `/{apiVersion}/linode/instances/{linodeId}/transfer` | Get this month's network transfer stats |
| ❌ Missing | GET | `/{apiVersion}/linode/instances/{linodeId}/transfer/{year}/{month}` | Get monthly network transfer stats |
| ✅ Implemented | GET | `/{apiVersion}/nodebalancers/{nodeBalancerId}/stats` | Get NodeBalancer statistics |

### Support tickets

**Coverage**: 0/4 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/support/tickets` | List support tickets |
| ❌ Missing | GET | `/{apiVersion}/support/tickets/{ticketId}` | Get a support ticket |
| ❌ Missing | POST | `/{apiVersion}/support/tickets` | Open a support ticket |
| ❌ Missing | POST | `/{apiVersion}/support/tickets/{ticketId}/close` | Close a support ticket |

### TLS/SSL certificates

**Coverage**: 0/3 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/object-storage/buckets/{regionId}/{bucket}/ssl` | Delete an Object Storage TLS/SSL certificate |
| ❌ Missing | GET | `/{apiVersion}/object-storage/buckets/{regionId}/{bucket}/ssl` | Get an Object Storage TLS/SSL certificate |
| ❌ Missing | POST | `/{apiVersion}/object-storage/buckets/{regionId}/{bucket}/ssl` | Upload an Object Storage TLS/SSL certificate |

### Tags

**Coverage**: 4/4 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/tags/{tagLabel}` | Delete a tag |
| ✅ Implemented | GET | `/{apiVersion}/tags` | List tags |
| ✅ Implemented | GET | `/{apiVersion}/tags/{tagLabel}` | List tagged objects |
| ✅ Implemented | POST | `/{apiVersion}/tags` | Create a tag |

### Templates

**Coverage**: 0/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/networking/firewalls/templates` | List firewall templates |
| ❌ Missing | GET | `/{apiVersion}/networking/firewalls/templates/{slug}` | Get a firewall template |

### Trusted devices

**Coverage**: 0/3 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/profile/devices/{deviceId}` | Revoke a trusted device |
| ❌ Missing | GET | `/{apiVersion}/profile/devices` | List trusted devices |
| ❌ Missing | GET | `/{apiVersion}/profile/devices/{deviceId}` | Get a trusted device |

### Two-factor authentication

**Coverage**: 0/3 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | POST | `/{apiVersion}/profile/tfa-disable` | Disable two-factor authentication |
| ❌ Missing | POST | `/{apiVersion}/profile/tfa-enable` | Generate a secret key for two-factor authentication |
| ❌ Missing | POST | `/{apiVersion}/profile/tfa-enable-confirm` | Enable two-factor authentication |

### Types

**Coverage**: 0/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/databases/types` | List Managed Databases types |
| ❌ Missing | GET | `/{apiVersion}/databases/types/{typeId}` | Get a Managed Databases type |

### Users

**Coverage**: 0/7 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/account/users/{username}` | Delete a user |
| ❌ Missing | GET | `/{apiVersion}/account/users` | List users |
| ❌ Missing | GET | `/{apiVersion}/account/users/{username}` | Get a user |
| ❌ Missing | GET | `/{apiVersion}/account/users/{username}/grants` | List a user's grants |
| ❌ Missing | POST | `/{apiVersion}/account/users` | Create a user |
| ❌ Missing | PUT | `/{apiVersion}/account/users/{username}` | Update a user |
| ❌ Missing | PUT | `/{apiVersion}/account/users/{username}/grants` | Update a user's grants |

### VLANs

**Coverage**: 0/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/networking/vlans/{regionId}/{label}` | Delete a VLAN |
| ❌ Missing | GET | `/{apiVersion}/networking/vlans` | List VLANs |

### VPC subnets

**Coverage**: 5/5 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/vpcs/{vpcId}/subnets/{vpcSubnetId}` | Delete a VPC subnet |
| ✅ Implemented | GET | `/{apiVersion}/vpcs/{vpcId}/subnets` | List VPC subnets |
| ✅ Implemented | GET | `/{apiVersion}/vpcs/{vpcId}/subnets/{vpcSubnetId}` | Get a VPC subnet |
| ✅ Implemented | POST | `/{apiVersion}/vpcs/{vpcId}/subnets` | Create a VPC subnet |
| ✅ Implemented | PUT | `/{apiVersion}/vpcs/{vpcId}/subnets/{vpcSubnetId}` | Update a VPC subnet |

### VPCs

**Coverage**: 7/7 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/vpcs/{vpcId}` | Delete a VPC |
| ✅ Implemented | GET | `/{apiVersion}/nodebalancers/{nodeBalancerId}/vpcs` | List VPC configurations |
| ✅ Implemented | GET | `/{apiVersion}/nodebalancers/{nodeBalancerId}/vpcs/{nodeBalancerVpcConfigId}` | Get a VPC configuration |
| ✅ Implemented | GET | `/{apiVersion}/vpcs` | List VPCs |
| ✅ Implemented | GET | `/{apiVersion}/vpcs/{vpcId}` | Get a VPC |
| ✅ Implemented | POST | `/{apiVersion}/vpcs` | Create a VPC |
| ✅ Implemented | PUT | `/{apiVersion}/vpcs/{vpcId}` | Update a VPC |

### Volume types

**Coverage**: 0/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/volumes/types` | List volume types |

### Volumes

**Coverage**: 9/10 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/volumes/{volumeId}` | Delete a volume |
| ❌ Missing | GET | `/{apiVersion}/linode/instances/{linodeId}/volumes` | List a Linode's volumes |
| ✅ Implemented | GET | `/{apiVersion}/volumes` | List volumes |
| ✅ Implemented | GET | `/{apiVersion}/volumes/{volumeId}` | Get a volume |
| ✅ Implemented | POST | `/{apiVersion}/volumes` | Create a volume |
| ✅ Implemented | POST | `/{apiVersion}/volumes/{volumeId}/attach` | Attach a volume |
| ✅ Implemented | POST | `/{apiVersion}/volumes/{volumeId}/clone` | Clone a volume |
| ✅ Implemented | POST | `/{apiVersion}/volumes/{volumeId}/detach` | Detach a volume |
| ✅ Implemented | POST | `/{apiVersion}/volumes/{volumeId}/resize` | Resize a volume |
| ✅ Implemented | PUT | `/{apiVersion}/volumes/{volumeId}` | Update a volume |

## Parameter Coverage Analysis

This section analyzes parameter coverage for endpoints that ARE implemented in the SDK.
For each implemented endpoint, it identifies:
- Parameters documented in the API but not found in SDK structs
- Parameters in SDK structs but not documented in the API

### Methodology

This analysis compares:
1. Parameters defined in the OpenAPI spec (path params, query params, headers, body fields)
2. JSON-tagged fields in Go struct definitions found in the SDK

**Note**: This is a heuristic analysis. The tool attempts to match API endpoints with SDK structs
based on naming patterns. Manual review is recommended to validate findings.

### Detailed Findings

#### DELETE /{apiVersion}/domains/{domainId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `domainId` (Required, type: `integer`)

#### DELETE /{apiVersion}/domains/{domainId}/records/{recordId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `domainId` (Required, type: `integer`)
- `recordId` (Required, type: `integer`)

#### DELETE /{apiVersion}/images/{imageId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `imageId` (Required, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `capabilities`
- `created_by`
- `deprecated`
- `description`
- `id`
- `image_sharing`
- `images`
- `images_count`
- `is_public`
- `is_shared`
- `is_suspended`
- `label`
- `members_count`
- `regions`
- `shared_by`
- `shared_with`
- `sharegroup_count`
- `sharegroup_id`
- `sharegroup_label`
- `sharegroup_list_url`
- `sharegroup_uuid`
- `size`
- `source_image_id`
- `status`
- `tags`
- `token`
- `token_uuid`
- `total_size`
- `type`
- `uuid`
- `valid_for_sharegroup_uuid`
- `vendor`

*Related structs analyzed*: ImageSharing, ImageSharingSharedWith, ImageSharingSharedBy, ImageShareEntry, ProducerImageShareGroup, ImageShareGroupCreateOptions, ImageShareGroupUpdateOptions, ImageShareGroupAddImagesOptions, ImageShareGroupUpdateImageOptions, ImageShareGroupImage, ImageShareGroupMember, ImageShareGroupUpdateMemberOptions, ImageShareGroupAddMemberOptions, ConsumerImageShareGroup, ImageShareGroupToken, ImageShareGroupCreateTokenResponse, ImageShareGroupCreateTokenOptions, ImageShareGroupUpdateTokenOptions

#### DELETE /{apiVersion}/nodebalancers/{nodeBalancerId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `nodeBalancerId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `connections`
- `data`
- `id`
- `ipv4_range`
- `ipv6_ranges`
- `range`
- `title`
- `traffic`

*Related structs analyzed*: VPCSubnetNodebalancersRanges, VPCSubnetNodebalancers, NodeBalancerStats, NodeBalancerStatsData

#### DELETE /{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `configId` (Required, type: `integer`)
- `nodeBalancerId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `connections`
- `data`
- `id`
- `ipv4_range`
- `ipv6_ranges`
- `range`
- `title`
- `traffic`

*Related structs analyzed*: VPCSubnetNodebalancersRanges, VPCSubnetNodebalancers, NodeBalancerStats, NodeBalancerStatsData

#### DELETE /{apiVersion}/tags/{tagLabel}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `tagLabel` (Required, type: `string`)

#### DELETE /{apiVersion}/volumes/{volumeId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `volumeId` (Required, type: `integer`)

#### DELETE /{apiVersion}/vpcs/{vpcId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `vpcId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `active`
- `config_id`
- `databases`
- `id`
- `interfaces`
- `ipv4`
- `ipv4_range`
- `ipv6`
- `ipv6_ranges`
- `label`
- `linodes`
- `nodebalancers`
- `range`

*Related structs analyzed*: VPCSubnetLinodeInterface, VPCSubnetLinode, VPCSubnetDatabase, VPCSubnetNodebalancersRanges, VPCSubnetNodebalancers, VPCSubnet, VPCSubnetCreateOptions, VPCSubnetCreateOptionsIPv6, VPCSubnetUpdateOptions

#### DELETE /{apiVersion}/vpcs/{vpcId}/subnets/{vpcSubnetId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `vpcId` (Required, type: `integer`)
- `vpcSubnetId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `active`
- `config_id`
- `databases`
- `id`
- `interfaces`
- `ipv4`
- `ipv4_range`
- `ipv6`
- `ipv6_ranges`
- `label`
- `linodes`
- `nodebalancers`
- `range`

*Related structs analyzed*: VPCSubnetLinodeInterface, VPCSubnetLinode, VPCSubnetDatabase, VPCSubnetNodebalancersRanges, VPCSubnetNodebalancers, VPCSubnet, VPCSubnetCreateOptions, VPCSubnetCreateOptionsIPv6, VPCSubnetUpdateOptions

#### GET /{apiVersion}/account

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)

**Extra in SDK** (found in SDK but not documented in API):

- `account_access`
- `active_promotions`
- `active_since`
- `address_1`
- `address_2`
- `available`
- `backups_enabled`
- `balance`
- `balance_uninvoiced`
- `billable`
- `billing_source`
- `capabilities`
- `city`
- `company`
- `country`
- `credit_card`
- `description`
- `email`
- `entities`
- `entity`
- `entity_access`
- `eu_model`
- `euuid`
- `first_name`
- `id`
- `interfaces_for_new_linodes`
- `is_sender`
- `label`
- `last_name`
- `linodes`
- `longview_subscription`
- `maintenance_policy`
- `maintenance_policy_set`
- `managed`
- `master_service_agreement`
- `network_helper`
- `object_storage`
- `phone`
- `privacy_policy`
- `quota`
- `reason`
- `region`
- `region_transfers`
- `roles`
- `source`
- `state`
- `status`
- `tax_id`
- `token`
- `type`
- `unavailable`
- `used`
- `when`
- `zip`

*Related structs analyzed*: AccountMaintenance, AccountSettings, AccountSettingsUpdateOptions, AccountServiceTransfer, AccountServiceTransferEntity, AccountServiceTransferRequestOptions, Account, AccountUpdateOptions, AccountAgreements, AccountAgreementsUpdateOptions, AccountRolePermissions, AccountAccess, AccountTransfer, AccountTransferRegion, AccountAvailability, AccountBetaProgram, AccountBetaProgramCreateOpts

#### GET /{apiVersion}/account/availability

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `account_access`
- `active_promotions`
- `active_since`
- `address_1`
- `address_2`
- `available`
- `available_ipv6_prefix_lengths`
- `backups_enabled`
- `balance`
- `balance_uninvoiced`
- `billable`
- `billing_source`
- `capabilities`
- `city`
- `company`
- `country`
- `credit_card`
- `description`
- `email`
- `entities`
- `entity`
- `entity_access`
- `eu_model`
- `euuid`
- `first_name`
- `id`
- `interfaces_for_new_linodes`
- `is_sender`
- `label`
- `last_name`
- `linodes`
- `longview_subscription`
- `maintenance_policy`
- `maintenance_policy_set`
- `managed`
- `master_service_agreement`
- `network_helper`
- `object_storage`
- `phone`
- `plan`
- `privacy_policy`
- `quota`
- `reason`
- `region`
- `region_transfers`
- `roles`
- `source`
- `state`
- `status`
- `tax_id`
- `token`
- `type`
- `unavailable`
- `used`
- `when`
- `zip`

*Related structs analyzed*: AccountMaintenance, AccountSettings, AccountSettingsUpdateOptions, AccountServiceTransfer, AccountServiceTransferEntity, AccountServiceTransferRequestOptions, Account, AccountUpdateOptions, AccountAgreements, AccountAgreementsUpdateOptions, AccountRolePermissions, AccountAccess, AccountTransfer, AccountTransferRegion, RegionAvailability, RegionVPCAvailability, AccountAvailability, AccountBetaProgram, AccountBetaProgramCreateOpts

#### GET /{apiVersion}/betas

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

#### GET /{apiVersion}/betas/{betaId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `betaId` (Required, type: `string`)

#### GET /{apiVersion}/domains

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

#### GET /{apiVersion}/domains/{domainId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `domainId` (Required, type: `integer`)

#### GET /{apiVersion}/domains/{domainId}/records

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `domainId` (Required, type: `integer`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

#### GET /{apiVersion}/domains/{domainId}/records/{recordId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `domainId` (Required, type: `integer`)
- `recordId` (Required, type: `integer`)

#### GET /{apiVersion}/domains/{domainId}/zone-file

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `domainId` (Required, type: `string`)

#### GET /{apiVersion}/entities

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4...]`)

#### GET /{apiVersion}/images

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `capabilities`
- `created_by`
- `deprecated`
- `description`
- `id`
- `image_sharing`
- `images`
- `images_count`
- `is_public`
- `is_shared`
- `is_suspended`
- `label`
- `members_count`
- `regions`
- `shared_by`
- `shared_with`
- `sharegroup_count`
- `sharegroup_id`
- `sharegroup_label`
- `sharegroup_list_url`
- `sharegroup_uuid`
- `size`
- `source_image_id`
- `status`
- `tags`
- `token`
- `token_uuid`
- `total_size`
- `type`
- `uuid`
- `valid_for_sharegroup_uuid`
- `vendor`

*Related structs analyzed*: ImageSharing, ImageSharingSharedWith, ImageSharingSharedBy, ImageShareEntry, ProducerImageShareGroup, ImageShareGroupCreateOptions, ImageShareGroupUpdateOptions, ImageShareGroupAddImagesOptions, ImageShareGroupUpdateImageOptions, ImageShareGroupImage, ImageShareGroupMember, ImageShareGroupUpdateMemberOptions, ImageShareGroupAddMemberOptions, ConsumerImageShareGroup, ImageShareGroupToken, ImageShareGroupCreateTokenResponse, ImageShareGroupCreateTokenOptions, ImageShareGroupUpdateTokenOptions

#### GET /{apiVersion}/images/sharegroups

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `capabilities`
- `created_by`
- `deprecated`
- `description`
- `id`
- `image_sharing`
- `images`
- `images_count`
- `is_public`
- `is_shared`
- `is_suspended`
- `label`
- `members_count`
- `regions`
- `shared_by`
- `shared_with`
- `sharegroup_count`
- `sharegroup_id`
- `sharegroup_label`
- `sharegroup_list_url`
- `sharegroup_uuid`
- `size`
- `source_image_id`
- `status`
- `tags`
- `token`
- `token_uuid`
- `total_size`
- `type`
- `uuid`
- `valid_for_sharegroup_uuid`
- `vendor`

*Related structs analyzed*: ImageSharing, ImageSharingSharedWith, ImageSharingSharedBy, ImageShareEntry, ProducerImageShareGroup, ImageShareGroupCreateOptions, ImageShareGroupUpdateOptions, ImageShareGroupAddImagesOptions, ImageShareGroupUpdateImageOptions, ImageShareGroupImage, ImageShareGroupMember, ImageShareGroupUpdateMemberOptions, ImageShareGroupAddMemberOptions, ConsumerImageShareGroup, ImageShareGroupToken, ImageShareGroupCreateTokenResponse, ImageShareGroupCreateTokenOptions, ImageShareGroupUpdateTokenOptions

#### GET /{apiVersion}/images/{imageId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `imageId` (Required, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `capabilities`
- `created_by`
- `deprecated`
- `description`
- `id`
- `image_sharing`
- `images`
- `images_count`
- `is_public`
- `is_shared`
- `is_suspended`
- `label`
- `members_count`
- `regions`
- `shared_by`
- `shared_with`
- `sharegroup_count`
- `sharegroup_id`
- `sharegroup_label`
- `sharegroup_list_url`
- `sharegroup_uuid`
- `size`
- `source_image_id`
- `status`
- `tags`
- `token`
- `token_uuid`
- `total_size`
- `type`
- `uuid`
- `valid_for_sharegroup_uuid`
- `vendor`

*Related structs analyzed*: ImageSharing, ImageSharingSharedWith, ImageSharingSharedBy, ImageShareEntry, ProducerImageShareGroup, ImageShareGroupCreateOptions, ImageShareGroupUpdateOptions, ImageShareGroupAddImagesOptions, ImageShareGroupUpdateImageOptions, ImageShareGroupImage, ImageShareGroupMember, ImageShareGroupUpdateMemberOptions, ImageShareGroupAddMemberOptions, ConsumerImageShareGroup, ImageShareGroupToken, ImageShareGroupCreateTokenResponse, ImageShareGroupCreateTokenOptions, ImageShareGroupUpdateTokenOptions

#### GET /{apiVersion}/images/{imageId}/sharegroups

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `imageId` (Required, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `capabilities`
- `created_by`
- `deprecated`
- `description`
- `id`
- `image_sharing`
- `images`
- `images_count`
- `is_public`
- `is_shared`
- `is_suspended`
- `label`
- `members_count`
- `regions`
- `shared_by`
- `shared_with`
- `sharegroup_count`
- `sharegroup_id`
- `sharegroup_label`
- `sharegroup_list_url`
- `sharegroup_uuid`
- `size`
- `source_image_id`
- `status`
- `tags`
- `token`
- `token_uuid`
- `total_size`
- `type`
- `uuid`
- `valid_for_sharegroup_uuid`
- `vendor`

*Related structs analyzed*: ImageSharing, ImageSharingSharedWith, ImageSharingSharedBy, ImageShareEntry, ProducerImageShareGroup, ImageShareGroupCreateOptions, ImageShareGroupUpdateOptions, ImageShareGroupAddImagesOptions, ImageShareGroupUpdateImageOptions, ImageShareGroupImage, ImageShareGroupMember, ImageShareGroupUpdateMemberOptions, ImageShareGroupAddMemberOptions, ConsumerImageShareGroup, ImageShareGroupToken, ImageShareGroupCreateTokenResponse, ImageShareGroupCreateTokenOptions, ImageShareGroupUpdateTokenOptions

#### GET /{apiVersion}/managed/stats

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)

**Extra in SDK** (found in SDK but not documented in API):

- `bytes_in`
- `bytes_out`
- `bytes_total`
- `connections`
- `cpu`
- `data`
- `description`
- `enum`
- `example`
- `executionTimeMsec`
- `in`
- `io`
- `maximum`
- `minimum`
- `netv4`
- `netv6`
- `out`
- `private_in`
- `private_out`
- `requires_restart`
- `seriesFetched`
- `swap`
- `title`
- `traffic`
- `type`

*Related structs analyzed*: StatsNet, StatsIO, InstanceStatsData, InstanceStats, InformationSchemaStatsExpiry, NodeBalancerStats, NodeBalancerStatsData, StatsTraffic, PGStatStatementsTrack, MonthlyInstanceTransferStats, MonthlyInstanceTransferStatsV2, EntityMetricsStats

#### GET /{apiVersion}/networking/firewalls

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `default_firewall_ids`

*Related structs analyzed*: FirewallSettings, FirewallSettingsUpdateOptions

#### GET /{apiVersion}/nodebalancers

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `connections`
- `data`
- `id`
- `ipv4_range`
- `ipv6_ranges`
- `range`
- `title`
- `traffic`

*Related structs analyzed*: VPCSubnetNodebalancersRanges, VPCSubnetNodebalancers, NodeBalancerStats, NodeBalancerStatsData

#### GET /{apiVersion}/nodebalancers/{nodeBalancerId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `nodeBalancerId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `connections`
- `data`
- `id`
- `ipv4_range`
- `ipv6_ranges`
- `range`
- `title`
- `traffic`

*Related structs analyzed*: VPCSubnetNodebalancersRanges, VPCSubnetNodebalancers, NodeBalancerStats, NodeBalancerStatsData

#### GET /{apiVersion}/nodebalancers/{nodeBalancerId}/configs

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `nodeBalancerId` (Required, type: `integer`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `connections`
- `data`
- `id`
- `ipv4_range`
- `ipv6_ranges`
- `range`
- `title`
- `traffic`

*Related structs analyzed*: VPCSubnetNodebalancersRanges, VPCSubnetNodebalancers, NodeBalancerStats, NodeBalancerStatsData

#### GET /{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `configId` (Required, type: `integer`)
- `nodeBalancerId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `connections`
- `data`
- `id`
- `ipv4_range`
- `ipv6_ranges`
- `range`
- `title`
- `traffic`

*Related structs analyzed*: VPCSubnetNodebalancersRanges, VPCSubnetNodebalancers, NodeBalancerStats, NodeBalancerStatsData

#### GET /{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId}/nodes

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `configId` (Required, type: `integer`)
- `nodeBalancerId` (Required, type: `integer`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `assignments`
- `connections`
- `data`
- `down`
- `id`
- `ipv4_range`
- `ipv6_ranges`
- `range`
- `region`
- `title`
- `traffic`
- `up`

*Related structs analyzed*: VPCSubnetNodebalancersRanges, VPCSubnetNodebalancers, NodeBalancerStats, NodeBalancerStatsData, NodeBalancerNodeStatus, LinodesAssignIPsOptions

#### GET /{apiVersion}/nodebalancers/{nodeBalancerId}/firewalls

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `nodeBalancerId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `connections`
- `data`
- `default_firewall_ids`
- `id`
- `ipv4_range`
- `ipv6_ranges`
- `range`
- `title`
- `traffic`

*Related structs analyzed*: VPCSubnetNodebalancersRanges, VPCSubnetNodebalancers, NodeBalancerStats, NodeBalancerStatsData, FirewallSettings, FirewallSettingsUpdateOptions

#### GET /{apiVersion}/nodebalancers/{nodeBalancerId}/stats

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `nodeBalancerId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `bytes_in`
- `bytes_out`
- `bytes_total`
- `connections`
- `cpu`
- `data`
- `description`
- `enum`
- `example`
- `executionTimeMsec`
- `id`
- `in`
- `io`
- `ipv4_range`
- `ipv6_ranges`
- `maximum`
- `minimum`
- `netv4`
- `netv6`
- `out`
- `private_in`
- `private_out`
- `range`
- `requires_restart`
- `seriesFetched`
- `swap`
- `title`
- `traffic`
- `type`

*Related structs analyzed*: StatsNet, StatsIO, InstanceStatsData, InstanceStats, InformationSchemaStatsExpiry, VPCSubnetNodebalancersRanges, VPCSubnetNodebalancers, NodeBalancerStats, NodeBalancerStatsData, StatsTraffic, PGStatStatementsTrack, MonthlyInstanceTransferStats, MonthlyInstanceTransferStatsV2, EntityMetricsStats

#### GET /{apiVersion}/nodebalancers/{nodeBalancerId}/vpcs

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `nodeBalancerId` (Required, type: `integer`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `active`
- `config_id`
- `connections`
- `data`
- `databases`
- `id`
- `interfaces`
- `ipv4`
- `ipv4_range`
- `ipv6`
- `ipv6_ranges`
- `label`
- `linodes`
- `nodebalancers`
- `range`
- `title`
- `traffic`

*Related structs analyzed*: VPCSubnetLinodeInterface, VPCSubnetLinode, VPCSubnetDatabase, VPCSubnetNodebalancersRanges, VPCSubnetNodebalancers, VPCSubnet, VPCSubnetCreateOptions, VPCSubnetCreateOptionsIPv6, VPCSubnetUpdateOptions, NodeBalancerStats, NodeBalancerStatsData

#### GET /{apiVersion}/nodebalancers/{nodeBalancerId}/vpcs/{nodeBalancerVpcConfigId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `nodeBalancerId` (Required, type: `integer`)
- `nodeBalancerVpcConfigId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `active`
- `config_id`
- `connections`
- `data`
- `databases`
- `id`
- `interfaces`
- `ipv4`
- `ipv4_range`
- `ipv6`
- `ipv6_ranges`
- `label`
- `linodes`
- `nodebalancers`
- `range`
- `title`
- `traffic`

*Related structs analyzed*: VPCSubnetLinodeInterface, VPCSubnetLinode, VPCSubnetDatabase, VPCSubnetNodebalancersRanges, VPCSubnetNodebalancers, VPCSubnet, VPCSubnetCreateOptions, VPCSubnetCreateOptionsIPv6, VPCSubnetUpdateOptions, NodeBalancerStats, NodeBalancerStatsData

#### GET /{apiVersion}/profile

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)

**Extra in SDK** (found in SDK but not documented in API):

- `authentication_type`
- `authorized_keys`
- `code`
- `completed`
- `credit`
- `datetime`
- `email`
- `email_notifications`
- `id`
- `ip`
- `ip_whitelist_enabled`
- `label`
- `last_remote_addr`
- `lish_auth_method`
- `pending`
- `referrals`
- `restricted`
- `scopes`
- `status`
- `thumbnail_url`
- `timezone`
- `total`
- `two_factor_auth`
- `uid`
- `url`
- `user_agent`
- `username`
- `verified_phone_number`
- `website`

*Related structs analyzed*: ProfileReferrals, Profile, ProfileUpdateOptions, ProfileLogin, ProfileDevice, ProfileApp

#### GET /{apiVersion}/regions

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)

#### GET /{apiVersion}/regions/availability

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)

**Extra in SDK** (found in SDK but not documented in API):

- `available`
- `available_ipv6_prefix_lengths`
- `plan`
- `region`
- `unavailable`

*Related structs analyzed*: RegionAvailability, RegionVPCAvailability, AccountAvailability

#### GET /{apiVersion}/regions/{regionId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `regionId` (Required, type: `string`)

#### GET /{apiVersion}/regions/{regionId}/availability

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `regionId` (Required, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `available`
- `available_ipv6_prefix_lengths`
- `plan`
- `region`
- `unavailable`

*Related structs analyzed*: RegionAvailability, RegionVPCAvailability, AccountAvailability

#### GET /{apiVersion}/tags

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

#### GET /{apiVersion}/tags/{tagLabel}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)
- `tagLabel` (Required, type: `string`)

#### GET /{apiVersion}/volumes

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

#### GET /{apiVersion}/volumes/{volumeId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)
- `volumeId` (Required, type: `integer`)

#### GET /{apiVersion}/vpcs

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `active`
- `config_id`
- `databases`
- `id`
- `interfaces`
- `ipv4`
- `ipv4_range`
- `ipv6`
- `ipv6_ranges`
- `label`
- `linodes`
- `nodebalancers`
- `range`

*Related structs analyzed*: VPCSubnetLinodeInterface, VPCSubnetLinode, VPCSubnetDatabase, VPCSubnetNodebalancersRanges, VPCSubnetNodebalancers, VPCSubnet, VPCSubnetCreateOptions, VPCSubnetCreateOptionsIPv6, VPCSubnetUpdateOptions

#### GET /{apiVersion}/vpcs/{vpcId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `vpcId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `active`
- `config_id`
- `databases`
- `id`
- `interfaces`
- `ipv4`
- `ipv4_range`
- `ipv6`
- `ipv6_ranges`
- `label`
- `linodes`
- `nodebalancers`
- `range`

*Related structs analyzed*: VPCSubnetLinodeInterface, VPCSubnetLinode, VPCSubnetDatabase, VPCSubnetNodebalancersRanges, VPCSubnetNodebalancers, VPCSubnet, VPCSubnetCreateOptions, VPCSubnetCreateOptionsIPv6, VPCSubnetUpdateOptions

#### GET /{apiVersion}/vpcs/{vpcId}/ips

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)
- `vpcId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `active`
- `assignments`
- `config_id`
- `databases`
- `id`
- `interfaces`
- `ipv4`
- `ipv4_range`
- `ipv6`
- `ipv6_ranges`
- `label`
- `linodes`
- `nodebalancers`
- `range`
- `region`

*Related structs analyzed*: VPCSubnetLinodeInterface, VPCSubnetLinode, VPCSubnetDatabase, VPCSubnetNodebalancersRanges, VPCSubnetNodebalancers, VPCSubnet, VPCSubnetCreateOptions, VPCSubnetCreateOptionsIPv6, VPCSubnetUpdateOptions, LinodesAssignIPsOptions

#### GET /{apiVersion}/vpcs/{vpcId}/subnets

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)
- `vpcId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `active`
- `config_id`
- `databases`
- `id`
- `interfaces`
- `ipv4`
- `ipv4_range`
- `ipv6`
- `ipv6_ranges`
- `label`
- `linodes`
- `nodebalancers`
- `range`

*Related structs analyzed*: VPCSubnetLinodeInterface, VPCSubnetLinode, VPCSubnetDatabase, VPCSubnetNodebalancersRanges, VPCSubnetNodebalancers, VPCSubnet, VPCSubnetCreateOptions, VPCSubnetCreateOptionsIPv6, VPCSubnetUpdateOptions

#### GET /{apiVersion}/vpcs/{vpcId}/subnets/{vpcSubnetId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `vpcId` (Required, type: `integer`)
- `vpcSubnetId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `active`
- `config_id`
- `databases`
- `id`
- `interfaces`
- `ipv4`
- `ipv4_range`
- `ipv6`
- `ipv6_ranges`
- `label`
- `linodes`
- `nodebalancers`
- `range`

*Related structs analyzed*: VPCSubnetLinodeInterface, VPCSubnetLinode, VPCSubnetDatabase, VPCSubnetNodebalancersRanges, VPCSubnetNodebalancers, VPCSubnet, VPCSubnetCreateOptions, VPCSubnetCreateOptionsIPv6, VPCSubnetUpdateOptions

#### POST /{apiVersion}/domains

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)

#### POST /{apiVersion}/domains/{domainId}/clone

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `domainId` (Required, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `backups_enabled`
- `configs`
- `disks`
- `group`
- `label`
- `linode_id`
- `metadata`
- `placement_group`
- `private_ip`
- `region`
- `type`

*Related structs analyzed*: InstanceCloneOptions, DomainCloneOptions

#### POST /{apiVersion}/domains/{domainId}/records

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `domainId` (Required, type: `integer`)

#### POST /{apiVersion}/images

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `cloud_init` (Optional, type: `boolean`)
- `disk_id` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `capabilities`
- `created_by`
- `deprecated`
- `id`
- `image_sharing`
- `images`
- `images_count`
- `is_public`
- `is_shared`
- `is_suspended`
- `members_count`
- `regions`
- `shared_by`
- `shared_with`
- `sharegroup_count`
- `sharegroup_id`
- `sharegroup_label`
- `sharegroup_list_url`
- `sharegroup_uuid`
- `size`
- `source_image_id`
- `status`
- `token`
- `token_uuid`
- `total_size`
- `type`
- `uuid`
- `valid_for_sharegroup_uuid`
- `vendor`

*Related structs analyzed*: ImageSharing, ImageSharingSharedWith, ImageSharingSharedBy, ImageShareEntry, ProducerImageShareGroup, ImageShareGroupCreateOptions, ImageShareGroupUpdateOptions, ImageShareGroupAddImagesOptions, ImageShareGroupUpdateImageOptions, ImageShareGroupImage, ImageShareGroupMember, ImageShareGroupUpdateMemberOptions, ImageShareGroupAddMemberOptions, ConsumerImageShareGroup, ImageShareGroupToken, ImageShareGroupCreateTokenResponse, ImageShareGroupCreateTokenOptions, ImageShareGroupUpdateTokenOptions

#### POST /{apiVersion}/images/sharegroups

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)

**Extra in SDK** (found in SDK but not documented in API):

- `capabilities`
- `created_by`
- `deprecated`
- `id`
- `image_sharing`
- `images_count`
- `is_public`
- `is_shared`
- `is_suspended`
- `members_count`
- `regions`
- `shared_by`
- `shared_with`
- `sharegroup_count`
- `sharegroup_id`
- `sharegroup_label`
- `sharegroup_list_url`
- `sharegroup_uuid`
- `size`
- `source_image_id`
- `status`
- `tags`
- `token`
- `token_uuid`
- `total_size`
- `type`
- `uuid`
- `valid_for_sharegroup_uuid`
- `vendor`

*Related structs analyzed*: ImageSharing, ImageSharingSharedWith, ImageSharingSharedBy, ImageShareEntry, ProducerImageShareGroup, ImageShareGroupCreateOptions, ImageShareGroupUpdateOptions, ImageShareGroupAddImagesOptions, ImageShareGroupUpdateImageOptions, ImageShareGroupImage, ImageShareGroupMember, ImageShareGroupUpdateMemberOptions, ImageShareGroupAddMemberOptions, ConsumerImageShareGroup, ImageShareGroupToken, ImageShareGroupCreateTokenResponse, ImageShareGroupCreateTokenOptions, ImageShareGroupUpdateTokenOptions

#### POST /{apiVersion}/images/{imageId}/regions

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `imageId` (Required, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `capabilities`
- `created_by`
- `deprecated`
- `description`
- `id`
- `image_sharing`
- `images`
- `images_count`
- `is_public`
- `is_shared`
- `is_suspended`
- `label`
- `members_count`
- `shared_by`
- `shared_with`
- `sharegroup_count`
- `sharegroup_id`
- `sharegroup_label`
- `sharegroup_list_url`
- `sharegroup_uuid`
- `size`
- `source_image_id`
- `status`
- `tags`
- `token`
- `token_uuid`
- `total_size`
- `type`
- `uuid`
- `valid_for_sharegroup_uuid`
- `vendor`

*Related structs analyzed*: ImageSharing, ImageSharingSharedWith, ImageSharingSharedBy, ImageShareEntry, ProducerImageShareGroup, ImageShareGroupCreateOptions, ImageShareGroupUpdateOptions, ImageShareGroupAddImagesOptions, ImageShareGroupUpdateImageOptions, ImageShareGroupImage, ImageShareGroupMember, ImageShareGroupUpdateMemberOptions, ImageShareGroupAddMemberOptions, ConsumerImageShareGroup, ImageShareGroupToken, ImageShareGroupCreateTokenResponse, ImageShareGroupCreateTokenOptions, ImageShareGroupUpdateTokenOptions

#### POST /{apiVersion}/networking/firewalls

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `devices` (Optional, type: `object`)
- `devices.linode_interfaces` (Optional, type: `array[integer]`)
- `devices.linodes` (Optional, type: `array[integer]`)
- `devices.nodebalancers` (Optional, type: `array[integer]`)
- `rules` (Required, type: `unknown`)

**Extra in SDK** (found in SDK but not documented in API):

- `default_firewall_ids`

*Related structs analyzed*: FirewallSettings, FirewallSettingsUpdateOptions

#### POST /{apiVersion}/nodebalancers

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `client_conn_throttle` (Optional, type: `integer`)
- `configs` (Optional, type: `array[object]`)
- `firewall_id` (Optional, type: `integer`)
- `label` (Optional, type: `string`)
- `region` (Required, type: `string`)
- `tags` (Optional, type: `array[string]`)
- `vpcs` (Optional, type: `array[object]`)

**Extra in SDK** (found in SDK but not documented in API):

- `connections`
- `data`
- `id`
- `ipv4_range`
- `ipv6_ranges`
- `range`
- `title`
- `traffic`

*Related structs analyzed*: VPCSubnetNodebalancersRanges, VPCSubnetNodebalancers, NodeBalancerStats, NodeBalancerStatsData

#### POST /{apiVersion}/nodebalancers/{nodeBalancerId}/configs

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `nodeBalancerId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `connections`
- `data`
- `id`
- `ipv4_range`
- `ipv6_ranges`
- `range`
- `title`
- `traffic`

*Related structs analyzed*: VPCSubnetNodebalancersRanges, VPCSubnetNodebalancers, NodeBalancerStats, NodeBalancerStatsData

#### POST /{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId}/nodes

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `configId` (Required, type: `integer`)
- `nodeBalancerId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `assignments`
- `connections`
- `data`
- `down`
- `id`
- `ipv4_range`
- `ipv6_ranges`
- `range`
- `region`
- `title`
- `traffic`
- `up`

*Related structs analyzed*: VPCSubnetNodebalancersRanges, VPCSubnetNodebalancers, NodeBalancerStats, NodeBalancerStatsData, NodeBalancerNodeStatus, LinodesAssignIPsOptions

#### POST /{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId}/rebuild

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `configId` (Required, type: `integer`)
- `nodeBalancerId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `algorithm`
- `authorized_keys`
- `authorized_users`
- `booted`
- `check`
- `check_attempts`
- `check_body`
- `check_interval`
- `check_passive`
- `check_path`
- `check_timeout`
- `cipher_suite`
- `connections`
- `data`
- `disk_encryption`
- `id`
- `image`
- `ipv4_range`
- `ipv6_ranges`
- `metadata`
- `nodes`
- `port`
- `protocol`
- `proxy_protocol`
- `range`
- `root_pass`
- `ssl_cert`
- `ssl_key`
- `stackscript_data`
- `stackscript_id`
- `stickiness`
- `title`
- `traffic`
- `type`
- `udp_check_port`

*Related structs analyzed*: VPCSubnetNodebalancersRanges, VPCSubnetNodebalancers, NodeBalancerStats, NodeBalancerStatsData, InstanceRebuildOptions, NodeBalancerConfigRebuildOptions, NodeBalancerConfigRebuildNodeOptions

#### POST /{apiVersion}/tags

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `domains` (Optional, type: `array[integer]`)
- `label` (Required, type: `string`)
- `linodes` (Optional, type: `array[integer]`)
- `nodebalancers` (Optional, type: `array[integer]`)
- `volumes` (Optional, type: `array[integer]`)

#### POST /{apiVersion}/volumes

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `config_id` (Optional, type: `integer`)
- `encryption` (Optional, type: `enum[enabled,disabled...]`)
- `label` (Required, type: `string`)
- `linode_id` (Optional, type: `integer`)
- `region` (Optional, type: `string`)
- `size` (Optional, type: `integer`)
- `tags` (Optional, type: `array[string]`)

#### POST /{apiVersion}/volumes/{volumeId}/attach

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `volumeId` (Required, type: `integer`)

*Related structs analyzed*: VolumeAttachOptions

#### POST /{apiVersion}/volumes/{volumeId}/clone

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `volumeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `backups_enabled`
- `configs`
- `disks`
- `domain`
- `group`
- `linode_id`
- `metadata`
- `placement_group`
- `private_ip`
- `region`
- `type`

*Related structs analyzed*: InstanceCloneOptions, DomainCloneOptions

#### POST /{apiVersion}/volumes/{volumeId}/detach

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `volumeId` (Required, type: `integer`)

#### POST /{apiVersion}/volumes/{volumeId}/resize

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `size` (Required, type: `integer`)
- `volumeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `allow_auto_disk_resize`
- `migration_type`
- `type`

*Related structs analyzed*: InstanceResizeOptions

#### POST /{apiVersion}/vpcs

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)

**Extra in SDK** (found in SDK but not documented in API):

- `active`
- `config_id`
- `databases`
- `id`
- `interfaces`
- `ipv4`
- `ipv4_range`
- `ipv6`
- `ipv6_ranges`
- `label`
- `linodes`
- `nodebalancers`
- `range`

*Related structs analyzed*: VPCSubnetLinodeInterface, VPCSubnetLinode, VPCSubnetDatabase, VPCSubnetNodebalancersRanges, VPCSubnetNodebalancers, VPCSubnet, VPCSubnetCreateOptions, VPCSubnetCreateOptionsIPv6, VPCSubnetUpdateOptions

#### POST /{apiVersion}/vpcs/{vpcId}/subnets

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `vpcId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `active`
- `config_id`
- `databases`
- `id`
- `interfaces`
- `ipv4_range`
- `ipv6`
- `ipv6_ranges`
- `linodes`
- `nodebalancers`
- `range`

*Related structs analyzed*: VPCSubnetLinodeInterface, VPCSubnetLinode, VPCSubnetDatabase, VPCSubnetNodebalancersRanges, VPCSubnetNodebalancers, VPCSubnet, VPCSubnetCreateOptions, VPCSubnetCreateOptionsIPv6, VPCSubnetUpdateOptions

#### PUT /{apiVersion}/account

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `credit_card.expiry` (Optional, type: `string`)
- `credit_card.last_four` (Optional, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `account_access`
- `available`
- `backups_enabled`
- `billable`
- `description`
- `entities`
- `entity`
- `entity_access`
- `eu_model`
- `id`
- `interfaces_for_new_linodes`
- `is_sender`
- `label`
- `linodes`
- `longview_subscription`
- `maintenance_policy`
- `maintenance_policy_set`
- `managed`
- `master_service_agreement`
- `network_helper`
- `object_storage`
- `privacy_policy`
- `quota`
- `reason`
- `region`
- `region_transfers`
- `roles`
- `source`
- `status`
- `token`
- `type`
- `unavailable`
- `used`
- `when`

*Related structs analyzed*: AccountMaintenance, AccountSettings, AccountSettingsUpdateOptions, AccountServiceTransfer, AccountServiceTransferEntity, AccountServiceTransferRequestOptions, Account, AccountUpdateOptions, AccountAgreements, AccountAgreementsUpdateOptions, AccountRolePermissions, AccountAccess, AccountTransfer, AccountTransferRegion, AccountAvailability, AccountBetaProgram, AccountBetaProgramCreateOpts

#### PUT /{apiVersion}/domains/{domainId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `axfr_ips` (Optional, type: `array[string]`)
- `description` (Optional, type: `string`)
- `domain` (Optional, type: `string`)
- `domainId` (Required, type: `integer`)
- `expire_sec` (Optional, type: `integer`)
- `group` (Optional, type: `string`)
- `id` (Optional, type: `integer`)
- `master_ips` (Optional, type: `array[string]`)
- `refresh_sec` (Optional, type: `integer`)
- `retry_sec` (Optional, type: `integer`)
- `soa_email` (Optional, type: `string`)
- `status` (Optional, type: `enum[disabled,active...]`)
- `tags` (Optional, type: `array[string]`)
- `ttl_sec` (Optional, type: `integer`)
- `type` (Optional, type: `enum[master,slave...]`)

#### PUT /{apiVersion}/domains/{domainId}/records/{recordId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `domainId` (Required, type: `integer`)
- `name` (Optional, type: `string`)
- `port` (Optional, type: `integer`)
- `priority` (Optional, type: `integer`)
- `protocol` (Optional, type: `string`)
- `recordId` (Required, type: `integer`)
- `service` (Optional, type: `string`)
- `tag` (Optional, type: `enum[issue,issuewild,iodef...]`)
- `target` (Optional, type: `string`)
- `ttl_sec` (Optional, type: `integer`)
- `weight` (Optional, type: `integer`)

#### PUT /{apiVersion}/images/{imageId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `created` (Optional, type: `string`)
- `eol` (Optional, type: `string`)
- `expiry` (Optional, type: `string`)
- `imageId` (Required, type: `string`)
- `updated` (Optional, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `image_sharing`
- `images`
- `images_count`
- `is_suspended`
- `members_count`
- `shared_by`
- `shared_with`
- `sharegroup_count`
- `sharegroup_id`
- `sharegroup_label`
- `sharegroup_list_url`
- `sharegroup_uuid`
- `source_image_id`
- `token`
- `token_uuid`
- `uuid`
- `valid_for_sharegroup_uuid`

*Related structs analyzed*: ImageSharing, ImageSharingSharedWith, ImageSharingSharedBy, ImageShareEntry, ProducerImageShareGroup, ImageShareGroupCreateOptions, ImageShareGroupUpdateOptions, ImageShareGroupAddImagesOptions, ImageShareGroupUpdateImageOptions, ImageShareGroupImage, ImageShareGroupMember, ImageShareGroupUpdateMemberOptions, ImageShareGroupAddMemberOptions, ConsumerImageShareGroup, ImageShareGroupToken, ImageShareGroupCreateTokenResponse, ImageShareGroupCreateTokenOptions, ImageShareGroupUpdateTokenOptions

#### PUT /{apiVersion}/nodebalancers/{nodeBalancerId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `client_conn_throttle` (Optional, type: `integer`)
- `created` (Optional, type: `string`)
- `hostname` (Optional, type: `string`)
- `ipv4` (Optional, type: `string`)
- `ipv6` (Optional, type: `string`)
- `label` (Optional, type: `string`)
- `lke_cluster` (Optional, type: `object`)
- `lke_cluster.id` (Optional, type: `string`)
- `lke_cluster.label` (Optional, type: `string`)
- `lke_cluster.type` (Optional, type: `string`)
- `lke_cluster.url` (Optional, type: `string`)
- `nodeBalancerId` (Required, type: `integer`)
- `region` (Optional, type: `string`)
- `tags` (Optional, type: `array[string]`)
- `transfer` (Optional, type: `object`)
- `transfer.in` (Optional, type: `number`)
- `transfer.out` (Optional, type: `number`)
- `transfer.total` (Optional, type: `number`)
- `type` (Optional, type: `enum[common,premium...]`)
- `updated` (Optional, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `connections`
- `data`
- `ipv4_range`
- `ipv6_ranges`
- `range`
- `title`
- `traffic`

*Related structs analyzed*: VPCSubnetNodebalancersRanges, VPCSubnetNodebalancers, NodeBalancerStats, NodeBalancerStatsData

#### PUT /{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `configId` (Required, type: `integer`)
- `nodeBalancerId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `connections`
- `data`
- `id`
- `ipv4_range`
- `ipv6_ranges`
- `range`
- `title`
- `traffic`

*Related structs analyzed*: VPCSubnetNodebalancersRanges, VPCSubnetNodebalancers, NodeBalancerStats, NodeBalancerStatsData

#### PUT /{apiVersion}/nodebalancers/{nodeBalancerId}/firewalls

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `firewall_ids` (Required, type: `array[integer]`)
- `nodeBalancerId` (Required, type: `integer`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `connections`
- `data`
- `default_firewall_ids`
- `id`
- `ipv4_range`
- `ipv6_ranges`
- `range`
- `title`
- `traffic`

*Related structs analyzed*: VPCSubnetNodebalancersRanges, VPCSubnetNodebalancers, NodeBalancerStats, NodeBalancerStatsData, FirewallSettings, FirewallSettingsUpdateOptions

#### PUT /{apiVersion}/profile

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `referrals.code` (Optional, type: `string`)
- `referrals.completed` (Optional, type: `integer`)
- `referrals.credit` (Optional, type: `integer`)
- `referrals.pending` (Optional, type: `integer`)
- `referrals.total` (Optional, type: `integer`)
- `referrals.url` (Optional, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `code`
- `completed`
- `credit`
- `datetime`
- `id`
- `ip`
- `label`
- `last_remote_addr`
- `pending`
- `scopes`
- `status`
- `thumbnail_url`
- `total`
- `url`
- `user_agent`
- `website`

*Related structs analyzed*: ProfileReferrals, Profile, ProfileUpdateOptions, ProfileLogin, ProfileDevice, ProfileApp

#### PUT /{apiVersion}/volumes/{volumeId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `volumeId` (Required, type: `integer`)

#### PUT /{apiVersion}/vpcs/{vpcId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `description` (Optional, type: `string`)
- `vpcId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `active`
- `config_id`
- `databases`
- `id`
- `interfaces`
- `ipv4`
- `ipv4_range`
- `ipv6`
- `ipv6_ranges`
- `linodes`
- `nodebalancers`
- `range`

*Related structs analyzed*: VPCSubnetLinodeInterface, VPCSubnetLinode, VPCSubnetDatabase, VPCSubnetNodebalancersRanges, VPCSubnetNodebalancers, VPCSubnet, VPCSubnetCreateOptions, VPCSubnetCreateOptionsIPv6, VPCSubnetUpdateOptions

#### PUT /{apiVersion}/vpcs/{vpcId}/subnets/{vpcSubnetId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `vpcId` (Required, type: `integer`)
- `vpcSubnetId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `active`
- `config_id`
- `databases`
- `id`
- `interfaces`
- `ipv4`
- `ipv4_range`
- `ipv6`
- `ipv6_ranges`
- `linodes`
- `nodebalancers`
- `range`

*Related structs analyzed*: VPCSubnetLinodeInterface, VPCSubnetLinode, VPCSubnetDatabase, VPCSubnetNodebalancersRanges, VPCSubnetNodebalancers, VPCSubnet, VPCSubnetCreateOptions, VPCSubnetCreateOptionsIPv6, VPCSubnetUpdateOptions

## Appendix

### SDK Endpoints Detected

The analyzer detected 299 endpoint calls in the linodego SDK.

Sample of detected endpoints:

- `DELETE /profile/phone-number` (in `profile_phone_number.go`)
- `GET /account` (in `account.go`)
- `GET /account/agreements` (in `account_agreements.go`)
- `GET /account/availability` (in `account_availability.go`)
- `GET /account/betas` (in `account_betas.go`)
- `GET /account/child-accounts` (in `account_child.go`)
- `GET /account/events` (in `account_events.go`)
- `GET /account/invoices` (in `account_invoices.go`)
- `GET /account/logins` (in `account_logins.go`)
- `GET /account/maintenance` (in `account_maintenance.go`)
- `GET /account/notifications` (in `account_notifications.go`)
- `GET /account/oauth-clients` (in `account_oauth_client.go`)
- `GET /account/payment-methods` (in `account_payment_methods.go`)
- `GET /account/payments` (in `account_payments.go`)
- `GET /account/service-transfers` (in `account_service_transfer.go`)
- `GET /account/settings` (in `account_settings.go`)
- `GET /account/transfer` (in `account_transfer.go`)
- `GET /account/users` (in `account_users.go`)
- `GET /betas` (in `betas.go`)
- `GET /databases/engines` (in `databases.go`)

### SDK Structs Detected

The analyzer detected 510 struct definitions with JSON tags.
