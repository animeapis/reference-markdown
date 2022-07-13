# Package animeshon.webcache.v1alpha1

## Index
- [WebCache](#animeshon.webcache.v1alpha1.WebCache)
- [Cache](#animeshon.webcache.v1alpha1.Cache)
- [CreateCacheRequest](#animeshon.webcache.v1alpha1.CreateCacheRequest)
- [DeleteCacheRequest](#animeshon.webcache.v1alpha1.DeleteCacheRequest)
- [GetCacheRequest](#animeshon.webcache.v1alpha1.GetCacheRequest)
- [ListCachesRequest](#animeshon.webcache.v1alpha1.ListCachesRequest)
- [ListCachesResponse](#animeshon.webcache.v1alpha1.ListCachesResponse)

## WebCache {#animeshon.webcache.v1alpha1.WebCache}

| CreateCache |
| --- |
| **rpc** CreateCache([CreateCacheRequest](#animeshon.webcache.v1alpha1.CreateCacheRequest)) [Cache](#animeshon.webcache.v1alpha1.Cache)<br/> |

| ListCaches |
| --- |
| **rpc** ListCaches([ListCachesRequest](#animeshon.webcache.v1alpha1.ListCachesRequest)) [ListCachesResponse](#animeshon.webcache.v1alpha1.ListCachesResponse)<br/> |

| GetCache |
| --- |
| **rpc** GetCache([GetCacheRequest](#animeshon.webcache.v1alpha1.GetCacheRequest)) [Cache](#animeshon.webcache.v1alpha1.Cache)<br/>See https://google.aip.dev/162#referencing-revisions for more information. |

| DeleteCache |
| --- |
| **rpc** DeleteCache([DeleteCacheRequest](#animeshon.webcache.v1alpha1.DeleteCacheRequest)) [.google.protobuf.Empty](#google.protobuf.Empty)<br/> |

## Cache {#animeshon.webcache.v1alpha1.Cache}
Cache contains meta information about a specific web resource.
| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the cache, idempotently generated from the scheme and uri. |
| scheme | **[ string](#string)**<br/>The original scheme indicating the protocol used for the original request. |
| uri | **[ string](#string)**<br/>The request uri stripped of the original scheme. |
| mime_type | **[ string](#string)**<br/>The response content type indicating the original media type. |
| status_code | **[ int32](#int32)**<br/>The response code indicating the status of the remote response. |
| redirect_uri | **[ string](#string)**<br/>The absolute redirect uri indicating any permanent or temporary redirect. |
| resource | **[ string](#string)**<br/>The full resource name of the cached resource. |
| revision_id | **[ string](#string)**<br/>The randomly generated revision identifier of this cache. The format is an 8-character hexadecimal string. |
| revision_create_time | **[ google.protobuf.Timestamp](#google.protobuf.Timestamp)**<br/>The creation time indicating when this revision was created. |
| revision_expire_time | **[ google.protobuf.Timestamp](#google.protobuf.Timestamp)**<br/>The expiration time indicating when this revision should no longer be considered valid. |
## CreateCacheRequest {#animeshon.webcache.v1alpha1.CreateCacheRequest}

| Field | Description |
| --- | --- |
| cache | **[ Cache](#Cache)**<br/>The cache to be created. |
| ttl | **[ google.protobuf.Duration](#google.protobuf.Duration)**<br/>The time-to-live indicating how long this cache should be considered valid. If set to zero, the cache will not have an expiration time. |
## DeleteCacheRequest {#animeshon.webcache.v1alpha1.DeleteCacheRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the cache to delete. |
## GetCacheRequest {#animeshon.webcache.v1alpha1.GetCacheRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the requested cache. |
## ListCachesRequest {#animeshon.webcache.v1alpha1.ListCachesRequest}

| Field | Description |
| --- | --- |
| page_size | **[ int32](#int32)**<br/>If unspecified, server will pick an appropriate default. |
| page_token | **[ string](#string)**<br/>The value returned from the previous call. |
| filter | **[ string](#string)**<br/>A filter to be applied to results.

Currently accepted filters include: - uri:{absolute uri} - resource:{full resource name} |
| only_latest_revision | **[ bool](#bool)**<br/>Whether to return only the latest revision for each cache. |
## ListCachesResponse {#animeshon.webcache.v1alpha1.ListCachesResponse}

| Field | Description |
| --- | --- |
| caches | **[repeated Cache](#Cache)**<br/>The list of caches. |
| next_page_token | **[ string](#string)**<br/>A token to retrieve next page of results. |
