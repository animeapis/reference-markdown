# Protocol Documentation
<a name="top"></a>

## Table of Contents

- [animeshon/hub/v1alpha1/hub.proto](#animeshon/hub/v1alpha1/hub.proto)
    - [AdvertiseReferencesRequest](#animeshon.hub.v1alpha1.AdvertiseReferencesRequest)
    - [CreateRepositoryRequest](#animeshon.hub.v1alpha1.CreateRepositoryRequest)
    - [DeleteRepositoryRequest](#animeshon.hub.v1alpha1.DeleteRepositoryRequest)
    - [ListRepositoriesRequest](#animeshon.hub.v1alpha1.ListRepositoriesRequest)
    - [ListRepositoriesResponse](#animeshon.hub.v1alpha1.ListRepositoriesResponse)
    - [ReceivePackRequest](#animeshon.hub.v1alpha1.ReceivePackRequest)
    - [Repository](#animeshon.hub.v1alpha1.Repository)
    - [UploadPackRequest](#animeshon.hub.v1alpha1.UploadPackRequest)
  
    - [Git](#animeshon.hub.v1alpha1.Git)
    - [Hub](#animeshon.hub.v1alpha1.Hub)
  
- [Scalar Value Types](#scalar-value-types)



<a name="animeshon/hub/v1alpha1/hub.proto"></a>
<p align="right"><a href="#top">Top</a></p>

## animeshon/hub/v1alpha1/hub.proto



<a name="animeshon.hub.v1alpha1.AdvertiseReferencesRequest"></a>

### AdvertiseReferencesRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The resource name of the repository. |
| service | [string](#string) |  | The git service according to the git protocol. |






<a name="animeshon.hub.v1alpha1.CreateRepositoryRequest"></a>

### CreateRepositoryRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The resource name of the repository to be created. |






<a name="animeshon.hub.v1alpha1.DeleteRepositoryRequest"></a>

### DeleteRepositoryRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The resource name of the repository to be deleted. |






<a name="animeshon.hub.v1alpha1.ListRepositoriesRequest"></a>

### ListRepositoriesRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| parent | [string](#string) |  | The parent, which owns this collection of repositories. |
| page_size | [int32](#int32) |  | If unspecified, server will pick an appropriate default. |
| page_token | [string](#string) |  | The value returned from the previous call. |






<a name="animeshon.hub.v1alpha1.ListRepositoriesResponse"></a>

### ListRepositoriesResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| repositories | [Repository](#animeshon.hub.v1alpha1.Repository) | repeated | The list of repositories. |
| next_page_token | [string](#string) |  | A token to retrieve next page of results. |






<a name="animeshon.hub.v1alpha1.ReceivePackRequest"></a>

### ReceivePackRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The resource name of the repository. |
| body | [google.api.HttpBody](#google.api.HttpBody) |  | The request content, represented as an HttpBody. |






<a name="animeshon.hub.v1alpha1.Repository"></a>

### Repository



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The repository resource name. |






<a name="animeshon.hub.v1alpha1.UploadPackRequest"></a>

### UploadPackRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The resource name of the repository. |
| body | [google.api.HttpBody](#google.api.HttpBody) |  | The request content, represented as an HttpBody. |





 

 

 


<a name="animeshon.hub.v1alpha1.Git"></a>

### Git


| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| AdvertiseReferences | [AdvertiseReferencesRequest](#animeshon.hub.v1alpha1.AdvertiseReferencesRequest) | [.google.api.HttpBody](#google.api.HttpBody) |  |
| ReceivePack | [ReceivePackRequest](#animeshon.hub.v1alpha1.ReceivePackRequest) | [.google.api.HttpBody](#google.api.HttpBody) |  |
| UploadPack | [UploadPackRequest](#animeshon.hub.v1alpha1.UploadPackRequest) | [.google.api.HttpBody](#google.api.HttpBody) |  |


<a name="animeshon.hub.v1alpha1.Hub"></a>

### Hub


| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| CreateRepository | [CreateRepositoryRequest](#animeshon.hub.v1alpha1.CreateRepositoryRequest) | [Repository](#animeshon.hub.v1alpha1.Repository) |  |
| DeleteRepository | [DeleteRepositoryRequest](#animeshon.hub.v1alpha1.DeleteRepositoryRequest) | [.google.protobuf.Empty](#google.protobuf.Empty) |  |
| ListRepositories | [ListRepositoriesRequest](#animeshon.hub.v1alpha1.ListRepositoriesRequest) | [ListRepositoriesResponse](#animeshon.hub.v1alpha1.ListRepositoriesResponse) |  |

 



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

