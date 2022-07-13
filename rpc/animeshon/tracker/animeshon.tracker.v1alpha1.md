# Package animeshon.tracker.v1alpha1

## Index
- [TrackerService](#animeshon.tracker.v1alpha1.TrackerService)
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
## TrackerService {#animeshon.tracker.v1alpha1.TrackerService}

| GetTracker |
| --- |
| **rpc** GetTracker([GetTrackerRequest](#animeshon.tracker.v1alpha1.GetTrackerRequest)) [Tracker](#animeshon.tracker.v1alpha1.Tracker)<br/>Get a tracker by its unique identifier.

To fetch a tracker by the resource, use `ListTrackers` instead with an appropriate filter. Example: `filter = "resource:animes/1245678"`. |

| ListTrackers |
| --- |
| **rpc** ListTrackers([ListTrackersRequest](#animeshon.tracker.v1alpha1.ListTrackersRequest)) [ListTrackersResponse](#animeshon.tracker.v1alpha1.ListTrackersResponse)<br/>TODO: add documentation about supported filters. |

| CreateTracker |
| --- |
| **rpc** CreateTracker([CreateTrackerRequest](#animeshon.tracker.v1alpha1.CreateTrackerRequest)) [Tracker](#animeshon.tracker.v1alpha1.Tracker)<br/> |

| UpdateTracker |
| --- |
| **rpc** UpdateTracker([UpdateTrackerRequest](#animeshon.tracker.v1alpha1.UpdateTrackerRequest)) [Tracker](#animeshon.tracker.v1alpha1.Tracker)<br/> |

| DeleteTracker |
| --- |
| **rpc** DeleteTracker([DeleteTrackerRequest](#animeshon.tracker.v1alpha1.DeleteTrackerRequest)) [.google.protobuf.Empty](#google.protobuf.Empty)<br/> |

| ImportTrackers |
| --- |
| **rpc** ImportTrackers([ImportTrackersRequest](#animeshon.tracker.v1alpha1.ImportTrackersRequest)) [.google.longrunning.Operation](#google.longrunning.Operation)<br/> |

| ExportTrackers |
| --- |
| **rpc** ExportTrackers([ExportTrackersRequest](#animeshon.tracker.v1alpha1.ExportTrackersRequest)) [.google.longrunning.Operation](#google.longrunning.Operation)<br/> |

| CreateActivity |
| --- |
| **rpc** CreateActivity([CreateActivityRequest](#animeshon.tracker.v1alpha1.CreateActivityRequest)) [Activity](#animeshon.tracker.v1alpha1.Activity)<br/> |

| DeleteActivity |
| --- |
| **rpc** DeleteActivity([DeleteActivityRequest](#animeshon.tracker.v1alpha1.DeleteActivityRequest)) [.google.protobuf.Empty](#google.protobuf.Empty)<br/> |

## Activity {#animeshon.tracker.v1alpha1.Activity}
Activities track the progress of a user related to readable or watchable
resources such as light novel and graphic novel chapters, and anime episodes.

Activities are immutable and store meta information such as when the activity
started, when it ended, from where the progress started and where it stopped.

An example of activities might be a user watching on Netflix the Episode N of
the Anime XYZ from minute 5:47 to minute 15:32 on the 7th of July at 8:35 PM.

In this specific case a Chrome extension might automatically create a new
activity every minute until the user pauses the video or closes the tab.

The information collected allows the service to let the user know when was
the last "checkpoint" recorded, enabling the user to resume the episode at
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
| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The id of the activity. |
| resource | **[ string](#string)**<br/>The content whose progress is being tracked. |
| platform | **[ string](#string)**<br/>The platform that the user used to consume the resource. |
| from | **[ int32](#int32)**<br/>Where the activity started within the resource. This value represents the time in seconds within an episode or the page number within a graphic novel or light novel chapter. |
| to | **[ int32](#int32)**<br/>Where the activity ended within the resource. This value represents the time in seconds within an episode or the page number within a graphic novel or light novel chapter. |
| start_time | **[ google.protobuf.Timestamp](#google.protobuf.Timestamp)**<br/>When this activity started. |
| end_time | **[ google.protobuf.Timestamp](#google.protobuf.Timestamp)**<br/>When this activity ended. |
## Audience {#animeshon.tracker.v1alpha1.Audience}
TODO: this is represented as a group in authorization.
TODO: who should be the owner of an audience? the user who created it?
| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The id of the audience. |
| members | **[repeated string](#string)**<br/>The members of this audience. |
## CreateActivityRequest {#animeshon.tracker.v1alpha1.CreateActivityRequest}

| Field | Description |
| --- | --- |
| parent | **[ string](#string)**<br/>The parent this tracker belongs to. |
| activity | **[ Activity](#Activity)**<br/>The activity to create. |
## CreateTrackerRequest {#animeshon.tracker.v1alpha1.CreateTrackerRequest}

| Field | Description |
| --- | --- |
| parent | **[ string](#string)**<br/>The parent this tracker belongs to. |
| tracker | **[ Tracker](#Tracker)**<br/>The tracker to create. |
## DeleteActivityRequest {#animeshon.tracker.v1alpha1.DeleteActivityRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the activity to delete. |
## DeleteTrackerRequest {#animeshon.tracker.v1alpha1.DeleteTrackerRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the tracker to delete. |
## ExportTrackersRequest {#animeshon.tracker.v1alpha1.ExportTrackersRequest}
Selecting what provider we want to export to
| Field | Description |
| --- | --- |
| parent | **[ string](#string)**<br/> |
| provider | **[ Provider](#Provider)**<br/> |
## ExportTrackersResponse {#animeshon.tracker.v1alpha1.ExportTrackersResponse}

## GetTrackerRequest {#animeshon.tracker.v1alpha1.GetTrackerRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the tracker to retrieve. |
## ImportTrackersRequest {#animeshon.tracker.v1alpha1.ImportTrackersRequest}
Selecting what provider we want to import from
| Field | Description |
| --- | --- |
| parent | **[ string](#string)**<br/> |
| provider | **[ Provider](#Provider)**<br/> |
## ImportTrackersResponse {#animeshon.tracker.v1alpha1.ImportTrackersResponse}
TODO(christian-roggia): this is a workaround to solve the issue of GAPIC
CLI where broken code is generated if google.protobuf.Empty is used in the
response_type of longrunning operations.
## ListTrackersRequest {#animeshon.tracker.v1alpha1.ListTrackersRequest}

| Field | Description |
| --- | --- |
| parent | **[ string](#string)**<br/>The user this tracker belongs to. |
| page_size | **[ int32](#int32)**<br/>If unspecified, server will pick an appropriate default. |
| page_token | **[ string](#string)**<br/>The value returned from the previous call. |
| filter | **[ string](#string)**<br/>A filter to be applied to results. |
## ListTrackersResponse {#animeshon.tracker.v1alpha1.ListTrackersResponse}

| Field | Description |
| --- | --- |
| trackers | **[repeated Tracker](#Tracker)**<br/>The list of trackers. |
| next_page_token | **[ string](#string)**<br/>A token to retrieve next page of results. |
## OperationMetadata {#animeshon.tracker.v1alpha1.OperationMetadata}
Represents the metadata of the long-running operation.
| Field | Description |
| --- | --- |
| create_time | **[ google.protobuf.Timestamp](#google.protobuf.Timestamp)**<br/>Output only. The time the operation was created. |
| end_time | **[ google.protobuf.Timestamp](#google.protobuf.Timestamp)**<br/>Output only. The time the operation finished running. |
| target | **[ string](#string)**<br/>Output only. Server-defined resource path for the target of the operation. |
| verb | **[ string](#string)**<br/>Output only. Name of the verb executed by the operation. |
| status_message | **[ string](#string)**<br/>Output only. Human-readable status of the operation, if any. |
| requested_cancellation | **[ bool](#bool)**<br/>Output only. Identifies whether the user has requested cancellation of the operation. Operations that have successfully been cancelled have [Operation.error][] value with a [google.rpc.Status.code][google.rpc.Status.code] of 1, corresponding to `Code.CANCELLED`. |
| api_version | **[ string](#string)**<br/>Output only. API version used to start the operation. |
| progress_percentage | **[ int32](#int32)**<br/>Output only. |
## Tracker {#animeshon.tracker.v1alpha1.Tracker}
A tracker tracks the progress of one or more users related to releasable
resources such as animes, graphic novels, light novels, and visual novels.

It is important to notice that users cannot `watch` an anime from a technical
perspective but rather they can watch one of its releases such as its pysical
DVD copy or its broadcast on Funimation. Nevertheless, for a better user
experience a releasable content is considered completed whenever a user
watched, played, or read all of its "regular" episodes, chapters, or
releases. This means that "recaps" and "specials" are ultimately ignored.

Animes and novels are easier to track as they have a countable and defined
amount of resources that can be consumed (episodes and chapters). Their
progress is therefore automatically updated whenever a new user activity is
generated.

Visual novels and video games in general do not always have a clear progress
and therefore must be updated manually by the user.

A tracker accounts only for the overall progress on a releasable content,
this means that it won't provide any information about rewatches.

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
| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The id of the tracker. |
| resource | **[ string](#string)**<br/>The content whose progress is being tracked. |
| start_time | **[ google.protobuf.Timestamp](#google.protobuf.Timestamp)**<br/>When the progress started. |
| end_time | **[ google.protobuf.Timestamp](#google.protobuf.Timestamp)**<br/>When the progress ended. |
| completed_resources | **[repeated string](#string)**<br/>The list of completed sub-resources (e.g episodes or chapters). |
| progress_percentage | **[ google.protobuf.FloatValue](#google.protobuf.FloatValue)**<br/>The percentage of progress from 0 to 100. A null value means the value was not manually defined and therefore the percentage should be calculated on-the-fly. |
| state | **[ State](#State)**<br/>The progress state of the tracker. |
## UpdateTrackerRequest {#animeshon.tracker.v1alpha1.UpdateTrackerRequest}

| Field | Description |
| --- | --- |
| tracker | **[ Tracker](#Tracker)**<br/>The tracker to update. |
| update_mask | **[ google.protobuf.FieldMask](#google.protobuf.FieldMask)**<br/>The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |

## Provider {#animeshon.tracker.v1alpha1.Provider}


| Name | Description |
| --- | --- |
| PROVIDER_UNSPECIFIED | No description. |
| MYANIMELIST | No description. |
| MANGADEX | No description. |
| ANILIST | No description. |
| ANIDB | No description. |
| MANGAUPDATES | No description. |
| VNDB | No description. |

## State {#animeshon.tracker.v1alpha1.State}


| Name | Description |
| --- | --- |
| STATE_UNSPECIFIED | No description. |
| IN_PROGRESS | The consumption of the media is still in progress. |
| COMPLETED | The consumption of the media has been completed. |
| ON_HOLD | The consumption of the media is on hold. |
