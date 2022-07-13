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

## AccessControl {#animeshon.grbac.v1alpha1.AccessControl}
AccessControl is the internal service used by Animeshon to enforce RBAC rules.
| TestIamPolicy |
| --- |
| **rpc** TestIamPolicy([TestIamPolicyRequest](#animeshon.grbac.v1alpha1.TestIamPolicyRequest)) [.google.protobuf.Empty](#google.protobuf.Empty)<br/>Checks whether a member has a specific permission for a specific resource. If not allowed an Unauthorized (403) error will be returned. |

| GetIamPolicy |
| --- |
| **rpc** GetIamPolicy([.google.iam.v1.GetIamPolicyRequest](#google.iam.v1.GetIamPolicyRequest)) [.google.iam.v1.Policy](#google.iam.v1.Policy)<br/>Gets the IAM policy that is attached to a generic resource. Note: the full resource name that identifies the resource must be provided. |

| SetIamPolicy |
| --- |
| **rpc** SetIamPolicy([.google.iam.v1.SetIamPolicyRequest](#google.iam.v1.SetIamPolicyRequest)) [.google.iam.v1.Policy](#google.iam.v1.Policy)<br/>Sets the IAM policy that is attached to a generic resource. Note: the full resource name that identifies the resource must be provided. |

| GetResource |
| --- |
| **rpc** GetResource([GetResourceRequest](#animeshon.grbac.v1alpha1.GetResourceRequest)) [Resource](#animeshon.grbac.v1alpha1.Resource)<br/>GetResource returns a resource. |

| CreateResource |
| --- |
| **rpc** CreateResource([CreateResourceRequest](#animeshon.grbac.v1alpha1.CreateResourceRequest)) [Resource](#animeshon.grbac.v1alpha1.Resource)<br/>CreateResource creates a new resource. |

| TransferResource |
| --- |
| **rpc** TransferResource([TransferResourceRequest](#animeshon.grbac.v1alpha1.TransferResourceRequest)) [Resource](#animeshon.grbac.v1alpha1.Resource)<br/>TransferResource transfers a resource to a new parent. |

| DeleteResource |
| --- |
| **rpc** DeleteResource([DeleteResourceRequest](#animeshon.grbac.v1alpha1.DeleteResourceRequest)) [.google.protobuf.Empty](#google.protobuf.Empty)<br/>DeleteResource deletes a resource. |

| CreateSubject |
| --- |
| **rpc** CreateSubject([CreateSubjectRequest](#animeshon.grbac.v1alpha1.CreateSubjectRequest)) [Subject](#animeshon.grbac.v1alpha1.Subject)<br/>CreateSubject creates a new subject. |

| DeleteSubject |
| --- |
| **rpc** DeleteSubject([DeleteSubjectRequest](#animeshon.grbac.v1alpha1.DeleteSubjectRequest)) [.google.protobuf.Empty](#google.protobuf.Empty)<br/>DeleteSubject deletes a subject. |

| GetGroup |
| --- |
| **rpc** GetGroup([GetGroupRequest](#animeshon.grbac.v1alpha1.GetGroupRequest)) [Group](#animeshon.grbac.v1alpha1.Group)<br/>GetGroup returns a group. |

| CreateGroup |
| --- |
| **rpc** CreateGroup([CreateGroupRequest](#animeshon.grbac.v1alpha1.CreateGroupRequest)) [Group](#animeshon.grbac.v1alpha1.Group)<br/>CreateGroup creates a new group. |

| UpdateGroup |
| --- |
| **rpc** UpdateGroup([UpdateGroupRequest](#animeshon.grbac.v1alpha1.UpdateGroupRequest)) [Group](#animeshon.grbac.v1alpha1.Group)<br/>UpdateGroup updates a group with a field mask. |

| AddGroupMember |
| --- |
| **rpc** AddGroupMember([AddGroupMemberRequest](#animeshon.grbac.v1alpha1.AddGroupMemberRequest)) [Group](#animeshon.grbac.v1alpha1.Group)<br/>AddGroupMember adds a member to a group. |

| RemoveGroupMember |
| --- |
| **rpc** RemoveGroupMember([RemoveGroupMemberRequest](#animeshon.grbac.v1alpha1.RemoveGroupMemberRequest)) [Group](#animeshon.grbac.v1alpha1.Group)<br/>RemoveGroupMember removes a member from a group. |

| DeleteGroup |
| --- |
| **rpc** DeleteGroup([DeleteGroupRequest](#animeshon.grbac.v1alpha1.DeleteGroupRequest)) [.google.protobuf.Empty](#google.protobuf.Empty)<br/>DeleteGroup deletes a group. |

| CreatePermission |
| --- |
| **rpc** CreatePermission([CreatePermissionRequest](#animeshon.grbac.v1alpha1.CreatePermissionRequest)) [Permission](#animeshon.grbac.v1alpha1.Permission)<br/>CreatePermission creates a new permission. |

| DeletePermission |
| --- |
| **rpc** DeletePermission([DeletePermissionRequest](#animeshon.grbac.v1alpha1.DeletePermissionRequest)) [.google.protobuf.Empty](#google.protobuf.Empty)<br/>DeletePermission deletes a permission. |

| GetRole |
| --- |
| **rpc** GetRole([GetRoleRequest](#animeshon.grbac.v1alpha1.GetRoleRequest)) [Role](#animeshon.grbac.v1alpha1.Role)<br/>GetRole returns a role. |

| CreateRole |
| --- |
| **rpc** CreateRole([CreateRoleRequest](#animeshon.grbac.v1alpha1.CreateRoleRequest)) [Role](#animeshon.grbac.v1alpha1.Role)<br/>CreateRole creates a new role. |

| UpdateRole |
| --- |
| **rpc** UpdateRole([UpdateRoleRequest](#animeshon.grbac.v1alpha1.UpdateRoleRequest)) [Role](#animeshon.grbac.v1alpha1.Role)<br/>UpdateRole updates a role with a field mask. |

| DeleteRole |
| --- |
| **rpc** DeleteRole([DeleteRoleRequest](#animeshon.grbac.v1alpha1.DeleteRoleRequest)) [.google.protobuf.Empty](#google.protobuf.Empty)<br/>DeleteRole deletes a role. |

## AccessTuple {#animeshon.grbac.v1alpha1.AccessTuple}
Information about the member, resource, and permission to check.
| Field | Description |
| --- | --- |
| principal | **[ string](#string)**<br/>The member, or principal, whose access you want to check. |
| full_resource_name | **[ string](#string)**<br/>The full resource name that identifies the resource. |
| permission | **[ string](#string)**<br/>The IAM permission to check for the specified member and resource. |
## AddGroupMemberRequest {#animeshon.grbac.v1alpha1.AddGroupMemberRequest}

| Field | Description |
| --- | --- |
| group | **[ string](#string)**<br/>The name of the group to add a member to. |
| member | **[ string](#string)**<br/>The member to be added. |
## CreateGroupRequest {#animeshon.grbac.v1alpha1.CreateGroupRequest}

| Field | Description |
| --- | --- |
| group | **[ Group](#Group)**<br/>The group to create. |
## CreatePermissionRequest {#animeshon.grbac.v1alpha1.CreatePermissionRequest}

| Field | Description |
| --- | --- |
| permission | **[ Permission](#Permission)**<br/>The permission to create. |
## CreateResourceRequest {#animeshon.grbac.v1alpha1.CreateResourceRequest}

| Field | Description |
| --- | --- |
| resource | **[ Resource](#Resource)**<br/>The resource to create. |
## CreateRoleRequest {#animeshon.grbac.v1alpha1.CreateRoleRequest}

| Field | Description |
| --- | --- |
| role | **[ Role](#Role)**<br/>The role to create. |
## CreateSubjectRequest {#animeshon.grbac.v1alpha1.CreateSubjectRequest}

| Field | Description |
| --- | --- |
| subject | **[ Subject](#Subject)**<br/>The subject to create. |
## DeleteGroupRequest {#animeshon.grbac.v1alpha1.DeleteGroupRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the group to delete. |
## DeletePermissionRequest {#animeshon.grbac.v1alpha1.DeletePermissionRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the permission to delete. |
## DeleteResourceRequest {#animeshon.grbac.v1alpha1.DeleteResourceRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The full resource name that identifies the resource. |
## DeleteRoleRequest {#animeshon.grbac.v1alpha1.DeleteRoleRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the role to delete. |
## DeleteSubjectRequest {#animeshon.grbac.v1alpha1.DeleteSubjectRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The subject to delete. |
## GetGroupRequest {#animeshon.grbac.v1alpha1.GetGroupRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the group to retrieve. |
## GetResourceRequest {#animeshon.grbac.v1alpha1.GetResourceRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The full resource name of the resource to retrieve. |
## GetRoleRequest {#animeshon.grbac.v1alpha1.GetRoleRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the role to retrieve. |
## Group {#animeshon.grbac.v1alpha1.Group}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the group. |
| members | **[repeated string](#string)**<br/>The list of members of the group. Groups might include other groups. |
| etag | **[ bytes](#bytes)**<br/>An etag for concurrency control, ignored during creation. |
## Permission {#animeshon.grbac.v1alpha1.Permission}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the permission. |
## RemoveGroupMemberRequest {#animeshon.grbac.v1alpha1.RemoveGroupMemberRequest}

| Field | Description |
| --- | --- |
| group | **[ string](#string)**<br/>The name of the group to remove an member from. |
| member | **[ string](#string)**<br/>The member to be removed. |
## Resource {#animeshon.grbac.v1alpha1.Resource}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The full resource name that identifies the resource. |
| parent | **[ string](#string)**<br/>The full resource name that identifies the parent resource. |
| etag | **[ bytes](#bytes)**<br/>An etag for concurrency control, ignored during creation. |
## Role {#animeshon.grbac.v1alpha1.Role}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the role. |
| permissions | **[repeated string](#string)**<br/>The list of permissions granted by the role. |
| etag | **[ bytes](#bytes)**<br/>An etag for concurrency control, ignored during creation. |
## Subject {#animeshon.grbac.v1alpha1.Subject}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the subject. |
## TestIamPolicyRequest {#animeshon.grbac.v1alpha1.TestIamPolicyRequest}

| Field | Description |
| --- | --- |
| access_tuple | **[ AccessTuple](#AccessTuple)**<br/>The information to use for checking whether a member has a permission for a resource. |
## TransferResourceRequest {#animeshon.grbac.v1alpha1.TransferResourceRequest}

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
## TransferResourceRequest.SubstitutionsEntry {#animeshon.grbac.v1alpha1.TransferResourceRequest.SubstitutionsEntry}

| Field | Description |
| --- | --- |
| key | **[ string](#string)**<br/> |
| value | **[ string](#string)**<br/> |
## UpdateGroupRequest {#animeshon.grbac.v1alpha1.UpdateGroupRequest}

| Field | Description |
| --- | --- |
| group | **[ Group](#Group)**<br/>The group to update. |
| update_mask | **[ google.protobuf.FieldMask](#google.protobuf.FieldMask)**<br/>The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |
## UpdateRoleRequest {#animeshon.grbac.v1alpha1.UpdateRoleRequest}

| Field | Description |
| --- | --- |
| role | **[ Role](#Role)**<br/>The role to update. |
| update_mask | **[ google.protobuf.FieldMask](#google.protobuf.FieldMask)**<br/>The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |
