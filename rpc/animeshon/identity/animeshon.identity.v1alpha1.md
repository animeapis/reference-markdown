# Package animeshon.identity.v1alpha1

## Index
- [Identity](#animeshon.identity.v1alpha1.Identity)
- [CreateGroupRequest](#animeshon.identity.v1alpha1.CreateGroupRequest)
- [CreateUserRequest](#animeshon.identity.v1alpha1.CreateUserRequest)
- [DeleteGroupRequest](#animeshon.identity.v1alpha1.DeleteGroupRequest)
- [DeleteUserRequest](#animeshon.identity.v1alpha1.DeleteUserRequest)
- [GetGroupRequest](#animeshon.identity.v1alpha1.GetGroupRequest)
- [GetUserDefaultsRequest](#animeshon.identity.v1alpha1.GetUserDefaultsRequest)
- [GetUserNotificationsRequest](#animeshon.identity.v1alpha1.GetUserNotificationsRequest)
- [GetUserProfileRequest](#animeshon.identity.v1alpha1.GetUserProfileRequest)
- [GetUserRequest](#animeshon.identity.v1alpha1.GetUserRequest)
- [GetUserSettingsRequest](#animeshon.identity.v1alpha1.GetUserSettingsRequest)
- [Group](#animeshon.identity.v1alpha1.Group)
- [ListGroupsRequest](#animeshon.identity.v1alpha1.ListGroupsRequest)
- [ListGroupsResponse](#animeshon.identity.v1alpha1.ListGroupsResponse)
- [ListUsersRequest](#animeshon.identity.v1alpha1.ListUsersRequest)
- [ListUsersResponse](#animeshon.identity.v1alpha1.ListUsersResponse)
- [UpdateGroupRequest](#animeshon.identity.v1alpha1.UpdateGroupRequest)
- [UpdateUserNotificationsRequest](#animeshon.identity.v1alpha1.UpdateUserNotificationsRequest)
- [UpdateUserRequest](#animeshon.identity.v1alpha1.UpdateUserRequest)
- [UpdateUserSettingsRequest](#animeshon.identity.v1alpha1.UpdateUserSettingsRequest)
- [User](#animeshon.identity.v1alpha1.User)
- [UserDefaults](#animeshon.identity.v1alpha1.UserDefaults)
- [UserNotifications](#animeshon.identity.v1alpha1.UserNotifications)
- [UserProfile](#animeshon.identity.v1alpha1.UserProfile)
- [UserSettings](#animeshon.identity.v1alpha1.UserSettings)

- [Gender](#animeshon.identity.v1alpha1.Gender)
- [UserSettings.Visibility](#animeshon.identity.v1alpha1.UserSettings.Visibility)
## Identity {#animeshon.identity.v1alpha1.Identity}

| GetUserProfile |
| --- |
| **rpc** GetUserProfile([GetUserProfileRequest](#animeshon.identity.v1alpha1.GetUserProfileRequest)) [UserProfile](#animeshon.identity.v1alpha1.UserProfile)<br/> |

| GetUser |
| --- |
| **rpc** GetUser([GetUserRequest](#animeshon.identity.v1alpha1.GetUserRequest)) [User](#animeshon.identity.v1alpha1.User)<br/> |

| ListUsers |
| --- |
| **rpc** ListUsers([ListUsersRequest](#animeshon.identity.v1alpha1.ListUsersRequest)) [ListUsersResponse](#animeshon.identity.v1alpha1.ListUsersResponse)<br/> |

| CreateUser |
| --- |
| **rpc** CreateUser([CreateUserRequest](#animeshon.identity.v1alpha1.CreateUserRequest)) [User](#animeshon.identity.v1alpha1.User)<br/> |

| UpdateUser |
| --- |
| **rpc** UpdateUser([UpdateUserRequest](#animeshon.identity.v1alpha1.UpdateUserRequest)) [User](#animeshon.identity.v1alpha1.User)<br/> |

| DeleteUser |
| --- |
| **rpc** DeleteUser([DeleteUserRequest](#animeshon.identity.v1alpha1.DeleteUserRequest)) [.google.protobuf.Empty](#google.protobuf.Empty)<br/> |

| GetUserSettings |
| --- |
| **rpc** GetUserSettings([GetUserSettingsRequest](#animeshon.identity.v1alpha1.GetUserSettingsRequest)) [UserSettings](#animeshon.identity.v1alpha1.UserSettings)<br/> |

| UpdateUserSettings |
| --- |
| **rpc** UpdateUserSettings([UpdateUserSettingsRequest](#animeshon.identity.v1alpha1.UpdateUserSettingsRequest)) [UserSettings](#animeshon.identity.v1alpha1.UserSettings)<br/> |

| GetUserNotifications |
| --- |
| **rpc** GetUserNotifications([GetUserNotificationsRequest](#animeshon.identity.v1alpha1.GetUserNotificationsRequest)) [UserNotifications](#animeshon.identity.v1alpha1.UserNotifications)<br/> |

| UpdateUserNotifications |
| --- |
| **rpc** UpdateUserNotifications([UpdateUserNotificationsRequest](#animeshon.identity.v1alpha1.UpdateUserNotificationsRequest)) [UserNotifications](#animeshon.identity.v1alpha1.UserNotifications)<br/> |

| GetUserDefaults |
| --- |
| **rpc** GetUserDefaults([GetUserDefaultsRequest](#animeshon.identity.v1alpha1.GetUserDefaultsRequest)) [UserDefaults](#animeshon.identity.v1alpha1.UserDefaults)<br/> |

| GetGroup |
| --- |
| **rpc** GetGroup([GetGroupRequest](#animeshon.identity.v1alpha1.GetGroupRequest)) [Group](#animeshon.identity.v1alpha1.Group)<br/> |

| ListGroups |
| --- |
| **rpc** ListGroups([ListGroupsRequest](#animeshon.identity.v1alpha1.ListGroupsRequest)) [ListGroupsResponse](#animeshon.identity.v1alpha1.ListGroupsResponse)<br/> |

| CreateGroup |
| --- |
| **rpc** CreateGroup([CreateGroupRequest](#animeshon.identity.v1alpha1.CreateGroupRequest)) [Group](#animeshon.identity.v1alpha1.Group)<br/> |

| UpdateGroup |
| --- |
| **rpc** UpdateGroup([UpdateGroupRequest](#animeshon.identity.v1alpha1.UpdateGroupRequest)) [Group](#animeshon.identity.v1alpha1.Group)<br/> |

| DeleteGroup |
| --- |
| **rpc** DeleteGroup([DeleteGroupRequest](#animeshon.identity.v1alpha1.DeleteGroupRequest)) [.google.protobuf.Empty](#google.protobuf.Empty)<br/> |

## CreateGroupRequest {#animeshon.identity.v1alpha1.CreateGroupRequest}

| Field | Description |
| --- | --- |
| group | **[ Group](#Group)**<br/>The group to create. |
## CreateUserRequest {#animeshon.identity.v1alpha1.CreateUserRequest}

| Field | Description |
| --- | --- |
| user | **[ User](#User)**<br/>The user to create. |
## DeleteGroupRequest {#animeshon.identity.v1alpha1.DeleteGroupRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the group to delete. |
## DeleteUserRequest {#animeshon.identity.v1alpha1.DeleteUserRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the user to delete. |
## GetGroupRequest {#animeshon.identity.v1alpha1.GetGroupRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the group to retrieve. |
## GetUserDefaultsRequest {#animeshon.identity.v1alpha1.GetUserDefaultsRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the user to retrieve the defaults from. |
## GetUserNotificationsRequest {#animeshon.identity.v1alpha1.GetUserNotificationsRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the user to retrieve the notifications from. |
## GetUserProfileRequest {#animeshon.identity.v1alpha1.GetUserProfileRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the user to retrieve the profile from. |
## GetUserRequest {#animeshon.identity.v1alpha1.GetUserRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the user to retrieve. |
## GetUserSettingsRequest {#animeshon.identity.v1alpha1.GetUserSettingsRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The name of the user to retrieve the settings from. |
## Group {#animeshon.identity.v1alpha1.Group}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the group. |
| members | **[repeated string](#string)**<br/>The list of members of the group. Groups might include other groups. |
| etag | **[ bytes](#bytes)**<br/>An etag for concurrency control, ignored during creation. |
## ListGroupsRequest {#animeshon.identity.v1alpha1.ListGroupsRequest}

| Field | Description |
| --- | --- |
| page_size | **[ int32](#int32)**<br/>If unspecified, server will pick an appropriate default. |
| page_token | **[ string](#string)**<br/>The value returned from the previous call. |
| filter | **[ string](#string)**<br/>A filter to be applied to results. |
## ListGroupsResponse {#animeshon.identity.v1alpha1.ListGroupsResponse}

| Field | Description |
| --- | --- |
| groups | **[repeated Group](#Group)**<br/>The list of groups. |
| next_page_token | **[ string](#string)**<br/>A token to retrieve next page of results. |
## ListUsersRequest {#animeshon.identity.v1alpha1.ListUsersRequest}

| Field | Description |
| --- | --- |
| page_size | **[ int32](#int32)**<br/>If unspecified, server will pick an appropriate default. |
| page_token | **[ string](#string)**<br/>The value returned from the previous call. |
| filter | **[ string](#string)**<br/>A filter to be applied to results. |
## ListUsersResponse {#animeshon.identity.v1alpha1.ListUsersResponse}

| Field | Description |
| --- | --- |
| users | **[repeated User](#User)**<br/>The list of users. |
| next_page_token | **[ string](#string)**<br/>A token to retrieve next page of results. |
## UpdateGroupRequest {#animeshon.identity.v1alpha1.UpdateGroupRequest}

| Field | Description |
| --- | --- |
| group | **[ Group](#Group)**<br/>The group to update. |
| update_mask | **[ google.protobuf.FieldMask](#google.protobuf.FieldMask)**<br/>The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |
## UpdateUserNotificationsRequest {#animeshon.identity.v1alpha1.UpdateUserNotificationsRequest}

| Field | Description |
| --- | --- |
| notifications | **[ UserNotifications](#UserNotifications)**<br/>The user notifications to update. |
| update_mask | **[ google.protobuf.FieldMask](#google.protobuf.FieldMask)**<br/>The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |
## UpdateUserRequest {#animeshon.identity.v1alpha1.UpdateUserRequest}

| Field | Description |
| --- | --- |
| user | **[ User](#User)**<br/>The user to update. |
| update_mask | **[ google.protobuf.FieldMask](#google.protobuf.FieldMask)**<br/>The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |
## UpdateUserSettingsRequest {#animeshon.identity.v1alpha1.UpdateUserSettingsRequest}

| Field | Description |
| --- | --- |
| settings | **[ UserSettings](#UserSettings)**<br/>The user settings to update. |
| update_mask | **[ google.protobuf.FieldMask](#google.protobuf.FieldMask)**<br/>The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |
## User {#animeshon.identity.v1alpha1.User}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the user. |
| uuid | **[ string](#string)**<br/>The uuid that identifies the user during the authentication flow. |
| username | **[ string](#string)**<br/>The public username of the user. |
| discriminator | **[ string](#string)**<br/>The public discriminator of the user. |
| primary_email | **[ string](#string)**<br/>The primary email address of the user. |
| primary_email_verified | **[ bool](#bool)**<br/>Whether the primary email address has been verified. |
| given_name | **[ string](#string)**<br/>The given name of the user. |
| family_name | **[ string](#string)**<br/>The family name of the user. |
| display_name | **[ string](#string)**<br/>The name of the user. |
| country_code | **[ string](#string)**<br/>The country where the user is located at, must be a valid ISO-3166 code. |
| locale | **[ string](#string)**<br/>The locale preferred by the user, must be a valid BCP-47 code. |
| locale_fallback | **[ string](#string)**<br/>The fallback locale preferred by the user, must be a valid BCP-47 code. The only allowed values are eng, jpn, and jpn-Latn (romaji). |
| birthday | **[ google.type.Date](#google.type.Date)**<br/>The birthday defined by the user, this value is used to determine whether the user should be allowed to access explicit and sensitive content. |
| gender | **[ Gender](#Gender)**<br/>The gender of the user. |
| profile_image | **[ string](#string)**<br/>The profile image of the user. |
| banner_image | **[ string](#string)**<br/>The banner image of the user. |
## UserDefaults {#animeshon.identity.v1alpha1.UserDefaults}

| Field | Description |
| --- | --- |
| album_profile | **[ string](#string)**<br/>The system-managed album dedicated to user profile images. |
| album_banner | **[ string](#string)**<br/>The system-managed album dedicated to user banner images. |
| playlist_liked | **[ string](#string)**<br/>The system-managed playlist dedicated to user liked content. |
| playlist_later | **[ string](#string)**<br/>The system-managed playlist dedicated to user saved for later content. |
## UserNotifications {#animeshon.identity.v1alpha1.UserNotifications}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the user. |
## UserProfile {#animeshon.identity.v1alpha1.UserProfile}
This message is returned only when a user wants to fetch information about
another user and the amount of information returned is greatly reduced to
ensure that personal and confidential information is never disclosed by
accident to other users. The user profile is read-only.
| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the user. |
| profile_image | **[ string](#string)**<br/>The profile image of the user. |
| banner_image | **[ string](#string)**<br/>The banner image of the user. |
| username | **[ string](#string)**<br/>The public username of the user. |
| discriminator | **[ string](#string)**<br/>The public discriminator of the user. |
| birthday | **[ google.type.Date](#google.type.Date)**<br/>The birthday of the user, this value is hidden for private profiles. |
| gender | **[ Gender](#Gender)**<br/>The gender of the user, this value is hidden for private profiles. |
## UserSettings {#animeshon.identity.v1alpha1.UserSettings}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the user. |
| profile_visibility | **[ UserSettings.Visibility](#UserSettings.Visibility)**<br/>A private user will only have the username, discriminator, profile image and banner image public. |
| show_explicit_content | **[ bool](#bool)**<br/>Whether the user choose to see explicit content during navigation. |
| enable_developer_mode | **[ bool](#bool)**<br/>Whether the user has enabled the developer mode. |

## Gender {#animeshon.identity.v1alpha1.Gender}


| Name | Description |
| --- | --- |
| GENDER_UNSPECIFIED | Not specified. |
| MALE | Male. |
| FEMALE | Female. |
| OTHER | Any other non-binary gender. |

## UserSettings.Visibility {#animeshon.identity.v1alpha1.UserSettings.Visibility}


| Name | Description |
| --- | --- |
| VISIBILITY_UNSPECIFIED | Not specified. |
| PUBLIC | Public. |
| PRIVATE | Private. |
