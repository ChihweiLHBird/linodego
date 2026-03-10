# Linode API v4 SDK Gap Report

_Source spec:_ linode-api-openapi `openapi.json` (main branch) fetched on 2026-03-10. SDK analyzed: this repo at current HEAD. Paths normalize `{apiVersion}` and format placeholders to `{}` for comparison.

## Coverage Summary
- Documented endpoints: 465
- SDK-implemented endpoints: 388
- Missing endpoints: 77
- SDK endpoints not in spec: 25
- Implemented endpoints with parameter mapping gaps: 127

## Endpoint Coverage
| Method | Path | Status | SDK Function |
|---|---|---|---|
| GET | /{apiVersion}/account | Implemented | GetAccount |
| PUT | /{apiVersion}/account | Implemented | UpdateAccount |
| POST | /{apiVersion}/account/agreements | Implemented | AcknowledgeAccountAgreements |
| GET | /{apiVersion}/account/agreements | Implemented | GetAccountAgreements |
| GET | /{apiVersion}/account/availability | Implemented | ListAccountAvailabilities |
| GET | /{apiVersion}/account/availability/{regionId} | Implemented | GetAccountAvailability |
| POST | /{apiVersion}/account/betas | Implemented | JoinBetaProgram |
| GET | /{apiVersion}/account/betas | Implemented | ListAccountBetaPrograms |
| GET | /{apiVersion}/account/betas/{betaId} | Implemented | GetAccountBetaProgram |
| POST | /{apiVersion}/account/cancel | Missing |  |
| GET | /{apiVersion}/account/child-accounts | Implemented | ListChildAccounts |
| GET | /{apiVersion}/account/child-accounts/{euuId} | Implemented | GetChildAccount |
| POST | /{apiVersion}/account/child-accounts/{euuId}/token | Implemented | CreateChildAccountToken |
| POST | /{apiVersion}/account/credit-card | Missing |  |
| POST | /{apiVersion}/account/entity-transfers | Missing |  |
| GET | /{apiVersion}/account/entity-transfers | Missing |  |
| GET | /{apiVersion}/account/entity-transfers/{token} | Missing |  |
| DELETE | /{apiVersion}/account/entity-transfers/{token} | Missing |  |
| POST | /{apiVersion}/account/entity-transfers/{token}/accept | Missing |  |
| GET | /{apiVersion}/account/events | Implemented | ListEvents |
| GET | /{apiVersion}/account/events/{eventId} | Implemented | GetEvent |
| POST | /{apiVersion}/account/events/{eventId}/seen | Implemented | MarkEventsSeen |
| GET | /{apiVersion}/account/invoices | Implemented | ListInvoices |
| GET | /{apiVersion}/account/invoices/{invoiceId} | Implemented | GetInvoice |
| GET | /{apiVersion}/account/invoices/{invoiceId}/items | Implemented | ListInvoiceItems |
| GET | /{apiVersion}/account/logins | Implemented | ListLogins |
| GET | /{apiVersion}/account/logins/{loginId} | Implemented | GetLogin |
| GET | /{apiVersion}/account/maintenance | Implemented | ListMaintenances |
| GET | /{apiVersion}/account/notifications | Implemented | ListNotifications |
| POST | /{apiVersion}/account/oauth-clients | Implemented | CreateOAuthClient |
| GET | /{apiVersion}/account/oauth-clients | Implemented | ListOAuthClients |
| GET | /{apiVersion}/account/oauth-clients/{clientId} | Implemented | GetOAuthClient |
| PUT | /{apiVersion}/account/oauth-clients/{clientId} | Implemented | UpdateOAuthClient |
| DELETE | /{apiVersion}/account/oauth-clients/{clientId} | Implemented | DeleteOAuthClient |
| POST | /{apiVersion}/account/oauth-clients/{clientId}/reset-secret | Implemented | ResetOAuthClientSecret |
| GET | /{apiVersion}/account/oauth-clients/{clientId}/thumbnail | Missing |  |
| PUT | /{apiVersion}/account/oauth-clients/{clientId}/thumbnail | Missing |  |
| POST | /{apiVersion}/account/payment-methods | Implemented | AddPaymentMethod |
| GET | /{apiVersion}/account/payment-methods | Implemented | ListPaymentMethods |
| GET | /{apiVersion}/account/payment-methods/{paymentMethodId} | Implemented | GetPaymentMethod |
| DELETE | /{apiVersion}/account/payment-methods/{paymentMethodId} | Implemented | DeletePaymentMethod |
| POST | /{apiVersion}/account/payment-methods/{paymentMethodId}/make-default | Missing |  |
| POST | /{apiVersion}/account/payments | Implemented | CreatePayment |
| GET | /{apiVersion}/account/payments | Implemented | ListPayments |
| POST | /{apiVersion}/account/payments/paypal | Missing |  |
| POST | /{apiVersion}/account/payments/paypal/execute | Missing |  |
| GET | /{apiVersion}/account/payments/{paymentId} | Implemented | GetPayment |
| POST | /{apiVersion}/account/promo-codes | Implemented | AddPromoCode |
| POST | /{apiVersion}/account/service-transfers | Implemented | RequestAccountServiceTransfer |
| GET | /{apiVersion}/account/service-transfers | Implemented | ListAccountServiceTransfer |
| GET | /{apiVersion}/account/service-transfers/{token} | Implemented | GetAccountServiceTransfer |
| DELETE | /{apiVersion}/account/service-transfers/{token} | Implemented | CancelAccountServiceTransfer |
| POST | /{apiVersion}/account/service-transfers/{token}/accept | Implemented | AcceptAccountServiceTransfer |
| GET | /{apiVersion}/account/settings | Implemented | GetAccountSettings |
| PUT | /{apiVersion}/account/settings | Implemented | UpdateAccountSettings |
| POST | /{apiVersion}/account/settings/managed-enable | Missing |  |
| GET | /{apiVersion}/account/transfer | Implemented | GetAccountTransfer |
| POST | /{apiVersion}/account/users | Implemented | CreateUser |
| GET | /{apiVersion}/account/users | Implemented | ListUsers |
| GET | /{apiVersion}/account/users/{username} | Implemented | GetUser |
| PUT | /{apiVersion}/account/users/{username} | Implemented | UpdateUser |
| DELETE | /{apiVersion}/account/users/{username} | Implemented | DeleteUser |
| GET | /{apiVersion}/account/users/{username}/grants | Implemented | GetUserGrants |
| PUT | /{apiVersion}/account/users/{username}/grants | Implemented | UpdateUserGrants |
| GET | /{apiVersion}/betas | Implemented | ListBetaPrograms |
| GET | /{apiVersion}/betas/{betaId} | Implemented | GetBetaProgram |
| GET | /{apiVersion}/databases/engines | Implemented | ListDatabaseEngines |
| GET | /{apiVersion}/databases/engines/{engineId} | Implemented | GetDatabaseEngine |
| GET | /{apiVersion}/databases/instances | Implemented | ListDatabases |
| GET | /{apiVersion}/databases/mysql/config | Implemented | GetMySQLDatabaseConfig |
| POST | /{apiVersion}/databases/mysql/instances | Implemented | CreateMySQLDatabase |
| GET | /{apiVersion}/databases/mysql/instances | Implemented | ListMySQLDatabases |
| GET | /{apiVersion}/databases/mysql/instances/{instanceId} | Implemented | GetMySQLDatabase |
| PUT | /{apiVersion}/databases/mysql/instances/{instanceId} | Implemented | UpdateMySQLDatabase |
| DELETE | /{apiVersion}/databases/mysql/instances/{instanceId} | Implemented | DeleteMySQLDatabase |
| GET | /{apiVersion}/databases/mysql/instances/{instanceId}/credentials | Implemented | GetMySQLDatabaseCredentials |
| POST | /{apiVersion}/databases/mysql/instances/{instanceId}/credentials/reset | Implemented | ResetMySQLDatabaseCredentials |
| POST | /{apiVersion}/databases/mysql/instances/{instanceId}/patch | Implemented | PatchMySQLDatabase |
| POST | /{apiVersion}/databases/mysql/instances/{instanceId}/resume | Implemented | ResumeMySQLDatabase |
| GET | /{apiVersion}/databases/mysql/instances/{instanceId}/ssl | Implemented | GetMySQLDatabaseSSL |
| POST | /{apiVersion}/databases/mysql/instances/{instanceId}/suspend | Implemented | SuspendMySQLDatabase |
| GET | /{apiVersion}/databases/postgresql/config | Implemented | GetPostgresDatabaseConfig |
| POST | /{apiVersion}/databases/postgresql/instances | Implemented | CreatePostgresDatabase |
| GET | /{apiVersion}/databases/postgresql/instances | Implemented | ListPostgresDatabases |
| GET | /{apiVersion}/databases/postgresql/instances/{instanceId} | Implemented | GetPostgresDatabase |
| PUT | /{apiVersion}/databases/postgresql/instances/{instanceId} | Implemented | UpdatePostgresDatabase |
| DELETE | /{apiVersion}/databases/postgresql/instances/{instanceId} | Implemented | DeletePostgresDatabase |
| GET | /{apiVersion}/databases/postgresql/instances/{instanceId}/credentials | Implemented | GetPostgresDatabaseCredentials |
| POST | /{apiVersion}/databases/postgresql/instances/{instanceId}/credentials/reset | Implemented | ResetPostgresDatabaseCredentials |
| POST | /{apiVersion}/databases/postgresql/instances/{instanceId}/patch | Implemented | PatchPostgresDatabase |
| POST | /{apiVersion}/databases/postgresql/instances/{instanceId}/resume | Implemented | ResumePostgresDatabase |
| GET | /{apiVersion}/databases/postgresql/instances/{instanceId}/ssl | Implemented | GetPostgresDatabaseSSL |
| POST | /{apiVersion}/databases/postgresql/instances/{instanceId}/suspend | Implemented | SuspendPostgresDatabase |
| GET | /{apiVersion}/databases/types | Implemented | ListDatabaseTypes |
| GET | /{apiVersion}/databases/types/{typeId} | Implemented | GetDatabaseType |
| POST | /{apiVersion}/domains | Implemented | CreateDomain |
| GET | /{apiVersion}/domains | Implemented | ListDomains |
| POST | /{apiVersion}/domains/import | Implemented | ImportDomain |
| GET | /{apiVersion}/domains/{domainId} | Implemented | GetDomain |
| PUT | /{apiVersion}/domains/{domainId} | Implemented | UpdateDomain |
| DELETE | /{apiVersion}/domains/{domainId} | Implemented | DeleteDomain |
| POST | /{apiVersion}/domains/{domainId}/clone | Implemented | CloneDomain |
| POST | /{apiVersion}/domains/{domainId}/records | Implemented | CreateDomainRecord |
| GET | /{apiVersion}/domains/{domainId}/records | Implemented | ListDomainRecords |
| GET | /{apiVersion}/domains/{domainId}/records/{recordId} | Implemented | GetDomainRecord |
| PUT | /{apiVersion}/domains/{domainId}/records/{recordId} | Implemented | UpdateDomainRecord |
| DELETE | /{apiVersion}/domains/{domainId}/records/{recordId} | Implemented | DeleteDomainRecord |
| GET | /{apiVersion}/domains/{domainId}/zone-file | Implemented | GetDomainZoneFile |
| GET | /{apiVersion}/entities | Implemented | ListEntities |
| GET | /{apiVersion}/iam/role-permissions | Implemented | GetAccountRolePermissions |
| GET | /{apiVersion}/iam/users/{username}/role-permissions | Implemented | GetUserRolePermissions |
| PUT | /{apiVersion}/iam/users/{username}/role-permissions | Implemented | UpdateUserRolePermissions |
| POST | /{apiVersion}/images | Implemented | CreateImage |
| GET | /{apiVersion}/images | Implemented | ListImages |
| POST | /{apiVersion}/images/sharegroups | Implemented | CreateImageShareGroup |
| GET | /{apiVersion}/images/sharegroups | Implemented | ListImageShareGroups |
| POST | /{apiVersion}/images/sharegroups/tokens | Implemented | ImageShareGroupCreateToken |
| GET | /{apiVersion}/images/sharegroups/tokens | Implemented | ImageShareGroupListTokens |
| GET | /{apiVersion}/images/sharegroups/tokens/{tokenUuid} | Implemented | ImageShareGroupGetToken |
| PUT | /{apiVersion}/images/sharegroups/tokens/{tokenUuid} | Implemented | ImageShareGroupUpdateToken |
| DELETE | /{apiVersion}/images/sharegroups/tokens/{tokenUuid} | Implemented | ImageShareGroupRemoveToken |
| GET | /{apiVersion}/images/sharegroups/tokens/{tokenUuid}/sharegroup | Implemented | ImageShareGroupGetByToken |
| GET | /{apiVersion}/images/sharegroups/tokens/{tokenUuid}/sharegroup/images | Implemented | ImageShareGroupGetImageShareEntriesByToken |
| GET | /{apiVersion}/images/sharegroups/{sharegroupId} | Implemented | GetImageShareGroup |
| PUT | /{apiVersion}/images/sharegroups/{sharegroupId} | Implemented | UpdateImageShareGroup |
| DELETE | /{apiVersion}/images/sharegroups/{sharegroupId} | Implemented | DeleteImageShareGroup |
| POST | /{apiVersion}/images/sharegroups/{sharegroupId}/images | Implemented | ImageShareGroupAddImages |
| GET | /{apiVersion}/images/sharegroups/{sharegroupId}/images | Implemented | ImageShareGroupListImageShareEntries |
| PUT | /{apiVersion}/images/sharegroups/{sharegroupId}/images/{imageId} | Implemented | ImageShareGroupUpdateImageShareEntry |
| DELETE | /{apiVersion}/images/sharegroups/{sharegroupId}/images/{imageId} | Implemented | ImageShareGroupRemoveImage |
| POST | /{apiVersion}/images/sharegroups/{sharegroupId}/members | Implemented | ImageShareGroupAddMember |
| GET | /{apiVersion}/images/sharegroups/{sharegroupId}/members | Implemented | ImageShareGroupListMembers |
| GET | /{apiVersion}/images/sharegroups/{sharegroupId}/members/{tokenUuid} | Implemented | ImageShareGroupGetMember |
| PUT | /{apiVersion}/images/sharegroups/{sharegroupId}/members/{tokenUuid} | Implemented | ImageShareGroupUpdateMember |
| DELETE | /{apiVersion}/images/sharegroups/{sharegroupId}/members/{tokenUuid} | Implemented | ImageShareGroupRemoveMember |
| POST | /{apiVersion}/images/upload | Implemented | CreateImageUpload |
| GET | /{apiVersion}/images/{imageId} | Implemented | GetImage |
| PUT | /{apiVersion}/images/{imageId} | Implemented | UpdateImage |
| DELETE | /{apiVersion}/images/{imageId} | Implemented | DeleteImage |
| POST | /{apiVersion}/images/{imageId}/regions | Implemented | ReplicateImage |
| GET | /{apiVersion}/images/{imageId}/sharegroups | Implemented | ListImageShareGroupsContainingPrivateImage |
| POST | /{apiVersion}/linode/instances | Implemented | CreateInstance |
| GET | /{apiVersion}/linode/instances | Implemented | ListInstances |
| GET | /{apiVersion}/linode/instances/{linodeId} | Implemented | GetInstance |
| PUT | /{apiVersion}/linode/instances/{linodeId} | Implemented | UpdateInstance |
| DELETE | /{apiVersion}/linode/instances/{linodeId} | Implemented | DeleteInstance |
| POST | /{apiVersion}/linode/instances/{linodeId}/backups | Implemented | CreateInstanceSnapshot |
| GET | /{apiVersion}/linode/instances/{linodeId}/backups | Implemented | GetInstanceBackups |
| POST | /{apiVersion}/linode/instances/{linodeId}/backups/cancel | Implemented | CancelInstanceBackups |
| POST | /{apiVersion}/linode/instances/{linodeId}/backups/enable | Implemented | EnableInstanceBackups |
| GET | /{apiVersion}/linode/instances/{linodeId}/backups/{backupId} | Implemented | GetInstanceSnapshot |
| POST | /{apiVersion}/linode/instances/{linodeId}/backups/{backupId}/restore | Implemented | RestoreInstanceBackup |
| POST | /{apiVersion}/linode/instances/{linodeId}/boot | Implemented | BootInstance |
| POST | /{apiVersion}/linode/instances/{linodeId}/clone | Implemented | CloneInstance |
| POST | /{apiVersion}/linode/instances/{linodeId}/configs | Implemented | CreateInstanceConfig |
| GET | /{apiVersion}/linode/instances/{linodeId}/configs | Implemented | ListInstanceConfigs |
| GET | /{apiVersion}/linode/instances/{linodeId}/configs/{configId} | Implemented | GetInstanceConfig |
| PUT | /{apiVersion}/linode/instances/{linodeId}/configs/{configId} | Implemented | UpdateInstanceConfig |
| DELETE | /{apiVersion}/linode/instances/{linodeId}/configs/{configId} | Implemented | DeleteInstanceConfig |
| POST | /{apiVersion}/linode/instances/{linodeId}/configs/{configId}/interfaces | Implemented | AppendInstanceConfigInterface |
| GET | /{apiVersion}/linode/instances/{linodeId}/configs/{configId}/interfaces | Implemented | ListInstanceConfigInterfaces |
| POST | /{apiVersion}/linode/instances/{linodeId}/configs/{configId}/interfaces/order | Implemented | ReorderInstanceConfigInterfaces |
| GET | /{apiVersion}/linode/instances/{linodeId}/configs/{configId}/interfaces/{interfaceId} | Implemented | GetInstanceConfigInterface |
| PUT | /{apiVersion}/linode/instances/{linodeId}/configs/{configId}/interfaces/{interfaceId} | Implemented | UpdateInstanceConfigInterface |
| DELETE | /{apiVersion}/linode/instances/{linodeId}/configs/{configId}/interfaces/{interfaceId} | Implemented | DeleteInstanceConfigInterface |
| POST | /{apiVersion}/linode/instances/{linodeId}/disks | Implemented | CreateInstanceDisk |
| GET | /{apiVersion}/linode/instances/{linodeId}/disks | Implemented | ListInstanceDisks |
| GET | /{apiVersion}/linode/instances/{linodeId}/disks/{diskId} | Implemented | GetInstanceDisk |
| PUT | /{apiVersion}/linode/instances/{linodeId}/disks/{diskId} | Implemented | UpdateInstanceDisk |
| DELETE | /{apiVersion}/linode/instances/{linodeId}/disks/{diskId} | Implemented | DeleteInstanceDisk |
| POST | /{apiVersion}/linode/instances/{linodeId}/disks/{diskId}/clone | Implemented | CloneInstanceDisk |
| POST | /{apiVersion}/linode/instances/{linodeId}/disks/{diskId}/password | Implemented | PasswordResetInstanceDisk |
| POST | /{apiVersion}/linode/instances/{linodeId}/disks/{diskId}/resize | Implemented | ResizeInstanceDisk |
| GET | /{apiVersion}/linode/instances/{linodeId}/firewalls | Implemented | ListInstanceFirewalls |
| PUT | /{apiVersion}/linode/instances/{linodeId}/firewalls | Implemented | UpdateInstanceFirewalls |
| POST | /{apiVersion}/linode/instances/{linodeId}/firewalls/apply | Missing |  |
| POST | /{apiVersion}/linode/instances/{linodeId}/interfaces | Implemented | CreateInterface |
| GET | /{apiVersion}/linode/instances/{linodeId}/interfaces | Implemented | ListInterfaces |
| GET | /{apiVersion}/linode/instances/{linodeId}/interfaces/history | Missing |  |
| GET | /{apiVersion}/linode/instances/{linodeId}/interfaces/settings | Implemented | GetInterfaceSettings |
| PUT | /{apiVersion}/linode/instances/{linodeId}/interfaces/settings | Implemented | UpdateInterfaceSettings |
| GET | /{apiVersion}/linode/instances/{linodeId}/interfaces/{interfaceId} | Implemented | GetInterface |
| PUT | /{apiVersion}/linode/instances/{linodeId}/interfaces/{interfaceId} | Implemented | UpdateInterface |
| DELETE | /{apiVersion}/linode/instances/{linodeId}/interfaces/{interfaceId} | Implemented | DeleteInterface |
| GET | /{apiVersion}/linode/instances/{linodeId}/interfaces/{interfaceId}/firewalls | Implemented | ListInterfaceFirewalls |
| POST | /{apiVersion}/linode/instances/{linodeId}/ips | Implemented | AssignInstanceReservedIP |
| GET | /{apiVersion}/linode/instances/{linodeId}/ips | Implemented | GetInstanceIPAddresses |
| GET | /{apiVersion}/linode/instances/{linodeId}/ips/{address} | Implemented | GetInstanceIPAddress |
| PUT | /{apiVersion}/linode/instances/{linodeId}/ips/{address} | Implemented | UpdateInstanceIPAddress |
| DELETE | /{apiVersion}/linode/instances/{linodeId}/ips/{address} | Implemented | DeleteInstanceIPAddress |
| POST | /{apiVersion}/linode/instances/{linodeId}/migrate | Implemented | MigrateInstance |
| POST | /{apiVersion}/linode/instances/{linodeId}/mutate | Implemented | UpgradeInstance |
| GET | /{apiVersion}/linode/instances/{linodeId}/nodebalancers | Implemented | ListInstanceNodeBalancers |
| POST | /{apiVersion}/linode/instances/{linodeId}/password | Implemented | ResetInstancePassword |
| POST | /{apiVersion}/linode/instances/{linodeId}/reboot | Implemented | RebootInstance |
| POST | /{apiVersion}/linode/instances/{linodeId}/rebuild | Implemented | RebuildInstance |
| POST | /{apiVersion}/linode/instances/{linodeId}/rescue | Implemented | RescueInstance |
| POST | /{apiVersion}/linode/instances/{linodeId}/resize | Implemented | ResizeInstance |
| POST | /{apiVersion}/linode/instances/{linodeId}/shutdown | Missing |  |
| GET | /{apiVersion}/linode/instances/{linodeId}/stats | Implemented | GetInstanceStats |
| GET | /{apiVersion}/linode/instances/{linodeId}/stats/{year}/{month} | Implemented | GetInstanceStatsByDate |
| GET | /{apiVersion}/linode/instances/{linodeId}/transfer | Implemented | GetInstanceTransfer |
| GET | /{apiVersion}/linode/instances/{linodeId}/transfer/{year}/{month} | Implemented | GetInstanceTransferMonthlyV2 |
| POST | /{apiVersion}/linode/instances/{linodeId}/upgrade-interfaces | Implemented | UpgradeInterfaces |
| GET | /{apiVersion}/linode/instances/{linodeId}/volumes | Implemented | ListInstanceVolumes |
| GET | /{apiVersion}/linode/kernels | Implemented | ListKernels |
| GET | /{apiVersion}/linode/kernels/{kernelId} | Implemented | GetKernel |
| POST | /{apiVersion}/linode/stackscripts | Implemented | CreateStackscript |
| GET | /{apiVersion}/linode/stackscripts | Implemented | ListStackscripts |
| GET | /{apiVersion}/linode/stackscripts/{stackscriptId} | Implemented | GetStackscript |
| PUT | /{apiVersion}/linode/stackscripts/{stackscriptId} | Implemented | UpdateStackscript |
| DELETE | /{apiVersion}/linode/stackscripts/{stackscriptId} | Implemented | DeleteStackscript |
| GET | /{apiVersion}/linode/types | Missing |  |
| GET | /{apiVersion}/linode/types/{typeId} | Implemented | GetType |
| POST | /{apiVersion}/lke/clusters | Implemented | CreateLKECluster |
| GET | /{apiVersion}/lke/clusters | Implemented | ListLKEClusters |
| GET | /{apiVersion}/lke/clusters/{clusterId} | Implemented | GetLKECluster |
| PUT | /{apiVersion}/lke/clusters/{clusterId} | Implemented | UpdateLKECluster |
| DELETE | /{apiVersion}/lke/clusters/{clusterId} | Implemented | DeleteLKECluster |
| GET | /{apiVersion}/lke/clusters/{clusterId}/api-endpoints | Implemented | ListLKEClusterAPIEndpoints |
| GET | /{apiVersion}/lke/clusters/{clusterId}/control_plane_acl | Implemented | GetLKEClusterControlPlaneACL |
| PUT | /{apiVersion}/lke/clusters/{clusterId}/control_plane_acl | Implemented | UpdateLKEClusterControlPlaneACL |
| DELETE | /{apiVersion}/lke/clusters/{clusterId}/control_plane_acl | Implemented | DeleteLKEClusterControlPlaneACL |
| GET | /{apiVersion}/lke/clusters/{clusterId}/dashboard | Implemented | GetLKEClusterDashboard |
| GET | /{apiVersion}/lke/clusters/{clusterId}/kubeconfig | Implemented | GetLKEClusterKubeconfig |
| DELETE | /{apiVersion}/lke/clusters/{clusterId}/kubeconfig | Implemented | DeleteLKEClusterKubeconfig |
| GET | /{apiVersion}/lke/clusters/{clusterId}/nodes/{nodeId} | Implemented | GetLKENodePoolNode |
| DELETE | /{apiVersion}/lke/clusters/{clusterId}/nodes/{nodeId} | Implemented | DeleteLKENodePoolNode |
| POST | /{apiVersion}/lke/clusters/{clusterId}/nodes/{nodeId}/recycle | Implemented | RecycleLKENodePoolNode |
| POST | /{apiVersion}/lke/clusters/{clusterId}/pools | Implemented | CreateLKENodePool |
| GET | /{apiVersion}/lke/clusters/{clusterId}/pools | Implemented | ListLKENodePools |
| GET | /{apiVersion}/lke/clusters/{clusterId}/pools/{poolId} | Implemented | GetLKENodePool |
| PUT | /{apiVersion}/lke/clusters/{clusterId}/pools/{poolId} | Implemented | UpdateLKENodePool |
| DELETE | /{apiVersion}/lke/clusters/{clusterId}/pools/{poolId} | Implemented | DeleteLKENodePool |
| POST | /{apiVersion}/lke/clusters/{clusterId}/pools/{poolId}/recycle | Implemented | RecycleLKENodePool |
| POST | /{apiVersion}/lke/clusters/{clusterId}/recycle | Implemented | RecycleLKEClusterNodes |
| POST | /{apiVersion}/lke/clusters/{clusterId}/regenerate | Implemented | RegenerateLKECluster |
| DELETE | /{apiVersion}/lke/clusters/{clusterId}/servicetoken | Implemented | DeleteLKEClusterServiceToken |
| GET | /{apiVersion}/lke/tiers/{tier}/versions | Implemented | ListLKETierVersions |
| GET | /{apiVersion}/lke/tiers/{tier}/versions/{version} | Implemented | GetLKETierVersion |
| GET | /{apiVersion}/lke/types | Missing |  |
| GET | /{apiVersion}/lke/versions | Missing |  |
| GET | /{apiVersion}/lke/versions/{version} | Implemented | GetLKEVersion |
| POST | /{apiVersion}/longview/clients | Implemented | CreateLongviewClient |
| GET | /{apiVersion}/longview/clients | Implemented | ListLongviewClients |
| GET | /{apiVersion}/longview/clients/{clientId} | Implemented | GetLongviewClient |
| PUT | /{apiVersion}/longview/clients/{clientId} | Implemented | UpdateLongviewClient |
| DELETE | /{apiVersion}/longview/clients/{clientId} | Implemented | DeleteLongviewClient |
| GET | /{apiVersion}/longview/plan | Implemented | GetLongviewPlan |
| PUT | /{apiVersion}/longview/plan | Implemented | UpdateLongviewPlan |
| GET | /{apiVersion}/longview/subscriptions | Implemented | ListLongviewSubscriptions |
| GET | /{apiVersion}/longview/subscriptions/{subscriptionId} | Implemented | GetLongviewSubscription |
| GET | /{apiVersion}/longview/types | Missing |  |
| GET | /{apiVersion}/maintenance/policies | Implemented | ListMaintenancePolicies |
| POST | /{apiVersion}/managed/contacts | Missing |  |
| GET | /{apiVersion}/managed/contacts | Missing |  |
| GET | /{apiVersion}/managed/contacts/{contactId} | Missing |  |
| PUT | /{apiVersion}/managed/contacts/{contactId} | Missing |  |
| DELETE | /{apiVersion}/managed/contacts/{contactId} | Missing |  |
| POST | /{apiVersion}/managed/credentials | Missing |  |
| GET | /{apiVersion}/managed/credentials | Missing |  |
| GET | /{apiVersion}/managed/credentials/sshkey | Missing |  |
| GET | /{apiVersion}/managed/credentials/{credentialId} | Missing |  |
| PUT | /{apiVersion}/managed/credentials/{credentialId} | Missing |  |
| POST | /{apiVersion}/managed/credentials/{credentialId}/revoke | Missing |  |
| POST | /{apiVersion}/managed/credentials/{credentialId}/update | Missing |  |
| GET | /{apiVersion}/managed/issues | Missing |  |
| GET | /{apiVersion}/managed/issues/{issueId} | Missing |  |
| GET | /{apiVersion}/managed/linode-settings | Missing |  |
| GET | /{apiVersion}/managed/linode-settings/{linodeId} | Missing |  |
| PUT | /{apiVersion}/managed/linode-settings/{linodeId} | Missing |  |
| POST | /{apiVersion}/managed/services | Missing |  |
| GET | /{apiVersion}/managed/services | Missing |  |
| GET | /{apiVersion}/managed/services/{serviceId} | Missing |  |
| PUT | /{apiVersion}/managed/services/{serviceId} | Missing |  |
| DELETE | /{apiVersion}/managed/services/{serviceId} | Missing |  |
| POST | /{apiVersion}/managed/services/{serviceId}/disable | Missing |  |
| POST | /{apiVersion}/managed/services/{serviceId}/enable | Missing |  |
| GET | /{apiVersion}/managed/stats | Missing |  |
| GET | /{apiVersion}/monitor/alert-channels | Implemented | ListAlertChannels |
| GET | /{apiVersion}/monitor/alert-definitions | Implemented | ListAllMonitorAlertDefinitions |
| GET | /{apiVersion}/monitor/dashboards | Implemented | ListMonitorDashboards |
| GET | /{apiVersion}/monitor/dashboards/{dashboardId} | Implemented | GetMonitorDashboard |
| GET | /{apiVersion}/monitor/services | Implemented | ListMonitorServices |
| GET | /{apiVersion}/monitor/services/{serviceType} | Implemented | GetMonitorServiceByType |
| POST | /{apiVersion}/monitor/services/{serviceType}/alert-definitions | Implemented | CreateMonitorAlertDefinitionWithIdempotency |
| GET | /{apiVersion}/monitor/services/{serviceType}/alert-definitions | Implemented | ListMonitorAlertDefinitions |
| GET | /{apiVersion}/monitor/services/{serviceType}/alert-definitions/{alertId} | Implemented | GetMonitorAlertDefinition |
| PUT | /{apiVersion}/monitor/services/{serviceType}/alert-definitions/{alertId} | Implemented | UpdateMonitorAlertDefinition |
| DELETE | /{apiVersion}/monitor/services/{serviceType}/alert-definitions/{alertId} | Implemented | DeleteMonitorAlertDefinition |
| GET | /{apiVersion}/monitor/services/{serviceType}/dashboards | Implemented | ListMonitorDashboardsByServiceType |
| GET | /{apiVersion}/monitor/services/{serviceType}/metric-definitions | Implemented | ListMonitorMetricsDefinitionByServiceType |
| POST | /{apiVersion}/monitor/services/{serviceType}/metrics | Implemented | FetchEntityMetrics |
| POST | /{apiVersion}/monitor/services/{serviceType}/token | Implemented | CreateMonitorServiceTokenForServiceType |
| POST | /{apiVersion}/monitor/streams | Missing |  |
| GET | /{apiVersion}/monitor/streams | Missing |  |
| POST | /{apiVersion}/monitor/streams/destinations | Missing |  |
| GET | /{apiVersion}/monitor/streams/destinations | Missing |  |
| GET | /{apiVersion}/monitor/streams/destinations/{destinationId} | Missing |  |
| PUT | /{apiVersion}/monitor/streams/destinations/{destinationId} | Missing |  |
| DELETE | /{apiVersion}/monitor/streams/destinations/{destinationId} | Missing |  |
| GET | /{apiVersion}/monitor/streams/destinations/{destinationId}/history | Missing |  |
| GET | /{apiVersion}/monitor/streams/{streamId} | Missing |  |
| PUT | /{apiVersion}/monitor/streams/{streamId} | Missing |  |
| DELETE | /{apiVersion}/monitor/streams/{streamId} | Missing |  |
| GET | /{apiVersion}/monitor/streams/{streamId}/history | Missing |  |
| GET | /{apiVersion}/network-transfer/prices | Missing |  |
| POST | /{apiVersion}/networking/firewalls | Implemented | CreateFirewall |
| GET | /{apiVersion}/networking/firewalls | Implemented | ListFirewalls |
| GET | /{apiVersion}/networking/firewalls/settings | Implemented | GetFirewallSettings |
| PUT | /{apiVersion}/networking/firewalls/settings | Implemented | UpdateFirewallSettings |
| GET | /{apiVersion}/networking/firewalls/templates | Implemented | ListFirewallTemplates |
| GET | /{apiVersion}/networking/firewalls/templates/{slug} | Implemented | GetFirewallTemplate |
| GET | /{apiVersion}/networking/firewalls/{firewallId} | Implemented | GetFirewall |
| PUT | /{apiVersion}/networking/firewalls/{firewallId} | Implemented | UpdateFirewall |
| DELETE | /{apiVersion}/networking/firewalls/{firewallId} | Implemented | DeleteFirewall |
| POST | /{apiVersion}/networking/firewalls/{firewallId}/devices | Implemented | CreateFirewallDevice |
| GET | /{apiVersion}/networking/firewalls/{firewallId}/devices | Implemented | ListFirewallDevices |
| GET | /{apiVersion}/networking/firewalls/{firewallId}/devices/{deviceId} | Implemented | GetFirewallDevice |
| DELETE | /{apiVersion}/networking/firewalls/{firewallId}/devices/{deviceId} | Implemented | DeleteFirewallDevice |
| GET | /{apiVersion}/networking/firewalls/{firewallId}/history | Missing |  |
| GET | /{apiVersion}/networking/firewalls/{firewallId}/history/rules/{version} | Missing |  |
| GET | /{apiVersion}/networking/firewalls/{firewallId}/rules | Implemented | GetFirewallRules |
| PUT | /{apiVersion}/networking/firewalls/{firewallId}/rules | Implemented | UpdateFirewallRules |
| POST | /{apiVersion}/networking/ips | Implemented | AllocateReserveIP |
| GET | /{apiVersion}/networking/ips | Implemented | ListIPAddresses |
| POST | /{apiVersion}/networking/ips/assign | Implemented | InstancesAssignIPs |
| POST | /{apiVersion}/networking/ips/share | Implemented | ShareIPAddresses |
| GET | /{apiVersion}/networking/ips/{address} | Implemented | GetIPAddress |
| PUT | /{apiVersion}/networking/ips/{address} | Implemented | UpdateIPAddress |
| POST | /{apiVersion}/networking/ipv4/assign | Missing |  |
| POST | /{apiVersion}/networking/ipv4/share | Missing |  |
| GET | /{apiVersion}/networking/ipv6/pools | Implemented | ListIPv6Pools |
| POST | /{apiVersion}/networking/ipv6/ranges | Implemented | CreateIPv6Range |
| GET | /{apiVersion}/networking/ipv6/ranges | Implemented | ListIPv6Ranges |
| GET | /{apiVersion}/networking/ipv6/ranges/{range} | Implemented | GetIPv6Range |
| DELETE | /{apiVersion}/networking/ipv6/ranges/{range} | Implemented | DeleteIPv6Range |
| GET | /{apiVersion}/networking/vlans | Implemented | ListVLANs |
| DELETE | /{apiVersion}/networking/vlans/{regionId}/{label} | Missing |  |
| POST | /{apiVersion}/nodebalancers | Implemented | CreateNodeBalancer |
| GET | /{apiVersion}/nodebalancers | Implemented | ListNodeBalancers |
| GET | /{apiVersion}/nodebalancers/types | Missing |  |
| GET | /{apiVersion}/nodebalancers/{nodeBalancerId} | Implemented | GetNodeBalancer |
| PUT | /{apiVersion}/nodebalancers/{nodeBalancerId} | Implemented | UpdateNodeBalancer |
| DELETE | /{apiVersion}/nodebalancers/{nodeBalancerId} | Implemented | DeleteNodeBalancer |
| POST | /{apiVersion}/nodebalancers/{nodeBalancerId}/configs | Implemented | CreateNodeBalancerConfig |
| GET | /{apiVersion}/nodebalancers/{nodeBalancerId}/configs | Implemented | ListNodeBalancerConfigs |
| GET | /{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId} | Implemented | GetNodeBalancerConfig |
| PUT | /{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId} | Implemented | UpdateNodeBalancerConfig |
| DELETE | /{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId} | Implemented | DeleteNodeBalancerConfig |
| POST | /{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId}/nodes | Implemented | CreateNodeBalancerNode |
| GET | /{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId}/nodes | Implemented | ListNodeBalancerNodes |
| GET | /{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId}/nodes/{nodeId} | Implemented | GetNodeBalancerNode |
| PUT | /{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId}/nodes/{nodeId} | Implemented | UpdateNodeBalancerNode |
| DELETE | /{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId}/nodes/{nodeId} | Implemented | DeleteNodeBalancerNode |
| POST | /{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId}/rebuild | Implemented | RebuildNodeBalancerConfig |
| GET | /{apiVersion}/nodebalancers/{nodeBalancerId}/firewalls | Implemented | ListNodeBalancerFirewalls |
| PUT | /{apiVersion}/nodebalancers/{nodeBalancerId}/firewalls | Missing |  |
| GET | /{apiVersion}/nodebalancers/{nodeBalancerId}/stats | Implemented | GetNodeBalancerStats |
| GET | /{apiVersion}/nodebalancers/{nodeBalancerId}/vpcs | Implemented | ListNodeBalancerVPCConfigs |
| GET | /{apiVersion}/nodebalancers/{nodeBalancerId}/vpcs/{nodeBalancerVpcConfigId} | Implemented | GetNodeBalancerVPCConfig |
| POST | /{apiVersion}/object-storage/buckets | Implemented | CreateObjectStorageBucket |
| GET | /{apiVersion}/object-storage/buckets | Implemented | ListObjectStorageBuckets |
| GET | /{apiVersion}/object-storage/buckets/{regionId} | Implemented | ListObjectStorageBucketsInCluster |
| GET | /{apiVersion}/object-storage/buckets/{regionId}/{bucket} | Implemented | GetObjectStorageBucket |
| DELETE | /{apiVersion}/object-storage/buckets/{regionId}/{bucket} | Implemented | DeleteObjectStorageBucket |
| POST | /{apiVersion}/object-storage/buckets/{regionId}/{bucket}/access | Implemented | UpdateObjectStorageBucketAccess |
| GET | /{apiVersion}/object-storage/buckets/{regionId}/{bucket}/access | Implemented | GetObjectStorageBucketAccessV2 |
| PUT | /{apiVersion}/object-storage/buckets/{regionId}/{bucket}/access | Missing |  |
| GET | /{apiVersion}/object-storage/buckets/{regionId}/{bucket}/object-acl | Missing |  |
| PUT | /{apiVersion}/object-storage/buckets/{regionId}/{bucket}/object-acl | Implemented | UpdateObjectStorageObjectACLConfigV2 |
| GET | /{apiVersion}/object-storage/buckets/{regionId}/{bucket}/object-list | Missing |  |
| POST | /{apiVersion}/object-storage/buckets/{regionId}/{bucket}/object-url | Implemented | CreateObjectStorageObjectURL |
| POST | /{apiVersion}/object-storage/buckets/{regionId}/{bucket}/ssl | Implemented | UploadObjectStorageBucketCertV2 |
| GET | /{apiVersion}/object-storage/buckets/{regionId}/{bucket}/ssl | Implemented | GetObjectStorageBucketCertV2 |
| DELETE | /{apiVersion}/object-storage/buckets/{regionId}/{bucket}/ssl | Implemented | DeleteObjectStorageBucketCert |
| POST | /{apiVersion}/object-storage/cancel | Implemented | CancelObjectStorage |
| GET | /{apiVersion}/object-storage/clusters | Implemented | ListObjectStorageClusters |
| GET | /{apiVersion}/object-storage/clusters/{clusterId} | Implemented | GetObjectStorageCluster |
| GET | /{apiVersion}/object-storage/endpoints | Implemented | ListObjectStorageEndpoints |
| POST | /{apiVersion}/object-storage/keys | Implemented | CreateObjectStorageKey |
| GET | /{apiVersion}/object-storage/keys | Implemented | ListObjectStorageKeys |
| GET | /{apiVersion}/object-storage/keys/{keyId} | Implemented | GetObjectStorageKey |
| PUT | /{apiVersion}/object-storage/keys/{keyId} | Implemented | UpdateObjectStorageKey |
| DELETE | /{apiVersion}/object-storage/keys/{keyId} | Implemented | DeleteObjectStorageKey |
| GET | /{apiVersion}/object-storage/quotas | Implemented | ListObjectStorageQuotas |
| GET | /{apiVersion}/object-storage/quotas/{objQuotaId} | Implemented | GetObjectStorageQuota |
| GET | /{apiVersion}/object-storage/quotas/{objQuotaId}/usage | Implemented | GetObjectStorageQuotaUsage |
| GET | /{apiVersion}/object-storage/transfer | Implemented | GetObjectStorageTransfer |
| GET | /{apiVersion}/object-storage/types | Missing |  |
| POST | /{apiVersion}/placement/groups | Implemented | CreatePlacementGroup |
| GET | /{apiVersion}/placement/groups | Implemented | ListPlacementGroups |
| GET | /{apiVersion}/placement/groups/{groupId} | Implemented | GetPlacementGroup |
| PUT | /{apiVersion}/placement/groups/{groupId} | Implemented | UpdatePlacementGroup |
| DELETE | /{apiVersion}/placement/groups/{groupId} | Implemented | DeletePlacementGroup |
| POST | /{apiVersion}/placement/groups/{groupId}/assign | Implemented | AssignPlacementGroupLinodes |
| POST | /{apiVersion}/placement/groups/{groupId}/unassign | Implemented | UnassignPlacementGroupLinodes |
| GET | /{apiVersion}/profile | Implemented | GetProfile |
| PUT | /{apiVersion}/profile | Implemented | UpdateProfile |
| GET | /{apiVersion}/profile/apps | Implemented | ListProfileApps |
| GET | /{apiVersion}/profile/apps/{appId} | Implemented | GetProfileApp |
| DELETE | /{apiVersion}/profile/apps/{appId} | Implemented | DeleteProfileApp |
| GET | /{apiVersion}/profile/devices | Implemented | ListProfileDevices |
| GET | /{apiVersion}/profile/devices/{deviceId} | Implemented | GetProfileDevice |
| DELETE | /{apiVersion}/profile/devices/{deviceId} | Implemented | DeleteProfileDevice |
| GET | /{apiVersion}/profile/grants | Implemented | GrantsList |
| GET | /{apiVersion}/profile/logins | Implemented | ListProfileLogins |
| GET | /{apiVersion}/profile/logins/{loginId} | Implemented | GetProfileLogin |
| POST | /{apiVersion}/profile/phone-number | Implemented | SendPhoneNumberVerificationCode |
| DELETE | /{apiVersion}/profile/phone-number | Implemented | DeletePhoneNumber |
| POST | /{apiVersion}/profile/phone-number/verify | Implemented | VerifyPhoneNumber |
| GET | /{apiVersion}/profile/preferences | Implemented | GetProfilePreferences |
| PUT | /{apiVersion}/profile/preferences | Implemented | UpdateProfilePreferences |
| POST | /{apiVersion}/profile/security-questions | Implemented | SecurityQuestionsAnswer |
| GET | /{apiVersion}/profile/security-questions | Implemented | SecurityQuestionsList |
| POST | /{apiVersion}/profile/sshkeys | Implemented | CreateSSHKey |
| GET | /{apiVersion}/profile/sshkeys | Implemented | ListSSHKeys |
| GET | /{apiVersion}/profile/sshkeys/{sshKeyId} | Implemented | GetSSHKey |
| PUT | /{apiVersion}/profile/sshkeys/{sshKeyId} | Implemented | UpdateSSHKey |
| DELETE | /{apiVersion}/profile/sshkeys/{sshKeyId} | Implemented | DeleteSSHKey |
| POST | /{apiVersion}/profile/tfa-disable | Implemented | DisableTwoFactor |
| POST | /{apiVersion}/profile/tfa-enable | Implemented | CreateTwoFactorSecret |
| POST | /{apiVersion}/profile/tfa-enable-confirm | Implemented | ConfirmTwoFactor |
| POST | /{apiVersion}/profile/tokens | Implemented | CreateToken |
| GET | /{apiVersion}/profile/tokens | Implemented | ListTokens |
| GET | /{apiVersion}/profile/tokens/{tokenId} | Implemented | GetToken |
| PUT | /{apiVersion}/profile/tokens/{tokenId} | Implemented | UpdateToken |
| DELETE | /{apiVersion}/profile/tokens/{tokenId} | Implemented | DeleteToken |
| GET | /{apiVersion}/regions | Implemented | ListRegions |
| GET | /{apiVersion}/regions/availability | Missing |  |
| GET | /{apiVersion}/regions/{regionId} | Implemented | GetRegion |
| GET | /{apiVersion}/regions/{regionId}/availability | Implemented | GetRegionAvailability |
| POST | /{apiVersion}/support/tickets | Missing |  |
| GET | /{apiVersion}/support/tickets | Implemented | ListTickets |
| GET | /{apiVersion}/support/tickets/{ticketId} | Implemented | GetTicket |
| POST | /{apiVersion}/support/tickets/{ticketId}/attachments | Missing |  |
| POST | /{apiVersion}/support/tickets/{ticketId}/close | Missing |  |
| POST | /{apiVersion}/support/tickets/{ticketId}/replies | Missing |  |
| GET | /{apiVersion}/support/tickets/{ticketId}/replies | Missing |  |
| POST | /{apiVersion}/tags | Implemented | CreateTag |
| GET | /{apiVersion}/tags | Implemented | ListTags |
| GET | /{apiVersion}/tags/{tagLabel} | Implemented | ListTaggedObjects |
| DELETE | /{apiVersion}/tags/{tagLabel} | Implemented | DeleteTag |
| POST | /{apiVersion}/volumes | Implemented | CreateVolume |
| GET | /{apiVersion}/volumes | Implemented | ListVolumes |
| GET | /{apiVersion}/volumes/types | Missing |  |
| GET | /{apiVersion}/volumes/{volumeId} | Implemented | GetVolume |
| PUT | /{apiVersion}/volumes/{volumeId} | Implemented | UpdateVolume |
| DELETE | /{apiVersion}/volumes/{volumeId} | Implemented | DeleteVolume |
| POST | /{apiVersion}/volumes/{volumeId}/attach | Implemented | AttachVolume |
| POST | /{apiVersion}/volumes/{volumeId}/clone | Implemented | CloneVolume |
| POST | /{apiVersion}/volumes/{volumeId}/detach | Implemented | DetachVolume |
| POST | /{apiVersion}/volumes/{volumeId}/resize | Implemented | ResizeVolume |
| POST | /{apiVersion}/vpcs | Implemented | CreateVPC |
| GET | /{apiVersion}/vpcs | Implemented | ListVPCs |
| GET | /{apiVersion}/vpcs/ips | Implemented | ListAllVPCIPAddresses |
| GET | /{apiVersion}/vpcs/{vpcId} | Implemented | GetVPC |
| PUT | /{apiVersion}/vpcs/{vpcId} | Implemented | UpdateVPC |
| DELETE | /{apiVersion}/vpcs/{vpcId} | Implemented | DeleteVPC |
| GET | /{apiVersion}/vpcs/{vpcId}/ips | Missing |  |
| POST | /{apiVersion}/vpcs/{vpcId}/subnets | Implemented | CreateVPCSubnet |
| GET | /{apiVersion}/vpcs/{vpcId}/subnets | Implemented | ListVPCSubnets |
| GET | /{apiVersion}/vpcs/{vpcId}/subnets/{vpcSubnetId} | Implemented | GetVPCSubnet |
| PUT | /{apiVersion}/vpcs/{vpcId}/subnets/{vpcSubnetId} | Implemented | UpdateVPCSubnet |
| DELETE | /{apiVersion}/vpcs/{vpcId}/subnets/{vpcSubnetId} | Implemented | DeleteVPCSubnet |
## Parameter Coverage Gaps (implemented endpoints with differences)
| Method | Path | SDK Function | Missing Body | Extra Body | Missing Query | Extra Query |
|---|---|---|---|---|---|---|
| PUT | /{apiVersion}/account | UpdateAccount | active_promotions;active_since;balance;balance_uninvoiced;billing_source;capabilities;credit_card;euuid | - | - | - |
| POST | /{apiVersion}/account/agreements | AcknowledgeAccountAgreements | billing_agreement | - | - | - |
| GET | /{apiVersion}/account/availability | ListAccountAvailabilities | - | - | page;page_size | - |
| GET | /{apiVersion}/account/betas | ListAccountBetaPrograms | - | - | page;page_size | - |
| GET | /{apiVersion}/account/child-accounts | ListChildAccounts | - | - | page;page_size | - |
| GET | /{apiVersion}/account/events | ListEvents | - | - | page;page_size | - |
| GET | /{apiVersion}/account/invoices | ListInvoices | - | - | page;page_size | - |
| GET | /{apiVersion}/account/invoices/{invoiceId}/items | ListInvoiceItems | - | - | page;page_size | - |
| POST | /{apiVersion}/account/oauth-clients | CreateOAuthClient | - | label;public;redirect_uri | - | - |
| GET | /{apiVersion}/account/oauth-clients | ListOAuthClients | - | - | page;page_size | - |
| PUT | /{apiVersion}/account/oauth-clients/{clientId} | UpdateOAuthClient | id;secret;status;thumbnail_url | - | - | - |
| GET | /{apiVersion}/account/payment-methods | ListPaymentMethods | - | - | page;page_size | - |
| POST | /{apiVersion}/account/payments | CreatePayment | payment_method_id | cvv | - | - |
| GET | /{apiVersion}/account/payments | ListPayments | - | - | page;page_size | - |
| GET | /{apiVersion}/account/service-transfers | ListAccountServiceTransfer | - | - | page;page_size | - |
| PUT | /{apiVersion}/account/settings | UpdateAccountSettings | longview_subscription;managed;object_storage | - | - | - |
| POST | /{apiVersion}/account/users | CreateUser | - | email;restricted;username | - | - |
| GET | /{apiVersion}/account/users | ListUsers | - | - | page;page_size | - |
| PUT | /{apiVersion}/account/users/{username} | UpdateUser | last_login;password_created;ssh_keys;tfa_enabled;verified_phone_number | - | - | - |
| PUT | /{apiVersion}/account/users/{username}/grants | UpdateUserGrants | - | placement_group | - | - |
| GET | /{apiVersion}/betas | ListBetaPrograms | - | - | page;page_size | - |
| GET | /{apiVersion}/databases/engines | ListDatabaseEngines | - | - | page;page_size | - |
| GET | /{apiVersion}/databases/engines/{engineId} | GetDatabaseEngine | - | - | page;page_size | - |
| GET | /{apiVersion}/databases/instances | ListDatabases | - | - | page;page_size | - |
| POST | /{apiVersion}/databases/mysql/instances | CreateMySQLDatabase | ssl_connection | - | - | - |
| GET | /{apiVersion}/databases/mysql/instances | ListMySQLDatabases | - | - | page;page_size | - |
| PUT | /{apiVersion}/databases/mysql/instances/{instanceId} | UpdateMySQLDatabase | - | cluster_size | - | - |
| POST | /{apiVersion}/databases/postgresql/instances | CreatePostgresDatabase | ssl_connection | - | - | - |
| GET | /{apiVersion}/databases/postgresql/instances | ListPostgresDatabases | - | - | page;page_size | - |
| PUT | /{apiVersion}/databases/postgresql/instances/{instanceId} | UpdatePostgresDatabase | - | cluster_size | - | - |
| GET | /{apiVersion}/databases/types | ListDatabaseTypes | - | - | page;page_size | - |
| GET | /{apiVersion}/databases/types/{typeId} | GetDatabaseType | - | - | page;page_size | - |
| POST | /{apiVersion}/domains | CreateDomain | - | axfr_ips;description;domain;expire_sec;group;master_ips;refresh_sec;retry_sec;soa_email;status;tags;ttl_sec;type | - | - |
| GET | /{apiVersion}/domains | ListDomains | - | - | page;page_size | - |
| POST | /{apiVersion}/domains/import | ImportDomain | remote_nameserver | remove_nameserver | - | - |
| PUT | /{apiVersion}/domains/{domainId} | UpdateDomain | id | - | - | - |
| POST | /{apiVersion}/domains/{domainId}/records | CreateDomainRecord | - | name;port;priority;protocol;service;tag;target;ttl_sec;type;weight | - | - |
| GET | /{apiVersion}/domains/{domainId}/records | ListDomainRecords | - | - | page;page_size | - |
| PUT | /{apiVersion}/domains/{domainId}/records/{recordId} | UpdateDomainRecord | - | type | - | - |
| GET | /{apiVersion}/images | ListImages | - | - | page;page_size | - |
| GET | /{apiVersion}/images/sharegroups | ListImageShareGroups | - | - | page;page_size | - |
| POST | /{apiVersion}/images/sharegroups/{sharegroupId}/images | ImageShareGroupAddImages | images | - | - | - |
| PUT | /{apiVersion}/images/{imageId} | UpdateImage | capabilities;created;created_by;deprecated;eol;expiry;id;is_public;is_shared;regions;size;status;total_size;type;updated;vendor | - | - | - |
| POST | /{apiVersion}/linode/instances | CreateInstance | - | authorized_keys;authorized_users;backup_id;backups_enabled;booted;disk_encryption;firewall_id;group;image;interface_generation;ipv4;label;maintenance_policy;metadata;network_helper;placement_group;private_ip;region;root_pass;stackscript_data;stackscript_id;swap_size;tags;type | - | - |
| GET | /{apiVersion}/linode/instances | ListInstances | - | - | page;page_size | - |
| PUT | /{apiVersion}/linode/instances/{linodeId} | UpdateInstance | capabilities;created;disk_encryption;has_user_data;host_uuid;hypervisor;id;image;interface_generation;ipv4;ipv6;lke_cluster_id;placement_group;region;specs;status;type;updated | - | - | - |
| POST | /{apiVersion}/linode/instances/{linodeId}/backups | CreateInstanceSnapshot | label | - | - | - |
| POST | /{apiVersion}/linode/instances/{linodeId}/boot | BootInstance | config_id | - | - | - |
| POST | /{apiVersion}/linode/instances/{linodeId}/clone | CloneInstance | maintenance_policy | - | - | - |
| POST | /{apiVersion}/linode/instances/{linodeId}/configs | CreateInstanceConfig | - | comments;devices;helpers;init_rd;interfaces;kernel;label;memory_limit;root_device;run_level;virt_mode | - | - |
| GET | /{apiVersion}/linode/instances/{linodeId}/configs | ListInstanceConfigs | - | - | page;page_size | - |
| PUT | /{apiVersion}/linode/instances/{linodeId}/configs/{configId} | UpdateInstanceConfig | id | init_rd | - | - |
| POST | /{apiVersion}/linode/instances/{linodeId}/configs/{configId}/interfaces | AppendInstanceConfigInterface | - | ip_ranges;ipam_address;ipv4;ipv6;label;primary;purpose;subnet_id | - | - |
| PUT | /{apiVersion}/linode/instances/{linodeId}/configs/{configId}/interfaces/{interfaceId} | UpdateInstanceConfigInterface | - | ipv6 | - | - |
| POST | /{apiVersion}/linode/instances/{linodeId}/disks | CreateInstanceDisk | - | authorized_keys;authorized_users;filesystem;image;label;root_pass;size;stackscript_data;stackscript_id | - | - |
| GET | /{apiVersion}/linode/instances/{linodeId}/disks | ListInstanceDisks | - | - | page;page_size | - |
| POST | /{apiVersion}/linode/instances/{linodeId}/disks/{diskId}/password | PasswordResetInstanceDisk | password | - | - | - |
| POST | /{apiVersion}/linode/instances/{linodeId}/disks/{diskId}/resize | ResizeInstanceDisk | size | - | - | - |
| GET | /{apiVersion}/linode/instances/{linodeId}/firewalls | ListInstanceFirewalls | - | - | page;page_size | - |
| PUT | /{apiVersion}/linode/instances/{linodeId}/firewalls | UpdateInstanceFirewalls | firewall_ids | - | page;page_size | - |
| POST | /{apiVersion}/linode/instances/{linodeId}/interfaces | CreateInterface | - | default_route;firewall_id;public;vlan;vpc | - | - |
| PUT | /{apiVersion}/linode/instances/{linodeId}/interfaces/{interfaceId} | UpdateInterface | - | default_route;public;vpc | - | - |
| POST | /{apiVersion}/linode/instances/{linodeId}/ips | AssignInstanceReservedIP | - | address | - | - |
| POST | /{apiVersion}/linode/instances/{linodeId}/reboot | RebootInstance | config_id | - | - | - |
| POST | /{apiVersion}/linode/instances/{linodeId}/rebuild | RebuildInstance | - | authorized_keys;authorized_users;booted;disk_encryption;image;metadata;root_pass;stackscript_data;stackscript_id;type | - | - |
| GET | /{apiVersion}/linode/instances/{linodeId}/volumes | ListInstanceVolumes | - | - | page;page_size | - |
| GET | /{apiVersion}/linode/kernels | ListKernels | - | - | page;page_size | - |
| POST | /{apiVersion}/linode/stackscripts | CreateStackscript | - | description;images;is_public;label;rev_note;script | - | - |
| GET | /{apiVersion}/linode/stackscripts | ListStackscripts | - | - | page;page_size | - |
| PUT | /{apiVersion}/linode/stackscripts/{stackscriptId} | UpdateStackscript | created;deployments_active;deployments_total;id;mine;updated;user_defined_fields;user_gravatar_id;username | - | - | - |
| POST | /{apiVersion}/lke/clusters/{clusterId}/pools | CreateLKENodePool | - | autoscaler;count;disks;firewall_id;k8s_version;label;labels;tags;taints;type;update_strategy | - | - |
| PUT | /{apiVersion}/lke/clusters/{clusterId}/pools/{poolId} | UpdateLKENodePool | - | k8s_version;label;update_strategy | - | - |
| POST | /{apiVersion}/longview/clients | CreateLongviewClient | api_key;apps;created;id;install_code;updated | - | - | - |
| GET | /{apiVersion}/longview/clients | ListLongviewClients | - | - | page;page_size | - |
| PUT | /{apiVersion}/longview/clients/{clientId} | UpdateLongviewClient | api_key;apps;created;id;install_code;updated | - | - | - |
| GET | /{apiVersion}/longview/subscriptions | ListLongviewSubscriptions | - | - | page;page_size | - |
| POST | /{apiVersion}/monitor/services/{serviceType}/alert-definitions | CreateMonitorAlertDefinitionWithIdempotency | channel_ids;description;entity_ids;label;rule_criteria;severity;trigger_conditions | - | - | - |
| POST | /{apiVersion}/networking/firewalls | CreateFirewall | - | devices;label;rules;tags | - | - |
| GET | /{apiVersion}/networking/firewalls | ListFirewalls | - | - | page;page_size | - |
| GET | /{apiVersion}/networking/firewalls/settings | GetFirewallSettings | - | - | page;page_size | - |
| GET | /{apiVersion}/networking/firewalls/templates | ListFirewallTemplates | - | - | page;page_size | - |
| GET | /{apiVersion}/networking/firewalls/templates/{slug} | GetFirewallTemplate | - | - | page;page_size | - |
| POST | /{apiVersion}/networking/firewalls/{firewallId}/devices | CreateFirewallDevice | - | id;type | - | - |
| GET | /{apiVersion}/networking/firewalls/{firewallId}/devices | ListFirewallDevices | - | - | page;page_size | - |
| PUT | /{apiVersion}/networking/firewalls/{firewallId}/rules | UpdateFirewallRules | - | inbound;inbound_policy;outbound;outbound_policy | - | - |
| POST | /{apiVersion}/networking/ips | AllocateReserveIP | - | region;reserved | - | - |
| GET | /{apiVersion}/networking/ips | ListIPAddresses | - | - | skip_ipv6_rdns | - |
| GET | /{apiVersion}/networking/ipv6/pools | ListIPv6Pools | - | - | page;page_size | - |
| GET | /{apiVersion}/networking/ipv6/ranges | ListIPv6Ranges | - | - | page;page_size | - |
| GET | /{apiVersion}/networking/vlans | ListVLANs | - | - | page;page_size | - |
| POST | /{apiVersion}/nodebalancers | CreateNodeBalancer | - | client_udp_sess_throttle;ipv4;type | - | - |
| GET | /{apiVersion}/nodebalancers | ListNodeBalancers | - | - | page;page_size | - |
| PUT | /{apiVersion}/nodebalancers/{nodeBalancerId} | UpdateNodeBalancer | created;hostname;id;ipv4;ipv6;lke_cluster;region;transfer;type;updated | client_udp_sess_throttle | - | - |
| POST | /{apiVersion}/nodebalancers/{nodeBalancerId}/configs | CreateNodeBalancerConfig | - | algorithm;check;check_attempts;check_body;check_interval;check_passive;check_path;check_timeout;cipher_suite;nodes;port;protocol;proxy_protocol;ssl_cert;ssl_key;stickiness;udp_check_port | - | - |
| GET | /{apiVersion}/nodebalancers/{nodeBalancerId}/configs | ListNodeBalancerConfigs | - | - | page;page_size | - |
| PUT | /{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId} | UpdateNodeBalancerConfig | - | algorithm;check;check_attempts;check_body;check_interval;check_passive;check_path;check_timeout;cipher_suite;nodes;port;protocol;proxy_protocol;ssl_cert;ssl_key;stickiness;udp_check_port | - | - |
| POST | /{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId}/nodes | CreateNodeBalancerNode | - | address;label;mode;subnet_id;weight | - | - |
| GET | /{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId}/nodes | ListNodeBalancerNodes | - | - | page;page_size | - |
| PUT | /{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId}/nodes/{nodeId} | UpdateNodeBalancerNode | - | address;label;mode;subnet_id;weight | - | - |
| POST | /{apiVersion}/nodebalancers/{nodeBalancerId}/configs/{configId}/rebuild | RebuildNodeBalancerConfig | - | algorithm;check;check_attempts;check_body;check_interval;check_passive;check_path;check_timeout;cipher_suite;nodes;port;protocol;proxy_protocol;ssl_cert;ssl_key;stickiness;udp_check_port | - | - |
| GET | /{apiVersion}/nodebalancers/{nodeBalancerId}/vpcs | ListNodeBalancerVPCConfigs | - | - | page;page_size | - |
| POST | /{apiVersion}/object-storage/buckets | CreateObjectStorageBucket | - | cluster | - | - |
| POST | /{apiVersion}/object-storage/buckets/{regionId}/{bucket}/object-url | CreateObjectStorageObjectURL | - | content_disposition | - | - |
| POST | /{apiVersion}/object-storage/keys | CreateObjectStorageKey | - | bucket_access;label;regions | - | - |
| POST | /{apiVersion}/placement/groups | CreatePlacementGroup | - | label;placement_group_policy;placement_group_type;region | - | - |
| GET | /{apiVersion}/placement/groups | ListPlacementGroups | - | - | page;page_size | - |
| POST | /{apiVersion}/placement/groups/{groupId}/assign | AssignPlacementGroupLinodes | - | compliant_only | - | - |
| PUT | /{apiVersion}/profile | UpdateProfile | authentication_type;referrals;uid;username;verified_phone_number | - | - | - |
| GET | /{apiVersion}/profile/apps | ListProfileApps | - | - | page;page_size | - |
| POST | /{apiVersion}/profile/sshkeys | CreateSSHKey | created;id | - | - | - |
| GET | /{apiVersion}/profile/sshkeys | ListSSHKeys | - | - | page;page_size | - |
| PUT | /{apiVersion}/profile/tokens/{tokenId} | UpdateToken | created;expiry;id;scopes;token | - | - | - |
| GET | /{apiVersion}/support/tickets | ListTickets | - | - | page;page_size | - |
| POST | /{apiVersion}/tags | CreateTag | - | lke_clusters | - | - |
| GET | /{apiVersion}/tags | ListTags | - | - | page;page_size | - |
| GET | /{apiVersion}/tags/{tagLabel} | ListTaggedObjects | - | - | page;page_size | - |
| POST | /{apiVersion}/volumes | CreateVolume | - | persist_across_boots | - | - |
| GET | /{apiVersion}/volumes | ListVolumes | - | - | page;page_size | - |
| GET | /{apiVersion}/volumes/{volumeId} | GetVolume | - | - | page;page_size | - |
| PUT | /{apiVersion}/volumes/{volumeId} | UpdateVolume | - | label;tags | - | - |
| POST | /{apiVersion}/volumes/{volumeId}/clone | CloneVolume | label | - | - | - |
| POST | /{apiVersion}/volumes/{volumeId}/resize | ResizeVolume | size | - | - | - |
| POST | /{apiVersion}/vpcs | CreateVPC | - | description;ipv6;label;region;subnets | - | - |
| GET | /{apiVersion}/vpcs | ListVPCs | - | - | page;page_size | - |
| GET | /{apiVersion}/vpcs/ips | ListAllVPCIPAddresses | - | - | page;page_size | - |
| POST | /{apiVersion}/vpcs/{vpcId}/subnets | CreateVPCSubnet | - | ipv6 | - | - |
| GET | /{apiVersion}/vpcs/{vpcId}/subnets | ListVPCSubnets | - | - | page;page_size | - |
## SDK Endpoints Not In Spec
| Method | Path | SDK Function |
|---|---|---|
| POST | account/events/%d/read | MarkEventRead |
| POST | account/payment-methods/%d | SetDefaultPaymentMethod |
| GET | iam/users/%s/permissions/%s/%d | GetEntityRoles |
| GET | networking/firewalls/%d/rules/expansion | GetFirewallRulesExpansion |
| GET | networking/firewalls/rulesets | ListFirewallRuleSets |
| POST | networking/firewalls/rulesets | CreateFirewallRuleSet |
| GET | networking/firewalls/rulesets/%d | GetFirewallRuleSet |
| PUT | networking/firewalls/rulesets/%d | UpdateFirewallRuleSet |
| DELETE | networking/firewalls/rulesets/%d | DeleteFirewallRuleSet |
| GET | iam/users/%s/permissions/account | GetUserAccountPermissions |
| POST | linode/instances/%d/%s | simpleInstanceAction |
| GET | locks | ListLocks |
| GET | locks/%d | GetLock |
| POST | locks | CreateLock |
| DELETE | locks/%d | DeleteLock |
| GET | networking/ipv6/pools/%s | GetIPv6Pool |
| GET | networking/reserved/ips | ListReservedIPAddresses |
| GET | networking/reserved/ips/%s | GetReservedIPAddress |
| POST | networking/reserved/ips | ReserveIPAddress |
| DELETE | networking/reserved/ips/%s | DeleteReservedIPAddress |
| GET | object-storage/buckets/%s/%s/object-acl?name=%s | GetObjectStorageObjectACLConfigV2 |
| GET | networking/prefixlists | ListPrefixLists |
| GET | networking/prefixlists/%d | GetPrefixList |
| GET | regions/%s/vpc-availability | GetRegionVPCAvailability |
| GET | vpcs/ipv6s | ListAllVPCIPv6Addresses |