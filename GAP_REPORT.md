# 📊 Linode API Coverage Report

**linodego Go SDK Implementation Analysis**

---

## 🎯 Executive Summary

```text
Total Endpoints:    465
✅ Implemented:     373 (80.2%)
❌ Missing:         92

Progress: [████████████████░░░░] 80.2%
```

---

## 📂 Coverage by Category

### 🟢 Complete Coverage (100%)

- **Access keys**: 5/5
- **Account agreements**: 2/2
- **Account availability**: 2/2
- **Account transfer**: 1/1
- **Advanced parameters**: 2/2
- **Backups**: 6/6
- **Beta programs**: 5/5
- **Cluster dashboard**: 1/1
- **Clusters**: 9/9
- **Configuration profiles**: 5/5
- **Configurations**: 6/6
- **Credentials**: 4/4
- **Databases**: 17/17
- **Devices**: 4/4
- **Disks**: 8/8
- **Domain zone file**: 1/1
- **Domains**: 7/7
- **Endpoints**: 1/1
- **Engines**: 2/2
- **Events**: 3/3
- **Firewall settings**: 2/2
- **Grants**: 1/1
- **IPv6 pools**: 1/1
- **IPv6 ranges**: 4/4
- **Invoices**: 3/3
- **Kernels**: 2/2
- **Kubeconfigs**: 2/2
- **LKE API endpoints**: 1/1
- **LKE service tokens**: 1/1
- **Linode instances**: 15/15
- **Linode interfaces**: 10/10
- **Logins**: 4/4
- **Longview clients**: 5/5
- **Longview plans**: 2/2
- **Longview subscriptions**: 2/2
- **Maintenance policies**: 1/1
- **Maintenances**: 1/1
- **Node pools**: 6/6
- **NodeBalancer types**: 1/1
- **NodeBalancers**: 6/6
- **Nodes**: 8/8
- **Notifications**: 1/1
- **OAuth apps**: 3/3
- **OAuth clients**: 6/6
- **OAuth preferences**: 2/2
- **Personal access tokens**: 5/5
- **Profile**: 2/2
- **Promo credits**: 1/1
- **Records**: 5/5
- **Regions**: 4/4
- **SSH keys**: 5/5
- **SSL certificates**: 2/2
- **Security questions**: 2/2
- **Service transfers**: 5/5
- **StackScripts**: 5/5
- **Statistics**: 5/5
- **TLS/SSL certificates**: 3/3
- **Tags**: 4/4
- **Templates**: 2/2
- **Trusted devices**: 3/3
- **Two-factor authentication**: 3/3
- **Types**: 2/2
- **Users**: 7/7
- **VPC subnets**: 5/5
- **VPCs**: 7/7
- **Volume types**: 1/1
- **Volumes**: 10/10

### 🟡 High Coverage (75-99%)

- **IP addresses**: 12/13 (92%)
- **Object Storage**: 5/6 (83%)
- **Payment methods**: 4/5 (80%)
- **Firewalls**: 11/14 (79%)
- **Buckets**: 9/12 (75%)

### 🟠 Medium Coverage (50-74%)

- **Account**: 2/3 (67%)
- **Account settings**: 2/3 (67%)
- **Phone number**: 2/3 (67%)
- **Metrics**: 5/8 (62%)
- **Alerts**: 4/7 (57%)
- **Identity Management**: 2/4 (50%)
- **LKE versions**: 2/4 (50%)
- **Linode types**: 1/2 (50%)
- **Payments**: 3/6 (50%)
- **Support tickets**: 2/4 (50%)
- **VLANs**: 1/2 (50%)

### 🔴 Low Coverage (< 50%)

- **Image sharing**: 7/22 (32%)
- **Configuration profile interfaces**: 1/6 (17%)
- **Attachments**: 0/1 (0%)
- **Child accounts**: 0/3 (0%)
- **Control Plane ACL**: 0/3 (0%)
- **Entity transfers**: 0/5 (0%)
- **IPv4 addresses**: 0/2 (0%)
- **Images**: 0/7 (0%)
- **LKE types**: 0/1 (0%)
- **Logs**: 0/12 (0%)
- **Longview types**: 0/1 (0%)
- **Managed Linode settings**: 0/3 (0%)
- **Managed SSH keys**: 0/1 (0%)
- **Managed contacts**: 0/5 (0%)
- **Managed credentials**: 0/6 (0%)
- **Managed issues**: 0/2 (0%)
- **Managed service monitors**: 0/7 (0%)
- **Managed statistics**: 0/1 (0%)
- **Network transfer prices**: 0/1 (0%)
- **OAuth client**: 0/2 (0%)
- **Placement groups**: 0/7 (0%)
- **Replies**: 0/2 (0%)

---

## ❌ Missing Endpoints by Category

### 📁 Logs

🔴 **Coverage**: 0/12 (0%)

**Missing 12 endpoint(s):**

#### `GET` — 6 endpoint(s)

- **`/{apiVersion}/monitor/streams`**
  - *List streams*

- **`/{apiVersion}/monitor/streams/destinations`**
  - *List destinations*

- **`/{apiVersion}/monitor/streams/destinations/{destinationId}`**
  - *Get a destination*

- **`/{apiVersion}/monitor/streams/destinations/{destinationId}/history`**
  - *Get a destination's history*

- **`/{apiVersion}/monitor/streams/{streamId}`**
  - *Get a stream*

- **`/{apiVersion}/monitor/streams/{streamId}/history`**
  - *Get a stream's history*

#### `POST` — 2 endpoint(s)

- **`/{apiVersion}/monitor/streams`**
  - *Create a stream*

- **`/{apiVersion}/monitor/streams/destinations`**
  - *Create a destination*

#### `PUT` — 2 endpoint(s)

- **`/{apiVersion}/monitor/streams/destinations/{destinationId}`**
  - *Update a destination*

- **`/{apiVersion}/monitor/streams/{streamId}`**
  - *Update a stream*

#### `DELETE` — 2 endpoint(s)

- **`/{apiVersion}/monitor/streams/destinations/{destinationId}`**
  - *Delete a destination*

- **`/{apiVersion}/monitor/streams/{streamId}`**
  - *Delete a stream*


### 📁 Managed service monitors

🔴 **Coverage**: 0/7 (0%)

**Missing 7 endpoint(s):**

#### `GET` — 2 endpoint(s)

- **`/{apiVersion}/managed/services`**
  - *List managed services*

- **`/{apiVersion}/managed/services/{serviceId}`**
  - *Get a managed service monitor*

#### `POST` — 3 endpoint(s)

- **`/{apiVersion}/managed/services`**
  - *Create a managed service*

- **`/{apiVersion}/managed/services/{serviceId}/disable`**
  - *Disable a managed service monitor*

- **`/{apiVersion}/managed/services/{serviceId}/enable`**
  - *Enable a managed service monitor*

#### `PUT` — 1 endpoint(s)

- **`/{apiVersion}/managed/services/{serviceId}`**
  - *Update a managed service monitor*

#### `DELETE` — 1 endpoint(s)

- **`/{apiVersion}/managed/services/{serviceId}`**
  - *Delete a managed service monitor*


### 📁 Managed credentials

🔴 **Coverage**: 0/6 (0%)

**Missing 6 endpoint(s):**

#### `GET` — 2 endpoint(s)

- **`/{apiVersion}/managed/credentials`**
  - *List managed credentials*

- **`/{apiVersion}/managed/credentials/{credentialId}`**
  - *Get a managed credential*

#### `POST` — 3 endpoint(s)

- **`/{apiVersion}/managed/credentials`**
  - *Create a managed credential*

- **`/{apiVersion}/managed/credentials/{credentialId}/revoke`**
  - *Delete a managed credential*

- **`/{apiVersion}/managed/credentials/{credentialId}/update`**
  - *Update a managed credential's username and passwor...*

#### `PUT` — 1 endpoint(s)

- **`/{apiVersion}/managed/credentials/{credentialId}`**
  - *Update a managed credential*


### 📁 Configuration profile interfaces

🔴 **Coverage**: 1/6 (17%)

**Missing 5 endpoint(s):**

#### `GET` — 2 endpoint(s)

- **`/{apiVersion}/linode/instances/{linodeId}/configs/{configId}/interfaces`**
  - *List configuration profile interfaces*

- **`/{apiVersion}/linode/instances/{linodeId}/configs/{configId}/interfaces/{interfaceId}`**
  - *Get a configuration profile interface*

#### `POST` — 1 endpoint(s)

- **`/{apiVersion}/linode/instances/{linodeId}/configs/{configId}/interfaces/order`**
  - *Reorder configuration profile interfaces*

#### `PUT` — 1 endpoint(s)

- **`/{apiVersion}/linode/instances/{linodeId}/configs/{configId}/interfaces/{interfaceId}`**
  - *Update a configuration profile interface*

#### `DELETE` — 1 endpoint(s)

- **`/{apiVersion}/linode/instances/{linodeId}/configs/{configId}/interfaces/{interfaceId}`**
  - *Delete a configuration profile interface*


### 📁 Entity transfers

🔴 **Coverage**: 0/5 (0%)

**Missing 5 endpoint(s):**

#### `GET` — 2 endpoint(s)

- **`/{apiVersion}/account/entity-transfers`**
  - *List entity transfers (deprecated)*

- **`/{apiVersion}/account/entity-transfers/{token}`**
  - *Get an entity transfer (deprecated)*

#### `POST` — 2 endpoint(s)

- **`/{apiVersion}/account/entity-transfers`**
  - *Create an entity transfer (deprecated)*

- **`/{apiVersion}/account/entity-transfers/{token}/accept`**
  - *Accept an entity transfer (deprecated)*

#### `DELETE` — 1 endpoint(s)

- **`/{apiVersion}/account/entity-transfers/{token}`**
  - *Cancel an entity transfer (deprecated)*


### 📁 Managed contacts

🔴 **Coverage**: 0/5 (0%)

**Missing 5 endpoint(s):**

#### `GET` — 2 endpoint(s)

- **`/{apiVersion}/managed/contacts`**
  - *List managed contacts*

- **`/{apiVersion}/managed/contacts/{contactId}`**
  - *Get a managed contact*

#### `POST` — 1 endpoint(s)

- **`/{apiVersion}/managed/contacts`**
  - *Create a managed contact*

#### `PUT` — 1 endpoint(s)

- **`/{apiVersion}/managed/contacts/{contactId}`**
  - *Update a managed contact*

#### `DELETE` — 1 endpoint(s)

- **`/{apiVersion}/managed/contacts/{contactId}`**
  - *Delete a managed contact*


### 📁 Alerts

🟠 **Coverage**: 4/7 (57%)

**Missing 3 endpoint(s):**

#### `GET` — 3 endpoint(s)

- **`/{apiVersion}/monitor/alert-channels`**
  - *List alert channels*

- **`/{apiVersion}/monitor/alert-definitions`**
  - *List alert definitions*

- **`/{apiVersion}/monitor/services/{serviceType}/alert-definitions`**
  - *List alert definitions for a service type*


### 📁 Buckets

🟡 **Coverage**: 9/12 (75%)

**Missing 3 endpoint(s):**

#### `GET` — 2 endpoint(s)

- **`/{apiVersion}/object-storage/buckets/{regionId}/{bucket}/object-acl`**
  - *Get an Object Storage object ACL configuration*

- **`/{apiVersion}/object-storage/buckets/{regionId}/{bucket}/object-list`**
  - *List Object Storage bucket contents*

#### `PUT` — 1 endpoint(s)

- **`/{apiVersion}/object-storage/buckets/{regionId}/{bucket}/access`**
  - *Update access to an Object Storage bucket*


### 📁 Firewalls

🟡 **Coverage**: 11/14 (79%)

**Missing 3 endpoint(s):**

#### `GET` — 1 endpoint(s)

- **`/{apiVersion}/networking/firewalls/{firewallId}/history/rules/{version}`**
  - *Get a firewall rule version*

#### `POST` — 1 endpoint(s)

- **`/{apiVersion}/linode/instances/{linodeId}/firewalls/apply`**
  - *Apply a Linode's firewalls*

#### `PUT` — 1 endpoint(s)

- **`/{apiVersion}/nodebalancers/{nodeBalancerId}/firewalls`**
  - *Update a NodeBalancer's firewalls*


### 📁 Image sharing

🔴 **Coverage**: 7/22 (32%)

**Missing 3 endpoint(s):**

#### `GET` — 2 endpoint(s)

- **`/{apiVersion}/images/sharegroups`**
  - *List share groups*

- **`/{apiVersion}/images/sharegroups/tokens`**
  - *List a user's tokens*

#### `POST` — 1 endpoint(s)

- **`/{apiVersion}/images/sharegroups`**
  - *Create a share group*


### 📁 Images

🔴 **Coverage**: 0/7 (0%)

**Missing 3 endpoint(s):**

#### `GET` — 1 endpoint(s)

- **`/{apiVersion}/images`**
  - *List images*

#### `POST` — 2 endpoint(s)

- **`/{apiVersion}/images`**
  - *Create an image*

- **`/{apiVersion}/images/upload`**
  - *Upload an image*


### 📁 Managed Linode settings

🔴 **Coverage**: 0/3 (0%)

**Missing 3 endpoint(s):**

#### `GET` — 2 endpoint(s)

- **`/{apiVersion}/managed/linode-settings`**
  - *List managed Linode settings*

- **`/{apiVersion}/managed/linode-settings/{linodeId}`**
  - *Get a Linode's managed settings*

#### `PUT` — 1 endpoint(s)

- **`/{apiVersion}/managed/linode-settings/{linodeId}`**
  - *Update a Linode's managed settings*


### 📁 Metrics

🟠 **Coverage**: 5/8 (62%)

**Missing 3 endpoint(s):**

#### `GET` — 2 endpoint(s)

- **`/{apiVersion}/monitor/services/{serviceType}/dashboards`**
  - *List dashboards for a service type*

- **`/{apiVersion}/monitor/services/{serviceType}/metric-definitions`**
  - *List metrics for a service type*

#### `POST` — 1 endpoint(s)

- **`/{apiVersion}/monitor/services/{serviceType}/metrics`**
  - *Get an entity's metrics*


### 📁 Payments

🟠 **Coverage**: 3/6 (50%)

**Missing 3 endpoint(s):**

#### `POST` — 3 endpoint(s)

- **`/{apiVersion}/account/credit-card`**
  - *Add or edit a credit card (deprecated)*

- **`/{apiVersion}/account/payments/paypal`**
  - *Stage a PayPal payment (deprecated)*

- **`/{apiVersion}/account/payments/paypal/execute`**
  - *Execute a PayPal payment (deprecated)*


### 📁 IPv4 addresses

🔴 **Coverage**: 0/2 (0%)

**Missing 2 endpoint(s):**

#### `POST` — 2 endpoint(s)

- **`/{apiVersion}/networking/ipv4/assign`**
  - *Assign IPv4s to Linodes*

- **`/{apiVersion}/networking/ipv4/share`**
  - *Configure IPv4 sharing*


### 📁 Managed issues

🔴 **Coverage**: 0/2 (0%)

**Missing 2 endpoint(s):**

#### `GET` — 2 endpoint(s)

- **`/{apiVersion}/managed/issues`**
  - *List managed issues*

- **`/{apiVersion}/managed/issues/{issueId}`**
  - *Get a managed issue*


### 📁 OAuth client

🔴 **Coverage**: 0/2 (0%)

**Missing 2 endpoint(s):**

#### `GET` — 1 endpoint(s)

- **`/{apiVersion}/account/oauth-clients/{clientId}/thumbnail`**
  - *Get the OAuth client's thumbnail*

#### `PUT` — 1 endpoint(s)

- **`/{apiVersion}/account/oauth-clients/{clientId}/thumbnail`**
  - *Update the OAuth client's thumbnail*


### 📁 Placement groups

🔴 **Coverage**: 0/7 (0%)

**Missing 2 endpoint(s):**

#### `GET` — 1 endpoint(s)

- **`/{apiVersion}/placement/groups`**
  - *List placement groups*

#### `POST` — 1 endpoint(s)

- **`/{apiVersion}/placement/groups`**
  - *Create a placement group*


### 📁 Replies

🔴 **Coverage**: 0/2 (0%)

**Missing 2 endpoint(s):**

#### `GET` — 1 endpoint(s)

- **`/{apiVersion}/support/tickets/{ticketId}/replies`**
  - *List replies*

#### `POST` — 1 endpoint(s)

- **`/{apiVersion}/support/tickets/{ticketId}/replies`**
  - *Create a reply*


### 📁 Support tickets

🟠 **Coverage**: 2/4 (50%)

**Missing 2 endpoint(s):**

#### `POST` — 2 endpoint(s)

- **`/{apiVersion}/support/tickets`**
  - *Open a support ticket*

- **`/{apiVersion}/support/tickets/{ticketId}/close`**
  - *Close a support ticket*


### 📁 Account

🟠 **Coverage**: 2/3 (67%)

**Missing 1 endpoint(s):**

#### `POST` — 1 endpoint(s)

- **`/{apiVersion}/account/cancel`**
  - *Delete your account*


### 📁 Account settings

🟠 **Coverage**: 2/3 (67%)

**Missing 1 endpoint(s):**

#### `POST` — 1 endpoint(s)

- **`/{apiVersion}/account/settings/managed-enable`**
  - *Enable Linode Managed*


### 📁 Attachments

🔴 **Coverage**: 0/1 (0%)

**Missing 1 endpoint(s):**

#### `POST` — 1 endpoint(s)

- **`/{apiVersion}/support/tickets/{ticketId}/attachments`**
  - *Create a support ticket attachment*


### 📁 Child accounts

🔴 **Coverage**: 0/3 (0%)

**Missing 1 endpoint(s):**

#### `GET` — 1 endpoint(s)

- **`/{apiVersion}/account/child-accounts`**
  - *List child accounts*


### 📁 IP addresses

🟡 **Coverage**: 12/13 (92%)

**Missing 1 endpoint(s):**

#### `GET` — 1 endpoint(s)

- **`/{apiVersion}/vpcs/{vpcId}/ips`**
  - *List a VPC's IP addresses*


### 📁 LKE types

🔴 **Coverage**: 0/1 (0%)

**Missing 1 endpoint(s):**

#### `GET` — 1 endpoint(s)

- **`/{apiVersion}/lke/types`**
  - *List Kubernetes types*


### 📁 LKE versions

🟠 **Coverage**: 2/4 (50%)

**Missing 1 endpoint(s):**

#### `GET` — 1 endpoint(s)

- **`/{apiVersion}/lke/versions`**
  - *List LKE Kubernetes versions (non-enterprise)*


### 📁 Linode types

🟠 **Coverage**: 1/2 (50%)

**Missing 1 endpoint(s):**

#### `GET` — 1 endpoint(s)

- **`/{apiVersion}/linode/types`**
  - *List types*


### 📁 Longview types

🔴 **Coverage**: 0/1 (0%)

**Missing 1 endpoint(s):**

#### `GET` — 1 endpoint(s)

- **`/{apiVersion}/longview/types`**
  - *List Longview types*


### 📁 Managed SSH keys

🔴 **Coverage**: 0/1 (0%)

**Missing 1 endpoint(s):**

#### `GET` — 1 endpoint(s)

- **`/{apiVersion}/managed/credentials/sshkey`**
  - *Get a managed SSH key*


### 📁 Managed statistics

🔴 **Coverage**: 0/1 (0%)

**Missing 1 endpoint(s):**

#### `GET` — 1 endpoint(s)

- **`/{apiVersion}/managed/stats`**
  - *List managed stats*


### 📁 Network transfer prices

🔴 **Coverage**: 0/1 (0%)

**Missing 1 endpoint(s):**

#### `GET` — 1 endpoint(s)

- **`/{apiVersion}/network-transfer/prices`**
  - *List network transfer prices*


### 📁 Object Storage

🟡 **Coverage**: 5/6 (83%)

**Missing 1 endpoint(s):**

#### `GET` — 1 endpoint(s)

- **`/{apiVersion}/object-storage/types`**
  - *List Object Storage types*


### 📁 Payment methods

🟡 **Coverage**: 4/5 (80%)

**Missing 1 endpoint(s):**

#### `POST` — 1 endpoint(s)

- **`/{apiVersion}/account/payment-methods/{paymentMethodId}/make-default`**
  - *Set a default payment method*


### 📁 Phone number

🟠 **Coverage**: 2/3 (67%)

**Missing 1 endpoint(s):**

#### `DELETE` — 1 endpoint(s)

- **`/{apiVersion}/profile/phone-number`**
  - *Delete a phone number*


### 📁 VLANs

🟠 **Coverage**: 1/2 (50%)

**Missing 1 endpoint(s):**

#### `DELETE` — 1 endpoint(s)

- **`/{apiVersion}/networking/vlans/{regionId}/{label}`**
  - *Delete a VLAN*


---

## 📊 Summary Table

| Category | Implemented | Total | Coverage | Status |
|----------|-------------|-------|----------|--------|
| Access keys | 5 | 5 | 100% | ✅ Complete |
| Account | 2 | 3 | 67% | 🟠 Medium |
| Account agreements | 2 | 2 | 100% | ✅ Complete |
| Account availability | 2 | 2 | 100% | ✅ Complete |
| Account settings | 2 | 3 | 67% | 🟠 Medium |
| Account transfer | 1 | 1 | 100% | ✅ Complete |
| Advanced parameters | 2 | 2 | 100% | ✅ Complete |
| Alerts | 4 | 7 | 57% | 🟠 Medium |
| Attachments | 0 | 1 | 0% | 🔴 Low |
| Backups | 6 | 6 | 100% | ✅ Complete |
| Beta programs | 5 | 5 | 100% | ✅ Complete |
| Buckets | 9 | 12 | 75% | 🟡 High |
| Child accounts | 0 | 3 | 0% | 🔴 Low |
| Cluster dashboard | 1 | 1 | 100% | ✅ Complete |
| Clusters | 9 | 9 | 100% | ✅ Complete |
| Configuration profile interfaces | 1 | 6 | 17% | 🔴 Low |
| Configuration profiles | 5 | 5 | 100% | ✅ Complete |
| Configurations | 6 | 6 | 100% | ✅ Complete |
| Control Plane ACL | 0 | 3 | 0% | 🔴 Low |
| Credentials | 4 | 4 | 100% | ✅ Complete |
| Databases | 17 | 17 | 100% | ✅ Complete |
| Devices | 4 | 4 | 100% | ✅ Complete |
| Disks | 8 | 8 | 100% | ✅ Complete |
| Domain zone file | 1 | 1 | 100% | ✅ Complete |
| Domains | 7 | 7 | 100% | ✅ Complete |
| Endpoints | 1 | 1 | 100% | ✅ Complete |
| Engines | 2 | 2 | 100% | ✅ Complete |
| Entity transfers | 0 | 5 | 0% | 🔴 Low |
| Events | 3 | 3 | 100% | ✅ Complete |
| Firewall settings | 2 | 2 | 100% | ✅ Complete |
| Firewalls | 11 | 14 | 79% | 🟡 High |
| Grants | 1 | 1 | 100% | ✅ Complete |
| IP addresses | 12 | 13 | 92% | 🟡 High |
| IPv4 addresses | 0 | 2 | 0% | 🔴 Low |
| IPv6 pools | 1 | 1 | 100% | ✅ Complete |
| IPv6 ranges | 4 | 4 | 100% | ✅ Complete |
| Identity Management | 2 | 4 | 50% | 🟠 Medium |
| Image sharing | 7 | 22 | 32% | 🔴 Low |
| Images | 0 | 7 | 0% | 🔴 Low |
| Invoices | 3 | 3 | 100% | ✅ Complete |
| Kernels | 2 | 2 | 100% | ✅ Complete |
| Kubeconfigs | 2 | 2 | 100% | ✅ Complete |
| LKE API endpoints | 1 | 1 | 100% | ✅ Complete |
| LKE service tokens | 1 | 1 | 100% | ✅ Complete |
| LKE types | 0 | 1 | 0% | 🔴 Low |
| LKE versions | 2 | 4 | 50% | 🟠 Medium |
| Linode instances | 15 | 15 | 100% | ✅ Complete |
| Linode interfaces | 10 | 10 | 100% | ✅ Complete |
| Linode types | 1 | 2 | 50% | 🟠 Medium |
| Logins | 4 | 4 | 100% | ✅ Complete |
| Logs | 0 | 12 | 0% | 🔴 Low |
| Longview clients | 5 | 5 | 100% | ✅ Complete |
| Longview plans | 2 | 2 | 100% | ✅ Complete |
| Longview subscriptions | 2 | 2 | 100% | ✅ Complete |
| Longview types | 0 | 1 | 0% | 🔴 Low |
| Maintenance policies | 1 | 1 | 100% | ✅ Complete |
| Maintenances | 1 | 1 | 100% | ✅ Complete |
| Managed Linode settings | 0 | 3 | 0% | 🔴 Low |
| Managed SSH keys | 0 | 1 | 0% | 🔴 Low |
| Managed contacts | 0 | 5 | 0% | 🔴 Low |
| Managed credentials | 0 | 6 | 0% | 🔴 Low |
| Managed issues | 0 | 2 | 0% | 🔴 Low |
| Managed service monitors | 0 | 7 | 0% | 🔴 Low |
| Managed statistics | 0 | 1 | 0% | 🔴 Low |
| Metrics | 5 | 8 | 62% | 🟠 Medium |
| Network transfer prices | 0 | 1 | 0% | 🔴 Low |
| Node pools | 6 | 6 | 100% | ✅ Complete |
| NodeBalancer types | 1 | 1 | 100% | ✅ Complete |
| NodeBalancers | 6 | 6 | 100% | ✅ Complete |
| Nodes | 8 | 8 | 100% | ✅ Complete |
| Notifications | 1 | 1 | 100% | ✅ Complete |
| OAuth apps | 3 | 3 | 100% | ✅ Complete |
| OAuth client | 0 | 2 | 0% | 🔴 Low |
| OAuth clients | 6 | 6 | 100% | ✅ Complete |
| OAuth preferences | 2 | 2 | 100% | ✅ Complete |
| Object Storage | 5 | 6 | 83% | 🟡 High |
| Payment methods | 4 | 5 | 80% | 🟡 High |
| Payments | 3 | 6 | 50% | 🟠 Medium |
| Personal access tokens | 5 | 5 | 100% | ✅ Complete |
| Phone number | 2 | 3 | 67% | 🟠 Medium |
| Placement groups | 0 | 7 | 0% | 🔴 Low |
| Profile | 2 | 2 | 100% | ✅ Complete |
| Promo credits | 1 | 1 | 100% | ✅ Complete |
| Records | 5 | 5 | 100% | ✅ Complete |
| Regions | 4 | 4 | 100% | ✅ Complete |
| Replies | 0 | 2 | 0% | 🔴 Low |
| SSH keys | 5 | 5 | 100% | ✅ Complete |
| SSL certificates | 2 | 2 | 100% | ✅ Complete |
| Security questions | 2 | 2 | 100% | ✅ Complete |
| Service transfers | 5 | 5 | 100% | ✅ Complete |
| StackScripts | 5 | 5 | 100% | ✅ Complete |
| Statistics | 5 | 5 | 100% | ✅ Complete |
| Support tickets | 2 | 4 | 50% | 🟠 Medium |
| TLS/SSL certificates | 3 | 3 | 100% | ✅ Complete |
| Tags | 4 | 4 | 100% | ✅ Complete |
| Templates | 2 | 2 | 100% | ✅ Complete |
| Trusted devices | 3 | 3 | 100% | ✅ Complete |
| Two-factor authentication | 3 | 3 | 100% | ✅ Complete |
| Types | 2 | 2 | 100% | ✅ Complete |
| Users | 7 | 7 | 100% | ✅ Complete |
| VLANs | 1 | 2 | 50% | 🟠 Medium |
| VPC subnets | 5 | 5 | 100% | ✅ Complete |
| VPCs | 7 | 7 | 100% | ✅ Complete |
| Volume types | 1 | 1 | 100% | ✅ Complete |
| Volumes | 10 | 10 | 100% | ✅ Complete |

---

## 📝 Report Details

- **Generated**: 2026-03-10 17:24 UTC
- **Analysis Method**: Static code analysis with comprehensive pattern matching
- **OpenAPI Spec Version**: 4.219.1
- **Pattern Detection**: Includes inline `formatAPIPath()` with CRUD helpers

### Detection Patterns

This analysis detects the following patterns:

1. **Variable assignment**: `e := formatAPIPath(...); doGETRequest(..., e)`
2. **Direct strings**: `doGETRequest(..., "path")`
3. **Inline paginated**: `getPaginatedResults(..., formatAPIPath(...), opts)`
4. **Inline CRUD**: `doPUTRequest[T](..., formatAPIPath(...), opts)`

---

*Generated by Gap Analysis Tool v7 with improved inline pattern detection*
