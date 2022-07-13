# Package animeshon.hub.v1alpha1

## Index
- [Git](#animeshon.hub.v1alpha1.Git)
- [Hub](#animeshon.hub.v1alpha1.Hub)
- [AdvertiseReferencesRequest](#animeshon.hub.v1alpha1.AdvertiseReferencesRequest)
- [CreateRepositoryRequest](#animeshon.hub.v1alpha1.CreateRepositoryRequest)
- [DeleteRepositoryRequest](#animeshon.hub.v1alpha1.DeleteRepositoryRequest)
- [ListRepositoriesRequest](#animeshon.hub.v1alpha1.ListRepositoriesRequest)
- [ListRepositoriesResponse](#animeshon.hub.v1alpha1.ListRepositoriesResponse)
- [ReceivePackRequest](#animeshon.hub.v1alpha1.ReceivePackRequest)
- [Repository](#animeshon.hub.v1alpha1.Repository)
- [UploadPackRequest](#animeshon.hub.v1alpha1.UploadPackRequest)

## Git {#animeshon.hub.v1alpha1.Git}

| AdvertiseReferences |
| --- |
| **rpc** AdvertiseReferences([AdvertiseReferencesRequest](#animeshon.hub.v1alpha1.AdvertiseReferencesRequest)) [.google.api.HttpBody](#google.api.HttpBody)<br/> |

| ReceivePack |
| --- |
| **rpc** ReceivePack([ReceivePackRequest](#animeshon.hub.v1alpha1.ReceivePackRequest)) [.google.api.HttpBody](#google.api.HttpBody)<br/> |

| UploadPack |
| --- |
| **rpc** UploadPack([UploadPackRequest](#animeshon.hub.v1alpha1.UploadPackRequest)) [.google.api.HttpBody](#google.api.HttpBody)<br/> |

## Hub {#animeshon.hub.v1alpha1.Hub}

| CreateRepository |
| --- |
| **rpc** CreateRepository([CreateRepositoryRequest](#animeshon.hub.v1alpha1.CreateRepositoryRequest)) [Repository](#animeshon.hub.v1alpha1.Repository)<br/> |

| DeleteRepository |
| --- |
| **rpc** DeleteRepository([DeleteRepositoryRequest](#animeshon.hub.v1alpha1.DeleteRepositoryRequest)) [.google.protobuf.Empty](#google.protobuf.Empty)<br/> |

| ListRepositories |
| --- |
| **rpc** ListRepositories([ListRepositoriesRequest](#animeshon.hub.v1alpha1.ListRepositoriesRequest)) [ListRepositoriesResponse](#animeshon.hub.v1alpha1.ListRepositoriesResponse)<br/> |

## AdvertiseReferencesRequest {#animeshon.hub.v1alpha1.AdvertiseReferencesRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the repository. |
| service | **[ string](#string)**<br/>The git service according to the git protocol. |
## CreateRepositoryRequest {#animeshon.hub.v1alpha1.CreateRepositoryRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the repository to be created. |
## DeleteRepositoryRequest {#animeshon.hub.v1alpha1.DeleteRepositoryRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the repository to be deleted. |
## ListRepositoriesRequest {#animeshon.hub.v1alpha1.ListRepositoriesRequest}

| Field | Description |
| --- | --- |
| parent | **[ string](#string)**<br/>The parent, which owns this collection of repositories. |
| page_size | **[ int32](#int32)**<br/>If unspecified, server will pick an appropriate default. |
| page_token | **[ string](#string)**<br/>The value returned from the previous call. |
## ListRepositoriesResponse {#animeshon.hub.v1alpha1.ListRepositoriesResponse}

| Field | Description |
| --- | --- |
| repositories | **[repeated Repository](#Repository)**<br/>The list of repositories. |
| next_page_token | **[ string](#string)**<br/>A token to retrieve next page of results. |
## ReceivePackRequest {#animeshon.hub.v1alpha1.ReceivePackRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the repository. |
| body | **[ google.api.HttpBody](#google.api.HttpBody)**<br/>The request content, represented as an HttpBody. |
## Repository {#animeshon.hub.v1alpha1.Repository}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The repository resource name. |
## UploadPackRequest {#animeshon.hub.v1alpha1.UploadPackRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the repository. |
| body | **[ google.api.HttpBody](#google.api.HttpBody)**<br/>The request content, represented as an HttpBody. |
