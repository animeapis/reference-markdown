# Protocol Documentation
<a name="top"></a>

## Table of Contents

- [animeshon/credentials/v1alpha1/credentials.proto](#animeshon/credentials/v1alpha1/credentials.proto)
    - [ActAsCredentialsRequest](#animeshon.credentials.v1alpha1.ActAsCredentialsRequest)
    - [ActAsCredentialsResponse](#animeshon.credentials.v1alpha1.ActAsCredentialsResponse)
    - [ActAsCredentialsResponse.Basic](#animeshon.credentials.v1alpha1.ActAsCredentialsResponse.Basic)
    - [CreateCredentialsRequest](#animeshon.credentials.v1alpha1.CreateCredentialsRequest)
    - [CreateCredentialsRequest.Basic](#animeshon.credentials.v1alpha1.CreateCredentialsRequest.Basic)
    - [CreateCredentialsRequest.OAuth2](#animeshon.credentials.v1alpha1.CreateCredentialsRequest.OAuth2)
    - [Credentials](#animeshon.credentials.v1alpha1.Credentials)
    - [DeleteCredentialsRequest](#animeshon.credentials.v1alpha1.DeleteCredentialsRequest)
    - [ExchangeRequest](#animeshon.credentials.v1alpha1.ExchangeRequest)
    - [ExchangeResponse](#animeshon.credentials.v1alpha1.ExchangeResponse)
    - [GetCredentialsRequest](#animeshon.credentials.v1alpha1.GetCredentialsRequest)
    - [ListCredentialsRequest](#animeshon.credentials.v1alpha1.ListCredentialsRequest)
    - [ListCredentialsResponse](#animeshon.credentials.v1alpha1.ListCredentialsResponse)
    - [SignInRequest](#animeshon.credentials.v1alpha1.SignInRequest)
    - [SignInResponse](#animeshon.credentials.v1alpha1.SignInResponse)
  
    - [Credentials.AuthenticationMethod](#animeshon.credentials.v1alpha1.Credentials.AuthenticationMethod)
  
    - [Keeper](#animeshon.credentials.v1alpha1.Keeper)
    - [OAuth2](#animeshon.credentials.v1alpha1.OAuth2)
  
- [Scalar Value Types](#scalar-value-types)



<a name="animeshon/credentials/v1alpha1/credentials.proto"></a>
<p align="right"><a href="#top">Top</a></p>

## animeshon/credentials/v1alpha1/credentials.proto



<a name="animeshon.credentials.v1alpha1.ActAsCredentialsRequest"></a>

### ActAsCredentialsRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The resorce name of the credentials. |






<a name="animeshon.credentials.v1alpha1.ActAsCredentialsResponse"></a>

### ActAsCredentialsResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| access_token | [string](#string) |  | The access token to be attached in the request headers. Only returned for OAuth 2.0 credentials. |
| basic | [ActAsCredentialsResponse.Basic](#animeshon.credentials.v1alpha1.ActAsCredentialsResponse.Basic) |  | The basic credentials (username and password) to be used to authenticate requests, as different APIs implement authentication in different ways, the plain basic credentials are provided as-is. |






<a name="animeshon.credentials.v1alpha1.ActAsCredentialsResponse.Basic"></a>

### ActAsCredentialsResponse.Basic



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| username | [string](#string) |  |  |
| password | [string](#string) |  |  |






<a name="animeshon.credentials.v1alpha1.CreateCredentialsRequest"></a>

### CreateCredentialsRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| credentials | [Credentials](#animeshon.credentials.v1alpha1.Credentials) |  | The credentials to create. |
| basic | [CreateCredentialsRequest.Basic](#animeshon.credentials.v1alpha1.CreateCredentialsRequest.Basic) |  | Basic authentication credentials composed by username and password. |
| oauth2 | [CreateCredentialsRequest.OAuth2](#animeshon.credentials.v1alpha1.CreateCredentialsRequest.OAuth2) |  | OAuth 2.0 authentication credentials composed by a refresh token. |






<a name="animeshon.credentials.v1alpha1.CreateCredentialsRequest.Basic"></a>

### CreateCredentialsRequest.Basic



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| username | [string](#string) |  |  |
| password | [string](#string) |  |  |






<a name="animeshon.credentials.v1alpha1.CreateCredentialsRequest.OAuth2"></a>

### CreateCredentialsRequest.OAuth2



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| principal | [string](#string) |  |  |
| refresh_token | [string](#string) |  |  |






<a name="animeshon.credentials.v1alpha1.Credentials"></a>

### Credentials
Credentials are persistent authentication


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The resorce name of the credentials. |
| uid | [string](#string) |  | The unique and immutable identifier of the credentials. |
| principal | [string](#string) |  | The principal of the credentialscode, usually the username. |
| active | [google.protobuf.BoolValue](#google.protobuf.BoolValue) |  | Whether these credentials are active and can be used to perform requests. |
| authentication_method | [Credentials.AuthenticationMethod](#animeshon.credentials.v1alpha1.Credentials.AuthenticationMethod) |  | Which authentication method is used by the credentials. |
| last_activity_time | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | When the credentials were last used. |






<a name="animeshon.credentials.v1alpha1.DeleteCredentialsRequest"></a>

### DeleteCredentialsRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the credentials to delete. |






<a name="animeshon.credentials.v1alpha1.ExchangeRequest"></a>

### ExchangeRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The resorce name of the flow. |
| code | [string](#string) |  | The OAuth 2.0 code returned from the authentication flow. |
| state | [string](#string) |  | The OAuth 2.0 state returned from the authentication flow. |






<a name="animeshon.credentials.v1alpha1.ExchangeResponse"></a>

### ExchangeResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| credentials | [Credentials](#animeshon.credentials.v1alpha1.Credentials) |  | The credentials created by the authentication flow. |






<a name="animeshon.credentials.v1alpha1.GetCredentialsRequest"></a>

### GetCredentialsRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the credentials to retrieve. |






<a name="animeshon.credentials.v1alpha1.ListCredentialsRequest"></a>

### ListCredentialsRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| parent | [string](#string) |  | The parent, which owns this collection of credentials. |
| page_size | [int32](#int32) |  | If unspecified, server will pick an appropriate default. |
| page_token | [string](#string) |  | The value returned from the previous call. |
| filter | [string](#string) |  | A filter to be applied to results. |






<a name="animeshon.credentials.v1alpha1.ListCredentialsResponse"></a>

### ListCredentialsResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| credentials | [Credentials](#animeshon.credentials.v1alpha1.Credentials) | repeated | The list of credentials. |
| next_page_token | [string](#string) |  | A token to retrieve next page of results. |






<a name="animeshon.credentials.v1alpha1.SignInRequest"></a>

### SignInRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The resorce name of the flow. |






<a name="animeshon.credentials.v1alpha1.SignInResponse"></a>

### SignInResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| authorization_url | [string](#string) |  | The authorization url that the user should be redirect to for web sign-in. |





 


<a name="animeshon.credentials.v1alpha1.Credentials.AuthenticationMethod"></a>

### Credentials.AuthenticationMethod


| Name | Number | Description |
| ---- | ------ | ----------- |
| AUTHENTICATION_METHOD_UNSPECIFIED | 0 | The default value. This value is used if the state is omitted. |
| BASIC | 1 | The authentication method used is username/password. |
| OAUTH2 | 2 | The authentication method used is OAuth 2.0. |


 

 


<a name="animeshon.credentials.v1alpha1.Keeper"></a>

### Keeper


| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| GetCredentials | [GetCredentialsRequest](#animeshon.credentials.v1alpha1.GetCredentialsRequest) | [Credentials](#animeshon.credentials.v1alpha1.Credentials) |  |
| ListCredentials | [ListCredentialsRequest](#animeshon.credentials.v1alpha1.ListCredentialsRequest) | [ListCredentialsResponse](#animeshon.credentials.v1alpha1.ListCredentialsResponse) |  |
| CreateCredentials | [CreateCredentialsRequest](#animeshon.credentials.v1alpha1.CreateCredentialsRequest) | [Credentials](#animeshon.credentials.v1alpha1.Credentials) |  |
| DeleteCredentials | [DeleteCredentialsRequest](#animeshon.credentials.v1alpha1.DeleteCredentialsRequest) | [.google.protobuf.Empty](#google.protobuf.Empty) |  |
| ActAsCredentials | [ActAsCredentialsRequest](#animeshon.credentials.v1alpha1.ActAsCredentialsRequest) | [ActAsCredentialsResponse](#animeshon.credentials.v1alpha1.ActAsCredentialsResponse) |  |


<a name="animeshon.credentials.v1alpha1.OAuth2"></a>

### OAuth2


| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| SignIn | [SignInRequest](#animeshon.credentials.v1alpha1.SignInRequest) | [SignInResponse](#animeshon.credentials.v1alpha1.SignInResponse) |  |
| Exchange | [ExchangeRequest](#animeshon.credentials.v1alpha1.ExchangeRequest) | [ExchangeResponse](#animeshon.credentials.v1alpha1.ExchangeResponse) |  |

 



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

