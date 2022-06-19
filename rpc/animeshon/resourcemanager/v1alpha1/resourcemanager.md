# Protocol Documentation
<a name="top"></a>

## Table of Contents

- [animeshon/resourcemanager/v1alpha1/resourcemanager.proto](#animeshon/resourcemanager/v1alpha1/resourcemanager.proto)
    - [CreateOrganizationRequest](#animeshon.resourcemanager.v1alpha1.CreateOrganizationRequest)
    - [CreateTeamRequest](#animeshon.resourcemanager.v1alpha1.CreateTeamRequest)
    - [DeleteOrganizationRequest](#animeshon.resourcemanager.v1alpha1.DeleteOrganizationRequest)
    - [DeleteTeamRequest](#animeshon.resourcemanager.v1alpha1.DeleteTeamRequest)
    - [GetOrganizationRequest](#animeshon.resourcemanager.v1alpha1.GetOrganizationRequest)
    - [GetTeamRequest](#animeshon.resourcemanager.v1alpha1.GetTeamRequest)
    - [ListOrganizationsRequest](#animeshon.resourcemanager.v1alpha1.ListOrganizationsRequest)
    - [ListOrganizationsResponse](#animeshon.resourcemanager.v1alpha1.ListOrganizationsResponse)
    - [ListTeamsRequest](#animeshon.resourcemanager.v1alpha1.ListTeamsRequest)
    - [ListTeamsResponse](#animeshon.resourcemanager.v1alpha1.ListTeamsResponse)
    - [Organization](#animeshon.resourcemanager.v1alpha1.Organization)
    - [Team](#animeshon.resourcemanager.v1alpha1.Team)
    - [UpdateOrganizationRequest](#animeshon.resourcemanager.v1alpha1.UpdateOrganizationRequest)
    - [UpdateTeamRequest](#animeshon.resourcemanager.v1alpha1.UpdateTeamRequest)
  
    - [ResourceManager](#animeshon.resourcemanager.v1alpha1.ResourceManager)
  
- [Scalar Value Types](#scalar-value-types)



<a name="animeshon/resourcemanager/v1alpha1/resourcemanager.proto"></a>
<p align="right"><a href="#top">Top</a></p>

## animeshon/resourcemanager/v1alpha1/resourcemanager.proto



<a name="animeshon.resourcemanager.v1alpha1.CreateOrganizationRequest"></a>

### CreateOrganizationRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| organization | [Organization](#animeshon.resourcemanager.v1alpha1.Organization) |  | The organization to create. |






<a name="animeshon.resourcemanager.v1alpha1.CreateTeamRequest"></a>

### CreateTeamRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| team | [Team](#animeshon.resourcemanager.v1alpha1.Team) |  | The team to create. |






<a name="animeshon.resourcemanager.v1alpha1.DeleteOrganizationRequest"></a>

### DeleteOrganizationRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the organization to delete. |






<a name="animeshon.resourcemanager.v1alpha1.DeleteTeamRequest"></a>

### DeleteTeamRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the team to delete. |






<a name="animeshon.resourcemanager.v1alpha1.GetOrganizationRequest"></a>

### GetOrganizationRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the organization to retrieve. |






<a name="animeshon.resourcemanager.v1alpha1.GetTeamRequest"></a>

### GetTeamRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the team to retrieve. |






<a name="animeshon.resourcemanager.v1alpha1.ListOrganizationsRequest"></a>

### ListOrganizationsRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| page_size | [int32](#int32) |  | If unspecified, server will pick an appropriate default. |
| page_token | [string](#string) |  | The value returned from the previous call. |
| filter | [string](#string) |  | A filter to be applied to results. |






<a name="animeshon.resourcemanager.v1alpha1.ListOrganizationsResponse"></a>

### ListOrganizationsResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| organizations | [Organization](#animeshon.resourcemanager.v1alpha1.Organization) | repeated | The list of organizations. |
| next_page_token | [string](#string) |  | A token to retrieve next page of results. |






<a name="animeshon.resourcemanager.v1alpha1.ListTeamsRequest"></a>

### ListTeamsRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| page_size | [int32](#int32) |  | If unspecified, server will pick an appropriate default. |
| page_token | [string](#string) |  | The value returned from the previous call. |
| filter | [string](#string) |  | A filter to be applied to results. |






<a name="animeshon.resourcemanager.v1alpha1.ListTeamsResponse"></a>

### ListTeamsResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| teams | [Team](#animeshon.resourcemanager.v1alpha1.Team) | repeated | The list of teams. |
| next_page_token | [string](#string) |  | A token to retrieve next page of results. |






<a name="animeshon.resourcemanager.v1alpha1.Organization"></a>

### Organization



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  |  |






<a name="animeshon.resourcemanager.v1alpha1.Team"></a>

### Team



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  |  |






<a name="animeshon.resourcemanager.v1alpha1.UpdateOrganizationRequest"></a>

### UpdateOrganizationRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| organization | [Organization](#animeshon.resourcemanager.v1alpha1.Organization) |  | The organization to update. |
| update_mask | [google.protobuf.FieldMask](#google.protobuf.FieldMask) |  | The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |






<a name="animeshon.resourcemanager.v1alpha1.UpdateTeamRequest"></a>

### UpdateTeamRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| team | [Team](#animeshon.resourcemanager.v1alpha1.Team) |  | The team to update. |
| update_mask | [google.protobuf.FieldMask](#google.protobuf.FieldMask) |  | The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |





 

 

 


<a name="animeshon.resourcemanager.v1alpha1.ResourceManager"></a>

### ResourceManager


| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| GetOrganization | [GetOrganizationRequest](#animeshon.resourcemanager.v1alpha1.GetOrganizationRequest) | [Organization](#animeshon.resourcemanager.v1alpha1.Organization) |  |
| ListOrganizations | [ListOrganizationsRequest](#animeshon.resourcemanager.v1alpha1.ListOrganizationsRequest) | [ListOrganizationsResponse](#animeshon.resourcemanager.v1alpha1.ListOrganizationsResponse) |  |
| CreateOrganization | [CreateOrganizationRequest](#animeshon.resourcemanager.v1alpha1.CreateOrganizationRequest) | [Organization](#animeshon.resourcemanager.v1alpha1.Organization) |  |
| UpdateOrganization | [UpdateOrganizationRequest](#animeshon.resourcemanager.v1alpha1.UpdateOrganizationRequest) | [Organization](#animeshon.resourcemanager.v1alpha1.Organization) |  |
| DeleteOrganization | [DeleteOrganizationRequest](#animeshon.resourcemanager.v1alpha1.DeleteOrganizationRequest) | [.google.protobuf.Empty](#google.protobuf.Empty) |  |
| GetTeam | [GetTeamRequest](#animeshon.resourcemanager.v1alpha1.GetTeamRequest) | [Team](#animeshon.resourcemanager.v1alpha1.Team) |  |
| ListTeams | [ListTeamsRequest](#animeshon.resourcemanager.v1alpha1.ListTeamsRequest) | [ListTeamsResponse](#animeshon.resourcemanager.v1alpha1.ListTeamsResponse) |  |
| CreateTeam | [CreateTeamRequest](#animeshon.resourcemanager.v1alpha1.CreateTeamRequest) | [Team](#animeshon.resourcemanager.v1alpha1.Team) |  |
| UpdateTeam | [UpdateTeamRequest](#animeshon.resourcemanager.v1alpha1.UpdateTeamRequest) | [Team](#animeshon.resourcemanager.v1alpha1.Team) |  |
| DeleteTeam | [DeleteTeamRequest](#animeshon.resourcemanager.v1alpha1.DeleteTeamRequest) | [.google.protobuf.Empty](#google.protobuf.Empty) |  |

 



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

