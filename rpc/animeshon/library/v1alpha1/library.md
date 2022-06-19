# Protocol Documentation
<a name="top"></a>

## Table of Contents

- [animeshon/library/v1alpha1/library.proto](#animeshon/library/v1alpha1/library.proto)
    - [Audience](#animeshon.library.v1alpha1.Audience)
    - [BatchCreatePlaylistItemsRequest](#animeshon.library.v1alpha1.BatchCreatePlaylistItemsRequest)
    - [BatchCreatePlaylistItemsResponse](#animeshon.library.v1alpha1.BatchCreatePlaylistItemsResponse)
    - [CreatePlaylistItemRequest](#animeshon.library.v1alpha1.CreatePlaylistItemRequest)
    - [CreatePlaylistRequest](#animeshon.library.v1alpha1.CreatePlaylistRequest)
    - [DeletePlaylistItemRequest](#animeshon.library.v1alpha1.DeletePlaylistItemRequest)
    - [DeletePlaylistRequest](#animeshon.library.v1alpha1.DeletePlaylistRequest)
    - [GetPlaylistRequest](#animeshon.library.v1alpha1.GetPlaylistRequest)
    - [ListPlaylistItemsRequest](#animeshon.library.v1alpha1.ListPlaylistItemsRequest)
    - [ListPlaylistItemsResponse](#animeshon.library.v1alpha1.ListPlaylistItemsResponse)
    - [ListPlaylistsRequest](#animeshon.library.v1alpha1.ListPlaylistsRequest)
    - [ListPlaylistsResponse](#animeshon.library.v1alpha1.ListPlaylistsResponse)
    - [Playlist](#animeshon.library.v1alpha1.Playlist)
    - [PlaylistItem](#animeshon.library.v1alpha1.PlaylistItem)
    - [UpdatePlaylistRequest](#animeshon.library.v1alpha1.UpdatePlaylistRequest)
  
    - [Type](#animeshon.library.v1alpha1.Type)
  
    - [Library](#animeshon.library.v1alpha1.Library)
  
- [Scalar Value Types](#scalar-value-types)



<a name="animeshon/library/v1alpha1/library.proto"></a>
<p align="right"><a href="#top">Top</a></p>

## animeshon/library/v1alpha1/library.proto



<a name="animeshon.library.v1alpha1.Audience"></a>

### Audience
TODO: this is represented as a group in authorization.
TODO: who should be the owner of an audience? the user who created it?


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The id of the audience. |
| members | [string](#string) | repeated | The members of this audience. |






<a name="animeshon.library.v1alpha1.BatchCreatePlaylistItemsRequest"></a>

### BatchCreatePlaylistItemsRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| parent | [string](#string) |  | The parent this playlist item belongs to. |
| item | [PlaylistItem](#animeshon.library.v1alpha1.PlaylistItem) | repeated | The playlist items to create. |






<a name="animeshon.library.v1alpha1.BatchCreatePlaylistItemsResponse"></a>

### BatchCreatePlaylistItemsResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| items | [PlaylistItem](#animeshon.library.v1alpha1.PlaylistItem) | repeated | The list of items added to the playlist |






<a name="animeshon.library.v1alpha1.CreatePlaylistItemRequest"></a>

### CreatePlaylistItemRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| parent | [string](#string) |  | The parent this playlist item belongs to. |
| item | [PlaylistItem](#animeshon.library.v1alpha1.PlaylistItem) |  | The playlist item to create. |






<a name="animeshon.library.v1alpha1.CreatePlaylistRequest"></a>

### CreatePlaylistRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| parent | [string](#string) |  | The parent this playlist belongs to. |
| playlist | [Playlist](#animeshon.library.v1alpha1.Playlist) |  | The playlist to create. |






<a name="animeshon.library.v1alpha1.DeletePlaylistItemRequest"></a>

### DeletePlaylistItemRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the playlist item to delete. |






<a name="animeshon.library.v1alpha1.DeletePlaylistRequest"></a>

### DeletePlaylistRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the playlist to delete. |






<a name="animeshon.library.v1alpha1.GetPlaylistRequest"></a>

### GetPlaylistRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the playlist to retrieve. |






<a name="animeshon.library.v1alpha1.ListPlaylistItemsRequest"></a>

### ListPlaylistItemsRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| parent | [string](#string) |  | The playlist this item belongs to. |
| page_size | [int32](#int32) |  | If unspecified, server will pick an appropriate default. |
| page_token | [string](#string) |  | The value returned from the previous call. |
| filter | [string](#string) |  | A filter to be applied to results. |






<a name="animeshon.library.v1alpha1.ListPlaylistItemsResponse"></a>

### ListPlaylistItemsResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| items | [PlaylistItem](#animeshon.library.v1alpha1.PlaylistItem) | repeated | The list of playlist items. |
| next_page_token | [string](#string) |  | A token to retrieve next page of results. |
| total_size | [int32](#int32) |  | The total number of items available in this playlist. |






<a name="animeshon.library.v1alpha1.ListPlaylistsRequest"></a>

### ListPlaylistsRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| parent | [string](#string) |  | The user this playlist belongs to. |
| page_size | [int32](#int32) |  | If unspecified, server will pick an appropriate default. |
| page_token | [string](#string) |  | The value returned from the previous call. |
| filter | [string](#string) |  | A filter to be applied to results. |






<a name="animeshon.library.v1alpha1.ListPlaylistsResponse"></a>

### ListPlaylistsResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| playlists | [Playlist](#animeshon.library.v1alpha1.Playlist) | repeated | The list of playlists. |
| next_page_token | [string](#string) |  | A token to retrieve next page of results. |






<a name="animeshon.library.v1alpha1.Playlist"></a>

### Playlist



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The id of the playlist. |
| display_name | [string](#string) |  | The display name of the playlist. |
| type | [Type](#animeshon.library.v1alpha1.Type) |  | The type of the playlist. |






<a name="animeshon.library.v1alpha1.PlaylistItem"></a>

### PlaylistItem



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The id of the playlist. |
| resource | [string](#string) |  | The full resource name that identifies the resource. |
| create_time | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | The timestamp at which the playlist item was created. |






<a name="animeshon.library.v1alpha1.UpdatePlaylistRequest"></a>

### UpdatePlaylistRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| playlist | [Playlist](#animeshon.library.v1alpha1.Playlist) |  | The playlist to update. |
| update_mask | [google.protobuf.FieldMask](#google.protobuf.FieldMask) |  | The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |





 


<a name="animeshon.library.v1alpha1.Type"></a>

### Type


| Name | Number | Description |
| ---- | ------ | ----------- |
| TYPE_UNSPECIFIED | 0 |  |
| LATER | 1 | The playlist holds items intended to be consumed at a later date |
| LIKED | 2 | The playlist holds liked items |
| CUSTOM | 3 | The playlist is custom made by the user |


 

 


<a name="animeshon.library.v1alpha1.Library"></a>

### Library


| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| GetPlaylist | [GetPlaylistRequest](#animeshon.library.v1alpha1.GetPlaylistRequest) | [Playlist](#animeshon.library.v1alpha1.Playlist) |  |
| ListPlaylists | [ListPlaylistsRequest](#animeshon.library.v1alpha1.ListPlaylistsRequest) | [ListPlaylistsResponse](#animeshon.library.v1alpha1.ListPlaylistsResponse) |  |
| CreatePlaylist | [CreatePlaylistRequest](#animeshon.library.v1alpha1.CreatePlaylistRequest) | [Playlist](#animeshon.library.v1alpha1.Playlist) |  |
| UpdatePlaylist | [UpdatePlaylistRequest](#animeshon.library.v1alpha1.UpdatePlaylistRequest) | [Playlist](#animeshon.library.v1alpha1.Playlist) |  |
| DeletePlaylist | [DeletePlaylistRequest](#animeshon.library.v1alpha1.DeletePlaylistRequest) | [.google.protobuf.Empty](#google.protobuf.Empty) |  |
| ListPlaylistItems | [ListPlaylistItemsRequest](#animeshon.library.v1alpha1.ListPlaylistItemsRequest) | [ListPlaylistItemsResponse](#animeshon.library.v1alpha1.ListPlaylistItemsResponse) |  |
| CreatePlaylistItem | [CreatePlaylistItemRequest](#animeshon.library.v1alpha1.CreatePlaylistItemRequest) | [PlaylistItem](#animeshon.library.v1alpha1.PlaylistItem) |  |
| BatchCreatePlaylistItems | [BatchCreatePlaylistItemsRequest](#animeshon.library.v1alpha1.BatchCreatePlaylistItemsRequest) | [BatchCreatePlaylistItemsResponse](#animeshon.library.v1alpha1.BatchCreatePlaylistItemsResponse) |  |
| DeletePlaylistItem | [DeletePlaylistItemRequest](#animeshon.library.v1alpha1.DeletePlaylistItemRequest) | [.google.protobuf.Empty](#google.protobuf.Empty) |  |

 



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

