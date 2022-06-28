# Protocol Documentation
<a name="top"></a>

## Table of Contents

- [animeshon/webpage/v1alpha1/archive.proto](#animeshon/webpage/v1alpha1/archive.proto)
    - [CreatePageRequest](#animeshon.webpage.v1alpha1.CreatePageRequest)
    - [DeletePageRequest](#animeshon.webpage.v1alpha1.DeletePageRequest)
    - [GetPageRequest](#animeshon.webpage.v1alpha1.GetPageRequest)
    - [ImportPageRequest](#animeshon.webpage.v1alpha1.ImportPageRequest)
    - [ImportPageRequest.WebCacheOptions](#animeshon.webpage.v1alpha1.ImportPageRequest.WebCacheOptions)
    - [ImportPageResponse](#animeshon.webpage.v1alpha1.ImportPageResponse)
    - [ImportPageResponse.ImportPageRemoteError](#animeshon.webpage.v1alpha1.ImportPageResponse.ImportPageRemoteError)
    - [ImportPageResponse.ImportPageResult](#animeshon.webpage.v1alpha1.ImportPageResponse.ImportPageResult)
    - [ListPagesRequest](#animeshon.webpage.v1alpha1.ListPagesRequest)
    - [ListPagesResponse](#animeshon.webpage.v1alpha1.ListPagesResponse)
    - [Page](#animeshon.webpage.v1alpha1.Page)
  
    - [Archive](#animeshon.webpage.v1alpha1.Archive)
  
- [Scalar Value Types](#scalar-value-types)



<a name="animeshon/webpage/v1alpha1/archive.proto"></a>
<p align="right"><a href="#top">Top</a></p>

## animeshon/webpage/v1alpha1/archive.proto



<a name="animeshon.webpage.v1alpha1.CreatePageRequest"></a>

### CreatePageRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| parent | [string](#string) |  | The parent this page belongs to. |
| page | [Page](#animeshon.webpage.v1alpha1.Page) |  | The page to create. |






<a name="animeshon.webpage.v1alpha1.DeletePageRequest"></a>

### DeletePageRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the page to delete. |






<a name="animeshon.webpage.v1alpha1.GetPageRequest"></a>

### GetPageRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the page to retrieve. |
| selector | [string](#string) |  | The html selector to use to return the page content. |






<a name="animeshon.webpage.v1alpha1.ImportPageRequest"></a>

### ImportPageRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the page to retrieve. |
| cache_options | [ImportPageRequest.WebCacheOptions](#animeshon.webpage.v1alpha1.ImportPageRequest.WebCacheOptions) |  | The web cache options to apply to the import request. |






<a name="animeshon.webpage.v1alpha1.ImportPageRequest.WebCacheOptions"></a>

### ImportPageRequest.WebCacheOptions
The WebCache options to be used when importing a page from a public site.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| refresh | [bool](#bool) |  | If refresh is set to true the page is imported from the remote address regardless of an existing local cache, if the fetched page does not match the existing cache the new page is stored and a new resource is created, otherwise the existing (cached) resource is returned. |
| ignore | [bool](#bool) |  | If ignore is set to true no cache lookup is performed and the page is imported into a new resource. If both &#34;ignore&#34; and &#34;refresh&#34; are set to true then &#34;refresh&#34; has no effect. |






<a name="animeshon.webpage.v1alpha1.ImportPageResponse"></a>

### ImportPageResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| result | [ImportPageResponse.ImportPageResult](#animeshon.webpage.v1alpha1.ImportPageResponse.ImportPageResult) |  | If the operation was successful this field will return the imported page. |
| error | [ImportPageResponse.ImportPageRemoteError](#animeshon.webpage.v1alpha1.ImportPageResponse.ImportPageRemoteError) |  | If the operation ended up in a failure due to an error with the remote server this field will provide more details about the failure. |
| cache_hit | [bool](#bool) |  | Whether this page was found in the cache. |






<a name="animeshon.webpage.v1alpha1.ImportPageResponse.ImportPageRemoteError"></a>

### ImportPageResponse.ImportPageRemoteError



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| status_code | [int32](#int32) |  | The status code returned from the remote server. |
| details | [string](#string) |  | The details related to the import failure. |






<a name="animeshon.webpage.v1alpha1.ImportPageResponse.ImportPageResult"></a>

### ImportPageResponse.ImportPageResult



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| page | [Page](#animeshon.webpage.v1alpha1.Page) |  | The successfully imported page. |






<a name="animeshon.webpage.v1alpha1.ListPagesRequest"></a>

### ListPagesRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| parent | [string](#string) |  | The parent this page belongs to. |
| page_size | [int32](#int32) |  | If unspecified, server will pick an appropriate default. |
| page_token | [string](#string) |  | The value returned from the previous call. |
| filter | [string](#string) |  | A filter to be applied to results. |






<a name="animeshon.webpage.v1alpha1.ListPagesResponse"></a>

### ListPagesResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| pages | [Page](#animeshon.webpage.v1alpha1.Page) | repeated | The list of pages. |
| next_page_token | [string](#string) |  | A token to retrieve next page of results. |






<a name="animeshon.webpage.v1alpha1.Page"></a>

### Page



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the page. |
| content | [string](#string) |  | The page content according to the html selector. |





 

 

 


<a name="animeshon.webpage.v1alpha1.Archive"></a>

### Archive


| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| GetPage | [GetPageRequest](#animeshon.webpage.v1alpha1.GetPageRequest) | [Page](#animeshon.webpage.v1alpha1.Page) |  |
| ListPages | [ListPagesRequest](#animeshon.webpage.v1alpha1.ListPagesRequest) | [ListPagesResponse](#animeshon.webpage.v1alpha1.ListPagesResponse) |  |
| ImportPage | [ImportPageRequest](#animeshon.webpage.v1alpha1.ImportPageRequest) | [ImportPageResponse](#animeshon.webpage.v1alpha1.ImportPageResponse) |  |
| CreatePage | [CreatePageRequest](#animeshon.webpage.v1alpha1.CreatePageRequest) | [Page](#animeshon.webpage.v1alpha1.Page) |  |
| DeletePage | [DeletePageRequest](#animeshon.webpage.v1alpha1.DeletePageRequest) | [.google.protobuf.Empty](#google.protobuf.Empty) |  |

 



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

