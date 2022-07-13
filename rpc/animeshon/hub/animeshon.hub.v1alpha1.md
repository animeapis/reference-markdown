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

## <span id="animeshon.hub.v1alpha1.Git">Git</span>



| <span id="animeshon.hub.v1alpha1.Git.AdvertiseReferences">AdvertiseReferences</span> |
| --- |
| **rpc AdvertiseReferences([AdvertiseReferencesRequest](#animeshon.hub.v1alpha1.AdvertiseReferencesRequest)) [.google.api.HttpBody](#google.api.HttpBody)**<br/><br/> |

| <span id="animeshon.hub.v1alpha1.Git.ReceivePack">ReceivePack</span> |
| --- |
| **rpc ReceivePack([ReceivePackRequest](#animeshon.hub.v1alpha1.ReceivePackRequest)) [.google.api.HttpBody](#google.api.HttpBody)**<br/><br/> |

| <span id="animeshon.hub.v1alpha1.Git.UploadPack">UploadPack</span> |
| --- |
| **rpc UploadPack([UploadPackRequest](#animeshon.hub.v1alpha1.UploadPackRequest)) [.google.api.HttpBody](#google.api.HttpBody)**<br/><br/> |

## <span id="animeshon.hub.v1alpha1.Hub">Hub</span>



| <span id="animeshon.hub.v1alpha1.Hub.CreateRepository">CreateRepository</span> |
| --- |
| **rpc CreateRepository([CreateRepositoryRequest](#animeshon.hub.v1alpha1.CreateRepositoryRequest)) [Repository](#animeshon.hub.v1alpha1.Repository)**<br/><br/> |

| <span id="animeshon.hub.v1alpha1.Hub.DeleteRepository">DeleteRepository</span> |
| --- |
| **rpc DeleteRepository([DeleteRepositoryRequest](#animeshon.hub.v1alpha1.DeleteRepositoryRequest)) [.google.protobuf.Empty](#google.protobuf.Empty)**<br/><br/> |

| <span id="animeshon.hub.v1alpha1.Hub.ListRepositories">ListRepositories</span> |
| --- |
| **rpc ListRepositories([ListRepositoriesRequest](#animeshon.hub.v1alpha1.ListRepositoriesRequest)) [ListRepositoriesResponse](#animeshon.hub.v1alpha1.ListRepositoriesResponse)**<br/><br/> |


## <span id="animeshon.hub.v1alpha1.AdvertiseReferencesRequest">AdvertiseReferencesRequest</span>



| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the repository. |
| service | **[ string](#string)**<br/>The git service according to the git protocol. |

## <span id="animeshon.hub.v1alpha1.CreateRepositoryRequest">CreateRepositoryRequest</span>



| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the repository to be created. |

## <span id="animeshon.hub.v1alpha1.DeleteRepositoryRequest">DeleteRepositoryRequest</span>



| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the repository to be deleted. |

## <span id="animeshon.hub.v1alpha1.ListRepositoriesRequest">ListRepositoriesRequest</span>



| Field | Description |
| --- | --- |
| parent | **[ string](#string)**<br/>The parent, which owns this collection of repositories. |
| page_size | **[ int32](#int32)**<br/>If unspecified, server will pick an appropriate default. |
| page_token | **[ string](#string)**<br/>The value returned from the previous call. |

## <span id="animeshon.hub.v1alpha1.ListRepositoriesResponse">ListRepositoriesResponse</span>



| Field | Description |
| --- | --- |
| repositories | **[repeated Repository](#Repository)**<br/>The list of repositories. |
| next_page_token | **[ string](#string)**<br/>A token to retrieve next page of results. |

## <span id="animeshon.hub.v1alpha1.ReceivePackRequest">ReceivePackRequest</span>



| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the repository. |
| body | **[ google.api.HttpBody](#google.api.HttpBody)**<br/>The request content, represented as an HttpBody. |

## <span id="animeshon.hub.v1alpha1.Repository">Repository</span>



| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The repository resource name. |

## <span id="animeshon.hub.v1alpha1.UploadPackRequest">UploadPackRequest</span>



| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the repository. |
| body | **[ google.api.HttpBody](#google.api.HttpBody)**<br/>The request content, represented as an HttpBody. |
