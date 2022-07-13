# Package animeshon.knowledge.v1alpha1

## Index
- [Knowledge](#animeshon.knowledge.v1alpha1.Knowledge)
- [AllocateResourceNameRequest](#animeshon.knowledge.v1alpha1.AllocateResourceNameRequest)
- [AllocateResourceNameResponse](#animeshon.knowledge.v1alpha1.AllocateResourceNameResponse)
- [Anime](#animeshon.knowledge.v1alpha1.Anime)
- [ApproveContributionRequest](#animeshon.knowledge.v1alpha1.ApproveContributionRequest)
- [Canonical](#animeshon.knowledge.v1alpha1.Canonical)
- [Cast](#animeshon.knowledge.v1alpha1.Cast)
- [Chapter](#animeshon.knowledge.v1alpha1.Chapter)
- [Character](#animeshon.knowledge.v1alpha1.Character)
- [Collaboration](#animeshon.knowledge.v1alpha1.Collaboration)
- [ContentRelation](#animeshon.knowledge.v1alpha1.ContentRelation)
- [Contribution](#animeshon.knowledge.v1alpha1.Contribution)
- [ContributionChanges](#animeshon.knowledge.v1alpha1.ContributionChanges)
- [CreateContributionRequest](#animeshon.knowledge.v1alpha1.CreateContributionRequest)
- [Edge](#animeshon.knowledge.v1alpha1.Edge)
- [EntryEntity](#animeshon.knowledge.v1alpha1.EntryEntity)
- [Episode](#animeshon.knowledge.v1alpha1.Episode)
- [GameRelease](#animeshon.knowledge.v1alpha1.GameRelease)
- [GetContributionChangesRequest](#animeshon.knowledge.v1alpha1.GetContributionChangesRequest)
- [GetContributionRequest](#animeshon.knowledge.v1alpha1.GetContributionRequest)
- [GraphicNovel](#animeshon.knowledge.v1alpha1.GraphicNovel)
- [LightNovel](#animeshon.knowledge.v1alpha1.LightNovel)
- [ListContributionsRequest](#animeshon.knowledge.v1alpha1.ListContributionsRequest)
- [ListContributionsResponse](#animeshon.knowledge.v1alpha1.ListContributionsResponse)
- [Marketplace](#animeshon.knowledge.v1alpha1.Marketplace)
- [Organization](#animeshon.knowledge.v1alpha1.Organization)
- [Person](#animeshon.knowledge.v1alpha1.Person)
- [RejectContributionRequest](#animeshon.knowledge.v1alpha1.RejectContributionRequest)
- [ReviewContributionRequest](#animeshon.knowledge.v1alpha1.ReviewContributionRequest)
- [Running](#animeshon.knowledge.v1alpha1.Running)
- [Soundtrack](#animeshon.knowledge.v1alpha1.Soundtrack)
- [Track](#animeshon.knowledge.v1alpha1.Track)
- [Universe](#animeshon.knowledge.v1alpha1.Universe)
- [VisualNovel](#animeshon.knowledge.v1alpha1.VisualNovel)
- [VoiceActing](#animeshon.knowledge.v1alpha1.VoiceActing)
- [Website](#animeshon.knowledge.v1alpha1.Website)

## Knowledge {#animeshon.knowledge.v1alpha1.Knowledge}

| GetContribution |
| --- |
| **rpc** GetContribution([GetContributionRequest](#animeshon.knowledge.v1alpha1.GetContributionRequest)) [Contribution](#animeshon.knowledge.v1alpha1.Contribution)<br/> |

| ListContributions |
| --- |
| **rpc** ListContributions([ListContributionsRequest](#animeshon.knowledge.v1alpha1.ListContributionsRequest)) [ListContributionsResponse](#animeshon.knowledge.v1alpha1.ListContributionsResponse)<br/> |

| CreateContribution |
| --- |
| **rpc** CreateContribution([CreateContributionRequest](#animeshon.knowledge.v1alpha1.CreateContributionRequest)) [Contribution](#animeshon.knowledge.v1alpha1.Contribution)<br/> |

| GetContributionChanges |
| --- |
| **rpc** GetContributionChanges([GetContributionChangesRequest](#animeshon.knowledge.v1alpha1.GetContributionChangesRequest)) [ContributionChanges](#animeshon.knowledge.v1alpha1.ContributionChanges)<br/> |

| ReviewContribution |
| --- |
| **rpc** ReviewContribution([ReviewContributionRequest](#animeshon.knowledge.v1alpha1.ReviewContributionRequest)) [Contribution](#animeshon.knowledge.v1alpha1.Contribution)<br/>ReviewContribution allows moderators or the owner to modify and correct the contribution while in the PENDING or DRAFT state |

| ApproveContribution |
| --- |
| **rpc** ApproveContribution([ApproveContributionRequest](#animeshon.knowledge.v1alpha1.ApproveContributionRequest)) [Contribution](#animeshon.knowledge.v1alpha1.Contribution)<br/>ApproveContribution approves the contribution and applies the changes |

| RejectContribution |
| --- |
| **rpc** RejectContribution([RejectContributionRequest](#animeshon.knowledge.v1alpha1.RejectContributionRequest)) [Contribution](#animeshon.knowledge.v1alpha1.Contribution)<br/>RejectContribution rejects the contribution and DESTROYS all the changes |

| AllocateResourceName |
| --- |
| **rpc** AllocateResourceName([AllocateResourceNameRequest](#animeshon.knowledge.v1alpha1.AllocateResourceNameRequest)) [AllocateResourceNameResponse](#animeshon.knowledge.v1alpha1.AllocateResourceNameResponse)<br/>AllocateResourceName reserves a new resource name for entities which are not already part of Animeshon's Encyclopedia |

## AllocateResourceNameRequest {#animeshon.knowledge.v1alpha1.AllocateResourceNameRequest}

| Field | Description |
| --- | --- |
| kind | **[ string](#string)**<br/>The resource kind of the resource to migrate. |
## AllocateResourceNameResponse {#animeshon.knowledge.v1alpha1.AllocateResourceNameResponse}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the resource to migrate. |
## Anime {#animeshon.knowledge.v1alpha1.Anime}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>Required resource name |
| type | **[ string](#string)**<br/>Type of the anime Valid anime types:

Unknown type UNKNOWN

Tv series TV

Movie MOVIE

Original video animation OVA

Original Net Anime ONA

Special SPECIAL

Web anime WEB

Music video MUSIC_VIDEO

Other OTHER |
| episodes | **[repeated Edge](#Edge)**<br/>List of episode part of the anime |
| episode_count | **[ int32](#int32)**<br/>Number of scheduled episodes This field is useful for season anime which already announced how many episodes will be aired |
| names | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized names of the entity |
| aliases | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized aliases of the entity |
| descriptions | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized descriptions of the entity |
| synopsys | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized synopsys of the entity |
| cover_image_id | **[ string](#string)**<br/>Cover Image id of the entity |
| banner_image_id | **[ string](#string)**<br/>Banner Image id of the entity |
| websites | **[repeated Website](#Website)**<br/>List of websiste related to the entity. Websites might be official websites, Social, Wiki Entries |
| marketplaces | **[repeated Marketplace](#Marketplace)**<br/>List of marketplaces related to the entry. Maketplaces tells where to buy / consume / read the entity |
| status | **[ string](#string)**<br/>Status of the content Valid content statuses:

Unknown status UNKNOWN

Publishing or airing is still ongoing. ONGOING

Publishing or airing has been completed. COMPLETED

Publishing or airing has been scheduled. SCHEDULED

Publishing or airing started but never finished. INTERRUPTED

Publishing or airing was scheduled but later canceled. CANCELED

Publishing or airing has been suspended / has been put on hold. SUSPENDED

The content is in work in progress WORK_IN_PROGRESS |
| content_relations | **[repeated ContentRelation](#ContentRelation)**<br/>List of relations with other content |
| publishing_type | **[ string](#string)**<br/>Publishin Type specifies wether the content has been produced by a self published creator or if it's backed by a corporation

Valid Publishing types: Unknown status UNKNOWN

Self publishing SELF

Published by a corporation CORPORATE |
| original | **[ string](#string)**<br/>Original specifies if the idea behind the content is original or if it's base on an existing opera. Parodies of other content are normally not original, because charactes/settings/storyline are not owned by the creator.

Valid values: TRUE FALSE UNKNOWN |
| runnings | **[repeated Running](#Running)**<br/>List of localized airing/publishing periods of the content |
| release_date | **[ google.type.Date](#google.type.Date)**<br/>The release date in homeland of the content |
| starring | **[repeated Cast](#Cast)**<br/>List of characters starred in the content |
| staff | **[repeated Collaboration](#Collaboration)**<br/>List of people/organizations which contributed to the production/distribution of the content |
| soundtracks | **[repeated Soundtrack](#Soundtrack)**<br/>List of soundtracks in the content |
| voiceactings | **[repeated VoiceActing](#VoiceActing)**<br/>List of voice actors giving voice to the characters in the content |
| maturity_ratings | **[repeated string](#string)**<br/>Maturity ratings describes what it the minum age to legally consume a content Valid maturity Ratings:

Over 18 in USA MTR_RTN_USA_NC17

Over 18 in USA MTR_RTN_USA_R

Over 13 in USA MTR_RTN_USA_PG13

Over 3 in USA MTR_RTN_USA_PG

Safe in USA MTR_RTN_USA_G |
| region_restrictions | **[repeated string](#string)**<br/>Region restrictions mark the content as illegal in some region given the local regulations Valid Region Restrictions:

No Region Restriction NONE

The Entity is illegal following the U.N. guidelines ILLEGAL |
## ApproveContributionRequest {#animeshon.knowledge.v1alpha1.ApproveContributionRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>Required resource name |
## Canonical {#animeshon.knowledge.v1alpha1.Canonical}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>Required resource name |
| names | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized names of the entity |
| aliases | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized aliases of the entity |
| descriptions | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized descriptions of the entity |
| synopsys | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized synopsys of the entity |
| cover_image_id | **[ string](#string)**<br/>Cover Image id of the entity |
| banner_image_id | **[ string](#string)**<br/>Banner Image id of the entity |
| websites | **[repeated Website](#Website)**<br/>List of websiste related to the entity. Websites might be official websites, Social, Wiki Entries |
| marketplaces | **[repeated Marketplace](#Marketplace)**<br/>List of marketplaces related to the entry. Maketplaces tells where to buy / consume / read the entity |
| contents | **[repeated Edge](#Edge)**<br/>List of contents part of the canonical Canonicals can include Anime, GraphicNovels, LightNovels and VisualNovels |
## Cast {#animeshon.knowledge.v1alpha1.Cast}
Cast represnt the relation between a character and a content.
The cast is always field of the content and the Edge points to the character.
| Field | Description |
| --- | --- |
| character | **[ Edge](#Edge)**<br/>Casted Chracter |
| relation | **[ string](#string)**<br/>Relation within the content Valid relations:

MAIN SUPPORT APPEARS |
## Chapter {#animeshon.knowledge.v1alpha1.Chapter}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>Required resource name |
| type | **[ string](#string)**<br/>Type of the chapter Valid Chapter types

Unknown type UNKNOWN

Regular chapter REGULAR

Extra chapter EXTRA |
| index | **[ int32](#int32)**<br/>Incremental index of the chapter. Describes the release order |
| page_count | **[ int32](#int32)**<br/>Number of page of the chapter without extra pages |
| release_date | **[ google.type.Date](#google.type.Date)**<br/>The release date in homeland of the content |
| names | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized names of the entity |
| aliases | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized aliases of the entity |
| descriptions | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized descriptions of the entity |
| synopsys | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized synopsys of the entity |
| cover_image_id | **[ string](#string)**<br/>Cover Image id of the entity |
| banner_image_id | **[ string](#string)**<br/>Banner Image id of the entity |
| websites | **[repeated Website](#Website)**<br/>List of websiste related to the entity. Websites might be official websites, Social, Wiki Entries |
| marketplaces | **[repeated Marketplace](#Marketplace)**<br/>List of marketplaces related to the entry. Maketplaces tells where to buy / consume / read the entity |
| staff | **[repeated Collaboration](#Collaboration)**<br/>List of people/organizations which contributed to the production/distribution of the content |
## Character {#animeshon.knowledge.v1alpha1.Character}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>Required resource name |
| birthday | **[ google.type.Date](#google.type.Date)**<br/>The birthday of the character |
| gender | **[ string](#string)**<br/>Gender Valid Gender values:

Unknown gender UNKNOWN

Male MALE

Female FEMALE

Male which seems a female MALE_TRAP

Female which seems a male FEMALE_TRAP

Both male and female HERMAPHRODITIC

None of the default gender applies OTHER

The gender is undefined UNDEFINED

The gender something between male and female INTERSEXUAL |
| blood_type | **[ string](#string)**<br/>Blod Type Valid blood types:

Unknown blood type UNKNOWN

A (no Rh info) A

B (no Rh info) B

AB (no Rh info) AB

O (no Rh info) O

A+ A_PLUS

B+ B_PLUS

AB+ AB_PLUS

O+ O_PLUS

A- A_MINUS

B- B_MINUS

AB- AB_MINUS

O- O_MINUS |
| names | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized names of the entity |
| aliases | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized aliases of the entity |
| descriptions | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized descriptions of the entity |
| cover_image_id | **[ string](#string)**<br/>Cover Image id of the entity |
| banner_image_id | **[ string](#string)**<br/>Banner Image id of the entity |
| websites | **[repeated Website](#Website)**<br/>List of websiste related to the entity. Websites might be official websites, Social, Wiki Entries |
| marketplaces | **[repeated Marketplace](#Marketplace)**<br/>List of marketplaces related to the entry. Maketplaces tells where to buy / consume / read the entity

repeated Edge guise_of = 13; |
## Collaboration {#animeshon.knowledge.v1alpha1.Collaboration}
Collaboration represent the relation between a content and a person or organization.
The collaboration must be localizaed and it must carry the information about the role of the collaborator.
The Collaboration is always field of the content and the Edge points to the collaborator.
The localization must be a valid ISO3 localization which identifies the language/full localization of the content's version 
for which the collaborator collaborated
| Field | Description |
| --- | --- |
| collaborator | **[ Edge](#Edge)**<br/>Person / organization taking part to the collaboration |
| localization | **[ string](#string)**<br/>Valid ISO3 localization in which the collaborator took part in |
| role | **[ string](#string)**<br/>What role the collaborator had |
## ContentRelation {#animeshon.knowledge.v1alpha1.ContentRelation}
ContentRelation represent the relation between 2 different content.
The ContentReleation field is common to both the content, therefore the server do not need
to have both relations (from content A to B, and from B to A) because it will generate automatically
the reverse relation.

> Sending A sequel of B, the server will generate B prequel A

The relation has to be read as
entity -> has <relation> -> which is <related>
EG: Naruto -> Sequel -> Naruto Shippuden = <Naruto> has <sequel>, which is <Naruto Shippuden>
| Field | Description |
| --- | --- |
| related | **[ Edge](#Edge)**<br/>Object of the relation |
| relation | **[ string](#string)**<br/>Relation Valid relations:

ADAPTATION implies that the subject is the base from which the object has been adapted ADAPTATION

BASE Adaptation BASE

SAMESETTING Same universe/world/reality/timeline with completely different characters. SAME_SETTING

ALTSETTING Same universe/world/reality/timeline same characters with different universe/world/reality/timeline. ALTERNATIVE_SETTING

ALTVERSION alternative version Same setting, same characters, story is told differently. ALTERNATIVE_VERSION

CHARACTER When characters appear in both series, but is not a spin-off CHARACTER

FULLSTORY the object is full story of the subject this implies that the subject is a summary of the object FULL_STORY

SUMMARY summary SUMMARY

PARENTSTORY the object is the parent story of the subject this implies that the subject is a spin-off of the object PARENT_STORY

SpinOff spin off SPIN_OFF

PREQUEL prequel PREQUEL

SEQUEL sequel SEQUEL

MAINSTORY the object is the main story from which the subject has been created this implies that the subject is a side story of the object MAIN_STORY

SIDESTORY side story SIDE_STORY

ORIGINAL the object is the original of the subject this implies that the subject is the parody or fan made object ORIGINAL

PARODY is parody PARODY |
## Contribution {#animeshon.knowledge.v1alpha1.Contribution}
Contribution is the overall reppresentation of the contribution
| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the contribution. Required resource name |
| reviewer | **[ string](#string)**<br/>Who reviewed (accepting or rejecting) the contribution. Null if the contribution is still in reviewing phase |
| state | **[ Contribution.State](#Contribution.State)**<br/>The state of the contribution |
| display_name | **[ string](#string)**<br/>Arbitrary human readible contribution |
| generation | **[ int32](#int32)**<br/>Incremental value which specifies how many times the contribution has been reviewed. |
| create_time | **[ google.protobuf.Timestamp](#google.protobuf.Timestamp)**<br/>When the album was created. |
| update_time | **[ google.protobuf.Timestamp](#google.protobuf.Timestamp)**<br/>When the album was updated. |
| review_time | **[ google.protobuf.Timestamp](#google.protobuf.Timestamp)**<br/>When the album was reviewed. |
## ContributionChanges {#animeshon.knowledge.v1alpha1.ContributionChanges}
ContributionChanges decribes all the operations the contribution performs on an arbitrary number of entities
| Field | Description |
| --- | --- |
| additions | **[repeated EntryEntity](#EntryEntity)**<br/>List of additions of the contribution |
| deletions | **[repeated EntryEntity](#EntryEntity)**<br/>List of deletions of the cotributions Deleletion on primary entities (Anime/GraphicNovel/...) replace the old values while deletion on relations preserve the relation itself but mark it as deleted |
## CreateContributionRequest {#animeshon.knowledge.v1alpha1.CreateContributionRequest}

| Field | Description |
| --- | --- |
| parent | **[ string](#string)**<br/>The parent resource where this contribution will be created. |
| contribution | **[ Contribution](#Contribution)**<br/> |
| changes | **[ ContributionChanges](#ContributionChanges)**<br/> |
## Edge {#animeshon.knowledge.v1alpha1.Edge}
Relation with another entity
| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>Entity resource name |
## EntryEntity {#animeshon.knowledge.v1alpha1.EntryEntity}

| Field | Description |
| --- | --- |
| **[oneof](https://developers.google.com/protocol-buffers/docs/proto3#oneof)** _entity_<br />anime | **[ Anime](#Anime)**<br/> |
| **[oneof](https://developers.google.com/protocol-buffers/docs/proto3#oneof)** _entity_<br />canonical | **[ Canonical](#Canonical)**<br/> |
| **[oneof](https://developers.google.com/protocol-buffers/docs/proto3#oneof)** _entity_<br />chapter | **[ Chapter](#Chapter)**<br/> |
| **[oneof](https://developers.google.com/protocol-buffers/docs/proto3#oneof)** _entity_<br />character | **[ Character](#Character)**<br/> |
| **[oneof](https://developers.google.com/protocol-buffers/docs/proto3#oneof)** _entity_<br />episode | **[ Episode](#Episode)**<br/> |
| **[oneof](https://developers.google.com/protocol-buffers/docs/proto3#oneof)** _entity_<br />game_release | **[ GameRelease](#GameRelease)**<br/> |
| **[oneof](https://developers.google.com/protocol-buffers/docs/proto3#oneof)** _entity_<br />graphic_novel | **[ GraphicNovel](#GraphicNovel)**<br/> |
| **[oneof](https://developers.google.com/protocol-buffers/docs/proto3#oneof)** _entity_<br />light_novel | **[ LightNovel](#LightNovel)**<br/> |
| **[oneof](https://developers.google.com/protocol-buffers/docs/proto3#oneof)** _entity_<br />organization | **[ Organization](#Organization)**<br/> |
| **[oneof](https://developers.google.com/protocol-buffers/docs/proto3#oneof)** _entity_<br />person | **[ Person](#Person)**<br/> |
| **[oneof](https://developers.google.com/protocol-buffers/docs/proto3#oneof)** _entity_<br />track | **[ Track](#Track)**<br/> |
| **[oneof](https://developers.google.com/protocol-buffers/docs/proto3#oneof)** _entity_<br />universe | **[ Universe](#Universe)**<br/> |
| **[oneof](https://developers.google.com/protocol-buffers/docs/proto3#oneof)** _entity_<br />visual_novel | **[ VisualNovel](#VisualNovel)**<br/> |
## Episode {#animeshon.knowledge.v1alpha1.Episode}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>Required resource name |
| type | **[ string](#string)**<br/>Type of the episode Valid Episode types:

Unknown episode type UNKNOWN

Regular episode REGULAR

Recapitolation episode RECAP

Parody Fan made PARODY

Promo episode PROMO

Special episode SPECIAL

Opening / ending episode OPENING_ENDING

Other OTHER |
| index | **[ int32](#int32)**<br/>Incremental index of the episode. Describes the release order |
| release_date | **[ google.type.Date](#google.type.Date)**<br/>The release date in homeland of the content |
| names | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized names of the entity |
| aliases | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized aliases of the entity |
| descriptions | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized descriptions of the entity |
| synopsys | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized synopsys of the entity |
| cover_image_id | **[ string](#string)**<br/>Cover Image id of the entity |
| banner_image_id | **[ string](#string)**<br/>Banner Image id of the entity |
| websites | **[repeated Website](#Website)**<br/>List of websiste related to the entity. Websites might be official websites, Social, Wiki Entries |
| marketplaces | **[repeated Marketplace](#Marketplace)**<br/>List of marketplaces related to the entry. Maketplaces tells where to buy / consume / read the entity |
| staff | **[repeated Collaboration](#Collaboration)**<br/>List of people/organizations which contributed to the production/distribution of the content |
| soundtracks | **[repeated Soundtrack](#Soundtrack)**<br/>List of soundtracks in the content |
| voiceactings | **[repeated VoiceActing](#VoiceActing)**<br/>List of voice actors giving voice to the characters in the content |
| length_seconds | **[ int32](#int32)**<br/>Length of the episode in seconds. |
## GameRelease {#animeshon.knowledge.v1alpha1.GameRelease}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>Required resource name |
| languages | **[repeated string](#string)**<br/>List of languages the release is localized in |
| release_date | **[ google.type.Date](#google.type.Date)**<br/>The release date in homeland of the content

repeated Media media = 4; |
| censorship | **[ string](#string)**<br/>Valid Censorships Unknown censorship UNKNOWN

No censorship NONE

Censorship applied CENSORED |
| publishing_type | **[ string](#string)**<br/>Publishin Type specifies wether the content has been produced by a self published creator or if it's backed by a corporation Valid Publishing types:

Unknown status UNKNOWN

Self publishing SELF

Published by a corporation CORPORATE |
| asin | **[ string](#string)**<br/>Amazon identifier of the good |
| gtin | **[ string](#string)**<br/>Global Trade identifier of the good |
| type | **[ string](#string)**<br/>valid game release types: Unknown game release type UNKNOWN

The release is complete COMPLETE

The release is only a part of the content PARTIAL

The release is just trial TRIAL

The release is a dlc DLC |
| IsPatch | **[ string](#string)**<br/>If patch the release is not sold alone and it's ment to be applied to an existing game Valid values:

TRUE FALSE UNKNOWN |
| dub_degree | **[ string](#string)**<br/>dub_degree describes how much of the game is dubbed Valid game dub degree

Unknown DUB degree UNKNOWN

Not dubbed NONE

Only erotic scenes are dubbed ERO_ONLY

Partially dubbed PARTIAL

Full dubbed FULL |
| story_animation_degree | **[ string](#string)**<br/>story_animation_degree specifies how well the story scenes are animated Valid game animation degrees:

Unknown animation degree UNKNOWN

No animation NONE

Simple animations SIMPLE

Partial animation - Some fully animated scenes PARTIAL

Fully animated FULL |
| ero_animation_degree | **[ string](#string)**<br/>ero_animation_degree specifies how well the erotic scenes are animated Valid game animation degrees:

Unknown animation degree UNKNOWN

No animation NONE

Simple animations SIMPLE

Partial animation - Some fully animated scenes PARTIAL

Fully animated FULL |
| engine | **[ string](#string)**<br/> |
| platforms | **[repeated string](#string)**<br/>Valid Platforms: Unknown platform UNKNOWN 

Windows WINDOWS 

DOS DOS 

LINUX LINUX 

Mac MAC 

IOs devices IOS 

Android ANDROID 

DVD player DVD_PLAYER 

Blu-ray Player BLU_RAY_PLAYER 

FM Towns https://en.wikipedia.org/wiki/FM_Towns FM_TOWNS 

FM-7 Towns https://en.wikipedia.org/wiki/FM-7 FM7_TOWNS 

FM-8 Towns https://en.wikipedia.org/wiki/FM-8 FM8_TOWNS 

Gameboy advance GAMEBOY_ADVANCE 

Gameboy color GAMEBOY_COLOR 

MSX Computer https://en.wikipedia.org/wiki/MSX MSX 

Nintendo DS NINTENDO_DS 

NES platform NES 

C88 https://en.wikipedia.org/wiki/PC-8800_series P88 

PC98 https://en.wikipedia.org/wiki/PC-9800_series P98 

PC Engine PC_ENGINE 

Pc-FX https://en.wikipedia.org/wiki/PC-FX PC_FX 

Playstation portable PSP 

Playstation 1 PS1 

Playstation 2 PS2 

Playstation 3 PS3 

Playstation 4 PS4 

Playstation 5 PS5 

Playstation vita PS_VITA 

Dgramcast https://en.wikipedia.org/wiki/Dreamcast DGRAMCAST 

Sega Staurn SEGA_SATURN 

Sega Mega-CD SEGA_MEGACD 

Super Nintendo SUPER_NINTENDO 

Nintendo Switch NINTENDO_SWITCH 

Ninentdo WII NINTENDO_WII 

Nintendo WI NINTENDO_WII_U 

Nintendo 3Ds NINTENDO_3DS 

X68000 https://en.wikipedia.org/wiki/X68000 X68000 

Xbox One XBOX_ONE 

Xbox 360 XBOX_360 

Xbox XBOX 

Xbox Series X XBOX_X 

Website WEBSITE 

Visual Novel DS https://github.com/BASLQC/vnds/wiki VN_DS 

Sharp X1 https://en.wikipedia.org/wiki/Sharp_X1 SHARP_X1 

3DO Interactive Multiplayer INTERACTIVE_3DO 

Other OTHER 

Mobile Other MOBILE_OTHER |
| names | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized names of the entity |
| aliases | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized aliases of the entity |
| descriptions | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized descriptions of the entity |
| synopsys | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized synopsys of the entity |
| cover_image_id | **[ string](#string)**<br/>Cover Image id of the entity |
| banner_image_id | **[ string](#string)**<br/>Banner Image id of the entity |
| websites | **[repeated Website](#Website)**<br/>List of websiste related to the entity. Websites might be official websites, Social, Wiki Entries |
| marketplaces | **[repeated Marketplace](#Marketplace)**<br/>List of marketplaces related to the entry. Maketplaces tells where to buy / consume / read the entity |
| starring | **[repeated Cast](#Cast)**<br/>List of characters starred in the content |
| staff | **[repeated Collaboration](#Collaboration)**<br/>List of people/organizations which contributed to the production/distribution of the content |
| soundtracks | **[repeated Soundtrack](#Soundtrack)**<br/>List of soundtracks in the content |
| voiceactings | **[repeated VoiceActing](#VoiceActing)**<br/>List of voice actors giving voice to the characters in the content |
| maturity_ratings | **[repeated string](#string)**<br/>Maturity ratings describes what it the minum age to legally consume a content Valid maturity Ratings:

Over 18 in USA MTR_RTN_USA_NC17

Over 18 in USA MTR_RTN_USA_R

Over 13 in USA MTR_RTN_USA_PG13

Over 3 in USA MTR_RTN_USA_PG

Safe in USA MTR_RTN_USA_G |
| region_restrictions | **[repeated string](#string)**<br/>Region restrictions mark the content as illegal in some region given the local regulations Valid Region Restrictions:

No Region Restriction NONE

The Entity is illegal following the U.N. guidelines ILLEGAL |
| original | **[ string](#string)**<br/>Original specifies if the idea behind the content is original or if it's base on an existing opera. Parodies of other content are normally not original, because charactes/settings/storyline are not owned by the creator.

Valid values: TRUE FALSE UNKNOWN |
## GetContributionChangesRequest {#animeshon.knowledge.v1alpha1.GetContributionChangesRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the requested contribution. Required resource name |
## GetContributionRequest {#animeshon.knowledge.v1alpha1.GetContributionRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the requested contribution. Required resource name |
## GraphicNovel {#animeshon.knowledge.v1alpha1.GraphicNovel}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>Required resource name |
| type | **[ string](#string)**<br/>Type of the graphic novel Valid Graphic Novel types:

Unknown graphic novel type UNKNOWN

Japanese GraphicNovel MANGA

One shot (only one volume) ONE_SHOT

Cinese GraphicNovel MANHUA

Korean GraphicNovel MANHWA

Original English Language OEL

Web native comic (webtoon) WEB_COMIC

GraphicNovel consisting of 4 pannels YON_KOMA

Other OTHER |
| chapters | **[repeated Edge](#Edge)**<br/>List of chaters part of the graphic novel |
| chapter_count | **[ int32](#int32)**<br/>Number of scheduled chapters This field is useful for graphic novels which already announced how many chapter will be published |
| names | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized names of the entity |
| aliases | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized aliases of the entity |
| descriptions | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized descriptions of the entity |
| synopsys | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized synopsys of the entity |
| cover_image_id | **[ string](#string)**<br/>Cover Image id of the entity |
| banner_image_id | **[ string](#string)**<br/>Banner Image id of the entity |
| websites | **[repeated Website](#Website)**<br/>List of websiste related to the entity. Websites might be official websites, Social, Wiki Entries |
| marketplaces | **[repeated Marketplace](#Marketplace)**<br/>List of marketplaces related to the entry. Maketplaces tells where to buy / consume / read the entity |
| status | **[ string](#string)**<br/>Status of the content Valid content statuses:

Unknown status UNKNOWN

Publishing or airing is still ongoing. ONGOING

Publishing or airing has been completed. COMPLETED

Publishing or airing has been scheduled. SCHEDULED

Publishing or airing started but never finished. INTERRUPTED

Publishing or airing was scheduled but later canceled. CANCELED

Publishing or airing has been suspended / has been put on hold. SUSPENDED

The content is in work in progress WORK_IN_PROGRESS |
| content_relations | **[repeated ContentRelation](#ContentRelation)**<br/>List of relations with other content |
| publishing_type | **[ string](#string)**<br/>Publishin Type specifies wether the content has been produced by a self published creator or if it's backed by a corporation Valid Publishing types: Unknown status UNKNOWN

Self publishing SELF

Published by a corporation CORPORATE |
| original | **[ string](#string)**<br/>Original specifies if the idea behind the content is original or if it's base on an existing opera. Parodies of other content are normally not original, because charactes/settings/storyline are not owned by the creator.

Valid values: TRUE FALSE UNKNOWN |
| runnings | **[repeated Running](#Running)**<br/>List of localized airing/publishing periods of the content |
| release_date | **[ google.type.Date](#google.type.Date)**<br/>The release date in homeland of the content |
| starring | **[repeated Cast](#Cast)**<br/>List of characters starred in the content |
| staff | **[repeated Collaboration](#Collaboration)**<br/>List of people/organizations which contributed to the production/distribution of the content |
| maturity_ratings | **[repeated string](#string)**<br/>Maturity ratings describes what it the minum age to legally consume a content Valid maturity Ratings:

Over 18 in USA MTR_RTN_USA_NC17

Over 18 in USA MTR_RTN_USA_R

Over 13 in USA MTR_RTN_USA_PG13

Over 3 in USA MTR_RTN_USA_PG

Safe in USA MTR_RTN_USA_G |
| region_restrictions | **[repeated string](#string)**<br/>Region restrictions mark the content as illegal in some region given the local regulations Valid Region Restrictions:

No Region Restriction NONE

The Entity is illegal following the U.N. guidelines ILLEGAL |
## LightNovel {#animeshon.knowledge.v1alpha1.LightNovel}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>Required resource name |
| chapters | **[repeated Edge](#Edge)**<br/>List of chaters part of the light novel |
| chapter_count | **[ int32](#int32)**<br/>Number of scheduled chapters This field is useful for light novels which already announced how many chapter will be published |
| names | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized names of the entity |
| aliases | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized aliases of the entity |
| descriptions | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized descriptions of the entity |
| synopsys | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized synopsys of the entity |
| cover_image_id | **[ string](#string)**<br/>Cover Image id of the entity |
| banner_image_id | **[ string](#string)**<br/>Banner Image id of the entity |
| websites | **[repeated Website](#Website)**<br/>List of websiste related to the entity. Websites might be official websites, Social, Wiki Entries |
| marketplaces | **[repeated Marketplace](#Marketplace)**<br/>List of marketplaces related to the entry. Maketplaces tells where to buy / consume / read the entity |
| status | **[ string](#string)**<br/>Status of the content Valid content statuses:

Unknown status UNKNOWN

Publishing or airing is still ongoing. ONGOING

Publishing or airing has been completed. COMPLETED

Publishing or airing has been scheduled. SCHEDULED

Publishing or airing started but never finished. INTERRUPTED

Publishing or airing was scheduled but later canceled. CANCELED

Publishing or airing has been suspended / has been put on hold. SUSPENDED

The content is in work in progress WORK_IN_PROGRESS |
| content_relations | **[repeated ContentRelation](#ContentRelation)**<br/>List of relations with other content |
| publishing_type | **[ string](#string)**<br/>Publishin Type specifies wether the content has been produced by a self published creator or if it's backed by a corporation Valid Publishing types:

Unknown status UNKNOWN

Self publishing SELF

Published by a corporation CORPORATE |
| original | **[ string](#string)**<br/>Original specifies if the idea behind the content is original or if it's base on an existing opera. Parodies of other content are normally not original, because charactes/settings/storyline are not owned by the creator.

Valid values: TRUE FALSE UNKNOWN |
| runnings | **[repeated Running](#Running)**<br/>List of localized airing/publishing periods of the content |
| release_date | **[ google.type.Date](#google.type.Date)**<br/>The release date in homeland of the content |
| starring | **[repeated Cast](#Cast)**<br/>List of characters starred in the content |
| staff | **[repeated Collaboration](#Collaboration)**<br/>List of people/organizations which contributed to the production/distribution of the content |
| maturity_ratings | **[repeated string](#string)**<br/>Maturity ratings describes what it the minum age to legally consume a content Valid maturity Ratings:

Over 18 in USA MTR_RTN_USA_NC17

Over 18 in USA MTR_RTN_USA_R

Over 13 in USA MTR_RTN_USA_PG13

Over 3 in USA MTR_RTN_USA_PG

Safe in USA MTR_RTN_USA_G |
| region_restrictions | **[repeated string](#string)**<br/>Region restrictions mark the content as illegal in some region given the local regulations Valid Region Restrictions:

No Region Restriction NONE

The Entity is illegal following the U.N. guidelines ILLEGAL |
## ListContributionsRequest {#animeshon.knowledge.v1alpha1.ListContributionsRequest}

| Field | Description |
| --- | --- |
| parent | **[ string](#string)**<br/>The parent, which owns this collection of contributions. |
| page_size | **[ int32](#int32)**<br/>The maximum number of users to return. Server may return fewer users than requested. If unspecified, server will pick an appropriate default. |
| page_token | **[ string](#string)**<br/>The value returned from the previous call. |
| filter | **[ string](#string)**<br/>A filter to be applied to results. |
## ListContributionsResponse {#animeshon.knowledge.v1alpha1.ListContributionsResponse}

| Field | Description |
| --- | --- |
| contributions | **[repeated Contribution](#Contribution)**<br/>The list of contributions. |
| next_page_token | **[ string](#string)**<br/>A token to retrieve next page of results. |
## Marketplace {#animeshon.knowledge.v1alpha1.Marketplace}
Marketplace is where to consume the content.
The name field must point to a valid valid marketplace id in order to load icon and name of the marketplace.
If the marketplace is limited to some specific country, add them to the field region following the IOS3 standard
| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>Required resource name |
| url | **[ string](#string)**<br/>Marketplace url |
| region | **[ string](#string)**<br/>region in which the marketplace distributes |
## Organization {#animeshon.knowledge.v1alpha1.Organization}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>Required resource name |
| type | **[ string](#string)**<br/>Type of the organization Valid Organization types:

Uunknown organization type UNKNOWN

Coorporation / company CORPORATE

Circle of people CIRCLE |
| foundation_date | **[ google.type.Date](#google.type.Date)**<br/>Foundation date of the organization |
| names | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized names of the entity |
| aliases | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized aliases of the entity |
| descriptions | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized descriptions of the entity |
| synopsys | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized synopsys of the entity |
| cover_image_id | **[ string](#string)**<br/>Cover Image id of the entity |
| banner_image_id | **[ string](#string)**<br/>Banner Image id of the entity |
| websites | **[repeated Website](#Website)**<br/>List of websiste related to the entity. Websites might be official websites, Social, Wiki Entries |
## Person {#animeshon.knowledge.v1alpha1.Person}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>Required resource name |
| birthday | **[ google.type.Date](#google.type.Date)**<br/>Birthday of the person |
| gender | **[ string](#string)**<br/>Gender Valid Gender values:

Unknown gender UNKNOWN 

Male MALE 

Female FEMALE |
| blood_type | **[ string](#string)**<br/>Blod Type Valid blood types:

Unknown blood type UNKNOWN

A (no Rh info) A

B (no Rh info) B

AB (no Rh info) AB

O (no Rh info) O

A+ A_PLUS

B+ B_PLUS

AB+ AB_PLUS

O+ O_PLUS

A- A_MINUS

B- B_MINUS

AB- AB_MINUS

O- O_MINUS |
| names | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized names of the entity |
| aliases | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized aliases of the entity |
| descriptions | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized descriptions of the entity |
| synopsys | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized synopsys of the entity |
| cover_image_id | **[ string](#string)**<br/>Cover Image id of the entity |
| banner_image_id | **[ string](#string)**<br/>Banner Image id of the entity |
| websites | **[repeated Website](#Website)**<br/>List of websiste related to the entity. Websites might be official websites, Social, Wiki Entries |
## RejectContributionRequest {#animeshon.knowledge.v1alpha1.RejectContributionRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>Required resource name |
## ReviewContributionRequest {#animeshon.knowledge.v1alpha1.ReviewContributionRequest}
ReviewContributionRequest specifies the edit to apply to an existing contribution
| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>Name of the contribution |
| comment | **[ string](#string)**<br/>Optional comment on the review |
| changes | **[ ContributionChanges](#ContributionChanges)**<br/>Changes to the existing contribution New changes will be added on top of the existing ones |
| discards | **[ ContributionChanges](#ContributionChanges)**<br/>Changes to discard from the contribution Discarded changes will be completely removed from the contribution |
## Running {#animeshon.knowledge.v1alpha1.Running}
Period in which the content has been aired/released/published for a particular localization
| Field | Description |
| --- | --- |
| start_time | **[ google.type.Date](#google.type.Date)**<br/>Start of the publishing/airing/release |
| end_time | **[ google.type.Date](#google.type.Date)**<br/>End of the publishing/airing/release Omitted if the content is still ONGOING |
| localization | **[ string](#string)**<br/>Valid ISO3 localization |
## Soundtrack {#animeshon.knowledge.v1alpha1.Soundtrack}
Soundtrack exposes the information about which Track has been used in which Content in which localization and for what.
The localization must be a valid ISO3 localization which identifies the language/full localization of the content's version 
for which the Track is used
| Field | Description |
| --- | --- |
| track | **[ Edge](#Edge)**<br/>Track used as soundtrack |
| type | **[ string](#string)**<br/>Type describes for what purpose the track was used Valid Soundtrack types:

Unknown type UNKNOWN

The track is used as ending ENDING

The track is used as opening OPENING

The track is used as insert song INSERT

The track is used as background song BACKGROUND

The track is used as image song IMAGE

The track is used as theme song THEME |
| localization | **[ string](#string)**<br/>Valid ISO3 localization in which the track was used |
## Track {#animeshon.knowledge.v1alpha1.Track}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>Required resource name |
| release_date | **[ google.type.Date](#google.type.Date)**<br/>The release date in homeland of the content |
| names | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized names of the entity |
| aliases | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized aliases of the entity |
| descriptions | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized descriptions of the entity |
| synopsys | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized synopsys of the entity |
| cover_image_id | **[ string](#string)**<br/>Cover Image id of the entity |
| banner_image_id | **[ string](#string)**<br/>Banner Image id of the entity |
| websites | **[repeated Website](#Website)**<br/>List of websiste related to the entity. Websites might be official websites, Social, Wiki Entries |
| marketplaces | **[repeated Marketplace](#Marketplace)**<br/>List of marketplaces related to the entry. Maketplaces tells where to buy / consume / read the entity |
| staff | **[repeated Collaboration](#Collaboration)**<br/>List of people/organizations which contributed to the production/distribution of the content |
## Universe {#animeshon.knowledge.v1alpha1.Universe}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>Required resource name |
| names | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized names of the entity |
| aliases | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized aliases of the entity |
| descriptions | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized descriptions of the entity |
| synopsys | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized synopsys of the entity |
| cover_image_id | **[ string](#string)**<br/>Cover Image id of the entity |
| banner_image_id | **[ string](#string)**<br/>Banner Image id of the entity |
| websites | **[repeated Website](#Website)**<br/>List of websiste related to the entity. Websites might be official websites, Social, Wiki Entries |
| marketplaces | **[repeated Marketplace](#Marketplace)**<br/>List of marketplaces related to the entry. Maketplaces tells where to buy / consume / read the entity |
| contents | **[repeated Edge](#Edge)**<br/>List of contents part of the universe Universes can include Anime, GraphicNovels, LightNovels and VisualNovels |
| canonicals | **[repeated Edge](#Edge)**<br/>List of canonicals part of the universe |
## VisualNovel {#animeshon.knowledge.v1alpha1.VisualNovel}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>Required resource name |
| length | **[ string](#string)**<br/>Valid Visual Novel lengths: Unknown length UNKNOWN

< 2 hours VERY_SHORT

20 - 10 hours SHORT

10 - 30 hours MEDIUM

30 - 50 hours LONG

> 50 hours VERY_LONG |
| names | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized names of the entity |
| aliases | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized aliases of the entity |
| descriptions | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized descriptions of the entity |
| synopsys | **[repeated google.type.LocalizedText](#google.type.LocalizedText)**<br/>List of localized synopsys of the entity |
| cover_image_id | **[ string](#string)**<br/>Cover Image id of the entity |
| banner_image_id | **[ string](#string)**<br/>Banner Image id of the entity |
| websites | **[repeated Website](#Website)**<br/>List of websiste related to the entity. Websites might be official websites, Social, Wiki Entries |
| marketplaces | **[repeated Marketplace](#Marketplace)**<br/>List of marketplaces related to the entry. Maketplaces tells where to buy / consume / read the entity |
| status | **[ string](#string)**<br/>Status of the content Valid content statuses:

Unknown status UNKNOWN

Publishing or airing is still ongoing. ONGOING

Publishing or airing has been completed. COMPLETED

Publishing or airing has been scheduled. SCHEDULED

Publishing or airing started but never finished. INTERRUPTED

Publishing or airing was scheduled but later canceled. CANCELED

Publishing or airing has been suspended / has been put on hold. SUSPENDED

The content is in work in progress WORK_IN_PROGRESS |
| content_relations | **[repeated ContentRelation](#ContentRelation)**<br/>List of relations with other content |
| publishing_type | **[ string](#string)**<br/>Publishin Type specifies wether the content has been produced by a self published creator or if it's backed by a corporation Valid Publishing types:

Unknown status UNKNOWN

Self publishing SELF

Published by a corporation CORPORATE |
| original | **[ string](#string)**<br/>Original specifies if the idea behind the content is original or if it's base on an existing opera. Parodies of other content are normally not original, because charactes/settings/storyline are not owned by the creator.

Valid values: TRUE FALSE UNKNOWN |
| runnings | **[repeated Running](#Running)**<br/>List of localized airing/publishing periods of the content |
| release_date | **[ google.type.Date](#google.type.Date)**<br/>The release date in homeland of the content |
| starring | **[repeated Cast](#Cast)**<br/>List of characters starred in the content |
| staff | **[repeated Collaboration](#Collaboration)**<br/>List of people/organizations which contributed to the production/distribution of the content |
| soundtracks | **[repeated Soundtrack](#Soundtrack)**<br/>List of soundtracks in the content |
| voiceactings | **[repeated VoiceActing](#VoiceActing)**<br/>List of voice actors giving voice to the characters in the content |
| maturity_ratings | **[repeated string](#string)**<br/>Maturity ratings describes what it the minum age to legally consume a content Valid maturity Ratings:

Over 18 in USA MTR_RTN_USA_NC17

Over 18 in USA MTR_RTN_USA_R

Over 13 in USA MTR_RTN_USA_PG13

Over 3 in USA MTR_RTN_USA_PG

Safe in USA MTR_RTN_USA_G |
| region_restrictions | **[repeated string](#string)**<br/>Region restrictions mark the content as illegal in some region given the local regulations Valid Region Restrictions:

No Region Restriction NONE

The Entity is illegal following the U.N. guidelines ILLEGAL |
| releases | **[repeated Edge](#Edge)**<br/>Releases are all those entities which practically make the content consumable Some examples are: Volumes for GraphicNovels/LightNovels/Chapters, BlueRays for Anime, Collector Editions... |
## VoiceActing {#animeshon.knowledge.v1alpha1.VoiceActing}
Voice Acting represent voice given by a person to a voiced entity in a specific content
The Voice Acting is always field of the content and it must be localized.
The localization must be a valid ISO3 localization which identifies the language/full localization of the content's version 
for which the actor gave the voice to the entity
| Field | Description |
| --- | --- |
| voiced | **[ Edge](#Edge)**<br/>The entity receiving the voice Character or VoiceOver |
| actor | **[ Edge](#Edge)**<br/>Who gave the voice |
| localization | **[ string](#string)**<br/>Valid ISO3 localization for which the voice was given |
| primary | **[ string](#string)**<br/>Voices can be primary or not. Primary voices are those lasting for the majority of the conte While Secondary voices are normally used in flashbacks or side events

Valid values: TRUE FALSE UNKNOWN |
## Website {#animeshon.knowledge.v1alpha1.Website}
Any kind of website related to the entity.
Could be official website, twitter, or external resources such as wikipedia
| Field | Description |
| --- | --- |
| url | **[ string](#string)**<br/>Website url |

## Contribution.State {#animeshon.knowledge.v1alpha1.Contribution.State}


| Name | Description |
| --- | --- |
| PENDING | No description. |
| APPROVED | No description. |
| REJECTED | No description. |
| DRAFT | No description. |
