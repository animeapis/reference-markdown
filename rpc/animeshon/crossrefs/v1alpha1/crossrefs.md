# Protocol Documentation
<a name="top"></a>

## Table of Contents

- [animeshon/crossrefs/v1alpha1/crossrefs.proto](#animeshon/crossrefs/v1alpha1/crossrefs.proto)
    - [AnalyzeCrossRefRequest](#animeshon.crossrefs.v1alpha1.AnalyzeCrossRefRequest)
    - [AnalyzeCrossRefRequest.AnalyzeCrossRefConfig](#animeshon.crossrefs.v1alpha1.AnalyzeCrossRefRequest.AnalyzeCrossRefConfig)
    - [AnalyzeCrossRefRequest.AnalyzeCrossRefConfig.OptsEntry](#animeshon.crossrefs.v1alpha1.AnalyzeCrossRefRequest.AnalyzeCrossRefConfig.OptsEntry)
    - [AnalyzeCrossRefRequest.AnalyzeCrossRefNamespaceConfig](#animeshon.crossrefs.v1alpha1.AnalyzeCrossRefRequest.AnalyzeCrossRefNamespaceConfig)
    - [AnalyzeCrossRefRequest.AnalyzeCrossRefTargetConfig](#animeshon.crossrefs.v1alpha1.AnalyzeCrossRefRequest.AnalyzeCrossRefTargetConfig)
    - [AnalyzeCrossRefRequest.AnalyzeCrossRefTargetConfig.NamespacesEntry](#animeshon.crossrefs.v1alpha1.AnalyzeCrossRefRequest.AnalyzeCrossRefTargetConfig.NamespacesEntry)
    - [AnalyzeCrossRefRequest.TargetKindsEntry](#animeshon.crossrefs.v1alpha1.AnalyzeCrossRefRequest.TargetKindsEntry)
    - [AnalyzeCrossRefsResponse](#animeshon.crossrefs.v1alpha1.AnalyzeCrossRefsResponse)
    - [AnalyzeParodiesResponse](#animeshon.crossrefs.v1alpha1.AnalyzeParodiesResponse)
    - [BatchCreateCrossRefsRequest](#animeshon.crossrefs.v1alpha1.BatchCreateCrossRefsRequest)
    - [BatchCreateCrossRefsResponse](#animeshon.crossrefs.v1alpha1.BatchCreateCrossRefsResponse)
    - [CountCrossRefsRequest](#animeshon.crossrefs.v1alpha1.CountCrossRefsRequest)
    - [CountCrossRefsResponse](#animeshon.crossrefs.v1alpha1.CountCrossRefsResponse)
    - [CreateCrossRefRequest](#animeshon.crossrefs.v1alpha1.CreateCrossRefRequest)
    - [CrossRef](#animeshon.crossrefs.v1alpha1.CrossRef)
    - [CrossRefEdge](#animeshon.crossrefs.v1alpha1.CrossRefEdge)
    - [CrossRefsFilterRequest](#animeshon.crossrefs.v1alpha1.CrossRefsFilterRequest)
    - [ExpandUniverseRequest](#animeshon.crossrefs.v1alpha1.ExpandUniverseRequest)
    - [ExpandUniverseResponse](#animeshon.crossrefs.v1alpha1.ExpandUniverseResponse)
    - [ExportCrossRefRequest](#animeshon.crossrefs.v1alpha1.ExportCrossRefRequest)
    - [ExportCrossRefsResponse](#animeshon.crossrefs.v1alpha1.ExportCrossRefsResponse)
    - [ExportParodiesResponse](#animeshon.crossrefs.v1alpha1.ExportParodiesResponse)
    - [GetCrossRefRequest](#animeshon.crossrefs.v1alpha1.GetCrossRefRequest)
    - [GetUniverseRequest](#animeshon.crossrefs.v1alpha1.GetUniverseRequest)
    - [GetWormholeRequest](#animeshon.crossrefs.v1alpha1.GetWormholeRequest)
    - [ImportCrossRefRequest](#animeshon.crossrefs.v1alpha1.ImportCrossRefRequest)
    - [ImportCrossRefRequest.OptsEntry](#animeshon.crossrefs.v1alpha1.ImportCrossRefRequest.OptsEntry)
    - [ImportCrossRefsResponse](#animeshon.crossrefs.v1alpha1.ImportCrossRefsResponse)
    - [InitializeCrossRefsResponse](#animeshon.crossrefs.v1alpha1.InitializeCrossRefsResponse)
    - [ListCrossRefsRequest](#animeshon.crossrefs.v1alpha1.ListCrossRefsRequest)
    - [ListCrossRefsResponse](#animeshon.crossrefs.v1alpha1.ListCrossRefsResponse)
    - [ListWormholeCrossRefsRequest](#animeshon.crossrefs.v1alpha1.ListWormholeCrossRefsRequest)
    - [ListWormholeCrossRefsResponse](#animeshon.crossrefs.v1alpha1.ListWormholeCrossRefsResponse)
    - [OperationMetadata](#animeshon.crossrefs.v1alpha1.OperationMetadata)
    - [Universe](#animeshon.crossrefs.v1alpha1.Universe)
    - [UpdateCrossRefRequest](#animeshon.crossrefs.v1alpha1.UpdateCrossRefRequest)
    - [UpdateCrossRefResponse](#animeshon.crossrefs.v1alpha1.UpdateCrossRefResponse)
    - [UpdateUniverseRequest](#animeshon.crossrefs.v1alpha1.UpdateUniverseRequest)
    - [Wormhole](#animeshon.crossrefs.v1alpha1.Wormhole)
    - [Wormhole.Text](#animeshon.crossrefs.v1alpha1.Wormhole.Text)
  
    - [ExportCrossRefRequest.Target](#animeshon.crossrefs.v1alpha1.ExportCrossRefRequest.Target)
  
    - [Referrer](#animeshon.crossrefs.v1alpha1.Referrer)
  
- [Scalar Value Types](#scalar-value-types)



<a name="animeshon/crossrefs/v1alpha1/crossrefs.proto"></a>
<p align="right"><a href="#top">Top</a></p>

## animeshon/crossrefs/v1alpha1/crossrefs.proto



<a name="animeshon.crossrefs.v1alpha1.AnalyzeCrossRefRequest"></a>

### AnalyzeCrossRefRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| config | [AnalyzeCrossRefRequest.AnalyzeCrossRefConfig](#animeshon.crossrefs.v1alpha1.AnalyzeCrossRefRequest.AnalyzeCrossRefConfig) |  | Global configuration |
| target_kinds | [AnalyzeCrossRefRequest.TargetKindsEntry](#animeshon.crossrefs.v1alpha1.AnalyzeCrossRefRequest.TargetKindsEntry) | repeated | Kind configurations |






<a name="animeshon.crossrefs.v1alpha1.AnalyzeCrossRefRequest.AnalyzeCrossRefConfig"></a>

### AnalyzeCrossRefRequest.AnalyzeCrossRefConfig



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| tollerance | [int32](#int32) |  | Tollerance of the match in pct |
| opts | [AnalyzeCrossRefRequest.AnalyzeCrossRefConfig.OptsEntry](#animeshon.crossrefs.v1alpha1.AnalyzeCrossRefRequest.AnalyzeCrossRefConfig.OptsEntry) | repeated | Map of all options for the analysis |






<a name="animeshon.crossrefs.v1alpha1.AnalyzeCrossRefRequest.AnalyzeCrossRefConfig.OptsEntry"></a>

### AnalyzeCrossRefRequest.AnalyzeCrossRefConfig.OptsEntry



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| key | [string](#string) |  |  |
| value | [bool](#bool) |  |  |






<a name="animeshon.crossrefs.v1alpha1.AnalyzeCrossRefRequest.AnalyzeCrossRefNamespaceConfig"></a>

### AnalyzeCrossRefRequest.AnalyzeCrossRefNamespaceConfig



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| namespace | [string](#string) |  | Namespace to analyze |
| config | [AnalyzeCrossRefRequest.AnalyzeCrossRefConfig](#animeshon.crossrefs.v1alpha1.AnalyzeCrossRefRequest.AnalyzeCrossRefConfig) |  | Optional Namespace specific configuration |






<a name="animeshon.crossrefs.v1alpha1.AnalyzeCrossRefRequest.AnalyzeCrossRefTargetConfig"></a>

### AnalyzeCrossRefRequest.AnalyzeCrossRefTargetConfig



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| target_kind | [string](#string) |  | Kind to analyze |
| config | [AnalyzeCrossRefRequest.AnalyzeCrossRefConfig](#animeshon.crossrefs.v1alpha1.AnalyzeCrossRefRequest.AnalyzeCrossRefConfig) |  | Optional Target specific configuration |
| namespaces | [AnalyzeCrossRefRequest.AnalyzeCrossRefTargetConfig.NamespacesEntry](#animeshon.crossrefs.v1alpha1.AnalyzeCrossRefRequest.AnalyzeCrossRefTargetConfig.NamespacesEntry) | repeated | Namespace configurations |






<a name="animeshon.crossrefs.v1alpha1.AnalyzeCrossRefRequest.AnalyzeCrossRefTargetConfig.NamespacesEntry"></a>

### AnalyzeCrossRefRequest.AnalyzeCrossRefTargetConfig.NamespacesEntry



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| key | [string](#string) |  |  |
| value | [AnalyzeCrossRefRequest.AnalyzeCrossRefNamespaceConfig](#animeshon.crossrefs.v1alpha1.AnalyzeCrossRefRequest.AnalyzeCrossRefNamespaceConfig) |  |  |






<a name="animeshon.crossrefs.v1alpha1.AnalyzeCrossRefRequest.TargetKindsEntry"></a>

### AnalyzeCrossRefRequest.TargetKindsEntry



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| key | [string](#string) |  |  |
| value | [AnalyzeCrossRefRequest.AnalyzeCrossRefTargetConfig](#animeshon.crossrefs.v1alpha1.AnalyzeCrossRefRequest.AnalyzeCrossRefTargetConfig) |  |  |






<a name="animeshon.crossrefs.v1alpha1.AnalyzeCrossRefsResponse"></a>

### AnalyzeCrossRefsResponse
TODO(christian-roggia): this is a workaround to solve the issue of GAPIC
CLI where broken code is generated if google.protobuf.Empty is used in the
response_type of longrunning operations.






<a name="animeshon.crossrefs.v1alpha1.AnalyzeParodiesResponse"></a>

### AnalyzeParodiesResponse







<a name="animeshon.crossrefs.v1alpha1.BatchCreateCrossRefsRequest"></a>

### BatchCreateCrossRefsRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| crossrefs | [CrossRef](#animeshon.crossrefs.v1alpha1.CrossRef) | repeated |  |






<a name="animeshon.crossrefs.v1alpha1.BatchCreateCrossRefsResponse"></a>

### BatchCreateCrossRefsResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| crossrefs | [CrossRef](#animeshon.crossrefs.v1alpha1.CrossRef) | repeated | The list of crossrefs to create. |






<a name="animeshon.crossrefs.v1alpha1.CountCrossRefsRequest"></a>

### CountCrossRefsRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| filter | [CrossRefsFilterRequest](#animeshon.crossrefs.v1alpha1.CrossRefsFilterRequest) |  | A filter to be applied to results. |






<a name="animeshon.crossrefs.v1alpha1.CountCrossRefsResponse"></a>

### CountCrossRefsResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| count | [int32](#int32) |  |  |






<a name="animeshon.crossrefs.v1alpha1.CreateCrossRefRequest"></a>

### CreateCrossRefRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| crossref | [CrossRef](#animeshon.crossrefs.v1alpha1.CrossRef) |  |  |






<a name="animeshon.crossrefs.v1alpha1.CrossRef"></a>

### CrossRef



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The resource name of the crossref. |
| root | [string](#string) |  | root entity which generated the crossreference. |
| etag | [string](#string) |  | version control. |
| verified | [bool](#bool) |  | if verified, the crossreference has been generated by a trusty process or verified by an operator |
| operator | [string](#string) |  | last operator which edited the crossreference |
| create_time | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | creation time |
| update_time | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | update time |
| edges | [CrossRefEdge](#animeshon.crossrefs.v1alpha1.CrossRefEdge) | repeated | all edges of the crossreference |






<a name="animeshon.crossrefs.v1alpha1.CrossRefEdge"></a>

### CrossRefEdge



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  |  |
| state | [int32](#int32) |  |  |






<a name="animeshon.crossrefs.v1alpha1.CrossRefsFilterRequest"></a>

### CrossRefsFilterRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| prefix | [string](#string) |  | specifies the prefix of the CrossRefs name to search in |
| pendingOnly | [bool](#bool) |  | if true only crossreferences with pendings are returned |






<a name="animeshon.crossrefs.v1alpha1.ExpandUniverseRequest"></a>

### ExpandUniverseRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The universe to expand. |
| depth_limit | [int32](#int32) |  | The maximum depth to expand. |
| filter | [string](#string) |  | The filter to use. Accepted values are CONTENT and CHARACTER. |






<a name="animeshon.crossrefs.v1alpha1.ExpandUniverseResponse"></a>

### ExpandUniverseResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The resource name of the requested universe. |
| payload | [bytes](#bytes) |  | TODO(christian-roggia): resources should be available through protobuf messages. |






<a name="animeshon.crossrefs.v1alpha1.ExportCrossRefRequest"></a>

### ExportCrossRefRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| target | [ExportCrossRefRequest.Target](#animeshon.crossrefs.v1alpha1.ExportCrossRefRequest.Target) |  |  |
| prefix | [string](#string) |  | Prefix to restrict the crossrefs to export to a specific subset |






<a name="animeshon.crossrefs.v1alpha1.ExportCrossRefsResponse"></a>

### ExportCrossRefsResponse







<a name="animeshon.crossrefs.v1alpha1.ExportParodiesResponse"></a>

### ExportParodiesResponse







<a name="animeshon.crossrefs.v1alpha1.GetCrossRefRequest"></a>

### GetCrossRefRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The resource name of the requested crossref. |






<a name="animeshon.crossrefs.v1alpha1.GetUniverseRequest"></a>

### GetUniverseRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The resource name of the requested universe. |






<a name="animeshon.crossrefs.v1alpha1.GetWormholeRequest"></a>

### GetWormholeRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  |  |






<a name="animeshon.crossrefs.v1alpha1.ImportCrossRefRequest"></a>

### ImportCrossRefRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| opts | [ImportCrossRefRequest.OptsEntry](#animeshon.crossrefs.v1alpha1.ImportCrossRefRequest.OptsEntry) | repeated | Map of all options for the import |






<a name="animeshon.crossrefs.v1alpha1.ImportCrossRefRequest.OptsEntry"></a>

### ImportCrossRefRequest.OptsEntry



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| key | [string](#string) |  |  |
| value | [bool](#bool) |  |  |






<a name="animeshon.crossrefs.v1alpha1.ImportCrossRefsResponse"></a>

### ImportCrossRefsResponse







<a name="animeshon.crossrefs.v1alpha1.InitializeCrossRefsResponse"></a>

### InitializeCrossRefsResponse







<a name="animeshon.crossrefs.v1alpha1.ListCrossRefsRequest"></a>

### ListCrossRefsRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| page_size | [int32](#int32) |  | The maximum number of users to return. Server may return fewer users than requested. The maximum page_size is 100 If unspecified, server will pick an appropriate default. |
| page_token | [string](#string) |  | The value returned from the previous call. |
| filter | [CrossRefsFilterRequest](#animeshon.crossrefs.v1alpha1.CrossRefsFilterRequest) |  | A filter to be applied to results. |






<a name="animeshon.crossrefs.v1alpha1.ListCrossRefsResponse"></a>

### ListCrossRefsResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| crossrefs | [CrossRef](#animeshon.crossrefs.v1alpha1.CrossRef) | repeated | The list of crossrefs. |
| next_page_token | [string](#string) |  | A token to retrieve next page of results. |






<a name="animeshon.crossrefs.v1alpha1.ListWormholeCrossRefsRequest"></a>

### ListWormholeCrossRefsRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  |  |
| withApproved | [bool](#bool) |  | search wormhole entity in approved edges |
| withPending | [bool](#bool) |  | search wormhole entity in pending edges |
| withPartial | [bool](#bool) |  | search wormhole entity in partial edges |
| withRejected | [bool](#bool) |  | search wormhole entity in rejected edges |
| crossRefsExclusion | [string](#string) | repeated | list of CrossRefs to exclude |
| prefix | [string](#string) |  | prefix of the CrossRefs name to search |






<a name="animeshon.crossrefs.v1alpha1.ListWormholeCrossRefsResponse"></a>

### ListWormholeCrossRefsResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| crossrefs | [CrossRef](#animeshon.crossrefs.v1alpha1.CrossRef) | repeated | The list of crossrefs. |






<a name="animeshon.crossrefs.v1alpha1.OperationMetadata"></a>

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
| step_count | [int32](#int32) |  | Output only. |
| step_progress | [int32](#int32) |  | Output only. |
| item_count | [int32](#int32) |  | Output only. |
| item_progress | [int32](#int32) |  | Output only. |






<a name="animeshon.crossrefs.v1alpha1.Universe"></a>

### Universe
TODO(christian-roggia): move the universe together with all other resources.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The resource name of the universe. |
| payload | [bytes](#bytes) |  | TODO(christian-roggia): resources should be available through protobuf messages. |






<a name="animeshon.crossrefs.v1alpha1.UpdateCrossRefRequest"></a>

### UpdateCrossRefRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| crossref | [CrossRef](#animeshon.crossrefs.v1alpha1.CrossRef) |  | The crossref to update. |
| update_mask | [google.protobuf.FieldMask](#google.protobuf.FieldMask) |  | The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |






<a name="animeshon.crossrefs.v1alpha1.UpdateCrossRefResponse"></a>

### UpdateCrossRefResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| crossrefs | [CrossRef](#animeshon.crossrefs.v1alpha1.CrossRef) | repeated | All CrossRef involved in the update |






<a name="animeshon.crossrefs.v1alpha1.UpdateUniverseRequest"></a>

### UpdateUniverseRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| universe | [Universe](#animeshon.crossrefs.v1alpha1.Universe) |  | The universe to update. |
| update_mask | [google.protobuf.FieldMask](#google.protobuf.FieldMask) |  | The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |






<a name="animeshon.crossrefs.v1alpha1.Wormhole"></a>

### Wormhole



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  |  |
| names | [Wormhole.Text](#animeshon.crossrefs.v1alpha1.Wormhole.Text) | repeated | The names of te content |
| aliases | [Wormhole.Text](#animeshon.crossrefs.v1alpha1.Wormhole.Text) | repeated | The aliases of te content |
| image | [bytes](#bytes) |  | raw bytes of image |
| image_url | [string](#string) |  | url of the image |
| type | [string](#string) |  | type of the content |
| subtype | [string](#string) |  | subtype of the content |
| external_url | [string](#string) |  | external url of the content |
| publishing_type | [string](#string) |  | type of publication |
| is_parody | [bool](#bool) |  | the content is parody of another content |
| identifier | [string](#string) |  | identifier |
| date | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | most significant date |
| parent_name | [string](#string) |  | parent&#39;s resource name useful for chapters and episodes to know which content it refers |
| parent_external_url | [string](#string) |  | prant external url |






<a name="animeshon.crossrefs.v1alpha1.Wormhole.Text"></a>

### Wormhole.Text



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| text | [string](#string) |  |  |
| localization | [string](#string) |  |  |





 


<a name="animeshon.crossrefs.v1alpha1.ExportCrossRefRequest.Target"></a>

### ExportCrossRefRequest.Target
Determine the target of the export.
Full means storage &#43; migration
Storage means only persinstent stogare
Migration means notify the migrato to perform the data consolidation

| Name | Number | Description |
| ---- | ------ | ----------- |
| FULL | 0 |  |
| STORAGE | 1 |  |
| MIGRATOR | 2 |  |


 

 


<a name="animeshon.crossrefs.v1alpha1.Referrer"></a>

### Referrer


| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| GetCrossRef | [GetCrossRefRequest](#animeshon.crossrefs.v1alpha1.GetCrossRefRequest) | [CrossRef](#animeshon.crossrefs.v1alpha1.CrossRef) | GetCrossRef returns a crossref. |
| ListCrossRefs | [ListCrossRefsRequest](#animeshon.crossrefs.v1alpha1.ListCrossRefsRequest) | [ListCrossRefsResponse](#animeshon.crossrefs.v1alpha1.ListCrossRefsResponse) |  |
| CreateCrossRef | [CreateCrossRefRequest](#animeshon.crossrefs.v1alpha1.CreateCrossRefRequest) | [CrossRef](#animeshon.crossrefs.v1alpha1.CrossRef) | CreateCrossRef creates a new crossref. |
| BatchCreateCrossRefs | [BatchCreateCrossRefsRequest](#animeshon.crossrefs.v1alpha1.BatchCreateCrossRefsRequest) | [BatchCreateCrossRefsResponse](#animeshon.crossrefs.v1alpha1.BatchCreateCrossRefsResponse) | BatchCreateCrossRefs creates new crossrefs in batch. The limit is of 10 crossreferences and it&#39;s blocking. It ensures that the crossreferences are created in the database but not propagated to the other services |
| UpdateCrossRef | [UpdateCrossRefRequest](#animeshon.crossrefs.v1alpha1.UpdateCrossRefRequest) | [UpdateCrossRefResponse](#animeshon.crossrefs.v1alpha1.UpdateCrossRefResponse) |  |
| CountCrossRefs | [CountCrossRefsRequest](#animeshon.crossrefs.v1alpha1.CountCrossRefsRequest) | [CountCrossRefsResponse](#animeshon.crossrefs.v1alpha1.CountCrossRefsResponse) |  |
| AnalyzeCrossRefs | [AnalyzeCrossRefRequest](#animeshon.crossrefs.v1alpha1.AnalyzeCrossRefRequest) | [.google.longrunning.Operation](#google.longrunning.Operation) | Analyzes and proposes new cross-references according to their similarity. |
| ImportCrossRefs | [ImportCrossRefRequest](#animeshon.crossrefs.v1alpha1.ImportCrossRefRequest) | [.google.longrunning.Operation](#google.longrunning.Operation) | Imports already existing cross-references from third-parties. |
| ExportCrossRefs | [ExportCrossRefRequest](#animeshon.crossrefs.v1alpha1.ExportCrossRefRequest) | [.google.longrunning.Operation](#google.longrunning.Operation) | Exports the cross-references to Cloud Pub/Sub for a full synchronization. This operation is usually called after a new import with a clean database. |
| InitializeCrossRefs | [.google.protobuf.Empty](#google.protobuf.Empty) | [.google.longrunning.Operation](#google.longrunning.Operation) | Initialize the cross-references using specific namespaces for each kind. This operation first analyzes the entities meeting the kind and namespace precondition to match new entities with existing ones |
| AnalyzeParodies | [.google.protobuf.Empty](#google.protobuf.Empty) | [.google.longrunning.Operation](#google.longrunning.Operation) |  |
| ExportParodies | [.google.protobuf.Empty](#google.protobuf.Empty) | [.google.longrunning.Operation](#google.longrunning.Operation) |  |
| GetUniverse | [GetUniverseRequest](#animeshon.crossrefs.v1alpha1.GetUniverseRequest) | [Universe](#animeshon.crossrefs.v1alpha1.Universe) |  |
| UpdateUniverse | [UpdateUniverseRequest](#animeshon.crossrefs.v1alpha1.UpdateUniverseRequest) | [Universe](#animeshon.crossrefs.v1alpha1.Universe) |  |
| ExpandUniverse | [ExpandUniverseRequest](#animeshon.crossrefs.v1alpha1.ExpandUniverseRequest) | [ExpandUniverseResponse](#animeshon.crossrefs.v1alpha1.ExpandUniverseResponse) |  |
| GetWormhole | [GetWormholeRequest](#animeshon.crossrefs.v1alpha1.GetWormholeRequest) | [Wormhole](#animeshon.crossrefs.v1alpha1.Wormhole) |  |
| ListWormholeCrossRefs | [ListWormholeCrossRefsRequest](#animeshon.crossrefs.v1alpha1.ListWormholeCrossRefsRequest) | [ListWormholeCrossRefsResponse](#animeshon.crossrefs.v1alpha1.ListWormholeCrossRefsResponse) |  |

 



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

