# Linode API to linodego SDK Gap Report

## Report Metadata

- **Generated**: 2026-03-10 17:09:38 UTC
- **OpenAPI Spec Version**: 4.219.1
- **Analysis Type**: Static Code Analysis

## Executive Summary

- **Total API Endpoints**: 465
- **Implemented in SDK**: 344 (74.0%)
- **Missing from SDK**: 121
  - *Of which deprecated*: 8

## Endpoint Coverage by Category

### Access keys
**Coverage**: 5/5 (100%)

### Account
**Coverage**: 2/3 (67%)

**Missing Endpoints:**

- `POST /{apiVersion}/account/cancel` - Delete your account

### Account agreements
**Coverage**: 2/2 (100%)

### Account availability
**Coverage**: 2/2 (100%)

### Account settings
**Coverage**: 2/3 (67%)

**Missing Endpoints:**

- `POST /{apiVersion}/account/settings/managed-enable` - Enable Linode Managed

### Account transfer
**Coverage**: 1/1 (100%)

### Advanced parameters
**Coverage**: 2/2 (100%)

### Alerts
**Coverage**: 4/7 (57%)

**Missing Endpoints:**

- `GET /{apiVersion}/monitor/alert-channels` - List alert channels
- `GET /{apiVersion}/monitor/alert-definitions` - List alert definitions
- `GET /{apiVersion}/monitor/services/{serviceType}/alert-definitions` - List alert definitions for a service type

### Attachments
**Coverage**: 0/1 (0%)

**Missing Endpoints:**

- `POST /{apiVersion}/support/tickets/{ticketId}/attachments` - Create a support ticket attachment

### Backups
**Coverage**: 6/6 (100%)

### Beta programs
**Coverage**: 5/5 (100%)

### Buckets
**Coverage**: 9/12 (75%)

**Missing Endpoints:**

- `GET /{apiVersion}/object-storage/buckets/{regionId}/{bucket}/object-acl` - Get an Object Storage object ACL configuration
- `GET /{apiVersion}/object-storage/buckets/{regionId}/{bucket}/object-list` - List Object Storage bucket contents
- `PUT /{apiVersion}/object-storage/buckets/{regionId}/{bucket}/access` - Update access to an Object Storage bucket

### Child accounts
**Coverage**: 0/3 (0%)

**Missing Endpoints:**

- `GET /{apiVersion}/account/child-accounts` - List child accounts
- `GET /{apiVersion}/account/child-accounts/{euuId}` - Get a child account
- `POST /{apiVersion}/account/child-accounts/{euuId}/token` - Create a proxy user token

### Cluster dashboard
**Coverage**: 1/1 (100%)

### Clusters
**Coverage**: 9/9 (100%)

### Configuration profile interfaces
**Coverage**: 1/6 (17%)

**Missing Endpoints:**

- `DELETE /{apiVersion}/linode/instances/{linodeId}/configs/{configId}/interfaces/{interfaceId}` - Delete a configuration profile interface
- `GET /{apiVersion}/linode/instances/{linodeId}/configs/{configId}/interfaces` - List configuration profile interfaces
- `GET /{apiVersion}/linode/instances/{linodeId}/configs/{configId}/interfaces/{interfaceId}` - Get a configuration profile interface
- `POST /{apiVersion}/linode/instances/{linodeId}/configs/{configId}/interfaces/order` - Reorder configuration profile interfaces
- `PUT /{apiVersion}/linode/instances/{linodeId}/configs/{configId}/interfaces/{interfaceId}` - Update a configuration profile interface

### Configuration profiles
**Coverage**: 5/5 (100%)

### Configurations
**Coverage**: 6/6 (100%)

### Control Plane ACL
**Coverage**: 0/3 (0%)

**Missing Endpoints:**

- `DELETE /{apiVersion}/lke/clusters/{clusterId}/control_plane_acl` - Delete the control plane access control list
- `GET /{apiVersion}/lke/clusters/{clusterId}/control_plane_acl` - Get the control plane access control list
- `PUT /{apiVersion}/lke/clusters/{clusterId}/control_plane_acl` - Update the control plane access control list

### Credentials
**Coverage**: 4/4 (100%)

### Databases
**Coverage**: 17/17 (100%)

### Devices
**Coverage**: 4/4 (100%)

### Disks
**Coverage**: 8/8 (100%)

### Domain zone file
**Coverage**: 1/1 (100%)

### Domains
**Coverage**: 7/7 (100%)

### Endpoints
**Coverage**: 1/1 (100%)

### Engines
**Coverage**: 2/2 (100%)

### Entity transfers
**Coverage**: 0/5 (0%)

**Missing Endpoints:**

- `DELETE /{apiVersion}/account/entity-transfers/{token}` - Cancel an entity transfer (deprecated)
- `GET /{apiVersion}/account/entity-transfers` - List entity transfers (deprecated)
- `GET /{apiVersion}/account/entity-transfers/{token}` - Get an entity transfer (deprecated)
- `POST /{apiVersion}/account/entity-transfers` - Create an entity transfer (deprecated)
- `POST /{apiVersion}/account/entity-transfers/{token}/accept` - Accept an entity transfer (deprecated)

### Events
**Coverage**: 3/3 (100%)

### Firewall settings
**Coverage**: 2/2 (100%)

### Firewalls
**Coverage**: 11/14 (79%)

**Missing Endpoints:**

- `GET /{apiVersion}/networking/firewalls/{firewallId}/history/rules/{version}` - Get a firewall rule version
- `POST /{apiVersion}/linode/instances/{linodeId}/firewalls/apply` - Apply a Linode's firewalls
- `PUT /{apiVersion}/nodebalancers/{nodeBalancerId}/firewalls` - Update a NodeBalancer's firewalls

### Grants
**Coverage**: 1/1 (100%)

### IP addresses
**Coverage**: 12/13 (92%)

**Missing Endpoints:**

- `GET /{apiVersion}/vpcs/{vpcId}/ips` - List a VPC's IP addresses

### IPv4 addresses
**Coverage**: 0/2 (0%)

**Missing Endpoints:**

- `POST /{apiVersion}/networking/ipv4/assign` - Assign IPv4s to Linodes
- `POST /{apiVersion}/networking/ipv4/share` - Configure IPv4 sharing

### IPv6 pools
**Coverage**: 1/1 (100%)

### IPv6 ranges
**Coverage**: 4/4 (100%)

### Identity Management
**Coverage**: 2/4 (50%)

**Missing Endpoints:**

- `GET /{apiVersion}/iam/users/{username}/role-permissions` - Get a user's access level
- `PUT /{apiVersion}/iam/users/{username}/role-permissions` - Update a user's access level

### Image sharing
**Coverage**: 7/22 (32%)

**Missing Endpoints:**

- `DELETE /{apiVersion}/images/sharegroups/tokens/{tokenUuid}` - Delete a token
- `DELETE /{apiVersion}/images/sharegroups/{sharegroupId}` - Delete a share group
- `DELETE /{apiVersion}/images/sharegroups/{sharegroupId}/images/{imageId}` - Revoke access to a shared image
- `DELETE /{apiVersion}/images/sharegroups/{sharegroupId}/members/{tokenUuid}` - Revoke a membership token
- `GET /{apiVersion}/images/sharegroups` - List share groups
- `GET /{apiVersion}/images/sharegroups/tokens` - List a user's tokens
- `GET /{apiVersion}/images/sharegroups/tokens/{tokenUuid}/sharegroup` - Get a token's share group
- `GET /{apiVersion}/images/sharegroups/{sharegroupId}/members/{tokenUuid}` - Get a membership token
- `POST /{apiVersion}/images/sharegroups` - Create a share group
- `POST /{apiVersion}/images/sharegroups/tokens` - Create a token
- `POST /{apiVersion}/images/sharegroups/{sharegroupId}/members` - Add members to a share group
- `PUT /{apiVersion}/images/sharegroups/tokens/{tokenUuid}` - Update a token
- `PUT /{apiVersion}/images/sharegroups/{sharegroupId}` - Update a share group
- `PUT /{apiVersion}/images/sharegroups/{sharegroupId}/images/{imageId}` - Update a shared image
- `PUT /{apiVersion}/images/sharegroups/{sharegroupId}/members/{tokenUuid}` - Update a membership token

### Images
**Coverage**: 0/7 (0%)

**Missing Endpoints:**

- `DELETE /{apiVersion}/images/{imageId}` - Delete an image
- `GET /{apiVersion}/images` - List images
- `GET /{apiVersion}/images/{imageId}` - Get an image
- `POST /{apiVersion}/images` - Create an image
- `POST /{apiVersion}/images/upload` - Upload an image
- `POST /{apiVersion}/images/{imageId}/regions` - Replicate an image
- `PUT /{apiVersion}/images/{imageId}` - Update an image

### Invoices
**Coverage**: 3/3 (100%)

### Kernels
**Coverage**: 2/2 (100%)

### Kubeconfigs
**Coverage**: 2/2 (100%)

### LKE API endpoints
**Coverage**: 1/1 (100%)

### LKE service tokens
**Coverage**: 1/1 (100%)

### LKE types
**Coverage**: 0/1 (0%)

**Missing Endpoints:**

- `GET /{apiVersion}/lke/types` - List Kubernetes types

### LKE versions
**Coverage**: 2/4 (50%)

**Missing Endpoints:**

- `GET /{apiVersion}/lke/tiers/{tier}/versions/{version}` - Get an LKE Kubernetes version (any tier)
- `GET /{apiVersion}/lke/versions` - List LKE Kubernetes versions (non-enterprise)

### Linode instances
**Coverage**: 15/15 (100%)

### Linode interfaces
**Coverage**: 10/10 (100%)

### Linode types
**Coverage**: 1/2 (50%)

**Missing Endpoints:**

- `GET /{apiVersion}/linode/types` - List types

### Logins
**Coverage**: 4/4 (100%)

### Logs
**Coverage**: 0/12 (0%)

**Missing Endpoints:**

- `DELETE /{apiVersion}/monitor/streams/destinations/{destinationId}` - Delete a destination
- `DELETE /{apiVersion}/monitor/streams/{streamId}` - Delete a stream
- `GET /{apiVersion}/monitor/streams` - List streams
- `GET /{apiVersion}/monitor/streams/destinations` - List destinations
- `GET /{apiVersion}/monitor/streams/destinations/{destinationId}` - Get a destination
- `GET /{apiVersion}/monitor/streams/destinations/{destinationId}/history` - Get a destination's history
- `GET /{apiVersion}/monitor/streams/{streamId}` - Get a stream
- `GET /{apiVersion}/monitor/streams/{streamId}/history` - Get a stream's history
- `POST /{apiVersion}/monitor/streams` - Create a stream
- `POST /{apiVersion}/monitor/streams/destinations` - Create a destination
- `PUT /{apiVersion}/monitor/streams/destinations/{destinationId}` - Update a destination
- `PUT /{apiVersion}/monitor/streams/{streamId}` - Update a stream

### Longview clients
**Coverage**: 5/5 (100%)

### Longview plans
**Coverage**: 2/2 (100%)

### Longview subscriptions
**Coverage**: 2/2 (100%)

### Longview types
**Coverage**: 0/1 (0%)

**Missing Endpoints:**

- `GET /{apiVersion}/longview/types` - List Longview types

### Maintenance policies
**Coverage**: 1/1 (100%)

### Maintenances
**Coverage**: 1/1 (100%)

### Managed Linode settings
**Coverage**: 0/3 (0%)

**Missing Endpoints:**

- `GET /{apiVersion}/managed/linode-settings` - List managed Linode settings
- `GET /{apiVersion}/managed/linode-settings/{linodeId}` - Get a Linode's managed settings
- `PUT /{apiVersion}/managed/linode-settings/{linodeId}` - Update a Linode's managed settings

### Managed SSH keys
**Coverage**: 0/1 (0%)

**Missing Endpoints:**

- `GET /{apiVersion}/managed/credentials/sshkey` - Get a managed SSH key

### Managed contacts
**Coverage**: 0/5 (0%)

**Missing Endpoints:**

- `DELETE /{apiVersion}/managed/contacts/{contactId}` - Delete a managed contact
- `GET /{apiVersion}/managed/contacts` - List managed contacts
- `GET /{apiVersion}/managed/contacts/{contactId}` - Get a managed contact
- `POST /{apiVersion}/managed/contacts` - Create a managed contact
- `PUT /{apiVersion}/managed/contacts/{contactId}` - Update a managed contact

### Managed credentials
**Coverage**: 0/6 (0%)

**Missing Endpoints:**

- `GET /{apiVersion}/managed/credentials` - List managed credentials
- `GET /{apiVersion}/managed/credentials/{credentialId}` - Get a managed credential
- `POST /{apiVersion}/managed/credentials` - Create a managed credential
- `POST /{apiVersion}/managed/credentials/{credentialId}/revoke` - Delete a managed credential
- `POST /{apiVersion}/managed/credentials/{credentialId}/update` - Update a managed credential's username and passwor...
- `PUT /{apiVersion}/managed/credentials/{credentialId}` - Update a managed credential

### Managed issues
**Coverage**: 0/2 (0%)

**Missing Endpoints:**

- `GET /{apiVersion}/managed/issues` - List managed issues
- `GET /{apiVersion}/managed/issues/{issueId}` - Get a managed issue

### Managed service monitors
**Coverage**: 0/7 (0%)

**Missing Endpoints:**

- `DELETE /{apiVersion}/managed/services/{serviceId}` - Delete a managed service monitor
- `GET /{apiVersion}/managed/services` - List managed services
- `GET /{apiVersion}/managed/services/{serviceId}` - Get a managed service monitor
- `POST /{apiVersion}/managed/services` - Create a managed service
- `POST /{apiVersion}/managed/services/{serviceId}/disable` - Disable a managed service monitor
- `POST /{apiVersion}/managed/services/{serviceId}/enable` - Enable a managed service monitor
- `PUT /{apiVersion}/managed/services/{serviceId}` - Update a managed service monitor

### Managed statistics
**Coverage**: 0/1 (0%)

**Missing Endpoints:**

- `GET /{apiVersion}/managed/stats` - List managed stats

### Metrics
**Coverage**: 5/8 (62%)

**Missing Endpoints:**

- `GET /{apiVersion}/monitor/services/{serviceType}/dashboards` - List dashboards for a service type
- `GET /{apiVersion}/monitor/services/{serviceType}/metric-definitions` - List metrics for a service type
- `POST /{apiVersion}/monitor/services/{serviceType}/metrics` - Get an entity's metrics

### Network transfer prices
**Coverage**: 0/1 (0%)

**Missing Endpoints:**

- `GET /{apiVersion}/network-transfer/prices` - List network transfer prices

### Node pools
**Coverage**: 6/6 (100%)

### NodeBalancer types
**Coverage**: 1/1 (100%)

### NodeBalancers
**Coverage**: 6/6 (100%)

### Nodes
**Coverage**: 8/8 (100%)

### Notifications
**Coverage**: 1/1 (100%)

### OAuth apps
**Coverage**: 3/3 (100%)

### OAuth client
**Coverage**: 0/2 (0%)

**Missing Endpoints:**

- `GET /{apiVersion}/account/oauth-clients/{clientId}/thumbnail` - Get the OAuth client's thumbnail
- `PUT /{apiVersion}/account/oauth-clients/{clientId}/thumbnail` - Update the OAuth client's thumbnail

### OAuth clients
**Coverage**: 6/6 (100%)

### OAuth preferences
**Coverage**: 2/2 (100%)

### Object Storage
**Coverage**: 5/6 (83%)

**Missing Endpoints:**

- `GET /{apiVersion}/object-storage/types` - List Object Storage types

### Payment methods
**Coverage**: 4/5 (80%)

**Missing Endpoints:**

- `POST /{apiVersion}/account/payment-methods/{paymentMethodId}/make-default` - Set a default payment method

### Payments
**Coverage**: 3/6 (50%)

**Missing Endpoints:**

- `POST /{apiVersion}/account/credit-card` - Add or edit a credit card (deprecated)
- `POST /{apiVersion}/account/payments/paypal` - Stage a PayPal payment (deprecated)
- `POST /{apiVersion}/account/payments/paypal/execute` - Execute a PayPal payment (deprecated)

### Personal access tokens
**Coverage**: 5/5 (100%)

### Phone number
**Coverage**: 2/3 (67%)

**Missing Endpoints:**

- `DELETE /{apiVersion}/profile/phone-number` - Delete a phone number

### Placement groups
**Coverage**: 0/7 (0%)

**Missing Endpoints:**

- `DELETE /{apiVersion}/placement/groups/{groupId}` - Delete a placement group
- `GET /{apiVersion}/placement/groups` - List placement groups
- `GET /{apiVersion}/placement/groups/{groupId}` - Get a placement group
- `POST /{apiVersion}/placement/groups` - Create a placement group
- `POST /{apiVersion}/placement/groups/{groupId}/assign` - Assign a placement group
- `POST /{apiVersion}/placement/groups/{groupId}/unassign` - Unassign a placement group
- `PUT /{apiVersion}/placement/groups/{groupId}` - Update a placement group

### Profile
**Coverage**: 2/2 (100%)

### Promo credits
**Coverage**: 1/1 (100%)

### Records
**Coverage**: 5/5 (100%)

### Regions
**Coverage**: 4/4 (100%)

### Replies
**Coverage**: 0/2 (0%)

**Missing Endpoints:**

- `GET /{apiVersion}/support/tickets/{ticketId}/replies` - List replies
- `POST /{apiVersion}/support/tickets/{ticketId}/replies` - Create a reply

### SSH keys
**Coverage**: 5/5 (100%)

### SSL certificates
**Coverage**: 2/2 (100%)

### Security questions
**Coverage**: 2/2 (100%)

### Service transfers
**Coverage**: 5/5 (100%)

### StackScripts
**Coverage**: 5/5 (100%)

### Statistics
**Coverage**: 5/5 (100%)

### Support tickets
**Coverage**: 2/4 (50%)

**Missing Endpoints:**

- `POST /{apiVersion}/support/tickets` - Open a support ticket
- `POST /{apiVersion}/support/tickets/{ticketId}/close` - Close a support ticket

### TLS/SSL certificates
**Coverage**: 3/3 (100%)

### Tags
**Coverage**: 4/4 (100%)

### Templates
**Coverage**: 2/2 (100%)

### Trusted devices
**Coverage**: 3/3 (100%)

### Two-factor authentication
**Coverage**: 3/3 (100%)

### Types
**Coverage**: 2/2 (100%)

### Users
**Coverage**: 7/7 (100%)

### VLANs
**Coverage**: 1/2 (50%)

**Missing Endpoints:**

- `DELETE /{apiVersion}/networking/vlans/{regionId}/{label}` - Delete a VLAN

### VPC subnets
**Coverage**: 5/5 (100%)

### VPCs
**Coverage**: 7/7 (100%)

### Volume types
**Coverage**: 1/1 (100%)

### Volumes
**Coverage**: 10/10 (100%)
