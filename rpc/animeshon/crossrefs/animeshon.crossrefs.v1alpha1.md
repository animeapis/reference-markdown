# Package animeshon.crossrefs.v1alpha1

## Index
- [Referrer](#animeshon.crossrefs.v1alpha1.Referrer)
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

## Referrer {#animeshon.crossrefs.v1alpha1.Referrer}

| GetCrossRef |
| --- |
| **rpc** GetCrossRef([GetCrossRefRequest](#animeshon.crossrefs.v1alpha1.GetCrossRefRequest)) [CrossRef](#animeshon.crossrefs.v1alpha1.CrossRef)<br/>GetCrossRef returns a crossref. |

| ListCrossRefs |
| --- |
| **rpc** ListCrossRefs([ListCrossRefsRequest](#animeshon.crossrefs.v1alpha1.ListCrossRefsRequest)) [ListCrossRefsResponse](#animeshon.crossrefs.v1alpha1.ListCrossRefsResponse)<br/> |

| CreateCrossRef |
| --- |
| **rpc** CreateCrossRef([CreateCrossRefRequest](#animeshon.crossrefs.v1alpha1.CreateCrossRefRequest)) [CrossRef](#animeshon.crossrefs.v1alpha1.CrossRef)<br/>CreateCrossRef creates a new crossref. |

| BatchCreateCrossRefs |
| --- |
| **rpc** BatchCreateCrossRefs([BatchCreateCrossRefsRequest](#animeshon.crossrefs.v1alpha1.BatchCreateCrossRefsRequest)) [BatchCreateCrossRefsResponse](#animeshon.crossrefs.v1alpha1.BatchCreateCrossRefsResponse)<br/>BatchCreateCrossRefs creates new crossrefs in batch. The limit is of 10 crossreferences and it's blocking. It ensures that the crossreferences are created in the database but not propagated to the other services |

| UpdateCrossRef |
| --- |
| **rpc** UpdateCrossRef([UpdateCrossRefRequest](#animeshon.crossrefs.v1alpha1.UpdateCrossRefRequest)) [UpdateCrossRefResponse](#animeshon.crossrefs.v1alpha1.UpdateCrossRefResponse)<br/> |

| CountCrossRefs |
| --- |
| **rpc** CountCrossRefs([CountCrossRefsRequest](#animeshon.crossrefs.v1alpha1.CountCrossRefsRequest)) [CountCrossRefsResponse](#animeshon.crossrefs.v1alpha1.CountCrossRefsResponse)<br/> |

| AnalyzeCrossRefs |
| --- |
| **rpc** AnalyzeCrossRefs([AnalyzeCrossRefRequest](#animeshon.crossrefs.v1alpha1.AnalyzeCrossRefRequest)) [.google.longrunning.Operation](#google.longrunning.Operation)<br/>Analyzes and proposes new cross-references according to their similarity. |

| ImportCrossRefs |
| --- |
| **rpc** ImportCrossRefs([ImportCrossRefRequest](#animeshon.crossrefs.v1alpha1.ImportCrossRefRequest)) [.google.longrunning.Operation](#google.longrunning.Operation)<br/>Imports already existing cross-references from third-parties. |

| ExportCrossRefs |
| --- |
| **rpc** ExportCrossRefs([ExportCrossRefRequest](#animeshon.crossrefs.v1alpha1.ExportCrossRefRequest)) [.google.longrunning.Operation](#google.longrunning.Operation)<br/>Exports the cross-references to Cloud Pub/Sub for a full synchronization. This operation is usually called after a new import with a clean database. |

| InitializeCrossRefs |
| --- |
| **rpc** InitializeCrossRefs([.google.protobuf.Empty](#google.protobuf.Empty)) [.google.longrunning.Operation](#google.longrunning.Operation)<br/>Initialize the cross-references using specific namespaces for each kind. This operation first analyzes the entities meeting the kind and namespace precondition to match new entities with existing ones |

| AnalyzeParodies |
| --- |
| **rpc** AnalyzeParodies([.google.protobuf.Empty](#google.protobuf.Empty)) [.google.longrunning.Operation](#google.longrunning.Operation)<br/> |

| ExportParodies |
| --- |
| **rpc** ExportParodies([.google.protobuf.Empty](#google.protobuf.Empty)) [.google.longrunning.Operation](#google.longrunning.Operation)<br/> |

| GetUniverse |
| --- |
| **rpc** GetUniverse([GetUniverseRequest](#animeshon.crossrefs.v1alpha1.GetUniverseRequest)) [Universe](#animeshon.crossrefs.v1alpha1.Universe)<br/> |

| UpdateUniverse |
| --- |
| **rpc** UpdateUniverse([UpdateUniverseRequest](#animeshon.crossrefs.v1alpha1.UpdateUniverseRequest)) [Universe](#animeshon.crossrefs.v1alpha1.Universe)<br/> |

| ExpandUniverse |
| --- |
| **rpc** ExpandUniverse([ExpandUniverseRequest](#animeshon.crossrefs.v1alpha1.ExpandUniverseRequest)) [ExpandUniverseResponse](#animeshon.crossrefs.v1alpha1.ExpandUniverseResponse)<br/> |

| GetWormhole |
| --- |
| **rpc** GetWormhole([GetWormholeRequest](#animeshon.crossrefs.v1alpha1.GetWormholeRequest)) [Wormhole](#animeshon.crossrefs.v1alpha1.Wormhole)<br/> |

| ListWormholeCrossRefs |
| --- |
| **rpc** ListWormholeCrossRefs([ListWormholeCrossRefsRequest](#animeshon.crossrefs.v1alpha1.ListWormholeCrossRefsRequest)) [ListWormholeCrossRefsResponse](#animeshon.crossrefs.v1alpha1.ListWormholeCrossRefsResponse)<br/> |

## AnalyzeCrossRefRequest {#animeshon.crossrefs.v1alpha1.AnalyzeCrossRefRequest}

| Field | Description |
| --- | --- |
| config | **[ AnalyzeCrossRefRequest.AnalyzeCrossRefConfig](#AnalyzeCrossRefRequest.AnalyzeCrossRefConfig)**<br/>Global configuration |
| target_kinds | **[map AnalyzeCrossRefRequest.TargetKindsEntry](#AnalyzeCrossRefRequest.TargetKindsEntry)**<br/>Kind configurations |
## AnalyzeCrossRefRequest.AnalyzeCrossRefConfig {#animeshon.crossrefs.v1alpha1.AnalyzeCrossRefRequest.AnalyzeCrossRefConfig}

| Field | Description |
| --- | --- |
| tollerance | **[ int32](#int32)**<br/>Tollerance of the match in pct |
| opts | **[map AnalyzeCrossRefRequest.AnalyzeCrossRefConfig.OptsEntry](#AnalyzeCrossRefRequest.AnalyzeCrossRefConfig.OptsEntry)**<br/>Map of all options for the analysis |
## AnalyzeCrossRefRequest.AnalyzeCrossRefConfig.OptsEntry {#animeshon.crossrefs.v1alpha1.AnalyzeCrossRefRequest.AnalyzeCrossRefConfig.OptsEntry}

| Field | Description |
| --- | --- |
| key | **[ string](#string)**<br/> |
| value | **[ bool](#bool)**<br/> |
## AnalyzeCrossRefRequest.AnalyzeCrossRefNamespaceConfig {#animeshon.crossrefs.v1alpha1.AnalyzeCrossRefRequest.AnalyzeCrossRefNamespaceConfig}

| Field | Description |
| --- | --- |
| namespace | **[ string](#string)**<br/>Namespace to analyze |
| config | **[ AnalyzeCrossRefRequest.AnalyzeCrossRefConfig](#AnalyzeCrossRefRequest.AnalyzeCrossRefConfig)**<br/>Optional Namespace specific configuration |
## AnalyzeCrossRefRequest.AnalyzeCrossRefTargetConfig {#animeshon.crossrefs.v1alpha1.AnalyzeCrossRefRequest.AnalyzeCrossRefTargetConfig}

| Field | Description |
| --- | --- |
| target_kind | **[ string](#string)**<br/>Kind to analyze |
| config | **[ AnalyzeCrossRefRequest.AnalyzeCrossRefConfig](#AnalyzeCrossRefRequest.AnalyzeCrossRefConfig)**<br/>Optional Target specific configuration |
| namespaces | **[map AnalyzeCrossRefRequest.AnalyzeCrossRefTargetConfig.NamespacesEntry](#AnalyzeCrossRefRequest.AnalyzeCrossRefTargetConfig.NamespacesEntry)**<br/>Namespace configurations |
## AnalyzeCrossRefRequest.AnalyzeCrossRefTargetConfig.NamespacesEntry {#animeshon.crossrefs.v1alpha1.AnalyzeCrossRefRequest.AnalyzeCrossRefTargetConfig.NamespacesEntry}

| Field | Description |
| --- | --- |
| key | **[ string](#string)**<br/> |
| value | **[ AnalyzeCrossRefRequest.AnalyzeCrossRefNamespaceConfig](#AnalyzeCrossRefRequest.AnalyzeCrossRefNamespaceConfig)**<br/> |
## AnalyzeCrossRefRequest.TargetKindsEntry {#animeshon.crossrefs.v1alpha1.AnalyzeCrossRefRequest.TargetKindsEntry}

| Field | Description |
| --- | --- |
| key | **[ string](#string)**<br/> |
| value | **[ AnalyzeCrossRefRequest.AnalyzeCrossRefTargetConfig](#AnalyzeCrossRefRequest.AnalyzeCrossRefTargetConfig)**<br/> |
## AnalyzeCrossRefsResponse {#animeshon.crossrefs.v1alpha1.AnalyzeCrossRefsResponse}
TODO(christian-roggia): this is a workaround to solve the issue of GAPIC
CLI where broken code is generated if google.protobuf.Empty is used in the
response_type of longrunning operations.
## AnalyzeParodiesResponse {#animeshon.crossrefs.v1alpha1.AnalyzeParodiesResponse}

## BatchCreateCrossRefsRequest {#animeshon.crossrefs.v1alpha1.BatchCreateCrossRefsRequest}

| Field | Description |
| --- | --- |
| crossrefs | **[repeated CrossRef](#CrossRef)**<br/> |
## BatchCreateCrossRefsResponse {#animeshon.crossrefs.v1alpha1.BatchCreateCrossRefsResponse}

| Field | Description |
| --- | --- |
| crossrefs | **[repeated CrossRef](#CrossRef)**<br/>The list of crossrefs to create. |
## CountCrossRefsRequest {#animeshon.crossrefs.v1alpha1.CountCrossRefsRequest}

| Field | Description |
| --- | --- |
| filter | **[ CrossRefsFilterRequest](#CrossRefsFilterRequest)**<br/>A filter to be applied to results. |
## CountCrossRefsResponse {#animeshon.crossrefs.v1alpha1.CountCrossRefsResponse}

| Field | Description |
| --- | --- |
| count | **[ int32](#int32)**<br/> |
## CreateCrossRefRequest {#animeshon.crossrefs.v1alpha1.CreateCrossRefRequest}

| Field | Description |
| --- | --- |
| crossref | **[ CrossRef](#CrossRef)**<br/> |
## CrossRef {#animeshon.crossrefs.v1alpha1.CrossRef}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the crossref. |
| root | **[ string](#string)**<br/>root entity which generated the crossreference. |
| etag | **[ string](#string)**<br/>version control. |
| verified | **[ bool](#bool)**<br/>if verified, the crossreference has been generated by a trusty process or verified by an operator |
| operator | **[ string](#string)**<br/>last operator which edited the crossreference |
| create_time | **[ google.protobuf.Timestamp](#google.protobuf.Timestamp)**<br/>creation time |
| update_time | **[ google.protobuf.Timestamp](#google.protobuf.Timestamp)**<br/>update time |
| edges | **[repeated CrossRefEdge](#CrossRefEdge)**<br/>all edges of the crossreference |
## CrossRefEdge {#animeshon.crossrefs.v1alpha1.CrossRefEdge}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/> |
| state | **[ int32](#int32)**<br/> |
## CrossRefsFilterRequest {#animeshon.crossrefs.v1alpha1.CrossRefsFilterRequest}

| Field | Description |
| --- | --- |
| prefix | **[ string](#string)**<br/>specifies the prefix of the CrossRefs name to search in |
| pendingOnly | **[ bool](#bool)**<br/>if true only crossreferences with pendings are returned |
## ExpandUniverseRequest {#animeshon.crossrefs.v1alpha1.ExpandUniverseRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The universe to expand. |
| depth_limit | **[ int32](#int32)**<br/>The maximum depth to expand. |
| filter | **[ string](#string)**<br/>The filter to use. Accepted values are CONTENT and CHARACTER. |
## ExpandUniverseResponse {#animeshon.crossrefs.v1alpha1.ExpandUniverseResponse}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the requested universe. |
| payload | **[ bytes](#bytes)**<br/>TODO(christian-roggia): resources should be available through protobuf messages. |
## ExportCrossRefRequest {#animeshon.crossrefs.v1alpha1.ExportCrossRefRequest}

| Field | Description |
| --- | --- |
| target | **[ ExportCrossRefRequest.Target](#ExportCrossRefRequest.Target)**<br/> |
| prefix | **[ string](#string)**<br/>Prefix to restrict the crossrefs to export to a specific subset |
## ExportCrossRefsResponse {#animeshon.crossrefs.v1alpha1.ExportCrossRefsResponse}

## ExportParodiesResponse {#animeshon.crossrefs.v1alpha1.ExportParodiesResponse}

## GetCrossRefRequest {#animeshon.crossrefs.v1alpha1.GetCrossRefRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the requested crossref. |
## GetUniverseRequest {#animeshon.crossrefs.v1alpha1.GetUniverseRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the requested universe. |
## GetWormholeRequest {#animeshon.crossrefs.v1alpha1.GetWormholeRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/> |
## ImportCrossRefRequest {#animeshon.crossrefs.v1alpha1.ImportCrossRefRequest}

| Field | Description |
| --- | --- |
| opts | **[map ImportCrossRefRequest.OptsEntry](#ImportCrossRefRequest.OptsEntry)**<br/>Map of all options for the import |
## ImportCrossRefRequest.OptsEntry {#animeshon.crossrefs.v1alpha1.ImportCrossRefRequest.OptsEntry}

| Field | Description |
| --- | --- |
| key | **[ string](#string)**<br/> |
| value | **[ bool](#bool)**<br/> |
## ImportCrossRefsResponse {#animeshon.crossrefs.v1alpha1.ImportCrossRefsResponse}

## InitializeCrossRefsResponse {#animeshon.crossrefs.v1alpha1.InitializeCrossRefsResponse}

## ListCrossRefsRequest {#animeshon.crossrefs.v1alpha1.ListCrossRefsRequest}

| Field | Description |
| --- | --- |
| page_size | **[ int32](#int32)**<br/>The maximum number of users to return. Server may return fewer users than requested. The maximum page_size is 100 If unspecified, server will pick an appropriate default. |
| page_token | **[ string](#string)**<br/>The value returned from the previous call. |
| filter | **[ CrossRefsFilterRequest](#CrossRefsFilterRequest)**<br/>A filter to be applied to results. |
## ListCrossRefsResponse {#animeshon.crossrefs.v1alpha1.ListCrossRefsResponse}

| Field | Description |
| --- | --- |
| crossrefs | **[repeated CrossRef](#CrossRef)**<br/>The list of crossrefs. |
| next_page_token | **[ string](#string)**<br/>A token to retrieve next page of results. |
## ListWormholeCrossRefsRequest {#animeshon.crossrefs.v1alpha1.ListWormholeCrossRefsRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/> |
| withApproved | **[ bool](#bool)**<br/>search wormhole entity in approved edges |
| withPending | **[ bool](#bool)**<br/>search wormhole entity in pending edges |
| withPartial | **[ bool](#bool)**<br/>search wormhole entity in partial edges |
| withRejected | **[ bool](#bool)**<br/>search wormhole entity in rejected edges |
| crossRefsExclusion | **[repeated string](#string)**<br/>list of CrossRefs to exclude |
| prefix | **[ string](#string)**<br/>prefix of the CrossRefs name to search |
## ListWormholeCrossRefsResponse {#animeshon.crossrefs.v1alpha1.ListWormholeCrossRefsResponse}

| Field | Description |
| --- | --- |
| crossrefs | **[repeated CrossRef](#CrossRef)**<br/>The list of crossrefs. |
## OperationMetadata {#animeshon.crossrefs.v1alpha1.OperationMetadata}
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
| step_count | **[ int32](#int32)**<br/>Output only. |
| step_progress | **[ int32](#int32)**<br/>Output only. |
| item_count | **[ int32](#int32)**<br/>Output only. |
| item_progress | **[ int32](#int32)**<br/>Output only. |
## Universe {#animeshon.crossrefs.v1alpha1.Universe}
TODO(christian-roggia): move the universe together with all other resources.
| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the universe. |
| payload | **[ bytes](#bytes)**<br/>TODO(christian-roggia): resources should be available through protobuf messages. |
## UpdateCrossRefRequest {#animeshon.crossrefs.v1alpha1.UpdateCrossRefRequest}

| Field | Description |
| --- | --- |
| crossref | **[ CrossRef](#CrossRef)**<br/>The crossref to update. |
| update_mask | **[ google.protobuf.FieldMask](#google.protobuf.FieldMask)**<br/>The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |
## UpdateCrossRefResponse {#animeshon.crossrefs.v1alpha1.UpdateCrossRefResponse}

| Field | Description |
| --- | --- |
| crossrefs | **[repeated CrossRef](#CrossRef)**<br/>All CrossRef involved in the update |
## UpdateUniverseRequest {#animeshon.crossrefs.v1alpha1.UpdateUniverseRequest}

| Field | Description |
| --- | --- |
| universe | **[ Universe](#Universe)**<br/>The universe to update. |
| update_mask | **[ google.protobuf.FieldMask](#google.protobuf.FieldMask)**<br/>The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |
## Wormhole {#animeshon.crossrefs.v1alpha1.Wormhole}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/> |
| names | **[repeated Wormhole.Text](#Wormhole.Text)**<br/>The names of te content |
| aliases | **[repeated Wormhole.Text](#Wormhole.Text)**<br/>The aliases of te content |
| image | **[ bytes](#bytes)**<br/>raw bytes of image |
| image_url | **[ string](#string)**<br/>url of the image |
| type | **[ string](#string)**<br/>type of the content |
| subtype | **[ string](#string)**<br/>subtype of the content |
| external_url | **[ string](#string)**<br/>external url of the content |
| publishing_type | **[ string](#string)**<br/>type of publication |
| is_parody | **[ bool](#bool)**<br/>the content is parody of another content |
| identifier | **[ string](#string)**<br/>identifier |
| date | **[ google.protobuf.Timestamp](#google.protobuf.Timestamp)**<br/>most significant date |
| parent_name | **[ string](#string)**<br/>parent's resource name useful for chapters and episodes to know which content it refers |
| parent_external_url | **[ string](#string)**<br/>prant external url |
## Wormhole.Text {#animeshon.crossrefs.v1alpha1.Wormhole.Text}

| Field | Description |
| --- | --- |
| text | **[ string](#string)**<br/> |
| localization | **[ string](#string)**<br/> |

## ExportCrossRefRequest.Target {#animeshon.crossrefs.v1alpha1.ExportCrossRefRequest.Target}
Determine the target of the export.
Full means storage + migration
Storage means only persinstent stogare
Migration means notify the migrato to perform the data consolidation

| Name | Description |
| --- | --- |
| FULL | No description. |
| STORAGE | No description. |
| MIGRATOR | No description. |
