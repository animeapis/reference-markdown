# Protocol Documentation
<a name="top"></a>

## Table of Contents

- [animeshon/vision/v1alpha1/geometry.proto](#animeshon/vision/v1alpha1/geometry.proto)
    - [BoundingPoly](#animeshon.vision.v1alpha1.BoundingPoly)
    - [Vertex](#animeshon.vision.v1alpha1.Vertex)
  
- [animeshon/vision/v1alpha1/annotations.proto](#animeshon/vision/v1alpha1/annotations.proto)
    - [EntityAnnotation](#animeshon.vision.v1alpha1.EntityAnnotation)
    - [ImageAnnotations](#animeshon.vision.v1alpha1.ImageAnnotations)
    - [KnowledgeGraphAnnotation](#animeshon.vision.v1alpha1.KnowledgeGraphAnnotation)
    - [LabelAnnotation](#animeshon.vision.v1alpha1.LabelAnnotation)
    - [SafeSearchAnnotation](#animeshon.vision.v1alpha1.SafeSearchAnnotation)
    - [TextAnnotation](#animeshon.vision.v1alpha1.TextAnnotation)
    - [TextAnnotation.Language](#animeshon.vision.v1alpha1.TextAnnotation.Language)
    - [TextAnnotation.TextProperty](#animeshon.vision.v1alpha1.TextAnnotation.TextProperty)
    - [WebSearchAnnotation](#animeshon.vision.v1alpha1.WebSearchAnnotation)
  
    - [Likelihood](#animeshon.vision.v1alpha1.Likelihood)
  
- [animeshon/vision/v1alpha1/properties.proto](#animeshon/vision/v1alpha1/properties.proto)
    - [ColorProperty](#animeshon.vision.v1alpha1.ColorProperty)
    - [FingerprintProperty](#animeshon.vision.v1alpha1.FingerprintProperty)
    - [ImageProperties](#animeshon.vision.v1alpha1.ImageProperties)
  
- [animeshon/vision/v1alpha1/vision.proto](#animeshon/vision/v1alpha1/vision.proto)
    - [AnalyzeImageRequest](#animeshon.vision.v1alpha1.AnalyzeImageRequest)
    - [AnalyzeImageResponse](#animeshon.vision.v1alpha1.AnalyzeImageResponse)
    - [CreateImageAnnotationRequest](#animeshon.vision.v1alpha1.CreateImageAnnotationRequest)
    - [DeleteImageAnalysisRequest](#animeshon.vision.v1alpha1.DeleteImageAnalysisRequest)
    - [DeleteImageAnnotationRequest](#animeshon.vision.v1alpha1.DeleteImageAnnotationRequest)
    - [GetImageAnalysisRequest](#animeshon.vision.v1alpha1.GetImageAnalysisRequest)
    - [GetImageAnnotationRequest](#animeshon.vision.v1alpha1.GetImageAnnotationRequest)
    - [ImageAnalysis](#animeshon.vision.v1alpha1.ImageAnalysis)
    - [ImageAnnotation](#animeshon.vision.v1alpha1.ImageAnnotation)
    - [ListImageAnalysesRequest](#animeshon.vision.v1alpha1.ListImageAnalysesRequest)
    - [ListImageAnalysesResponse](#animeshon.vision.v1alpha1.ListImageAnalysesResponse)
    - [ListImageAnnotationsRequest](#animeshon.vision.v1alpha1.ListImageAnnotationsRequest)
    - [ListImageAnnotationsResponse](#animeshon.vision.v1alpha1.ListImageAnnotationsResponse)
    - [UpdateImageAnnotationRequest](#animeshon.vision.v1alpha1.UpdateImageAnnotationRequest)
  
    - [ImageAnnotator](#animeshon.vision.v1alpha1.ImageAnnotator)
  
- [animeshon/vision/v1alpha1/internal.proto](#animeshon/vision/v1alpha1/internal.proto)
    - [ImageAnalysisEntry](#animeshon.vision.v1alpha1.ImageAnalysisEntry)
    - [ImageAnnotationEntry](#animeshon.vision.v1alpha1.ImageAnnotationEntry)
  
- [Scalar Value Types](#scalar-value-types)



<a name="animeshon/vision/v1alpha1/geometry.proto"></a>
<p align="right"><a href="#top">Top</a></p>

## animeshon/vision/v1alpha1/geometry.proto



<a name="animeshon.vision.v1alpha1.BoundingPoly"></a>

### BoundingPoly
A bounding polygon for the detected image annotation.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| vertices | [Vertex](#animeshon.vision.v1alpha1.Vertex) | repeated | The bounding polygon vertices. |






<a name="animeshon.vision.v1alpha1.Vertex"></a>

### Vertex
A vertex represents a 2D point in the image.
NOTE: the vertex coordinates are in the same scale as the original image.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| x | [int32](#int32) |  | X coordinate. |
| y | [int32](#int32) |  | Y coordinate. |





 

 

 

 



<a name="animeshon/vision/v1alpha1/annotations.proto"></a>
<p align="right"><a href="#top">Top</a></p>

## animeshon/vision/v1alpha1/annotations.proto



<a name="animeshon.vision.v1alpha1.EntityAnnotation"></a>

### EntityAnnotation



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The entity resource name. |
| score | [float](#float) |  | Overall score of the result. Range [0, 1]. |
| bounding_box | [BoundingPoly](#animeshon.vision.v1alpha1.BoundingPoly) |  | Image region to which this entity belongs. |






<a name="animeshon.vision.v1alpha1.ImageAnnotations"></a>

### ImageAnnotations



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| text_annotations | [TextAnnotation](#animeshon.vision.v1alpha1.TextAnnotation) | repeated | The texts detected in the image. |
| label_annotations | [LabelAnnotation](#animeshon.vision.v1alpha1.LabelAnnotation) | repeated | The labels detected in the image. |
| entity_annotations | [EntityAnnotation](#animeshon.vision.v1alpha1.EntityAnnotation) | repeated | The entites detected in the image. |
| knowledge_graph_annotations | [KnowledgeGraphAnnotation](#animeshon.vision.v1alpha1.KnowledgeGraphAnnotation) | repeated | The Animeshon Graph Knowledge-Base resources detected in the image. |
| web_search_annotations | [WebSearchAnnotation](#animeshon.vision.v1alpha1.WebSearchAnnotation) | repeated | The WebSearch resources (pages and images) detected in the image. |
| safe_search_annotation | [SafeSearchAnnotation](#animeshon.vision.v1alpha1.SafeSearchAnnotation) |  | The SafeSearch ratings detected in the image. |






<a name="animeshon.vision.v1alpha1.KnowledgeGraphAnnotation"></a>

### KnowledgeGraphAnnotation



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| resource | [string](#string) |  | The Animeshon Graph Knowledge-Base resource name. |
| score | [float](#float) |  | Overall score of the result. Range [0, 1]. |
| bounding_box | [BoundingPoly](#animeshon.vision.v1alpha1.BoundingPoly) |  | Image region to which this entity belongs. |






<a name="animeshon.vision.v1alpha1.LabelAnnotation"></a>

### LabelAnnotation



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The label resource name. |
| score | [float](#float) |  | Overall score of the result. Range [0, 1]. |
| topicality | [float](#float) |  | The relevancy of the annotation. Range [0, 1]. |






<a name="animeshon.vision.v1alpha1.SafeSearchAnnotation"></a>

### SafeSearchAnnotation



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| adult | [Likelihood](#animeshon.vision.v1alpha1.Likelihood) |  | Represents the adult content likelihood for the image. Adult content may contain elements such as nudity, pornographic images or cartoons, or sexual activities. |
| racy | [Likelihood](#animeshon.vision.v1alpha1.Likelihood) |  | Likelihood that the request image contains racy content. Racy content may include (but is not limited to) skimpy or sheer clothing, strategically covered nudity, lewd or provocative poses, or close-ups of sensitive body areas. |
| violence | [Likelihood](#animeshon.vision.v1alpha1.Likelihood) |  | Likelihood that this image contains violent content. |
| medical | [Likelihood](#animeshon.vision.v1alpha1.Likelihood) |  | Likelihood that this is a medical image. |
| juvenile | [Likelihood](#animeshon.vision.v1alpha1.Likelihood) |  | Likelihood that the request image contains one or more individuals decipted as juveniles. Juvenile content may contain elements such as school-aged children, preschoolers, toddlers, infants, and newborns. The target age considered as juvenile is from 0 to 14~16 years old. |






<a name="animeshon.vision.v1alpha1.TextAnnotation"></a>

### TextAnnotation



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| property | [TextAnnotation.TextProperty](#animeshon.vision.v1alpha1.TextAnnotation.TextProperty) |  | Additional information detected for the paragraph. |
| bounding_box | [BoundingPoly](#animeshon.vision.v1alpha1.BoundingPoly) |  | The bounding box for the paragraph. |
| text | [string](#string) |  | UTF-8 text detected by the OCR. |
| confidence | [float](#float) |  | Confidence of the OCR results for the paragraph. Range [0, 1]. |






<a name="animeshon.vision.v1alpha1.TextAnnotation.Language"></a>

### TextAnnotation.Language
Detected language for a structural component.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| language_code | [string](#string) |  | The BCP-47 language code, such as &#34;en-US&#34; or &#34;sr-Latn&#34;. |
| confidence | [float](#float) |  | Confidence of detected language. Range [0, 1]. |






<a name="animeshon.vision.v1alpha1.TextAnnotation.TextProperty"></a>

### TextAnnotation.TextProperty
Additional information detected on the structural component.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| languages | [TextAnnotation.Language](#animeshon.vision.v1alpha1.TextAnnotation.Language) | repeated | A list of detected languages together with confidence. |






<a name="animeshon.vision.v1alpha1.WebSearchAnnotation"></a>

### WebSearchAnnotation



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| url | [string](#string) |  | The result image URL. |
| score | [float](#float) |  | Overall relevancy score for the image. |





 


<a name="animeshon.vision.v1alpha1.Likelihood"></a>

### Likelihood
A bucketized representation of likelihood, which is intended to give clients
highly stable results across model upgrades.

| Name | Number | Description |
| ---- | ------ | ----------- |
| UNKNOWN | 0 | Unknown likelihood. |
| VERY_UNLIKELY | 1 | It is very unlikely. |
| UNLIKELY | 2 | It is unlikely. |
| POSSIBLE | 3 | It is possible. |
| LIKELY | 4 | It is likely. |
| VERY_LIKELY | 5 | It is very likely. |


 

 

 



<a name="animeshon/vision/v1alpha1/properties.proto"></a>
<p align="right"><a href="#top">Top</a></p>

## animeshon/vision/v1alpha1/properties.proto



<a name="animeshon.vision.v1alpha1.ColorProperty"></a>

### ColorProperty
Color information consists of RGB channels, score, and the fraction of
the image that the color occupies in the image.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| color | [google.type.Color](#google.type.Color) |  | RGB components of the color. |
| score | [float](#float) |  | Image-specific score for this color. Value in range [0, 1]. |
| pixel_fraction | [float](#float) |  | The fraction of pixels the color occupies in the image. Value in range [0, 1]. |






<a name="animeshon.vision.v1alpha1.FingerprintProperty"></a>

### FingerprintProperty



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| content | [bytes](#bytes) |  | The fingerprint of the image in binary representation. |
| algorithm | [string](#string) |  | The algorithm used to generate the fingerprint. |






<a name="animeshon.vision.v1alpha1.ImageProperties"></a>

### ImageProperties



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| dominant_colors | [ColorProperty](#animeshon.vision.v1alpha1.ColorProperty) | repeated | Set of dominant colors and their corresponding scores. |
| fingerprints | [FingerprintProperty](#animeshon.vision.v1alpha1.FingerprintProperty) | repeated | The fingerprints of the image. |





 

 

 

 



<a name="animeshon/vision/v1alpha1/vision.proto"></a>
<p align="right"><a href="#top">Top</a></p>

## animeshon/vision/v1alpha1/vision.proto



<a name="animeshon.vision.v1alpha1.AnalyzeImageRequest"></a>

### AnalyzeImageRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| parent | [string](#string) |  | The parent image to be analyzed. |
| features | [string](#string) | repeated | A list of features to analyze. |






<a name="animeshon.vision.v1alpha1.AnalyzeImageResponse"></a>

### AnalyzeImageResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| analysis | [ImageAnalysis](#animeshon.vision.v1alpha1.ImageAnalysis) |  | The analysis of the image. |






<a name="animeshon.vision.v1alpha1.CreateImageAnnotationRequest"></a>

### CreateImageAnnotationRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| parent | [string](#string) |  | The parent this image annotation belongs to. |
| annotation | [ImageAnnotation](#animeshon.vision.v1alpha1.ImageAnnotation) |  | The image annotation to create. |






<a name="animeshon.vision.v1alpha1.DeleteImageAnalysisRequest"></a>

### DeleteImageAnalysisRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the analysis to delete. |






<a name="animeshon.vision.v1alpha1.DeleteImageAnnotationRequest"></a>

### DeleteImageAnnotationRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The image annotation to delete. |






<a name="animeshon.vision.v1alpha1.GetImageAnalysisRequest"></a>

### GetImageAnalysisRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the image analysis to retrieve. |
| field_mask | [google.protobuf.FieldMask](#google.protobuf.FieldMask) |  | FieldMask that represents which fields should be retrieved. |






<a name="animeshon.vision.v1alpha1.GetImageAnnotationRequest"></a>

### GetImageAnnotationRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the image annotation to retrieve. |






<a name="animeshon.vision.v1alpha1.ImageAnalysis"></a>

### ImageAnalysis
TODO: add information about the model used and whether the analysis is STABLE
TODO: or EXPERIMENTAL. NOTE: Latest should return the latest STABLE analysis.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the image analysis. |
| properties | [ImageProperties](#animeshon.vision.v1alpha1.ImageProperties) |  | The (immutable) properties of the image. |
| annotations | [ImageAnnotations](#animeshon.vision.v1alpha1.ImageAnnotations) |  | The annotations of the image. |
| create_time | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | The creation time indicating when this revision was created. |






<a name="animeshon.vision.v1alpha1.ImageAnnotation"></a>

### ImageAnnotation



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The annotation resource name. |
| resource | [string](#string) |  | The annotated image. |
| annotations | [ImageAnnotations](#animeshon.vision.v1alpha1.ImageAnnotations) |  | The annotations of the image. |
| create_time | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | The timestamp at which the annotation was created. |
| update_time | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | The latest timestamp at which the annotation was updated. |






<a name="animeshon.vision.v1alpha1.ListImageAnalysesRequest"></a>

### ListImageAnalysesRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| parent | [string](#string) |  | The parent image to list analyses from. |
| page_size | [int32](#int32) |  | If unspecified, server will pick an appropriate default. |
| page_token | [string](#string) |  | The value returned from the previous call. |






<a name="animeshon.vision.v1alpha1.ListImageAnalysesResponse"></a>

### ListImageAnalysesResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| analyses | [ImageAnalysis](#animeshon.vision.v1alpha1.ImageAnalysis) | repeated | The list of image analyses. |
| next_page_token | [string](#string) |  | A token to retrieve next page of results. |






<a name="animeshon.vision.v1alpha1.ListImageAnnotationsRequest"></a>

### ListImageAnnotationsRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| parent | [string](#string) |  | The parent, which owns this collection of image annotations. |
| page_size | [int32](#int32) |  | If unspecified, server will pick an appropriate default. |
| page_token | [string](#string) |  | The value returned from the previous call. |
| filter | [string](#string) |  | A filter to be applied to results.

Currently accepted filters include: - resource:{full resource name} |






<a name="animeshon.vision.v1alpha1.ListImageAnnotationsResponse"></a>

### ListImageAnnotationsResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| annotations | [ImageAnnotation](#animeshon.vision.v1alpha1.ImageAnnotation) | repeated | The list of image annotations. |
| next_page_token | [string](#string) |  | A token to retrieve next page of results. |






<a name="animeshon.vision.v1alpha1.UpdateImageAnnotationRequest"></a>

### UpdateImageAnnotationRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| annotation | [ImageAnnotation](#animeshon.vision.v1alpha1.ImageAnnotation) |  | The image annotation to update. |
| update_mask | [google.protobuf.FieldMask](#google.protobuf.FieldMask) |  | The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |





 

 

 


<a name="animeshon.vision.v1alpha1.ImageAnnotator"></a>

### ImageAnnotator


| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| AnalyzeImage | [AnalyzeImageRequest](#animeshon.vision.v1alpha1.AnalyzeImageRequest) | [AnalyzeImageResponse](#animeshon.vision.v1alpha1.AnalyzeImageResponse) |  |
| ListImageAnalyses | [ListImageAnalysesRequest](#animeshon.vision.v1alpha1.ListImageAnalysesRequest) | [ListImageAnalysesResponse](#animeshon.vision.v1alpha1.ListImageAnalysesResponse) |  |
| GetImageAnalysis | [GetImageAnalysisRequest](#animeshon.vision.v1alpha1.GetImageAnalysisRequest) | [ImageAnalysis](#animeshon.vision.v1alpha1.ImageAnalysis) | Note: to fetch the latest available report use &#34;latest&#34; as report id. |
| DeleteImageAnalysis | [DeleteImageAnalysisRequest](#animeshon.vision.v1alpha1.DeleteImageAnalysisRequest) | [.google.protobuf.Empty](#google.protobuf.Empty) |  |
| CreateImageAnnotation | [CreateImageAnnotationRequest](#animeshon.vision.v1alpha1.CreateImageAnnotationRequest) | [ImageAnnotation](#animeshon.vision.v1alpha1.ImageAnnotation) |  |
| ListImageAnnotations | [ListImageAnnotationsRequest](#animeshon.vision.v1alpha1.ListImageAnnotationsRequest) | [ListImageAnnotationsResponse](#animeshon.vision.v1alpha1.ListImageAnnotationsResponse) |  |
| GetImageAnnotation | [GetImageAnnotationRequest](#animeshon.vision.v1alpha1.GetImageAnnotationRequest) | [ImageAnnotation](#animeshon.vision.v1alpha1.ImageAnnotation) |  |
| UpdateImageAnnotation | [UpdateImageAnnotationRequest](#animeshon.vision.v1alpha1.UpdateImageAnnotationRequest) | [ImageAnnotation](#animeshon.vision.v1alpha1.ImageAnnotation) |  |
| DeleteImageAnnotation | [DeleteImageAnnotationRequest](#animeshon.vision.v1alpha1.DeleteImageAnnotationRequest) | [.google.protobuf.Empty](#google.protobuf.Empty) |  |

 



<a name="animeshon/vision/v1alpha1/internal.proto"></a>
<p align="right"><a href="#top">Top</a></p>

## animeshon/vision/v1alpha1/internal.proto



<a name="animeshon.vision.v1alpha1.ImageAnalysisEntry"></a>

### ImageAnalysisEntry
This is a private internal structure used to store metadata information
about a specific ImageAnalysis. This structure is never exposed to the
public.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [int64](#int64) |  | The image analysis resource id. |
| properties | [ImageProperties](#animeshon.vision.v1alpha1.ImageProperties) |  | The (immutable) properties of the image. |
| annotations | [ImageAnnotations](#animeshon.vision.v1alpha1.ImageAnnotations) |  | The annotations of the image. |
| create_time | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | The creation time indicating when this revision was created. |






<a name="animeshon.vision.v1alpha1.ImageAnnotationEntry"></a>

### ImageAnnotationEntry
This is a private internal structure used to store metadata information
about a specific ImageAnnotation. This structure is never exposed to the
public.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [int64](#int64) |  | The image annotation resource id. |
| parent | [string](#string) |  | A reference to a parent resource. |
| resource | [string](#string) |  | The annotated image. |
| annotations | [ImageAnnotations](#animeshon.vision.v1alpha1.ImageAnnotations) |  | The annotations of the image. |
| create_time | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | When the album was created. |
| update_time | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | When the album was updated. |





 

 

 

 



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

