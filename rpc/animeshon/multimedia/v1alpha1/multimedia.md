# Protocol Documentation
<a name="top"></a>

## Table of Contents

- [animeshon/multimedia/v1alpha1/common.proto](#animeshon/multimedia/v1alpha1/common.proto)
    - [OperationMetadata](#animeshon.multimedia.v1alpha1.OperationMetadata)
  
    - [PublishingType](#animeshon.multimedia.v1alpha1.PublishingType)
    - [State](#animeshon.multimedia.v1alpha1.State)
  
- [animeshon/multimedia/v1alpha1/anime.proto](#animeshon/multimedia/v1alpha1/anime.proto)
    - [Anime](#animeshon.multimedia.v1alpha1.Anime)
    - [CreateAnimeRequest](#animeshon.multimedia.v1alpha1.CreateAnimeRequest)
    - [DeleteAnimeRequest](#animeshon.multimedia.v1alpha1.DeleteAnimeRequest)
    - [GetAnimeRequest](#animeshon.multimedia.v1alpha1.GetAnimeRequest)
    - [ListAnimesRequest](#animeshon.multimedia.v1alpha1.ListAnimesRequest)
    - [ListAnimesResponse](#animeshon.multimedia.v1alpha1.ListAnimesResponse)
    - [ReconcileAnimesRequest](#animeshon.multimedia.v1alpha1.ReconcileAnimesRequest)
    - [ReconcileAnimesResponse](#animeshon.multimedia.v1alpha1.ReconcileAnimesResponse)
    - [UpdateAnimeRequest](#animeshon.multimedia.v1alpha1.UpdateAnimeRequest)
  
    - [Anime.Type](#animeshon.multimedia.v1alpha1.Anime.Type)
  
    - [AnimeService](#animeshon.multimedia.v1alpha1.AnimeService)
  
- [animeshon/multimedia/v1alpha1/chapter.proto](#animeshon/multimedia/v1alpha1/chapter.proto)
    - [BatchCreateChaptersRequest](#animeshon.multimedia.v1alpha1.BatchCreateChaptersRequest)
    - [BatchCreateChaptersRequest.Request](#animeshon.multimedia.v1alpha1.BatchCreateChaptersRequest.Request)
    - [BatchCreateChaptersResponse](#animeshon.multimedia.v1alpha1.BatchCreateChaptersResponse)
    - [BatchCreateChaptersResponse.Response](#animeshon.multimedia.v1alpha1.BatchCreateChaptersResponse.Response)
    - [Chapter](#animeshon.multimedia.v1alpha1.Chapter)
    - [CreateChapterRequest](#animeshon.multimedia.v1alpha1.CreateChapterRequest)
    - [DeleteChapterRequest](#animeshon.multimedia.v1alpha1.DeleteChapterRequest)
    - [GetChapterRequest](#animeshon.multimedia.v1alpha1.GetChapterRequest)
    - [ListChaptersRequest](#animeshon.multimedia.v1alpha1.ListChaptersRequest)
    - [ListChaptersResponse](#animeshon.multimedia.v1alpha1.ListChaptersResponse)
    - [ReconcileChaptersRequest](#animeshon.multimedia.v1alpha1.ReconcileChaptersRequest)
    - [ReconcileChaptersResponse](#animeshon.multimedia.v1alpha1.ReconcileChaptersResponse)
    - [UpdateChapterRequest](#animeshon.multimedia.v1alpha1.UpdateChapterRequest)
  
    - [Chapter.Type](#animeshon.multimedia.v1alpha1.Chapter.Type)
  
    - [ChapterService](#animeshon.multimedia.v1alpha1.ChapterService)
  
- [animeshon/multimedia/v1alpha1/episode.proto](#animeshon/multimedia/v1alpha1/episode.proto)
    - [BatchCreateEpisodesRequest](#animeshon.multimedia.v1alpha1.BatchCreateEpisodesRequest)
    - [BatchCreateEpisodesRequest.Request](#animeshon.multimedia.v1alpha1.BatchCreateEpisodesRequest.Request)
    - [BatchCreateEpisodesResponse](#animeshon.multimedia.v1alpha1.BatchCreateEpisodesResponse)
    - [BatchCreateEpisodesResponse.Response](#animeshon.multimedia.v1alpha1.BatchCreateEpisodesResponse.Response)
    - [CreateEpisodeRequest](#animeshon.multimedia.v1alpha1.CreateEpisodeRequest)
    - [DeleteEpisodeRequest](#animeshon.multimedia.v1alpha1.DeleteEpisodeRequest)
    - [Episode](#animeshon.multimedia.v1alpha1.Episode)
    - [GetEpisodeRequest](#animeshon.multimedia.v1alpha1.GetEpisodeRequest)
    - [ListEpisodesRequest](#animeshon.multimedia.v1alpha1.ListEpisodesRequest)
    - [ListEpisodesResponse](#animeshon.multimedia.v1alpha1.ListEpisodesResponse)
    - [ReconcileEpisodesRequest](#animeshon.multimedia.v1alpha1.ReconcileEpisodesRequest)
    - [ReconcileEpisodesResponse](#animeshon.multimedia.v1alpha1.ReconcileEpisodesResponse)
    - [UpdateEpisodeRequest](#animeshon.multimedia.v1alpha1.UpdateEpisodeRequest)
  
    - [Episode.Type](#animeshon.multimedia.v1alpha1.Episode.Type)
  
    - [EpisodeService](#animeshon.multimedia.v1alpha1.EpisodeService)
  
- [animeshon/multimedia/v1alpha1/graphic_novel.proto](#animeshon/multimedia/v1alpha1/graphic_novel.proto)
    - [CreateGraphicNovelRequest](#animeshon.multimedia.v1alpha1.CreateGraphicNovelRequest)
    - [DeleteGraphicNovelRequest](#animeshon.multimedia.v1alpha1.DeleteGraphicNovelRequest)
    - [GetGraphicNovelRequest](#animeshon.multimedia.v1alpha1.GetGraphicNovelRequest)
    - [GraphicNovel](#animeshon.multimedia.v1alpha1.GraphicNovel)
    - [ListGraphicNovelsRequest](#animeshon.multimedia.v1alpha1.ListGraphicNovelsRequest)
    - [ListGraphicNovelsResponse](#animeshon.multimedia.v1alpha1.ListGraphicNovelsResponse)
    - [ReconcileGraphicNovelsRequest](#animeshon.multimedia.v1alpha1.ReconcileGraphicNovelsRequest)
    - [ReconcileGraphicNovelsResponse](#animeshon.multimedia.v1alpha1.ReconcileGraphicNovelsResponse)
    - [UpdateGraphicNovelRequest](#animeshon.multimedia.v1alpha1.UpdateGraphicNovelRequest)
  
    - [GraphicNovel.Type](#animeshon.multimedia.v1alpha1.GraphicNovel.Type)
  
    - [GraphicNovelService](#animeshon.multimedia.v1alpha1.GraphicNovelService)
  
- [animeshon/multimedia/v1alpha1/visual_novel.proto](#animeshon/multimedia/v1alpha1/visual_novel.proto)
    - [CreateVisualNovelRequest](#animeshon.multimedia.v1alpha1.CreateVisualNovelRequest)
    - [DeleteVisualNovelRequest](#animeshon.multimedia.v1alpha1.DeleteVisualNovelRequest)
    - [GetVisualNovelRequest](#animeshon.multimedia.v1alpha1.GetVisualNovelRequest)
    - [ListVisualNovelsRequest](#animeshon.multimedia.v1alpha1.ListVisualNovelsRequest)
    - [ListVisualNovelsResponse](#animeshon.multimedia.v1alpha1.ListVisualNovelsResponse)
    - [ReconcileVisualNovelsRequest](#animeshon.multimedia.v1alpha1.ReconcileVisualNovelsRequest)
    - [ReconcileVisualNovelsResponse](#animeshon.multimedia.v1alpha1.ReconcileVisualNovelsResponse)
    - [UpdateVisualNovelRequest](#animeshon.multimedia.v1alpha1.UpdateVisualNovelRequest)
    - [VisualNovel](#animeshon.multimedia.v1alpha1.VisualNovel)
  
    - [VisualNovel.PlayLength](#animeshon.multimedia.v1alpha1.VisualNovel.PlayLength)
    - [VisualNovel.Type](#animeshon.multimedia.v1alpha1.VisualNovel.Type)
  
    - [VisualNovelService](#animeshon.multimedia.v1alpha1.VisualNovelService)
  
- [animeshon/multimedia/v1alpha1/light_novel.proto](#animeshon/multimedia/v1alpha1/light_novel.proto)
    - [CreateLightNovelRequest](#animeshon.multimedia.v1alpha1.CreateLightNovelRequest)
    - [DeleteLightNovelRequest](#animeshon.multimedia.v1alpha1.DeleteLightNovelRequest)
    - [GetLightNovelRequest](#animeshon.multimedia.v1alpha1.GetLightNovelRequest)
    - [LightNovel](#animeshon.multimedia.v1alpha1.LightNovel)
    - [ListLightNovelsRequest](#animeshon.multimedia.v1alpha1.ListLightNovelsRequest)
    - [ListLightNovelsResponse](#animeshon.multimedia.v1alpha1.ListLightNovelsResponse)
    - [ReconcileLightNovelsRequest](#animeshon.multimedia.v1alpha1.ReconcileLightNovelsRequest)
    - [ReconcileLightNovelsResponse](#animeshon.multimedia.v1alpha1.ReconcileLightNovelsResponse)
    - [UpdateLightNovelRequest](#animeshon.multimedia.v1alpha1.UpdateLightNovelRequest)
  
    - [LightNovel.Type](#animeshon.multimedia.v1alpha1.LightNovel.Type)
  
    - [LightNovelService](#animeshon.multimedia.v1alpha1.LightNovelService)
  
- [Scalar Value Types](#scalar-value-types)



<a name="animeshon/multimedia/v1alpha1/common.proto"></a>
<p align="right"><a href="#top">Top</a></p>

## animeshon/multimedia/v1alpha1/common.proto



<a name="animeshon.multimedia.v1alpha1.OperationMetadata"></a>

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





 


<a name="animeshon.multimedia.v1alpha1.PublishingType"></a>

### PublishingType


| Name | Number | Description |
| ---- | ------ | ----------- |
| PUBLISHING_TYPE_UNSPECIFIED | 0 | The default value. This value is used if the state is omitted. |
| SELF | 1 |  |
| CORPORATE | 2 |  |



<a name="animeshon.multimedia.v1alpha1.State"></a>

### State


| Name | Number | Description |
| ---- | ------ | ----------- |
| STATE_UNSPECIFIED | 0 | The default value. This value is used if the state is omitted. |
| ONGOING | 1 |  |
| COMPLETED | 2 |  |
| SCHEDULED | 3 |  |
| INTERRUPTED | 4 |  |
| CANCELED | 5 |  |
| SUSPENDED | 6 |  |
| WORK_IN_PROGRESS | 7 |  |


 

 

 



<a name="animeshon/multimedia/v1alpha1/anime.proto"></a>
<p align="right"><a href="#top">Top</a></p>

## animeshon/multimedia/v1alpha1/anime.proto



<a name="animeshon.multimedia.v1alpha1.Anime"></a>

### Anime



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The id of the anime. |
| cover_image | [string](#string) |  | The cover image of the anime. |
| banner_image | [string](#string) |  | The banner image of the anime. |
| title | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | The title of the anime localized in multiple languages. |
| synopsis | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | The synopsis of the anime localized in multiple languages. |
| description | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | The description of the anime localized in multiple languages. |
| type | [Anime.Type](#animeshon.multimedia.v1alpha1.Anime.Type) |  | The type of anime. |
| release_date | [google.type.Date](#google.type.Date) |  | The original release date of anime. |
| publishing_type | [PublishingType](#animeshon.multimedia.v1alpha1.PublishingType) |  | The original publishing type of this content. TODO: migrate this field to a more structured licensing history. |
| state | [State](#animeshon.multimedia.v1alpha1.State) |  | The current state of the anime. |
| original | [bool](#bool) |  | Whether this content is an original work or a derivative work (parody). |






<a name="animeshon.multimedia.v1alpha1.CreateAnimeRequest"></a>

### CreateAnimeRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| anime | [Anime](#animeshon.multimedia.v1alpha1.Anime) |  | The anime to create. |
| idempotent_resource_id | [int64](#int64) |  | An idempotent identifier to be used as static resource id. |






<a name="animeshon.multimedia.v1alpha1.DeleteAnimeRequest"></a>

### DeleteAnimeRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the anime to delete. |






<a name="animeshon.multimedia.v1alpha1.GetAnimeRequest"></a>

### GetAnimeRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the anime to retrieve. |






<a name="animeshon.multimedia.v1alpha1.ListAnimesRequest"></a>

### ListAnimesRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| page_size | [int32](#int32) |  | If unspecified, server will pick an appropriate default. |
| page_token | [string](#string) |  | The value returned from the previous call. |
| filter | [string](#string) |  | A filter to be applied to results. |






<a name="animeshon.multimedia.v1alpha1.ListAnimesResponse"></a>

### ListAnimesResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| animes | [Anime](#animeshon.multimedia.v1alpha1.Anime) | repeated | The list of animes. |
| next_page_token | [string](#string) |  | A token to retrieve next page of results. |






<a name="animeshon.multimedia.v1alpha1.ReconcileAnimesRequest"></a>

### ReconcileAnimesRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the anime to reconcile. Use the wildcard `animes/-` to reconcile all animes. |






<a name="animeshon.multimedia.v1alpha1.ReconcileAnimesResponse"></a>

### ReconcileAnimesResponse







<a name="animeshon.multimedia.v1alpha1.UpdateAnimeRequest"></a>

### UpdateAnimeRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| anime | [Anime](#animeshon.multimedia.v1alpha1.Anime) |  | The anime to update. |
| update_mask | [google.protobuf.FieldMask](#google.protobuf.FieldMask) |  | The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |





 


<a name="animeshon.multimedia.v1alpha1.Anime.Type"></a>

### Anime.Type


| Name | Number | Description |
| ---- | ------ | ----------- |
| TYPE_UNSPECIFIED | 0 | The default value. This value is used if the state is omitted. |
| TV | 1 |  |
| MOVIE | 2 |  |
| OVA | 3 |  |
| ONA | 4 |  |
| SPECIAL | 5 |  |
| WEB | 6 |  |
| MUSIC_VIDEO | 7 |  |
| OTHER | 8 |  |


 

 


<a name="animeshon.multimedia.v1alpha1.AnimeService"></a>

### AnimeService


| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| GetAnime | [GetAnimeRequest](#animeshon.multimedia.v1alpha1.GetAnimeRequest) | [Anime](#animeshon.multimedia.v1alpha1.Anime) |  |
| ListAnimes | [ListAnimesRequest](#animeshon.multimedia.v1alpha1.ListAnimesRequest) | [ListAnimesResponse](#animeshon.multimedia.v1alpha1.ListAnimesResponse) |  |
| CreateAnime | [CreateAnimeRequest](#animeshon.multimedia.v1alpha1.CreateAnimeRequest) | [Anime](#animeshon.multimedia.v1alpha1.Anime) |  |
| UpdateAnime | [UpdateAnimeRequest](#animeshon.multimedia.v1alpha1.UpdateAnimeRequest) | [Anime](#animeshon.multimedia.v1alpha1.Anime) |  |
| DeleteAnime | [DeleteAnimeRequest](#animeshon.multimedia.v1alpha1.DeleteAnimeRequest) | [.google.protobuf.Empty](#google.protobuf.Empty) |  |
| ReconcileAnimes | [ReconcileAnimesRequest](#animeshon.multimedia.v1alpha1.ReconcileAnimesRequest) | [.google.longrunning.Operation](#google.longrunning.Operation) | Reconcile animes with the search and knowledge base. |

 



<a name="animeshon/multimedia/v1alpha1/chapter.proto"></a>
<p align="right"><a href="#top">Top</a></p>

## animeshon/multimedia/v1alpha1/chapter.proto



<a name="animeshon.multimedia.v1alpha1.BatchCreateChaptersRequest"></a>

### BatchCreateChaptersRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| requests | [BatchCreateChaptersRequest.Request](#animeshon.multimedia.v1alpha1.BatchCreateChaptersRequest.Request) | repeated | Individual create chapter requests for this batch. |
| parent | [string](#string) |  | The parent this batch belongs to. |






<a name="animeshon.multimedia.v1alpha1.BatchCreateChaptersRequest.Request"></a>

### BatchCreateChaptersRequest.Request



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| chapter | [Chapter](#animeshon.multimedia.v1alpha1.Chapter) |  | The chapter to create. |
| idempotent_resource_id | [int64](#int64) |  | An idempotent identifier to be used as static resource id. |






<a name="animeshon.multimedia.v1alpha1.BatchCreateChaptersResponse"></a>

### BatchCreateChaptersResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| responses | [BatchCreateChaptersResponse.Response](#animeshon.multimedia.v1alpha1.BatchCreateChaptersResponse.Response) | repeated | Individual responses to create chapter requests within the batch. |






<a name="animeshon.multimedia.v1alpha1.BatchCreateChaptersResponse.Response"></a>

### BatchCreateChaptersResponse.Response



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| chapter | [Chapter](#animeshon.multimedia.v1alpha1.Chapter) |  | The newly created chapter. |
| error | [google.rpc.Status](#google.rpc.Status) |  | If set, represents the error message for the operation. |






<a name="animeshon.multimedia.v1alpha1.Chapter"></a>

### Chapter



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The id of the chapter. |
| cover_image | [string](#string) |  | The cover image of the chapter. |
| banner_image | [string](#string) |  | The banner image of the chapter. |
| title | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | The title of the chapter localized in multiple languages. |
| synopsis | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | The synopsis of the chapter localized in multiple languages. |
| description | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | The description of the chapter localized in multiple languages. |
| type | [Chapter.Type](#animeshon.multimedia.v1alpha1.Chapter.Type) |  | The type of chapter. |
| index | [int32](#int32) |  | The index of chapter. |
| release_date | [google.type.Date](#google.type.Date) |  | The original release date of chapter. |
| page_count | [int32](#int32) |  | The original page count of the chapter. |






<a name="animeshon.multimedia.v1alpha1.CreateChapterRequest"></a>

### CreateChapterRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| parent | [string](#string) |  | The parent this chapter belongs to. |
| chapter | [Chapter](#animeshon.multimedia.v1alpha1.Chapter) |  | The chapter to create. |
| idempotent_resource_id | [int64](#int64) |  | An idempotent identifier to be used as static resource id. |






<a name="animeshon.multimedia.v1alpha1.DeleteChapterRequest"></a>

### DeleteChapterRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the chapter to delete. |






<a name="animeshon.multimedia.v1alpha1.GetChapterRequest"></a>

### GetChapterRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the chapter to retrieve. |






<a name="animeshon.multimedia.v1alpha1.ListChaptersRequest"></a>

### ListChaptersRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| parent | [string](#string) |  | The parent this chapter belongs to. |
| page_size | [int32](#int32) |  | If unspecified, server will pick an appropriate default. |
| page_token | [string](#string) |  | The value returned from the previous call. |
| filter | [string](#string) |  | A filter to be applied to results. |






<a name="animeshon.multimedia.v1alpha1.ListChaptersResponse"></a>

### ListChaptersResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| chapters | [Chapter](#animeshon.multimedia.v1alpha1.Chapter) | repeated | The list of chapters. |
| next_page_token | [string](#string) |  | A token to retrieve next page of results. |






<a name="animeshon.multimedia.v1alpha1.ReconcileChaptersRequest"></a>

### ReconcileChaptersRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| parent | [string](#string) |  |  |






<a name="animeshon.multimedia.v1alpha1.ReconcileChaptersResponse"></a>

### ReconcileChaptersResponse







<a name="animeshon.multimedia.v1alpha1.UpdateChapterRequest"></a>

### UpdateChapterRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| chapter | [Chapter](#animeshon.multimedia.v1alpha1.Chapter) |  | The chapter to update. |
| update_mask | [google.protobuf.FieldMask](#google.protobuf.FieldMask) |  | The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |





 


<a name="animeshon.multimedia.v1alpha1.Chapter.Type"></a>

### Chapter.Type


| Name | Number | Description |
| ---- | ------ | ----------- |
| TYPE_UNSPECIFIED | 0 | The default value. This value is used if the state is omitted. |
| REGULAR | 1 | The chapter is a regular canonical chapter. |
| EXTRA | 2 | The chapter is an extra chapter (e.g. specials, credits, etc.). |


 

 


<a name="animeshon.multimedia.v1alpha1.ChapterService"></a>

### ChapterService


| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| GetChapter | [GetChapterRequest](#animeshon.multimedia.v1alpha1.GetChapterRequest) | [Chapter](#animeshon.multimedia.v1alpha1.Chapter) |  |
| ListChapters | [ListChaptersRequest](#animeshon.multimedia.v1alpha1.ListChaptersRequest) | [ListChaptersResponse](#animeshon.multimedia.v1alpha1.ListChaptersResponse) |  |
| CreateChapter | [CreateChapterRequest](#animeshon.multimedia.v1alpha1.CreateChapterRequest) | [Chapter](#animeshon.multimedia.v1alpha1.Chapter) |  |
| BatchCreateChapters | [BatchCreateChaptersRequest](#animeshon.multimedia.v1alpha1.BatchCreateChaptersRequest) | [.google.longrunning.Operation](#google.longrunning.Operation) |  |
| UpdateChapter | [UpdateChapterRequest](#animeshon.multimedia.v1alpha1.UpdateChapterRequest) | [Chapter](#animeshon.multimedia.v1alpha1.Chapter) |  |
| DeleteChapter | [DeleteChapterRequest](#animeshon.multimedia.v1alpha1.DeleteChapterRequest) | [.google.protobuf.Empty](#google.protobuf.Empty) |  |
| ReconcileChapters | [ReconcileChaptersRequest](#animeshon.multimedia.v1alpha1.ReconcileChaptersRequest) | [.google.longrunning.Operation](#google.longrunning.Operation) | Reconcile chapters with the search and knowledge base. |

 



<a name="animeshon/multimedia/v1alpha1/episode.proto"></a>
<p align="right"><a href="#top">Top</a></p>

## animeshon/multimedia/v1alpha1/episode.proto



<a name="animeshon.multimedia.v1alpha1.BatchCreateEpisodesRequest"></a>

### BatchCreateEpisodesRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| requests | [BatchCreateEpisodesRequest.Request](#animeshon.multimedia.v1alpha1.BatchCreateEpisodesRequest.Request) | repeated | Individual create episode requests for this batch. |
| parent | [string](#string) |  | The parent this batch belongs to. |






<a name="animeshon.multimedia.v1alpha1.BatchCreateEpisodesRequest.Request"></a>

### BatchCreateEpisodesRequest.Request



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| episode | [Episode](#animeshon.multimedia.v1alpha1.Episode) |  | The episode to create. |
| idempotent_resource_id | [int64](#int64) |  | An idempotent identifier to be used as static resource id. |






<a name="animeshon.multimedia.v1alpha1.BatchCreateEpisodesResponse"></a>

### BatchCreateEpisodesResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| responses | [BatchCreateEpisodesResponse.Response](#animeshon.multimedia.v1alpha1.BatchCreateEpisodesResponse.Response) | repeated | Individual responses to create episode requests within the batch. |






<a name="animeshon.multimedia.v1alpha1.BatchCreateEpisodesResponse.Response"></a>

### BatchCreateEpisodesResponse.Response



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| episode | [Episode](#animeshon.multimedia.v1alpha1.Episode) |  | The newly created episode. |
| error | [google.rpc.Status](#google.rpc.Status) |  | If set, represents the error message for the operation. |






<a name="animeshon.multimedia.v1alpha1.CreateEpisodeRequest"></a>

### CreateEpisodeRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| parent | [string](#string) |  | The parent this episode belongs to. |
| episode | [Episode](#animeshon.multimedia.v1alpha1.Episode) |  | The episode to create. |
| idempotent_resource_id | [int64](#int64) |  | An idempotent identifier to be used as static resource id. |






<a name="animeshon.multimedia.v1alpha1.DeleteEpisodeRequest"></a>

### DeleteEpisodeRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the episode to delete. |






<a name="animeshon.multimedia.v1alpha1.Episode"></a>

### Episode



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The id of the episode. |
| cover_image | [string](#string) |  | The cover image of the episode. |
| banner_image | [string](#string) |  | The banner image of the episode. |
| title | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | The title of the episode localized in multiple languages. |
| synopsis | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | The synopsis of the episode localized in multiple languages. |
| description | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | The description of the episode localized in multiple languages. |
| type | [Episode.Type](#animeshon.multimedia.v1alpha1.Episode.Type) |  | The type of episode. |
| index | [int32](#int32) |  | The index of episode. |
| release_date | [google.type.Date](#google.type.Date) |  | The original release date of episode. |
| duration | [google.protobuf.Duration](#google.protobuf.Duration) |  | The original duration of the episode. |






<a name="animeshon.multimedia.v1alpha1.GetEpisodeRequest"></a>

### GetEpisodeRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the episode to retrieve. |






<a name="animeshon.multimedia.v1alpha1.ListEpisodesRequest"></a>

### ListEpisodesRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| parent | [string](#string) |  | The parent this episode belongs to. |
| page_size | [int32](#int32) |  | If unspecified, server will pick an appropriate default. |
| page_token | [string](#string) |  | The value returned from the previous call. |
| filter | [string](#string) |  | A filter to be applied to results. |






<a name="animeshon.multimedia.v1alpha1.ListEpisodesResponse"></a>

### ListEpisodesResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| episodes | [Episode](#animeshon.multimedia.v1alpha1.Episode) | repeated | The list of episodes. |
| next_page_token | [string](#string) |  | A token to retrieve next page of results. |






<a name="animeshon.multimedia.v1alpha1.ReconcileEpisodesRequest"></a>

### ReconcileEpisodesRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| parent | [string](#string) |  |  |






<a name="animeshon.multimedia.v1alpha1.ReconcileEpisodesResponse"></a>

### ReconcileEpisodesResponse







<a name="animeshon.multimedia.v1alpha1.UpdateEpisodeRequest"></a>

### UpdateEpisodeRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| episode | [Episode](#animeshon.multimedia.v1alpha1.Episode) |  | The episode to update. |
| update_mask | [google.protobuf.FieldMask](#google.protobuf.FieldMask) |  | The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |





 


<a name="animeshon.multimedia.v1alpha1.Episode.Type"></a>

### Episode.Type


| Name | Number | Description |
| ---- | ------ | ----------- |
| TYPE_UNSPECIFIED | 0 | The default value. This value is used if the state is omitted. |
| REGULAR | 1 | The episode is a regular canonical episode. |
| RECAP | 2 | The episode is a recap. |
| PARODY | 3 | The episode is a parody. |
| PROMO | 4 | The episode is a promo. |
| SPECIAL | 5 | The episode is a special. |
| OPENING_ENDING | 6 | The episode is an opening or ending. |
| OTHER | 7 | The episode is unclassified. |


 

 


<a name="animeshon.multimedia.v1alpha1.EpisodeService"></a>

### EpisodeService


| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| GetEpisode | [GetEpisodeRequest](#animeshon.multimedia.v1alpha1.GetEpisodeRequest) | [Episode](#animeshon.multimedia.v1alpha1.Episode) |  |
| ListEpisodes | [ListEpisodesRequest](#animeshon.multimedia.v1alpha1.ListEpisodesRequest) | [ListEpisodesResponse](#animeshon.multimedia.v1alpha1.ListEpisodesResponse) |  |
| CreateEpisode | [CreateEpisodeRequest](#animeshon.multimedia.v1alpha1.CreateEpisodeRequest) | [Episode](#animeshon.multimedia.v1alpha1.Episode) |  |
| BatchCreateEpisodes | [BatchCreateEpisodesRequest](#animeshon.multimedia.v1alpha1.BatchCreateEpisodesRequest) | [.google.longrunning.Operation](#google.longrunning.Operation) |  |
| UpdateEpisode | [UpdateEpisodeRequest](#animeshon.multimedia.v1alpha1.UpdateEpisodeRequest) | [Episode](#animeshon.multimedia.v1alpha1.Episode) |  |
| DeleteEpisode | [DeleteEpisodeRequest](#animeshon.multimedia.v1alpha1.DeleteEpisodeRequest) | [.google.protobuf.Empty](#google.protobuf.Empty) |  |
| ReconcileEpisodes | [ReconcileEpisodesRequest](#animeshon.multimedia.v1alpha1.ReconcileEpisodesRequest) | [.google.longrunning.Operation](#google.longrunning.Operation) | Reconcile episodes with the search and knowledge base. |

 



<a name="animeshon/multimedia/v1alpha1/graphic_novel.proto"></a>
<p align="right"><a href="#top">Top</a></p>

## animeshon/multimedia/v1alpha1/graphic_novel.proto



<a name="animeshon.multimedia.v1alpha1.CreateGraphicNovelRequest"></a>

### CreateGraphicNovelRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| graphic_novel | [GraphicNovel](#animeshon.multimedia.v1alpha1.GraphicNovel) |  | The graphic novel to create. |
| idempotent_resource_id | [int64](#int64) |  | An idempotent identifier to be used as static resource id. |






<a name="animeshon.multimedia.v1alpha1.DeleteGraphicNovelRequest"></a>

### DeleteGraphicNovelRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the graphic novel to delete. |






<a name="animeshon.multimedia.v1alpha1.GetGraphicNovelRequest"></a>

### GetGraphicNovelRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the graphic novel to retrieve. |






<a name="animeshon.multimedia.v1alpha1.GraphicNovel"></a>

### GraphicNovel



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The id of the graphic novel. |
| cover_image | [string](#string) |  | The cover image of the graphic novel. |
| banner_image | [string](#string) |  | The banner image of the graphic novel. |
| title | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | The title of the graphic novel localized in multiple languages. |
| synopsis | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | The synopsis of the graphic novel localized in multiple languages. |
| description | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | The description of the graphic novel localized in multiple languages. |
| type | [GraphicNovel.Type](#animeshon.multimedia.v1alpha1.GraphicNovel.Type) |  | The type of graphic novel. |
| release_date | [google.type.Date](#google.type.Date) |  | The original release date of graphic novel. |
| publishing_type | [PublishingType](#animeshon.multimedia.v1alpha1.PublishingType) |  | The original publishing type of this content. TODO: migrate this field to a more structured licensing history. |
| state | [State](#animeshon.multimedia.v1alpha1.State) |  | The current state of the graphic novel. |
| original | [bool](#bool) |  | Whether this content is an original work or a derivative work (parody). |






<a name="animeshon.multimedia.v1alpha1.ListGraphicNovelsRequest"></a>

### ListGraphicNovelsRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| page_size | [int32](#int32) |  | If unspecified, server will pick an appropriate default. |
| page_token | [string](#string) |  | The value returned from the previous call. |
| filter | [string](#string) |  | A filter to be applied to results. |






<a name="animeshon.multimedia.v1alpha1.ListGraphicNovelsResponse"></a>

### ListGraphicNovelsResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| graphic_novels | [GraphicNovel](#animeshon.multimedia.v1alpha1.GraphicNovel) | repeated | The list of graphic novels. |
| next_page_token | [string](#string) |  | A token to retrieve next page of results. |






<a name="animeshon.multimedia.v1alpha1.ReconcileGraphicNovelsRequest"></a>

### ReconcileGraphicNovelsRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the graphic novel to reconcile. Use the wildcard `graphicNovels/-` to reconcile all graphic novels. |






<a name="animeshon.multimedia.v1alpha1.ReconcileGraphicNovelsResponse"></a>

### ReconcileGraphicNovelsResponse







<a name="animeshon.multimedia.v1alpha1.UpdateGraphicNovelRequest"></a>

### UpdateGraphicNovelRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| graphic_novel | [GraphicNovel](#animeshon.multimedia.v1alpha1.GraphicNovel) |  | The graphic novel to update. |
| update_mask | [google.protobuf.FieldMask](#google.protobuf.FieldMask) |  | The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |





 


<a name="animeshon.multimedia.v1alpha1.GraphicNovel.Type"></a>

### GraphicNovel.Type


| Name | Number | Description |
| ---- | ------ | ----------- |
| TYPE_UNSPECIFIED | 0 | The default value. This value is used if the state is omitted. |
| MANGA | 1 |  |
| ONE_SHOT | 2 |  |
| MANHUA | 3 |  |
| MANHWA | 4 |  |
| OEL | 5 |  |
| WEB_COMIC | 6 |  |
| YON_KOMA | 7 |  |
| OTHER | 8 |  |


 

 


<a name="animeshon.multimedia.v1alpha1.GraphicNovelService"></a>

### GraphicNovelService


| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| GetGraphicNovel | [GetGraphicNovelRequest](#animeshon.multimedia.v1alpha1.GetGraphicNovelRequest) | [GraphicNovel](#animeshon.multimedia.v1alpha1.GraphicNovel) |  |
| ListGraphicNovels | [ListGraphicNovelsRequest](#animeshon.multimedia.v1alpha1.ListGraphicNovelsRequest) | [ListGraphicNovelsResponse](#animeshon.multimedia.v1alpha1.ListGraphicNovelsResponse) |  |
| CreateGraphicNovel | [CreateGraphicNovelRequest](#animeshon.multimedia.v1alpha1.CreateGraphicNovelRequest) | [GraphicNovel](#animeshon.multimedia.v1alpha1.GraphicNovel) |  |
| UpdateGraphicNovel | [UpdateGraphicNovelRequest](#animeshon.multimedia.v1alpha1.UpdateGraphicNovelRequest) | [GraphicNovel](#animeshon.multimedia.v1alpha1.GraphicNovel) |  |
| DeleteGraphicNovel | [DeleteGraphicNovelRequest](#animeshon.multimedia.v1alpha1.DeleteGraphicNovelRequest) | [.google.protobuf.Empty](#google.protobuf.Empty) |  |
| ReconcileGraphicNovels | [ReconcileGraphicNovelsRequest](#animeshon.multimedia.v1alpha1.ReconcileGraphicNovelsRequest) | [.google.longrunning.Operation](#google.longrunning.Operation) | Reconcile graphic novels with the search and knowledge base. |

 



<a name="animeshon/multimedia/v1alpha1/visual_novel.proto"></a>
<p align="right"><a href="#top">Top</a></p>

## animeshon/multimedia/v1alpha1/visual_novel.proto



<a name="animeshon.multimedia.v1alpha1.CreateVisualNovelRequest"></a>

### CreateVisualNovelRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| visual_novel | [VisualNovel](#animeshon.multimedia.v1alpha1.VisualNovel) |  | The visual novel to create. |
| idempotent_resource_id | [int64](#int64) |  | An idempotent identifier to be used as static resource id. |






<a name="animeshon.multimedia.v1alpha1.DeleteVisualNovelRequest"></a>

### DeleteVisualNovelRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the visual novel to delete. |






<a name="animeshon.multimedia.v1alpha1.GetVisualNovelRequest"></a>

### GetVisualNovelRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the visual novel to retrieve. |






<a name="animeshon.multimedia.v1alpha1.ListVisualNovelsRequest"></a>

### ListVisualNovelsRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| page_size | [int32](#int32) |  | If unspecified, server will pick an appropriate default. |
| page_token | [string](#string) |  | The value returned from the previous call. |
| filter | [string](#string) |  | A filter to be applied to results. |






<a name="animeshon.multimedia.v1alpha1.ListVisualNovelsResponse"></a>

### ListVisualNovelsResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| visual_novels | [VisualNovel](#animeshon.multimedia.v1alpha1.VisualNovel) | repeated | The list of visual novels. |
| next_page_token | [string](#string) |  | A token to retrieve next page of results. |






<a name="animeshon.multimedia.v1alpha1.ReconcileVisualNovelsRequest"></a>

### ReconcileVisualNovelsRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the visual novel to reconcile. Use the wildcard `visualNovels/-` to reconcile all visual novels. |






<a name="animeshon.multimedia.v1alpha1.ReconcileVisualNovelsResponse"></a>

### ReconcileVisualNovelsResponse







<a name="animeshon.multimedia.v1alpha1.UpdateVisualNovelRequest"></a>

### UpdateVisualNovelRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| visual_novel | [VisualNovel](#animeshon.multimedia.v1alpha1.VisualNovel) |  | The visual novel to update. |
| update_mask | [google.protobuf.FieldMask](#google.protobuf.FieldMask) |  | The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |






<a name="animeshon.multimedia.v1alpha1.VisualNovel"></a>

### VisualNovel



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The id of the visual novel. |
| cover_image | [string](#string) |  | The cover image of the visual novel. |
| banner_image | [string](#string) |  | The banner image of the visual novel. |
| title | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | The title of the visual novel localized in multiple languages. |
| synopsis | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | The synopsis of the visual novel localized in multiple languages. |
| description | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | The description of the visual novel localized in multiple languages. |
| type | [VisualNovel.Type](#animeshon.multimedia.v1alpha1.VisualNovel.Type) |  | The type of visual novel. |
| release_date | [google.type.Date](#google.type.Date) |  | The original release date of visual novel. |
| publishing_type | [PublishingType](#animeshon.multimedia.v1alpha1.PublishingType) |  | The original publishing type of this content. TODO: migrate this field to a more structured licensing history. |
| state | [State](#animeshon.multimedia.v1alpha1.State) |  | The current state of the light novel. |
| original | [bool](#bool) |  | Whether this content is an original work or a derivative work (parody). |
| length | [VisualNovel.PlayLength](#animeshon.multimedia.v1alpha1.VisualNovel.PlayLength) |  | The average duration of the visual novel. |





 


<a name="animeshon.multimedia.v1alpha1.VisualNovel.PlayLength"></a>

### VisualNovel.PlayLength


| Name | Number | Description |
| ---- | ------ | ----------- |
| PLAY_LENGTH_UNSPECIFIED | 0 | The default value. This value is used if the state is omitted. |
| VERY_SHORT | 1 |  |
| SHORT | 2 |  |
| MEDIUM | 3 |  |
| LONG | 4 |  |
| VERY_LONG | 5 |  |



<a name="animeshon.multimedia.v1alpha1.VisualNovel.Type"></a>

### VisualNovel.Type


| Name | Number | Description |
| ---- | ------ | ----------- |
| TYPE_UNSPECIFIED | 0 | The default value. This value is used if the state is omitted. |


 

 


<a name="animeshon.multimedia.v1alpha1.VisualNovelService"></a>

### VisualNovelService


| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| GetVisualNovel | [GetVisualNovelRequest](#animeshon.multimedia.v1alpha1.GetVisualNovelRequest) | [VisualNovel](#animeshon.multimedia.v1alpha1.VisualNovel) |  |
| ListVisualNovels | [ListVisualNovelsRequest](#animeshon.multimedia.v1alpha1.ListVisualNovelsRequest) | [ListVisualNovelsResponse](#animeshon.multimedia.v1alpha1.ListVisualNovelsResponse) |  |
| CreateVisualNovel | [CreateVisualNovelRequest](#animeshon.multimedia.v1alpha1.CreateVisualNovelRequest) | [VisualNovel](#animeshon.multimedia.v1alpha1.VisualNovel) |  |
| UpdateVisualNovel | [UpdateVisualNovelRequest](#animeshon.multimedia.v1alpha1.UpdateVisualNovelRequest) | [VisualNovel](#animeshon.multimedia.v1alpha1.VisualNovel) |  |
| DeleteVisualNovel | [DeleteVisualNovelRequest](#animeshon.multimedia.v1alpha1.DeleteVisualNovelRequest) | [.google.protobuf.Empty](#google.protobuf.Empty) |  |
| ReconcileVisualNovels | [ReconcileVisualNovelsRequest](#animeshon.multimedia.v1alpha1.ReconcileVisualNovelsRequest) | [.google.longrunning.Operation](#google.longrunning.Operation) | Reconcile visual novels with the search and knowledge base. |

 



<a name="animeshon/multimedia/v1alpha1/light_novel.proto"></a>
<p align="right"><a href="#top">Top</a></p>

## animeshon/multimedia/v1alpha1/light_novel.proto



<a name="animeshon.multimedia.v1alpha1.CreateLightNovelRequest"></a>

### CreateLightNovelRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| light_novel | [LightNovel](#animeshon.multimedia.v1alpha1.LightNovel) |  | The light novel to create. |
| idempotent_resource_id | [int64](#int64) |  | An idempotent identifier to be used as static resource id. |






<a name="animeshon.multimedia.v1alpha1.DeleteLightNovelRequest"></a>

### DeleteLightNovelRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the light novel to delete. |






<a name="animeshon.multimedia.v1alpha1.GetLightNovelRequest"></a>

### GetLightNovelRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the light novel to retrieve. |






<a name="animeshon.multimedia.v1alpha1.LightNovel"></a>

### LightNovel



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The id of the light novel. |
| cover_image | [string](#string) |  | The cover image of the light novel. |
| banner_image | [string](#string) |  | The banner image of the light novel. |
| title | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | The title of the light novel localized in multiple languages. |
| synopsis | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | The synopsis of the light novel localized in multiple languages. |
| description | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | The description of the light novel localized in multiple languages. |
| type | [LightNovel.Type](#animeshon.multimedia.v1alpha1.LightNovel.Type) |  | The type of light novel. |
| release_date | [google.type.Date](#google.type.Date) |  | The original release date of light novel. |
| publishing_type | [PublishingType](#animeshon.multimedia.v1alpha1.PublishingType) |  | The original publishing type of this content. TODO: migrate this field to a more structured licensing history. |
| state | [State](#animeshon.multimedia.v1alpha1.State) |  | The current state of the light novel. |
| original | [bool](#bool) |  | Whether this content is an original work or a derivative work (parody). |






<a name="animeshon.multimedia.v1alpha1.ListLightNovelsRequest"></a>

### ListLightNovelsRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| page_size | [int32](#int32) |  | If unspecified, server will pick an appropriate default. |
| page_token | [string](#string) |  | The value returned from the previous call. |
| filter | [string](#string) |  | A filter to be applied to results. |






<a name="animeshon.multimedia.v1alpha1.ListLightNovelsResponse"></a>

### ListLightNovelsResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| light_novels | [LightNovel](#animeshon.multimedia.v1alpha1.LightNovel) | repeated | The list of light novels. |
| next_page_token | [string](#string) |  | A token to retrieve next page of results. |






<a name="animeshon.multimedia.v1alpha1.ReconcileLightNovelsRequest"></a>

### ReconcileLightNovelsRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the light novel to reconcile. Use the wildcard `lightNovels/-` to reconcile all light novels. |






<a name="animeshon.multimedia.v1alpha1.ReconcileLightNovelsResponse"></a>

### ReconcileLightNovelsResponse







<a name="animeshon.multimedia.v1alpha1.UpdateLightNovelRequest"></a>

### UpdateLightNovelRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| light_novel | [LightNovel](#animeshon.multimedia.v1alpha1.LightNovel) |  | The light novel to update. |
| update_mask | [google.protobuf.FieldMask](#google.protobuf.FieldMask) |  | The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |





 


<a name="animeshon.multimedia.v1alpha1.LightNovel.Type"></a>

### LightNovel.Type


| Name | Number | Description |
| ---- | ------ | ----------- |
| TYPE_UNSPECIFIED | 0 | The default value. This value is used if the state is omitted. |


 

 


<a name="animeshon.multimedia.v1alpha1.LightNovelService"></a>

### LightNovelService


| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| GetLightNovel | [GetLightNovelRequest](#animeshon.multimedia.v1alpha1.GetLightNovelRequest) | [LightNovel](#animeshon.multimedia.v1alpha1.LightNovel) |  |
| ListLightNovels | [ListLightNovelsRequest](#animeshon.multimedia.v1alpha1.ListLightNovelsRequest) | [ListLightNovelsResponse](#animeshon.multimedia.v1alpha1.ListLightNovelsResponse) |  |
| CreateLightNovel | [CreateLightNovelRequest](#animeshon.multimedia.v1alpha1.CreateLightNovelRequest) | [LightNovel](#animeshon.multimedia.v1alpha1.LightNovel) |  |
| UpdateLightNovel | [UpdateLightNovelRequest](#animeshon.multimedia.v1alpha1.UpdateLightNovelRequest) | [LightNovel](#animeshon.multimedia.v1alpha1.LightNovel) |  |
| DeleteLightNovel | [DeleteLightNovelRequest](#animeshon.multimedia.v1alpha1.DeleteLightNovelRequest) | [.google.protobuf.Empty](#google.protobuf.Empty) |  |
| ReconcileLightNovels | [ReconcileLightNovelsRequest](#animeshon.multimedia.v1alpha1.ReconcileLightNovelsRequest) | [.google.longrunning.Operation](#google.longrunning.Operation) | Reconcile light novels with the search and knowledge base. |

 



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

