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

## <span id="animeshon.resourcemanager.v1alpha1.ResourceManager">ResourceManager</span>



| <span id="animeshon.resourcemanager.v1alpha1.ResourceManager.GetOrganization">GetOrganization</span> |
| --- |
| **rpc GetOrganization([GetOrganizationRequest](#animeshon.resourcemanager.v1alpha1.GetOrganizationRequest)) [Organization](#animeshon.resourcemanager.v1alpha1.Organization)**<br/><br/> |

| <span id="animeshon.resourcemanager.v1alpha1.ResourceManager.ListOrganizations">ListOrganizations</span> |
| --- |
| **rpc ListOrganizations([ListOrganizationsRequest](#animeshon.resourcemanager.v1alpha1.ListOrganizationsRequest)) [ListOrganizationsResponse](#animeshon.resourcemanager.v1alpha1.ListOrganizationsResponse)**<br/><br/> |

| <span id="animeshon.resourcemanager.v1alpha1.ResourceManager.CreateOrganization">CreateOrganization</span> |
| --- |
| **rpc CreateOrganization([CreateOrganizationRequest](#animeshon.resourcemanager.v1alpha1.CreateOrganizationRequest)) [Organization](#animeshon.resourcemanager.v1alpha1.Organization)**<br/><br/> |

| <span id="animeshon.resourcemanager.v1alpha1.ResourceManager.UpdateOrganization">UpdateOrganization</span> |
| --- |
| **rpc UpdateOrganization([UpdateOrganizationRequest](#animeshon.resourcemanager.v1alpha1.UpdateOrganizationRequest)) [Organization](#animeshon.resourcemanager.v1alpha1.Organization)**<br/><br/> |

| <span id="animeshon.resourcemanager.v1alpha1.ResourceManager.DeleteOrganization">DeleteOrganization</span> |
| --- |
| **rpc DeleteOrganization([DeleteOrganizationRequest](#animeshon.resourcemanager.v1alpha1.DeleteOrganizationRequest)) [.google.protobuf.Empty](#google.protobuf.Empty)**<br/><br/> |

| <span id="animeshon.resourcemanager.v1alpha1.ResourceManager.GetTeam">GetTeam</span> |
| --- |
| **rpc GetTeam([GetTeamRequest](#animeshon.resourcemanager.v1alpha1.GetTeamRequest)) [Team](#animeshon.resourcemanager.v1alpha1.Team)**<br/><br/> |

| <span id="animeshon.resourcemanager.v1alpha1.ResourceManager.ListTeams">ListTeams</span> |
| --- |
| **rpc ListTeams([ListTeamsRequest](#animeshon.resourcemanager.v1alpha1.ListTeamsRequest)) [ListTeamsResponse](#animeshon.resourcemanager.v1alpha1.ListTeamsResponse)**<br/><br/> |

| <span id="animeshon.resourcemanager.v1alpha1.ResourceManager.CreateTeam">CreateTeam</span> |
| --- |
| **rpc CreateTeam([CreateTeamRequest](#animeshon.resourcemanager.v1alpha1.CreateTeamRequest)) [Team](#animeshon.resourcemanager.v1alpha1.Team)**<br/><br/> |

| <span id="animeshon.resourcemanager.v1alpha1.ResourceManager.UpdateTeam">UpdateTeam</span> |
| --- |
| **rpc UpdateTeam([UpdateTeamRequest](#animeshon.resourcemanager.v1alpha1.UpdateTeamRequest)) [Team](#animeshon.resourcemanager.v1alpha1.Team)**<br/><br/> |

| <span id="animeshon.resourcemanager.v1alpha1.ResourceManager.DeleteTeam">DeleteTeam</span> |
| --- |
| **rpc DeleteTeam([DeleteTeamRequest](#animeshon.resourcemanager.v1alpha1.DeleteTeamRequest)) [.google.protobuf.Empty](#google.protobuf.Empty)**<br/><br/> |


## <span id="animeshon.resourcemanager.v1alpha1.CreateOrganizationRequest">CreateOrganizationRequest</span>



| Field | Description |
| --- | --- |
| organization | **[ Organization](#Organization)**<br/>The organization to create. |

## <span id="animeshon.resourcemanager.v1alpha1.CreateTeamRequest">CreateTeamRequest</span>



| Field | Description |
| --- | --- |
| team | **[ Team](#Team)**<br/>The team to create. |

## <span id="animeshon.resourcemanager.v1alpha1.DeleteOrganizationRequest">DeleteOrganizationRequest</span>



| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the organization to delete. |

## <span id="animeshon.resourcemanager.v1alpha1.DeleteTeamRequest">DeleteTeamRequest</span>



| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the team to delete. |

## <span id="animeshon.resourcemanager.v1alpha1.GetOrganizationRequest">GetOrganizationRequest</span>



| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the organization to retrieve. |

## <span id="animeshon.resourcemanager.v1alpha1.GetTeamRequest">GetTeamRequest</span>



| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the team to retrieve. |

## <span id="animeshon.resourcemanager.v1alpha1.ListOrganizationsRequest">ListOrganizationsRequest</span>



| Field | Description |
| --- | --- |
| page_size | **[ int32](#int32)**<br/>If unspecified, server will pick an appropriate default. |
| page_token | **[ string](#string)**<br/>The value returned from the previous call. |
| filter | **[ string](#string)**<br/>A filter to be applied to results. |

## <span id="animeshon.resourcemanager.v1alpha1.ListOrganizationsResponse">ListOrganizationsResponse</span>



| Field | Description |
| --- | --- |
| organizations | **[repeated Organization](#Organization)**<br/>The list of organizations. |
| next_page_token | **[ string](#string)**<br/>A token to retrieve next page of results. |

## <span id="animeshon.resourcemanager.v1alpha1.ListTeamsRequest">ListTeamsRequest</span>



| Field | Description |
| --- | --- |
| page_size | **[ int32](#int32)**<br/>If unspecified, server will pick an appropriate default. |
| page_token | **[ string](#string)**<br/>The value returned from the previous call. |
| filter | **[ string](#string)**<br/>A filter to be applied to results. |

## <span id="animeshon.resourcemanager.v1alpha1.ListTeamsResponse">ListTeamsResponse</span>



| Field | Description |
| --- | --- |
| teams | **[repeated Team](#Team)**<br/>The list of teams. |
| next_page_token | **[ string](#string)**<br/>A token to retrieve next page of results. |

## <span id="animeshon.resourcemanager.v1alpha1.Organization">Organization</span>



| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/> |

## <span id="animeshon.resourcemanager.v1alpha1.Team">Team</span>



| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/> |

## <span id="animeshon.resourcemanager.v1alpha1.UpdateOrganizationRequest">UpdateOrganizationRequest</span>



| Field | Description |
| --- | --- |
| organization | **[ Organization](#Organization)**<br/>The organization to update. |
| update_mask | **[ google.protobuf.FieldMask](#google.protobuf.FieldMask)**<br/>The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |

## <span id="animeshon.resourcemanager.v1alpha1.UpdateTeamRequest">UpdateTeamRequest</span>



| Field | Description |
| --- | --- |
| team | **[ Team](#Team)**<br/>The team to update. |
| update_mask | **[ google.protobuf.FieldMask](#google.protobuf.FieldMask)**<br/>The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |
