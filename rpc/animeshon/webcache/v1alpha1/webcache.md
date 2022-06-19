# Protocol Documentation
<a name="top"></a>

## Table of Contents

- [animeshon/webcache/v1alpha1/webcache.proto](#animeshon/webcache/v1alpha1/webcache.proto)
    - [Cache](#animeshon.webcache.v1alpha1.Cache)
    - [CreateCacheRequest](#animeshon.webcache.v1alpha1.CreateCacheRequest)
    - [DeleteCacheRequest](#animeshon.webcache.v1alpha1.DeleteCacheRequest)
    - [GetCacheRequest](#animeshon.webcache.v1alpha1.GetCacheRequest)
    - [ListCachesRequest](#animeshon.webcache.v1alpha1.ListCachesRequest)
    - [ListCachesResponse](#animeshon.webcache.v1alpha1.ListCachesResponse)
  
    - [WebCache](#animeshon.webcache.v1alpha1.WebCache)
  
- [Scalar Value Types](#scalar-value-types)



<a name="animeshon/webcache/v1alpha1/webcache.proto"></a>
<p align="right"><a href="#top">Top</a></p>

## animeshon/webcache/v1alpha1/webcache.proto



<a name="animeshon.webcache.v1alpha1.Cache"></a>

### Cache
Cache contains meta information about a specific web resource.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the cache, idempotently generated from the scheme and uri. |
| scheme | [string](#string) |  | The original scheme indicating the protocol used for the original request. |
| uri | [string](#string) |  | The request uri stripped of the original scheme. |
| mime_type | [string](#string) |  | The response content type indicating the original media type. |
| status_code | [int32](#int32) |  | The response code indicating the status of the remote response. |
| redirect_uri | [string](#string) |  | The absolute redirect uri indicating any permanent or temporary redirect. |
| resource | [string](#string) |  | The full resource name of the cached resource. |
| revision_id | [string](#string) |  | The randomly generated revision identifier of this cache. The format is an 8-character hexadecimal string. |
| revision_create_time | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | The creation time indicating when this revision was created. |
| revision_expire_time | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | The expiration time indicating when this revision should no longer be considered valid. |






<a name="animeshon.webcache.v1alpha1.CreateCacheRequest"></a>

### CreateCacheRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| cache | [Cache](#animeshon.webcache.v1alpha1.Cache) |  | The cache to be created. |
| ttl | [google.protobuf.Duration](#google.protobuf.Duration) |  | The time-to-live indicating how long this cache should be considered valid. If set to zero, the cache will not have an expiration time. |






<a name="animeshon.webcache.v1alpha1.DeleteCacheRequest"></a>

### DeleteCacheRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the cache to delete. |






<a name="animeshon.webcache.v1alpha1.GetCacheRequest"></a>

### GetCacheRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The resource name of the requested cache. |






<a name="animeshon.webcache.v1alpha1.ListCachesRequest"></a>

### ListCachesRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| page_size | [int32](#int32) |  | If unspecified, server will pick an appropriate default. |
| page_token | [string](#string) |  | The value returned from the previous call. |
| filter | [string](#string) |  | A filter to be applied to results.

Currently accepted filters include: - uri:{absolute uri} - resource:{full resource name} |
| only_latest_revision | [bool](#bool) |  | Whether to return only the latest revision for each cache. |






<a name="animeshon.webcache.v1alpha1.ListCachesResponse"></a>

### ListCachesResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| caches | [Cache](#animeshon.webcache.v1alpha1.Cache) | repeated | The list of caches. |
| next_page_token | [string](#string) |  | A token to retrieve next page of results. |





 

 

 


<a name="animeshon.webcache.v1alpha1.WebCache"></a>

### WebCache


| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| CreateCache | [CreateCacheRequest](#animeshon.webcache.v1alpha1.CreateCacheRequest) | [Cache](#animeshon.webcache.v1alpha1.Cache) |  |
| ListCaches | [ListCachesRequest](#animeshon.webcache.v1alpha1.ListCachesRequest) | [ListCachesResponse](#animeshon.webcache.v1alpha1.ListCachesResponse) |  |
| GetCache | [GetCacheRequest](#animeshon.webcache.v1alpha1.GetCacheRequest) | [Cache](#animeshon.webcache.v1alpha1.Cache) | See https://google.aip.dev/162#referencing-revisions for more information. |
| DeleteCache | [DeleteCacheRequest](#animeshon.webcache.v1alpha1.DeleteCacheRequest) | [.google.protobuf.Empty](#google.protobuf.Empty) |  |

 



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

