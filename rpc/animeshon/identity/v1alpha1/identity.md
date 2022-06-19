# Protocol Documentation
<a name="top"></a>

## Table of Contents

- [animeshon/identity/v1alpha1/identity.proto](#animeshon/identity/v1alpha1/identity.proto)
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
  
    - [Identity](#animeshon.identity.v1alpha1.Identity)
  
- [Scalar Value Types](#scalar-value-types)



<a name="animeshon/identity/v1alpha1/identity.proto"></a>
<p align="right"><a href="#top">Top</a></p>

## animeshon/identity/v1alpha1/identity.proto



<a name="animeshon.identity.v1alpha1.CreateGroupRequest"></a>

### CreateGroupRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| group | [Group](#animeshon.identity.v1alpha1.Group) |  | The group to create. |






<a name="animeshon.identity.v1alpha1.CreateUserRequest"></a>

### CreateUserRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| user | [User](#animeshon.identity.v1alpha1.User) |  | The user to create. |






<a name="animeshon.identity.v1alpha1.DeleteGroupRequest"></a>

### DeleteGroupRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the group to delete. |






<a name="animeshon.identity.v1alpha1.DeleteUserRequest"></a>

### DeleteUserRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the user to delete. |






<a name="animeshon.identity.v1alpha1.GetGroupRequest"></a>

### GetGroupRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the group to retrieve. |






<a name="animeshon.identity.v1alpha1.GetUserDefaultsRequest"></a>

### GetUserDefaultsRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the user to retrieve the defaults from. |






<a name="animeshon.identity.v1alpha1.GetUserNotificationsRequest"></a>

### GetUserNotificationsRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the user to retrieve the notifications from. |






<a name="animeshon.identity.v1alpha1.GetUserProfileRequest"></a>

### GetUserProfileRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the user to retrieve the profile from. |






<a name="animeshon.identity.v1alpha1.GetUserRequest"></a>

### GetUserRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the user to retrieve. |






<a name="animeshon.identity.v1alpha1.GetUserSettingsRequest"></a>

### GetUserSettingsRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The name of the user to retrieve the settings from. |






<a name="animeshon.identity.v1alpha1.Group"></a>

### Group



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The resource name of the group. |
| members | [string](#string) | repeated | The list of members of the group. Groups might include other groups. |
| etag | [bytes](#bytes) |  | An etag for concurrency control, ignored during creation. |






<a name="animeshon.identity.v1alpha1.ListGroupsRequest"></a>

### ListGroupsRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| page_size | [int32](#int32) |  | If unspecified, server will pick an appropriate default. |
| page_token | [string](#string) |  | The value returned from the previous call. |
| filter | [string](#string) |  | A filter to be applied to results. |






<a name="animeshon.identity.v1alpha1.ListGroupsResponse"></a>

### ListGroupsResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| groups | [Group](#animeshon.identity.v1alpha1.Group) | repeated | The list of groups. |
| next_page_token | [string](#string) |  | A token to retrieve next page of results. |






<a name="animeshon.identity.v1alpha1.ListUsersRequest"></a>

### ListUsersRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| page_size | [int32](#int32) |  | If unspecified, server will pick an appropriate default. |
| page_token | [string](#string) |  | The value returned from the previous call. |
| filter | [string](#string) |  | A filter to be applied to results. |






<a name="animeshon.identity.v1alpha1.ListUsersResponse"></a>

### ListUsersResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| users | [User](#animeshon.identity.v1alpha1.User) | repeated | The list of users. |
| next_page_token | [string](#string) |  | A token to retrieve next page of results. |






<a name="animeshon.identity.v1alpha1.UpdateGroupRequest"></a>

### UpdateGroupRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| group | [Group](#animeshon.identity.v1alpha1.Group) |  | The group to update. |
| update_mask | [google.protobuf.FieldMask](#google.protobuf.FieldMask) |  | The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |






<a name="animeshon.identity.v1alpha1.UpdateUserNotificationsRequest"></a>

### UpdateUserNotificationsRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| notifications | [UserNotifications](#animeshon.identity.v1alpha1.UserNotifications) |  | The user notifications to update. |
| update_mask | [google.protobuf.FieldMask](#google.protobuf.FieldMask) |  | The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |






<a name="animeshon.identity.v1alpha1.UpdateUserRequest"></a>

### UpdateUserRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| user | [User](#animeshon.identity.v1alpha1.User) |  | The user to update. |
| update_mask | [google.protobuf.FieldMask](#google.protobuf.FieldMask) |  | The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |






<a name="animeshon.identity.v1alpha1.UpdateUserSettingsRequest"></a>

### UpdateUserSettingsRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| settings | [UserSettings](#animeshon.identity.v1alpha1.UserSettings) |  | The user settings to update. |
| update_mask | [google.protobuf.FieldMask](#google.protobuf.FieldMask) |  | The field mask to determine which fields are to be updated. If empty, the server will assume all fields are to be updated. |






<a name="animeshon.identity.v1alpha1.User"></a>

### User



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The resource name of the user. |
| uuid | [string](#string) |  | The uuid that identifies the user during the authentication flow. |
| username | [string](#string) |  | The public username of the user. |
| discriminator | [string](#string) |  | The public discriminator of the user. |
| primary_email | [string](#string) |  | The primary email address of the user. |
| primary_email_verified | [bool](#bool) |  | Whether the primary email address has been verified. |
| given_name | [string](#string) |  | The given name of the user. |
| family_name | [string](#string) |  | The family name of the user. |
| display_name | [string](#string) |  | The name of the user. |
| country_code | [string](#string) |  | The country where the user is located at, must be a valid ISO-3166 code. |
| locale | [string](#string) |  | The locale preferred by the user, must be a valid BCP-47 code. |
| locale_fallback | [string](#string) |  | The fallback locale preferred by the user, must be a valid BCP-47 code. The only allowed values are eng, jpn, and jpn-Latn (romaji). |
| birthday | [google.type.Date](#google.type.Date) |  | The birthday defined by the user, this value is used to determine whether the user should be allowed to access explicit and sensitive content. |
| gender | [Gender](#animeshon.identity.v1alpha1.Gender) |  | The gender of the user. |
| profile_image | [string](#string) |  | The profile image of the user. |
| banner_image | [string](#string) |  | The banner image of the user. |






<a name="animeshon.identity.v1alpha1.UserDefaults"></a>

### UserDefaults



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| album_profile | [string](#string) |  | The system-managed album dedicated to user profile images. |
| album_banner | [string](#string) |  | The system-managed album dedicated to user banner images. |
| playlist_liked | [string](#string) |  | The system-managed playlist dedicated to user liked content. |
| playlist_later | [string](#string) |  | The system-managed playlist dedicated to user saved for later content. |






<a name="animeshon.identity.v1alpha1.UserNotifications"></a>

### UserNotifications



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The resource name of the user. |






<a name="animeshon.identity.v1alpha1.UserProfile"></a>

### UserProfile
This message is returned only when a user wants to fetch information about
another user and the amount of information returned is greatly reduced to
ensure that personal and confidential information is never disclosed by
accident to other users. The user profile is read-only.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The resource name of the user. |
| profile_image | [string](#string) |  | The profile image of the user. |
| banner_image | [string](#string) |  | The banner image of the user. |
| username | [string](#string) |  | The public username of the user. |
| discriminator | [string](#string) |  | The public discriminator of the user. |
| birthday | [google.type.Date](#google.type.Date) |  | The birthday of the user, this value is hidden for private profiles. |
| gender | [Gender](#animeshon.identity.v1alpha1.Gender) |  | The gender of the user, this value is hidden for private profiles. |






<a name="animeshon.identity.v1alpha1.UserSettings"></a>

### UserSettings



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The resource name of the user. |
| profile_visibility | [UserSettings.Visibility](#animeshon.identity.v1alpha1.UserSettings.Visibility) |  | A private user will only have the username, discriminator, profile image and banner image public. |
| show_explicit_content | [bool](#bool) |  | Whether the user choose to see explicit content during navigation. |
| enable_developer_mode | [bool](#bool) |  | Whether the user has enabled the developer mode. |





 


<a name="animeshon.identity.v1alpha1.Gender"></a>

### Gender


| Name | Number | Description |
| ---- | ------ | ----------- |
| GENDER_UNSPECIFIED | 0 | Not specified. |
| MALE | 1 | Male. |
| FEMALE | 2 | Female. |
| OTHER | 3 | Any other non-binary gender. |



<a name="animeshon.identity.v1alpha1.UserSettings.Visibility"></a>

### UserSettings.Visibility


| Name | Number | Description |
| ---- | ------ | ----------- |
| VISIBILITY_UNSPECIFIED | 0 | Not specified. |
| PUBLIC | 1 | Public. |
| PRIVATE | 2 | Private. |


 

 


<a name="animeshon.identity.v1alpha1.Identity"></a>

### Identity


| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| GetUserProfile | [GetUserProfileRequest](#animeshon.identity.v1alpha1.GetUserProfileRequest) | [UserProfile](#animeshon.identity.v1alpha1.UserProfile) |  |
| GetUser | [GetUserRequest](#animeshon.identity.v1alpha1.GetUserRequest) | [User](#animeshon.identity.v1alpha1.User) |  |
| ListUsers | [ListUsersRequest](#animeshon.identity.v1alpha1.ListUsersRequest) | [ListUsersResponse](#animeshon.identity.v1alpha1.ListUsersResponse) |  |
| CreateUser | [CreateUserRequest](#animeshon.identity.v1alpha1.CreateUserRequest) | [User](#animeshon.identity.v1alpha1.User) |  |
| UpdateUser | [UpdateUserRequest](#animeshon.identity.v1alpha1.UpdateUserRequest) | [User](#animeshon.identity.v1alpha1.User) |  |
| DeleteUser | [DeleteUserRequest](#animeshon.identity.v1alpha1.DeleteUserRequest) | [.google.protobuf.Empty](#google.protobuf.Empty) |  |
| GetUserSettings | [GetUserSettingsRequest](#animeshon.identity.v1alpha1.GetUserSettingsRequest) | [UserSettings](#animeshon.identity.v1alpha1.UserSettings) |  |
| UpdateUserSettings | [UpdateUserSettingsRequest](#animeshon.identity.v1alpha1.UpdateUserSettingsRequest) | [UserSettings](#animeshon.identity.v1alpha1.UserSettings) |  |
| GetUserNotifications | [GetUserNotificationsRequest](#animeshon.identity.v1alpha1.GetUserNotificationsRequest) | [UserNotifications](#animeshon.identity.v1alpha1.UserNotifications) |  |
| UpdateUserNotifications | [UpdateUserNotificationsRequest](#animeshon.identity.v1alpha1.UpdateUserNotificationsRequest) | [UserNotifications](#animeshon.identity.v1alpha1.UserNotifications) |  |
| GetUserDefaults | [GetUserDefaultsRequest](#animeshon.identity.v1alpha1.GetUserDefaultsRequest) | [UserDefaults](#animeshon.identity.v1alpha1.UserDefaults) |  |
| GetGroup | [GetGroupRequest](#animeshon.identity.v1alpha1.GetGroupRequest) | [Group](#animeshon.identity.v1alpha1.Group) |  |
| ListGroups | [ListGroupsRequest](#animeshon.identity.v1alpha1.ListGroupsRequest) | [ListGroupsResponse](#animeshon.identity.v1alpha1.ListGroupsResponse) |  |
| CreateGroup | [CreateGroupRequest](#animeshon.identity.v1alpha1.CreateGroupRequest) | [Group](#animeshon.identity.v1alpha1.Group) |  |
| UpdateGroup | [UpdateGroupRequest](#animeshon.identity.v1alpha1.UpdateGroupRequest) | [Group](#animeshon.identity.v1alpha1.Group) |  |
| DeleteGroup | [DeleteGroupRequest](#animeshon.identity.v1alpha1.DeleteGroupRequest) | [.google.protobuf.Empty](#google.protobuf.Empty) |  |

 



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

