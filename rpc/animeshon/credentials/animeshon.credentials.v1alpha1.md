# Package animeshon.credentials.v1alpha1

## Index
- [Keeper](#animeshon.credentials.v1alpha1.Keeper)
- [OAuth2](#animeshon.credentials.v1alpha1.OAuth2)
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

## Keeper {#animeshon.credentials.v1alpha1.Keeper}

| GetCredentials |
| --- |
| **rpc** GetCredentials([GetCredentialsRequest](#animeshon.credentials.v1alpha1.GetCredentialsRequest)) [Credentials](#animeshon.credentials.v1alpha1.Credentials)<br/> |

| ListCredentials |
| --- |
| **rpc** ListCredentials([ListCredentialsRequest](#animeshon.credentials.v1alpha1.ListCredentialsRequest)) [ListCredentialsResponse](#animeshon.credentials.v1alpha1.ListCredentialsResponse)<br/> |

| CreateCredentials |
| --- |
| **rpc** CreateCredentials([CreateCredentialsRequest](#animeshon.credentials.v1alpha1.CreateCredentialsRequest)) [Credentials](#animeshon.credentials.v1alpha1.Credentials)<br/> |

| DeleteCredentials |
| --- |
| **rpc** DeleteCredentials([DeleteCredentialsRequest](#animeshon.credentials.v1alpha1.DeleteCredentialsRequest)) [.google.protobuf.Empty](#google.protobuf.Empty)<br/> |

| ActAsCredentials |
| --- |
| **rpc** ActAsCredentials([ActAsCredentialsRequest](#animeshon.credentials.v1alpha1.ActAsCredentialsRequest)) [ActAsCredentialsResponse](#animeshon.credentials.v1alpha1.ActAsCredentialsResponse)<br/> |

## OAuth2 {#animeshon.credentials.v1alpha1.OAuth2}

| SignIn |
| --- |
| **rpc** SignIn([SignInRequest](#animeshon.credentials.v1alpha1.SignInRequest)) [SignInResponse](#animeshon.credentials.v1alpha1.SignInResponse)<br/> |

| Exchange |
| --- |
| **rpc** Exchange([ExchangeRequest](#animeshon.credentials.v1alpha1.ExchangeRequest)) [ExchangeResponse](#animeshon.credentials.v1alpha1.ExchangeResponse)<br/> |

## ActAsCredentialsRequest {#animeshon.credentials.v1alpha1.ActAsCredentialsRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resorce name of the credentials. |
## ActAsCredentialsResponse {#animeshon.credentials.v1alpha1.ActAsCredentialsResponse}

| Field | Description |
| --- | --- |
| access_token | **[ string](#string)**<br/>The access token to be attached in the request headers. Only returned for OAuth 2.0 credentials. |
| basic | **[ ActAsCredentialsResponse.Basic](#ActAsCredentialsResponse.Basic)**<br/>The basic credentials (username and password) to be used to authenticate requests, as different APIs implement authentication in different ways, the plain basic credentials are provided as-is. |
## ActAsCredentialsResponse.Basic {#animeshon.credentials.v1alpha1.ActAsCredentialsResponse.Basic}

| Field | Description |
| --- | --- |
| username | **[ string](#string)**<br/> |
| password | **[ string](#string)**<br/> |
## CreateCredentialsRequest {#animeshon.credentials.v1alpha1.CreateCredentialsRequest}

| Field | Description |
| --- | --- |
| credentials | **[ Credentials](#Credentials)**<br/>The credentials to create. |
| **[oneof](https://developers.google.com/protocol-buffers/docs/proto3#oneof)** _payload_<br />basic | **[ CreateCredentialsRequest.Basic](#CreateCredentialsRequest.Basic)**<br/>Basic authentication credentials composed by username and password. |
| **[oneof](https://developers.google.com/protocol-buffers/docs/proto3#oneof)** _payload_<br />oauth2 | **[ CreateCredentialsRequest.OAuth2](#CreateCredentialsRequest.OAuth2)**<br/>OAuth 2.0 authentication credentials composed by a refresh token. |
## CreateCredentialsRequest.Basic {#animeshon.credentials.v1alpha1.CreateCredentialsRequest.Basic}

| Field | Description |
| --- | --- |
| username | **[ string](#string)**<br/> |
| password | **[ string](#string)**<br/> |
## CreateCredentialsRequest.OAuth2 {#animeshon.credentials.v1alpha1.CreateCredentialsRequest.OAuth2}

| Field | Description |
| --- | --- |
| principal | **[ string](#string)**<br/> |
| refresh_token | **[ string](#string)**<br/> |
## Credentials {#animeshon.credentials.v1alpha1.Credentials}
Credentials are persistent authentication
| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resorce name of the credentials. |
| uid | **[ string](#string)**<br/>The unique and immutable identifier of the credentials. |
| principal | **[ string](#string)**<br/>The principal of the credentialscode, usually the username. |
| active | **[ google.protobuf.BoolValue](#google.protobuf.BoolValue)**<br/>Whether these credentials are active and can be used to perform requests. |
| authentication_method | **[ Credentials.AuthenticationMethod](#Credentials.AuthenticationMethod)**<br/>Which authentication method is used by the credentials. |
| last_activity_time | **[ google.protobuf.Timestamp](#google.protobuf.Timestamp)**<br/>When the credentials were last used. |
## DeleteCredentialsRequest {#animeshon.credentials.v1alpha1.DeleteCredentialsRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the credentials to delete. |
## ExchangeRequest {#animeshon.credentials.v1alpha1.ExchangeRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resorce name of the flow. |
| code | **[ string](#string)**<br/>The OAuth 2.0 code returned from the authentication flow. |
| state | **[ string](#string)**<br/>The OAuth 2.0 state returned from the authentication flow. |
## ExchangeResponse {#animeshon.credentials.v1alpha1.ExchangeResponse}

| Field | Description |
| --- | --- |
| credentials | **[ Credentials](#Credentials)**<br/>The credentials created by the authentication flow. |
## GetCredentialsRequest {#animeshon.credentials.v1alpha1.GetCredentialsRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the credentials to retrieve. |
## ListCredentialsRequest {#animeshon.credentials.v1alpha1.ListCredentialsRequest}

| Field | Description |
| --- | --- |
| parent | **[ string](#string)**<br/>The parent, which owns this collection of credentials. |
| page_size | **[ int32](#int32)**<br/>If unspecified, server will pick an appropriate default. |
| page_token | **[ string](#string)**<br/>The value returned from the previous call. |
| filter | **[ string](#string)**<br/>A filter to be applied to results. |
## ListCredentialsResponse {#animeshon.credentials.v1alpha1.ListCredentialsResponse}

| Field | Description |
| --- | --- |
| credentials | **[repeated Credentials](#Credentials)**<br/>The list of credentials. |
| next_page_token | **[ string](#string)**<br/>A token to retrieve next page of results. |
## SignInRequest {#animeshon.credentials.v1alpha1.SignInRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resorce name of the flow. |
## SignInResponse {#animeshon.credentials.v1alpha1.SignInResponse}

| Field | Description |
| --- | --- |
| authorization_url | **[ string](#string)**<br/>The authorization url that the user should be redirect to for web sign-in. |

## Credentials.AuthenticationMethod {#animeshon.credentials.v1alpha1.Credentials.AuthenticationMethod}


| Name | Description |
| --- | --- |
| AUTHENTICATION_METHOD_UNSPECIFIED | The default value. This value is used if the state is omitted. |
| BASIC | The authentication method used is username/password. |
| OAUTH2 | The authentication method used is OAuth 2.0. |
