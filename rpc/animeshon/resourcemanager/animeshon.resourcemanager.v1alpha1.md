# Package animeshon.resourcemanager.v1alpha1

## Index
- [ResourceManager](#animeshon.resourcemanager.v1alpha1.ResourceManager)
- [CreateOrganizationRequest](#animeshon.resourcemanager.v1alpha1.CreateOrganizationRequest)
- [CreateTeamRequest](#animeshon.resourcemanager.v1alpha1.CreateTeamRequest)
- [DeleteOrganizationRequest](#animeshon.resourcemanager.v1alpha1.DeleteOrganizationRequest)
- [DeleteTeamRequest](#animeshon.resourcemanager.v1alpha1.DeleteTeamRequest)
- [GetOrganizationRequest](#animeshon.resourcemanager.v1alpha1.GetOrganizationRequest)
- [GetTeamRequest](#animeshon.resourcemanager.v1alpha1.GetTeamRequest)
- [ListOrganizationsRequest](#animeshon.resourcemanager.v1alpha1.ListOrganizationsRequest)
- [ListOrganizationsResponse](#animeshon.resourcemanager.v1alpha1.ListOrganizationsResponse)
- [ListTeamsRequest](#animeshon.resourcemanager.v1alpha1.ListTeamsRequest)
- [ListTeamsResponse](#animeshon.resourcemanager.v1alpha1.ListTeamsResponse)
- [Organization](#animeshon.resourcemanager.v1alpha1.Organization)
- [Team](#animeshon.resourcemanager.v1alpha1.Team)
- [UpdateOrganizationRequest](#animeshon.resourcemanager.v1alpha1.UpdateOrganizationRequest)
- [UpdateTeamRequest](#animeshon.resourcemanager.v1alpha1.UpdateTeamRequest)

## ResourceManager {#animeshon.resourcemanager.v1alpha1.ResourceManager}

| GetOrganization |
| --- |
| **rpc** GetOrganization([GetOrganizationRequest](#animeshon.resourcemanager.v1alpha1.GetOrganizationRequest)) [Organization](#animeshon.resourcemanager.v1alpha1.Organization)<br/> |

| ListOrganizations |
| --- |
| **rpc** ListOrganizations([ListOrganizationsRequest](#animeshon.resourcemanager.v1alpha1.ListOrganizationsRequest)) [ListOrganizationsResponse](#animeshon.resourcemanager.v1alpha1.ListOrganizationsResponse)<br/> |

| CreateOrganization |
| --- |
| **rpc** CreateOrganization([CreateOrganizationRequest](#animeshon.resourcemanager.v1alpha1.CreateOrganizationRequest)) [Organization](#animeshon.resourcemanager.v1alpha1.Organization)<br/> |

| UpdateOrganization |
| --- |
| **rpc** UpdateOrganization([UpdateOrganizationRequest](#animeshon.resourcemanager.v1alpha1.UpdateOrganizationRequest)) [Organization](#animeshon.resourcemanager.v1alpha1.Organization)<br/> |

| DeleteOrganization |
| --- |
| **rpc** DeleteOrganization([DeleteOrganizationRequest](#animeshon.resourcemanager.v1alpha1.DeleteOrganizationRequest)) [.google.protobuf.Empty](#google.protobuf.Empty)<br/> |

| GetTeam |
| --- |
| **rpc** GetTeam([GetTeamRequest](#animeshon.resourcemanager.v1alpha1.GetTeamRequest)) [Team](#animeshon.resourcemanager.v1alpha1.Team)<br/> |

| ListTeams |
| --- |
| **rpc** ListTeams([ListTeamsRequest](#animeshon.resourcemanager.v1alpha1.ListTeamsRequest)) [ListTeamsResponse](#animeshon.resourcemanager.v1alpha1.ListTeamsResponse)<br/> |

| CreateTeam |
| --- |
| **rpc** CreateTeam([CreateTeamRequest](#animeshon.resourcemanager.v1alpha1.CreateTeamRequest)) [Team](#animeshon.resourcemanager.v1alpha1.Team)<br/> |

| UpdateTeam |
| --- |
| **rpc** UpdateTeam([UpdateTeamRequest](#animeshon.resourcemanager.v1alpha1.UpdateTeamRequest)) [Team](#animeshon.resourcemanager.v1alpha1.Team)<br/> |

| DeleteTeam |
| --- |
| **rpc** DeleteTeam([DeleteTeamRequest](#animeshon.resourcemanager.v1alpha1.DeleteTeamRequest)) [.google.protobuf.Empty](#google.protobuf.Empty)<br/> |

## CreateOrganizationRequest {#animeshon.resourcemanager.v1alpha1.CreateOrganizationRequest}

| Field | Description |
| --- | --- |
| organization | **[ Organization](#Organization)**<br/>The organization to create. |
## CreateTeamRequest {#animeshon.resourcemanager.v1alpha1.CreateTeamRequest}

| Field | Description |
| --- | --- |
| team | **[ Team](#Team)**<br/>The team to create. |
## DeleteOrganizationRequest {#animeshon.resourcemanager.v1alpha1.DeleteOrganizationRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the organization to delete. |
## DeleteTeamRequest {#animeshon.resourcemanager.v1alpha1.DeleteTeamRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the team to delete. |
## GetOrganizationRequest {#animeshon.resourcemanager.v1alpha1.GetOrganizationRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the organization to retrieve. |
## GetTeamRequest {#animeshon.resourcemanager.v1alpha1.GetTeamRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the team to retrieve. |
## ListOrganizationsRequest {#animeshon.resourcemanager.v1alpha1.ListOrganizationsRequest}

| Field | Description |
| --- | --- |
| page_size | **[ int32](#int32)**<br/>If unspecified, server will pick an appropriate default. |
| page_token | **[ string](#string)**<br/>The value returned from the previous call. |
| filter | **[ string](#string)**<br/>A filter to be applied to results. |
## ListOrganizationsResponse {#animeshon.resourcemanager.v1alpha1.ListOrganizationsResponse}

| Field | Description |
| --- | --- |
| organizations | **[repeated Organization](#Organization)**<br/>The list of organizations. |
| next_page_token | **[ string](#string)**<br/>A token to retrieve next page of results. |
## ListTeamsRequest {#animeshon.resourcemanager.v1alpha1.ListTeamsRequest}

| Field | Description |
| --- | --- |
| page_size | **[ int32](#int32)**<br/>If unspecified, server will pick an appropriate default. |
| page_token | **[ string](#string)**<br/>The value returned from the previous call. |
| filter | **[ string](#string)**<br/>A filter to be applied to results. |
## ListTeamsResponse {#animeshon.resourcemanager.v1alpha1.ListTeamsResponse}

| Field | Description |
| --- | --- |
| teams | **[repeated Team](#Team)**<br/>The list of teams. |
| next_page_token | **[ string](#string)**<br/>A token to retrieve next page of results. |
## Organization {#animeshon.resourcemanager.v1alpha1.Organization}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/> |
## Team {#animeshon.resourcemanager.v1alpha1.Team}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/> |
## UpdateOrganizationRequest {#animeshon.resourcemanager.v1alpha1.UpdateOrganizationRequest}

| Field | Description |
| --- | --- |
| organization | **[ Organization](#Organization)**<br/>The organization to update. |
| update_mask | **[ google.protobuf.FieldMask](#google.protobuf.FieldMask)**<br/>The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |
## UpdateTeamRequest {#animeshon.resourcemanager.v1alpha1.UpdateTeamRequest}

| Field | Description |
| --- | --- |
| team | **[ Team](#Team)**<br/>The team to update. |
| update_mask | **[ google.protobuf.FieldMask](#google.protobuf.FieldMask)**<br/>The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |
