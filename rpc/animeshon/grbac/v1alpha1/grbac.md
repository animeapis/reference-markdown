# Protocol Documentation
<a name="top"></a>

## Table of Contents

- [animeshon/grbac/v1alpha1/grbac.proto](#animeshon/grbac/v1alpha1/grbac.proto)
    - [AccessTuple](#animeshon.grbac.v1alpha1.AccessTuple)
    - [AddGroupMemberRequest](#animeshon.grbac.v1alpha1.AddGroupMemberRequest)
    - [CreateGroupRequest](#animeshon.grbac.v1alpha1.CreateGroupRequest)
    - [CreatePermissionRequest](#animeshon.grbac.v1alpha1.CreatePermissionRequest)
    - [CreateResourceRequest](#animeshon.grbac.v1alpha1.CreateResourceRequest)
    - [CreateRoleRequest](#animeshon.grbac.v1alpha1.CreateRoleRequest)
    - [CreateSubjectRequest](#animeshon.grbac.v1alpha1.CreateSubjectRequest)
    - [DeleteGroupRequest](#animeshon.grbac.v1alpha1.DeleteGroupRequest)
    - [DeletePermissionRequest](#animeshon.grbac.v1alpha1.DeletePermissionRequest)
    - [DeleteResourceRequest](#animeshon.grbac.v1alpha1.DeleteResourceRequest)
    - [DeleteRoleRequest](#animeshon.grbac.v1alpha1.DeleteRoleRequest)
    - [DeleteSubjectRequest](#animeshon.grbac.v1alpha1.DeleteSubjectRequest)
    - [GetGroupRequest](#animeshon.grbac.v1alpha1.GetGroupRequest)
    - [GetResourceRequest](#animeshon.grbac.v1alpha1.GetResourceRequest)
    - [GetRoleRequest](#animeshon.grbac.v1alpha1.GetRoleRequest)
    - [Group](#animeshon.grbac.v1alpha1.Group)
    - [Permission](#animeshon.grbac.v1alpha1.Permission)
    - [RemoveGroupMemberRequest](#animeshon.grbac.v1alpha1.RemoveGroupMemberRequest)
    - [Resource](#animeshon.grbac.v1alpha1.Resource)
    - [Role](#animeshon.grbac.v1alpha1.Role)
    - [Subject](#animeshon.grbac.v1alpha1.Subject)
    - [TestIamPolicyRequest](#animeshon.grbac.v1alpha1.TestIamPolicyRequest)
    - [TransferResourceRequest](#animeshon.grbac.v1alpha1.TransferResourceRequest)
    - [TransferResourceRequest.SubstitutionsEntry](#animeshon.grbac.v1alpha1.TransferResourceRequest.SubstitutionsEntry)
    - [UpdateGroupRequest](#animeshon.grbac.v1alpha1.UpdateGroupRequest)
    - [UpdateRoleRequest](#animeshon.grbac.v1alpha1.UpdateRoleRequest)
  
    - [AccessControl](#animeshon.grbac.v1alpha1.AccessControl)
  
- [Scalar Value Types](#scalar-value-types)



<a name="animeshon/grbac/v1alpha1/grbac.proto"></a>
<p align="right"><a href="#top">Top</a></p>

## animeshon/grbac/v1alpha1/grbac.proto



<a name="animeshon.grbac.v1alpha1.AccessTuple"></a>

### AccessTuple
Information about the member, resource, and permission to check.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| principal | [string](#string) |  | The member, or principal, whose access you want to check. |
| full_resource_name | [string](#string) |  | The full resource name that identifies the resource. |
| permission | [string](#string) |  | The IAM permission to check for the specified member and resource. |






<a name="animeshon.grbac.v1alpha1.AddGroupMemberRequest"></a>

### AddGroupMemberRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| group | [string](#string) |  | The name of the group to add a member to. |
| member | [string](#string) |  | The member to be added. |






<a name="animeshon.grbac.v1alpha1.CreateGroupRequest"></a>

### CreateGroupRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| group | [Group](#animeshon.grbac.v1alpha1.Group) |  | The group to create. |






<a name="animeshon.grbac.v1alpha1.CreatePermissionRequest"></a>

### CreatePermissionRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| permission | [Permission](#animeshon.grbac.v1alpha1.Permission) |  | The permission to create. |






<a name="animeshon.grbac.v1alpha1.CreateResourceRequest"></a>

### CreateResourceRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| resource | [Resource](#animeshon.grbac.v1alpha1.Resource) |  | The resource to create. |






<a name="animeshon.grbac.v1alpha1.CreateRoleRequest"></a>

### CreateRoleRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| role | [Role](#animeshon.grbac.v1alpha1.Role) |  | The role to create. |






<a name="animeshon.grbac.v1alpha1.CreateSubjectRequest"></a>

### CreateSubjectRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| subject | [Subject](#animeshon.grbac.v1alpha1.Subject) |  | The subject to create. |






<a name="animeshon.grbac.v1alpha1.DeleteGroupRequest"></a>

### DeleteGroupRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The resource name of the group to delete. |






<a name="animeshon.grbac.v1alpha1.DeletePermissionRequest"></a>

### DeletePermissionRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The resource name of the permission to delete. |






<a name="animeshon.grbac.v1alpha1.DeleteResourceRequest"></a>

### DeleteResourceRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The full resource name that identifies the resource. |






<a name="animeshon.grbac.v1alpha1.DeleteRoleRequest"></a>

### DeleteRoleRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The resource name of the role to delete. |






<a name="animeshon.grbac.v1alpha1.DeleteSubjectRequest"></a>

### DeleteSubjectRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The subject to delete. |






<a name="animeshon.grbac.v1alpha1.GetGroupRequest"></a>

### GetGroupRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the group to retrieve. |






<a name="animeshon.grbac.v1alpha1.GetResourceRequest"></a>

### GetResourceRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The full resource name of the resource to retrieve. |






<a name="animeshon.grbac.v1alpha1.GetRoleRequest"></a>

### GetRoleRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the role to retrieve. |






<a name="animeshon.grbac.v1alpha1.Group"></a>

### Group



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The resource name of the group. |
| members | [string](#string) | repeated | The list of members of the group. Groups might include other groups. |
| etag | [bytes](#bytes) |  | An etag for concurrency control, ignored during creation. |






<a name="animeshon.grbac.v1alpha1.Permission"></a>

### Permission



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The resource name of the permission. |






<a name="animeshon.grbac.v1alpha1.RemoveGroupMemberRequest"></a>

### RemoveGroupMemberRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| group | [string](#string) |  | The name of the group to remove an member from. |
| member | [string](#string) |  | The member to be removed. |






<a name="animeshon.grbac.v1alpha1.Resource"></a>

### Resource



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The full resource name that identifies the resource. |
| parent | [string](#string) |  | The full resource name that identifies the parent resource. |
| etag | [bytes](#bytes) |  | An etag for concurrency control, ignored during creation. |






<a name="animeshon.grbac.v1alpha1.Role"></a>

### Role



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The resource name of the role. |
| permissions | [string](#string) | repeated | The list of permissions granted by the role. |
| etag | [bytes](#bytes) |  | An etag for concurrency control, ignored during creation. |






<a name="animeshon.grbac.v1alpha1.Subject"></a>

### Subject



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The resource name of the subject. |






<a name="animeshon.grbac.v1alpha1.TestIamPolicyRequest"></a>

### TestIamPolicyRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| access_tuple | [AccessTuple](#animeshon.grbac.v1alpha1.AccessTuple) |  | The information to use for checking whether a member has a permission for a resource. |






<a name="animeshon.grbac.v1alpha1.TransferResourceRequest"></a>

### TransferResourceRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The full resource name that identifies the resource. |
| target_parent | [string](#string) |  | The full resource name that identifies the new parent resource. |
| substitutions | [TransferResourceRequest.SubstitutionsEntry](#animeshon.grbac.v1alpha1.TransferResourceRequest.SubstitutionsEntry) | repeated | The map of substitutions to apply to the full resource name and all of its children.

As an example, it might be required to change the parent of a resource from &#34;users/123&#34; to &#34;users/678&#34;, the substitutions would then look like this:

substitutions = {&#34;users/123&#34;: &#34;users/456789&#34;}

and the expected result would then be the following:

from : //abc.animeapis.com/users/123/resources/210 to : //abc.animeapis.com/users/456789/resources/210

The same applies if we need to transfer a resource between two parents of different type:

substitutions = {&#34;users/123&#34;: &#34;organizations/678/teams/987&#34;}

and the expected result would then be the following:

from : //abc.animeapis.com/users/123/resources/210 to : //abc.animeapis.com/organizations/678/teams/987/resources/210

It is possible to apply multiple substitutions simultaneously. |






<a name="animeshon.grbac.v1alpha1.TransferResourceRequest.SubstitutionsEntry"></a>

### TransferResourceRequest.SubstitutionsEntry



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| key | [string](#string) |  |  |
| value | [string](#string) |  |  |






<a name="animeshon.grbac.v1alpha1.UpdateGroupRequest"></a>

### UpdateGroupRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| group | [Group](#animeshon.grbac.v1alpha1.Group) |  | The group to update. |
| update_mask | [google.protobuf.FieldMask](#google.protobuf.FieldMask) |  | The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |






<a name="animeshon.grbac.v1alpha1.UpdateRoleRequest"></a>

### UpdateRoleRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| role | [Role](#animeshon.grbac.v1alpha1.Role) |  | The role to update. |
| update_mask | [google.protobuf.FieldMask](#google.protobuf.FieldMask) |  | The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |





 

 

 


<a name="animeshon.grbac.v1alpha1.AccessControl"></a>

### AccessControl
AccessControl is the internal service used by Animeshon to enforce RBAC rules.

| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| TestIamPolicy | [TestIamPolicyRequest](#animeshon.grbac.v1alpha1.TestIamPolicyRequest) | [.google.protobuf.Empty](#google.protobuf.Empty) | Checks whether a member has a specific permission for a specific resource. If not allowed an Unauthorized (403) error will be returned. |
| GetIamPolicy | [.google.iam.v1.GetIamPolicyRequest](#google.iam.v1.GetIamPolicyRequest) | [.google.iam.v1.Policy](#google.iam.v1.Policy) | Gets the IAM policy that is attached to a generic resource. Note: the full resource name that identifies the resource must be provided. |
| SetIamPolicy | [.google.iam.v1.SetIamPolicyRequest](#google.iam.v1.SetIamPolicyRequest) | [.google.iam.v1.Policy](#google.iam.v1.Policy) | Sets the IAM policy that is attached to a generic resource. Note: the full resource name that identifies the resource must be provided. |
| GetResource | [GetResourceRequest](#animeshon.grbac.v1alpha1.GetResourceRequest) | [Resource](#animeshon.grbac.v1alpha1.Resource) | GetResource returns a resource. |
| CreateResource | [CreateResourceRequest](#animeshon.grbac.v1alpha1.CreateResourceRequest) | [Resource](#animeshon.grbac.v1alpha1.Resource) | CreateResource creates a new resource. |
| TransferResource | [TransferResourceRequest](#animeshon.grbac.v1alpha1.TransferResourceRequest) | [Resource](#animeshon.grbac.v1alpha1.Resource) | TransferResource transfers a resource to a new parent. |
| DeleteResource | [DeleteResourceRequest](#animeshon.grbac.v1alpha1.DeleteResourceRequest) | [.google.protobuf.Empty](#google.protobuf.Empty) | DeleteResource deletes a resource. |
| CreateSubject | [CreateSubjectRequest](#animeshon.grbac.v1alpha1.CreateSubjectRequest) | [Subject](#animeshon.grbac.v1alpha1.Subject) | CreateSubject creates a new subject. |
| DeleteSubject | [DeleteSubjectRequest](#animeshon.grbac.v1alpha1.DeleteSubjectRequest) | [.google.protobuf.Empty](#google.protobuf.Empty) | DeleteSubject deletes a subject. |
| GetGroup | [GetGroupRequest](#animeshon.grbac.v1alpha1.GetGroupRequest) | [Group](#animeshon.grbac.v1alpha1.Group) | GetGroup returns a group. |
| CreateGroup | [CreateGroupRequest](#animeshon.grbac.v1alpha1.CreateGroupRequest) | [Group](#animeshon.grbac.v1alpha1.Group) | CreateGroup creates a new group. |
| UpdateGroup | [UpdateGroupRequest](#animeshon.grbac.v1alpha1.UpdateGroupRequest) | [Group](#animeshon.grbac.v1alpha1.Group) | UpdateGroup updates a group with a field mask. |
| AddGroupMember | [AddGroupMemberRequest](#animeshon.grbac.v1alpha1.AddGroupMemberRequest) | [Group](#animeshon.grbac.v1alpha1.Group) | AddGroupMember adds a member to a group. |
| RemoveGroupMember | [RemoveGroupMemberRequest](#animeshon.grbac.v1alpha1.RemoveGroupMemberRequest) | [Group](#animeshon.grbac.v1alpha1.Group) | RemoveGroupMember removes a member from a group. |
| DeleteGroup | [DeleteGroupRequest](#animeshon.grbac.v1alpha1.DeleteGroupRequest) | [.google.protobuf.Empty](#google.protobuf.Empty) | DeleteGroup deletes a group. |
| CreatePermission | [CreatePermissionRequest](#animeshon.grbac.v1alpha1.CreatePermissionRequest) | [Permission](#animeshon.grbac.v1alpha1.Permission) | CreatePermission creates a new permission. |
| DeletePermission | [DeletePermissionRequest](#animeshon.grbac.v1alpha1.DeletePermissionRequest) | [.google.protobuf.Empty](#google.protobuf.Empty) | DeletePermission deletes a permission. |
| GetRole | [GetRoleRequest](#animeshon.grbac.v1alpha1.GetRoleRequest) | [Role](#animeshon.grbac.v1alpha1.Role) | GetRole returns a role. |
| CreateRole | [CreateRoleRequest](#animeshon.grbac.v1alpha1.CreateRoleRequest) | [Role](#animeshon.grbac.v1alpha1.Role) | CreateRole creates a new role. |
| UpdateRole | [UpdateRoleRequest](#animeshon.grbac.v1alpha1.UpdateRoleRequest) | [Role](#animeshon.grbac.v1alpha1.Role) | UpdateRole updates a role with a field mask. |
| DeleteRole | [DeleteRoleRequest](#animeshon.grbac.v1alpha1.DeleteRoleRequest) | [.google.protobuf.Empty](#google.protobuf.Empty) | DeleteRole deletes a role. |

 



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

