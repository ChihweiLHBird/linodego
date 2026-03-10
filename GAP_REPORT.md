# Linode API to linodego SDK Gap Report

## Report Metadata

- **Generated**: 2026-03-10 16:55:29 UTC
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
- **Implemented in SDK**: 311 (66.9%)
- **Missing from SDK**: 154
  - *Of which deprecated*: 8

## Endpoint Coverage Analysis

This section lists every endpoint from the Linode API and its implementation status in the linodego SDK.

### Access keys

**Coverage**: 5/5 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/object-storage/keys/{keyId}` | Revoke an Object Storage access key |
| ✅ Implemented | GET | `/{apiVersion}/object-storage/keys` | List Object Storage access keys |
| ✅ Implemented | GET | `/{apiVersion}/object-storage/keys/{keyId}` | Get an Object Storage access key |
| ✅ Implemented | POST | `/{apiVersion}/object-storage/keys` | Create an Object Storage access key |
| ✅ Implemented | PUT | `/{apiVersion}/object-storage/keys/{keyId}` | Update an Object Storage access key |

### Account

**Coverage**: 2/3 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/account` | Get your account |
| ❌ Missing | POST | `/{apiVersion}/account/cancel` | Delete your account |
| ✅ Implemented | PUT | `/{apiVersion}/account` | Update your account |

### Account agreements

**Coverage**: 1/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/account/agreements` | List agreements |
| ❌ Missing | POST | `/{apiVersion}/account/agreements` | Acknowledge agreements |

### Account availability

**Coverage**: 2/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/account/availability` | List available services |
| ✅ Implemented | GET | `/{apiVersion}/account/availability/{regionId}` | Get available services for a region |

### Account settings

**Coverage**: 2/3 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/account/settings` | Get account settings |
| ❌ Missing | POST | `/{apiVersion}/account/settings/managed-enable` | Enable Linode Managed |
| ✅ Implemented | PUT | `/{apiVersion}/account/settings` | Update account settings |

### Account transfer

**Coverage**: 1/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/account/transfer` | Get network usage |

### Advanced parameters

**Coverage**: 2/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/databases/mysql/config` | List MySQL Managed Database advanced parameters |
| ✅ Implemented | GET | `/{apiVersion}/databases/postgresql/config` | List PostgreSQL Managed Database advanced parameters |

### Alerts

**Coverage**: 4/7 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/monitor/services/{serviceType}/alert-definitions/{alertId}` | Delete an alert definition |
| ❌ Missing | GET | `/{apiVersion}/monitor/alert-channels` | List alert channels |
| ❌ Missing | GET | `/{apiVersion}/monitor/alert-definitions` | List alert definitions |
| ❌ Missing | GET | `/{apiVersion}/monitor/services/{serviceType}/alert-definitions` | List alert definitions for a service type |
| ✅ Implemented | GET | `/{apiVersion}/monitor/services/{serviceType}/alert-definitions/{alertId}` | Get an alert definition |
| ✅ Implemented | POST | `/{apiVersion}/monitor/services/{serviceType}/alert-definitions` | Create an alert definition |
| ✅ Implemented | PUT | `/{apiVersion}/monitor/services/{serviceType}/alert-definitions/{alertId}` | Update an alert definition |

### Attachments

**Coverage**: 0/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | POST | `/{apiVersion}/support/tickets/{ticketId}/attachments` | Create a support ticket attachment |

### Backups

**Coverage**: 6/6 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/linode/instances/{linodeId}/backups` | List backups |
| ✅ Implemented | GET | `/{apiVersion}/linode/instances/{linodeId}/backups/{backupId}` | Get a backup |
| ✅ Implemented | POST | `/{apiVersion}/linode/instances/{linodeId}/backups` | Create a snapshot |
| ✅ Implemented | POST | `/{apiVersion}/linode/instances/{linodeId}/backups/cancel` | Cancel backups |
| ✅ Implemented | POST | `/{apiVersion}/linode/instances/{linodeId}/backups/enable` | Enable backups |
| ✅ Implemented | POST | `/{apiVersion}/linode/instances/{linodeId}/backups/{backupId}/restore` | Restore a backup |

### Beta programs

**Coverage**: 5/5 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/account/betas` | List enrolled Beta programs |
| ✅ Implemented | GET | `/{apiVersion}/account/betas/{betaId}` | Get an enrolled Beta program |
| ✅ Implemented | GET | `/{apiVersion}/betas` | List Beta programs |
| ✅ Implemented | GET | `/{apiVersion}/betas/{betaId}` | Get a Beta program |
| ✅ Implemented | POST | `/{apiVersion}/account/betas` | Enroll in a Beta program |

### Buckets

**Coverage**: 8/12 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/object-storage/buckets/{regionId}/{bucket}` | Remove an Object Storage bucket |
| ✅ Implemented | GET | `/{apiVersion}/object-storage/buckets` | List Object Storage buckets |
| ❌ Missing | GET | `/{apiVersion}/object-storage/buckets/{regionId}` | List Object Storage buckets per region |
| ✅ Implemented | GET | `/{apiVersion}/object-storage/buckets/{regionId}/{bucket}` | Get an Object Storage bucket |
| ✅ Implemented | GET | `/{apiVersion}/object-storage/buckets/{regionId}/{bucket}/access` | Get Object Storage bucket access |
| ❌ Missing | GET | `/{apiVersion}/object-storage/buckets/{regionId}/{bucket}/object-acl` | Get an Object Storage object ACL configuration |
| ❌ Missing | GET | `/{apiVersion}/object-storage/buckets/{regionId}/{bucket}/object-list` | List Object Storage bucket contents |
| ✅ Implemented | POST | `/{apiVersion}/object-storage/buckets` | Create an Object Storage bucket |
| ✅ Implemented | POST | `/{apiVersion}/object-storage/buckets/{regionId}/{bucket}/access` | Allow access to an Object Storage bucket |
| ✅ Implemented | POST | `/{apiVersion}/object-storage/buckets/{regionId}/{bucket}/object-url` | Create a URL for an object |
| ❌ Missing | PUT | `/{apiVersion}/object-storage/buckets/{regionId}/{bucket}/access` | Update access to an Object Storage bucket |
| ✅ Implemented | PUT | `/{apiVersion}/object-storage/buckets/{regionId}/{bucket}/object-acl` | Update an object's ACL configuration |

### Child accounts

**Coverage**: 0/3 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/account/child-accounts` | List child accounts |
| ❌ Missing | GET | `/{apiVersion}/account/child-accounts/{euuId}` | Get a child account |
| ❌ Missing | POST | `/{apiVersion}/account/child-accounts/{euuId}/token` | Create a proxy user token |

### Cluster dashboard

**Coverage**: 1/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/lke/clusters/{clusterId}/dashboard` | Get a Kubernetes cluster dashboard URL |

### Clusters

**Coverage**: 9/9 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/lke/clusters/{clusterId}` | Delete a Kubernetes cluster |
| ✅ Implemented | GET | `/{apiVersion}/lke/clusters` | List Kubernetes clusters |
| ✅ Implemented | GET | `/{apiVersion}/lke/clusters/{clusterId}` | Get a Kubernetes cluster |
| ✅ Implemented | GET | `/{apiVersion}/object-storage/clusters` | List clusters |
| ✅ Implemented | GET | `/{apiVersion}/object-storage/clusters/{clusterId}` | Get a cluster |
| ✅ Implemented | POST | `/{apiVersion}/lke/clusters` | Create a Kubernetes cluster |
| ✅ Implemented | POST | `/{apiVersion}/lke/clusters/{clusterId}/recycle` | Recycle cluster nodes |
| ✅ Implemented | POST | `/{apiVersion}/lke/clusters/{clusterId}/regenerate` | Regenerate a Kubernetes cluster |
| ✅ Implemented | PUT | `/{apiVersion}/lke/clusters/{clusterId}` | Update a Kubernetes cluster |

### Configuration profile interfaces

**Coverage**: 1/6 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/linode/instances/{linodeId}/configs/{configId}/interfaces/{interfaceId}` | Delete a configuration profile interface |
| ❌ Missing | GET | `/{apiVersion}/linode/instances/{linodeId}/configs/{configId}/interfaces` | List configuration profile interfaces |
| ❌ Missing | GET | `/{apiVersion}/linode/instances/{linodeId}/configs/{configId}/interfaces/{interfaceId}` | Get a configuration profile interface |
| ✅ Implemented | POST | `/{apiVersion}/linode/instances/{linodeId}/configs/{configId}/interfaces` | Add a configuration profile interface |
| ❌ Missing | POST | `/{apiVersion}/linode/instances/{linodeId}/configs/{configId}/interfaces/order` | Reorder configuration profile interfaces |
| ❌ Missing | PUT | `/{apiVersion}/linode/instances/{linodeId}/configs/{configId}/interfaces/{interfaceId}` | Update a configuration profile interface |

### Configuration profiles

**Coverage**: 4/5 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/linode/instances/{linodeId}/configs/{configId}` | Delete a configuration profile |
| ❌ Missing | GET | `/{apiVersion}/linode/instances/{linodeId}/configs` | List configuration profiles |
| ✅ Implemented | GET | `/{apiVersion}/linode/instances/{linodeId}/configs/{configId}` | Get a configuration profile |
| ✅ Implemented | POST | `/{apiVersion}/linode/instances/{linodeId}/configs` | Create a configuration profile |
| ✅ Implemented | PUT | `/{apiVersion}/linode/instances/{linodeId}/configs/{configId}` | Update a configuration profile |

### Configurations

**Coverage**: 5/6 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId}` | Delete a config |
| ❌ Missing | GET | `/{apiVersion}/nodebalancers/{nodeBalancerId}/configs` | List configs |
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

**Coverage**: 4/4 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/databases/mysql/instances/{instanceId}/credentials` | Get MySQL Managed Database credentials |
| ✅ Implemented | GET | `/{apiVersion}/databases/postgresql/instances/{instanceId}/credentials` | Get PostgreSQL Managed Database credentials |
| ✅ Implemented | POST | `/{apiVersion}/databases/mysql/instances/{instanceId}/credentials/reset` | Reset MySQL Managed Database credentials |
| ✅ Implemented | POST | `/{apiVersion}/databases/postgresql/instances/{instanceId}/credentials/reset` | Reset PostgreSQL Managed Database credentials |

### Databases

**Coverage**: 17/17 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/databases/mysql/instances/{instanceId}` | Delete a MySQL Managed Database |
| ✅ Implemented | DELETE | `/{apiVersion}/databases/postgresql/instances/{instanceId}` | Delete a PostgreSQL Managed Database |
| ✅ Implemented | GET | `/{apiVersion}/databases/instances` | List Managed Databases |
| ✅ Implemented | GET | `/{apiVersion}/databases/mysql/instances` | List MySQL Managed Databases |
| ✅ Implemented | GET | `/{apiVersion}/databases/mysql/instances/{instanceId}` | Get a MySQL Managed Database |
| ✅ Implemented | GET | `/{apiVersion}/databases/postgresql/instances` | List PostgreSQL Managed Databases |
| ✅ Implemented | GET | `/{apiVersion}/databases/postgresql/instances/{instanceId}` | Get a PostgreSQL Managed Database |
| ✅ Implemented | POST | `/{apiVersion}/databases/mysql/instances` | Create or restore a MySQL Managed Database |
| ✅ Implemented | POST | `/{apiVersion}/databases/mysql/instances/{instanceId}/patch` | Patch a MySQL Managed Database |
| ✅ Implemented | POST | `/{apiVersion}/databases/mysql/instances/{instanceId}/resume` | Resume a MySQL Managed Database |
| ✅ Implemented | POST | `/{apiVersion}/databases/mysql/instances/{instanceId}/suspend` | Suspend a MySQL Managed Database |
| ✅ Implemented | POST | `/{apiVersion}/databases/postgresql/instances` | Create or restore a PostgreSQL Managed Database |
| ✅ Implemented | POST | `/{apiVersion}/databases/postgresql/instances/{instanceId}/patch` | Patch a PostgreSQL Managed Database |
| ✅ Implemented | POST | `/{apiVersion}/databases/postgresql/instances/{instanceId}/resume` | Resume a PostgreSQL Managed Database |
| ✅ Implemented | POST | `/{apiVersion}/databases/postgresql/instances/{instanceId}/suspend` | Suspend a PostgreSQL Managed Database |
| ✅ Implemented | PUT | `/{apiVersion}/databases/mysql/instances/{instanceId}` | Update a MySQL Managed Database |
| ✅ Implemented | PUT | `/{apiVersion}/databases/postgresql/instances/{instanceId}` | Update a PostgreSQL Managed Database |

### Devices

**Coverage**: 4/4 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/networking/firewalls/{firewallId}/devices/{deviceId}` | Delete a firewall device |
| ✅ Implemented | GET | `/{apiVersion}/networking/firewalls/{firewallId}/devices` | List firewall devices |
| ✅ Implemented | GET | `/{apiVersion}/networking/firewalls/{firewallId}/devices/{deviceId}` | Get a firewall device |
| ✅ Implemented | POST | `/{apiVersion}/networking/firewalls/{firewallId}/devices` | Create a firewall device |

### Disks

**Coverage**: 7/8 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/linode/instances/{linodeId}/disks/{diskId}` | Delete a disk |
| ❌ Missing | GET | `/{apiVersion}/linode/instances/{linodeId}/disks` | List disks |
| ✅ Implemented | GET | `/{apiVersion}/linode/instances/{linodeId}/disks/{diskId}` | Get a disk |
| ✅ Implemented | POST | `/{apiVersion}/linode/instances/{linodeId}/disks` | Create a disk |
| ✅ Implemented | POST | `/{apiVersion}/linode/instances/{linodeId}/disks/{diskId}/clone` | Clone a disk |
| ✅ Implemented | POST | `/{apiVersion}/linode/instances/{linodeId}/disks/{diskId}/password` | Reset a disk root password |
| ✅ Implemented | POST | `/{apiVersion}/linode/instances/{linodeId}/disks/{diskId}/resize` | Resize a disk |
| ✅ Implemented | PUT | `/{apiVersion}/linode/instances/{linodeId}/disks/{diskId}` | Update a disk |

### Domain zone file

**Coverage**: 1/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/domains/{domainId}/zone-file` | Get a domain zone file |

### Domains

**Coverage**: 7/7 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/domains/{domainId}` | Delete a domain |
| ✅ Implemented | GET | `/{apiVersion}/domains` | List domains |
| ✅ Implemented | GET | `/{apiVersion}/domains/{domainId}` | Get a domain |
| ✅ Implemented | POST | `/{apiVersion}/domains` | Create a domain |
| ✅ Implemented | POST | `/{apiVersion}/domains/import` | Import a domain |
| ✅ Implemented | POST | `/{apiVersion}/domains/{domainId}/clone` | Clone a domain |
| ✅ Implemented | PUT | `/{apiVersion}/domains/{domainId}` | Update a domain |

### Endpoints

**Coverage**: 1/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/object-storage/endpoints` | List Object Storage endpoints |

### Engines

**Coverage**: 2/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/databases/engines` | List Managed Databases engines |
| ✅ Implemented | GET | `/{apiVersion}/databases/engines/{engineId}` | Get a Managed Databases engine |

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

**Coverage**: 3/3 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/account/events` | List events |
| ✅ Implemented | GET | `/{apiVersion}/account/events/{eventId}` | Get an event |
| ✅ Implemented | POST | `/{apiVersion}/account/events/{eventId}/seen` | Mark an event as seen |

### Firewall settings

**Coverage**: 2/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/networking/firewalls/settings` | List default firewalls |
| ✅ Implemented | PUT | `/{apiVersion}/networking/firewalls/settings` | Update default firewalls |

### Firewalls

**Coverage**: 8/14 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/networking/firewalls/{firewallId}` | Delete a firewall |
| ❌ Missing | GET | `/{apiVersion}/linode/instances/{linodeId}/firewalls` | List a Linode's firewalls |
| ✅ Implemented | GET | `/{apiVersion}/networking/firewalls` | List firewalls |
| ✅ Implemented | GET | `/{apiVersion}/networking/firewalls/{firewallId}` | Get a firewall |
| ✅ Implemented | GET | `/{apiVersion}/networking/firewalls/{firewallId}/history` | List firewall rule versions |
| ❌ Missing | GET | `/{apiVersion}/networking/firewalls/{firewallId}/history/rules/{version}` | Get a firewall rule version |
| ✅ Implemented | GET | `/{apiVersion}/networking/firewalls/{firewallId}/rules` | List firewall rules |
| ❌ Missing | GET | `/{apiVersion}/nodebalancers/{nodeBalancerId}/firewalls` | List NodeBalancer firewalls |
| ❌ Missing | POST | `/{apiVersion}/linode/instances/{linodeId}/firewalls/apply` | Apply a Linode's firewalls |
| ✅ Implemented | POST | `/{apiVersion}/networking/firewalls` | Create a firewall |
| ❌ Missing | PUT | `/{apiVersion}/linode/instances/{linodeId}/firewalls` | Update a Linode's firewalls |
| ✅ Implemented | PUT | `/{apiVersion}/networking/firewalls/{firewallId}` | Update a firewall |
| ✅ Implemented | PUT | `/{apiVersion}/networking/firewalls/{firewallId}/rules` | Update firewall rules |
| ❌ Missing | PUT | `/{apiVersion}/nodebalancers/{nodeBalancerId}/firewalls` | Update a NodeBalancer's firewalls |

### Grants

**Coverage**: 1/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/profile/grants` | List grants |

### IP addresses

**Coverage**: 10/13 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/linode/instances/{linodeId}/ips/{address}` | Delete an IPv4 address |
| ✅ Implemented | GET | `/{apiVersion}/linode/instances/{linodeId}/ips` | Get networking information |
| ✅ Implemented | GET | `/{apiVersion}/linode/instances/{linodeId}/ips/{address}` | Get a Linode's IP address |
| ✅ Implemented | GET | `/{apiVersion}/networking/ips` | List IP addresses |
| ✅ Implemented | GET | `/{apiVersion}/networking/ips/{address}` | Get an IP address |
| ✅ Implemented | GET | `/{apiVersion}/vpcs/ips` | List VPC IP addresses |
| ❌ Missing | GET | `/{apiVersion}/vpcs/{vpcId}/ips` | List a VPC's IP addresses |
| ✅ Implemented | POST | `/{apiVersion}/linode/instances/{linodeId}/ips` | Allocate an IPv4 address |
| ✅ Implemented | POST | `/{apiVersion}/networking/ips` | Allocate an IP address |
| ❌ Missing | POST | `/{apiVersion}/networking/ips/assign` | Assign IP addresses |
| ❌ Missing | POST | `/{apiVersion}/networking/ips/share` | Share IP addresses |
| ✅ Implemented | PUT | `/{apiVersion}/linode/instances/{linodeId}/ips/{address}` | Update an IP address's RDNS for a Linode |
| ✅ Implemented | PUT | `/{apiVersion}/networking/ips/{address}` | Update an IP address's RDNS |

### IPv4 addresses

**Coverage**: 0/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | POST | `/{apiVersion}/networking/ipv4/assign` | Assign IPv4s to Linodes |
| ❌ Missing | POST | `/{apiVersion}/networking/ipv4/share` | Configure IPv4 sharing |

### IPv6 pools

**Coverage**: 1/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/networking/ipv6/pools` | List IPv6 pools |

### IPv6 ranges

**Coverage**: 4/4 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/networking/ipv6/ranges/{range}` | Delete an IPv6 range |
| ✅ Implemented | GET | `/{apiVersion}/networking/ipv6/ranges` | List IPv6 ranges |
| ✅ Implemented | GET | `/{apiVersion}/networking/ipv6/ranges/{range}` | Get an IPv6 range |
| ✅ Implemented | POST | `/{apiVersion}/networking/ipv6/ranges` | Create an IPv6 range |

### Identity Management

**Coverage**: 2/4 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/entities` | List entities |
| ✅ Implemented | GET | `/{apiVersion}/iam/role-permissions` | List available roles |
| ❌ Missing | GET | `/{apiVersion}/iam/users/{username}/role-permissions` | Get a user's access level |
| ❌ Missing | PUT | `/{apiVersion}/iam/users/{username}/role-permissions` | Update a user's access level |

### Image sharing

**Coverage**: 0/22 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/images/sharegroups/tokens/{tokenUuid}` | Delete a token |
| ❌ Missing | DELETE | `/{apiVersion}/images/sharegroups/{sharegroupId}` | Delete a share group |
| ❌ Missing | DELETE | `/{apiVersion}/images/sharegroups/{sharegroupId}/images/{imageId}` | Revoke access to a shared image |
| ❌ Missing | DELETE | `/{apiVersion}/images/sharegroups/{sharegroupId}/members/{tokenUuid}` | Revoke a membership token |
| ❌ Missing | GET | `/{apiVersion}/images/sharegroups` | List share groups |
| ❌ Missing | GET | `/{apiVersion}/images/sharegroups/tokens` | List a user's tokens |
| ❌ Missing | GET | `/{apiVersion}/images/sharegroups/tokens/{tokenUuid}` | Get a token |
| ❌ Missing | GET | `/{apiVersion}/images/sharegroups/tokens/{tokenUuid}/sharegroup` | Get a token's share group |
| ❌ Missing | GET | `/{apiVersion}/images/sharegroups/tokens/{tokenUuid}/sharegroup/images` | List images by token |
| ❌ Missing | GET | `/{apiVersion}/images/sharegroups/{sharegroupId}` | Get a share group |
| ❌ Missing | GET | `/{apiVersion}/images/sharegroups/{sharegroupId}/images` | List shared images by group |
| ❌ Missing | GET | `/{apiVersion}/images/sharegroups/{sharegroupId}/members` | List members by share group |
| ❌ Missing | GET | `/{apiVersion}/images/sharegroups/{sharegroupId}/members/{tokenUuid}` | Get a membership token |
| ❌ Missing | GET | `/{apiVersion}/images/{imageId}/sharegroups` | List share groups by image |
| ❌ Missing | POST | `/{apiVersion}/images/sharegroups` | Create a share group |
| ❌ Missing | POST | `/{apiVersion}/images/sharegroups/tokens` | Create a token |
| ❌ Missing | POST | `/{apiVersion}/images/sharegroups/{sharegroupId}/images` | Add images to a share group |
| ❌ Missing | POST | `/{apiVersion}/images/sharegroups/{sharegroupId}/members` | Add members to a share group |
| ❌ Missing | PUT | `/{apiVersion}/images/sharegroups/tokens/{tokenUuid}` | Update a token |
| ❌ Missing | PUT | `/{apiVersion}/images/sharegroups/{sharegroupId}` | Update a share group |
| ❌ Missing | PUT | `/{apiVersion}/images/sharegroups/{sharegroupId}/images/{imageId}` | Update a shared image |
| ❌ Missing | PUT | `/{apiVersion}/images/sharegroups/{sharegroupId}/members/{tokenUuid}` | Update a membership token |

### Images

**Coverage**: 0/7 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/images/{imageId}` | Delete an image |
| ❌ Missing | GET | `/{apiVersion}/images` | List images |
| ❌ Missing | GET | `/{apiVersion}/images/{imageId}` | Get an image |
| ❌ Missing | POST | `/{apiVersion}/images` | Create an image |
| ❌ Missing | POST | `/{apiVersion}/images/upload` | Upload an image |
| ❌ Missing | POST | `/{apiVersion}/images/{imageId}/regions` | Replicate an image |
| ❌ Missing | PUT | `/{apiVersion}/images/{imageId}` | Update an image |

### Invoices

**Coverage**: 2/3 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/account/invoices` | List invoices |
| ✅ Implemented | GET | `/{apiVersion}/account/invoices/{invoiceId}` | Get an invoice |
| ❌ Missing | GET | `/{apiVersion}/account/invoices/{invoiceId}/items` | List invoice items |

### Kernels

**Coverage**: 2/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/linode/kernels` | List kernels |
| ✅ Implemented | GET | `/{apiVersion}/linode/kernels/{kernelId}` | Get a kernel |

### Kubeconfigs

**Coverage**: 2/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/lke/clusters/{clusterId}/kubeconfig` | Delete a Kubeconfig |
| ✅ Implemented | GET | `/{apiVersion}/lke/clusters/{clusterId}/kubeconfig` | Get a Kubeconfig |

### LKE API endpoints

**Coverage**: 0/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/lke/clusters/{clusterId}/api-endpoints` | List Kubernetes API endpoints |

### LKE service tokens

**Coverage**: 1/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/lke/clusters/{clusterId}/servicetoken` | Delete a service token |

### LKE types

**Coverage**: 0/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/lke/types` | List Kubernetes types |

### LKE versions

**Coverage**: 1/4 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/lke/tiers/{tier}/versions` | List LKE Kubernetes versions (any tier) |
| ❌ Missing | GET | `/{apiVersion}/lke/tiers/{tier}/versions/{version}` | Get an LKE Kubernetes version (any tier) |
| ❌ Missing | GET | `/{apiVersion}/lke/versions` | List LKE Kubernetes versions (non-enterprise) |
| ✅ Implemented | GET | `/{apiVersion}/lke/versions/{version}` | Get an LKE Kubernetes version (non-enterprise) |

### Linode instances

**Coverage**: 15/15 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/linode/instances/{linodeId}` | Delete a Linode |
| ✅ Implemented | GET | `/{apiVersion}/linode/instances` | List Linodes |
| ✅ Implemented | GET | `/{apiVersion}/linode/instances/{linodeId}` | Get a Linode |
| ✅ Implemented | POST | `/{apiVersion}/linode/instances` | Create a Linode |
| ✅ Implemented | POST | `/{apiVersion}/linode/instances/{linodeId}/boot` | Boot a Linode |
| ✅ Implemented | POST | `/{apiVersion}/linode/instances/{linodeId}/clone` | Clone a Linode |
| ✅ Implemented | POST | `/{apiVersion}/linode/instances/{linodeId}/migrate` | Launch a DC migration/pending host migration |
| ✅ Implemented | POST | `/{apiVersion}/linode/instances/{linodeId}/mutate` | Upgrade a Linode |
| ✅ Implemented | POST | `/{apiVersion}/linode/instances/{linodeId}/password` | Reset a Linode's root password |
| ✅ Implemented | POST | `/{apiVersion}/linode/instances/{linodeId}/reboot` | Reboot a Linode |
| ✅ Implemented | POST | `/{apiVersion}/linode/instances/{linodeId}/rebuild` | Rebuild a Linode |
| ✅ Implemented | POST | `/{apiVersion}/linode/instances/{linodeId}/rescue` | Boot a Linode into rescue mode |
| ✅ Implemented | POST | `/{apiVersion}/linode/instances/{linodeId}/resize` | Resize a Linode |
| ✅ Implemented | POST | `/{apiVersion}/linode/instances/{linodeId}/shutdown` | Shut down a Linode |
| ✅ Implemented | PUT | `/{apiVersion}/linode/instances/{linodeId}` | Update a Linode |

### Linode interfaces

**Coverage**: 10/10 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/linode/instances/{linodeId}/interfaces/{interfaceId}` | Delete a Linode interface |
| ✅ Implemented | GET | `/{apiVersion}/linode/instances/{linodeId}/interfaces` | List Linode interfaces |
| ✅ Implemented | GET | `/{apiVersion}/linode/instances/{linodeId}/interfaces/history` | List a Linode's network interface history |
| ✅ Implemented | GET | `/{apiVersion}/linode/instances/{linodeId}/interfaces/settings` | List Linode interface settings |
| ✅ Implemented | GET | `/{apiVersion}/linode/instances/{linodeId}/interfaces/{interfaceId}` | Get a Linode interface |
| ✅ Implemented | GET | `/{apiVersion}/linode/instances/{linodeId}/interfaces/{interfaceId}/firewalls` | List Linode interface firewalls |
| ✅ Implemented | POST | `/{apiVersion}/linode/instances/{linodeId}/interfaces` | Add a Linode interface |
| ✅ Implemented | POST | `/{apiVersion}/linode/instances/{linodeId}/upgrade-interfaces` | Upgrade to Linode interfaces |
| ✅ Implemented | PUT | `/{apiVersion}/linode/instances/{linodeId}/interfaces/settings` | Update Linode interface settings |
| ✅ Implemented | PUT | `/{apiVersion}/linode/instances/{linodeId}/interfaces/{interfaceId}` | Update a Linode interface |

### Linode types

**Coverage**: 1/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/linode/types` | List types |
| ✅ Implemented | GET | `/{apiVersion}/linode/types/{typeId}` | Get a type |

### Logins

**Coverage**: 4/4 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/account/logins` | List user logins |
| ✅ Implemented | GET | `/{apiVersion}/account/logins/{loginId}` | Get an account login |
| ✅ Implemented | GET | `/{apiVersion}/profile/logins` | List logins |
| ✅ Implemented | GET | `/{apiVersion}/profile/logins/{loginId}` | Get a profile's login |

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

**Coverage**: 5/5 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/longview/clients/{clientId}` | Delete a Longview client |
| ✅ Implemented | GET | `/{apiVersion}/longview/clients` | List Longview clients |
| ✅ Implemented | GET | `/{apiVersion}/longview/clients/{clientId}` | Get a Longview client |
| ✅ Implemented | POST | `/{apiVersion}/longview/clients` | Create a Longview client |
| ✅ Implemented | PUT | `/{apiVersion}/longview/clients/{clientId}` | Update a Longview client |

### Longview plans

**Coverage**: 2/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/longview/plan` | Get a Longview plan |
| ✅ Implemented | PUT | `/{apiVersion}/longview/plan` | Update a Longview plan |

### Longview subscriptions

**Coverage**: 2/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/longview/subscriptions` | List Longview subscriptions |
| ✅ Implemented | GET | `/{apiVersion}/longview/subscriptions/{subscriptionId}` | Get a Longview subscription |

### Longview types

**Coverage**: 0/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/longview/types` | List Longview types |

### Maintenance policies

**Coverage**: 1/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/maintenance/policies` | List maintenance policies |

### Maintenances

**Coverage**: 1/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/account/maintenance` | List maintenances |

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

**Coverage**: 0/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/managed/stats` | List managed stats |

### Metrics

**Coverage**: 5/8 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/monitor/dashboards` | List dashboards |
| ✅ Implemented | GET | `/{apiVersion}/monitor/dashboards/{dashboardId}` | Get a dashboard |
| ✅ Implemented | GET | `/{apiVersion}/monitor/services` | List supported service types |
| ✅ Implemented | GET | `/{apiVersion}/monitor/services/{serviceType}` | Get details for a supported service type |
| ❌ Missing | GET | `/{apiVersion}/monitor/services/{serviceType}/dashboards` | List dashboards for a service type |
| ❌ Missing | GET | `/{apiVersion}/monitor/services/{serviceType}/metric-definitions` | List metrics for a service type |
| ❌ Missing | POST | `/{apiVersion}/monitor/services/{serviceType}/metrics` | Get an entity's metrics |
| ✅ Implemented | POST | `/{apiVersion}/monitor/services/{serviceType}/token` | Create a token for a service type |

### Network transfer prices

**Coverage**: 0/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/network-transfer/prices` | List network transfer prices |

### Node pools

**Coverage**: 5/6 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/lke/clusters/{clusterId}/pools/{poolId}` | Delete a node pool |
| ❌ Missing | GET | `/{apiVersion}/lke/clusters/{clusterId}/pools` | List node pools |
| ✅ Implemented | GET | `/{apiVersion}/lke/clusters/{clusterId}/pools/{poolId}` | Get a node pool |
| ✅ Implemented | POST | `/{apiVersion}/lke/clusters/{clusterId}/pools` | Create a node pool |
| ✅ Implemented | POST | `/{apiVersion}/lke/clusters/{clusterId}/pools/{poolId}/recycle` | Recycle a node pool |
| ✅ Implemented | PUT | `/{apiVersion}/lke/clusters/{clusterId}/pools/{poolId}` | Update a node pool |

### NodeBalancer types

**Coverage**: 1/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/nodebalancers/types` | List NodeBalancer types |

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

**Coverage**: 7/8 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/lke/clusters/{clusterId}/nodes/{nodeId}` | Delete a node |
| ✅ Implemented | DELETE | `/{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId}/nodes/{nodeId}` | Delete a NodeBalancer's node |
| ✅ Implemented | GET | `/{apiVersion}/lke/clusters/{clusterId}/nodes/{nodeId}` | Get a node |
| ❌ Missing | GET | `/{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId}/nodes` | List nodes |
| ✅ Implemented | GET | `/{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId}/nodes/{nodeId}` | Get a NodeBalancer's node |
| ✅ Implemented | POST | `/{apiVersion}/lke/clusters/{clusterId}/nodes/{nodeId}/recycle` | Recycle a node |
| ✅ Implemented | POST | `/{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId}/nodes` | Create a node |
| ✅ Implemented | PUT | `/{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId}/nodes/{nodeId}` | Update a node |

### Notifications

**Coverage**: 1/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/account/notifications` | List notifications |

### OAuth apps

**Coverage**: 3/3 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/profile/apps/{appId}` | Revoke app access |
| ✅ Implemented | GET | `/{apiVersion}/profile/apps` | List authorized apps |
| ✅ Implemented | GET | `/{apiVersion}/profile/apps/{appId}` | Get an authorized app |

### OAuth client

**Coverage**: 0/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/account/oauth-clients/{clientId}/thumbnail` | Get the OAuth client's thumbnail |
| ❌ Missing | PUT | `/{apiVersion}/account/oauth-clients/{clientId}/thumbnail` | Update the OAuth client's thumbnail |

### OAuth clients

**Coverage**: 6/6 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/account/oauth-clients/{clientId}` | Delete an OAuth client |
| ✅ Implemented | GET | `/{apiVersion}/account/oauth-clients` | List OAuth clients |
| ✅ Implemented | GET | `/{apiVersion}/account/oauth-clients/{clientId}` | Get an OAuth client |
| ✅ Implemented | POST | `/{apiVersion}/account/oauth-clients` | Create an OAuth client |
| ✅ Implemented | POST | `/{apiVersion}/account/oauth-clients/{clientId}/reset-secret` | Reset an OAuth client secret |
| ✅ Implemented | PUT | `/{apiVersion}/account/oauth-clients/{clientId}` | Update an OAuth client |

### OAuth preferences

**Coverage**: 2/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/profile/preferences` | Get user preferences |
| ✅ Implemented | PUT | `/{apiVersion}/profile/preferences` | Update a user's preferences |

### Object Storage

**Coverage**: 4/6 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | GET | `/{apiVersion}/object-storage/quotas` | List Object Storage quotas |
| ✅ Implemented | GET | `/{apiVersion}/object-storage/quotas/{objQuotaId}` | Get an Object Storage quota |
| ✅ Implemented | GET | `/{apiVersion}/object-storage/quotas/{objQuotaId}/usage` | Get Object Storage quota usage data |
| ✅ Implemented | GET | `/{apiVersion}/object-storage/transfer` | Get Object Storage transfer data |
| ❌ Missing | GET | `/{apiVersion}/object-storage/types` | List Object Storage types |
| ✅ Implemented | POST | `/{apiVersion}/object-storage/cancel` | Cancel Object Storage |

### Payment methods

**Coverage**: 3/5 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/account/payment-methods/{paymentMethodId}` | Delete a payment method |
| ✅ Implemented | GET | `/{apiVersion}/account/payment-methods` | List payment methods |
| ✅ Implemented | GET | `/{apiVersion}/account/payment-methods/{paymentMethodId}` | Get a payment method |
| ❌ Missing | POST | `/{apiVersion}/account/payment-methods` | Add a payment method |
| ❌ Missing | POST | `/{apiVersion}/account/payment-methods/{paymentMethodId}/make-default` | Set a default payment method |

### Payments

**Coverage**: 3/6 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/account/payments` | List payments |
| ✅ Implemented | GET | `/{apiVersion}/account/payments/{paymentId}` | Get a payment |
| ⚠️ Missing (Deprecated) | POST | `/{apiVersion}/account/credit-card` | Add or edit a credit card |
| ✅ Implemented | POST | `/{apiVersion}/account/payments` | Make a payment |
| ⚠️ Missing (Deprecated) | POST | `/{apiVersion}/account/payments/paypal` | Stage a PayPal payment |
| ⚠️ Missing (Deprecated) | POST | `/{apiVersion}/account/payments/paypal/execute` | Execute a PayPal payment |

### Personal access tokens

**Coverage**: 5/5 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/profile/tokens/{tokenId}` | Revoke a personal access token |
| ✅ Implemented | GET | `/{apiVersion}/profile/tokens` | List personal access tokens |
| ✅ Implemented | GET | `/{apiVersion}/profile/tokens/{tokenId}` | Get a personal access token |
| ✅ Implemented | POST | `/{apiVersion}/profile/tokens` | Create a personal access token |
| ✅ Implemented | PUT | `/{apiVersion}/profile/tokens/{tokenId}` | Update a personal access token |

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

**Coverage**: 1/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | POST | `/{apiVersion}/account/promo-codes` | Add a promo credit |

### Records

**Coverage**: 4/5 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/domains/{domainId}/records/{recordId}` | Delete a domain record |
| ❌ Missing | GET | `/{apiVersion}/domains/{domainId}/records` | List domain records |
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

**Coverage**: 5/5 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/profile/sshkeys/{sshKeyId}` | Delete an SSH key |
| ✅ Implemented | GET | `/{apiVersion}/profile/sshkeys` | List SSH keys |
| ✅ Implemented | GET | `/{apiVersion}/profile/sshkeys/{sshKeyId}` | Get an SSH key |
| ✅ Implemented | POST | `/{apiVersion}/profile/sshkeys` | Add an SSH key |
| ✅ Implemented | PUT | `/{apiVersion}/profile/sshkeys/{sshKeyId}` | Update an SSH key |

### SSL certificates

**Coverage**: 2/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/databases/mysql/instances/{instanceId}/ssl` | Get a MySQL Managed Database SSL certificate |
| ✅ Implemented | GET | `/{apiVersion}/databases/postgresql/instances/{instanceId}/ssl` | Get a PostgreSQL Managed Database SSL certificate |

### Security questions

**Coverage**: 1/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/profile/security-questions` | List security questions |
| ❌ Missing | POST | `/{apiVersion}/profile/security-questions` | Answer security questions |

### Service transfers

**Coverage**: 5/5 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/account/service-transfers/{token}` | Cancel a service transfer |
| ✅ Implemented | GET | `/{apiVersion}/account/service-transfers` | List service transfers |
| ✅ Implemented | GET | `/{apiVersion}/account/service-transfers/{token}` | Get a service transfer request |
| ✅ Implemented | POST | `/{apiVersion}/account/service-transfers` | Request a service transfer |
| ✅ Implemented | POST | `/{apiVersion}/account/service-transfers/{token}/accept` | Accept a service transfer |

### StackScripts

**Coverage**: 5/5 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/linode/stackscripts/{stackscriptId}` | Delete a StackScript |
| ✅ Implemented | GET | `/{apiVersion}/linode/stackscripts` | List StackScripts |
| ✅ Implemented | GET | `/{apiVersion}/linode/stackscripts/{stackscriptId}` | Get a StackScript |
| ✅ Implemented | POST | `/{apiVersion}/linode/stackscripts` | Create a StackScript |
| ✅ Implemented | PUT | `/{apiVersion}/linode/stackscripts/{stackscriptId}` | Update a StackScript |

### Statistics

**Coverage**: 5/5 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/linode/instances/{linodeId}/stats` | Get daily Linode statistics |
| ✅ Implemented | GET | `/{apiVersion}/linode/instances/{linodeId}/stats/{year}/{month}` | Get a month's Linode statistics |
| ✅ Implemented | GET | `/{apiVersion}/linode/instances/{linodeId}/transfer` | Get this month's network transfer stats |
| ✅ Implemented | GET | `/{apiVersion}/linode/instances/{linodeId}/transfer/{year}/{month}` | Get monthly network transfer stats |
| ✅ Implemented | GET | `/{apiVersion}/nodebalancers/{nodeBalancerId}/stats` | Get NodeBalancer statistics |

### Support tickets

**Coverage**: 2/4 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/support/tickets` | List support tickets |
| ✅ Implemented | GET | `/{apiVersion}/support/tickets/{ticketId}` | Get a support ticket |
| ❌ Missing | POST | `/{apiVersion}/support/tickets` | Open a support ticket |
| ❌ Missing | POST | `/{apiVersion}/support/tickets/{ticketId}/close` | Close a support ticket |

### TLS/SSL certificates

**Coverage**: 3/3 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/object-storage/buckets/{regionId}/{bucket}/ssl` | Delete an Object Storage TLS/SSL certificate |
| ✅ Implemented | GET | `/{apiVersion}/object-storage/buckets/{regionId}/{bucket}/ssl` | Get an Object Storage TLS/SSL certificate |
| ✅ Implemented | POST | `/{apiVersion}/object-storage/buckets/{regionId}/{bucket}/ssl` | Upload an Object Storage TLS/SSL certificate |

### Tags

**Coverage**: 3/4 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/tags/{tagLabel}` | Delete a tag |
| ✅ Implemented | GET | `/{apiVersion}/tags` | List tags |
| ❌ Missing | GET | `/{apiVersion}/tags/{tagLabel}` | List tagged objects |
| ✅ Implemented | POST | `/{apiVersion}/tags` | Create a tag |

### Templates

**Coverage**: 2/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/networking/firewalls/templates` | List firewall templates |
| ✅ Implemented | GET | `/{apiVersion}/networking/firewalls/templates/{slug}` | Get a firewall template |

### Trusted devices

**Coverage**: 3/3 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/profile/devices/{deviceId}` | Revoke a trusted device |
| ✅ Implemented | GET | `/{apiVersion}/profile/devices` | List trusted devices |
| ✅ Implemented | GET | `/{apiVersion}/profile/devices/{deviceId}` | Get a trusted device |

### Two-factor authentication

**Coverage**: 3/3 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | POST | `/{apiVersion}/profile/tfa-disable` | Disable two-factor authentication |
| ✅ Implemented | POST | `/{apiVersion}/profile/tfa-enable` | Generate a secret key for two-factor authentication |
| ✅ Implemented | POST | `/{apiVersion}/profile/tfa-enable-confirm` | Enable two-factor authentication |

### Types

**Coverage**: 2/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/databases/types` | List Managed Databases types |
| ✅ Implemented | GET | `/{apiVersion}/databases/types/{typeId}` | Get a Managed Databases type |

### Users

**Coverage**: 7/7 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/account/users/{username}` | Delete a user |
| ✅ Implemented | GET | `/{apiVersion}/account/users` | List users |
| ✅ Implemented | GET | `/{apiVersion}/account/users/{username}` | Get a user |
| ✅ Implemented | GET | `/{apiVersion}/account/users/{username}/grants` | List a user's grants |
| ✅ Implemented | POST | `/{apiVersion}/account/users` | Create a user |
| ✅ Implemented | PUT | `/{apiVersion}/account/users/{username}` | Update a user |
| ✅ Implemented | PUT | `/{apiVersion}/account/users/{username}/grants` | Update a user's grants |

### VLANs

**Coverage**: 1/2 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ❌ Missing | DELETE | `/{apiVersion}/networking/vlans/{regionId}/{label}` | Delete a VLAN |
| ✅ Implemented | GET | `/{apiVersion}/networking/vlans` | List VLANs |

### VPC subnets

**Coverage**: 4/5 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/vpcs/{vpcId}/subnets/{vpcSubnetId}` | Delete a VPC subnet |
| ❌ Missing | GET | `/{apiVersion}/vpcs/{vpcId}/subnets` | List VPC subnets |
| ✅ Implemented | GET | `/{apiVersion}/vpcs/{vpcId}/subnets/{vpcSubnetId}` | Get a VPC subnet |
| ✅ Implemented | POST | `/{apiVersion}/vpcs/{vpcId}/subnets` | Create a VPC subnet |
| ✅ Implemented | PUT | `/{apiVersion}/vpcs/{vpcId}/subnets/{vpcSubnetId}` | Update a VPC subnet |

### VPCs

**Coverage**: 6/7 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | DELETE | `/{apiVersion}/vpcs/{vpcId}` | Delete a VPC |
| ❌ Missing | GET | `/{apiVersion}/nodebalancers/{nodeBalancerId}/vpcs` | List VPC configurations |
| ✅ Implemented | GET | `/{apiVersion}/nodebalancers/{nodeBalancerId}/vpcs/{nodeBalancerVpcConfigId}` | Get a VPC configuration |
| ✅ Implemented | GET | `/{apiVersion}/vpcs` | List VPCs |
| ✅ Implemented | GET | `/{apiVersion}/vpcs/{vpcId}` | Get a VPC |
| ✅ Implemented | POST | `/{apiVersion}/vpcs` | Create a VPC |
| ✅ Implemented | PUT | `/{apiVersion}/vpcs/{vpcId}` | Update a VPC |

### Volume types

**Coverage**: 1/1 endpoints implemented

| Status | Method | Path | Summary |
|--------|--------|------|---------|
| ✅ Implemented | GET | `/{apiVersion}/volumes/types` | List volume types |

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

#### DELETE /{apiVersion}/account/oauth-clients/{clientId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `clientId` (Required, type: `string`)

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

#### DELETE /{apiVersion}/account/payment-methods/{paymentMethodId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `paymentMethodId` (Required, type: `integer`)

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

#### DELETE /{apiVersion}/account/service-transfers/{token}

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
- `type`
- `unavailable`
- `used`
- `when`
- `zip`

*Related structs analyzed*: AccountMaintenance, AccountSettings, AccountSettingsUpdateOptions, AccountServiceTransfer, AccountServiceTransferEntity, AccountServiceTransferRequestOptions, Account, AccountUpdateOptions, AccountAgreements, AccountAgreementsUpdateOptions, AccountRolePermissions, AccountAccess, AccountTransfer, AccountTransferRegion, AccountAvailability, AccountBetaProgram, AccountBetaProgramCreateOpts

#### DELETE /{apiVersion}/account/users/{username}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `username` (Required, type: `string`)

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

#### DELETE /{apiVersion}/databases/mysql/instances/{instanceId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `instanceId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `allow_list`
- `available`
- `binlog_retention_period`
- `ca_certificate`
- `cluster_size`
- `configs`
- `connect_timeout`
- `cpu`
- `data`
- `default_time_zone`
- `description`
- `disk`
- `disks`
- `encrypted`
- `engine`
- `engine_config`
- `example`
- `filesystem`
- `fork`
- `gpus`
- `group_concat_max_len`
- `hosts`
- `id`
- `information_schema_stats_expiry`
- `innodb_change_buffer_max_size`
- `innodb_flush_neighbors`
- `innodb_ft_min_token_size`
- `innodb_ft_server_stopword_table`
- `innodb_lock_wait_timeout`
- `innodb_log_buffer_size`
- `innodb_online_alter_log_max_size`
- `innodb_read_io_threads`
- `innodb_rollback_on_timeout`
- `innodb_thread_concurrency`
- `innodb_write_io_threads`
- `interactive_timeout`
- `internal_tmp_mem_storage_engine`
- `io`
- `label`
- `max_allowed_packet`
- `max_heap_table_size`
- `maximum`
- `members`
- `memory`
- `minimum`
- `mysql`
- `net_buffer_length`
- `net_read_timeout`
- `net_write_timeout`
- `netv4`
- `netv6`
- `password`
- `platform`
- `port`
- `private_network`
- `region`
- `requires_restart`
- `size`
- `sort_buffer_size`
- `sql_mode`
- `sql_require_primary_key`
- `ssl_connection`
- `status`
- `title`
- `tmp_table_size`
- `total_disk_size_gb`
- `transfer`
- `type`
- `updates`
- `used_disk_size_gb`
- `username`
- `vcpus`
- `version`
- `wait_timeout`

*Related structs analyzed*: InstanceStatsData, InstanceStats, MySQLDatabase, MySQLDatabaseEngineConfig, MySQLDatabaseEngineConfigMySQL, MySQLDatabaseConfigInfo, MySQLDatabaseConfigInfoMySQL, MySQLDatabaseConfigInfoBinlogRetentionPeriod, MySQLCreateOptions, MySQLUpdateOptions, MySQLDatabaseCredential, MySQLDatabaseSSL, PostgresDatabaseSSL, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec

#### DELETE /{apiVersion}/databases/postgresql/instances/{instanceId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `instanceId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `available`
- `ca_certificate`
- `configs`
- `cpu`
- `data`
- `disk`
- `disks`
- `filesystem`
- `gpus`
- `id`
- `io`
- `label`
- `memory`
- `netv4`
- `netv6`
- `size`
- `status`
- `title`
- `transfer`
- `type`
- `vcpus`

*Related structs analyzed*: InstanceStatsData, InstanceStats, MySQLDatabaseSSL, PostgresDatabaseSSL, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec

#### DELETE /{apiVersion}/domains/{domainId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `domainId` (Required, type: `integer`)

#### DELETE /{apiVersion}/domains/{domainId}/records/{recordId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `domainId` (Required, type: `integer`)
- `recordId` (Required, type: `integer`)

#### DELETE /{apiVersion}/linode/instances/{linodeId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### DELETE /{apiVersion}/linode/instances/{linodeId}/configs/{configId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `configId` (Required, type: `integer`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### DELETE /{apiVersion}/linode/instances/{linodeId}/disks/{diskId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `diskId` (Required, type: `integer`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### DELETE /{apiVersion}/linode/instances/{linodeId}/interfaces/{interfaceId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `interfaceId` (Required, type: `integer`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `ids`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_helper`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InterfaceSettings, InterfaceSettingsUpdateOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel, InstanceConfigInterfacesReorderOptions

#### DELETE /{apiVersion}/linode/instances/{linodeId}/ips/{address}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### DELETE /{apiVersion}/linode/stackscripts/{stackscriptId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `stackscriptId` (Required, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `backups`
- `class`
- `config_id`
- `default_route`
- `deprecated`
- `disk`
- `dry_run`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `instance_id`
- `interfaces`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `status`
- `successor`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### DELETE /{apiVersion}/lke/clusters/{clusterId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `clusterId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `acl`
- `addresses`
- `apl_enabled`
- `audit_logs_enabled`
- `autoscaler`
- `control_plane`
- `count`
- `description`
- `disk_encryption`
- `disks`
- `effect`
- `enabled`
- `endpoint`
- `firewall_id`
- `high_availability`
- `id`
- `instance_id`
- `ipv4`
- `ipv6`
- `k8s_version`
- `key`
- `kubeconfig`
- `label`
- `labels`
- `max`
- `maximum`
- `min`
- `minimum`
- `node_pools`
- `nodes`
- `region`
- `requires_restart`
- `revision-id`
- `servicetoken`
- `size`
- `stack_type`
- `status`
- `subnet_id`
- `tags`
- `taints`
- `tier`
- `type`
- `update_strategy`
- `url`
- `value`
- `vpc_id`

*Related structs analyzed*: LKECluster, LKEClusterCreateOptions, LKEClusterUpdateOptions, LKEClusterAPIEndpoint, LKEClusterKubeconfig, LKEClusterDashboard, LKEVersion, LKETierVersion, LKEClusterRegenerateOptions, LKENodePoolDisk, LKENodePoolAutoscaler, LKENodePoolLinode, LKENodePoolTaint, LKENodePool, LKENodePoolCreateOptions, LKENodePoolUpdateOptions, MaxSlotWALKeepSize, LKEClusterControlPlane, LKEClusterControlPlaneACLAddresses, LKEClusterControlPlaneACL, LKEClusterControlPlaneACLAddressesOptions, LKEClusterControlPlaneACLOptions, LKEClusterControlPlaneOptions, LKEClusterControlPlaneACLUpdateOptions, LKEClusterControlPlaneACLResponse

#### DELETE /{apiVersion}/lke/clusters/{clusterId}/kubeconfig

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `clusterId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `acl`
- `addresses`
- `apl_enabled`
- `audit_logs_enabled`
- `autoscaler`
- `control_plane`
- `count`
- `description`
- `disk_encryption`
- `disks`
- `effect`
- `enabled`
- `endpoint`
- `firewall_id`
- `high_availability`
- `id`
- `instance_id`
- `ipv4`
- `ipv6`
- `k8s_version`
- `key`
- `kubeconfig`
- `label`
- `labels`
- `max`
- `maximum`
- `min`
- `minimum`
- `node_pools`
- `nodes`
- `region`
- `requires_restart`
- `revision-id`
- `servicetoken`
- `size`
- `stack_type`
- `status`
- `subnet_id`
- `tags`
- `taints`
- `tier`
- `type`
- `update_strategy`
- `url`
- `value`
- `vpc_id`

*Related structs analyzed*: LKECluster, LKEClusterCreateOptions, LKEClusterUpdateOptions, LKEClusterAPIEndpoint, LKEClusterKubeconfig, LKEClusterDashboard, LKEVersion, LKETierVersion, LKEClusterRegenerateOptions, LKENodePoolDisk, LKENodePoolAutoscaler, LKENodePoolLinode, LKENodePoolTaint, LKENodePool, LKENodePoolCreateOptions, LKENodePoolUpdateOptions, MaxSlotWALKeepSize, LKEClusterControlPlane, LKEClusterControlPlaneACLAddresses, LKEClusterControlPlaneACL, LKEClusterControlPlaneACLAddressesOptions, LKEClusterControlPlaneACLOptions, LKEClusterControlPlaneOptions, LKEClusterControlPlaneACLUpdateOptions, LKEClusterControlPlaneACLResponse

#### DELETE /{apiVersion}/lke/clusters/{clusterId}/nodes/{nodeId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `clusterId` (Required, type: `integer`)
- `nodeId` (Required, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `acl`
- `addresses`
- `apl_enabled`
- `assignments`
- `audit_logs_enabled`
- `autoscaler`
- `control_plane`
- `count`
- `description`
- `disk_encryption`
- `disks`
- `down`
- `effect`
- `enabled`
- `endpoint`
- `firewall_id`
- `high_availability`
- `id`
- `instance_id`
- `ipv4`
- `ipv6`
- `k8s_version`
- `key`
- `kubeconfig`
- `label`
- `labels`
- `max`
- `maximum`
- `min`
- `minimum`
- `node_pools`
- `nodes`
- `region`
- `requires_restart`
- `revision-id`
- `servicetoken`
- `size`
- `stack_type`
- `status`
- `subnet_id`
- `tags`
- `taints`
- `tier`
- `type`
- `up`
- `update_strategy`
- `url`
- `value`
- `vpc_id`

*Related structs analyzed*: LKECluster, LKEClusterCreateOptions, LKEClusterUpdateOptions, LKEClusterAPIEndpoint, LKEClusterKubeconfig, LKEClusterDashboard, LKEVersion, LKETierVersion, LKEClusterRegenerateOptions, LKENodePoolDisk, LKENodePoolAutoscaler, LKENodePoolLinode, LKENodePoolTaint, LKENodePool, LKENodePoolCreateOptions, LKENodePoolUpdateOptions, MaxSlotWALKeepSize, LKEClusterControlPlane, LKEClusterControlPlaneACLAddresses, LKEClusterControlPlaneACL, LKEClusterControlPlaneACLAddressesOptions, LKEClusterControlPlaneACLOptions, LKEClusterControlPlaneOptions, LKEClusterControlPlaneACLUpdateOptions, LKEClusterControlPlaneACLResponse, NodeBalancerNodeStatus, LinodesAssignIPsOptions

#### DELETE /{apiVersion}/lke/clusters/{clusterId}/pools/{poolId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `clusterId` (Required, type: `integer`)
- `poolId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `acl`
- `addresses`
- `apl_enabled`
- `audit_logs_enabled`
- `autoscaler`
- `control_plane`
- `count`
- `description`
- `disk_encryption`
- `disks`
- `effect`
- `enabled`
- `endpoint`
- `firewall_id`
- `high_availability`
- `id`
- `instance_id`
- `ipv4`
- `ipv6`
- `k8s_version`
- `key`
- `kubeconfig`
- `label`
- `labels`
- `max`
- `maximum`
- `min`
- `minimum`
- `node_pools`
- `nodes`
- `region`
- `requires_restart`
- `revision-id`
- `servicetoken`
- `size`
- `stack_type`
- `status`
- `subnet_id`
- `tags`
- `taints`
- `tier`
- `type`
- `update_strategy`
- `url`
- `value`
- `vpc_id`

*Related structs analyzed*: LKECluster, LKEClusterCreateOptions, LKEClusterUpdateOptions, LKEClusterAPIEndpoint, LKEClusterKubeconfig, LKEClusterDashboard, LKEVersion, LKETierVersion, LKEClusterRegenerateOptions, LKENodePoolDisk, LKENodePoolAutoscaler, LKENodePoolLinode, LKENodePoolTaint, LKENodePool, LKENodePoolCreateOptions, LKENodePoolUpdateOptions, MaxSlotWALKeepSize, LKEClusterControlPlane, LKEClusterControlPlaneACLAddresses, LKEClusterControlPlaneACL, LKEClusterControlPlaneACLAddressesOptions, LKEClusterControlPlaneACLOptions, LKEClusterControlPlaneOptions, LKEClusterControlPlaneACLUpdateOptions, LKEClusterControlPlaneACLResponse

#### DELETE /{apiVersion}/lke/clusters/{clusterId}/servicetoken

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `clusterId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `acl`
- `addresses`
- `apl_enabled`
- `audit_logs_enabled`
- `autoscaler`
- `control_plane`
- `count`
- `description`
- `disk_encryption`
- `disks`
- `effect`
- `enabled`
- `endpoint`
- `firewall_id`
- `high_availability`
- `id`
- `instance_id`
- `ipv4`
- `ipv6`
- `k8s_version`
- `key`
- `kubeconfig`
- `label`
- `labels`
- `max`
- `maximum`
- `min`
- `minimum`
- `node_pools`
- `nodes`
- `region`
- `requires_restart`
- `revision-id`
- `servicetoken`
- `size`
- `stack_type`
- `status`
- `subnet_id`
- `tags`
- `taints`
- `tier`
- `token`
- `type`
- `update_strategy`
- `url`
- `value`
- `vpc_id`

*Related structs analyzed*: LKECluster, LKEClusterCreateOptions, LKEClusterUpdateOptions, LKEClusterAPIEndpoint, LKEClusterKubeconfig, LKEClusterDashboard, LKEVersion, LKETierVersion, LKEClusterRegenerateOptions, LKENodePoolDisk, LKENodePoolAutoscaler, LKENodePoolLinode, LKENodePoolTaint, LKENodePool, LKENodePoolCreateOptions, LKENodePoolUpdateOptions, MaxSlotWALKeepSize, LKEClusterControlPlane, LKEClusterControlPlaneACLAddresses, LKEClusterControlPlaneACL, LKEClusterControlPlaneACLAddressesOptions, LKEClusterControlPlaneACLOptions, LKEClusterControlPlaneOptions, LKEClusterControlPlaneACLUpdateOptions, LKEClusterControlPlaneACLResponse, MonitorServiceToken

#### DELETE /{apiVersion}/longview/clients/{clientId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `clientId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `apache`
- `api_key`
- `clients_included`
- `hourly`
- `id`
- `install_code`
- `label`
- `longview_subscription`
- `monthly`
- `mysql`
- `nginx`
- `price`
- `updated`

*Related structs analyzed*: LongviewClient, LongviewClientCreateOptions, LongviewClientUpdateOptions, LongviewPlan, LongviewPlanUpdateOptions, LongviewSubscription

#### DELETE /{apiVersion}/monitor/services/{serviceType}/alert-definitions/{alertId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `alertId` (Required, type: `integer`)
- `apiVersion` (Required, type: `enum[v4beta...]`)
- `serviceType` (Required, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `alert`
- `alerts`
- `available_aggregate_functions`
- `description`
- `dimension_label`
- `dimensions`
- `entity_ids`
- `evaluation_period_seconds`
- `example`
- `id`
- `is_alertable`
- `label`
- `maximum`
- `metric`
- `metric_type`
- `metrics`
- `minimum`
- `polling_interval_seconds`
- `requires_restart`
- `scope`
- `scrape_interval`
- `service_type`
- `token`
- `type`
- `unit`
- `values`
- `widgets`

*Related structs analyzed*: MonitorService, MonitorServiceAlert, MonitorMetricsDefinition, MonitorDimension, RegionMonitors, PGStatMonitorPGSMEnableQueryPlan, PGStatMonitorPGSMMaxBuckets, PostgresDatabaseConfigInfoPGStatMonitorEnable, MonitorDashboard, MonitorServiceToken, MonitorTokenCreateOptions

#### DELETE /{apiVersion}/networking/firewalls/{firewallId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `firewallId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `default_firewall_ids`

*Related structs analyzed*: FirewallSettings, FirewallSettingsUpdateOptions

#### DELETE /{apiVersion}/networking/firewalls/{firewallId}/devices/{deviceId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `deviceId` (Required, type: `integer`)
- `firewallId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `default_firewall_ids`
- `interfaces`
- `linodes`
- `nodebalancers`

*Related structs analyzed*: DevicesCreationOptions, FirewallSettings, FirewallSettingsUpdateOptions

#### DELETE /{apiVersion}/networking/ipv6/ranges/{range}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)

**Extra in SDK** (found in SDK but not documented in API):

- `address`
- `allocation_class`
- `global`
- `is_bgp`
- `is_public`
- `link_local`
- `linode_id`
- `linodes`
- `prefix`
- `prefix_length`
- `ranges`
- `region`
- `route_target`
- `shared`
- `slaac`
- `slaac_address`
- `vpc`

*Related structs analyzed*: VPCSubnetNodebalancersRanges, VPCSubnetCreateOptionsIPv6, PublicInterfaceIPv6, PublicInterfaceIPv6Range, PublicInterfaceIPv6SLAAC, VPCInterfaceIPv6, VPCInterfaceIPv6SLAAC, VPCInterfaceIPv6Range, PublicInterfaceIPv6CreateOptions, PublicInterfaceIPv6RangeCreateOptions, VPCInterfaceIPv6CreateOptions, VPCInterfaceIPv6SLAACCreateOptions, VPCInterfaceIPv6RangeCreateOptions, VPCIPv6Range, VPCCreateOptionsIPv6, IPv6RangeCreateOptions, VPCIPIPv6Address, InstanceIPv6Response, IPv6Range, InstanceConfigInterfaceIPv6, InstanceConfigInterfaceIPv6SLAAC, InstanceConfigInterfaceIPv6Range, InstanceConfigInterfaceCreateOptionsIPv6, InstanceConfigInterfaceCreateOptionsIPv6SLAAC, InstanceConfigInterfaceCreateOptionsIPv6Range, InstanceConfigInterfaceUpdateOptionsIPv6, InstanceConfigInterfaceUpdateOptionsIPv6SLAAC, InstanceConfigInterfaceUpdateOptionsIPv6Range

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

#### DELETE /{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId}/nodes/{nodeId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `configId` (Required, type: `integer`)
- `nodeBalancerId` (Required, type: `integer`)
- `nodeId` (Required, type: `string`)

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

#### DELETE /{apiVersion}/object-storage/buckets/{regionId}/{bucket}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `bucket` (Required, type: `string`)
- `regionId` (Required, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `description`
- `example`
- `maximum`
- `minimum`
- `requires_restart`
- `type`

*Related structs analyzed*: PGStatMonitorPGSMMaxBuckets

#### DELETE /{apiVersion}/object-storage/buckets/{regionId}/{bucket}/ssl

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `bucket` (Required, type: `string`)
- `regionId` (Required, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `ca_certificate`
- `description`
- `example`
- `maximum`
- `minimum`
- `requires_restart`
- `type`

*Related structs analyzed*: MySQLDatabaseSSL, PGStatMonitorPGSMMaxBuckets, PostgresDatabaseSSL

#### DELETE /{apiVersion}/object-storage/keys/{keyId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `keyId` (Required, type: `integer`)

#### DELETE /{apiVersion}/profile/apps/{appId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `appId` (Required, type: `integer`)

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

#### DELETE /{apiVersion}/profile/devices/{deviceId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `deviceId` (Required, type: `integer`)

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
- `interfaces`
- `ip`
- `ip_whitelist_enabled`
- `label`
- `last_remote_addr`
- `linodes`
- `lish_auth_method`
- `nodebalancers`
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

*Related structs analyzed*: ProfileReferrals, Profile, ProfileUpdateOptions, ProfileLogin, ProfileDevice, DevicesCreationOptions, ProfileApp

#### DELETE /{apiVersion}/profile/sshkeys/{sshKeyId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `sshKeyId` (Required, type: `integer`)

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

#### DELETE /{apiVersion}/profile/tokens/{tokenId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `tokenId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `authentication_type`
- `authorized_keys`
- `code`
- `completed`
- `credit`
- `datetime`
- `description`
- `email`
- `email_notifications`
- `example`
- `id`
- `ip`
- `ip_whitelist_enabled`
- `label`
- `last_remote_addr`
- `lish_auth_method`
- `maximum`
- `minimum`
- `pending`
- `referrals`
- `requires_restart`
- `restricted`
- `scopes`
- `status`
- `thumbnail_url`
- `timezone`
- `total`
- `two_factor_auth`
- `type`
- `uid`
- `url`
- `user_agent`
- `username`
- `verified_phone_number`
- `website`

*Related structs analyzed*: InnoDBFTMinTokenSize, ProfileReferrals, Profile, ProfileUpdateOptions, ProfileLogin, ProfileDevice, ProfileApp

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

#### GET /{apiVersion}/account/agreements

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

#### GET /{apiVersion}/account/availability/{regionId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `regionId` (Required, type: `string`)

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

#### GET /{apiVersion}/account/betas

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

#### GET /{apiVersion}/account/betas/{betaId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `betaId` (Required, type: `string`)

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

#### GET /{apiVersion}/account/events

**Missing in SDK** (documented in API but not found in SDK structs):

- `X-Filter` (Optional, type: `unknown`)
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

#### GET /{apiVersion}/account/events/{eventId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `eventId` (Required, type: `integer`)

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

#### GET /{apiVersion}/account/invoices

**Missing in SDK** (documented in API but not found in SDK structs):

- `X-Filter` (Optional, type: `unknown`)
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

#### GET /{apiVersion}/account/invoices/{invoiceId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `invoiceId` (Required, type: `integer`)

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

#### GET /{apiVersion}/account/logins

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

#### GET /{apiVersion}/account/logins/{loginId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `loginId` (Required, type: `integer`)

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

#### GET /{apiVersion}/account/maintenance

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
- `day_of_week`
- `description`
- `duration`
- `email`
- `entities`
- `entity`
- `entity_access`
- `eu_model`
- `euuid`
- `first_name`
- `frequency`
- `hour_of_day`
- `id`
- `interfaces_for_new_linodes`
- `is_default`
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
- `notification_period_sec`
- `object_storage`
- `pending`
- `phone`
- `privacy_policy`
- `quota`
- `reason`
- `region`
- `region_transfers`
- `roles`
- `slug`
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

*Related structs analyzed*: AccountMaintenance, AccountSettings, AccountSettingsUpdateOptions, DatabaseMaintenanceWindow, DatabaseMaintenanceWindowPending, AccountServiceTransfer, AccountServiceTransferEntity, AccountServiceTransferRequestOptions, Account, AccountUpdateOptions, AccountAgreements, AccountAgreementsUpdateOptions, AccountRolePermissions, AccountAccess, AccountTransfer, AccountTransferRegion, AccountAvailability, AccountBetaProgram, AccountBetaProgramCreateOpts, MaintenancePolicy

#### GET /{apiVersion}/account/notifications

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

#### GET /{apiVersion}/account/oauth-clients

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

#### GET /{apiVersion}/account/oauth-clients/{clientId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `clientId` (Required, type: `string`)

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

#### GET /{apiVersion}/account/payment-methods

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

#### GET /{apiVersion}/account/payment-methods/{paymentMethodId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `paymentMethodId` (Required, type: `integer`)

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

#### GET /{apiVersion}/account/payments

**Missing in SDK** (documented in API but not found in SDK structs):

- `X-Filter` (Optional, type: `unknown`)
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

#### GET /{apiVersion}/account/payments/{paymentId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `paymentId` (Required, type: `integer`)

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

#### GET /{apiVersion}/account/service-transfers

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

#### GET /{apiVersion}/account/service-transfers/{token}

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
- `type`
- `unavailable`
- `used`
- `when`
- `zip`

*Related structs analyzed*: AccountMaintenance, AccountSettings, AccountSettingsUpdateOptions, AccountServiceTransfer, AccountServiceTransferEntity, AccountServiceTransferRequestOptions, Account, AccountUpdateOptions, AccountAgreements, AccountAgreementsUpdateOptions, AccountRolePermissions, AccountAccess, AccountTransfer, AccountTransferRegion, AccountAvailability, AccountBetaProgram, AccountBetaProgramCreateOpts

#### GET /{apiVersion}/account/settings

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
- `default_firewall_ids`
- `default_route`
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

*Related structs analyzed*: AccountMaintenance, AccountSettings, AccountSettingsUpdateOptions, AccountServiceTransfer, AccountServiceTransferEntity, AccountServiceTransferRequestOptions, Account, AccountUpdateOptions, AccountAgreements, AccountAgreementsUpdateOptions, InterfaceSettings, InterfaceSettingsUpdateOptions, AccountRolePermissions, AccountAccess, AccountTransfer, AccountTransferRegion, AccountAvailability, FirewallSettings, FirewallSettingsUpdateOptions, AccountBetaProgram, AccountBetaProgramCreateOpts

#### GET /{apiVersion}/account/transfer

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
- `bytes_in`
- `bytes_out`
- `bytes_total`
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
- `in`
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
- `out`
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
- `total`
- `type`
- `unavailable`
- `used`
- `when`
- `zip`

*Related structs analyzed*: AccountMaintenance, AccountSettings, AccountSettingsUpdateOptions, AccountServiceTransfer, AccountServiceTransferEntity, AccountServiceTransferRequestOptions, ObjectStorageTransfer, Account, AccountUpdateOptions, AccountAgreements, AccountAgreementsUpdateOptions, AccountRolePermissions, AccountAccess, AccountTransfer, AccountTransferRegion, InstanceTransfer, MonthlyInstanceTransferStats, MonthlyInstanceTransferStatsV2, NodeBalancerTransfer, AccountAvailability, AccountBetaProgram, AccountBetaProgramCreateOpts

#### GET /{apiVersion}/account/users

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

#### GET /{apiVersion}/account/users/{username}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `username` (Required, type: `string`)

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

#### GET /{apiVersion}/account/users/{username}/grants

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `username` (Required, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `account_access`
- `active_promotions`
- `active_since`
- `add_databases`
- `add_domains`
- `add_firewalls`
- `add_images`
- `add_linodes`
- `add_longview`
- `add_nodebalancers`
- `add_stackscripts`
- `add_volumes`
- `add_vpcs`
- `address_1`
- `address_2`
- `available`
- `backups_enabled`
- `balance`
- `balance_uninvoiced`
- `billable`
- `billing_source`
- `cancel_account`
- `capabilities`
- `child_account_access`
- `city`
- `company`
- `country`
- `credit_card`
- `database`
- `description`
- `domain`
- `email`
- `entities`
- `entity`
- `entity_access`
- `eu_model`
- `euuid`
- `firewall`
- `first_name`
- `global`
- `id`
- `image`
- `interfaces_for_new_linodes`
- `is_sender`
- `label`
- `last_name`
- `linode`
- `linodes`
- `longview`
- `longview_subscription`
- `maintenance_policy`
- `maintenance_policy_set`
- `managed`
- `master_service_agreement`
- `network_helper`
- `nodebalancer`
- `object_storage`
- `phone`
- `placement_group`
- `privacy_policy`
- `quota`
- `reason`
- `region`
- `region_transfers`
- `roles`
- `source`
- `stackscript`
- `state`
- `status`
- `tax_id`
- `token`
- `type`
- `unavailable`
- `used`
- `volume`
- `vpc`
- `when`
- `zip`

*Related structs analyzed*: AccountMaintenance, GlobalUserGrants, UserGrants, UserGrantsUpdateOptions, AccountSettings, AccountSettingsUpdateOptions, AccountServiceTransfer, AccountServiceTransferEntity, AccountServiceTransferRequestOptions, Account, AccountUpdateOptions, AccountAgreements, AccountAgreementsUpdateOptions, AccountRolePermissions, AccountAccess, AccountTransfer, AccountTransferRegion, AccountAvailability, AccountBetaProgram, AccountBetaProgramCreateOpts

#### GET /{apiVersion}/betas

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

#### GET /{apiVersion}/betas/{betaId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `betaId` (Required, type: `string`)

#### GET /{apiVersion}/databases/engines

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `ca_certificate`

*Related structs analyzed*: MySQLDatabaseSSL, PostgresDatabaseSSL

#### GET /{apiVersion}/databases/engines/{engineId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `engineId` (Required, type: `string`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `ca_certificate`

*Related structs analyzed*: MySQLDatabaseSSL, PostgresDatabaseSSL

#### GET /{apiVersion}/databases/instances

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `available`
- `ca_certificate`
- `configs`
- `cpu`
- `data`
- `disk`
- `disks`
- `filesystem`
- `gpus`
- `id`
- `io`
- `label`
- `memory`
- `netv4`
- `netv6`
- `size`
- `status`
- `title`
- `transfer`
- `type`
- `vcpus`

*Related structs analyzed*: InstanceStatsData, InstanceStats, MySQLDatabaseSSL, PostgresDatabaseSSL, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec

#### GET /{apiVersion}/databases/mysql/config

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)

**Extra in SDK** (found in SDK but not documented in API):

- `acl`
- `acl_xml`
- `active`
- `address`
- `algorithm`
- `allow_list`
- `autovacuum_analyze_scale_factor`
- `autovacuum_analyze_threshold`
- `autovacuum_max_workers`
- `autovacuum_naptime`
- `autovacuum_vacuum_cost_delay`
- `autovacuum_vacuum_cost_limit`
- `autovacuum_vacuum_scale_factor`
- `autovacuum_vacuum_threshold`
- `bgwriter_delay`
- `bgwriter_flush_after`
- `bgwriter_lru_maxpages`
- `bgwriter_lru_multiplier`
- `binlog_retention_period`
- `ca_certificate`
- `check`
- `check_attempts`
- `check_body`
- `check_interval`
- `check_passive`
- `check_path`
- `check_timeout`
- `cipher_suite`
- `cluster_size`
- `comments`
- `connect_timeout`
- `deadlock_timeout`
- `default_time_zone`
- `default_toast_compression`
- `description`
- `devices`
- `devtmpfs_automount`
- `disk_id`
- `distro`
- `encrypted`
- `engine`
- `engine_config`
- `example`
- `fork`
- `group_concat_max_len`
- `helpers`
- `hosts`
- `id`
- `idle_in_transaction_session_timeout`
- `ids`
- `information_schema_stats_expiry`
- `init_rd`
- `innodb_change_buffer_max_size`
- `innodb_flush_neighbors`
- `innodb_ft_min_token_size`
- `innodb_ft_server_stopword_table`
- `innodb_lock_wait_timeout`
- `innodb_log_buffer_size`
- `innodb_online_alter_log_max_size`
- `innodb_read_io_threads`
- `innodb_rollback_on_timeout`
- `innodb_thread_concurrency`
- `innodb_write_io_threads`
- `interactive_timeout`
- `interfaces`
- `internal_tmp_mem_storage_engine`
- `ip_ranges`
- `ipam_address`
- `ipv4`
- `ipv4_range`
- `ipv6`
- `ipv6_range`
- `is_public`
- `jit`
- `kernel`
- `kubeconfig`
- `label`
- `max_allowed_packet`
- `max_failover_replication_time_lag`
- `max_files_per_process`
- `max_heap_table_size`
- `max_locks_per_transaction`
- `max_logical_replication_workers`
- `max_parallel_workers`
- `max_parallel_workers_per_gather`
- `max_pred_locks_per_transaction`
- `max_replication_slots`
- `max_slot_wal_keep_size`
- `max_stack_depth`
- `max_standby_archive_delay`
- `max_standby_streaming_delay`
- `max_wal_senders`
- `max_worker_processes`
- `maximum`
- `members`
- `memory_limit`
- `minimum`
- `modules_dep`
- `mysql`
- `name`
- `net_buffer_length`
- `net_read_timeout`
- `net_write_timeout`
- `network`
- `nodebalancer_id`
- `nodes`
- `nodes_status`
- `password`
- `password_encryption`
- `pg`
- `pg_partman_bgw.interval`
- `pg_partman_bgw.role`
- `pg_stat_monitor.pgsm_enable_query_plan`
- `pg_stat_monitor.pgsm_max_buckets`
- `pg_stat_monitor_enable`
- `pg_stat_statements.track`
- `pglookout`
- `platform`
- `port`
- `primary`
- `private_network`
- `protocol`
- `proxy_protocol`
- `purpose`
- `range`
- `ranges`
- `region`
- `requires_restart`
- `root_device`
- `run_level`
- `sda`
- `sdaa`
- `sdab`
- `sdac`
- `sdad`
- `sdae`
- `sdaf`
- `sdag`
- `sdah`
- `sdai`
- `sdaj`
- `sdak`
- `sdal`
- `sdam`
- `sdan`
- `sdao`
- `sdap`
- `sdaq`
- `sdar`
- `sdas`
- `sdat`
- `sdau`
- `sdav`
- `sdaw`
- `sdax`
- `sday`
- `sdaz`
- `sdb`
- `sdba`
- `sdbb`
- `sdbc`
- `sdbd`
- `sdbe`
- `sdbf`
- `sdbg`
- `sdbh`
- `sdbi`
- `sdbj`
- `sdbk`
- `sdbl`
- `sdc`
- `sdd`
- `sde`
- `sdf`
- `sdg`
- `sdh`
- `sdi`
- `sdj`
- `sdk`
- `sdl`
- `sdm`
- `sdn`
- `sdo`
- `sdp`
- `sdq`
- `sdr`
- `sds`
- `sdt`
- `sdu`
- `sdv`
- `sdw`
- `sdx`
- `sdy`
- `sdz`
- `shared_buffers_percentage`
- `slaac`
- `sort_buffer_size`
- `sql_mode`
- `sql_require_primary_key`
- `ssl_cert`
- `ssl_commonname`
- `ssl_connection`
- `ssl_fingerprint`
- `ssl_key`
- `status`
- `stickiness`
- `subnet_id`
- `temp_file_limit`
- `timezone`
- `tmp_table_size`
- `total_disk_size_gb`
- `track_activity_query_size`
- `track_commit_timestamp`
- `track_functions`
- `track_io_timing`
- `type`
- `udp_check_port`
- `udp_session_timeout`
- `updatedb_disabled`
- `updates`
- `used_disk_size_gb`
- `username`
- `version`
- `virt_mode`
- `volume_id`
- `vpc_id`
- `wait_timeout`
- `wal_sender_timeout`
- `wal_writer_delay`
- `work_mem`

*Related structs analyzed*: ObjectStorageObjectACLConfig, ObjectStorageObjectACLConfigV2, ObjectStorageObjectACLConfigUpdateOptions, MySQLDatabase, MySQLDatabaseEngineConfig, MySQLDatabaseEngineConfigMySQL, MySQLDatabaseConfigInfo, MySQLDatabaseConfigInfoMySQL, MySQLDatabaseConfigInfoBinlogRetentionPeriod, MySQLCreateOptions, MySQLUpdateOptions, MySQLDatabaseCredential, MySQLDatabaseSSL, LKEClusterKubeconfig, PostgresDatabaseEngineConfig, PostgresDatabaseEngineConfigPG, PostgresDatabaseEngineConfigPGLookout, PostgresDatabaseConfigInfo, PostgresDatabaseConfigInfoPG, PostgresDatabaseConfigInfoPGStatMonitorEnable, PostgresDatabaseConfigInfoPGLookout, PostgresDatabaseConfigInfoSharedBuffersPercentage, PostgresDatabaseConfigInfoWorkMem, PostgresDatabaseSSL, NodeBalancerVPCConfig, InstanceConfig, InstanceConfigDevice, InstanceConfigDeviceMap, InstanceConfigHelpers, InstanceConfigCreateOptions, InstanceConfigUpdateOptions, NodeBalancerConfig, NodeBalancerConfigCreateOptions, NodeBalancerConfigRebuildOptions, NodeBalancerConfigRebuildNodeOptions, InstanceConfigInterface, InstanceConfigInterfaceIPv6, InstanceConfigInterfaceIPv6SLAAC, InstanceConfigInterfaceIPv6Range, InstanceConfigInterfaceCreateOptions, InstanceConfigInterfaceCreateOptionsIPv6, InstanceConfigInterfaceCreateOptionsIPv6SLAAC, InstanceConfigInterfaceCreateOptionsIPv6Range, InstanceConfigInterfaceUpdateOptions, InstanceConfigInterfaceUpdateOptionsIPv6, InstanceConfigInterfaceUpdateOptionsIPv6SLAAC, InstanceConfigInterfaceUpdateOptionsIPv6Range, InstanceConfigInterfacesReorderOptions

#### GET /{apiVersion}/databases/mysql/instances

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `allow_list`
- `available`
- `binlog_retention_period`
- `ca_certificate`
- `cluster_size`
- `configs`
- `connect_timeout`
- `cpu`
- `data`
- `default_time_zone`
- `description`
- `disk`
- `disks`
- `encrypted`
- `engine`
- `engine_config`
- `example`
- `filesystem`
- `fork`
- `gpus`
- `group_concat_max_len`
- `hosts`
- `id`
- `information_schema_stats_expiry`
- `innodb_change_buffer_max_size`
- `innodb_flush_neighbors`
- `innodb_ft_min_token_size`
- `innodb_ft_server_stopword_table`
- `innodb_lock_wait_timeout`
- `innodb_log_buffer_size`
- `innodb_online_alter_log_max_size`
- `innodb_read_io_threads`
- `innodb_rollback_on_timeout`
- `innodb_thread_concurrency`
- `innodb_write_io_threads`
- `interactive_timeout`
- `internal_tmp_mem_storage_engine`
- `io`
- `label`
- `max_allowed_packet`
- `max_heap_table_size`
- `maximum`
- `members`
- `memory`
- `minimum`
- `mysql`
- `net_buffer_length`
- `net_read_timeout`
- `net_write_timeout`
- `netv4`
- `netv6`
- `password`
- `platform`
- `port`
- `private_network`
- `region`
- `requires_restart`
- `size`
- `sort_buffer_size`
- `sql_mode`
- `sql_require_primary_key`
- `ssl_connection`
- `status`
- `title`
- `tmp_table_size`
- `total_disk_size_gb`
- `transfer`
- `type`
- `updates`
- `used_disk_size_gb`
- `username`
- `vcpus`
- `version`
- `wait_timeout`

*Related structs analyzed*: InstanceStatsData, InstanceStats, MySQLDatabase, MySQLDatabaseEngineConfig, MySQLDatabaseEngineConfigMySQL, MySQLDatabaseConfigInfo, MySQLDatabaseConfigInfoMySQL, MySQLDatabaseConfigInfoBinlogRetentionPeriod, MySQLCreateOptions, MySQLUpdateOptions, MySQLDatabaseCredential, MySQLDatabaseSSL, PostgresDatabaseSSL, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec

#### GET /{apiVersion}/databases/mysql/instances/{instanceId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `instanceId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `allow_list`
- `available`
- `binlog_retention_period`
- `ca_certificate`
- `cluster_size`
- `configs`
- `connect_timeout`
- `cpu`
- `data`
- `default_time_zone`
- `description`
- `disk`
- `disks`
- `encrypted`
- `engine`
- `engine_config`
- `example`
- `filesystem`
- `fork`
- `gpus`
- `group_concat_max_len`
- `hosts`
- `id`
- `information_schema_stats_expiry`
- `innodb_change_buffer_max_size`
- `innodb_flush_neighbors`
- `innodb_ft_min_token_size`
- `innodb_ft_server_stopword_table`
- `innodb_lock_wait_timeout`
- `innodb_log_buffer_size`
- `innodb_online_alter_log_max_size`
- `innodb_read_io_threads`
- `innodb_rollback_on_timeout`
- `innodb_thread_concurrency`
- `innodb_write_io_threads`
- `interactive_timeout`
- `internal_tmp_mem_storage_engine`
- `io`
- `label`
- `max_allowed_packet`
- `max_heap_table_size`
- `maximum`
- `members`
- `memory`
- `minimum`
- `mysql`
- `net_buffer_length`
- `net_read_timeout`
- `net_write_timeout`
- `netv4`
- `netv6`
- `password`
- `platform`
- `port`
- `private_network`
- `region`
- `requires_restart`
- `size`
- `sort_buffer_size`
- `sql_mode`
- `sql_require_primary_key`
- `ssl_connection`
- `status`
- `title`
- `tmp_table_size`
- `total_disk_size_gb`
- `transfer`
- `type`
- `updates`
- `used_disk_size_gb`
- `username`
- `vcpus`
- `version`
- `wait_timeout`

*Related structs analyzed*: InstanceStatsData, InstanceStats, MySQLDatabase, MySQLDatabaseEngineConfig, MySQLDatabaseEngineConfigMySQL, MySQLDatabaseConfigInfo, MySQLDatabaseConfigInfoMySQL, MySQLDatabaseConfigInfoBinlogRetentionPeriod, MySQLCreateOptions, MySQLUpdateOptions, MySQLDatabaseCredential, MySQLDatabaseSSL, PostgresDatabaseSSL, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec

#### GET /{apiVersion}/databases/mysql/instances/{instanceId}/credentials

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `instanceId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `allow_list`
- `available`
- `binlog_retention_period`
- `ca_certificate`
- `cluster_size`
- `configs`
- `connect_timeout`
- `cpu`
- `data`
- `default_time_zone`
- `description`
- `disk`
- `disks`
- `encrypted`
- `engine`
- `engine_config`
- `example`
- `filesystem`
- `fork`
- `gpus`
- `group_concat_max_len`
- `hosts`
- `id`
- `information_schema_stats_expiry`
- `innodb_change_buffer_max_size`
- `innodb_flush_neighbors`
- `innodb_ft_min_token_size`
- `innodb_ft_server_stopword_table`
- `innodb_lock_wait_timeout`
- `innodb_log_buffer_size`
- `innodb_online_alter_log_max_size`
- `innodb_read_io_threads`
- `innodb_rollback_on_timeout`
- `innodb_thread_concurrency`
- `innodb_write_io_threads`
- `interactive_timeout`
- `internal_tmp_mem_storage_engine`
- `io`
- `label`
- `max_allowed_packet`
- `max_heap_table_size`
- `maximum`
- `members`
- `memory`
- `minimum`
- `mysql`
- `net_buffer_length`
- `net_read_timeout`
- `net_write_timeout`
- `netv4`
- `netv6`
- `password`
- `platform`
- `port`
- `private_network`
- `region`
- `requires_restart`
- `size`
- `sort_buffer_size`
- `sql_mode`
- `sql_require_primary_key`
- `ssl_connection`
- `status`
- `title`
- `tmp_table_size`
- `total_disk_size_gb`
- `transfer`
- `type`
- `updates`
- `used_disk_size_gb`
- `username`
- `vcpus`
- `version`
- `wait_timeout`

*Related structs analyzed*: InstanceStatsData, InstanceStats, MySQLDatabase, MySQLDatabaseEngineConfig, MySQLDatabaseEngineConfigMySQL, MySQLDatabaseConfigInfo, MySQLDatabaseConfigInfoMySQL, MySQLDatabaseConfigInfoBinlogRetentionPeriod, MySQLCreateOptions, MySQLUpdateOptions, MySQLDatabaseCredential, MySQLDatabaseSSL, PostgresDatabaseSSL, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec

#### GET /{apiVersion}/databases/mysql/instances/{instanceId}/ssl

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `instanceId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `allow_list`
- `available`
- `binlog_retention_period`
- `ca_certificate`
- `cluster_size`
- `configs`
- `connect_timeout`
- `cpu`
- `data`
- `default_time_zone`
- `description`
- `disk`
- `disks`
- `encrypted`
- `engine`
- `engine_config`
- `example`
- `filesystem`
- `fork`
- `gpus`
- `group_concat_max_len`
- `hosts`
- `id`
- `information_schema_stats_expiry`
- `innodb_change_buffer_max_size`
- `innodb_flush_neighbors`
- `innodb_ft_min_token_size`
- `innodb_ft_server_stopword_table`
- `innodb_lock_wait_timeout`
- `innodb_log_buffer_size`
- `innodb_online_alter_log_max_size`
- `innodb_read_io_threads`
- `innodb_rollback_on_timeout`
- `innodb_thread_concurrency`
- `innodb_write_io_threads`
- `interactive_timeout`
- `internal_tmp_mem_storage_engine`
- `io`
- `label`
- `max_allowed_packet`
- `max_heap_table_size`
- `maximum`
- `members`
- `memory`
- `minimum`
- `mysql`
- `net_buffer_length`
- `net_read_timeout`
- `net_write_timeout`
- `netv4`
- `netv6`
- `password`
- `platform`
- `port`
- `private_network`
- `region`
- `requires_restart`
- `size`
- `sort_buffer_size`
- `sql_mode`
- `sql_require_primary_key`
- `ssl_connection`
- `status`
- `title`
- `tmp_table_size`
- `total_disk_size_gb`
- `transfer`
- `type`
- `updates`
- `used_disk_size_gb`
- `username`
- `vcpus`
- `version`
- `wait_timeout`

*Related structs analyzed*: InstanceStatsData, InstanceStats, MySQLDatabase, MySQLDatabaseEngineConfig, MySQLDatabaseEngineConfigMySQL, MySQLDatabaseConfigInfo, MySQLDatabaseConfigInfoMySQL, MySQLDatabaseConfigInfoBinlogRetentionPeriod, MySQLCreateOptions, MySQLUpdateOptions, MySQLDatabaseCredential, MySQLDatabaseSSL, PostgresDatabaseSSL, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec

#### GET /{apiVersion}/databases/postgresql/config

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)

**Extra in SDK** (found in SDK but not documented in API):

- `acl`
- `acl_xml`
- `active`
- `address`
- `algorithm`
- `autovacuum_analyze_scale_factor`
- `autovacuum_analyze_threshold`
- `autovacuum_max_workers`
- `autovacuum_naptime`
- `autovacuum_vacuum_cost_delay`
- `autovacuum_vacuum_cost_limit`
- `autovacuum_vacuum_scale_factor`
- `autovacuum_vacuum_threshold`
- `bgwriter_delay`
- `bgwriter_flush_after`
- `bgwriter_lru_maxpages`
- `bgwriter_lru_multiplier`
- `binlog_retention_period`
- `ca_certificate`
- `check`
- `check_attempts`
- `check_body`
- `check_interval`
- `check_passive`
- `check_path`
- `check_timeout`
- `cipher_suite`
- `comments`
- `connect_timeout`
- `deadlock_timeout`
- `default_time_zone`
- `default_toast_compression`
- `description`
- `devices`
- `devtmpfs_automount`
- `disk_id`
- `distro`
- `example`
- `group_concat_max_len`
- `helpers`
- `id`
- `idle_in_transaction_session_timeout`
- `ids`
- `information_schema_stats_expiry`
- `init_rd`
- `innodb_change_buffer_max_size`
- `innodb_flush_neighbors`
- `innodb_ft_min_token_size`
- `innodb_ft_server_stopword_table`
- `innodb_lock_wait_timeout`
- `innodb_log_buffer_size`
- `innodb_online_alter_log_max_size`
- `innodb_read_io_threads`
- `innodb_rollback_on_timeout`
- `innodb_thread_concurrency`
- `innodb_write_io_threads`
- `interactive_timeout`
- `interfaces`
- `internal_tmp_mem_storage_engine`
- `ip_ranges`
- `ipam_address`
- `ipv4`
- `ipv4_range`
- `ipv6`
- `ipv6_range`
- `is_public`
- `jit`
- `kernel`
- `kubeconfig`
- `label`
- `max_allowed_packet`
- `max_failover_replication_time_lag`
- `max_files_per_process`
- `max_heap_table_size`
- `max_locks_per_transaction`
- `max_logical_replication_workers`
- `max_parallel_workers`
- `max_parallel_workers_per_gather`
- `max_pred_locks_per_transaction`
- `max_replication_slots`
- `max_slot_wal_keep_size`
- `max_stack_depth`
- `max_standby_archive_delay`
- `max_standby_streaming_delay`
- `max_wal_senders`
- `max_worker_processes`
- `maximum`
- `memory_limit`
- `minimum`
- `modules_dep`
- `mysql`
- `name`
- `net_buffer_length`
- `net_read_timeout`
- `net_write_timeout`
- `network`
- `nodebalancer_id`
- `nodes`
- `nodes_status`
- `password_encryption`
- `pg`
- `pg_partman_bgw.interval`
- `pg_partman_bgw.role`
- `pg_stat_monitor.pgsm_enable_query_plan`
- `pg_stat_monitor.pgsm_max_buckets`
- `pg_stat_monitor_enable`
- `pg_stat_statements.track`
- `pglookout`
- `port`
- `primary`
- `protocol`
- `proxy_protocol`
- `purpose`
- `range`
- `ranges`
- `requires_restart`
- `root_device`
- `run_level`
- `sda`
- `sdaa`
- `sdab`
- `sdac`
- `sdad`
- `sdae`
- `sdaf`
- `sdag`
- `sdah`
- `sdai`
- `sdaj`
- `sdak`
- `sdal`
- `sdam`
- `sdan`
- `sdao`
- `sdap`
- `sdaq`
- `sdar`
- `sdas`
- `sdat`
- `sdau`
- `sdav`
- `sdaw`
- `sdax`
- `sday`
- `sdaz`
- `sdb`
- `sdba`
- `sdbb`
- `sdbc`
- `sdbd`
- `sdbe`
- `sdbf`
- `sdbg`
- `sdbh`
- `sdbi`
- `sdbj`
- `sdbk`
- `sdbl`
- `sdc`
- `sdd`
- `sde`
- `sdf`
- `sdg`
- `sdh`
- `sdi`
- `sdj`
- `sdk`
- `sdl`
- `sdm`
- `sdn`
- `sdo`
- `sdp`
- `sdq`
- `sdr`
- `sds`
- `sdt`
- `sdu`
- `sdv`
- `sdw`
- `sdx`
- `sdy`
- `sdz`
- `shared_buffers_percentage`
- `slaac`
- `sort_buffer_size`
- `sql_mode`
- `sql_require_primary_key`
- `ssl_cert`
- `ssl_commonname`
- `ssl_fingerprint`
- `ssl_key`
- `stickiness`
- `subnet_id`
- `temp_file_limit`
- `timezone`
- `tmp_table_size`
- `track_activity_query_size`
- `track_commit_timestamp`
- `track_functions`
- `track_io_timing`
- `type`
- `udp_check_port`
- `udp_session_timeout`
- `updatedb_disabled`
- `virt_mode`
- `volume_id`
- `vpc_id`
- `wait_timeout`
- `wal_sender_timeout`
- `wal_writer_delay`
- `work_mem`

*Related structs analyzed*: ObjectStorageObjectACLConfig, ObjectStorageObjectACLConfigV2, ObjectStorageObjectACLConfigUpdateOptions, MySQLDatabaseEngineConfig, MySQLDatabaseEngineConfigMySQL, MySQLDatabaseConfigInfo, MySQLDatabaseConfigInfoMySQL, MySQLDatabaseConfigInfoBinlogRetentionPeriod, MySQLDatabaseSSL, LKEClusterKubeconfig, PostgresDatabaseEngineConfig, PostgresDatabaseEngineConfigPG, PostgresDatabaseEngineConfigPGLookout, PostgresDatabaseConfigInfo, PostgresDatabaseConfigInfoPG, PostgresDatabaseConfigInfoPGStatMonitorEnable, PostgresDatabaseConfigInfoPGLookout, PostgresDatabaseConfigInfoSharedBuffersPercentage, PostgresDatabaseConfigInfoWorkMem, PostgresDatabaseSSL, NodeBalancerVPCConfig, InstanceConfig, InstanceConfigDevice, InstanceConfigDeviceMap, InstanceConfigHelpers, InstanceConfigCreateOptions, InstanceConfigUpdateOptions, NodeBalancerConfig, NodeBalancerConfigCreateOptions, NodeBalancerConfigRebuildOptions, NodeBalancerConfigRebuildNodeOptions, InstanceConfigInterface, InstanceConfigInterfaceIPv6, InstanceConfigInterfaceIPv6SLAAC, InstanceConfigInterfaceIPv6Range, InstanceConfigInterfaceCreateOptions, InstanceConfigInterfaceCreateOptionsIPv6, InstanceConfigInterfaceCreateOptionsIPv6SLAAC, InstanceConfigInterfaceCreateOptionsIPv6Range, InstanceConfigInterfaceUpdateOptions, InstanceConfigInterfaceUpdateOptionsIPv6, InstanceConfigInterfaceUpdateOptionsIPv6SLAAC, InstanceConfigInterfaceUpdateOptionsIPv6Range, InstanceConfigInterfacesReorderOptions

#### GET /{apiVersion}/databases/postgresql/instances

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `available`
- `ca_certificate`
- `configs`
- `cpu`
- `data`
- `disk`
- `disks`
- `filesystem`
- `gpus`
- `id`
- `io`
- `label`
- `memory`
- `netv4`
- `netv6`
- `size`
- `status`
- `title`
- `transfer`
- `type`
- `vcpus`

*Related structs analyzed*: InstanceStatsData, InstanceStats, MySQLDatabaseSSL, PostgresDatabaseSSL, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec

#### GET /{apiVersion}/databases/postgresql/instances/{instanceId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `instanceId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `available`
- `ca_certificate`
- `configs`
- `cpu`
- `data`
- `disk`
- `disks`
- `filesystem`
- `gpus`
- `id`
- `io`
- `label`
- `memory`
- `netv4`
- `netv6`
- `size`
- `status`
- `title`
- `transfer`
- `type`
- `vcpus`

*Related structs analyzed*: InstanceStatsData, InstanceStats, MySQLDatabaseSSL, PostgresDatabaseSSL, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec

#### GET /{apiVersion}/databases/postgresql/instances/{instanceId}/credentials

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `instanceId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `available`
- `ca_certificate`
- `configs`
- `cpu`
- `data`
- `disk`
- `disks`
- `filesystem`
- `gpus`
- `id`
- `io`
- `label`
- `memory`
- `netv4`
- `netv6`
- `size`
- `status`
- `title`
- `transfer`
- `type`
- `vcpus`

*Related structs analyzed*: InstanceStatsData, InstanceStats, MySQLDatabaseSSL, PostgresDatabaseSSL, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec

#### GET /{apiVersion}/databases/postgresql/instances/{instanceId}/ssl

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `instanceId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `available`
- `ca_certificate`
- `configs`
- `cpu`
- `data`
- `disk`
- `disks`
- `filesystem`
- `gpus`
- `id`
- `io`
- `label`
- `memory`
- `netv4`
- `netv6`
- `size`
- `status`
- `title`
- `transfer`
- `type`
- `vcpus`

*Related structs analyzed*: InstanceStatsData, InstanceStats, MySQLDatabaseSSL, PostgresDatabaseSSL, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec

#### GET /{apiVersion}/databases/types

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `ca_certificate`

*Related structs analyzed*: MySQLDatabaseSSL, PostgresDatabaseSSL

#### GET /{apiVersion}/databases/types/{typeId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)
- `typeId` (Required, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `ca_certificate`

*Related structs analyzed*: MySQLDatabaseSSL, PostgresDatabaseSSL

#### GET /{apiVersion}/domains

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

#### GET /{apiVersion}/domains/{domainId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `domainId` (Required, type: `integer`)

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

#### GET /{apiVersion}/iam/role-permissions

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4...]`)

#### GET /{apiVersion}/linode/instances

**Missing in SDK** (documented in API but not found in SDK structs):

- `X-Filter` (Optional, type: `unknown`)
- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### GET /{apiVersion}/linode/instances/{linodeId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### GET /{apiVersion}/linode/instances/{linodeId}/backups

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `automatic`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `current`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `in_progress`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `snapshot`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceBackupsResponse, InstanceBackupSnapshotResponse, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### GET /{apiVersion}/linode/instances/{linodeId}/backups/{backupId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `backupId` (Required, type: `integer`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `automatic`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `current`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `in_progress`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `snapshot`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceBackupsResponse, InstanceBackupSnapshotResponse, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### GET /{apiVersion}/linode/instances/{linodeId}/configs/{configId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `configId` (Required, type: `integer`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### GET /{apiVersion}/linode/instances/{linodeId}/disks/{diskId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `diskId` (Required, type: `integer`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### GET /{apiVersion}/linode/instances/{linodeId}/interfaces

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `ids`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_helper`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InterfaceSettings, InterfaceSettingsUpdateOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel, InstanceConfigInterfacesReorderOptions

#### GET /{apiVersion}/linode/instances/{linodeId}/interfaces/history

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `ids`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_helper`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InterfaceSettings, InterfaceSettingsUpdateOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel, InstanceConfigInterfacesReorderOptions

#### GET /{apiVersion}/linode/instances/{linodeId}/interfaces/settings

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `backups_enabled`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_firewall_ids`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `ids`
- `instance_id`
- `interfaces`
- `interfaces_for_new_linodes`
- `io`
- `kvm`
- `label`
- `linode_id`
- `longview_subscription`
- `mac_address`
- `maintenance_policy`
- `managed`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_helper`
- `network_out`
- `object_storage`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: AccountSettings, AccountSettingsUpdateOptions, InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InterfaceSettings, InterfaceSettingsUpdateOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, FirewallSettings, FirewallSettingsUpdateOptions, LinodeKernel, InstanceConfigInterfacesReorderOptions

#### GET /{apiVersion}/linode/instances/{linodeId}/interfaces/{interfaceId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `interfaceId` (Required, type: `integer`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `ids`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_helper`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InterfaceSettings, InterfaceSettingsUpdateOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel, InstanceConfigInterfacesReorderOptions

#### GET /{apiVersion}/linode/instances/{linodeId}/interfaces/{interfaceId}/firewalls

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `interfaceId` (Required, type: `integer`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_firewall_ids`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `ids`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_helper`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InterfaceSettings, InterfaceSettingsUpdateOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, FirewallSettings, FirewallSettingsUpdateOptions, LinodeKernel, InstanceConfigInterfacesReorderOptions

#### GET /{apiVersion}/linode/instances/{linodeId}/ips

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### GET /{apiVersion}/linode/instances/{linodeId}/ips/{address}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### GET /{apiVersion}/linode/instances/{linodeId}/stats

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `bytes_in`
- `bytes_out`
- `bytes_total`
- `class`
- `config_id`
- `configs`
- `connections`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `description`
- `disk`
- `disks`
- `dry_run`
- `enum`
- `example`
- `executionTimeMsec`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `in`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `maximum`
- `memory`
- `minimum`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `out`
- `price`
- `private_in`
- `private_out`
- `public`
- `pvops`
- `region`
- `region_prices`
- `requires_restart`
- `seriesFetched`
- `size`
- `status`
- `successor`
- `swap`
- `title`
- `traffic`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: StatsNet, StatsIO, InstanceStatsData, InstanceStats, InformationSchemaStatsExpiry, VPCSubnetLinodeInterface, VPCSubnetLinode, NodeBalancerStats, NodeBalancerStatsData, StatsTraffic, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, PGStatStatementsTrack, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, MonthlyInstanceTransferStats, MonthlyInstanceTransferStatsV2, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, EntityMetricsStats, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### GET /{apiVersion}/linode/instances/{linodeId}/stats/{year}/{month}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `linodeId` (Required, type: `integer`)
- `month` (Required, type: `integer`)
- `year` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `bytes_in`
- `bytes_out`
- `bytes_total`
- `class`
- `config_id`
- `configs`
- `connections`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `description`
- `disk`
- `disks`
- `dry_run`
- `enum`
- `example`
- `executionTimeMsec`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `in`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `maximum`
- `memory`
- `minimum`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `out`
- `price`
- `private_in`
- `private_out`
- `public`
- `pvops`
- `region`
- `region_prices`
- `requires_restart`
- `seriesFetched`
- `size`
- `status`
- `successor`
- `swap`
- `title`
- `traffic`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: StatsNet, StatsIO, InstanceStatsData, InstanceStats, InformationSchemaStatsExpiry, VPCSubnetLinodeInterface, VPCSubnetLinode, NodeBalancerStats, NodeBalancerStatsData, StatsTraffic, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, PGStatStatementsTrack, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, MonthlyInstanceTransferStats, MonthlyInstanceTransferStatsV2, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, EntityMetricsStats, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### GET /{apiVersion}/linode/instances/{linodeId}/transfer

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `billable`
- `bytes_in`
- `bytes_out`
- `bytes_total`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `entities`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `in`
- `instance_id`
- `interfaces`
- `io`
- `is_sender`
- `kvm`
- `label`
- `linode_id`
- `linodes`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `out`
- `price`
- `public`
- `pvops`
- `quota`
- `region`
- `region_prices`
- `region_transfers`
- `size`
- `status`
- `successor`
- `title`
- `token`
- `total`
- `transfer`
- `type`
- `used`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, AccountServiceTransfer, AccountServiceTransferEntity, AccountServiceTransferRequestOptions, ObjectStorageTransfer, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceSnapshot, InstanceSnapshotDisk, AccountTransfer, AccountTransferRegion, InstanceSpec, InstanceTransfer, MonthlyInstanceTransferStats, MonthlyInstanceTransferStatsV2, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, NodeBalancerTransfer, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### GET /{apiVersion}/linode/instances/{linodeId}/transfer/{year}/{month}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `linodeId` (Required, type: `integer`)
- `month` (Required, type: `integer`)
- `year` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `billable`
- `bytes_in`
- `bytes_out`
- `bytes_total`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `entities`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `in`
- `instance_id`
- `interfaces`
- `io`
- `is_sender`
- `kvm`
- `label`
- `linode_id`
- `linodes`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `out`
- `price`
- `public`
- `pvops`
- `quota`
- `region`
- `region_prices`
- `region_transfers`
- `size`
- `status`
- `successor`
- `title`
- `token`
- `total`
- `transfer`
- `type`
- `used`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, AccountServiceTransfer, AccountServiceTransferEntity, AccountServiceTransferRequestOptions, ObjectStorageTransfer, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceSnapshot, InstanceSnapshotDisk, AccountTransfer, AccountTransferRegion, InstanceSpec, InstanceTransfer, MonthlyInstanceTransferStats, MonthlyInstanceTransferStatsV2, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, NodeBalancerTransfer, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### GET /{apiVersion}/linode/kernels

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `backups`
- `class`
- `config_id`
- `default_route`
- `deprecated`
- `disk`
- `dry_run`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `instance_id`
- `interfaces`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `status`
- `successor`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### GET /{apiVersion}/linode/kernels/{kernelId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `kernelId` (Required, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `backups`
- `class`
- `config_id`
- `default_route`
- `deprecated`
- `disk`
- `dry_run`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `instance_id`
- `interfaces`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `status`
- `successor`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### GET /{apiVersion}/linode/stackscripts

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `backups`
- `class`
- `config_id`
- `default_route`
- `deprecated`
- `disk`
- `dry_run`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `instance_id`
- `interfaces`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `status`
- `successor`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### GET /{apiVersion}/linode/stackscripts/{stackscriptId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `stackscriptId` (Required, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `backups`
- `class`
- `config_id`
- `default_route`
- `deprecated`
- `disk`
- `dry_run`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `instance_id`
- `interfaces`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `status`
- `successor`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### GET /{apiVersion}/linode/types/{typeId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `typeId` (Required, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `backups`
- `class`
- `config_id`
- `default_route`
- `deprecated`
- `disk`
- `dry_run`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `instance_id`
- `interfaces`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `status`
- `successor`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### GET /{apiVersion}/lke/clusters

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)

**Extra in SDK** (found in SDK but not documented in API):

- `acl`
- `addresses`
- `apl_enabled`
- `audit_logs_enabled`
- `autoscaler`
- `control_plane`
- `count`
- `description`
- `disk_encryption`
- `disks`
- `effect`
- `enabled`
- `endpoint`
- `firewall_id`
- `high_availability`
- `id`
- `instance_id`
- `ipv4`
- `ipv6`
- `k8s_version`
- `key`
- `kubeconfig`
- `label`
- `labels`
- `max`
- `maximum`
- `min`
- `minimum`
- `node_pools`
- `nodes`
- `region`
- `requires_restart`
- `revision-id`
- `servicetoken`
- `size`
- `stack_type`
- `status`
- `subnet_id`
- `tags`
- `taints`
- `tier`
- `type`
- `update_strategy`
- `url`
- `value`
- `vpc_id`

*Related structs analyzed*: LKECluster, LKEClusterCreateOptions, LKEClusterUpdateOptions, LKEClusterAPIEndpoint, LKEClusterKubeconfig, LKEClusterDashboard, LKEVersion, LKETierVersion, LKEClusterRegenerateOptions, LKENodePoolDisk, LKENodePoolAutoscaler, LKENodePoolLinode, LKENodePoolTaint, LKENodePool, LKENodePoolCreateOptions, LKENodePoolUpdateOptions, MaxSlotWALKeepSize, LKEClusterControlPlane, LKEClusterControlPlaneACLAddresses, LKEClusterControlPlaneACL, LKEClusterControlPlaneACLAddressesOptions, LKEClusterControlPlaneACLOptions, LKEClusterControlPlaneOptions, LKEClusterControlPlaneACLUpdateOptions, LKEClusterControlPlaneACLResponse

#### GET /{apiVersion}/lke/clusters/{clusterId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `clusterId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `acl`
- `addresses`
- `apl_enabled`
- `audit_logs_enabled`
- `autoscaler`
- `control_plane`
- `count`
- `description`
- `disk_encryption`
- `disks`
- `effect`
- `enabled`
- `endpoint`
- `firewall_id`
- `high_availability`
- `id`
- `instance_id`
- `ipv4`
- `ipv6`
- `k8s_version`
- `key`
- `kubeconfig`
- `label`
- `labels`
- `max`
- `maximum`
- `min`
- `minimum`
- `node_pools`
- `nodes`
- `region`
- `requires_restart`
- `revision-id`
- `servicetoken`
- `size`
- `stack_type`
- `status`
- `subnet_id`
- `tags`
- `taints`
- `tier`
- `type`
- `update_strategy`
- `url`
- `value`
- `vpc_id`

*Related structs analyzed*: LKECluster, LKEClusterCreateOptions, LKEClusterUpdateOptions, LKEClusterAPIEndpoint, LKEClusterKubeconfig, LKEClusterDashboard, LKEVersion, LKETierVersion, LKEClusterRegenerateOptions, LKENodePoolDisk, LKENodePoolAutoscaler, LKENodePoolLinode, LKENodePoolTaint, LKENodePool, LKENodePoolCreateOptions, LKENodePoolUpdateOptions, MaxSlotWALKeepSize, LKEClusterControlPlane, LKEClusterControlPlaneACLAddresses, LKEClusterControlPlaneACL, LKEClusterControlPlaneACLAddressesOptions, LKEClusterControlPlaneACLOptions, LKEClusterControlPlaneOptions, LKEClusterControlPlaneACLUpdateOptions, LKEClusterControlPlaneACLResponse

#### GET /{apiVersion}/lke/clusters/{clusterId}/dashboard

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `clusterId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `acl`
- `addresses`
- `aggregate_function`
- `apl_enabled`
- `audit_logs_enabled`
- `autoscaler`
- `chart_type`
- `color`
- `control_plane`
- `count`
- `description`
- `dimension_label`
- `disk_encryption`
- `disks`
- `effect`
- `enabled`
- `endpoint`
- `filters`
- `firewall_id`
- `group_by`
- `high_availability`
- `id`
- `instance_id`
- `ipv4`
- `ipv6`
- `k8s_version`
- `key`
- `kubeconfig`
- `label`
- `labels`
- `max`
- `maximum`
- `metric`
- `min`
- `minimum`
- `node_pools`
- `nodes`
- `operator`
- `region`
- `requires_restart`
- `revision-id`
- `service_type`
- `servicetoken`
- `size`
- `stack_type`
- `status`
- `subnet_id`
- `tags`
- `taints`
- `tier`
- `type`
- `unit`
- `update_strategy`
- `url`
- `value`
- `vpc_id`
- `widgets`
- `y_label`

*Related structs analyzed*: LKECluster, LKEClusterCreateOptions, LKEClusterUpdateOptions, LKEClusterAPIEndpoint, LKEClusterKubeconfig, LKEClusterDashboard, LKEVersion, LKETierVersion, LKEClusterRegenerateOptions, LKENodePoolDisk, LKENodePoolAutoscaler, LKENodePoolLinode, LKENodePoolTaint, LKENodePool, LKENodePoolCreateOptions, LKENodePoolUpdateOptions, MaxSlotWALKeepSize, LKEClusterControlPlane, LKEClusterControlPlaneACLAddresses, LKEClusterControlPlaneACL, LKEClusterControlPlaneACLAddressesOptions, LKEClusterControlPlaneACLOptions, LKEClusterControlPlaneOptions, LKEClusterControlPlaneACLUpdateOptions, LKEClusterControlPlaneACLResponse, MonitorDashboard, DashboardWidget, DashboardFilter

#### GET /{apiVersion}/lke/clusters/{clusterId}/kubeconfig

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `clusterId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `acl`
- `addresses`
- `apl_enabled`
- `audit_logs_enabled`
- `autoscaler`
- `control_plane`
- `count`
- `description`
- `disk_encryption`
- `disks`
- `effect`
- `enabled`
- `endpoint`
- `firewall_id`
- `high_availability`
- `id`
- `instance_id`
- `ipv4`
- `ipv6`
- `k8s_version`
- `key`
- `kubeconfig`
- `label`
- `labels`
- `max`
- `maximum`
- `min`
- `minimum`
- `node_pools`
- `nodes`
- `region`
- `requires_restart`
- `revision-id`
- `servicetoken`
- `size`
- `stack_type`
- `status`
- `subnet_id`
- `tags`
- `taints`
- `tier`
- `type`
- `update_strategy`
- `url`
- `value`
- `vpc_id`

*Related structs analyzed*: LKECluster, LKEClusterCreateOptions, LKEClusterUpdateOptions, LKEClusterAPIEndpoint, LKEClusterKubeconfig, LKEClusterDashboard, LKEVersion, LKETierVersion, LKEClusterRegenerateOptions, LKENodePoolDisk, LKENodePoolAutoscaler, LKENodePoolLinode, LKENodePoolTaint, LKENodePool, LKENodePoolCreateOptions, LKENodePoolUpdateOptions, MaxSlotWALKeepSize, LKEClusterControlPlane, LKEClusterControlPlaneACLAddresses, LKEClusterControlPlaneACL, LKEClusterControlPlaneACLAddressesOptions, LKEClusterControlPlaneACLOptions, LKEClusterControlPlaneOptions, LKEClusterControlPlaneACLUpdateOptions, LKEClusterControlPlaneACLResponse

#### GET /{apiVersion}/lke/clusters/{clusterId}/nodes/{nodeId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `clusterId` (Required, type: `integer`)
- `nodeId` (Required, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `acl`
- `addresses`
- `apl_enabled`
- `assignments`
- `audit_logs_enabled`
- `autoscaler`
- `control_plane`
- `count`
- `description`
- `disk_encryption`
- `disks`
- `down`
- `effect`
- `enabled`
- `endpoint`
- `firewall_id`
- `high_availability`
- `id`
- `instance_id`
- `ipv4`
- `ipv6`
- `k8s_version`
- `key`
- `kubeconfig`
- `label`
- `labels`
- `max`
- `maximum`
- `min`
- `minimum`
- `node_pools`
- `nodes`
- `region`
- `requires_restart`
- `revision-id`
- `servicetoken`
- `size`
- `stack_type`
- `status`
- `subnet_id`
- `tags`
- `taints`
- `tier`
- `type`
- `up`
- `update_strategy`
- `url`
- `value`
- `vpc_id`

*Related structs analyzed*: LKECluster, LKEClusterCreateOptions, LKEClusterUpdateOptions, LKEClusterAPIEndpoint, LKEClusterKubeconfig, LKEClusterDashboard, LKEVersion, LKETierVersion, LKEClusterRegenerateOptions, LKENodePoolDisk, LKENodePoolAutoscaler, LKENodePoolLinode, LKENodePoolTaint, LKENodePool, LKENodePoolCreateOptions, LKENodePoolUpdateOptions, MaxSlotWALKeepSize, LKEClusterControlPlane, LKEClusterControlPlaneACLAddresses, LKEClusterControlPlaneACL, LKEClusterControlPlaneACLAddressesOptions, LKEClusterControlPlaneACLOptions, LKEClusterControlPlaneOptions, LKEClusterControlPlaneACLUpdateOptions, LKEClusterControlPlaneACLResponse, NodeBalancerNodeStatus, LinodesAssignIPsOptions

#### GET /{apiVersion}/lke/clusters/{clusterId}/pools/{poolId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `clusterId` (Required, type: `integer`)
- `poolId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `acl`
- `addresses`
- `apl_enabled`
- `audit_logs_enabled`
- `autoscaler`
- `control_plane`
- `count`
- `description`
- `disk_encryption`
- `disks`
- `effect`
- `enabled`
- `endpoint`
- `firewall_id`
- `high_availability`
- `id`
- `instance_id`
- `ipv4`
- `ipv6`
- `k8s_version`
- `key`
- `kubeconfig`
- `label`
- `labels`
- `max`
- `maximum`
- `min`
- `minimum`
- `node_pools`
- `nodes`
- `region`
- `requires_restart`
- `revision-id`
- `servicetoken`
- `size`
- `stack_type`
- `status`
- `subnet_id`
- `tags`
- `taints`
- `tier`
- `type`
- `update_strategy`
- `url`
- `value`
- `vpc_id`

*Related structs analyzed*: LKECluster, LKEClusterCreateOptions, LKEClusterUpdateOptions, LKEClusterAPIEndpoint, LKEClusterKubeconfig, LKEClusterDashboard, LKEVersion, LKETierVersion, LKEClusterRegenerateOptions, LKENodePoolDisk, LKENodePoolAutoscaler, LKENodePoolLinode, LKENodePoolTaint, LKENodePool, LKENodePoolCreateOptions, LKENodePoolUpdateOptions, MaxSlotWALKeepSize, LKEClusterControlPlane, LKEClusterControlPlaneACLAddresses, LKEClusterControlPlaneACL, LKEClusterControlPlaneACLAddressesOptions, LKEClusterControlPlaneACLOptions, LKEClusterControlPlaneOptions, LKEClusterControlPlaneACLUpdateOptions, LKEClusterControlPlaneACLResponse

#### GET /{apiVersion}/lke/versions/{version}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `version` (Required, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `acl`
- `addresses`
- `apl_enabled`
- `audit_logs_enabled`
- `autoscaler`
- `control_plane`
- `count`
- `description`
- `disk_encryption`
- `disks`
- `effect`
- `enabled`
- `endpoint`
- `firewall_id`
- `high_availability`
- `id`
- `instance_id`
- `ipv4`
- `ipv6`
- `k8s_version`
- `key`
- `kubeconfig`
- `label`
- `labels`
- `max`
- `maximum`
- `min`
- `minimum`
- `node_pools`
- `nodes`
- `region`
- `requires_restart`
- `revision-id`
- `servicetoken`
- `size`
- `stack_type`
- `status`
- `subnet_id`
- `tags`
- `taints`
- `tier`
- `type`
- `update_strategy`
- `url`
- `value`
- `vpc_id`

*Related structs analyzed*: LKECluster, LKEClusterCreateOptions, LKEClusterUpdateOptions, LKEClusterAPIEndpoint, LKEClusterKubeconfig, LKEClusterDashboard, LKEVersion, LKETierVersion, LKEClusterRegenerateOptions, LKENodePoolDisk, LKENodePoolAutoscaler, LKENodePoolLinode, LKENodePoolTaint, LKENodePool, LKENodePoolCreateOptions, LKENodePoolUpdateOptions, MaxSlotWALKeepSize, LKEClusterControlPlane, LKEClusterControlPlaneACLAddresses, LKEClusterControlPlaneACL, LKEClusterControlPlaneACLAddressesOptions, LKEClusterControlPlaneACLOptions, LKEClusterControlPlaneOptions, LKEClusterControlPlaneACLUpdateOptions, LKEClusterControlPlaneACLResponse

#### GET /{apiVersion}/longview/clients

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `apache`
- `api_key`
- `clients_included`
- `hourly`
- `id`
- `install_code`
- `label`
- `longview_subscription`
- `monthly`
- `mysql`
- `nginx`
- `price`
- `updated`

*Related structs analyzed*: LongviewClient, LongviewClientCreateOptions, LongviewClientUpdateOptions, LongviewPlan, LongviewPlanUpdateOptions, LongviewSubscription

#### GET /{apiVersion}/longview/clients/{clientId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `clientId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `apache`
- `api_key`
- `clients_included`
- `hourly`
- `id`
- `install_code`
- `label`
- `longview_subscription`
- `monthly`
- `mysql`
- `nginx`
- `price`
- `updated`

*Related structs analyzed*: LongviewClient, LongviewClientCreateOptions, LongviewClientUpdateOptions, LongviewPlan, LongviewPlanUpdateOptions, LongviewSubscription

#### GET /{apiVersion}/longview/plan

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)

**Extra in SDK** (found in SDK but not documented in API):

- `acl`
- `addresses`
- `apache`
- `api_key`
- `audit_logs_enabled`
- `clients_included`
- `description`
- `enabled`
- `example`
- `high_availability`
- `hourly`
- `id`
- `install_code`
- `ipv4`
- `ipv6`
- `label`
- `longview_subscription`
- `monthly`
- `mysql`
- `nginx`
- `price`
- `requires_restart`
- `revision-id`
- `type`
- `updated`

*Related structs analyzed*: PGStatMonitorPGSMEnableQueryPlan, LongviewClient, LongviewClientCreateOptions, LongviewClientUpdateOptions, LongviewPlan, LongviewPlanUpdateOptions, LKEClusterControlPlane, LKEClusterControlPlaneACLAddresses, LKEClusterControlPlaneACL, LKEClusterControlPlaneACLAddressesOptions, LKEClusterControlPlaneACLOptions, LKEClusterControlPlaneOptions, LKEClusterControlPlaneACLUpdateOptions, LKEClusterControlPlaneACLResponse, LongviewSubscription

#### GET /{apiVersion}/longview/subscriptions

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `apache`
- `api_key`
- `clients_included`
- `hourly`
- `id`
- `install_code`
- `label`
- `longview_subscription`
- `monthly`
- `mysql`
- `nginx`
- `price`
- `updated`

*Related structs analyzed*: LongviewClient, LongviewClientCreateOptions, LongviewClientUpdateOptions, LongviewPlan, LongviewPlanUpdateOptions, LongviewSubscription

#### GET /{apiVersion}/longview/subscriptions/{subscriptionId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `subscriptionId` (Required, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `apache`
- `api_key`
- `clients_included`
- `hourly`
- `id`
- `install_code`
- `label`
- `longview_subscription`
- `monthly`
- `mysql`
- `nginx`
- `price`
- `updated`

*Related structs analyzed*: LongviewClient, LongviewClientCreateOptions, LongviewClientUpdateOptions, LongviewPlan, LongviewPlanUpdateOptions, LongviewSubscription

#### GET /{apiVersion}/maintenance/policies

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4beta...]`)

**Extra in SDK** (found in SDK but not documented in API):

- `day_of_week`
- `description`
- `duration`
- `entity`
- `frequency`
- `hour_of_day`
- `is_default`
- `label`
- `maintenance_policy_set`
- `notification_period_sec`
- `pending`
- `reason`
- `slug`
- `source`
- `status`
- `type`
- `when`

*Related structs analyzed*: AccountMaintenance, DatabaseMaintenanceWindow, DatabaseMaintenanceWindowPending, MaintenancePolicy

#### GET /{apiVersion}/monitor/dashboards

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)

**Extra in SDK** (found in SDK but not documented in API):

- `alert`
- `alerts`
- `available_aggregate_functions`
- `description`
- `dimension_label`
- `dimensions`
- `entity_ids`
- `evaluation_period_seconds`
- `example`
- `id`
- `is_alertable`
- `label`
- `maximum`
- `metric`
- `metric_type`
- `metrics`
- `minimum`
- `polling_interval_seconds`
- `requires_restart`
- `scope`
- `scrape_interval`
- `service_type`
- `token`
- `type`
- `unit`
- `values`
- `widgets`

*Related structs analyzed*: MonitorService, MonitorServiceAlert, MonitorMetricsDefinition, MonitorDimension, RegionMonitors, PGStatMonitorPGSMEnableQueryPlan, PGStatMonitorPGSMMaxBuckets, PostgresDatabaseConfigInfoPGStatMonitorEnable, MonitorDashboard, MonitorServiceToken, MonitorTokenCreateOptions

#### GET /{apiVersion}/monitor/dashboards/{dashboardId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `dashboardId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `alert`
- `alerts`
- `available_aggregate_functions`
- `description`
- `dimension_label`
- `dimensions`
- `entity_ids`
- `evaluation_period_seconds`
- `example`
- `id`
- `is_alertable`
- `label`
- `maximum`
- `metric`
- `metric_type`
- `metrics`
- `minimum`
- `polling_interval_seconds`
- `requires_restart`
- `scope`
- `scrape_interval`
- `service_type`
- `token`
- `type`
- `unit`
- `values`
- `widgets`

*Related structs analyzed*: MonitorService, MonitorServiceAlert, MonitorMetricsDefinition, MonitorDimension, RegionMonitors, PGStatMonitorPGSMEnableQueryPlan, PGStatMonitorPGSMMaxBuckets, PostgresDatabaseConfigInfoPGStatMonitorEnable, MonitorDashboard, MonitorServiceToken, MonitorTokenCreateOptions

#### GET /{apiVersion}/monitor/services

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)

**Extra in SDK** (found in SDK but not documented in API):

- `alert`
- `alerts`
- `available_aggregate_functions`
- `description`
- `dimension_label`
- `dimensions`
- `entity_ids`
- `evaluation_period_seconds`
- `example`
- `id`
- `is_alertable`
- `label`
- `maximum`
- `metric`
- `metric_type`
- `metrics`
- `minimum`
- `polling_interval_seconds`
- `requires_restart`
- `scope`
- `scrape_interval`
- `service_type`
- `token`
- `type`
- `unit`
- `values`
- `widgets`

*Related structs analyzed*: MonitorService, MonitorServiceAlert, MonitorMetricsDefinition, MonitorDimension, RegionMonitors, PGStatMonitorPGSMEnableQueryPlan, PGStatMonitorPGSMMaxBuckets, PostgresDatabaseConfigInfoPGStatMonitorEnable, MonitorDashboard, MonitorServiceToken, MonitorTokenCreateOptions

#### GET /{apiVersion}/monitor/services/{serviceType}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `serviceType` (Required, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `alert`
- `alerts`
- `available_aggregate_functions`
- `description`
- `dimension_label`
- `dimensions`
- `entity_ids`
- `evaluation_period_seconds`
- `example`
- `id`
- `is_alertable`
- `label`
- `maximum`
- `metric`
- `metric_type`
- `metrics`
- `minimum`
- `polling_interval_seconds`
- `requires_restart`
- `scope`
- `scrape_interval`
- `service_type`
- `token`
- `type`
- `unit`
- `values`
- `widgets`

*Related structs analyzed*: MonitorService, MonitorServiceAlert, MonitorMetricsDefinition, MonitorDimension, RegionMonitors, PGStatMonitorPGSMEnableQueryPlan, PGStatMonitorPGSMMaxBuckets, PostgresDatabaseConfigInfoPGStatMonitorEnable, MonitorDashboard, MonitorServiceToken, MonitorTokenCreateOptions

#### GET /{apiVersion}/monitor/services/{serviceType}/alert-definitions/{alertId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `alertId` (Required, type: `integer`)
- `apiVersion` (Required, type: `enum[v4beta...]`)
- `serviceType` (Required, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `alert`
- `alerts`
- `available_aggregate_functions`
- `description`
- `dimension_label`
- `dimensions`
- `entity_ids`
- `evaluation_period_seconds`
- `example`
- `id`
- `is_alertable`
- `label`
- `maximum`
- `metric`
- `metric_type`
- `metrics`
- `minimum`
- `polling_interval_seconds`
- `requires_restart`
- `scope`
- `scrape_interval`
- `service_type`
- `token`
- `type`
- `unit`
- `values`
- `widgets`

*Related structs analyzed*: MonitorService, MonitorServiceAlert, MonitorMetricsDefinition, MonitorDimension, RegionMonitors, PGStatMonitorPGSMEnableQueryPlan, PGStatMonitorPGSMMaxBuckets, PostgresDatabaseConfigInfoPGStatMonitorEnable, MonitorDashboard, MonitorServiceToken, MonitorTokenCreateOptions

#### GET /{apiVersion}/networking/firewalls

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `default_firewall_ids`

*Related structs analyzed*: FirewallSettings, FirewallSettingsUpdateOptions

#### GET /{apiVersion}/networking/firewalls/settings

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `backups_enabled`
- `default_firewall_ids`
- `default_route`
- `interfaces_for_new_linodes`
- `longview_subscription`
- `maintenance_policy`
- `managed`
- `network_helper`
- `object_storage`

*Related structs analyzed*: AccountSettings, AccountSettingsUpdateOptions, InterfaceSettings, InterfaceSettingsUpdateOptions, FirewallSettings, FirewallSettingsUpdateOptions

#### GET /{apiVersion}/networking/firewalls/templates

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `default_firewall_ids`

*Related structs analyzed*: FirewallSettings, FirewallSettingsUpdateOptions

#### GET /{apiVersion}/networking/firewalls/templates/{slug}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)
- `slug` (Required, type: `enum[vpc,public...]`)

**Extra in SDK** (found in SDK but not documented in API):

- `default_firewall_ids`

*Related structs analyzed*: FirewallSettings, FirewallSettingsUpdateOptions

#### GET /{apiVersion}/networking/firewalls/{firewallId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `firewallId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `default_firewall_ids`

*Related structs analyzed*: FirewallSettings, FirewallSettingsUpdateOptions

#### GET /{apiVersion}/networking/firewalls/{firewallId}/devices

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `firewallId` (Required, type: `integer`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `default_firewall_ids`
- `interfaces`
- `linodes`
- `nodebalancers`

*Related structs analyzed*: DevicesCreationOptions, FirewallSettings, FirewallSettingsUpdateOptions

#### GET /{apiVersion}/networking/firewalls/{firewallId}/devices/{deviceId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `deviceId` (Required, type: `integer`)
- `firewallId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `default_firewall_ids`
- `interfaces`
- `linodes`
- `nodebalancers`

*Related structs analyzed*: DevicesCreationOptions, FirewallSettings, FirewallSettingsUpdateOptions

#### GET /{apiVersion}/networking/firewalls/{firewallId}/history

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `firewallId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `default_firewall_ids`

*Related structs analyzed*: FirewallSettings, FirewallSettingsUpdateOptions

#### GET /{apiVersion}/networking/firewalls/{firewallId}/rules

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `firewallId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `default_firewall_ids`
- `description`
- `id`
- `inbound`
- `inbound_policy`
- `is_service_defined`
- `label`
- `outbound`
- `outbound_policy`
- `rules`
- `ruleset`
- `type`
- `version`

*Related structs analyzed*: rulesetOnly, FirewallRuleSet, FirewallSettings, FirewallSettingsUpdateOptions, RuleSet, RuleSetCreateOptions, RuleSetUpdateOptions

#### GET /{apiVersion}/networking/ips

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `skip_ipv6_rdns` (Optional, type: `boolean`)

**Extra in SDK** (found in SDK but not documented in API):

- `assignments`
- `region`

*Related structs analyzed*: LinodesAssignIPsOptions

#### GET /{apiVersion}/networking/ips/{address}

**Missing in SDK** (documented in API but not found in SDK structs):

- `address` (Required, type: `string`)
- `apiVersion` (Required, type: `enum[v4,v4beta...]`)

**Extra in SDK** (found in SDK but not documented in API):

- `assignments`
- `region`

*Related structs analyzed*: LinodesAssignIPsOptions

#### GET /{apiVersion}/networking/ipv6/pools

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `address`
- `allocation_class`
- `global`
- `is_bgp`
- `is_public`
- `link_local`
- `linode_id`
- `linodes`
- `prefix`
- `prefix_length`
- `range`
- `ranges`
- `region`
- `route_target`
- `shared`
- `slaac`
- `slaac_address`
- `vpc`

*Related structs analyzed*: VPCSubnetCreateOptionsIPv6, PublicInterfaceIPv6, PublicInterfaceIPv6Range, PublicInterfaceIPv6SLAAC, VPCInterfaceIPv6, VPCInterfaceIPv6SLAAC, VPCInterfaceIPv6Range, PublicInterfaceIPv6CreateOptions, PublicInterfaceIPv6RangeCreateOptions, VPCInterfaceIPv6CreateOptions, VPCInterfaceIPv6SLAACCreateOptions, VPCInterfaceIPv6RangeCreateOptions, VPCIPv6Range, VPCCreateOptionsIPv6, IPv6RangeCreateOptions, VPCIPIPv6Address, InstanceIPv6Response, IPv6Range, InstanceConfigInterfaceIPv6, InstanceConfigInterfaceIPv6SLAAC, InstanceConfigInterfaceIPv6Range, InstanceConfigInterfaceCreateOptionsIPv6, InstanceConfigInterfaceCreateOptionsIPv6SLAAC, InstanceConfigInterfaceCreateOptionsIPv6Range, InstanceConfigInterfaceUpdateOptionsIPv6, InstanceConfigInterfaceUpdateOptionsIPv6SLAAC, InstanceConfigInterfaceUpdateOptionsIPv6Range

#### GET /{apiVersion}/networking/ipv6/ranges

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `address`
- `allocation_class`
- `global`
- `is_bgp`
- `is_public`
- `link_local`
- `linode_id`
- `linodes`
- `prefix`
- `prefix_length`
- `range`
- `ranges`
- `region`
- `route_target`
- `shared`
- `slaac`
- `slaac_address`
- `vpc`

*Related structs analyzed*: VPCSubnetNodebalancersRanges, VPCSubnetCreateOptionsIPv6, PublicInterfaceIPv6, PublicInterfaceIPv6Range, PublicInterfaceIPv6SLAAC, VPCInterfaceIPv6, VPCInterfaceIPv6SLAAC, VPCInterfaceIPv6Range, PublicInterfaceIPv6CreateOptions, PublicInterfaceIPv6RangeCreateOptions, VPCInterfaceIPv6CreateOptions, VPCInterfaceIPv6SLAACCreateOptions, VPCInterfaceIPv6RangeCreateOptions, VPCIPv6Range, VPCCreateOptionsIPv6, IPv6RangeCreateOptions, VPCIPIPv6Address, InstanceIPv6Response, IPv6Range, InstanceConfigInterfaceIPv6, InstanceConfigInterfaceIPv6SLAAC, InstanceConfigInterfaceIPv6Range, InstanceConfigInterfaceCreateOptionsIPv6, InstanceConfigInterfaceCreateOptionsIPv6SLAAC, InstanceConfigInterfaceCreateOptionsIPv6Range, InstanceConfigInterfaceUpdateOptionsIPv6, InstanceConfigInterfaceUpdateOptionsIPv6SLAAC, InstanceConfigInterfaceUpdateOptionsIPv6Range

#### GET /{apiVersion}/networking/ipv6/ranges/{range}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)

**Extra in SDK** (found in SDK but not documented in API):

- `address`
- `allocation_class`
- `global`
- `is_bgp`
- `is_public`
- `link_local`
- `linode_id`
- `linodes`
- `prefix`
- `prefix_length`
- `ranges`
- `region`
- `route_target`
- `shared`
- `slaac`
- `slaac_address`
- `vpc`

*Related structs analyzed*: VPCSubnetNodebalancersRanges, VPCSubnetCreateOptionsIPv6, PublicInterfaceIPv6, PublicInterfaceIPv6Range, PublicInterfaceIPv6SLAAC, VPCInterfaceIPv6, VPCInterfaceIPv6SLAAC, VPCInterfaceIPv6Range, PublicInterfaceIPv6CreateOptions, PublicInterfaceIPv6RangeCreateOptions, VPCInterfaceIPv6CreateOptions, VPCInterfaceIPv6SLAACCreateOptions, VPCInterfaceIPv6RangeCreateOptions, VPCIPv6Range, VPCCreateOptionsIPv6, IPv6RangeCreateOptions, VPCIPIPv6Address, InstanceIPv6Response, IPv6Range, InstanceConfigInterfaceIPv6, InstanceConfigInterfaceIPv6SLAAC, InstanceConfigInterfaceIPv6Range, InstanceConfigInterfaceCreateOptionsIPv6, InstanceConfigInterfaceCreateOptionsIPv6SLAAC, InstanceConfigInterfaceCreateOptionsIPv6Range, InstanceConfigInterfaceUpdateOptionsIPv6, InstanceConfigInterfaceUpdateOptionsIPv6SLAAC, InstanceConfigInterfaceUpdateOptionsIPv6Range

#### GET /{apiVersion}/networking/vlans

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

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

#### GET /{apiVersion}/nodebalancers/types

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)

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

#### GET /{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId}/nodes/{nodeId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `configId` (Required, type: `integer`)
- `nodeBalancerId` (Required, type: `integer`)
- `nodeId` (Required, type: `string`)

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

#### GET /{apiVersion}/object-storage/buckets

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)

**Extra in SDK** (found in SDK but not documented in API):

- `description`
- `example`
- `maximum`
- `minimum`
- `requires_restart`
- `type`

*Related structs analyzed*: PGStatMonitorPGSMMaxBuckets

#### GET /{apiVersion}/object-storage/buckets/{regionId}/{bucket}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `bucket` (Required, type: `string`)
- `regionId` (Required, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `description`
- `example`
- `maximum`
- `minimum`
- `requires_restart`
- `type`

*Related structs analyzed*: PGStatMonitorPGSMMaxBuckets

#### GET /{apiVersion}/object-storage/buckets/{regionId}/{bucket}/access

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `bucket` (Required, type: `string`)
- `regionId` (Required, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `acl`
- `acl_xml`
- `bucket_name`
- `cluster`
- `cors_enabled`
- `cors_xml`
- `description`
- `example`
- `id`
- `maximum`
- `minimum`
- `permissions`
- `region`
- `requires_restart`
- `roles`
- `type`

*Related structs analyzed*: PGStatMonitorPGSMMaxBuckets, UserAccess, AccountAccess, ObjectStorageBucketAccess, ObjectStorageBucketAccessV2, ObjectStorageBucketUpdateAccessOptions, ObjectStorageKeyBucketAccess

#### GET /{apiVersion}/object-storage/buckets/{regionId}/{bucket}/ssl

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `bucket` (Required, type: `string`)
- `regionId` (Required, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `ca_certificate`
- `description`
- `example`
- `maximum`
- `minimum`
- `requires_restart`
- `type`

*Related structs analyzed*: MySQLDatabaseSSL, PGStatMonitorPGSMMaxBuckets, PostgresDatabaseSSL

#### GET /{apiVersion}/object-storage/clusters

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)

#### GET /{apiVersion}/object-storage/clusters/{clusterId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `clusterId` (Required, type: `string`)

#### GET /{apiVersion}/object-storage/endpoints

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)

#### GET /{apiVersion}/object-storage/keys

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)

#### GET /{apiVersion}/object-storage/keys/{keyId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `keyId` (Required, type: `integer`)

#### GET /{apiVersion}/object-storage/quotas/{objQuotaId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `objQuotaId` (Required, type: `string`)

#### GET /{apiVersion}/object-storage/quotas/{objQuotaId}/usage

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `objQuotaId` (Required, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `quota_limit`
- `usage`

*Related structs analyzed*: ObjectStorageQuotaUsage

#### GET /{apiVersion}/object-storage/transfer

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)

**Extra in SDK** (found in SDK but not documented in API):

- `billable`
- `bytes_in`
- `bytes_out`
- `bytes_total`
- `entities`
- `id`
- `in`
- `is_sender`
- `linodes`
- `out`
- `quota`
- `region_transfers`
- `status`
- `token`
- `total`
- `used`

*Related structs analyzed*: AccountServiceTransfer, AccountServiceTransferEntity, AccountServiceTransferRequestOptions, ObjectStorageTransfer, AccountTransfer, AccountTransferRegion, InstanceTransfer, MonthlyInstanceTransferStats, MonthlyInstanceTransferStatsV2, NodeBalancerTransfer

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

#### GET /{apiVersion}/profile/apps

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

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

#### GET /{apiVersion}/profile/apps/{appId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `appId` (Required, type: `integer`)

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

#### GET /{apiVersion}/profile/devices

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
- `interfaces`
- `ip`
- `ip_whitelist_enabled`
- `label`
- `last_remote_addr`
- `linodes`
- `lish_auth_method`
- `nodebalancers`
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

*Related structs analyzed*: ProfileReferrals, Profile, ProfileUpdateOptions, ProfileLogin, ProfileDevice, DevicesCreationOptions, ProfileApp

#### GET /{apiVersion}/profile/devices/{deviceId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `deviceId` (Required, type: `integer`)

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
- `interfaces`
- `ip`
- `ip_whitelist_enabled`
- `label`
- `last_remote_addr`
- `linodes`
- `lish_auth_method`
- `nodebalancers`
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

*Related structs analyzed*: ProfileReferrals, Profile, ProfileUpdateOptions, ProfileLogin, ProfileDevice, DevicesCreationOptions, ProfileApp

#### GET /{apiVersion}/profile/grants

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)

**Extra in SDK** (found in SDK but not documented in API):

- `account_access`
- `add_databases`
- `add_domains`
- `add_firewalls`
- `add_images`
- `add_linodes`
- `add_longview`
- `add_nodebalancers`
- `add_stackscripts`
- `add_volumes`
- `add_vpcs`
- `authentication_type`
- `authorized_keys`
- `cancel_account`
- `child_account_access`
- `code`
- `completed`
- `credit`
- `database`
- `datetime`
- `domain`
- `email`
- `email_notifications`
- `firewall`
- `global`
- `id`
- `image`
- `ip`
- `ip_whitelist_enabled`
- `label`
- `last_remote_addr`
- `linode`
- `lish_auth_method`
- `longview`
- `longview_subscription`
- `nodebalancer`
- `pending`
- `placement_group`
- `referrals`
- `restricted`
- `scopes`
- `stackscript`
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
- `volume`
- `vpc`
- `website`

*Related structs analyzed*: GlobalUserGrants, UserGrants, UserGrantsUpdateOptions, ProfileReferrals, Profile, ProfileUpdateOptions, ProfileLogin, ProfileDevice, ProfileApp

#### GET /{apiVersion}/profile/logins

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

#### GET /{apiVersion}/profile/logins/{loginId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `loginId` (Required, type: `integer`)

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

#### GET /{apiVersion}/profile/preferences

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

#### GET /{apiVersion}/profile/security-questions

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

#### GET /{apiVersion}/profile/sshkeys

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

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

#### GET /{apiVersion}/profile/sshkeys/{sshKeyId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `sshKeyId` (Required, type: `integer`)

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

#### GET /{apiVersion}/profile/tokens

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)

**Extra in SDK** (found in SDK but not documented in API):

- `authentication_type`
- `authorized_keys`
- `code`
- `completed`
- `credit`
- `datetime`
- `description`
- `email`
- `email_notifications`
- `example`
- `id`
- `ip`
- `ip_whitelist_enabled`
- `label`
- `last_remote_addr`
- `lish_auth_method`
- `maximum`
- `minimum`
- `pending`
- `referrals`
- `requires_restart`
- `restricted`
- `scopes`
- `status`
- `thumbnail_url`
- `timezone`
- `total`
- `two_factor_auth`
- `type`
- `uid`
- `url`
- `user_agent`
- `username`
- `verified_phone_number`
- `website`

*Related structs analyzed*: InnoDBFTMinTokenSize, ProfileReferrals, Profile, ProfileUpdateOptions, ProfileLogin, ProfileDevice, ProfileApp

#### GET /{apiVersion}/profile/tokens/{tokenId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `tokenId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `authentication_type`
- `authorized_keys`
- `code`
- `completed`
- `credit`
- `datetime`
- `description`
- `email`
- `email_notifications`
- `example`
- `id`
- `ip`
- `ip_whitelist_enabled`
- `label`
- `last_remote_addr`
- `lish_auth_method`
- `maximum`
- `minimum`
- `pending`
- `referrals`
- `requires_restart`
- `restricted`
- `scopes`
- `status`
- `thumbnail_url`
- `timezone`
- `total`
- `two_factor_auth`
- `type`
- `uid`
- `url`
- `user_agent`
- `username`
- `verified_phone_number`
- `website`

*Related structs analyzed*: InnoDBFTMinTokenSize, ProfileReferrals, Profile, ProfileUpdateOptions, ProfileLogin, ProfileDevice, ProfileApp

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

#### GET /{apiVersion}/support/tickets

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

#### GET /{apiVersion}/support/tickets/{ticketId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `ticketId` (Required, type: `integer`)

#### GET /{apiVersion}/tags

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

#### GET /{apiVersion}/volumes

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

#### GET /{apiVersion}/volumes/types

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)

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

#### GET /{apiVersion}/vpcs/ips

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `page` (Optional, type: `integer`)
- `page_size` (Optional, type: `integer`)

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

#### POST /{apiVersion}/account/betas

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

#### POST /{apiVersion}/account/events/{eventId}/seen

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `eventId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `account_access`
- `active_promotions`
- `active_since`
- `address_1`
- `address_2`
- `autovacuum_analyze_scale_factor`
- `autovacuum_analyze_threshold`
- `autovacuum_max_workers`
- `autovacuum_naptime`
- `autovacuum_vacuum_cost_delay`
- `autovacuum_vacuum_cost_limit`
- `autovacuum_vacuum_scale_factor`
- `autovacuum_vacuum_threshold`
- `available`
- `backups_enabled`
- `balance`
- `balance_uninvoiced`
- `bgwriter_delay`
- `bgwriter_flush_after`
- `bgwriter_lru_maxpages`
- `bgwriter_lru_multiplier`
- `billable`
- `billing_source`
- `binlog_retention_period`
- `capabilities`
- `city`
- `company`
- `connect_timeout`
- `country`
- `credit_card`
- `deadlock_timeout`
- `default_time_zone`
- `default_toast_compression`
- `description`
- `email`
- `engine`
- `entities`
- `entity`
- `entity_access`
- `eu_model`
- `euuid`
- `first_name`
- `group_concat_max_len`
- `id`
- `idle_in_transaction_session_timeout`
- `information_schema_stats_expiry`
- `innodb_change_buffer_max_size`
- `innodb_flush_neighbors`
- `innodb_ft_min_token_size`
- `innodb_ft_server_stopword_table`
- `innodb_lock_wait_timeout`
- `innodb_log_buffer_size`
- `innodb_online_alter_log_max_size`
- `innodb_read_io_threads`
- `innodb_rollback_on_timeout`
- `innodb_thread_concurrency`
- `innodb_write_io_threads`
- `interactive_timeout`
- `interfaces_for_new_linodes`
- `internal_tmp_mem_storage_engine`
- `is_sender`
- `jit`
- `label`
- `last_name`
- `linodes`
- `longview_subscription`
- `maintenance_policy`
- `maintenance_policy_set`
- `managed`
- `master_service_agreement`
- `max_allowed_packet`
- `max_failover_replication_time_lag`
- `max_files_per_process`
- `max_heap_table_size`
- `max_locks_per_transaction`
- `max_logical_replication_workers`
- `max_parallel_workers`
- `max_parallel_workers_per_gather`
- `max_pred_locks_per_transaction`
- `max_replication_slots`
- `max_slot_wal_keep_size`
- `max_stack_depth`
- `max_standby_archive_delay`
- `max_standby_streaming_delay`
- `max_wal_senders`
- `max_worker_processes`
- `mysql`
- `net_buffer_length`
- `net_read_timeout`
- `net_write_timeout`
- `network_helper`
- `object_storage`
- `password_encryption`
- `pg`
- `pg_partman_bgw.interval`
- `pg_partman_bgw.role`
- `pg_stat_monitor.pgsm_enable_query_plan`
- `pg_stat_monitor.pgsm_max_buckets`
- `pg_stat_monitor_enable`
- `pg_stat_statements.track`
- `pglookout`
- `phone`
- `privacy_policy`
- `quota`
- `reason`
- `region`
- `region_transfers`
- `roles`
- `shared_buffers_percentage`
- `sort_buffer_size`
- `source`
- `sql_mode`
- `sql_require_primary_key`
- `state`
- `status`
- `tax_id`
- `temp_file_limit`
- `timezone`
- `tmp_table_size`
- `token`
- `track_activity_query_size`
- `track_commit_timestamp`
- `track_functions`
- `track_io_timing`
- `type`
- `unavailable`
- `used`
- `version`
- `wait_timeout`
- `wal_sender_timeout`
- `wal_writer_delay`
- `when`
- `work_mem`
- `zip`

*Related structs analyzed*: AccountMaintenance, AccountSettings, AccountSettingsUpdateOptions, MySQLDatabaseEngineConfig, MySQLDatabaseEngineConfigMySQL, DatabaseEngine, AccountServiceTransfer, AccountServiceTransferEntity, AccountServiceTransferRequestOptions, Account, AccountUpdateOptions, AccountAgreements, AccountAgreementsUpdateOptions, PostgresDatabaseEngineConfig, PostgresDatabaseEngineConfigPG, PostgresDatabaseEngineConfigPGLookout, AccountRolePermissions, AccountAccess, AccountTransfer, AccountTransferRegion, AccountAvailability, AccountBetaProgram, AccountBetaProgramCreateOpts

#### POST /{apiVersion}/account/oauth-clients

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

#### POST /{apiVersion}/account/oauth-clients/{clientId}/reset-secret

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `clientId` (Required, type: `string`)

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

#### POST /{apiVersion}/account/payments

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `payment_method_id` (Optional, type: `integer`)
- `usd` (Optional, type: `string`)

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

#### POST /{apiVersion}/account/promo-codes

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `promo_code` (Required, type: `string`)

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

#### POST /{apiVersion}/account/service-transfers

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `entities.linodes` (Optional, type: `array[integer]`)

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

#### POST /{apiVersion}/account/service-transfers/{token}/accept

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
- `type`
- `unavailable`
- `used`
- `when`
- `zip`

*Related structs analyzed*: AccountMaintenance, AccountSettings, AccountSettingsUpdateOptions, AccountServiceTransfer, AccountServiceTransferEntity, AccountServiceTransferRequestOptions, Account, AccountUpdateOptions, AccountAgreements, AccountAgreementsUpdateOptions, AccountRolePermissions, AccountAccess, AccountTransfer, AccountTransferRegion, AccountAvailability, AccountBetaProgram, AccountBetaProgramCreateOpts

#### POST /{apiVersion}/account/users

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

#### POST /{apiVersion}/databases/mysql/instances

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `engine_config.binlog_retention_period` (Optional, type: `integer`)
- `engine_config.mysql` (Optional, type: `object`)
- `engine_config.mysql.connect_timeout` (Optional, type: `integer`)
- `engine_config.mysql.default_time_zone` (Optional, type: `string`)
- `engine_config.mysql.group_concat_max_len` (Optional, type: `integer`)
- `engine_config.mysql.information_schema_stats_expiry` (Optional, type: `integer`)
- `engine_config.mysql.innodb_change_buffer_max_size` (Optional, type: `integer`)
- `engine_config.mysql.innodb_flush_neighbors` (Optional, type: `integer`)
- `engine_config.mysql.innodb_ft_min_token_size` (Optional, type: `integer`)
- `engine_config.mysql.innodb_ft_server_stopword_table` (Optional, type: `string`)
- `engine_config.mysql.innodb_lock_wait_timeout` (Optional, type: `integer`)
- `engine_config.mysql.innodb_log_buffer_size` (Optional, type: `integer`)
- `engine_config.mysql.innodb_online_alter_log_max_size` (Optional, type: `integer`)
- `engine_config.mysql.innodb_read_io_threads` (Optional, type: `integer`)
- `engine_config.mysql.innodb_rollback_on_timeout` (Optional, type: `boolean`)
- `engine_config.mysql.innodb_thread_concurrency` (Optional, type: `integer`)
- `engine_config.mysql.innodb_write_io_threads` (Optional, type: `integer`)
- `engine_config.mysql.interactive_timeout` (Optional, type: `integer`)
- `engine_config.mysql.internal_tmp_mem_storage_engine` (Optional, type: `enum[TempTable,MEMORY...]`)
- `engine_config.mysql.max_allowed_packet` (Optional, type: `integer`)
- `engine_config.mysql.max_heap_table_size` (Optional, type: `integer`)
- `engine_config.mysql.net_buffer_length` (Optional, type: `integer`)
- `engine_config.mysql.net_read_timeout` (Optional, type: `integer`)
- `engine_config.mysql.net_write_timeout` (Optional, type: `integer`)
- `engine_config.mysql.sql_mode` (Optional, type: `string`)
- `engine_config.mysql.sql_require_primary_key` (Optional, type: `boolean`)
- `engine_config.mysql.tmp_table_size` (Optional, type: `integer`)
- `engine_config.mysql.wait_timeout` (Optional, type: `integer`)
- `fork.restore_time` (Optional, type: `string`)
- `fork.source` (Required, type: `integer`)
- `private_network.public_access` (Optional, type: `boolean`)
- `private_network.subnet_id` (Optional, type: `integer`)
- `private_network.vpc_id` (Optional, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `available`
- `binlog_retention_period`
- `ca_certificate`
- `configs`
- `connect_timeout`
- `cpu`
- `data`
- `default_time_zone`
- `description`
- `disk`
- `disks`
- `encrypted`
- `example`
- `filesystem`
- `gpus`
- `group_concat_max_len`
- `hosts`
- `id`
- `information_schema_stats_expiry`
- `innodb_change_buffer_max_size`
- `innodb_flush_neighbors`
- `innodb_ft_min_token_size`
- `innodb_ft_server_stopword_table`
- `innodb_lock_wait_timeout`
- `innodb_log_buffer_size`
- `innodb_online_alter_log_max_size`
- `innodb_read_io_threads`
- `innodb_rollback_on_timeout`
- `innodb_thread_concurrency`
- `innodb_write_io_threads`
- `interactive_timeout`
- `internal_tmp_mem_storage_engine`
- `io`
- `max_allowed_packet`
- `max_heap_table_size`
- `maximum`
- `members`
- `memory`
- `minimum`
- `mysql`
- `net_buffer_length`
- `net_read_timeout`
- `net_write_timeout`
- `netv4`
- `netv6`
- `password`
- `platform`
- `port`
- `requires_restart`
- `size`
- `sort_buffer_size`
- `sql_mode`
- `sql_require_primary_key`
- `status`
- `title`
- `tmp_table_size`
- `total_disk_size_gb`
- `transfer`
- `updates`
- `used_disk_size_gb`
- `username`
- `vcpus`
- `version`
- `wait_timeout`

*Related structs analyzed*: InstanceStatsData, InstanceStats, MySQLDatabase, MySQLDatabaseEngineConfig, MySQLDatabaseEngineConfigMySQL, MySQLDatabaseConfigInfo, MySQLDatabaseConfigInfoMySQL, MySQLDatabaseConfigInfoBinlogRetentionPeriod, MySQLCreateOptions, MySQLUpdateOptions, MySQLDatabaseCredential, MySQLDatabaseSSL, PostgresDatabaseSSL, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec

#### POST /{apiVersion}/databases/mysql/instances/{instanceId}/credentials/reset

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `instanceId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `allow_list`
- `available`
- `binlog_retention_period`
- `ca_certificate`
- `cluster_size`
- `configs`
- `connect_timeout`
- `cpu`
- `data`
- `default_time_zone`
- `description`
- `disk`
- `disks`
- `encrypted`
- `engine`
- `engine_config`
- `example`
- `filesystem`
- `fork`
- `gpus`
- `group_concat_max_len`
- `hosts`
- `id`
- `information_schema_stats_expiry`
- `innodb_change_buffer_max_size`
- `innodb_flush_neighbors`
- `innodb_ft_min_token_size`
- `innodb_ft_server_stopword_table`
- `innodb_lock_wait_timeout`
- `innodb_log_buffer_size`
- `innodb_online_alter_log_max_size`
- `innodb_read_io_threads`
- `innodb_rollback_on_timeout`
- `innodb_thread_concurrency`
- `innodb_write_io_threads`
- `interactive_timeout`
- `internal_tmp_mem_storage_engine`
- `io`
- `label`
- `max_allowed_packet`
- `max_heap_table_size`
- `maximum`
- `members`
- `memory`
- `minimum`
- `mysql`
- `net_buffer_length`
- `net_read_timeout`
- `net_write_timeout`
- `netv4`
- `netv6`
- `password`
- `platform`
- `port`
- `private_network`
- `region`
- `requires_restart`
- `root_pass`
- `size`
- `sort_buffer_size`
- `sql_mode`
- `sql_require_primary_key`
- `ssl_connection`
- `status`
- `title`
- `tmp_table_size`
- `total_disk_size_gb`
- `transfer`
- `type`
- `updates`
- `used_disk_size_gb`
- `username`
- `vcpus`
- `version`
- `wait_timeout`

*Related structs analyzed*: InstanceStatsData, InstanceStats, MySQLDatabase, MySQLDatabaseEngineConfig, MySQLDatabaseEngineConfigMySQL, MySQLDatabaseConfigInfo, MySQLDatabaseConfigInfoMySQL, MySQLDatabaseConfigInfoBinlogRetentionPeriod, MySQLCreateOptions, MySQLUpdateOptions, MySQLDatabaseCredential, MySQLDatabaseSSL, PostgresDatabaseSSL, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, InstancePasswordResetOptions

#### POST /{apiVersion}/databases/mysql/instances/{instanceId}/patch

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `instanceId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `allow_list`
- `available`
- `binlog_retention_period`
- `ca_certificate`
- `cluster_size`
- `configs`
- `connect_timeout`
- `cpu`
- `data`
- `default_time_zone`
- `description`
- `disk`
- `disks`
- `encrypted`
- `engine`
- `engine_config`
- `example`
- `filesystem`
- `fork`
- `gpus`
- `group_concat_max_len`
- `hosts`
- `id`
- `information_schema_stats_expiry`
- `innodb_change_buffer_max_size`
- `innodb_flush_neighbors`
- `innodb_ft_min_token_size`
- `innodb_ft_server_stopword_table`
- `innodb_lock_wait_timeout`
- `innodb_log_buffer_size`
- `innodb_online_alter_log_max_size`
- `innodb_read_io_threads`
- `innodb_rollback_on_timeout`
- `innodb_thread_concurrency`
- `innodb_write_io_threads`
- `interactive_timeout`
- `internal_tmp_mem_storage_engine`
- `io`
- `label`
- `max_allowed_packet`
- `max_heap_table_size`
- `maximum`
- `members`
- `memory`
- `minimum`
- `mysql`
- `net_buffer_length`
- `net_read_timeout`
- `net_write_timeout`
- `netv4`
- `netv6`
- `password`
- `platform`
- `port`
- `private_network`
- `region`
- `requires_restart`
- `size`
- `sort_buffer_size`
- `sql_mode`
- `sql_require_primary_key`
- `ssl_connection`
- `status`
- `title`
- `tmp_table_size`
- `total_disk_size_gb`
- `transfer`
- `type`
- `updates`
- `used_disk_size_gb`
- `username`
- `vcpus`
- `version`
- `wait_timeout`

*Related structs analyzed*: InstanceStatsData, InstanceStats, MySQLDatabase, MySQLDatabaseEngineConfig, MySQLDatabaseEngineConfigMySQL, MySQLDatabaseConfigInfo, MySQLDatabaseConfigInfoMySQL, MySQLDatabaseConfigInfoBinlogRetentionPeriod, MySQLCreateOptions, MySQLUpdateOptions, MySQLDatabaseCredential, MySQLDatabaseSSL, PostgresDatabaseSSL, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec

#### POST /{apiVersion}/databases/mysql/instances/{instanceId}/resume

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4...]`)
- `instanceId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `allow_list`
- `available`
- `binlog_retention_period`
- `ca_certificate`
- `cluster_size`
- `configs`
- `connect_timeout`
- `cpu`
- `data`
- `default_time_zone`
- `description`
- `disk`
- `disks`
- `encrypted`
- `engine`
- `engine_config`
- `example`
- `filesystem`
- `fork`
- `gpus`
- `group_concat_max_len`
- `hosts`
- `id`
- `information_schema_stats_expiry`
- `innodb_change_buffer_max_size`
- `innodb_flush_neighbors`
- `innodb_ft_min_token_size`
- `innodb_ft_server_stopword_table`
- `innodb_lock_wait_timeout`
- `innodb_log_buffer_size`
- `innodb_online_alter_log_max_size`
- `innodb_read_io_threads`
- `innodb_rollback_on_timeout`
- `innodb_thread_concurrency`
- `innodb_write_io_threads`
- `interactive_timeout`
- `internal_tmp_mem_storage_engine`
- `io`
- `label`
- `max_allowed_packet`
- `max_heap_table_size`
- `maximum`
- `members`
- `memory`
- `minimum`
- `mysql`
- `net_buffer_length`
- `net_read_timeout`
- `net_write_timeout`
- `netv4`
- `netv6`
- `password`
- `platform`
- `port`
- `private_network`
- `region`
- `requires_restart`
- `size`
- `sort_buffer_size`
- `sql_mode`
- `sql_require_primary_key`
- `ssl_connection`
- `status`
- `title`
- `tmp_table_size`
- `total_disk_size_gb`
- `transfer`
- `type`
- `updates`
- `used_disk_size_gb`
- `username`
- `vcpus`
- `version`
- `wait_timeout`

*Related structs analyzed*: InstanceStatsData, InstanceStats, MySQLDatabase, MySQLDatabaseEngineConfig, MySQLDatabaseEngineConfigMySQL, MySQLDatabaseConfigInfo, MySQLDatabaseConfigInfoMySQL, MySQLDatabaseConfigInfoBinlogRetentionPeriod, MySQLCreateOptions, MySQLUpdateOptions, MySQLDatabaseCredential, MySQLDatabaseSSL, PostgresDatabaseSSL, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec

#### POST /{apiVersion}/databases/mysql/instances/{instanceId}/suspend

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4...]`)
- `instanceId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `allow_list`
- `available`
- `binlog_retention_period`
- `ca_certificate`
- `cluster_size`
- `configs`
- `connect_timeout`
- `cpu`
- `data`
- `default_time_zone`
- `description`
- `disk`
- `disks`
- `encrypted`
- `engine`
- `engine_config`
- `example`
- `filesystem`
- `fork`
- `gpus`
- `group_concat_max_len`
- `hosts`
- `id`
- `information_schema_stats_expiry`
- `innodb_change_buffer_max_size`
- `innodb_flush_neighbors`
- `innodb_ft_min_token_size`
- `innodb_ft_server_stopword_table`
- `innodb_lock_wait_timeout`
- `innodb_log_buffer_size`
- `innodb_online_alter_log_max_size`
- `innodb_read_io_threads`
- `innodb_rollback_on_timeout`
- `innodb_thread_concurrency`
- `innodb_write_io_threads`
- `interactive_timeout`
- `internal_tmp_mem_storage_engine`
- `io`
- `label`
- `max_allowed_packet`
- `max_heap_table_size`
- `maximum`
- `members`
- `memory`
- `minimum`
- `mysql`
- `net_buffer_length`
- `net_read_timeout`
- `net_write_timeout`
- `netv4`
- `netv6`
- `password`
- `platform`
- `port`
- `private_network`
- `region`
- `requires_restart`
- `size`
- `sort_buffer_size`
- `sql_mode`
- `sql_require_primary_key`
- `ssl_connection`
- `status`
- `title`
- `tmp_table_size`
- `total_disk_size_gb`
- `transfer`
- `type`
- `updates`
- `used_disk_size_gb`
- `username`
- `vcpus`
- `version`
- `wait_timeout`

*Related structs analyzed*: InstanceStatsData, InstanceStats, MySQLDatabase, MySQLDatabaseEngineConfig, MySQLDatabaseEngineConfigMySQL, MySQLDatabaseConfigInfo, MySQLDatabaseConfigInfoMySQL, MySQLDatabaseConfigInfoBinlogRetentionPeriod, MySQLCreateOptions, MySQLUpdateOptions, MySQLDatabaseCredential, MySQLDatabaseSSL, PostgresDatabaseSSL, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec

#### POST /{apiVersion}/databases/postgresql/instances

**Missing in SDK** (documented in API but not found in SDK structs):

- `allow_list` (Optional, type: `array[string]`)
- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `cluster_size` (Optional, type: `enum[1,2,3...]`)
- `engine` (Required, type: `string`)
- `engine_config` (Optional, type: `object`)
- `engine_config.pg` (Optional, type: `object`)
- `engine_config.pg.autovacuum_analyze_scale_factor` (Optional, type: `number`)
- `engine_config.pg.autovacuum_analyze_threshold` (Optional, type: `integer`)
- `engine_config.pg.autovacuum_max_workers` (Optional, type: `integer`)
- `engine_config.pg.autovacuum_naptime` (Optional, type: `integer`)
- `engine_config.pg.autovacuum_vacuum_cost_delay` (Optional, type: `integer`)
- `engine_config.pg.autovacuum_vacuum_cost_limit` (Optional, type: `integer`)
- `engine_config.pg.autovacuum_vacuum_scale_factor` (Optional, type: `number`)
- `engine_config.pg.autovacuum_vacuum_threshold` (Optional, type: `integer`)
- `engine_config.pg.bgwriter_delay` (Optional, type: `integer`)
- `engine_config.pg.bgwriter_flush_after` (Optional, type: `integer`)
- `engine_config.pg.bgwriter_lru_maxpages` (Optional, type: `integer`)
- `engine_config.pg.bgwriter_lru_multiplier` (Optional, type: `number`)
- `engine_config.pg.deadlock_timeout` (Optional, type: `integer`)
- `engine_config.pg.default_toast_compression` (Optional, type: `enum[lz4,pglz...]`)
- `engine_config.pg.idle_in_transaction_session_timeout` (Optional, type: `integer`)
- `engine_config.pg.jit` (Optional, type: `boolean`)
- `engine_config.pg.max_files_per_process` (Optional, type: `integer`)
- `engine_config.pg.max_locks_per_transaction` (Optional, type: `integer`)
- `engine_config.pg.max_logical_replication_workers` (Optional, type: `integer`)
- `engine_config.pg.max_parallel_workers` (Optional, type: `integer`)
- `engine_config.pg.max_parallel_workers_per_gather` (Optional, type: `integer`)
- `engine_config.pg.max_pred_locks_per_transaction` (Optional, type: `integer`)
- `engine_config.pg.max_replication_slots` (Optional, type: `integer`)
- `engine_config.pg.max_slot_wal_keep_size` (Optional, type: `integer`)
- `engine_config.pg.max_stack_depth` (Optional, type: `integer`)
- `engine_config.pg.max_standby_archive_delay` (Optional, type: `integer`)
- `engine_config.pg.max_standby_streaming_delay` (Optional, type: `integer`)
- `engine_config.pg.max_wal_senders` (Optional, type: `integer`)
- `engine_config.pg.max_worker_processes` (Optional, type: `integer`)
- `engine_config.pg.password_encryption` (Optional, type: `enum[scram-sh-256,md5...]`)
- `engine_config.pg.pg_partman_bgw.interval` (Optional, type: `integer`)
- `engine_config.pg.pg_partman_bgw.role` (Optional, type: `string`)
- `engine_config.pg.pg_stat_monitor.pgsm_enable_query_plan` (Optional, type: `boolean`)
- `engine_config.pg.pg_stat_monitor.pgsm_max_buckets` (Optional, type: `integer`)
- `engine_config.pg.pg_stat_statements.track` (Optional, type: `enum[all,top,none...]`)
- `engine_config.pg.synchronous_replication` (Optional, type: `enum[quorum,False...]`)
- `engine_config.pg.temp_file_limit` (Optional, type: `integer`)
- `engine_config.pg.timezone` (Optional, type: `string`)
- `engine_config.pg.track_activity_query_size` (Optional, type: `integer`)
- `engine_config.pg.track_commit_timestamp` (Optional, type: `enum[on,off...]`)
- `engine_config.pg.track_functions` (Optional, type: `enum[all,pl,none...]`)
- `engine_config.pg.track_io_timing` (Optional, type: `enum[on,off...]`)
- `engine_config.pg.wal_sender_timeout` (Optional, type: `integer`)
- `engine_config.pg.wal_writer_delay` (Optional, type: `integer`)
- `engine_config.pg_stat_monitor_enable` (Optional, type: `boolean`)
- `engine_config.pglookout` (Optional, type: `object`)
- `engine_config.pglookout.max_failover_replication_time_lag` (Optional, type: `integer`)
- `engine_config.shared_buffers_percentage` (Optional, type: `number`)
- `engine_config.work_mem` (Optional, type: `integer`)
- `fork` (Optional, type: `object`)
- `fork.restore_time` (Optional, type: `string`)
- `fork.source` (Required, type: `integer`)
- `private_network` (Optional, type: `object`)
- `private_network.public_access` (Optional, type: `boolean`)
- `private_network.subnet_id` (Optional, type: `integer`)
- `private_network.vpc_id` (Optional, type: `integer`)
- `region` (Required, type: `string`)
- `ssl_connection` (Optional, type: `boolean`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `available`
- `ca_certificate`
- `configs`
- `cpu`
- `data`
- `disk`
- `disks`
- `filesystem`
- `gpus`
- `id`
- `io`
- `memory`
- `netv4`
- `netv6`
- `size`
- `status`
- `title`
- `transfer`
- `vcpus`

*Related structs analyzed*: InstanceStatsData, InstanceStats, MySQLDatabaseSSL, PostgresDatabaseSSL, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec

#### POST /{apiVersion}/databases/postgresql/instances/{instanceId}/credentials/reset

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `instanceId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `available`
- `ca_certificate`
- `configs`
- `cpu`
- `data`
- `disk`
- `disks`
- `filesystem`
- `gpus`
- `id`
- `io`
- `label`
- `memory`
- `netv4`
- `netv6`
- `root_pass`
- `size`
- `status`
- `title`
- `transfer`
- `type`
- `vcpus`

*Related structs analyzed*: InstanceStatsData, InstanceStats, MySQLDatabaseSSL, PostgresDatabaseSSL, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, InstancePasswordResetOptions

#### POST /{apiVersion}/databases/postgresql/instances/{instanceId}/patch

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `instanceId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `available`
- `ca_certificate`
- `configs`
- `cpu`
- `data`
- `disk`
- `disks`
- `filesystem`
- `gpus`
- `id`
- `io`
- `label`
- `memory`
- `netv4`
- `netv6`
- `size`
- `status`
- `title`
- `transfer`
- `type`
- `vcpus`

*Related structs analyzed*: InstanceStatsData, InstanceStats, MySQLDatabaseSSL, PostgresDatabaseSSL, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec

#### POST /{apiVersion}/databases/postgresql/instances/{instanceId}/resume

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4...]`)
- `instanceId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `available`
- `ca_certificate`
- `configs`
- `cpu`
- `data`
- `disk`
- `disks`
- `filesystem`
- `gpus`
- `id`
- `io`
- `label`
- `memory`
- `netv4`
- `netv6`
- `size`
- `status`
- `title`
- `transfer`
- `type`
- `vcpus`

*Related structs analyzed*: InstanceStatsData, InstanceStats, MySQLDatabaseSSL, PostgresDatabaseSSL, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec

#### POST /{apiVersion}/databases/postgresql/instances/{instanceId}/suspend

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4...]`)
- `instanceId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `available`
- `ca_certificate`
- `configs`
- `cpu`
- `data`
- `disk`
- `disks`
- `filesystem`
- `gpus`
- `id`
- `io`
- `label`
- `memory`
- `netv4`
- `netv6`
- `size`
- `status`
- `title`
- `transfer`
- `type`
- `vcpus`

*Related structs analyzed*: InstanceStatsData, InstanceStats, MySQLDatabaseSSL, PostgresDatabaseSSL, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec

#### POST /{apiVersion}/domains

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)

#### POST /{apiVersion}/domains/import

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `remote_nameserver` (Required, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `remove_nameserver`

*Related structs analyzed*: DomainImportOptions

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

#### POST /{apiVersion}/linode/instances

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### POST /{apiVersion}/linode/instances/{linodeId}/backups

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `automatic`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `current`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `in_progress`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `snapshot`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceBackupsResponse, InstanceBackupSnapshotResponse, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### POST /{apiVersion}/linode/instances/{linodeId}/backups/cancel

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `automatic`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `current`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `in_progress`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `snapshot`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceBackupsResponse, InstanceBackupSnapshotResponse, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### POST /{apiVersion}/linode/instances/{linodeId}/backups/enable

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `automatic`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `current`
- `data`
- `default_route`
- `deprecated`
- `description`
- `disk`
- `disks`
- `dry_run`
- `example`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `in_progress`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `requires_restart`
- `size`
- `snapshot`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, PGStatMonitorPGSMEnableQueryPlan, PostgresDatabaseConfigInfoPGStatMonitorEnable, InstanceBackupsResponse, InstanceBackupSnapshotResponse, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### POST /{apiVersion}/linode/instances/{linodeId}/backups/{backupId}/restore

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `backupId` (Required, type: `integer`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `automatic`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `current`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `in_progress`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `snapshot`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceBackupsResponse, InstanceBackupSnapshotResponse, RestoreInstanceOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### POST /{apiVersion}/linode/instances/{linodeId}/boot

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### POST /{apiVersion}/linode/instances/{linodeId}/clone

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `linodeId` (Required, type: `integer`)
- `maintenance_policy` (Optional, type: `enum[linode/migrate,linode/power_off_on...]`)
- `metadata.user_data` (Optional, type: `string`)
- `placement_group.id` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `config_id`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `domain`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `price`
- `public`
- `pvops`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, InstanceCloneOptions, DomainCloneOptions, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### POST /{apiVersion}/linode/instances/{linodeId}/configs

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### POST /{apiVersion}/linode/instances/{linodeId}/configs/{configId}/interfaces

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `configId` (Required, type: `integer`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `ids`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_helper`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InterfaceSettings, InterfaceSettingsUpdateOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel, InstanceConfigInterfacesReorderOptions

#### POST /{apiVersion}/linode/instances/{linodeId}/disks

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### POST /{apiVersion}/linode/instances/{linodeId}/disks/{diskId}/clone

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `diskId` (Required, type: `integer`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `backups_enabled`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `domain`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `group`
- `hourly`
- `id`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `metadata`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `placement_group`
- `price`
- `private_ip`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, InstanceCloneOptions, DomainCloneOptions, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### POST /{apiVersion}/linode/instances/{linodeId}/disks/{diskId}/password

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `diskId` (Required, type: `integer`)
- `linodeId` (Required, type: `integer`)
- `password` (Required, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `description`
- `disk`
- `disks`
- `dry_run`
- `enum`
- `example`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `requires_restart`
- `root_pass`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, PasswordEncryption, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, InstancePasswordResetOptions, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### POST /{apiVersion}/linode/instances/{linodeId}/disks/{diskId}/resize

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `diskId` (Required, type: `integer`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `allow_auto_disk_resize`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `migration_type`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, InstanceResizeOptions, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### POST /{apiVersion}/linode/instances/{linodeId}/interfaces

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `ids`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_helper`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InterfaceSettings, InterfaceSettingsUpdateOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel, InstanceConfigInterfacesReorderOptions

#### POST /{apiVersion}/linode/instances/{linodeId}/ips

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `price`
- `pvops`
- `region`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### POST /{apiVersion}/linode/instances/{linodeId}/migrate

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `linodeId` (Required, type: `integer`)
- `placement_group.id` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `price`
- `public`
- `pvops`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, InstanceMigrateOptions, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### POST /{apiVersion}/linode/instances/{linodeId}/mutate

**Missing in SDK** (documented in API but not found in SDK structs):

- `allow_auto_disk_resize` (Optional, type: `boolean`)
- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### POST /{apiVersion}/linode/instances/{linodeId}/password

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `description`
- `disk`
- `disks`
- `dry_run`
- `enum`
- `example`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `requires_restart`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, PasswordEncryption, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, InstancePasswordResetOptions, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### POST /{apiVersion}/linode/instances/{linodeId}/reboot

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### POST /{apiVersion}/linode/instances/{linodeId}/rebuild

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `algorithm`
- `architecture`
- `assignments`
- `authorized_keys`
- `authorized_users`
- `available`
- `backups`
- `booted`
- `check`
- `check_attempts`
- `check_body`
- `check_interval`
- `check_passive`
- `check_path`
- `check_timeout`
- `cipher_suite`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disk_encryption`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `image`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `metadata`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `nodes`
- `port`
- `price`
- `protocol`
- `proxy_protocol`
- `public`
- `pvops`
- `region`
- `region_prices`
- `root_pass`
- `size`
- `ssl_cert`
- `ssl_key`
- `stackscript_data`
- `stackscript_id`
- `status`
- `stickiness`
- `successor`
- `title`
- `transfer`
- `type`
- `udp_check_port`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, InstanceRebuildOptions, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, NodeBalancerConfigRebuildOptions, NodeBalancerConfigRebuildNodeOptions, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### POST /{apiVersion}/linode/instances/{linodeId}/rescue

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `devices.sda` (Optional, type: `object`)
- `devices.sda.disk_id` (Optional, type: `integer`)
- `devices.sda.volume_id` (Optional, type: `integer`)
- `devices.sdb` (Optional, type: `object`)
- `devices.sdb.disk_id` (Optional, type: `integer`)
- `devices.sdb.volume_id` (Optional, type: `integer`)
- `devices.sdc` (Optional, type: `object`)
- `devices.sdc.disk_id` (Optional, type: `integer`)
- `devices.sdc.volume_id` (Optional, type: `integer`)
- `devices.sdd` (Optional, type: `object`)
- `devices.sdd.disk_id` (Optional, type: `integer`)
- `devices.sdd.volume_id` (Optional, type: `integer`)
- `devices.sde` (Optional, type: `object`)
- `devices.sde.disk_id` (Optional, type: `integer`)
- `devices.sde.volume_id` (Optional, type: `integer`)
- `devices.sdf` (Optional, type: `object`)
- `devices.sdf.disk_id` (Optional, type: `integer`)
- `devices.sdf.volume_id` (Optional, type: `integer`)
- `devices.sdg` (Optional, type: `object`)
- `devices.sdg.disk_id` (Optional, type: `integer`)
- `devices.sdg.volume_id` (Optional, type: `integer`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, InstanceRescueOptions, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### POST /{apiVersion}/linode/instances/{linodeId}/resize

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, InstanceResizeOptions, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### POST /{apiVersion}/linode/instances/{linodeId}/shutdown

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### POST /{apiVersion}/linode/instances/{linodeId}/upgrade-interfaces

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### POST /{apiVersion}/linode/stackscripts

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `backups`
- `class`
- `config_id`
- `default_route`
- `deprecated`
- `disk`
- `dry_run`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `instance_id`
- `interfaces`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `status`
- `successor`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### POST /{apiVersion}/lke/clusters

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `control_plane.acl` (Optional, type: `object`)
- `control_plane.acl.addresses` (Optional, type: `object`)
- `control_plane.acl.addresses.ipv4` (Optional, type: `array[string]`)
- `control_plane.acl.addresses.ipv6` (Optional, type: `array[string]`)
- `control_plane.acl.enabled` (Optional, type: `boolean`)
- `control_plane.acl.revision-id` (Optional, type: `string`)
- `control_plane.audit_logs_enabled` (Optional, type: `boolean`)
- `control_plane.high_availability` (Optional, type: `boolean`)

**Extra in SDK** (found in SDK but not documented in API):

- `acl`
- `addresses`
- `audit_logs_enabled`
- `autoscaler`
- `count`
- `description`
- `disk_encryption`
- `disks`
- `effect`
- `enabled`
- `endpoint`
- `firewall_id`
- `high_availability`
- `id`
- `instance_id`
- `ipv4`
- `ipv6`
- `key`
- `kubeconfig`
- `labels`
- `max`
- `maximum`
- `min`
- `minimum`
- `nodes`
- `requires_restart`
- `revision-id`
- `servicetoken`
- `size`
- `status`
- `taints`
- `type`
- `update_strategy`
- `url`
- `value`

*Related structs analyzed*: LKECluster, LKEClusterCreateOptions, LKEClusterUpdateOptions, LKEClusterAPIEndpoint, LKEClusterKubeconfig, LKEClusterDashboard, LKEVersion, LKETierVersion, LKEClusterRegenerateOptions, LKENodePoolDisk, LKENodePoolAutoscaler, LKENodePoolLinode, LKENodePoolTaint, LKENodePool, LKENodePoolCreateOptions, LKENodePoolUpdateOptions, MaxSlotWALKeepSize, LKEClusterControlPlane, LKEClusterControlPlaneACLAddresses, LKEClusterControlPlaneACL, LKEClusterControlPlaneACLAddressesOptions, LKEClusterControlPlaneACLOptions, LKEClusterControlPlaneOptions, LKEClusterControlPlaneACLUpdateOptions, LKEClusterControlPlaneACLResponse

#### POST /{apiVersion}/lke/clusters/{clusterId}/nodes/{nodeId}/recycle

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `clusterId` (Required, type: `integer`)
- `nodeId` (Required, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `acl`
- `addresses`
- `apl_enabled`
- `assignments`
- `audit_logs_enabled`
- `autoscaler`
- `control_plane`
- `count`
- `description`
- `disk_encryption`
- `disks`
- `down`
- `effect`
- `enabled`
- `endpoint`
- `firewall_id`
- `high_availability`
- `id`
- `instance_id`
- `ipv4`
- `ipv6`
- `k8s_version`
- `key`
- `kubeconfig`
- `label`
- `labels`
- `max`
- `maximum`
- `min`
- `minimum`
- `node_pools`
- `nodes`
- `region`
- `requires_restart`
- `revision-id`
- `servicetoken`
- `size`
- `stack_type`
- `status`
- `subnet_id`
- `tags`
- `taints`
- `tier`
- `type`
- `up`
- `update_strategy`
- `url`
- `value`
- `vpc_id`

*Related structs analyzed*: LKECluster, LKEClusterCreateOptions, LKEClusterUpdateOptions, LKEClusterAPIEndpoint, LKEClusterKubeconfig, LKEClusterDashboard, LKEVersion, LKETierVersion, LKEClusterRegenerateOptions, LKENodePoolDisk, LKENodePoolAutoscaler, LKENodePoolLinode, LKENodePoolTaint, LKENodePool, LKENodePoolCreateOptions, LKENodePoolUpdateOptions, MaxSlotWALKeepSize, LKEClusterControlPlane, LKEClusterControlPlaneACLAddresses, LKEClusterControlPlaneACL, LKEClusterControlPlaneACLAddressesOptions, LKEClusterControlPlaneACLOptions, LKEClusterControlPlaneOptions, LKEClusterControlPlaneACLUpdateOptions, LKEClusterControlPlaneACLResponse, NodeBalancerNodeStatus, LinodesAssignIPsOptions

#### POST /{apiVersion}/lke/clusters/{clusterId}/pools

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `clusterId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `acl`
- `addresses`
- `apl_enabled`
- `audit_logs_enabled`
- `autoscaler`
- `control_plane`
- `count`
- `description`
- `disk_encryption`
- `disks`
- `effect`
- `enabled`
- `endpoint`
- `firewall_id`
- `high_availability`
- `id`
- `instance_id`
- `ipv4`
- `ipv6`
- `k8s_version`
- `key`
- `kubeconfig`
- `label`
- `labels`
- `max`
- `maximum`
- `min`
- `minimum`
- `node_pools`
- `nodes`
- `region`
- `requires_restart`
- `revision-id`
- `servicetoken`
- `size`
- `stack_type`
- `status`
- `subnet_id`
- `tags`
- `taints`
- `tier`
- `type`
- `update_strategy`
- `url`
- `value`
- `vpc_id`

*Related structs analyzed*: LKECluster, LKEClusterCreateOptions, LKEClusterUpdateOptions, LKEClusterAPIEndpoint, LKEClusterKubeconfig, LKEClusterDashboard, LKEVersion, LKETierVersion, LKEClusterRegenerateOptions, LKENodePoolDisk, LKENodePoolAutoscaler, LKENodePoolLinode, LKENodePoolTaint, LKENodePool, LKENodePoolCreateOptions, LKENodePoolUpdateOptions, MaxSlotWALKeepSize, LKEClusterControlPlane, LKEClusterControlPlaneACLAddresses, LKEClusterControlPlaneACL, LKEClusterControlPlaneACLAddressesOptions, LKEClusterControlPlaneACLOptions, LKEClusterControlPlaneOptions, LKEClusterControlPlaneACLUpdateOptions, LKEClusterControlPlaneACLResponse

#### POST /{apiVersion}/lke/clusters/{clusterId}/pools/{poolId}/recycle

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `clusterId` (Required, type: `integer`)
- `poolId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `acl`
- `addresses`
- `apl_enabled`
- `audit_logs_enabled`
- `autoscaler`
- `control_plane`
- `count`
- `description`
- `disk_encryption`
- `disks`
- `effect`
- `enabled`
- `endpoint`
- `firewall_id`
- `high_availability`
- `id`
- `instance_id`
- `ipv4`
- `ipv6`
- `k8s_version`
- `key`
- `kubeconfig`
- `label`
- `labels`
- `max`
- `maximum`
- `min`
- `minimum`
- `node_pools`
- `nodes`
- `region`
- `requires_restart`
- `revision-id`
- `servicetoken`
- `size`
- `stack_type`
- `status`
- `subnet_id`
- `tags`
- `taints`
- `tier`
- `type`
- `update_strategy`
- `url`
- `value`
- `vpc_id`

*Related structs analyzed*: LKECluster, LKEClusterCreateOptions, LKEClusterUpdateOptions, LKEClusterAPIEndpoint, LKEClusterKubeconfig, LKEClusterDashboard, LKEVersion, LKETierVersion, LKEClusterRegenerateOptions, LKENodePoolDisk, LKENodePoolAutoscaler, LKENodePoolLinode, LKENodePoolTaint, LKENodePool, LKENodePoolCreateOptions, LKENodePoolUpdateOptions, MaxSlotWALKeepSize, LKEClusterControlPlane, LKEClusterControlPlaneACLAddresses, LKEClusterControlPlaneACL, LKEClusterControlPlaneACLAddressesOptions, LKEClusterControlPlaneACLOptions, LKEClusterControlPlaneOptions, LKEClusterControlPlaneACLUpdateOptions, LKEClusterControlPlaneACLResponse

#### POST /{apiVersion}/lke/clusters/{clusterId}/recycle

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `clusterId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `acl`
- `addresses`
- `apl_enabled`
- `audit_logs_enabled`
- `autoscaler`
- `control_plane`
- `count`
- `description`
- `disk_encryption`
- `disks`
- `effect`
- `enabled`
- `endpoint`
- `firewall_id`
- `high_availability`
- `id`
- `instance_id`
- `ipv4`
- `ipv6`
- `k8s_version`
- `key`
- `kubeconfig`
- `label`
- `labels`
- `max`
- `maximum`
- `min`
- `minimum`
- `node_pools`
- `nodes`
- `region`
- `requires_restart`
- `revision-id`
- `servicetoken`
- `size`
- `stack_type`
- `status`
- `subnet_id`
- `tags`
- `taints`
- `tier`
- `type`
- `update_strategy`
- `url`
- `value`
- `vpc_id`

*Related structs analyzed*: LKECluster, LKEClusterCreateOptions, LKEClusterUpdateOptions, LKEClusterAPIEndpoint, LKEClusterKubeconfig, LKEClusterDashboard, LKEVersion, LKETierVersion, LKEClusterRegenerateOptions, LKENodePoolDisk, LKENodePoolAutoscaler, LKENodePoolLinode, LKENodePoolTaint, LKENodePool, LKENodePoolCreateOptions, LKENodePoolUpdateOptions, MaxSlotWALKeepSize, LKEClusterControlPlane, LKEClusterControlPlaneACLAddresses, LKEClusterControlPlaneACL, LKEClusterControlPlaneACLAddressesOptions, LKEClusterControlPlaneACLOptions, LKEClusterControlPlaneOptions, LKEClusterControlPlaneACLUpdateOptions, LKEClusterControlPlaneACLResponse

#### POST /{apiVersion}/lke/clusters/{clusterId}/regenerate

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `clusterId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `acl`
- `addresses`
- `apl_enabled`
- `audit_logs_enabled`
- `autoscaler`
- `control_plane`
- `count`
- `description`
- `disk_encryption`
- `disks`
- `effect`
- `enabled`
- `endpoint`
- `firewall_id`
- `high_availability`
- `id`
- `instance_id`
- `ipv4`
- `ipv6`
- `k8s_version`
- `key`
- `label`
- `labels`
- `max`
- `maximum`
- `min`
- `minimum`
- `node_pools`
- `nodes`
- `region`
- `requires_restart`
- `revision-id`
- `size`
- `stack_type`
- `status`
- `subnet_id`
- `tags`
- `taints`
- `tier`
- `type`
- `update_strategy`
- `url`
- `value`
- `vpc_id`

*Related structs analyzed*: LKECluster, LKEClusterCreateOptions, LKEClusterUpdateOptions, LKEClusterAPIEndpoint, LKEClusterKubeconfig, LKEClusterDashboard, LKEVersion, LKETierVersion, LKEClusterRegenerateOptions, LKENodePoolDisk, LKENodePoolAutoscaler, LKENodePoolLinode, LKENodePoolTaint, LKENodePool, LKENodePoolCreateOptions, LKENodePoolUpdateOptions, MaxSlotWALKeepSize, LKEClusterControlPlane, LKEClusterControlPlaneACLAddresses, LKEClusterControlPlaneACL, LKEClusterControlPlaneACLAddressesOptions, LKEClusterControlPlaneACLOptions, LKEClusterControlPlaneOptions, LKEClusterControlPlaneACLUpdateOptions, LKEClusterControlPlaneACLResponse

#### POST /{apiVersion}/longview/clients

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `apps` (Optional, type: `object`)
- `apps.apache` (Optional, type: `boolean`)
- `apps.mysql` (Optional, type: `boolean`)
- `apps.nginx` (Optional, type: `boolean`)
- `created` (Optional, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `apache`
- `clients_included`
- `hourly`
- `longview_subscription`
- `monthly`
- `mysql`
- `nginx`
- `price`

*Related structs analyzed*: LongviewClient, LongviewClientCreateOptions, LongviewClientUpdateOptions, LongviewPlan, LongviewPlanUpdateOptions, LongviewSubscription

#### POST /{apiVersion}/monitor/services/{serviceType}/alert-definitions

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4beta...]`)
- `channel_ids` (Required, type: `array[integer]`)
- `rule_criteria` (Required, type: `object`)
- `rule_criteria.rules` (Optional, type: `array[object]`)
- `serviceType` (Required, type: `string`)
- `severity` (Required, type: `enum[0,1,2...]`)
- `trigger_conditions` (Required, type: `object`)
- `trigger_conditions.criteria_condition` (Optional, type: `enum[ALL...]`)
- `trigger_conditions.evaluation_period_seconds` (Optional, type: `integer`)
- `trigger_conditions.polling_interval_seconds` (Optional, type: `integer`)
- `trigger_conditions.trigger_occurrences` (Optional, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `alert`
- `alerts`
- `available_aggregate_functions`
- `dimension_label`
- `dimensions`
- `evaluation_period_seconds`
- `example`
- `id`
- `is_alertable`
- `maximum`
- `metric`
- `metric_type`
- `metrics`
- `minimum`
- `polling_interval_seconds`
- `requires_restart`
- `scope`
- `scrape_interval`
- `service_type`
- `token`
- `type`
- `unit`
- `values`
- `widgets`

*Related structs analyzed*: MonitorService, MonitorServiceAlert, MonitorMetricsDefinition, MonitorDimension, RegionMonitors, PGStatMonitorPGSMEnableQueryPlan, PGStatMonitorPGSMMaxBuckets, PostgresDatabaseConfigInfoPGStatMonitorEnable, MonitorDashboard, MonitorServiceToken, MonitorTokenCreateOptions

#### POST /{apiVersion}/monitor/services/{serviceType}/token

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `serviceType` (Required, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `alert`
- `alerts`
- `available_aggregate_functions`
- `description`
- `dimension_label`
- `dimensions`
- `evaluation_period_seconds`
- `example`
- `expiry`
- `id`
- `is_alertable`
- `label`
- `maximum`
- `metric`
- `metric_type`
- `metrics`
- `minimum`
- `polling_interval_seconds`
- `requires_restart`
- `scope`
- `scopes`
- `scrape_interval`
- `service_type`
- `sharegroup_label`
- `sharegroup_uuid`
- `status`
- `token`
- `token_uuid`
- `type`
- `unit`
- `valid_for_sharegroup_uuid`
- `values`
- `widgets`

*Related structs analyzed*: MonitorService, MonitorServiceAlert, MonitorMetricsDefinition, MonitorDimension, InnoDBFTMinTokenSize, RegionMonitors, PGStatMonitorPGSMEnableQueryPlan, PGStatMonitorPGSMMaxBuckets, PostgresDatabaseConfigInfoPGStatMonitorEnable, ImageShareGroupToken, ImageShareGroupCreateTokenResponse, ImageShareGroupCreateTokenOptions, ImageShareGroupUpdateTokenOptions, MonitorDashboard, MonitorServiceToken, MonitorTokenCreateOptions, Token, TokenCreateOptions, TokenUpdateOptions

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

#### POST /{apiVersion}/networking/firewalls/{firewallId}/devices

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `firewallId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `default_firewall_ids`
- `interfaces`
- `linodes`
- `nodebalancers`

*Related structs analyzed*: DevicesCreationOptions, FirewallSettings, FirewallSettingsUpdateOptions

#### POST /{apiVersion}/networking/ips

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `linode_id` (Required, type: `integer`)
- `public` (Required, type: `boolean`)
- `type` (Required, type: `enum[ipv4...]`)

**Extra in SDK** (found in SDK but not documented in API):

- `assignments`
- `region`

*Related structs analyzed*: LinodesAssignIPsOptions

#### POST /{apiVersion}/networking/ipv6/ranges

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)

**Extra in SDK** (found in SDK but not documented in API):

- `address`
- `allocation_class`
- `global`
- `is_bgp`
- `is_public`
- `link_local`
- `linodes`
- `prefix`
- `range`
- `ranges`
- `region`
- `shared`
- `slaac`
- `slaac_address`
- `vpc`

*Related structs analyzed*: VPCSubnetNodebalancersRanges, VPCSubnetCreateOptionsIPv6, PublicInterfaceIPv6, PublicInterfaceIPv6Range, PublicInterfaceIPv6SLAAC, VPCInterfaceIPv6, VPCInterfaceIPv6SLAAC, VPCInterfaceIPv6Range, PublicInterfaceIPv6CreateOptions, PublicInterfaceIPv6RangeCreateOptions, VPCInterfaceIPv6CreateOptions, VPCInterfaceIPv6SLAACCreateOptions, VPCInterfaceIPv6RangeCreateOptions, VPCIPv6Range, VPCCreateOptionsIPv6, IPv6RangeCreateOptions, VPCIPIPv6Address, InstanceIPv6Response, IPv6Range, InstanceConfigInterfaceIPv6, InstanceConfigInterfaceIPv6SLAAC, InstanceConfigInterfaceIPv6Range, InstanceConfigInterfaceCreateOptionsIPv6, InstanceConfigInterfaceCreateOptionsIPv6SLAAC, InstanceConfigInterfaceCreateOptionsIPv6Range, InstanceConfigInterfaceUpdateOptionsIPv6, InstanceConfigInterfaceUpdateOptionsIPv6SLAAC, InstanceConfigInterfaceUpdateOptionsIPv6Range

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

#### POST /{apiVersion}/object-storage/buckets

**Missing in SDK** (documented in API but not found in SDK structs):

- `acl` (Optional, type: `enum[private,public-read,authenticated-read...]`)
- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `cors_enabled` (Optional, type: `boolean`)
- `endpoint_type` (Optional, type: `enum[E0,E1,E2...]`)
- `label` (Required, type: `string`)
- `region` (Optional, type: `string`)
- `s3_endpoint` (Optional, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `description`
- `example`
- `maximum`
- `minimum`
- `requires_restart`
- `type`

*Related structs analyzed*: PGStatMonitorPGSMMaxBuckets

#### POST /{apiVersion}/object-storage/buckets/{regionId}/{bucket}/access

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `bucket` (Required, type: `string`)
- `regionId` (Required, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `acl_xml`
- `bucket_name`
- `cluster`
- `cors_xml`
- `description`
- `example`
- `id`
- `maximum`
- `minimum`
- `permissions`
- `region`
- `requires_restart`
- `roles`
- `type`

*Related structs analyzed*: PGStatMonitorPGSMMaxBuckets, UserAccess, AccountAccess, ObjectStorageBucketAccess, ObjectStorageBucketAccessV2, ObjectStorageBucketUpdateAccessOptions, ObjectStorageKeyBucketAccess

#### POST /{apiVersion}/object-storage/buckets/{regionId}/{bucket}/object-url

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `bucket` (Required, type: `string`)
- `content_type` (Optional, type: `string`)
- `expires_in` (Optional, type: `integer`)
- `method` (Required, type: `string`)
- `name` (Required, type: `string`)
- `regionId` (Required, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `description`
- `example`
- `maximum`
- `minimum`
- `requires_restart`
- `type`

*Related structs analyzed*: PGStatMonitorPGSMMaxBuckets

#### POST /{apiVersion}/object-storage/buckets/{regionId}/{bucket}/ssl

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `bucket` (Required, type: `string`)
- `certificate` (Required, type: `string`)
- `private_key` (Required, type: `string`)
- `regionId` (Required, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `ca_certificate`
- `description`
- `example`
- `maximum`
- `minimum`
- `requires_restart`
- `type`

*Related structs analyzed*: MySQLDatabaseSSL, PGStatMonitorPGSMMaxBuckets, PostgresDatabaseSSL

#### POST /{apiVersion}/object-storage/cancel

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)

#### POST /{apiVersion}/object-storage/keys

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)

#### POST /{apiVersion}/profile/sshkeys

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `created` (Optional, type: `string`)
- `ssh_key` (Optional, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `authentication_type`
- `authorized_keys`
- `code`
- `completed`
- `credit`
- `datetime`
- `email`
- `email_notifications`
- `ip`
- `ip_whitelist_enabled`
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

#### POST /{apiVersion}/profile/tfa-disable

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

#### POST /{apiVersion}/profile/tfa-enable

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

#### POST /{apiVersion}/profile/tfa-enable-confirm

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `tfa_code` (Optional, type: `string`)

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

#### POST /{apiVersion}/profile/tokens

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `expiry` (Optional, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `authentication_type`
- `authorized_keys`
- `code`
- `completed`
- `credit`
- `datetime`
- `description`
- `email`
- `email_notifications`
- `example`
- `id`
- `ip`
- `ip_whitelist_enabled`
- `last_remote_addr`
- `lish_auth_method`
- `maximum`
- `minimum`
- `pending`
- `referrals`
- `requires_restart`
- `restricted`
- `status`
- `thumbnail_url`
- `timezone`
- `total`
- `two_factor_auth`
- `type`
- `uid`
- `url`
- `user_agent`
- `username`
- `verified_phone_number`
- `website`

*Related structs analyzed*: InnoDBFTMinTokenSize, ProfileReferrals, Profile, ProfileUpdateOptions, ProfileLogin, ProfileDevice, ProfileApp

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

#### PUT /{apiVersion}/account/oauth-clients/{clientId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `clientId` (Required, type: `string`)
- `public` (Optional, type: `boolean`)
- `redirect_uri` (Optional, type: `string`)
- `secret` (Optional, type: `string`)
- `thumbnail_url` (Optional, type: `string`)

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
- `interfaces_for_new_linodes`
- `is_sender`
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
- `tax_id`
- `token`
- `type`
- `unavailable`
- `used`
- `when`
- `zip`

*Related structs analyzed*: AccountMaintenance, AccountSettings, AccountSettingsUpdateOptions, AccountServiceTransfer, AccountServiceTransferEntity, AccountServiceTransferRequestOptions, Account, AccountUpdateOptions, AccountAgreements, AccountAgreementsUpdateOptions, AccountRolePermissions, AccountAccess, AccountTransfer, AccountTransferRegion, AccountAvailability, AccountBetaProgram, AccountBetaProgramCreateOpts

#### PUT /{apiVersion}/account/settings

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)

**Extra in SDK** (found in SDK but not documented in API):

- `account_access`
- `active_promotions`
- `active_since`
- `address_1`
- `address_2`
- `available`
- `balance`
- `balance_uninvoiced`
- `billable`
- `billing_source`
- `capabilities`
- `city`
- `company`
- `country`
- `credit_card`
- `default_firewall_ids`
- `default_route`
- `description`
- `email`
- `entities`
- `entity`
- `entity_access`
- `eu_model`
- `euuid`
- `first_name`
- `id`
- `is_sender`
- `label`
- `last_name`
- `linodes`
- `maintenance_policy_set`
- `master_service_agreement`
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

*Related structs analyzed*: AccountMaintenance, AccountSettings, AccountSettingsUpdateOptions, AccountServiceTransfer, AccountServiceTransferEntity, AccountServiceTransferRequestOptions, Account, AccountUpdateOptions, AccountAgreements, AccountAgreementsUpdateOptions, InterfaceSettings, InterfaceSettingsUpdateOptions, AccountRolePermissions, AccountAccess, AccountTransfer, AccountTransferRegion, AccountAvailability, FirewallSettings, FirewallSettingsUpdateOptions, AccountBetaProgram, AccountBetaProgramCreateOpts

#### PUT /{apiVersion}/account/users/{username}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `last_login` (Optional, type: `object`)
- `last_login.login_datetime` (Optional, type: `string`)
- `last_login.status` (Optional, type: `enum[successful,failed...]`)
- `password_created` (Optional, type: `string`)
- `restricted` (Optional, type: `boolean`)
- `ssh_keys` (Optional, type: `array[string]`)
- `tfa_enabled` (Optional, type: `boolean`)
- `username` (Required, type: `string`)
- `verified_phone_number` (Optional, type: `string`)

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

#### PUT /{apiVersion}/account/users/{username}/grants

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `global.account_access` (Optional, type: `enum[read_only,read_write...]`)
- `global.add_databases` (Optional, type: `boolean`)
- `global.add_domains` (Optional, type: `boolean`)
- `global.add_firewalls` (Optional, type: `boolean`)
- `global.add_images` (Optional, type: `boolean`)
- `global.add_linodes` (Optional, type: `boolean`)
- `global.add_longview` (Optional, type: `boolean`)
- `global.add_nodebalancers` (Optional, type: `boolean`)
- `global.add_stackscripts` (Optional, type: `boolean`)
- `global.add_volumes` (Optional, type: `boolean`)
- `global.add_vpcs` (Optional, type: `boolean`)
- `global.cancel_account` (Optional, type: `boolean`)
- `global.child_account_access` (Optional, type: `boolean`)
- `global.longview_subscription` (Optional, type: `boolean`)
- `username` (Required, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `account_access`
- `active_promotions`
- `active_since`
- `add_databases`
- `add_domains`
- `add_firewalls`
- `add_images`
- `add_linodes`
- `add_longview`
- `add_nodebalancers`
- `add_stackscripts`
- `add_volumes`
- `add_vpcs`
- `address_1`
- `address_2`
- `available`
- `backups_enabled`
- `balance`
- `balance_uninvoiced`
- `billable`
- `billing_source`
- `cancel_account`
- `capabilities`
- `child_account_access`
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
- `placement_group`
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

*Related structs analyzed*: AccountMaintenance, GlobalUserGrants, UserGrants, UserGrantsUpdateOptions, AccountSettings, AccountSettingsUpdateOptions, AccountServiceTransfer, AccountServiceTransferEntity, AccountServiceTransferRequestOptions, Account, AccountUpdateOptions, AccountAgreements, AccountAgreementsUpdateOptions, AccountRolePermissions, AccountAccess, AccountTransfer, AccountTransferRegion, AccountAvailability, AccountBetaProgram, AccountBetaProgramCreateOpts

#### PUT /{apiVersion}/databases/mysql/instances/{instanceId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `engine_config.binlog_retention_period` (Optional, type: `integer`)
- `engine_config.mysql` (Optional, type: `object`)
- `engine_config.mysql.connect_timeout` (Optional, type: `integer`)
- `engine_config.mysql.default_time_zone` (Optional, type: `string`)
- `engine_config.mysql.group_concat_max_len` (Optional, type: `integer`)
- `engine_config.mysql.information_schema_stats_expiry` (Optional, type: `integer`)
- `engine_config.mysql.innodb_change_buffer_max_size` (Optional, type: `integer`)
- `engine_config.mysql.innodb_flush_neighbors` (Optional, type: `integer`)
- `engine_config.mysql.innodb_ft_min_token_size` (Optional, type: `integer`)
- `engine_config.mysql.innodb_ft_server_stopword_table` (Optional, type: `string`)
- `engine_config.mysql.innodb_lock_wait_timeout` (Optional, type: `integer`)
- `engine_config.mysql.innodb_log_buffer_size` (Optional, type: `integer`)
- `engine_config.mysql.innodb_online_alter_log_max_size` (Optional, type: `integer`)
- `engine_config.mysql.innodb_read_io_threads` (Optional, type: `integer`)
- `engine_config.mysql.innodb_rollback_on_timeout` (Optional, type: `boolean`)
- `engine_config.mysql.innodb_thread_concurrency` (Optional, type: `integer`)
- `engine_config.mysql.innodb_write_io_threads` (Optional, type: `integer`)
- `engine_config.mysql.interactive_timeout` (Optional, type: `integer`)
- `engine_config.mysql.internal_tmp_mem_storage_engine` (Optional, type: `enum[TempTable,MEMORY...]`)
- `engine_config.mysql.max_allowed_packet` (Optional, type: `integer`)
- `engine_config.mysql.max_heap_table_size` (Optional, type: `integer`)
- `engine_config.mysql.net_buffer_length` (Optional, type: `integer`)
- `engine_config.mysql.net_read_timeout` (Optional, type: `integer`)
- `engine_config.mysql.net_write_timeout` (Optional, type: `integer`)
- `engine_config.mysql.sql_mode` (Optional, type: `string`)
- `engine_config.mysql.sql_require_primary_key` (Optional, type: `boolean`)
- `engine_config.mysql.tmp_table_size` (Optional, type: `integer`)
- `engine_config.mysql.wait_timeout` (Optional, type: `integer`)
- `instanceId` (Required, type: `integer`)
- `private_network.public_access` (Optional, type: `boolean`)
- `private_network.subnet_id` (Optional, type: `integer`)
- `private_network.vpc_id` (Optional, type: `integer`)
- `updates.day_of_week` (Optional, type: `integer`)
- `updates.duration` (Optional, type: `integer`)
- `updates.frequency` (Optional, type: `enum[weekly...]`)
- `updates.hour_of_day` (Optional, type: `integer`)
- `updates.pending` (Optional, type: `array[object]`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `available`
- `binlog_retention_period`
- `ca_certificate`
- `cluster_size`
- `configs`
- `connect_timeout`
- `cpu`
- `data`
- `default_time_zone`
- `description`
- `disk`
- `disks`
- `encrypted`
- `engine`
- `example`
- `filesystem`
- `fork`
- `gpus`
- `group_concat_max_len`
- `hosts`
- `id`
- `information_schema_stats_expiry`
- `innodb_change_buffer_max_size`
- `innodb_flush_neighbors`
- `innodb_ft_min_token_size`
- `innodb_ft_server_stopword_table`
- `innodb_lock_wait_timeout`
- `innodb_log_buffer_size`
- `innodb_online_alter_log_max_size`
- `innodb_read_io_threads`
- `innodb_rollback_on_timeout`
- `innodb_thread_concurrency`
- `innodb_write_io_threads`
- `interactive_timeout`
- `internal_tmp_mem_storage_engine`
- `io`
- `max_allowed_packet`
- `max_heap_table_size`
- `maximum`
- `members`
- `memory`
- `minimum`
- `mysql`
- `net_buffer_length`
- `net_read_timeout`
- `net_write_timeout`
- `netv4`
- `netv6`
- `password`
- `platform`
- `port`
- `region`
- `requires_restart`
- `size`
- `sort_buffer_size`
- `sql_mode`
- `sql_require_primary_key`
- `ssl_connection`
- `status`
- `title`
- `tmp_table_size`
- `total_disk_size_gb`
- `transfer`
- `used_disk_size_gb`
- `username`
- `vcpus`
- `wait_timeout`

*Related structs analyzed*: InstanceStatsData, InstanceStats, MySQLDatabase, MySQLDatabaseEngineConfig, MySQLDatabaseEngineConfigMySQL, MySQLDatabaseConfigInfo, MySQLDatabaseConfigInfoMySQL, MySQLDatabaseConfigInfoBinlogRetentionPeriod, MySQLCreateOptions, MySQLUpdateOptions, MySQLDatabaseCredential, MySQLDatabaseSSL, PostgresDatabaseSSL, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec

#### PUT /{apiVersion}/databases/postgresql/instances/{instanceId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `allow_list` (Optional, type: `array[string]`)
- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `engine_config` (Optional, type: `object`)
- `engine_config.pg` (Optional, type: `object`)
- `engine_config.pg.autovacuum_analyze_scale_factor` (Optional, type: `number`)
- `engine_config.pg.autovacuum_analyze_threshold` (Optional, type: `integer`)
- `engine_config.pg.autovacuum_max_workers` (Optional, type: `integer`)
- `engine_config.pg.autovacuum_naptime` (Optional, type: `integer`)
- `engine_config.pg.autovacuum_vacuum_cost_delay` (Optional, type: `integer`)
- `engine_config.pg.autovacuum_vacuum_cost_limit` (Optional, type: `integer`)
- `engine_config.pg.autovacuum_vacuum_scale_factor` (Optional, type: `number`)
- `engine_config.pg.autovacuum_vacuum_threshold` (Optional, type: `integer`)
- `engine_config.pg.bgwriter_delay` (Optional, type: `integer`)
- `engine_config.pg.bgwriter_flush_after` (Optional, type: `integer`)
- `engine_config.pg.bgwriter_lru_maxpages` (Optional, type: `integer`)
- `engine_config.pg.bgwriter_lru_multiplier` (Optional, type: `number`)
- `engine_config.pg.deadlock_timeout` (Optional, type: `integer`)
- `engine_config.pg.default_toast_compression` (Optional, type: `enum[lz4,pglz...]`)
- `engine_config.pg.idle_in_transaction_session_timeout` (Optional, type: `integer`)
- `engine_config.pg.jit` (Optional, type: `boolean`)
- `engine_config.pg.max_files_per_process` (Optional, type: `integer`)
- `engine_config.pg.max_locks_per_transaction` (Optional, type: `integer`)
- `engine_config.pg.max_logical_replication_workers` (Optional, type: `integer`)
- `engine_config.pg.max_parallel_workers` (Optional, type: `integer`)
- `engine_config.pg.max_parallel_workers_per_gather` (Optional, type: `integer`)
- `engine_config.pg.max_pred_locks_per_transaction` (Optional, type: `integer`)
- `engine_config.pg.max_replication_slots` (Optional, type: `integer`)
- `engine_config.pg.max_slot_wal_keep_size` (Optional, type: `integer`)
- `engine_config.pg.max_stack_depth` (Optional, type: `integer`)
- `engine_config.pg.max_standby_archive_delay` (Optional, type: `integer`)
- `engine_config.pg.max_standby_streaming_delay` (Optional, type: `integer`)
- `engine_config.pg.max_wal_senders` (Optional, type: `integer`)
- `engine_config.pg.max_worker_processes` (Optional, type: `integer`)
- `engine_config.pg.password_encryption` (Optional, type: `enum[scram-sh-256,md5...]`)
- `engine_config.pg.pg_partman_bgw.interval` (Optional, type: `integer`)
- `engine_config.pg.pg_partman_bgw.role` (Optional, type: `string`)
- `engine_config.pg.pg_stat_monitor.pgsm_enable_query_plan` (Optional, type: `boolean`)
- `engine_config.pg.pg_stat_monitor.pgsm_max_buckets` (Optional, type: `integer`)
- `engine_config.pg.pg_stat_statements.track` (Optional, type: `enum[all,top,none...]`)
- `engine_config.pg.synchronous_replication` (Optional, type: `enum[quorum,False...]`)
- `engine_config.pg.temp_file_limit` (Optional, type: `integer`)
- `engine_config.pg.timezone` (Optional, type: `string`)
- `engine_config.pg.track_activity_query_size` (Optional, type: `integer`)
- `engine_config.pg.track_commit_timestamp` (Optional, type: `enum[on,off...]`)
- `engine_config.pg.track_functions` (Optional, type: `enum[all,pl,none...]`)
- `engine_config.pg.track_io_timing` (Optional, type: `enum[on,off...]`)
- `engine_config.pg.wal_sender_timeout` (Optional, type: `integer`)
- `engine_config.pg.wal_writer_delay` (Optional, type: `integer`)
- `engine_config.pg_stat_monitor_enable` (Optional, type: `boolean`)
- `engine_config.pglookout` (Optional, type: `object`)
- `engine_config.pglookout.max_failover_replication_time_lag` (Optional, type: `integer`)
- `engine_config.shared_buffers_percentage` (Optional, type: `number`)
- `engine_config.work_mem` (Optional, type: `integer`)
- `instanceId` (Required, type: `integer`)
- `private_network` (Optional, type: `object`)
- `private_network.public_access` (Optional, type: `boolean`)
- `private_network.subnet_id` (Optional, type: `integer`)
- `private_network.vpc_id` (Optional, type: `integer`)
- `updates` (Optional, type: `object`)
- `updates.day_of_week` (Optional, type: `integer`)
- `updates.duration` (Optional, type: `integer`)
- `updates.frequency` (Optional, type: `enum[weekly...]`)
- `updates.hour_of_day` (Optional, type: `integer`)
- `updates.pending` (Optional, type: `array[object]`)
- `version` (Optional, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `available`
- `ca_certificate`
- `configs`
- `cpu`
- `data`
- `disk`
- `disks`
- `filesystem`
- `gpus`
- `id`
- `io`
- `memory`
- `netv4`
- `netv6`
- `size`
- `status`
- `title`
- `transfer`
- `vcpus`

*Related structs analyzed*: InstanceStatsData, InstanceStats, MySQLDatabaseSSL, PostgresDatabaseSSL, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec

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

#### PUT /{apiVersion}/linode/instances/{linodeId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `alerts` (Optional, type: `object`)
- `alerts.cpu` (Optional, type: `integer`)
- `alerts.io` (Optional, type: `integer`)
- `alerts.network_in` (Optional, type: `integer`)
- `alerts.network_out` (Optional, type: `integer`)
- `alerts.transfer_quota` (Optional, type: `integer`)
- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `backups.available` (Optional, type: `boolean`)
- `backups.enabled` (Optional, type: `boolean`)
- `backups.last_successful` (Optional, type: `string`)
- `backups.schedule` (Optional, type: `object`)
- `backups.schedule.day` (Optional, type: `enum[Scheduling,Sunday,Monday...]`)
- `backups.schedule.window` (Optional, type: `enum[Scheduling,W0,W2...]`)
- `capabilities` (Optional, type: `array[string]`)
- `created` (Optional, type: `string`)
- `disk_encryption` (Optional, type: `string`)
- `group` (Optional, type: `string`)
- `has_user_data` (Optional, type: `boolean`)
- `host_uuid` (Optional, type: `string`)
- `hypervisor` (Optional, type: `enum[kvm...]`)
- `image` (Optional, type: `unknown`)
- `interface_generation` (Optional, type: `enum[legacy_config,linode...]`)
- `ipv4` (Optional, type: `array[string]`)
- `ipv6` (Optional, type: `string`)
- `linodeId` (Required, type: `integer`)
- `lke_cluster_id` (Optional, type: `integer`)
- `maintenance_policy` (Optional, type: `enum[linode/migrate,linode/power_off_on...]`)
- `placement_group` (Optional, type: `object`)
- `placement_group.id` (Optional, type: `integer`)
- `placement_group.label` (Optional, type: `string`)
- `placement_group.placement_group_policy` (Optional, type: `enum[strict,flexible...]`)
- `placement_group.placement_group_type` (Optional, type: `enum[anti_affinity:local...]`)
- `specs` (Optional, type: `object`)
- `specs.disk` (Optional, type: `integer`)
- `specs.gpus` (Optional, type: `integer`)
- `specs.memory` (Optional, type: `integer`)
- `specs.transfer` (Optional, type: `integer`)
- `specs.vcpus` (Optional, type: `integer`)
- `tags` (Optional, type: `array[string]`)
- `updated` (Optional, type: `string`)
- `watchdog_enabled` (Optional, type: `boolean`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `price`
- `public`
- `pvops`
- `region_prices`
- `size`
- `successor`
- `title`
- `transfer`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### PUT /{apiVersion}/linode/instances/{linodeId}/configs/{configId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `comments` (Optional, type: `string`)
- `configId` (Required, type: `integer`)
- `devices` (Optional, type: `object`)
- `devices.sda` (Optional, type: `object`)
- `devices.sda.disk_id` (Optional, type: `integer`)
- `devices.sda.volume_id` (Optional, type: `integer`)
- `devices.sdb` (Optional, type: `object`)
- `devices.sdb.disk_id` (Optional, type: `integer`)
- `devices.sdb.volume_id` (Optional, type: `integer`)
- `devices.sdc` (Optional, type: `object`)
- `devices.sdc.disk_id` (Optional, type: `integer`)
- `devices.sdc.volume_id` (Optional, type: `integer`)
- `devices.sdd` (Optional, type: `object`)
- `devices.sdd.disk_id` (Optional, type: `integer`)
- `devices.sdd.volume_id` (Optional, type: `integer`)
- `devices.sde` (Optional, type: `object`)
- `devices.sde.disk_id` (Optional, type: `integer`)
- `devices.sde.volume_id` (Optional, type: `integer`)
- `devices.sdf` (Optional, type: `object`)
- `devices.sdf.disk_id` (Optional, type: `integer`)
- `devices.sdf.volume_id` (Optional, type: `integer`)
- `devices.sdg` (Optional, type: `object`)
- `devices.sdg.disk_id` (Optional, type: `integer`)
- `devices.sdg.volume_id` (Optional, type: `integer`)
- `devices.sdh` (Optional, type: `object`)
- `devices.sdh.disk_id` (Optional, type: `integer`)
- `devices.sdh.volume_id` (Optional, type: `integer`)
- `helpers` (Optional, type: `object`)
- `helpers.devtmpfs_automount` (Optional, type: `boolean`)
- `helpers.distro` (Optional, type: `boolean`)
- `helpers.modules_dep` (Optional, type: `boolean`)
- `helpers.network` (Optional, type: `boolean`)
- `helpers.updatedb_disabled` (Optional, type: `boolean`)
- `kernel` (Optional, type: `string`)
- `linodeId` (Required, type: `integer`)
- `memory_limit` (Optional, type: `integer`)
- `root_device` (Optional, type: `string`)
- `run_level` (Optional, type: `enum[default,single,binbash...]`)
- `virt_mode` (Optional, type: `enum[paravirt,fullvirt...]`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `instance_id`
- `io`
- `kvm`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### PUT /{apiVersion}/linode/instances/{linodeId}/disks/{diskId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `diskId` (Required, type: `integer`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### PUT /{apiVersion}/linode/instances/{linodeId}/interfaces/settings

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `default_route.ipv4_eligible_interface_ids` (Optional, type: `array[integer]`)
- `default_route.ipv4_interface_id` (Optional, type: `integer`)
- `default_route.ipv6_eligible_interface_ids` (Optional, type: `array[integer]`)
- `default_route.ipv6_interface_id` (Optional, type: `integer`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `backups_enabled`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_firewall_ids`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `ids`
- `instance_id`
- `interfaces`
- `interfaces_for_new_linodes`
- `io`
- `kvm`
- `label`
- `linode_id`
- `longview_subscription`
- `mac_address`
- `maintenance_policy`
- `managed`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `object_storage`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: AccountSettings, AccountSettingsUpdateOptions, InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InterfaceSettings, InterfaceSettingsUpdateOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, FirewallSettings, FirewallSettingsUpdateOptions, LinodeKernel, InstanceConfigInterfacesReorderOptions

#### PUT /{apiVersion}/linode/instances/{linodeId}/interfaces/{interfaceId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `interfaceId` (Required, type: `integer`)
- `linodeId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `ids`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_helper`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InterfaceSettings, InterfaceSettingsUpdateOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel, InstanceConfigInterfacesReorderOptions

#### PUT /{apiVersion}/linode/instances/{linodeId}/ips/{address}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `linodeId` (Required, type: `integer`)
- `rdns` (Required, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `architecture`
- `assignments`
- `available`
- `backups`
- `class`
- `config_id`
- `configs`
- `cpu`
- `data`
- `default_route`
- `deprecated`
- `disk`
- `disks`
- `dry_run`
- `filesystem`
- `firewall_id`
- `gpus`
- `hourly`
- `id`
- `instance_id`
- `interfaces`
- `io`
- `kvm`
- `label`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `netv4`
- `netv6`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `size`
- `status`
- `successor`
- `title`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: InstanceStatsData, InstanceStats, VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, InstanceSnapshot, InstanceSnapshotDisk, InstanceSpec, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### PUT /{apiVersion}/linode/stackscripts/{stackscriptId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `created` (Optional, type: `string`)
- `deployments_active` (Optional, type: `integer`)
- `deployments_total` (Optional, type: `integer`)
- `description` (Optional, type: `string`)
- `images` (Optional, type: `array[string]`)
- `is_public` (Optional, type: `boolean`)
- `mine` (Optional, type: `boolean`)
- `rev_note` (Optional, type: `string`)
- `script` (Optional, type: `string`)
- `stackscriptId` (Required, type: `string`)
- `updated` (Optional, type: `string`)
- `user_defined_fields` (Optional, type: `array[object]`)
- `user_gravatar_id` (Optional, type: `string`)
- `username` (Optional, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `accelerated_devices`
- `active`
- `addons`
- `address`
- `architecture`
- `assignments`
- `backups`
- `class`
- `config_id`
- `default_route`
- `deprecated`
- `disk`
- `dry_run`
- `firewall_id`
- `gpus`
- `hourly`
- `instance_id`
- `interfaces`
- `kvm`
- `linode_id`
- `mac_address`
- `memory`
- `monthly`
- `network_out`
- `price`
- `public`
- `pvops`
- `region`
- `region_prices`
- `status`
- `successor`
- `transfer`
- `type`
- `vcpus`
- `version`
- `vlan`
- `vpc`
- `xen`

*Related structs analyzed*: VPCSubnetLinodeInterface, VPCSubnetLinode, LKENodePoolLinode, LinodeInterface, LinodeInterfaceCreateOptions, LinodeInterfaceUpdateOptions, LinodeInterfacesUpgrade, LinodeInterfacesUpgradeOptions, LinodeEntity, LinodeType, LinodePrice, LinodeBackupsAddon, LinodeAddons, LinodeRegionPrice, LinodeIPAssignment, LinodesAssignIPsOptions, LinodeKernel

#### PUT /{apiVersion}/lke/clusters/{clusterId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `clusterId` (Required, type: `integer`)
- `control_plane.acl` (Optional, type: `object`)
- `control_plane.acl.addresses` (Optional, type: `object`)
- `control_plane.acl.addresses.ipv4` (Optional, type: `array[string]`)
- `control_plane.acl.addresses.ipv6` (Optional, type: `array[string]`)
- `control_plane.acl.enabled` (Optional, type: `boolean`)
- `control_plane.acl.revision-id` (Optional, type: `string`)
- `control_plane.audit_logs_enabled` (Optional, type: `boolean`)
- `control_plane.high_availability` (Optional, type: `boolean`)

**Extra in SDK** (found in SDK but not documented in API):

- `acl`
- `addresses`
- `apl_enabled`
- `audit_logs_enabled`
- `autoscaler`
- `count`
- `description`
- `disk_encryption`
- `disks`
- `effect`
- `enabled`
- `endpoint`
- `firewall_id`
- `high_availability`
- `id`
- `instance_id`
- `ipv4`
- `ipv6`
- `key`
- `kubeconfig`
- `labels`
- `max`
- `maximum`
- `min`
- `minimum`
- `node_pools`
- `nodes`
- `region`
- `requires_restart`
- `revision-id`
- `servicetoken`
- `size`
- `stack_type`
- `status`
- `subnet_id`
- `taints`
- `tier`
- `type`
- `update_strategy`
- `url`
- `value`
- `vpc_id`

*Related structs analyzed*: LKECluster, LKEClusterCreateOptions, LKEClusterUpdateOptions, LKEClusterAPIEndpoint, LKEClusterKubeconfig, LKEClusterDashboard, LKEVersion, LKETierVersion, LKEClusterRegenerateOptions, LKENodePoolDisk, LKENodePoolAutoscaler, LKENodePoolLinode, LKENodePoolTaint, LKENodePool, LKENodePoolCreateOptions, LKENodePoolUpdateOptions, MaxSlotWALKeepSize, LKEClusterControlPlane, LKEClusterControlPlaneACLAddresses, LKEClusterControlPlaneACL, LKEClusterControlPlaneACLAddressesOptions, LKEClusterControlPlaneACLOptions, LKEClusterControlPlaneOptions, LKEClusterControlPlaneACLUpdateOptions, LKEClusterControlPlaneACLResponse

#### PUT /{apiVersion}/lke/clusters/{clusterId}/pools/{poolId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `autoscaler.enabled` (Optional, type: `boolean`)
- `autoscaler.max` (Optional, type: `integer`)
- `autoscaler.min` (Optional, type: `integer`)
- `clusterId` (Required, type: `integer`)
- `poolId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `acl`
- `addresses`
- `apl_enabled`
- `audit_logs_enabled`
- `control_plane`
- `description`
- `disk_encryption`
- `disks`
- `effect`
- `enabled`
- `endpoint`
- `high_availability`
- `id`
- `instance_id`
- `ipv4`
- `ipv6`
- `k8s_version`
- `key`
- `kubeconfig`
- `label`
- `max`
- `maximum`
- `min`
- `minimum`
- `node_pools`
- `nodes`
- `region`
- `requires_restart`
- `revision-id`
- `servicetoken`
- `size`
- `stack_type`
- `status`
- `subnet_id`
- `tier`
- `type`
- `update_strategy`
- `url`
- `value`
- `vpc_id`

*Related structs analyzed*: LKECluster, LKEClusterCreateOptions, LKEClusterUpdateOptions, LKEClusterAPIEndpoint, LKEClusterKubeconfig, LKEClusterDashboard, LKEVersion, LKETierVersion, LKEClusterRegenerateOptions, LKENodePoolDisk, LKENodePoolAutoscaler, LKENodePoolLinode, LKENodePoolTaint, LKENodePool, LKENodePoolCreateOptions, LKENodePoolUpdateOptions, MaxSlotWALKeepSize, LKEClusterControlPlane, LKEClusterControlPlaneACLAddresses, LKEClusterControlPlaneACL, LKEClusterControlPlaneACLAddressesOptions, LKEClusterControlPlaneACLOptions, LKEClusterControlPlaneOptions, LKEClusterControlPlaneACLUpdateOptions, LKEClusterControlPlaneACLResponse

#### PUT /{apiVersion}/longview/clients/{clientId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `apps` (Optional, type: `object`)
- `apps.apache` (Optional, type: `boolean`)
- `apps.mysql` (Optional, type: `boolean`)
- `apps.nginx` (Optional, type: `boolean`)
- `clientId` (Required, type: `integer`)
- `created` (Optional, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `apache`
- `clients_included`
- `hourly`
- `longview_subscription`
- `monthly`
- `mysql`
- `nginx`
- `price`

*Related structs analyzed*: LongviewClient, LongviewClientCreateOptions, LongviewClientUpdateOptions, LongviewPlan, LongviewPlanUpdateOptions, LongviewSubscription

#### PUT /{apiVersion}/longview/plan

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)

**Extra in SDK** (found in SDK but not documented in API):

- `acl`
- `addresses`
- `apache`
- `api_key`
- `audit_logs_enabled`
- `clients_included`
- `description`
- `enabled`
- `example`
- `high_availability`
- `hourly`
- `id`
- `install_code`
- `ipv4`
- `ipv6`
- `label`
- `monthly`
- `mysql`
- `nginx`
- `price`
- `requires_restart`
- `revision-id`
- `type`
- `updated`

*Related structs analyzed*: PGStatMonitorPGSMEnableQueryPlan, LongviewClient, LongviewClientCreateOptions, LongviewClientUpdateOptions, LongviewPlan, LongviewPlanUpdateOptions, LKEClusterControlPlane, LKEClusterControlPlaneACLAddresses, LKEClusterControlPlaneACL, LKEClusterControlPlaneACLAddressesOptions, LKEClusterControlPlaneACLOptions, LKEClusterControlPlaneOptions, LKEClusterControlPlaneACLUpdateOptions, LKEClusterControlPlaneACLResponse, LongviewSubscription

#### PUT /{apiVersion}/monitor/services/{serviceType}/alert-definitions/{alertId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `alertId` (Required, type: `integer`)
- `apiVersion` (Required, type: `enum[v4beta...]`)
- `channel_ids` (Optional, type: `array[integer]`)
- `rule_criteria` (Optional, type: `object`)
- `rule_criteria.rules` (Optional, type: `array[object]`)
- `serviceType` (Required, type: `string`)
- `severity` (Optional, type: `enum[0,1,2...]`)
- `status` (Optional, type: `enum[enabled,disabled...]`)
- `trigger_conditions` (Optional, type: `object`)
- `trigger_conditions.criteria_condition` (Optional, type: `enum[ALL...]`)
- `trigger_conditions.evaluation_period_seconds` (Optional, type: `integer`)
- `trigger_conditions.polling_interval_seconds` (Optional, type: `integer`)
- `trigger_conditions.trigger_occurrences` (Optional, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `alert`
- `alerts`
- `available_aggregate_functions`
- `dimension_label`
- `dimensions`
- `evaluation_period_seconds`
- `example`
- `id`
- `is_alertable`
- `maximum`
- `metric`
- `metric_type`
- `metrics`
- `minimum`
- `polling_interval_seconds`
- `requires_restart`
- `scope`
- `scrape_interval`
- `service_type`
- `token`
- `type`
- `unit`
- `values`
- `widgets`

*Related structs analyzed*: MonitorService, MonitorServiceAlert, MonitorMetricsDefinition, MonitorDimension, RegionMonitors, PGStatMonitorPGSMEnableQueryPlan, PGStatMonitorPGSMMaxBuckets, PostgresDatabaseConfigInfoPGStatMonitorEnable, MonitorDashboard, MonitorServiceToken, MonitorTokenCreateOptions

#### PUT /{apiVersion}/networking/firewalls/settings

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `default_firewall_ids.linode` (Optional, type: `integer`)
- `default_firewall_ids.nodebalancer` (Optional, type: `integer`)
- `default_firewall_ids.public_interface` (Optional, type: `integer`)
- `default_firewall_ids.vpc_interface` (Optional, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `backups_enabled`
- `default_route`
- `interfaces_for_new_linodes`
- `longview_subscription`
- `maintenance_policy`
- `managed`
- `network_helper`
- `object_storage`

*Related structs analyzed*: AccountSettings, AccountSettingsUpdateOptions, InterfaceSettings, InterfaceSettingsUpdateOptions, FirewallSettings, FirewallSettingsUpdateOptions

#### PUT /{apiVersion}/networking/firewalls/{firewallId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `firewallId` (Required, type: `integer`)
- `label` (Optional, type: `string`)
- `status` (Optional, type: `enum[enabled,disabled...]`)
- `tags` (Optional, type: `array[string]`)

**Extra in SDK** (found in SDK but not documented in API):

- `default_firewall_ids`

*Related structs analyzed*: FirewallSettings, FirewallSettingsUpdateOptions

#### PUT /{apiVersion}/networking/firewalls/{firewallId}/rules

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `firewallId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `default_firewall_ids`
- `description`
- `id`
- `inbound_policy`
- `is_service_defined`
- `label`
- `outbound_policy`
- `rules`
- `ruleset`
- `type`
- `version`

*Related structs analyzed*: rulesetOnly, FirewallRuleSet, FirewallSettings, FirewallSettingsUpdateOptions, RuleSet, RuleSetCreateOptions, RuleSetUpdateOptions

#### PUT /{apiVersion}/networking/ips/{address}

**Missing in SDK** (documented in API but not found in SDK structs):

- `address` (Required, type: `string`)
- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `rdns` (Required, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `assignments`
- `region`

*Related structs analyzed*: LinodesAssignIPsOptions

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

#### PUT /{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId}/nodes/{nodeId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `configId` (Required, type: `integer`)
- `nodeBalancerId` (Required, type: `integer`)
- `nodeId` (Required, type: `string`)

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

#### PUT /{apiVersion}/object-storage/buckets/{regionId}/{bucket}/object-acl

**Missing in SDK** (documented in API but not found in SDK structs):

- `acl` (Required, type: `enum[private,public-read,authenticated-read...]`)
- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `bucket` (Required, type: `string`)
- `name` (Required, type: `string`)
- `regionId` (Required, type: `string`)

**Extra in SDK** (found in SDK but not documented in API):

- `description`
- `example`
- `maximum`
- `minimum`
- `requires_restart`
- `type`

*Related structs analyzed*: PGStatMonitorPGSMMaxBuckets

#### PUT /{apiVersion}/object-storage/keys/{keyId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `keyId` (Required, type: `integer`)
- `label` (Optional, type: `string`)
- `regions` (Optional, type: `array[string]`)

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

#### PUT /{apiVersion}/profile/preferences

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

#### PUT /{apiVersion}/profile/sshkeys/{sshKeyId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `sshKeyId` (Required, type: `integer`)

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

#### PUT /{apiVersion}/profile/tokens/{tokenId}

**Missing in SDK** (documented in API but not found in SDK structs):

- `apiVersion` (Required, type: `enum[v4,v4beta...]`)
- `created` (Optional, type: `string`)
- `expiry` (Optional, type: `string`)
- `token` (Optional, type: `string`)
- `tokenId` (Required, type: `integer`)

**Extra in SDK** (found in SDK but not documented in API):

- `authentication_type`
- `authorized_keys`
- `code`
- `completed`
- `credit`
- `datetime`
- `description`
- `email`
- `email_notifications`
- `example`
- `ip`
- `ip_whitelist_enabled`
- `last_remote_addr`
- `lish_auth_method`
- `maximum`
- `minimum`
- `pending`
- `referrals`
- `requires_restart`
- `restricted`
- `status`
- `thumbnail_url`
- `timezone`
- `total`
- `two_factor_auth`
- `type`
- `uid`
- `url`
- `user_agent`
- `username`
- `verified_phone_number`
- `website`

*Related structs analyzed*: InnoDBFTMinTokenSize, ProfileReferrals, Profile, ProfileUpdateOptions, ProfileLogin, ProfileDevice, ProfileApp

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

The analyzer detected 327 endpoint calls in the linodego SDK.

Sample of detected endpoints:

- `DELETE /account/oauth-clients/{id}` (in `account_oauth_client.go`)
- `DELETE /account/payment-methods/{id}` (in `account_payment_methods.go`)
- `DELETE /account/service-transfers/{id}` (in `account_service_transfer.go`)
- `DELETE /account/users/{id}` (in `account_users.go`)
- `DELETE /databases/mysql/instances/{id}` (in `mysql.go`)
- `DELETE /databases/postgresql/instances/{id}` (in `postgres.go`)
- `DELETE /domains/{id}` (in `domains.go`)
- `DELETE /domains/{id}/records/{id}` (in `domain_records.go`)
- `DELETE /linode/instances/{id}` (in `instances.go`)
- `DELETE /linode/instances/{id}/configs/{id}` (in `instance_configs.go`)
- `DELETE /linode/instances/{id}/disks/{id}` (in `instance_disks.go`)
- `DELETE /linode/instances/{id}/interfaces/{id}` (in `interfaces.go`)
- `DELETE /linode/instances/{id}/ips/{id}` (in `instance_ips.go`)
- `DELETE /linode/stackscripts/{id}` (in `stackscripts.go`)
- `DELETE /lke/clusters/{id}` (in `lke_clusters.go`)
- `DELETE /lke/clusters/{id}/kubeconfig` (in `lke_clusters.go`)
- `DELETE /lke/clusters/{id}/nodes/{id}` (in `lke_node_pools.go`)
- `DELETE /lke/clusters/{id}/pools/{id}` (in `lke_node_pools.go`)
- `DELETE /lke/clusters/{id}/servicetoken` (in `lke_clusters.go`)
- `DELETE /locks/{id}` (in `locks.go`)
- `DELETE /longview/clients/{id}` (in `longview.go`)
- `DELETE /monitor/services/{id}/alert-definitions/{id}` (in `monitor_alert_definitions.go`)
- `DELETE /networking/firewalls/rulesets/{id}` (in `firewall_rulesets.go`)
- `DELETE /networking/firewalls/{id}` (in `firewalls.go`)
- `DELETE /networking/firewalls/{id}/devices/{id}` (in `firewall_devices.go`)
- `DELETE /networking/ipv6/ranges/{id}` (in `network_ranges.go`)
- `DELETE /networking/reserved/ips/{id}` (in `network_reserved_ips.go`)
- `DELETE /nodebalancers/{id}` (in `nodebalancer.go`)
- `DELETE /nodebalancers/{id}/configs/{id}` (in `nodebalancer_configs.go`)
- `DELETE /nodebalancers/{id}/configs/{id}/nodes/{id}` (in `nodebalancer_config_nodes.go`)

### SDK Structs Detected

The analyzer detected 510 struct definitions with JSON tags.
