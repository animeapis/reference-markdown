# Protocol Documentation
<a name="top"></a>

## Table of Contents

- [animeshon/release/v1alpha1/release.proto](#animeshon/release/v1alpha1/release.proto)
    - [CancelReleaseRequest](#animeshon.release.v1alpha1.CancelReleaseRequest)
    - [CancelReleaseResponse](#animeshon.release.v1alpha1.CancelReleaseResponse)
    - [CreateReleaseRequest](#animeshon.release.v1alpha1.CreateReleaseRequest)
    - [DeleteReleaseRequest](#animeshon.release.v1alpha1.DeleteReleaseRequest)
    - [GetReleaseRequest](#animeshon.release.v1alpha1.GetReleaseRequest)
    - [ListReleasesRequest](#animeshon.release.v1alpha1.ListReleasesRequest)
    - [ListReleasesResponse](#animeshon.release.v1alpha1.ListReleasesResponse)
    - [PublishReleaseRequest](#animeshon.release.v1alpha1.PublishReleaseRequest)
    - [PublishReleaseResponse](#animeshon.release.v1alpha1.PublishReleaseResponse)
    - [Release](#animeshon.release.v1alpha1.Release)
    - [Release.LabelsEntry](#animeshon.release.v1alpha1.Release.LabelsEntry)
    - [ReleaseStrategy](#animeshon.release.v1alpha1.ReleaseStrategy)
    - [ScheduleReleaseRequest](#animeshon.release.v1alpha1.ScheduleReleaseRequest)
    - [ScheduleReleaseResponse](#animeshon.release.v1alpha1.ScheduleReleaseResponse)
    - [SuspendReleaseRequest](#animeshon.release.v1alpha1.SuspendReleaseRequest)
    - [SuspendReleaseResponse](#animeshon.release.v1alpha1.SuspendReleaseResponse)
    - [UndeleteReleaseRequest](#animeshon.release.v1alpha1.UndeleteReleaseRequest)
    - [UnpublishReleaseRequest](#animeshon.release.v1alpha1.UnpublishReleaseRequest)
    - [UnpublishReleaseResponse](#animeshon.release.v1alpha1.UnpublishReleaseResponse)
    - [UpdateReleaseRequest](#animeshon.release.v1alpha1.UpdateReleaseRequest)
  
    - [Release.State](#animeshon.release.v1alpha1.Release.State)
    - [Visibility](#animeshon.release.v1alpha1.Visibility)
  
    - [Publisher](#animeshon.release.v1alpha1.Publisher)
  
- [Scalar Value Types](#scalar-value-types)



<a name="animeshon/release/v1alpha1/release.proto"></a>
<p align="right"><a href="#top">Top</a></p>

## animeshon/release/v1alpha1/release.proto



<a name="animeshon.release.v1alpha1.CancelReleaseRequest"></a>

### CancelReleaseRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the release to cancel. |






<a name="animeshon.release.v1alpha1.CancelReleaseResponse"></a>

### CancelReleaseResponse







<a name="animeshon.release.v1alpha1.CreateReleaseRequest"></a>

### CreateReleaseRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| parent | [string](#string) |  | The parent this release belongs to. |
| release | [Release](#animeshon.release.v1alpha1.Release) |  | The release to create. |
| ttl | [google.protobuf.Duration](#google.protobuf.Duration) |  | The time-to-live indicating for how long this release should be published. If set to zero, the release will not have an expiration time. |






<a name="animeshon.release.v1alpha1.DeleteReleaseRequest"></a>

### DeleteReleaseRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the release to delete. |






<a name="animeshon.release.v1alpha1.GetReleaseRequest"></a>

### GetReleaseRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the release to retrieve. |






<a name="animeshon.release.v1alpha1.ListReleasesRequest"></a>

### ListReleasesRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| parent | [string](#string) |  | The parent to list releases from. |
| page_size | [int32](#int32) |  | If unspecified, server will pick an appropriate default. |
| page_token | [string](#string) |  | The value returned from the previous call. |
| filter | [string](#string) |  | A filter to be applied to results. |






<a name="animeshon.release.v1alpha1.ListReleasesResponse"></a>

### ListReleasesResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| releases | [Release](#animeshon.release.v1alpha1.Release) | repeated | The list of releases. |
| next_page_token | [string](#string) |  | A token to retrieve next page of results. |






<a name="animeshon.release.v1alpha1.PublishReleaseRequest"></a>

### PublishReleaseRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the release to publish. |
| strategy | [ReleaseStrategy](#animeshon.release.v1alpha1.ReleaseStrategy) |  | The release strategy to use. |






<a name="animeshon.release.v1alpha1.PublishReleaseResponse"></a>

### PublishReleaseResponse







<a name="animeshon.release.v1alpha1.Release"></a>

### Release



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The release resource name. |
| display_name | [string](#string) |  | The human-readable display name of the release. |
| description | [string](#string) |  | The short description of the release. |
| authoritative_release | [string](#string) |  | The authoritative release is set only for sub-licensed releases that do not hold any publishing rights on the content being distributed.

A common case where the release is to be considered non-authoritative is a translation released by third-parties. In such scenario the original author(s) is to be considered the only publishing authority over the content.

If for any reason the authoritative release were to be unpublished or deleted from Animeshon all associated non-authoritative releases will be automatically hidden from public consumption and marked as suspended.

Furthermore, there can only be one authoritative release per resource, which means that you can have unlimited non-authoritative releases for one resource but it must have exactly one authoritative release. |
| resource | [string](#string) |  | The resource being released. |
| asset | [string](#string) |  | The product included in the release. |
| access_group | [string](#string) |  | The group of users authorized to access the asset. |
| visibility | [Visibility](#animeshon.release.v1alpha1.Visibility) |  | The visibility of the resources included in the asset. |
| state | [Release.State](#animeshon.release.v1alpha1.Release.State) |  | The current release state. |
| labels | [Release.LabelsEntry](#animeshon.release.v1alpha1.Release.LabelsEntry) | repeated | The map of labels associated with the release. |
| create_time | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | The timestamp at which the release was created. |
| update_time | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | The latest timestamp at which the release was updated. |
| expire_time | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | The timestamp at which the release will expire. |
| delete_time | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | The timestamp at which the release was deleted. |






<a name="animeshon.release.v1alpha1.Release.LabelsEntry"></a>

### Release.LabelsEntry



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| key | [string](#string) |  |  |
| value | [string](#string) |  |  |






<a name="animeshon.release.v1alpha1.ReleaseStrategy"></a>

### ReleaseStrategy
The release strategy describes how a release should be published.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| membership_only | [bool](#bool) |  | Whether the release should be available only to the members of a group. |






<a name="animeshon.release.v1alpha1.ScheduleReleaseRequest"></a>

### ScheduleReleaseRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the release to schedule. |
| strategy | [ReleaseStrategy](#animeshon.release.v1alpha1.ReleaseStrategy) |  | The release strategy to use. |






<a name="animeshon.release.v1alpha1.ScheduleReleaseResponse"></a>

### ScheduleReleaseResponse







<a name="animeshon.release.v1alpha1.SuspendReleaseRequest"></a>

### SuspendReleaseRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the release to suspend. |
| reason | [string](#string) |  | The reason why the release has been suspended. |






<a name="animeshon.release.v1alpha1.SuspendReleaseResponse"></a>

### SuspendReleaseResponse







<a name="animeshon.release.v1alpha1.UndeleteReleaseRequest"></a>

### UndeleteReleaseRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the release to undelete. |






<a name="animeshon.release.v1alpha1.UnpublishReleaseRequest"></a>

### UnpublishReleaseRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the release to publish. |






<a name="animeshon.release.v1alpha1.UnpublishReleaseResponse"></a>

### UnpublishReleaseResponse







<a name="animeshon.release.v1alpha1.UpdateReleaseRequest"></a>

### UpdateReleaseRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| release | [Release](#animeshon.release.v1alpha1.Release) |  | The release to update. |
| update_mask | [google.protobuf.FieldMask](#google.protobuf.FieldMask) |  | The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |





 


<a name="animeshon.release.v1alpha1.Release.State"></a>

### Release.State


| Name | Number | Description |
| ---- | ------ | ----------- |
| STATE_UNSPECIFIED | 0 | The default value. This value is used if the state is omitted. |
| ACTIVE | 1 | The release has been published and is available to the general public. |
| SCHEDULED | 2 | The release has been scheduled and will be made automatically available to the public according to the scheduling conditions. |
| DRAFT | 3 | The release is a draft and is still being worked on. |
| SUSPENDED | 4 | The release has been suspended. This state might automatically being set for non-authoritative releases when their authoritative release is also suspended, unpublished, or deleted. This state might also be set when a release is breaching general terms and conditions or is in conflict with community guidelines or internal governing policies. |
| DELETED | 5 | The release has been marked for deletion. |



<a name="animeshon.release.v1alpha1.Visibility"></a>

### Visibility


| Name | Number | Description |
| ---- | ------ | ----------- |
| VISIBILITY_UNSPECIFIED | 0 | The default value. This value is used if the state is omitted. |
| PRIVATE | 1 | The release is private and can only be accessed by users and service accounts that have been granted direct access to the release resource via explicit or inherited IAM policies. |
| MEMBERSHIP | 2 | The release has been published and access to its assets is limited to members that have paid the membership fee (e.g. a user who has bought the release). |
| PUBLIC | 3 | The release has been published and all of its assets are publicly available to all users. |


 

 


<a name="animeshon.release.v1alpha1.Publisher"></a>

### Publisher


| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| GetRelease | [GetReleaseRequest](#animeshon.release.v1alpha1.GetReleaseRequest) | [Release](#animeshon.release.v1alpha1.Release) |  |
| ListReleases | [ListReleasesRequest](#animeshon.release.v1alpha1.ListReleasesRequest) | [ListReleasesResponse](#animeshon.release.v1alpha1.ListReleasesResponse) |  |
| CreateRelease | [CreateReleaseRequest](#animeshon.release.v1alpha1.CreateReleaseRequest) | [Release](#animeshon.release.v1alpha1.Release) |  |
| UpdateRelease | [UpdateReleaseRequest](#animeshon.release.v1alpha1.UpdateReleaseRequest) | [Release](#animeshon.release.v1alpha1.Release) |  |
| DeleteRelease | [DeleteReleaseRequest](#animeshon.release.v1alpha1.DeleteReleaseRequest) | [.google.protobuf.Empty](#google.protobuf.Empty) | The release is soft-deleted and a grace period is granted before complete deletion. During this grace period the release can be recovered. |
| UndeleteRelease | [UndeleteReleaseRequest](#animeshon.release.v1alpha1.UndeleteReleaseRequest) | [Release](#animeshon.release.v1alpha1.Release) | This method allows to recover a release while still in the grace period. |
| PublishRelease | [PublishReleaseRequest](#animeshon.release.v1alpha1.PublishReleaseRequest) | [PublishReleaseResponse](#animeshon.release.v1alpha1.PublishReleaseResponse) | The release is marked as immediately available to the public. |
| UnpublishRelease | [UnpublishReleaseRequest](#animeshon.release.v1alpha1.UnpublishReleaseRequest) | [UnpublishReleaseResponse](#animeshon.release.v1alpha1.UnpublishReleaseResponse) | The release is unpublished and marked as a draft, associated non-authoritative will automatically be marked as suspended and hidden from the general public. |
| ScheduleRelease | [ScheduleReleaseRequest](#animeshon.release.v1alpha1.ScheduleReleaseRequest) | [ScheduleReleaseResponse](#animeshon.release.v1alpha1.ScheduleReleaseResponse) | The release is scheduled to be released at a specific future date and time. |
| CancelRelease | [CancelReleaseRequest](#animeshon.release.v1alpha1.CancelReleaseRequest) | [CancelReleaseResponse](#animeshon.release.v1alpha1.CancelReleaseResponse) | This method can only be called on scheduled releases. The scheduling is cancelled and the release is marked as a draft. |
| SuspendRelease | [SuspendReleaseRequest](#animeshon.release.v1alpha1.SuspendReleaseRequest) | [SuspendReleaseResponse](#animeshon.release.v1alpha1.SuspendReleaseResponse) | This method can only be called on published releases marked as active. Any non-authoritative release associated to the specified release will also be automatically marked as suspended. |

 



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

