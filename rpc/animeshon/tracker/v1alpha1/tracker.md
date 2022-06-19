# Protocol Documentation
<a name="top"></a>

## Table of Contents

- [animeshon/tracker/v1alpha1/tracker.proto](#animeshon/tracker/v1alpha1/tracker.proto)
    - [Activity](#animeshon.tracker.v1alpha1.Activity)
    - [Audience](#animeshon.tracker.v1alpha1.Audience)
    - [CreateActivityRequest](#animeshon.tracker.v1alpha1.CreateActivityRequest)
    - [CreateTrackerRequest](#animeshon.tracker.v1alpha1.CreateTrackerRequest)
    - [DeleteActivityRequest](#animeshon.tracker.v1alpha1.DeleteActivityRequest)
    - [DeleteTrackerRequest](#animeshon.tracker.v1alpha1.DeleteTrackerRequest)
    - [ExportTrackersRequest](#animeshon.tracker.v1alpha1.ExportTrackersRequest)
    - [ExportTrackersResponse](#animeshon.tracker.v1alpha1.ExportTrackersResponse)
    - [GetTrackerRequest](#animeshon.tracker.v1alpha1.GetTrackerRequest)
    - [ImportTrackersRequest](#animeshon.tracker.v1alpha1.ImportTrackersRequest)
    - [ImportTrackersResponse](#animeshon.tracker.v1alpha1.ImportTrackersResponse)
    - [ListTrackersRequest](#animeshon.tracker.v1alpha1.ListTrackersRequest)
    - [ListTrackersResponse](#animeshon.tracker.v1alpha1.ListTrackersResponse)
    - [OperationMetadata](#animeshon.tracker.v1alpha1.OperationMetadata)
    - [Tracker](#animeshon.tracker.v1alpha1.Tracker)
    - [UpdateTrackerRequest](#animeshon.tracker.v1alpha1.UpdateTrackerRequest)
  
    - [Provider](#animeshon.tracker.v1alpha1.Provider)
    - [State](#animeshon.tracker.v1alpha1.State)
  
    - [TrackerService](#animeshon.tracker.v1alpha1.TrackerService)
  
- [Scalar Value Types](#scalar-value-types)



<a name="animeshon/tracker/v1alpha1/tracker.proto"></a>
<p align="right"><a href="#top">Top</a></p>

## animeshon/tracker/v1alpha1/tracker.proto



<a name="animeshon.tracker.v1alpha1.Activity"></a>

### Activity
Activities track the progress of a user related to readable or watchable
resources such as light novel and graphic novel chapters, and anime episodes.

Activities are immutable and store meta information such as when the activity
started, when it ended, from where the progress started and where it stopped.

An example of activities might be a user watching on Netflix the Episode N of
the Anime XYZ from minute 5:47 to minute 15:32 on the 7th of July at 8:35 PM.

In this specific case a Chrome extension might automatically create a new
activity every minute until the user pauses the video or closes the tab.

The information collected allows the service to let the user know when was
the last &#34;checkpoint&#34; recorded, enabling the user to resume the episode at
the correct time on a different platform (i.e. continue from where I left).
Additionally, the information collected is useful to generate histograms and
to idenitify popular scenes within an episode (we all know Pornhub has an
identical feature already).

There is no limit to the number of activities a user might generate and some
activities are automatically registered from Animeshon itself, for example
when a user is reading a graph novel directly on our platform. Activities can
also be repeated multiple times for the same range (e.g. if a user rewatches
the same scene in an episode 5 times).

Whenever an activity is created that marks the end of a resource, its parent
tracker is updated to include it in the list of completed resource.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The id of the activity. |
| resource | [string](#string) |  | The content whose progress is being tracked. |
| platform | [string](#string) |  | The platform that the user used to consume the resource. |
| from | [int32](#int32) |  | Where the activity started within the resource. This value represents the time in seconds within an episode or the page number within a graphic novel or light novel chapter. |
| to | [int32](#int32) |  | Where the activity ended within the resource. This value represents the time in seconds within an episode or the page number within a graphic novel or light novel chapter. |
| start_time | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | When this activity started. |
| end_time | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | When this activity ended. |






<a name="animeshon.tracker.v1alpha1.Audience"></a>

### Audience
TODO: this is represented as a group in authorization.
TODO: who should be the owner of an audience? the user who created it?


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The id of the audience. |
| members | [string](#string) | repeated | The members of this audience. |






<a name="animeshon.tracker.v1alpha1.CreateActivityRequest"></a>

### CreateActivityRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| parent | [string](#string) |  | The parent this tracker belongs to. |
| activity | [Activity](#animeshon.tracker.v1alpha1.Activity) |  | The activity to create. |






<a name="animeshon.tracker.v1alpha1.CreateTrackerRequest"></a>

### CreateTrackerRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| parent | [string](#string) |  | The parent this tracker belongs to. |
| tracker | [Tracker](#animeshon.tracker.v1alpha1.Tracker) |  | The tracker to create. |






<a name="animeshon.tracker.v1alpha1.DeleteActivityRequest"></a>

### DeleteActivityRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the activity to delete. |






<a name="animeshon.tracker.v1alpha1.DeleteTrackerRequest"></a>

### DeleteTrackerRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the tracker to delete. |






<a name="animeshon.tracker.v1alpha1.ExportTrackersRequest"></a>

### ExportTrackersRequest
Selecting what provider we want to export to


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| parent | [string](#string) |  |  |
| provider | [Provider](#animeshon.tracker.v1alpha1.Provider) |  |  |






<a name="animeshon.tracker.v1alpha1.ExportTrackersResponse"></a>

### ExportTrackersResponse







<a name="animeshon.tracker.v1alpha1.GetTrackerRequest"></a>

### GetTrackerRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the tracker to retrieve. |






<a name="animeshon.tracker.v1alpha1.ImportTrackersRequest"></a>

### ImportTrackersRequest
Selecting what provider we want to import from


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| parent | [string](#string) |  |  |
| provider | [Provider](#animeshon.tracker.v1alpha1.Provider) |  |  |






<a name="animeshon.tracker.v1alpha1.ImportTrackersResponse"></a>

### ImportTrackersResponse
TODO(christian-roggia): this is a workaround to solve the issue of GAPIC
CLI where broken code is generated if google.protobuf.Empty is used in the
response_type of longrunning operations.






<a name="animeshon.tracker.v1alpha1.ListTrackersRequest"></a>

### ListTrackersRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| parent | [string](#string) |  | The user this tracker belongs to. |
| page_size | [int32](#int32) |  | If unspecified, server will pick an appropriate default. |
| page_token | [string](#string) |  | The value returned from the previous call. |
| filter | [string](#string) |  | A filter to be applied to results. |






<a name="animeshon.tracker.v1alpha1.ListTrackersResponse"></a>

### ListTrackersResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| trackers | [Tracker](#animeshon.tracker.v1alpha1.Tracker) | repeated | The list of trackers. |
| next_page_token | [string](#string) |  | A token to retrieve next page of results. |






<a name="animeshon.tracker.v1alpha1.OperationMetadata"></a>

### OperationMetadata
Represents the metadata of the long-running operation.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| create_time | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | Output only. The time the operation was created. |
| end_time | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | Output only. The time the operation finished running. |
| target | [string](#string) |  | Output only. Server-defined resource path for the target of the operation. |
| verb | [string](#string) |  | Output only. Name of the verb executed by the operation. |
| status_message | [string](#string) |  | Output only. Human-readable status of the operation, if any. |
| requested_cancellation | [bool](#bool) |  | Output only. Identifies whether the user has requested cancellation of the operation. Operations that have successfully been cancelled have [Operation.error][] value with a [google.rpc.Status.code][google.rpc.Status.code] of 1, corresponding to `Code.CANCELLED`. |
| api_version | [string](#string) |  | Output only. API version used to start the operation. |
| progress_percentage | [int32](#int32) |  | Output only. |






<a name="animeshon.tracker.v1alpha1.Tracker"></a>

### Tracker
A tracker tracks the progress of one or more users related to releasable
resources such as animes, graphic novels, light novels, and visual novels.

It is important to notice that users cannot `watch` an anime from a technical
perspective but rather they can watch one of its releases such as its pysical
DVD copy or its broadcast on Funimation. Nevertheless, for a better user
experience a releasable content is considered completed whenever a user
watched, played, or read all of its &#34;regular&#34; episodes, chapters, or
releases. This means that &#34;recaps&#34; and &#34;specials&#34; are ultimately ignored.

Animes and novels are easier to track as they have a countable and defined
amount of resources that can be consumed (episodes and chapters). Their
progress is therefore automatically updated whenever a new user activity is
generated.

Visual novels and video games in general do not always have a clear progress
and therefore must be updated manually by the user.

A tracker accounts only for the overall progress on a releasable content,
this means that it won&#39;t provide any information about rewatches.

Additionally, trackers can be shared among multiple users thorough audiences,
this is useful whenever a user is, for example, watching an anime together
with a group of friends and wants to keep track of the progress separately
from his/her own personal progress or from the progress on the same resource
with another group of friends (i.e. audience).

The progress of audience trackers affects the personal progress, that is
whenever new resources are consumed by an audience the personal tracker of
each member belonging to that audience will be updated automatically as well.
This behavior makes sense as a group of people  watching the Episode N of the
Anime XYZ also means that each member of the group also watched the episode
and therefore their collective personal progress changed.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The id of the tracker. |
| resource | [string](#string) |  | The content whose progress is being tracked. |
| start_time | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | When the progress started. |
| end_time | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | When the progress ended. |
| completed_resources | [string](#string) | repeated | The list of completed sub-resources (e.g episodes or chapters). |
| progress_percentage | [google.protobuf.FloatValue](#google.protobuf.FloatValue) |  | The percentage of progress from 0 to 100. A null value means the value was not manually defined and therefore the percentage should be calculated on-the-fly. |
| state | [State](#animeshon.tracker.v1alpha1.State) |  | The progress state of the tracker. |






<a name="animeshon.tracker.v1alpha1.UpdateTrackerRequest"></a>

### UpdateTrackerRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| tracker | [Tracker](#animeshon.tracker.v1alpha1.Tracker) |  | The tracker to update. |
| update_mask | [google.protobuf.FieldMask](#google.protobuf.FieldMask) |  | The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |





 


<a name="animeshon.tracker.v1alpha1.Provider"></a>

### Provider


| Name | Number | Description |
| ---- | ------ | ----------- |
| PROVIDER_UNSPECIFIED | 0 |  |
| MYANIMELIST | 1 |  |
| MANGADEX | 2 |  |
| ANILIST | 3 |  |
| ANIDB | 4 |  |
| MANGAUPDATES | 5 |  |
| VNDB | 6 |  |



<a name="animeshon.tracker.v1alpha1.State"></a>

### State


| Name | Number | Description |
| ---- | ------ | ----------- |
| STATE_UNSPECIFIED | 0 |  |
| IN_PROGRESS | 1 | The consumption of the media is still in progress. |
| COMPLETED | 2 | The consumption of the media has been completed. |
| ON_HOLD | 3 | The consumption of the media is on hold. |


 

 


<a name="animeshon.tracker.v1alpha1.TrackerService"></a>

### TrackerService


| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| GetTracker | [GetTrackerRequest](#animeshon.tracker.v1alpha1.GetTrackerRequest) | [Tracker](#animeshon.tracker.v1alpha1.Tracker) | Get a tracker by its unique identifier.

To fetch a tracker by the resource, use `ListTrackers` instead with an appropriate filter. Example: `filter = &#34;resource:animes/1245678&#34;`. |
| ListTrackers | [ListTrackersRequest](#animeshon.tracker.v1alpha1.ListTrackersRequest) | [ListTrackersResponse](#animeshon.tracker.v1alpha1.ListTrackersResponse) | TODO: add documentation about supported filters. |
| CreateTracker | [CreateTrackerRequest](#animeshon.tracker.v1alpha1.CreateTrackerRequest) | [Tracker](#animeshon.tracker.v1alpha1.Tracker) |  |
| UpdateTracker | [UpdateTrackerRequest](#animeshon.tracker.v1alpha1.UpdateTrackerRequest) | [Tracker](#animeshon.tracker.v1alpha1.Tracker) |  |
| DeleteTracker | [DeleteTrackerRequest](#animeshon.tracker.v1alpha1.DeleteTrackerRequest) | [.google.protobuf.Empty](#google.protobuf.Empty) |  |
| ImportTrackers | [ImportTrackersRequest](#animeshon.tracker.v1alpha1.ImportTrackersRequest) | [.google.longrunning.Operation](#google.longrunning.Operation) |  |
| ExportTrackers | [ExportTrackersRequest](#animeshon.tracker.v1alpha1.ExportTrackersRequest) | [.google.longrunning.Operation](#google.longrunning.Operation) |  |
| CreateActivity | [CreateActivityRequest](#animeshon.tracker.v1alpha1.CreateActivityRequest) | [Activity](#animeshon.tracker.v1alpha1.Activity) |  |
| DeleteActivity | [DeleteActivityRequest](#animeshon.tracker.v1alpha1.DeleteActivityRequest) | [.google.protobuf.Empty](#google.protobuf.Empty) |  |

 



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

