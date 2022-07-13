# Package animeshon.iam.admin.v1alpha1

## Index
- [IAM](#animeshon.iam.admin.v1alpha1.IAM)
- [CreatePermissionRequest](#animeshon.iam.admin.v1alpha1.CreatePermissionRequest)
- [CreateRoleRequest](#animeshon.iam.admin.v1alpha1.CreateRoleRequest)
- [CreateServiceAccountRequest](#animeshon.iam.admin.v1alpha1.CreateServiceAccountRequest)
- [DeletePermissionRequest](#animeshon.iam.admin.v1alpha1.DeletePermissionRequest)
- [DeleteRoleRequest](#animeshon.iam.admin.v1alpha1.DeleteRoleRequest)
- [DeleteServiceAccountRequest](#animeshon.iam.admin.v1alpha1.DeleteServiceAccountRequest)
- [GetPermissionRequest](#animeshon.iam.admin.v1alpha1.GetPermissionRequest)
- [GetRoleRequest](#animeshon.iam.admin.v1alpha1.GetRoleRequest)
- [GetServiceAccountRequest](#animeshon.iam.admin.v1alpha1.GetServiceAccountRequest)
- [ListPermissionsRequest](#animeshon.iam.admin.v1alpha1.ListPermissionsRequest)
- [ListPermissionsResponse](#animeshon.iam.admin.v1alpha1.ListPermissionsResponse)
- [ListRolesRequest](#animeshon.iam.admin.v1alpha1.ListRolesRequest)
- [ListRolesResponse](#animeshon.iam.admin.v1alpha1.ListRolesResponse)
- [ListServiceAccountsRequest](#animeshon.iam.admin.v1alpha1.ListServiceAccountsRequest)
- [ListServiceAccountsResponse](#animeshon.iam.admin.v1alpha1.ListServiceAccountsResponse)
- [Permission](#animeshon.iam.admin.v1alpha1.Permission)
- [Role](#animeshon.iam.admin.v1alpha1.Role)
- [ServiceAccount](#animeshon.iam.admin.v1alpha1.ServiceAccount)
- [UpdatePermissionRequest](#animeshon.iam.admin.v1alpha1.UpdatePermissionRequest)
- [UpdateRoleRequest](#animeshon.iam.admin.v1alpha1.UpdateRoleRequest)
- [UpdateServiceAccountRequest](#animeshon.iam.admin.v1alpha1.UpdateServiceAccountRequest)

## IAM {#animeshon.iam.admin.v1alpha1.IAM}

| GetServiceAccount |
| --- |
| **rpc** GetServiceAccount([GetServiceAccountRequest](#animeshon.iam.admin.v1alpha1.GetServiceAccountRequest)) [ServiceAccount](#animeshon.iam.admin.v1alpha1.ServiceAccount)<br/> |

| ListServiceAccounts |
| --- |
| **rpc** ListServiceAccounts([ListServiceAccountsRequest](#animeshon.iam.admin.v1alpha1.ListServiceAccountsRequest)) [ListServiceAccountsResponse](#animeshon.iam.admin.v1alpha1.ListServiceAccountsResponse)<br/> |

| CreateServiceAccount |
| --- |
| **rpc** CreateServiceAccount([CreateServiceAccountRequest](#animeshon.iam.admin.v1alpha1.CreateServiceAccountRequest)) [ServiceAccount](#animeshon.iam.admin.v1alpha1.ServiceAccount)<br/> |

| UpdateServiceAccount |
| --- |
| **rpc** UpdateServiceAccount([UpdateServiceAccountRequest](#animeshon.iam.admin.v1alpha1.UpdateServiceAccountRequest)) [ServiceAccount](#animeshon.iam.admin.v1alpha1.ServiceAccount)<br/> |

| DeleteServiceAccount |
| --- |
| **rpc** DeleteServiceAccount([DeleteServiceAccountRequest](#animeshon.iam.admin.v1alpha1.DeleteServiceAccountRequest)) [.google.protobuf.Empty](#google.protobuf.Empty)<br/> |

| GetRole |
| --- |
| **rpc** GetRole([GetRoleRequest](#animeshon.iam.admin.v1alpha1.GetRoleRequest)) [Role](#animeshon.iam.admin.v1alpha1.Role)<br/> |

| ListRoles |
| --- |
| **rpc** ListRoles([ListRolesRequest](#animeshon.iam.admin.v1alpha1.ListRolesRequest)) [ListRolesResponse](#animeshon.iam.admin.v1alpha1.ListRolesResponse)<br/> |

| CreateRole |
| --- |
| **rpc** CreateRole([CreateRoleRequest](#animeshon.iam.admin.v1alpha1.CreateRoleRequest)) [Role](#animeshon.iam.admin.v1alpha1.Role)<br/> |

| UpdateRole |
| --- |
| **rpc** UpdateRole([UpdateRoleRequest](#animeshon.iam.admin.v1alpha1.UpdateRoleRequest)) [Role](#animeshon.iam.admin.v1alpha1.Role)<br/> |

| DeleteRole |
| --- |
| **rpc** DeleteRole([DeleteRoleRequest](#animeshon.iam.admin.v1alpha1.DeleteRoleRequest)) [.google.protobuf.Empty](#google.protobuf.Empty)<br/> |

| GetPermission |
| --- |
| **rpc** GetPermission([GetPermissionRequest](#animeshon.iam.admin.v1alpha1.GetPermissionRequest)) [Permission](#animeshon.iam.admin.v1alpha1.Permission)<br/> |

| ListPermissions |
| --- |
| **rpc** ListPermissions([ListPermissionsRequest](#animeshon.iam.admin.v1alpha1.ListPermissionsRequest)) [ListPermissionsResponse](#animeshon.iam.admin.v1alpha1.ListPermissionsResponse)<br/> |

| CreatePermission |
| --- |
| **rpc** CreatePermission([CreatePermissionRequest](#animeshon.iam.admin.v1alpha1.CreatePermissionRequest)) [Permission](#animeshon.iam.admin.v1alpha1.Permission)<br/> |

| UpdatePermission |
| --- |
| **rpc** UpdatePermission([UpdatePermissionRequest](#animeshon.iam.admin.v1alpha1.UpdatePermissionRequest)) [Permission](#animeshon.iam.admin.v1alpha1.Permission)<br/> |

| DeletePermission |
| --- |
| **rpc** DeletePermission([DeletePermissionRequest](#animeshon.iam.admin.v1alpha1.DeletePermissionRequest)) [.google.protobuf.Empty](#google.protobuf.Empty)<br/> |

## CreatePermissionRequest {#animeshon.iam.admin.v1alpha1.CreatePermissionRequest}

| Field | Description |
| --- | --- |
| permission | **[ Permission](#Permission)**<br/>The permission to create. |
## CreateRoleRequest {#animeshon.iam.admin.v1alpha1.CreateRoleRequest}

| Field | Description |
| --- | --- |
| role | **[ Role](#Role)**<br/>The role to create. |
## CreateServiceAccountRequest {#animeshon.iam.admin.v1alpha1.CreateServiceAccountRequest}

| Field | Description |
| --- | --- |
| service_account | **[ ServiceAccount](#ServiceAccount)**<br/>The service account to create. |
## DeletePermissionRequest {#animeshon.iam.admin.v1alpha1.DeletePermissionRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the permission to delete. |
## DeleteRoleRequest {#animeshon.iam.admin.v1alpha1.DeleteRoleRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the role to delete. |
## DeleteServiceAccountRequest {#animeshon.iam.admin.v1alpha1.DeleteServiceAccountRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the service account to delete. |
## GetPermissionRequest {#animeshon.iam.admin.v1alpha1.GetPermissionRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the permission to retrieve. |
## GetRoleRequest {#animeshon.iam.admin.v1alpha1.GetRoleRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the role to retrieve. |
## GetServiceAccountRequest {#animeshon.iam.admin.v1alpha1.GetServiceAccountRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the service account to retrieve. |
## ListPermissionsRequest {#animeshon.iam.admin.v1alpha1.ListPermissionsRequest}

| Field | Description |
| --- | --- |
| page_size | **[ int32](#int32)**<br/>If unspecified, server will pick an appropriate default. |
| page_token | **[ string](#string)**<br/>The value returned from the previous call. |
| filter | **[ string](#string)**<br/>A filter to be applied to results. |
## ListPermissionsResponse {#animeshon.iam.admin.v1alpha1.ListPermissionsResponse}

| Field | Description |
| --- | --- |
| permissions | **[repeated Permission](#Permission)**<br/>The list of permissions. |
| next_page_token | **[ string](#string)**<br/>A token to retrieve next page of results. |
## ListRolesRequest {#animeshon.iam.admin.v1alpha1.ListRolesRequest}

| Field | Description |
| --- | --- |
| page_size | **[ int32](#int32)**<br/>If unspecified, server will pick an appropriate default. |
| page_token | **[ string](#string)**<br/>The value returned from the previous call. |
| filter | **[ string](#string)**<br/>A filter to be applied to results. |
## ListRolesResponse {#animeshon.iam.admin.v1alpha1.ListRolesResponse}

| Field | Description |
| --- | --- |
| roles | **[repeated Role](#Role)**<br/>The list of roles. |
| next_page_token | **[ string](#string)**<br/>A token to retrieve next page of results. |
## ListServiceAccountsRequest {#animeshon.iam.admin.v1alpha1.ListServiceAccountsRequest}

| Field | Description |
| --- | --- |
| parent | **[ string](#string)**<br/>The parent, which owns this collection of service accounts. |
| page_size | **[ int32](#int32)**<br/>If unspecified, server will pick an appropriate default. |
| page_token | **[ string](#string)**<br/>The value returned from the previous call. |
| filter | **[ string](#string)**<br/>A filter to be applied to results. |
## ListServiceAccountsResponse {#animeshon.iam.admin.v1alpha1.ListServiceAccountsResponse}

| Field | Description |
| --- | --- |
| service_accounts | **[repeated ServiceAccount](#ServiceAccount)**<br/>The list of service accounts. |
| next_page_token | **[ string](#string)**<br/>A token to retrieve next page of results. |
## Permission {#animeshon.iam.admin.v1alpha1.Permission}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of this permission. |
| display_name | **[ string](#string)**<br/>The display name of this permission. |
| description | **[ string](#string)**<br/>A brief description of what this permission is used for. |
## Role {#animeshon.iam.admin.v1alpha1.Role}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the role. |
| display_name | **[ string](#string)**<br/>The display name of this role. |
| description | **[ string](#string)**<br/>A brief description of what this role is used for. |
| included_permissions | **[repeated string](#string)**<br/>The names of the permissions this role grants when bound in an IAM policy. |
| etag | **[ bytes](#bytes)**<br/>Used to perform a consistent read-modify-write. |
## ServiceAccount {#animeshon.iam.admin.v1alpha1.ServiceAccount}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the service account. |
| uid | **[ string](#string)**<br/>The unique, stable numeric ID for the service account. |
| display_name | **[ string](#string)**<br/>The display name of this service account. |
| description | **[ string](#string)**<br/>A brief description of what this service account is used for. |
| oauth2_client_id | **[ string](#string)**<br/>OAuth2 client ID to use for the authentication flow. |
| oauth2_client_secret | **[ string](#string)**<br/>OAuth2 client secret to use for the authentication flow. |
## UpdatePermissionRequest {#animeshon.iam.admin.v1alpha1.UpdatePermissionRequest}

| Field | Description |
| --- | --- |
| permission | **[ Permission](#Permission)**<br/>The permission to update. |
| update_mask | **[ google.protobuf.FieldMask](#google.protobuf.FieldMask)**<br/>The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |
## UpdateRoleRequest {#animeshon.iam.admin.v1alpha1.UpdateRoleRequest}

| Field | Description |
| --- | --- |
| role | **[ Role](#Role)**<br/>The role to update. |
| update_mask | **[ google.protobuf.FieldMask](#google.protobuf.FieldMask)**<br/>The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |
## UpdateServiceAccountRequest {#animeshon.iam.admin.v1alpha1.UpdateServiceAccountRequest}

| Field | Description |
| --- | --- |
| service_account | **[ ServiceAccount](#ServiceAccount)**<br/>The service account to update. |
| update_mask | **[ google.protobuf.FieldMask](#google.protobuf.FieldMask)**<br/>The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |
