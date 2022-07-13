# Package animeshon.webpage.v1alpha1

## Index
- [Archive](#animeshon.webpage.v1alpha1.Archive)
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

## Archive {#animeshon.webpage.v1alpha1.Archive}

| GetPage |
| --- |
| **rpc** GetPage([GetPageRequest](#animeshon.webpage.v1alpha1.GetPageRequest)) [Page](#animeshon.webpage.v1alpha1.Page)<br/> |

| ListPages |
| --- |
| **rpc** ListPages([ListPagesRequest](#animeshon.webpage.v1alpha1.ListPagesRequest)) [ListPagesResponse](#animeshon.webpage.v1alpha1.ListPagesResponse)<br/> |

| ImportPage |
| --- |
| **rpc** ImportPage([ImportPageRequest](#animeshon.webpage.v1alpha1.ImportPageRequest)) [ImportPageResponse](#animeshon.webpage.v1alpha1.ImportPageResponse)<br/> |

| CreatePage |
| --- |
| **rpc** CreatePage([CreatePageRequest](#animeshon.webpage.v1alpha1.CreatePageRequest)) [Page](#animeshon.webpage.v1alpha1.Page)<br/> |

| DeletePage |
| --- |
| **rpc** DeletePage([DeletePageRequest](#animeshon.webpage.v1alpha1.DeletePageRequest)) [.google.protobuf.Empty](#google.protobuf.Empty)<br/> |

## CreatePageRequest {#animeshon.webpage.v1alpha1.CreatePageRequest}

| Field | Description |
| --- | --- |
| parent | **[ string](#string)**<br/>The parent this page belongs to. |
| page | **[ Page](#Page)**<br/>The page to create. |
## DeletePageRequest {#animeshon.webpage.v1alpha1.DeletePageRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the page to delete. |
## GetPageRequest {#animeshon.webpage.v1alpha1.GetPageRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the page to retrieve. |
| selector | **[ string](#string)**<br/>The html selector to use to return the page content. |
## ImportPageRequest {#animeshon.webpage.v1alpha1.ImportPageRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the page to retrieve. |
| cache_options | **[ ImportPageRequest.WebCacheOptions](#ImportPageRequest.WebCacheOptions)**<br/>The web cache options to apply to the import request. |
## ImportPageRequest.WebCacheOptions {#animeshon.webpage.v1alpha1.ImportPageRequest.WebCacheOptions}
The WebCache options to be used when importing a page from a public site.
| Field | Description |
| --- | --- |
| refresh | **[ bool](#bool)**<br/>If refresh is set to true the page is imported from the remote address regardless of an existing local cache, if the fetched page does not match the existing cache the new page is stored and a new resource is created, otherwise the existing (cached) resource is returned. |
| ignore | **[ bool](#bool)**<br/>If ignore is set to true no cache lookup is performed and the page is imported into a new resource. If both "ignore" and "refresh" are set to true then "refresh" has no effect. |
## ImportPageResponse {#animeshon.webpage.v1alpha1.ImportPageResponse}

| Field | Description |
| --- | --- |
| **[oneof](https://developers.google.com/protocol-buffers/docs/proto3#oneof)** _response_<br />result | **[ ImportPageResponse.ImportPageResult](#ImportPageResponse.ImportPageResult)**<br/>If the operation was successful this field will return the imported page. |
| **[oneof](https://developers.google.com/protocol-buffers/docs/proto3#oneof)** _response_<br />error | **[ ImportPageResponse.ImportPageRemoteError](#ImportPageResponse.ImportPageRemoteError)**<br/>If the operation ended up in a failure due to an error with the remote server this field will provide more details about the failure. |
| cache_hit | **[ bool](#bool)**<br/>Whether this page was found in the cache. |
## ImportPageResponse.ImportPageRemoteError {#animeshon.webpage.v1alpha1.ImportPageResponse.ImportPageRemoteError}

| Field | Description |
| --- | --- |
| status_code | **[ int32](#int32)**<br/>The status code returned from the remote server. |
| details | **[ string](#string)**<br/>The details related to the import failure. |
## ImportPageResponse.ImportPageResult {#animeshon.webpage.v1alpha1.ImportPageResponse.ImportPageResult}

| Field | Description |
| --- | --- |
| page | **[ Page](#Page)**<br/>The successfully imported page. |
## ListPagesRequest {#animeshon.webpage.v1alpha1.ListPagesRequest}

| Field | Description |
| --- | --- |
| parent | **[ string](#string)**<br/>The parent this page belongs to. |
| page_size | **[ int32](#int32)**<br/>If unspecified, server will pick an appropriate default. |
| page_token | **[ string](#string)**<br/>The value returned from the previous call. |
| filter | **[ string](#string)**<br/>A filter to be applied to results. |
## ListPagesResponse {#animeshon.webpage.v1alpha1.ListPagesResponse}

| Field | Description |
| --- | --- |
| pages | **[repeated Page](#Page)**<br/>The list of pages. |
| next_page_token | **[ string](#string)**<br/>A token to retrieve next page of results. |
## Page {#animeshon.webpage.v1alpha1.Page}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the page. |
| content | **[ string](#string)**<br/>The page content according to the html selector. |
