# Package animeshon.grbac.v1alpha1

## Index
- [AccessControl](#animeshon.grbac.v1alpha1.AccessControl)
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

## <span id="animeshon.grbac.v1alpha1.AccessControl">AccessControl</span>

AccessControl is the internal service used by Animeshon to enforce RBAC rules.

| <span id="animeshon.grbac.v1alpha1.AccessControl.TestIamPolicy">TestIamPolicy</span> |
| --- |
| **rpc TestIamPolicy([TestIamPolicyRequest](#animeshon.grbac.v1alpha1.TestIamPolicyRequest)) [.google.protobuf.Empty](#google.protobuf.Empty)**<br/><br/>Checks whether a member has a specific permission for a specific resource. If not allowed an Unauthorized (403) error will be returned. |

| <span id="animeshon.grbac.v1alpha1.AccessControl.GetIamPolicy">GetIamPolicy</span> |
| --- |
| **rpc GetIamPolicy([.google.iam.v1.GetIamPolicyRequest](#google.iam.v1.GetIamPolicyRequest)) [.google.iam.v1.Policy](#google.iam.v1.Policy)**<br/><br/>Gets the IAM policy that is attached to a generic resource. Note: the full resource name that identifies the resource must be provided. |

| <span id="animeshon.grbac.v1alpha1.AccessControl.SetIamPolicy">SetIamPolicy</span> |
| --- |
| **rpc SetIamPolicy([.google.iam.v1.SetIamPolicyRequest](#google.iam.v1.SetIamPolicyRequest)) [.google.iam.v1.Policy](#google.iam.v1.Policy)**<br/><br/>Sets the IAM policy that is attached to a generic resource. Note: the full resource name that identifies the resource must be provided. |

| <span id="animeshon.grbac.v1alpha1.AccessControl.GetResource">GetResource</span> |
| --- |
| **rpc GetResource([GetResourceRequest](#animeshon.grbac.v1alpha1.GetResourceRequest)) [Resource](#animeshon.grbac.v1alpha1.Resource)**<br/><br/>GetResource returns a resource. |

| <span id="animeshon.grbac.v1alpha1.AccessControl.CreateResource">CreateResource</span> |
| --- |
| **rpc CreateResource([CreateResourceRequest](#animeshon.grbac.v1alpha1.CreateResourceRequest)) [Resource](#animeshon.grbac.v1alpha1.Resource)**<br/><br/>CreateResource creates a new resource. |

| <span id="animeshon.grbac.v1alpha1.AccessControl.TransferResource">TransferResource</span> |
| --- |
| **rpc TransferResource([TransferResourceRequest](#animeshon.grbac.v1alpha1.TransferResourceRequest)) [Resource](#animeshon.grbac.v1alpha1.Resource)**<br/><br/>TransferResource transfers a resource to a new parent. |

| <span id="animeshon.grbac.v1alpha1.AccessControl.DeleteResource">DeleteResource</span> |
| --- |
| **rpc DeleteResource([DeleteResourceRequest](#animeshon.grbac.v1alpha1.DeleteResourceRequest)) [.google.protobuf.Empty](#google.protobuf.Empty)**<br/><br/>DeleteResource deletes a resource. |

| <span id="animeshon.grbac.v1alpha1.AccessControl.CreateSubject">CreateSubject</span> |
| --- |
| **rpc CreateSubject([CreateSubjectRequest](#animeshon.grbac.v1alpha1.CreateSubjectRequest)) [Subject](#animeshon.grbac.v1alpha1.Subject)**<br/><br/>CreateSubject creates a new subject. |

| <span id="animeshon.grbac.v1alpha1.AccessControl.DeleteSubject">DeleteSubject</span> |
| --- |
| **rpc DeleteSubject([DeleteSubjectRequest](#animeshon.grbac.v1alpha1.DeleteSubjectRequest)) [.google.protobuf.Empty](#google.protobuf.Empty)**<br/><br/>DeleteSubject deletes a subject. |

| <span id="animeshon.grbac.v1alpha1.AccessControl.GetGroup">GetGroup</span> |
| --- |
| **rpc GetGroup([GetGroupRequest](#animeshon.grbac.v1alpha1.GetGroupRequest)) [Group](#animeshon.grbac.v1alpha1.Group)**<br/><br/>GetGroup returns a group. |

| <span id="animeshon.grbac.v1alpha1.AccessControl.CreateGroup">CreateGroup</span> |
| --- |
| **rpc CreateGroup([CreateGroupRequest](#animeshon.grbac.v1alpha1.CreateGroupRequest)) [Group](#animeshon.grbac.v1alpha1.Group)**<br/><br/>CreateGroup creates a new group. |

| <span id="animeshon.grbac.v1alpha1.AccessControl.UpdateGroup">UpdateGroup</span> |
| --- |
| **rpc UpdateGroup([UpdateGroupRequest](#animeshon.grbac.v1alpha1.UpdateGroupRequest)) [Group](#animeshon.grbac.v1alpha1.Group)**<br/><br/>UpdateGroup updates a group with a field mask. |

| <span id="animeshon.grbac.v1alpha1.AccessControl.AddGroupMember">AddGroupMember</span> |
| --- |
| **rpc AddGroupMember([AddGroupMemberRequest](#animeshon.grbac.v1alpha1.AddGroupMemberRequest)) [Group](#animeshon.grbac.v1alpha1.Group)**<br/><br/>AddGroupMember adds a member to a group. |

| <span id="animeshon.grbac.v1alpha1.AccessControl.RemoveGroupMember">RemoveGroupMember</span> |
| --- |
| **rpc RemoveGroupMember([RemoveGroupMemberRequest](#animeshon.grbac.v1alpha1.RemoveGroupMemberRequest)) [Group](#animeshon.grbac.v1alpha1.Group)**<br/><br/>RemoveGroupMember removes a member from a group. |

| <span id="animeshon.grbac.v1alpha1.AccessControl.DeleteGroup">DeleteGroup</span> |
| --- |
| **rpc DeleteGroup([DeleteGroupRequest](#animeshon.grbac.v1alpha1.DeleteGroupRequest)) [.google.protobuf.Empty](#google.protobuf.Empty)**<br/><br/>DeleteGroup deletes a group. |

| <span id="animeshon.grbac.v1alpha1.AccessControl.CreatePermission">CreatePermission</span> |
| --- |
| **rpc CreatePermission([CreatePermissionRequest](#animeshon.grbac.v1alpha1.CreatePermissionRequest)) [Permission](#animeshon.grbac.v1alpha1.Permission)**<br/><br/>CreatePermission creates a new permission. |

| <span id="animeshon.grbac.v1alpha1.AccessControl.DeletePermission">DeletePermission</span> |
| --- |
| **rpc DeletePermission([DeletePermissionRequest](#animeshon.grbac.v1alpha1.DeletePermissionRequest)) [.google.protobuf.Empty](#google.protobuf.Empty)**<br/><br/>DeletePermission deletes a permission. |

| <span id="animeshon.grbac.v1alpha1.AccessControl.GetRole">GetRole</span> |
| --- |
| **rpc GetRole([GetRoleRequest](#animeshon.grbac.v1alpha1.GetRoleRequest)) [Role](#animeshon.grbac.v1alpha1.Role)**<br/><br/>GetRole returns a role. |

| <span id="animeshon.grbac.v1alpha1.AccessControl.CreateRole">CreateRole</span> |
| --- |
| **rpc CreateRole([CreateRoleRequest](#animeshon.grbac.v1alpha1.CreateRoleRequest)) [Role](#animeshon.grbac.v1alpha1.Role)**<br/><br/>CreateRole creates a new role. |

| <span id="animeshon.grbac.v1alpha1.AccessControl.UpdateRole">UpdateRole</span> |
| --- |
| **rpc UpdateRole([UpdateRoleRequest](#animeshon.grbac.v1alpha1.UpdateRoleRequest)) [Role](#animeshon.grbac.v1alpha1.Role)**<br/><br/>UpdateRole updates a role with a field mask. |

| <span id="animeshon.grbac.v1alpha1.AccessControl.DeleteRole">DeleteRole</span> |
| --- |
| **rpc DeleteRole([DeleteRoleRequest](#animeshon.grbac.v1alpha1.DeleteRoleRequest)) [.google.protobuf.Empty](#google.protobuf.Empty)**<br/><br/>DeleteRole deletes a role. |


## <span id="animeshon.grbac.v1alpha1.AccessTuple">AccessTuple</span>

Information about the member, resource, and permission to check.

| Field | Description |
| --- | --- |
| principal | **[ string](#string)**<br/>The member, or principal, whose access you want to check. |
| full_resource_name | **[ string](#string)**<br/>The full resource name that identifies the resource. |
| permission | **[ string](#string)**<br/>The IAM permission to check for the specified member and resource. |

## <span id="animeshon.grbac.v1alpha1.AddGroupMemberRequest">AddGroupMemberRequest</span>



| Field | Description |
| --- | --- |
| group | **[ string](#string)**<br/>The name of the group to add a member to. |
| member | **[ string](#string)**<br/>The member to be added. |

## <span id="animeshon.grbac.v1alpha1.CreateGroupRequest">CreateGroupRequest</span>



| Field | Description |
| --- | --- |
| group | **[ Group](#Group)**<br/>The group to create. |

## <span id="animeshon.grbac.v1alpha1.CreatePermissionRequest">CreatePermissionRequest</span>



| Field | Description |
| --- | --- |
| permission | **[ Permission](#Permission)**<br/>The permission to create. |

## <span id="animeshon.grbac.v1alpha1.CreateResourceRequest">CreateResourceRequest</span>



| Field | Description |
| --- | --- |
| resource | **[ Resource](#Resource)**<br/>The resource to create. |

## <span id="animeshon.grbac.v1alpha1.CreateRoleRequest">CreateRoleRequest</span>



| Field | Description |
| --- | --- |
| role | **[ Role](#Role)**<br/>The role to create. |

## <span id="animeshon.grbac.v1alpha1.CreateSubjectRequest">CreateSubjectRequest</span>



| Field | Description |
| --- | --- |
| subject | **[ Subject](#Subject)**<br/>The subject to create. |

## <span id="animeshon.grbac.v1alpha1.DeleteGroupRequest">DeleteGroupRequest</span>



| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the group to delete. |

## <span id="animeshon.grbac.v1alpha1.DeletePermissionRequest">DeletePermissionRequest</span>



| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the permission to delete. |

## <span id="animeshon.grbac.v1alpha1.DeleteResourceRequest">DeleteResourceRequest</span>



| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The full resource name that identifies the resource. |

## <span id="animeshon.grbac.v1alpha1.DeleteRoleRequest">DeleteRoleRequest</span>



| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the role to delete. |

## <span id="animeshon.grbac.v1alpha1.DeleteSubjectRequest">DeleteSubjectRequest</span>



| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The subject to delete. |

## <span id="animeshon.grbac.v1alpha1.GetGroupRequest">GetGroupRequest</span>



| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the group to retrieve. |

## <span id="animeshon.grbac.v1alpha1.GetResourceRequest">GetResourceRequest</span>



| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The full resource name of the resource to retrieve. |

## <span id="animeshon.grbac.v1alpha1.GetRoleRequest">GetRoleRequest</span>



| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the role to retrieve. |

## <span id="animeshon.grbac.v1alpha1.Group">Group</span>



| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the group. |
| members | **[repeated string](#string)**<br/>The list of members of the group. Groups might include other groups. |
| etag | **[ bytes](#bytes)**<br/>An etag for concurrency control, ignored during creation. |

## <span id="animeshon.grbac.v1alpha1.Permission">Permission</span>



| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the permission. |

## <span id="animeshon.grbac.v1alpha1.RemoveGroupMemberRequest">RemoveGroupMemberRequest</span>



| Field | Description |
| --- | --- |
| group | **[ string](#string)**<br/>The name of the group to remove an member from. |
| member | **[ string](#string)**<br/>The member to be removed. |

## <span id="animeshon.grbac.v1alpha1.Resource">Resource</span>



| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The full resource name that identifies the resource. |
| parent | **[ string](#string)**<br/>The full resource name that identifies the parent resource. |
| etag | **[ bytes](#bytes)**<br/>An etag for concurrency control, ignored during creation. |

## <span id="animeshon.grbac.v1alpha1.Role">Role</span>



| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the role. |
| permissions | **[repeated string](#string)**<br/>The list of permissions granted by the role. |
| etag | **[ bytes](#bytes)**<br/>An etag for concurrency control, ignored during creation. |

## <span id="animeshon.grbac.v1alpha1.Subject">Subject</span>



| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the subject. |

## <span id="animeshon.grbac.v1alpha1.TestIamPolicyRequest">TestIamPolicyRequest</span>



| Field | Description |
| --- | --- |
| access_tuple | **[ AccessTuple](#AccessTuple)**<br/>The information to use for checking whether a member has a permission for a resource. |

## <span id="animeshon.grbac.v1alpha1.TransferResourceRequest">TransferResourceRequest</span>



| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The full resource name that identifies the resource. |
| target_parent | **[ string](#string)**<br/>The full resource name that identifies the new parent resource. |
| substitutions | **[map TransferResourceRequest.SubstitutionsEntry](#TransferResourceRequest.SubstitutionsEntry)**<br/>The map of substitutions to apply to the full resource name and all of its children.

As an example, it might be required to change the parent of a resource from "users/123" to "users/678", the substitutions would then look like this:

substitutions = {"users/123": "users/456789"}

and the expected result would then be the following:

from : //abc.animeapis.com/users/123/resources/210 to : //abc.animeapis.com/users/456789/resources/210

The same applies if we need to transfer a resource between two parents of different type:

substitutions = {"users/123": "organizations/678/teams/987"}

and the expected result would then be the following:

from : //abc.animeapis.com/users/123/resources/210 to : //abc.animeapis.com/organizations/678/teams/987/resources/210

It is possible to apply multiple substitutions simultaneously. |

## <span id="animeshon.grbac.v1alpha1.TransferResourceRequest.SubstitutionsEntry">TransferResourceRequest.SubstitutionsEntry</span>



| Field | Description |
| --- | --- |
| key | **[ string](#string)**<br/> |
| value | **[ string](#string)**<br/> |

## <span id="animeshon.grbac.v1alpha1.UpdateGroupRequest">UpdateGroupRequest</span>



| Field | Description |
| --- | --- |
| group | **[ Group](#Group)**<br/>The group to update. |
| update_mask | **[ google.protobuf.FieldMask](#google.protobuf.FieldMask)**<br/>The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |

## <span id="animeshon.grbac.v1alpha1.UpdateRoleRequest">UpdateRoleRequest</span>



| Field | Description |
| --- | --- |
| role | **[ Role](#Role)**<br/>The role to update. |
| update_mask | **[ google.protobuf.FieldMask](#google.protobuf.FieldMask)**<br/>The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |
