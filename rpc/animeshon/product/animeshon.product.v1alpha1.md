# Package animeshon.product.v1alpha1

## Index
- [ChapterService](#animeshon.product.v1alpha1.ChapterService)
- [Chapter](#animeshon.product.v1alpha1.Chapter)
- [CreateChapterRequest](#animeshon.product.v1alpha1.CreateChapterRequest)
- [DeleteChapterRequest](#animeshon.product.v1alpha1.DeleteChapterRequest)
- [GetChapterRequest](#animeshon.product.v1alpha1.GetChapterRequest)
- [ListChaptersRequest](#animeshon.product.v1alpha1.ListChaptersRequest)
- [ListChaptersResponse](#animeshon.product.v1alpha1.ListChaptersResponse)
- [UpdateChapterRequest](#animeshon.product.v1alpha1.UpdateChapterRequest)

## ChapterService {#animeshon.product.v1alpha1.ChapterService}

| GetChapter |
| --- |
| **rpc** GetChapter([GetChapterRequest](#animeshon.product.v1alpha1.GetChapterRequest)) [Chapter](#animeshon.product.v1alpha1.Chapter)<br/> |

| ListChapters |
| --- |
| **rpc** ListChapters([ListChaptersRequest](#animeshon.product.v1alpha1.ListChaptersRequest)) [ListChaptersResponse](#animeshon.product.v1alpha1.ListChaptersResponse)<br/> |

| CreateChapter |
| --- |
| **rpc** CreateChapter([CreateChapterRequest](#animeshon.product.v1alpha1.CreateChapterRequest)) [Chapter](#animeshon.product.v1alpha1.Chapter)<br/> |

| UpdateChapter |
| --- |
| **rpc** UpdateChapter([UpdateChapterRequest](#animeshon.product.v1alpha1.UpdateChapterRequest)) [Chapter](#animeshon.product.v1alpha1.Chapter)<br/> |

| DeleteChapter |
| --- |
| **rpc** DeleteChapter([DeleteChapterRequest](#animeshon.product.v1alpha1.DeleteChapterRequest)) [.google.protobuf.Empty](#google.protobuf.Empty)<br/> |

## Chapter {#animeshon.product.v1alpha1.Chapter}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the chapter. |
| language_code | **[ string](#string)**<br/>The language code of the chapter pages. |
| album | **[ string](#string)**<br/>The album that contains all images associated to this chapter. |
| pages | **[repeated int64](#int64)**<br/>The ordered list of all pages represented as ids of images. |
## CreateChapterRequest {#animeshon.product.v1alpha1.CreateChapterRequest}

| Field | Description |
| --- | --- |
| parent | **[ string](#string)**<br/>The parent this chapter belongs to. |
| chapter | **[ Chapter](#Chapter)**<br/>The chapter to create. |
## DeleteChapterRequest {#animeshon.product.v1alpha1.DeleteChapterRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the chapter to delete. |
## GetChapterRequest {#animeshon.product.v1alpha1.GetChapterRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the chapter to retrieve. |
## ListChaptersRequest {#animeshon.product.v1alpha1.ListChaptersRequest}

| Field | Description |
| --- | --- |
| parent | **[ string](#string)**<br/>The parent this chapter belongs to. |
| page_size | **[ int32](#int32)**<br/>If unspecified, server will pick an appropriate default. |
| page_token | **[ string](#string)**<br/>The value returned from the previous call. |
| filter | **[ string](#string)**<br/>A filter to be applied to results. |
## ListChaptersResponse {#animeshon.product.v1alpha1.ListChaptersResponse}

| Field | Description |
| --- | --- |
| chapters | **[repeated Chapter](#Chapter)**<br/>The list of chapters. |
| next_page_token | **[ string](#string)**<br/>A token to retrieve next page of results. |
## UpdateChapterRequest {#animeshon.product.v1alpha1.UpdateChapterRequest}

| Field | Description |
| --- | --- |
| chapter | **[ Chapter](#Chapter)**<br/>The chapter to update. |
| update_mask | **[ google.protobuf.FieldMask](#google.protobuf.FieldMask)**<br/>The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |
