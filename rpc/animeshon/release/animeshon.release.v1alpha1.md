# Package animeshon.release.v1alpha1

## Index
- [Publisher](#animeshon.release.v1alpha1.Publisher)
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
## Publisher {#animeshon.release.v1alpha1.Publisher}

| GetRelease |
| --- |
| **rpc** GetRelease([GetReleaseRequest](#animeshon.release.v1alpha1.GetReleaseRequest)) [Release](#animeshon.release.v1alpha1.Release)<br/> |

| ListReleases |
| --- |
| **rpc** ListReleases([ListReleasesRequest](#animeshon.release.v1alpha1.ListReleasesRequest)) [ListReleasesResponse](#animeshon.release.v1alpha1.ListReleasesResponse)<br/> |

| CreateRelease |
| --- |
| **rpc** CreateRelease([CreateReleaseRequest](#animeshon.release.v1alpha1.CreateReleaseRequest)) [Release](#animeshon.release.v1alpha1.Release)<br/> |

| UpdateRelease |
| --- |
| **rpc** UpdateRelease([UpdateReleaseRequest](#animeshon.release.v1alpha1.UpdateReleaseRequest)) [Release](#animeshon.release.v1alpha1.Release)<br/> |

| DeleteRelease |
| --- |
| **rpc** DeleteRelease([DeleteReleaseRequest](#animeshon.release.v1alpha1.DeleteReleaseRequest)) [.google.protobuf.Empty](#google.protobuf.Empty)<br/>The release is soft-deleted and a grace period is granted before complete deletion. During this grace period the release can be recovered. |

| UndeleteRelease |
| --- |
| **rpc** UndeleteRelease([UndeleteReleaseRequest](#animeshon.release.v1alpha1.UndeleteReleaseRequest)) [Release](#animeshon.release.v1alpha1.Release)<br/>This method allows to recover a release while still in the grace period. |

| PublishRelease |
| --- |
| **rpc** PublishRelease([PublishReleaseRequest](#animeshon.release.v1alpha1.PublishReleaseRequest)) [PublishReleaseResponse](#animeshon.release.v1alpha1.PublishReleaseResponse)<br/>The release is marked as immediately available to the public. |

| UnpublishRelease |
| --- |
| **rpc** UnpublishRelease([UnpublishReleaseRequest](#animeshon.release.v1alpha1.UnpublishReleaseRequest)) [UnpublishReleaseResponse](#animeshon.release.v1alpha1.UnpublishReleaseResponse)<br/>The release is unpublished and marked as a draft, associated non-authoritative will automatically be marked as suspended and hidden from the general public. |

| ScheduleRelease |
| --- |
| **rpc** ScheduleRelease([ScheduleReleaseRequest](#animeshon.release.v1alpha1.ScheduleReleaseRequest)) [ScheduleReleaseResponse](#animeshon.release.v1alpha1.ScheduleReleaseResponse)<br/>The release is scheduled to be released at a specific future date and time. |

| CancelRelease |
| --- |
| **rpc** CancelRelease([CancelReleaseRequest](#animeshon.release.v1alpha1.CancelReleaseRequest)) [CancelReleaseResponse](#animeshon.release.v1alpha1.CancelReleaseResponse)<br/>This method can only be called on scheduled releases. The scheduling is cancelled and the release is marked as a draft. |

| SuspendRelease |
| --- |
| **rpc** SuspendRelease([SuspendReleaseRequest](#animeshon.release.v1alpha1.SuspendReleaseRequest)) [SuspendReleaseResponse](#animeshon.release.v1alpha1.SuspendReleaseResponse)<br/>This method can only be called on published releases marked as active. Any non-authoritative release associated to the specified release will also be automatically marked as suspended. |

## CancelReleaseRequest {#animeshon.release.v1alpha1.CancelReleaseRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the release to cancel. |
## CancelReleaseResponse {#animeshon.release.v1alpha1.CancelReleaseResponse}

## CreateReleaseRequest {#animeshon.release.v1alpha1.CreateReleaseRequest}

| Field | Description |
| --- | --- |
| parent | **[ string](#string)**<br/>The parent this release belongs to. |
| release | **[ Release](#Release)**<br/>The release to create. |
| ttl | **[ google.protobuf.Duration](#google.protobuf.Duration)**<br/>The time-to-live indicating for how long this release should be published. If set to zero, the release will not have an expiration time. |
## DeleteReleaseRequest {#animeshon.release.v1alpha1.DeleteReleaseRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the release to delete. |
## GetReleaseRequest {#animeshon.release.v1alpha1.GetReleaseRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the release to retrieve. |
## ListReleasesRequest {#animeshon.release.v1alpha1.ListReleasesRequest}

| Field | Description |
| --- | --- |
| parent | **[ string](#string)**<br/>The parent to list releases from. |
| page_size | **[ int32](#int32)**<br/>If unspecified, server will pick an appropriate default. |
| page_token | **[ string](#string)**<br/>The value returned from the previous call. |
| filter | **[ string](#string)**<br/>A filter to be applied to results. |
## ListReleasesResponse {#animeshon.release.v1alpha1.ListReleasesResponse}

| Field | Description |
| --- | --- |
| releases | **[repeated Release](#Release)**<br/>The list of releases. |
| next_page_token | **[ string](#string)**<br/>A token to retrieve next page of results. |
## PublishReleaseRequest {#animeshon.release.v1alpha1.PublishReleaseRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the release to publish. |
| strategy | **[ ReleaseStrategy](#ReleaseStrategy)**<br/>The release strategy to use. |
## PublishReleaseResponse {#animeshon.release.v1alpha1.PublishReleaseResponse}

## Release {#animeshon.release.v1alpha1.Release}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The release resource name. |
| display_name | **[ string](#string)**<br/>The human-readable display name of the release. |
| description | **[ string](#string)**<br/>The short description of the release. |
| authoritative_release | **[ string](#string)**<br/>The authoritative release is set only for sub-licensed releases that do not hold any publishing rights on the content being distributed.

A common case where the release is to be considered non-authoritative is a translation released by third-parties. In such scenario the original author(s) is to be considered the only publishing authority over the content.

If for any reason the authoritative release were to be unpublished or deleted from Animeshon all associated non-authoritative releases will be automatically hidden from public consumption and marked as suspended.

Furthermore, there can only be one authoritative release per resource, which means that you can have unlimited non-authoritative releases for one resource but it must have exactly one authoritative release. |
| resource | **[ string](#string)**<br/>The resource being released. |
| asset | **[ string](#string)**<br/>The product included in the release. |
| access_group | **[ string](#string)**<br/>The group of users authorized to access the asset. |
| visibility | **[ Visibility](#Visibility)**<br/>The visibility of the resources included in the asset. |
| state | **[ Release.State](#Release.State)**<br/>The current release state. |
| labels | **[map Release.LabelsEntry](#Release.LabelsEntry)**<br/>The map of labels associated with the release. |
| create_time | **[ google.protobuf.Timestamp](#google.protobuf.Timestamp)**<br/>The timestamp at which the release was created. |
| update_time | **[ google.protobuf.Timestamp](#google.protobuf.Timestamp)**<br/>The latest timestamp at which the release was updated. |
| expire_time | **[ google.protobuf.Timestamp](#google.protobuf.Timestamp)**<br/>The timestamp at which the release will expire. |
| delete_time | **[ google.protobuf.Timestamp](#google.protobuf.Timestamp)**<br/>The timestamp at which the release was deleted. |
## Release.LabelsEntry {#animeshon.release.v1alpha1.Release.LabelsEntry}

| Field | Description |
| --- | --- |
| key | **[ string](#string)**<br/> |
| value | **[ string](#string)**<br/> |
## ReleaseStrategy {#animeshon.release.v1alpha1.ReleaseStrategy}
The release strategy describes how a release should be published.
| Field | Description |
| --- | --- |
| membership_only | **[ bool](#bool)**<br/>Whether the release should be available only to the members of a group. |
## ScheduleReleaseRequest {#animeshon.release.v1alpha1.ScheduleReleaseRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the release to schedule. |
| strategy | **[ ReleaseStrategy](#ReleaseStrategy)**<br/>The release strategy to use. |
## ScheduleReleaseResponse {#animeshon.release.v1alpha1.ScheduleReleaseResponse}

## SuspendReleaseRequest {#animeshon.release.v1alpha1.SuspendReleaseRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the release to suspend. |
| reason | **[ string](#string)**<br/>The reason why the release has been suspended. |
## SuspendReleaseResponse {#animeshon.release.v1alpha1.SuspendReleaseResponse}

## UndeleteReleaseRequest {#animeshon.release.v1alpha1.UndeleteReleaseRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the release to undelete. |
## UnpublishReleaseRequest {#animeshon.release.v1alpha1.UnpublishReleaseRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the release to publish. |
## UnpublishReleaseResponse {#animeshon.release.v1alpha1.UnpublishReleaseResponse}

## UpdateReleaseRequest {#animeshon.release.v1alpha1.UpdateReleaseRequest}

| Field | Description |
| --- | --- |
| release | **[ Release](#Release)**<br/>The release to update. |
| update_mask | **[ google.protobuf.FieldMask](#google.protobuf.FieldMask)**<br/>The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |

## Release.State {#animeshon.release.v1alpha1.Release.State}


| Name | Description |
| --- | --- |
| STATE_UNSPECIFIED | The default value. This value is used if the state is omitted. |
| ACTIVE | The release has been published and is available to the general public. |
| SCHEDULED | The release has been scheduled and will be made automatically available to the public according to the scheduling conditions. |
| DRAFT | The release is a draft and is still being worked on. |
| SUSPENDED | The release has been suspended. This state might automatically being set for non-authoritative releases when their authoritative release is also suspended, unpublished, or deleted. This state might also be set when a release is breaching general terms and conditions or is in conflict with community guidelines or internal governing policies. |
| DELETED | The release has been marked for deletion. |

## Visibility {#animeshon.release.v1alpha1.Visibility}


| Name | Description |
| --- | --- |
| VISIBILITY_UNSPECIFIED | The default value. This value is used if the state is omitted. |
| PRIVATE | The release is private and can only be accessed by users and service accounts that have been granted direct access to the release resource via explicit or inherited IAM policies. |
| MEMBERSHIP | The release has been published and access to its assets is limited to members that have paid the membership fee (e.g. a user who has bought the release). |
| PUBLIC | The release has been published and all of its assets are publicly available to all users. |
