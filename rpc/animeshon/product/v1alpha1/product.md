# Protocol Documentation
<a name="top"></a>

## Table of Contents

- [animeshon/product/v1alpha1/chapter.proto](#animeshon/product/v1alpha1/chapter.proto)
    - [Chapter](#animeshon.product.v1alpha1.Chapter)
    - [CreateChapterRequest](#animeshon.product.v1alpha1.CreateChapterRequest)
    - [DeleteChapterRequest](#animeshon.product.v1alpha1.DeleteChapterRequest)
    - [GetChapterRequest](#animeshon.product.v1alpha1.GetChapterRequest)
    - [ListChaptersRequest](#animeshon.product.v1alpha1.ListChaptersRequest)
    - [ListChaptersResponse](#animeshon.product.v1alpha1.ListChaptersResponse)
    - [UpdateChapterRequest](#animeshon.product.v1alpha1.UpdateChapterRequest)
  
    - [ChapterService](#animeshon.product.v1alpha1.ChapterService)
  
- [Scalar Value Types](#scalar-value-types)



<a name="animeshon/product/v1alpha1/chapter.proto"></a>
<p align="right"><a href="#top">Top</a></p>

## animeshon/product/v1alpha1/chapter.proto



<a name="animeshon.product.v1alpha1.Chapter"></a>

### Chapter



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the chapter. |
| language_code | [string](#string) |  | The language code of the chapter pages. |
| album | [string](#string) |  | The album that contains all images associated to this chapter. |
| pages | [int64](#int64) | repeated | The ordered list of all pages represented as ids of images. |






<a name="animeshon.product.v1alpha1.CreateChapterRequest"></a>

### CreateChapterRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| parent | [string](#string) |  | The parent this chapter belongs to. |
| chapter | [Chapter](#animeshon.product.v1alpha1.Chapter) |  | The chapter to create. |






<a name="animeshon.product.v1alpha1.DeleteChapterRequest"></a>

### DeleteChapterRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the chapter to delete. |






<a name="animeshon.product.v1alpha1.GetChapterRequest"></a>

### GetChapterRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the chapter to retrieve. |






<a name="animeshon.product.v1alpha1.ListChaptersRequest"></a>

### ListChaptersRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| parent | [string](#string) |  | The parent this chapter belongs to. |
| page_size | [int32](#int32) |  | If unspecified, server will pick an appropriate default. |
| page_token | [string](#string) |  | The value returned from the previous call. |
| filter | [string](#string) |  | A filter to be applied to results. |






<a name="animeshon.product.v1alpha1.ListChaptersResponse"></a>

### ListChaptersResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| chapters | [Chapter](#animeshon.product.v1alpha1.Chapter) | repeated | The list of chapters. |
| next_page_token | [string](#string) |  | A token to retrieve next page of results. |






<a name="animeshon.product.v1alpha1.UpdateChapterRequest"></a>

### UpdateChapterRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| chapter | [Chapter](#animeshon.product.v1alpha1.Chapter) |  | The chapter to update. |
| update_mask | [google.protobuf.FieldMask](#google.protobuf.FieldMask) |  | The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |





 

 

 


<a name="animeshon.product.v1alpha1.ChapterService"></a>

### ChapterService


| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| GetChapter | [GetChapterRequest](#animeshon.product.v1alpha1.GetChapterRequest) | [Chapter](#animeshon.product.v1alpha1.Chapter) |  |
| ListChapters | [ListChaptersRequest](#animeshon.product.v1alpha1.ListChaptersRequest) | [ListChaptersResponse](#animeshon.product.v1alpha1.ListChaptersResponse) |  |
| CreateChapter | [CreateChapterRequest](#animeshon.product.v1alpha1.CreateChapterRequest) | [Chapter](#animeshon.product.v1alpha1.Chapter) |  |
| UpdateChapter | [UpdateChapterRequest](#animeshon.product.v1alpha1.UpdateChapterRequest) | [Chapter](#animeshon.product.v1alpha1.Chapter) |  |
| DeleteChapter | [DeleteChapterRequest](#animeshon.product.v1alpha1.DeleteChapterRequest) | [.google.protobuf.Empty](#google.protobuf.Empty) |  |

 



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

