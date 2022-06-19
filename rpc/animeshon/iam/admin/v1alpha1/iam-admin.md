# Protocol Documentation
<a name="top"></a>

## Table of Contents

- [animeshon/iam/admin/v1alpha1/iam.proto](#animeshon/iam/admin/v1alpha1/iam.proto)
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
  
    - [IAM](#animeshon.iam.admin.v1alpha1.IAM)
  
- [Scalar Value Types](#scalar-value-types)



<a name="animeshon/iam/admin/v1alpha1/iam.proto"></a>
<p align="right"><a href="#top">Top</a></p>

## animeshon/iam/admin/v1alpha1/iam.proto



<a name="animeshon.iam.admin.v1alpha1.CreatePermissionRequest"></a>

### CreatePermissionRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| permission | [Permission](#animeshon.iam.admin.v1alpha1.Permission) |  | The permission to create. |






<a name="animeshon.iam.admin.v1alpha1.CreateRoleRequest"></a>

### CreateRoleRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| role | [Role](#animeshon.iam.admin.v1alpha1.Role) |  | The role to create. |






<a name="animeshon.iam.admin.v1alpha1.CreateServiceAccountRequest"></a>

### CreateServiceAccountRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| service_account | [ServiceAccount](#animeshon.iam.admin.v1alpha1.ServiceAccount) |  | The service account to create. |






<a name="animeshon.iam.admin.v1alpha1.DeletePermissionRequest"></a>

### DeletePermissionRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the permission to delete. |






<a name="animeshon.iam.admin.v1alpha1.DeleteRoleRequest"></a>

### DeleteRoleRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the role to delete. |






<a name="animeshon.iam.admin.v1alpha1.DeleteServiceAccountRequest"></a>

### DeleteServiceAccountRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the service account to delete. |






<a name="animeshon.iam.admin.v1alpha1.GetPermissionRequest"></a>

### GetPermissionRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the permission to retrieve. |






<a name="animeshon.iam.admin.v1alpha1.GetRoleRequest"></a>

### GetRoleRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the role to retrieve. |






<a name="animeshon.iam.admin.v1alpha1.GetServiceAccountRequest"></a>

### GetServiceAccountRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the service account to retrieve. |






<a name="animeshon.iam.admin.v1alpha1.ListPermissionsRequest"></a>

### ListPermissionsRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| page_size | [int32](#int32) |  | If unspecified, server will pick an appropriate default. |
| page_token | [string](#string) |  | The value returned from the previous call. |
| filter | [string](#string) |  | A filter to be applied to results. |






<a name="animeshon.iam.admin.v1alpha1.ListPermissionsResponse"></a>

### ListPermissionsResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| permissions | [Permission](#animeshon.iam.admin.v1alpha1.Permission) | repeated | The list of permissions. |
| next_page_token | [string](#string) |  | A token to retrieve next page of results. |






<a name="animeshon.iam.admin.v1alpha1.ListRolesRequest"></a>

### ListRolesRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| page_size | [int32](#int32) |  | If unspecified, server will pick an appropriate default. |
| page_token | [string](#string) |  | The value returned from the previous call. |
| filter | [string](#string) |  | A filter to be applied to results. |






<a name="animeshon.iam.admin.v1alpha1.ListRolesResponse"></a>

### ListRolesResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| roles | [Role](#animeshon.iam.admin.v1alpha1.Role) | repeated | The list of roles. |
| next_page_token | [string](#string) |  | A token to retrieve next page of results. |






<a name="animeshon.iam.admin.v1alpha1.ListServiceAccountsRequest"></a>

### ListServiceAccountsRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| parent | [string](#string) |  | The parent, which owns this collection of service accounts. |
| page_size | [int32](#int32) |  | If unspecified, server will pick an appropriate default. |
| page_token | [string](#string) |  | The value returned from the previous call. |
| filter | [string](#string) |  | A filter to be applied to results. |






<a name="animeshon.iam.admin.v1alpha1.ListServiceAccountsResponse"></a>

### ListServiceAccountsResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| service_accounts | [ServiceAccount](#animeshon.iam.admin.v1alpha1.ServiceAccount) | repeated | The list of service accounts. |
| next_page_token | [string](#string) |  | A token to retrieve next page of results. |






<a name="animeshon.iam.admin.v1alpha1.Permission"></a>

### Permission



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of this permission. |
| display_name | [string](#string) |  | The display name of this permission. |
| description | [string](#string) |  | A brief description of what this permission is used for. |






<a name="animeshon.iam.admin.v1alpha1.Role"></a>

### Role



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the role. |
| display_name | [string](#string) |  | The display name of this role. |
| description | [string](#string) |  | A brief description of what this role is used for. |
| included_permissions | [string](#string) | repeated | The names of the permissions this role grants when bound in an IAM policy. |
| etag | [bytes](#bytes) |  | Used to perform a consistent read-modify-write. |






<a name="animeshon.iam.admin.v1alpha1.ServiceAccount"></a>

### ServiceAccount



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the service account. |
| uid | [string](#string) |  | The unique, stable numeric ID for the service account. |
| display_name | [string](#string) |  | The display name of this service account. |
| description | [string](#string) |  | A brief description of what this service account is used for. |
| oauth2_client_id | [string](#string) |  | OAuth2 client ID to use for the authentication flow. |
| oauth2_client_secret | [string](#string) |  | OAuth2 client secret to use for the authentication flow. |






<a name="animeshon.iam.admin.v1alpha1.UpdatePermissionRequest"></a>

### UpdatePermissionRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| permission | [Permission](#animeshon.iam.admin.v1alpha1.Permission) |  | The permission to update. |
| update_mask | [google.protobuf.FieldMask](#google.protobuf.FieldMask) |  | The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |






<a name="animeshon.iam.admin.v1alpha1.UpdateRoleRequest"></a>

### UpdateRoleRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| role | [Role](#animeshon.iam.admin.v1alpha1.Role) |  | The role to update. |
| update_mask | [google.protobuf.FieldMask](#google.protobuf.FieldMask) |  | The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |






<a name="animeshon.iam.admin.v1alpha1.UpdateServiceAccountRequest"></a>

### UpdateServiceAccountRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| service_account | [ServiceAccount](#animeshon.iam.admin.v1alpha1.ServiceAccount) |  | The service account to update. |
| update_mask | [google.protobuf.FieldMask](#google.protobuf.FieldMask) |  | The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |





 

 

 


<a name="animeshon.iam.admin.v1alpha1.IAM"></a>

### IAM


| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| GetServiceAccount | [GetServiceAccountRequest](#animeshon.iam.admin.v1alpha1.GetServiceAccountRequest) | [ServiceAccount](#animeshon.iam.admin.v1alpha1.ServiceAccount) |  |
| ListServiceAccounts | [ListServiceAccountsRequest](#animeshon.iam.admin.v1alpha1.ListServiceAccountsRequest) | [ListServiceAccountsResponse](#animeshon.iam.admin.v1alpha1.ListServiceAccountsResponse) |  |
| CreateServiceAccount | [CreateServiceAccountRequest](#animeshon.iam.admin.v1alpha1.CreateServiceAccountRequest) | [ServiceAccount](#animeshon.iam.admin.v1alpha1.ServiceAccount) |  |
| UpdateServiceAccount | [UpdateServiceAccountRequest](#animeshon.iam.admin.v1alpha1.UpdateServiceAccountRequest) | [ServiceAccount](#animeshon.iam.admin.v1alpha1.ServiceAccount) |  |
| DeleteServiceAccount | [DeleteServiceAccountRequest](#animeshon.iam.admin.v1alpha1.DeleteServiceAccountRequest) | [.google.protobuf.Empty](#google.protobuf.Empty) |  |
| GetRole | [GetRoleRequest](#animeshon.iam.admin.v1alpha1.GetRoleRequest) | [Role](#animeshon.iam.admin.v1alpha1.Role) |  |
| ListRoles | [ListRolesRequest](#animeshon.iam.admin.v1alpha1.ListRolesRequest) | [ListRolesResponse](#animeshon.iam.admin.v1alpha1.ListRolesResponse) |  |
| CreateRole | [CreateRoleRequest](#animeshon.iam.admin.v1alpha1.CreateRoleRequest) | [Role](#animeshon.iam.admin.v1alpha1.Role) |  |
| UpdateRole | [UpdateRoleRequest](#animeshon.iam.admin.v1alpha1.UpdateRoleRequest) | [Role](#animeshon.iam.admin.v1alpha1.Role) |  |
| DeleteRole | [DeleteRoleRequest](#animeshon.iam.admin.v1alpha1.DeleteRoleRequest) | [.google.protobuf.Empty](#google.protobuf.Empty) |  |
| GetPermission | [GetPermissionRequest](#animeshon.iam.admin.v1alpha1.GetPermissionRequest) | [Permission](#animeshon.iam.admin.v1alpha1.Permission) |  |
| ListPermissions | [ListPermissionsRequest](#animeshon.iam.admin.v1alpha1.ListPermissionsRequest) | [ListPermissionsResponse](#animeshon.iam.admin.v1alpha1.ListPermissionsResponse) |  |
| CreatePermission | [CreatePermissionRequest](#animeshon.iam.admin.v1alpha1.CreatePermissionRequest) | [Permission](#animeshon.iam.admin.v1alpha1.Permission) |  |
| UpdatePermission | [UpdatePermissionRequest](#animeshon.iam.admin.v1alpha1.UpdatePermissionRequest) | [Permission](#animeshon.iam.admin.v1alpha1.Permission) |  |
| DeletePermission | [DeletePermissionRequest](#animeshon.iam.admin.v1alpha1.DeletePermissionRequest) | [.google.protobuf.Empty](#google.protobuf.Empty) |  |

 



## Scalar Value Types

| .proto Type | Notes | C++ | Java | Python | Go | C# | PHP | Ruby |
| ----------- | ----- | --- | ---- | ------ | -- | -- | --- | ---- |
| <a name="double" /> double |  | double | double | float | float64 | double | float | Float |
| <a name="float" /> float |  | float | float | float | float32 | float | float | Float |
| <a name="int32" /> int32 | Uses variable-length encoding. Inefficient for encoding negative numbers – if your field is likely to have negative values, use sint32 instead. | int32 | int | int | int32 | int | integer | Bignum or Fixnum (as required) |
| <a name="int64" /> int64 | Uses variable-length encoding. Inefficient for encoding negative numbers – if your field is likely to have negative values, use sint64 instead. | int64 | long | int/long | int64 | long | integer/string | Bignum |
| <a name="uint32" /> uint32 | Uses variable-length encoding. | uint32 | int | int/long | uint32 | uint | integer | Bignum or Fixnum (as required) |
| <a name="uint64" /> uint64 | Uses variable-length encoding. | uint64 | long | int/long | uint64 | ulong | integer/string | Bignum or Fixnum (as required) |
| <a name="sint32" /> sint32 | Uses variable-length encoding. Signed int value. These more efficiently encode negative numbers than regular int32s. | int32 | int | int | int32 | int | integer | Bignum or Fixnum (as required) |
| <a name="sint64" /> sint64 | Uses variable-length encoding. Signed int value. These more efficiently encode negative numbers than regular int64s. | int64 | long | int/long | int64 | long | integer/string | Bignum |
| <a name="fixed32" /> fixed32 | Always four bytes. More efficient than uint32 if values are often greater than 2^28. | uint32 | int | int | uint32 | uint | integer | Bignum or Fixnum (as required) |
| <a name="fixed64" /> fixed64 | Always eight bytes. More efficient than uint64 if values are often greater than 2^56. | uint64 | long | int/long | uint64 | ulong | integer/string | Bignum |
| <a name="sfixed32" /> sfixed32 | Always four bytes. | int32 | int | int | int32 | int | integer | Bignum or Fixnum (as required) |
| <a name="sfixed64" /> sfixed64 | Always eight bytes. | int64 | long | int/long | int64 | long | integer/string | Bignum |
| <a name="bool" /> bool |  | bool | boolean | boolean | bool | bool | boolean | TrueClass/FalseClass |
| <a name="string" /> string | A string must always contain UTF-8 encoded or 7-bit ASCII text. | string | String | str/unicode | string | string | string | String (UTF-8) |
| <a name="bytes" /> bytes | May contain any arbitrary sequence of bytes. | string | ByteString | str | []byte | ByteString | string | String (ASCII-8BIT) |

