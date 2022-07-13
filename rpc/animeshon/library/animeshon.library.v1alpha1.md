# Package animeshon.library.v1alpha1

## Index
- [Library](#animeshon.library.v1alpha1.Library)
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
## Library {#animeshon.library.v1alpha1.Library}

| GetPlaylist |
| --- |
| **rpc** GetPlaylist([GetPlaylistRequest](#animeshon.library.v1alpha1.GetPlaylistRequest)) [Playlist](#animeshon.library.v1alpha1.Playlist)<br/> |

| ListPlaylists |
| --- |
| **rpc** ListPlaylists([ListPlaylistsRequest](#animeshon.library.v1alpha1.ListPlaylistsRequest)) [ListPlaylistsResponse](#animeshon.library.v1alpha1.ListPlaylistsResponse)<br/> |

| CreatePlaylist |
| --- |
| **rpc** CreatePlaylist([CreatePlaylistRequest](#animeshon.library.v1alpha1.CreatePlaylistRequest)) [Playlist](#animeshon.library.v1alpha1.Playlist)<br/> |

| UpdatePlaylist |
| --- |
| **rpc** UpdatePlaylist([UpdatePlaylistRequest](#animeshon.library.v1alpha1.UpdatePlaylistRequest)) [Playlist](#animeshon.library.v1alpha1.Playlist)<br/> |

| DeletePlaylist |
| --- |
| **rpc** DeletePlaylist([DeletePlaylistRequest](#animeshon.library.v1alpha1.DeletePlaylistRequest)) [.google.protobuf.Empty](#google.protobuf.Empty)<br/> |

| ListPlaylistItems |
| --- |
| **rpc** ListPlaylistItems([ListPlaylistItemsRequest](#animeshon.library.v1alpha1.ListPlaylistItemsRequest)) [ListPlaylistItemsResponse](#animeshon.library.v1alpha1.ListPlaylistItemsResponse)<br/> |

| CreatePlaylistItem |
| --- |
| **rpc** CreatePlaylistItem([CreatePlaylistItemRequest](#animeshon.library.v1alpha1.CreatePlaylistItemRequest)) [PlaylistItem](#animeshon.library.v1alpha1.PlaylistItem)<br/> |

| BatchCreatePlaylistItems |
| --- |
| **rpc** BatchCreatePlaylistItems([BatchCreatePlaylistItemsRequest](#animeshon.library.v1alpha1.BatchCreatePlaylistItemsRequest)) [BatchCreatePlaylistItemsResponse](#animeshon.library.v1alpha1.BatchCreatePlaylistItemsResponse)<br/> |

| DeletePlaylistItem |
| --- |
| **rpc** DeletePlaylistItem([DeletePlaylistItemRequest](#animeshon.library.v1alpha1.DeletePlaylistItemRequest)) [.google.protobuf.Empty](#google.protobuf.Empty)<br/> |

## Audience {#animeshon.library.v1alpha1.Audience}
TODO: this is represented as a group in authorization.
TODO: who should be the owner of an audience? the user who created it?
| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The id of the audience. |
| members | **[repeated string](#string)**<br/>The members of this audience. |
## BatchCreatePlaylistItemsRequest {#animeshon.library.v1alpha1.BatchCreatePlaylistItemsRequest}

| Field | Description |
| --- | --- |
| parent | **[ string](#string)**<br/>The parent this playlist item belongs to. |
| item | **[repeated PlaylistItem](#PlaylistItem)**<br/>The playlist items to create. |
## BatchCreatePlaylistItemsResponse {#animeshon.library.v1alpha1.BatchCreatePlaylistItemsResponse}

| Field | Description |
| --- | --- |
| items | **[repeated PlaylistItem](#PlaylistItem)**<br/>The list of items added to the playlist |
## CreatePlaylistItemRequest {#animeshon.library.v1alpha1.CreatePlaylistItemRequest}

| Field | Description |
| --- | --- |
| parent | **[ string](#string)**<br/>The parent this playlist item belongs to. |
| item | **[ PlaylistItem](#PlaylistItem)**<br/>The playlist item to create. |
## CreatePlaylistRequest {#animeshon.library.v1alpha1.CreatePlaylistRequest}

| Field | Description |
| --- | --- |
| parent | **[ string](#string)**<br/>The parent this playlist belongs to. |
| playlist | **[ Playlist](#Playlist)**<br/>The playlist to create. |
## DeletePlaylistItemRequest {#animeshon.library.v1alpha1.DeletePlaylistItemRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the playlist item to delete. |
## DeletePlaylistRequest {#animeshon.library.v1alpha1.DeletePlaylistRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the playlist to delete. |
## GetPlaylistRequest {#animeshon.library.v1alpha1.GetPlaylistRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the playlist to retrieve. |
## ListPlaylistItemsRequest {#animeshon.library.v1alpha1.ListPlaylistItemsRequest}

| Field | Description |
| --- | --- |
| parent | **[ string](#string)**<br/>The playlist this item belongs to. |
| page_size | **[ int32](#int32)**<br/>If unspecified, server will pick an appropriate default. |
| page_token | **[ string](#string)**<br/>The value returned from the previous call. |
| filter | **[ string](#string)**<br/>A filter to be applied to results. |
## ListPlaylistItemsResponse {#animeshon.library.v1alpha1.ListPlaylistItemsResponse}

| Field | Description |
| --- | --- |
| items | **[repeated PlaylistItem](#PlaylistItem)**<br/>The list of playlist items. |
| next_page_token | **[ string](#string)**<br/>A token to retrieve next page of results. |
| total_size | **[ int32](#int32)**<br/>The total number of items available in this playlist. |
## ListPlaylistsRequest {#animeshon.library.v1alpha1.ListPlaylistsRequest}

| Field | Description |
| --- | --- |
| parent | **[ string](#string)**<br/>The user this playlist belongs to. |
| page_size | **[ int32](#int32)**<br/>If unspecified, server will pick an appropriate default. |
| page_token | **[ string](#string)**<br/>The value returned from the previous call. |
| filter | **[ string](#string)**<br/>A filter to be applied to results. |
## ListPlaylistsResponse {#animeshon.library.v1alpha1.ListPlaylistsResponse}

| Field | Description |
| --- | --- |
| playlists | **[repeated Playlist](#Playlist)**<br/>The list of playlists. |
| next_page_token | **[ string](#string)**<br/>A token to retrieve next page of results. |
## Playlist {#animeshon.library.v1alpha1.Playlist}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The id of the playlist. |
| display_name | **[ string](#string)**<br/>The display name of the playlist. |
| type | **[ Type](#Type)**<br/>The type of the playlist. |
## PlaylistItem {#animeshon.library.v1alpha1.PlaylistItem}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The id of the playlist. |
| resource | **[ string](#string)**<br/>The full resource name that identifies the resource. |
| create_time | **[ google.protobuf.Timestamp](#google.protobuf.Timestamp)**<br/>The timestamp at which the playlist item was created. |
## UpdatePlaylistRequest {#animeshon.library.v1alpha1.UpdatePlaylistRequest}

| Field | Description |
| --- | --- |
| playlist | **[ Playlist](#Playlist)**<br/>The playlist to update. |
| update_mask | **[ google.protobuf.FieldMask](#google.protobuf.FieldMask)**<br/>The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |

## Type {#animeshon.library.v1alpha1.Type}


| Name | Description |
| --- | --- |
| TYPE_UNSPECIFIED | No description. |
| LATER | The playlist holds items intended to be consumed at a later date |
| LIKED | The playlist holds liked items |
| CUSTOM | The playlist is custom made by the user |
