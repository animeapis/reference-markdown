# Protocol Documentation
<a name="top"></a>

## Table of Contents

- [animeshon/knowledge/v1alpha1/knowledge.proto](#animeshon/knowledge/v1alpha1/knowledge.proto)
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
  
    - [Contribution.State](#animeshon.knowledge.v1alpha1.Contribution.State)
  
    - [Knowledge](#animeshon.knowledge.v1alpha1.Knowledge)
  
- [Scalar Value Types](#scalar-value-types)



<a name="animeshon/knowledge/v1alpha1/knowledge.proto"></a>
<p align="right"><a href="#top">Top</a></p>

## animeshon/knowledge/v1alpha1/knowledge.proto



<a name="animeshon.knowledge.v1alpha1.AllocateResourceNameRequest"></a>

### AllocateResourceNameRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| kind | [string](#string) |  | The resource kind of the resource to migrate. |






<a name="animeshon.knowledge.v1alpha1.AllocateResourceNameResponse"></a>

### AllocateResourceNameResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The resource name of the resource to migrate. |






<a name="animeshon.knowledge.v1alpha1.Anime"></a>

### Anime



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | Required resource name |
| type | [string](#string) |  | Type of the anime Valid anime types:

Unknown type UNKNOWN

Tv series TV

Movie MOVIE

Original video animation OVA

Original Net Anime ONA

Special SPECIAL

Web anime WEB

Music video MUSIC_VIDEO

Other OTHER |
| episodes | [Edge](#animeshon.knowledge.v1alpha1.Edge) | repeated | List of episode part of the anime |
| episode_count | [int32](#int32) |  | Number of scheduled episodes This field is useful for season anime which already announced how many episodes will be aired |
| names | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized names of the entity |
| aliases | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized aliases of the entity |
| descriptions | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized descriptions of the entity |
| synopsys | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized synopsys of the entity |
| cover_image_id | [string](#string) |  | Cover Image id of the entity |
| banner_image_id | [string](#string) |  | Banner Image id of the entity |
| websites | [Website](#animeshon.knowledge.v1alpha1.Website) | repeated | List of websiste related to the entity. Websites might be official websites, Social, Wiki Entries |
| marketplaces | [Marketplace](#animeshon.knowledge.v1alpha1.Marketplace) | repeated | List of marketplaces related to the entry. Maketplaces tells where to buy / consume / read the entity |
| status | [string](#string) |  | Status of the content Valid content statuses:

Unknown status UNKNOWN

Publishing or airing is still ongoing. ONGOING

Publishing or airing has been completed. COMPLETED

Publishing or airing has been scheduled. SCHEDULED

Publishing or airing started but never finished. INTERRUPTED

Publishing or airing was scheduled but later canceled. CANCELED

Publishing or airing has been suspended / has been put on hold. SUSPENDED

The content is in work in progress WORK_IN_PROGRESS |
| content_relations | [ContentRelation](#animeshon.knowledge.v1alpha1.ContentRelation) | repeated | List of relations with other content |
| publishing_type | [string](#string) |  | Publishin Type specifies wether the content has been produced by a self published creator or if it&#39;s backed by a corporation

Valid Publishing types: Unknown status UNKNOWN

Self publishing SELF

Published by a corporation CORPORATE |
| original | [string](#string) |  | Original specifies if the idea behind the content is original or if it&#39;s base on an existing opera. Parodies of other content are normally not original, because charactes/settings/storyline are not owned by the creator.

Valid values: TRUE FALSE UNKNOWN |
| runnings | [Running](#animeshon.knowledge.v1alpha1.Running) | repeated | List of localized airing/publishing periods of the content |
| release_date | [google.type.Date](#google.type.Date) |  | The release date in homeland of the content |
| starring | [Cast](#animeshon.knowledge.v1alpha1.Cast) | repeated | List of characters starred in the content |
| staff | [Collaboration](#animeshon.knowledge.v1alpha1.Collaboration) | repeated | List of people/organizations which contributed to the production/distribution of the content |
| soundtracks | [Soundtrack](#animeshon.knowledge.v1alpha1.Soundtrack) | repeated | List of soundtracks in the content |
| voiceactings | [VoiceActing](#animeshon.knowledge.v1alpha1.VoiceActing) | repeated | List of voice actors giving voice to the characters in the content |
| maturity_ratings | [string](#string) | repeated | Maturity ratings describes what it the minum age to legally consume a content Valid maturity Ratings:

Over 18 in USA MTR_RTN_USA_NC17

Over 18 in USA MTR_RTN_USA_R

Over 13 in USA MTR_RTN_USA_PG13

Over 3 in USA MTR_RTN_USA_PG

Safe in USA MTR_RTN_USA_G |
| region_restrictions | [string](#string) | repeated | Region restrictions mark the content as illegal in some region given the local regulations Valid Region Restrictions:

No Region Restriction NONE

The Entity is illegal following the U.N. guidelines ILLEGAL |






<a name="animeshon.knowledge.v1alpha1.ApproveContributionRequest"></a>

### ApproveContributionRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | Required resource name |






<a name="animeshon.knowledge.v1alpha1.Canonical"></a>

### Canonical



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | Required resource name |
| names | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized names of the entity |
| aliases | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized aliases of the entity |
| descriptions | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized descriptions of the entity |
| synopsys | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized synopsys of the entity |
| cover_image_id | [string](#string) |  | Cover Image id of the entity |
| banner_image_id | [string](#string) |  | Banner Image id of the entity |
| websites | [Website](#animeshon.knowledge.v1alpha1.Website) | repeated | List of websiste related to the entity. Websites might be official websites, Social, Wiki Entries |
| marketplaces | [Marketplace](#animeshon.knowledge.v1alpha1.Marketplace) | repeated | List of marketplaces related to the entry. Maketplaces tells where to buy / consume / read the entity |
| contents | [Edge](#animeshon.knowledge.v1alpha1.Edge) | repeated | List of contents part of the canonical Canonicals can include Anime, GraphicNovels, LightNovels and VisualNovels |






<a name="animeshon.knowledge.v1alpha1.Cast"></a>

### Cast
Cast represnt the relation between a character and a content.
The cast is always field of the content and the Edge points to the character.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| character | [Edge](#animeshon.knowledge.v1alpha1.Edge) |  | Casted Chracter |
| relation | [string](#string) |  | Relation within the content Valid relations:

MAIN SUPPORT APPEARS |






<a name="animeshon.knowledge.v1alpha1.Chapter"></a>

### Chapter



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | Required resource name |
| type | [string](#string) |  | Type of the chapter Valid Chapter types

Unknown type UNKNOWN

Regular chapter REGULAR

Extra chapter EXTRA |
| index | [int32](#int32) |  | Incremental index of the chapter. Describes the release order |
| page_count | [int32](#int32) |  | Number of page of the chapter without extra pages |
| release_date | [google.type.Date](#google.type.Date) |  | The release date in homeland of the content |
| names | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized names of the entity |
| aliases | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized aliases of the entity |
| descriptions | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized descriptions of the entity |
| synopsys | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized synopsys of the entity |
| cover_image_id | [string](#string) |  | Cover Image id of the entity |
| banner_image_id | [string](#string) |  | Banner Image id of the entity |
| websites | [Website](#animeshon.knowledge.v1alpha1.Website) | repeated | List of websiste related to the entity. Websites might be official websites, Social, Wiki Entries |
| marketplaces | [Marketplace](#animeshon.knowledge.v1alpha1.Marketplace) | repeated | List of marketplaces related to the entry. Maketplaces tells where to buy / consume / read the entity |
| staff | [Collaboration](#animeshon.knowledge.v1alpha1.Collaboration) | repeated | List of people/organizations which contributed to the production/distribution of the content |






<a name="animeshon.knowledge.v1alpha1.Character"></a>

### Character



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | Required resource name |
| birthday | [google.type.Date](#google.type.Date) |  | The birthday of the character |
| gender | [string](#string) |  | Gender Valid Gender values:

Unknown gender UNKNOWN

Male MALE

Female FEMALE

Male which seems a female MALE_TRAP

Female which seems a male FEMALE_TRAP

Both male and female HERMAPHRODITIC

None of the default gender applies OTHER

The gender is undefined UNDEFINED

The gender something between male and female INTERSEXUAL |
| blood_type | [string](#string) |  | Blod Type Valid blood types:

Unknown blood type UNKNOWN

A (no Rh info) A

B (no Rh info) B

AB (no Rh info) AB

O (no Rh info) O

A&#43; A_PLUS

B&#43; B_PLUS

AB&#43; AB_PLUS

O&#43; O_PLUS

A- A_MINUS

B- B_MINUS

AB- AB_MINUS

O- O_MINUS |
| names | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized names of the entity |
| aliases | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized aliases of the entity |
| descriptions | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized descriptions of the entity |
| cover_image_id | [string](#string) |  | Cover Image id of the entity |
| banner_image_id | [string](#string) |  | Banner Image id of the entity |
| websites | [Website](#animeshon.knowledge.v1alpha1.Website) | repeated | List of websiste related to the entity. Websites might be official websites, Social, Wiki Entries |
| marketplaces | [Marketplace](#animeshon.knowledge.v1alpha1.Marketplace) | repeated | List of marketplaces related to the entry. Maketplaces tells where to buy / consume / read the entity

repeated Edge guise_of = 13; |






<a name="animeshon.knowledge.v1alpha1.Collaboration"></a>

### Collaboration
Collaboration represent the relation between a content and a person or organization.
The collaboration must be localizaed and it must carry the information about the role of the collaborator.
The Collaboration is always field of the content and the Edge points to the collaborator.
The localization must be a valid ISO3 localization which identifies the language/full localization of the content&#39;s version 
for which the collaborator collaborated


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| collaborator | [Edge](#animeshon.knowledge.v1alpha1.Edge) |  | Person / organization taking part to the collaboration |
| localization | [string](#string) |  | Valid ISO3 localization in which the collaborator took part in |
| role | [string](#string) |  | What role the collaborator had |






<a name="animeshon.knowledge.v1alpha1.ContentRelation"></a>

### ContentRelation
ContentRelation represent the relation between 2 different content.
The ContentReleation field is common to both the content, therefore the server do not need
to have both relations (from content A to B, and from B to A) because it will generate automatically
the reverse relation.

&gt; Sending A sequel of B, the server will generate B prequel A

The relation has to be read as
entity -&gt; has &lt;relation&gt; -&gt; which is &lt;related&gt;
EG: Naruto -&gt; Sequel -&gt; Naruto Shippuden = &lt;Naruto&gt; has &lt;sequel&gt;, which is &lt;Naruto Shippuden&gt;


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| related | [Edge](#animeshon.knowledge.v1alpha1.Edge) |  | Object of the relation |
| relation | [string](#string) |  | Relation Valid relations:

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






<a name="animeshon.knowledge.v1alpha1.Contribution"></a>

### Contribution
Contribution is the overall reppresentation of the contribution


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The resource name of the contribution. Required resource name |
| reviewer | [string](#string) |  | Who reviewed (accepting or rejecting) the contribution. Null if the contribution is still in reviewing phase |
| state | [Contribution.State](#animeshon.knowledge.v1alpha1.Contribution.State) |  | The state of the contribution |
| display_name | [string](#string) |  | Arbitrary human readible contribution |
| generation | [int32](#int32) |  | Incremental value which specifies how many times the contribution has been reviewed. |
| create_time | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | When the album was created. |
| update_time | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | When the album was updated. |
| review_time | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | When the album was reviewed. |






<a name="animeshon.knowledge.v1alpha1.ContributionChanges"></a>

### ContributionChanges
ContributionChanges decribes all the operations the contribution performs on an arbitrary number of entities


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| additions | [EntryEntity](#animeshon.knowledge.v1alpha1.EntryEntity) | repeated | List of additions of the contribution |
| deletions | [EntryEntity](#animeshon.knowledge.v1alpha1.EntryEntity) | repeated | List of deletions of the cotributions Deleletion on primary entities (Anime/GraphicNovel/...) replace the old values while deletion on relations preserve the relation itself but mark it as deleted |






<a name="animeshon.knowledge.v1alpha1.CreateContributionRequest"></a>

### CreateContributionRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| parent | [string](#string) |  | The parent resource where this contribution will be created. |
| contribution | [Contribution](#animeshon.knowledge.v1alpha1.Contribution) |  |  |
| changes | [ContributionChanges](#animeshon.knowledge.v1alpha1.ContributionChanges) |  |  |






<a name="animeshon.knowledge.v1alpha1.Edge"></a>

### Edge
Relation with another entity


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | Entity resource name |






<a name="animeshon.knowledge.v1alpha1.EntryEntity"></a>

### EntryEntity



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| anime | [Anime](#animeshon.knowledge.v1alpha1.Anime) |  |  |
| canonical | [Canonical](#animeshon.knowledge.v1alpha1.Canonical) |  |  |
| chapter | [Chapter](#animeshon.knowledge.v1alpha1.Chapter) |  |  |
| character | [Character](#animeshon.knowledge.v1alpha1.Character) |  |  |
| episode | [Episode](#animeshon.knowledge.v1alpha1.Episode) |  |  |
| game_release | [GameRelease](#animeshon.knowledge.v1alpha1.GameRelease) |  |  |
| graphic_novel | [GraphicNovel](#animeshon.knowledge.v1alpha1.GraphicNovel) |  |  |
| light_novel | [LightNovel](#animeshon.knowledge.v1alpha1.LightNovel) |  |  |
| organization | [Organization](#animeshon.knowledge.v1alpha1.Organization) |  |  |
| person | [Person](#animeshon.knowledge.v1alpha1.Person) |  |  |
| track | [Track](#animeshon.knowledge.v1alpha1.Track) |  |  |
| universe | [Universe](#animeshon.knowledge.v1alpha1.Universe) |  |  |
| visual_novel | [VisualNovel](#animeshon.knowledge.v1alpha1.VisualNovel) |  |  |






<a name="animeshon.knowledge.v1alpha1.Episode"></a>

### Episode



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | Required resource name |
| type | [string](#string) |  | Type of the episode Valid Episode types:

Unknown episode type UNKNOWN

Regular episode REGULAR

Recapitolation episode RECAP

Parody Fan made PARODY

Promo episode PROMO

Special episode SPECIAL

Opening / ending episode OPENING_ENDING

Other OTHER |
| index | [int32](#int32) |  | Incremental index of the episode. Describes the release order |
| release_date | [google.type.Date](#google.type.Date) |  | The release date in homeland of the content |
| names | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized names of the entity |
| aliases | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized aliases of the entity |
| descriptions | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized descriptions of the entity |
| synopsys | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized synopsys of the entity |
| cover_image_id | [string](#string) |  | Cover Image id of the entity |
| banner_image_id | [string](#string) |  | Banner Image id of the entity |
| websites | [Website](#animeshon.knowledge.v1alpha1.Website) | repeated | List of websiste related to the entity. Websites might be official websites, Social, Wiki Entries |
| marketplaces | [Marketplace](#animeshon.knowledge.v1alpha1.Marketplace) | repeated | List of marketplaces related to the entry. Maketplaces tells where to buy / consume / read the entity |
| staff | [Collaboration](#animeshon.knowledge.v1alpha1.Collaboration) | repeated | List of people/organizations which contributed to the production/distribution of the content |
| soundtracks | [Soundtrack](#animeshon.knowledge.v1alpha1.Soundtrack) | repeated | List of soundtracks in the content |
| voiceactings | [VoiceActing](#animeshon.knowledge.v1alpha1.VoiceActing) | repeated | List of voice actors giving voice to the characters in the content |
| length_seconds | [int32](#int32) |  | Length of the episode in seconds. |






<a name="animeshon.knowledge.v1alpha1.GameRelease"></a>

### GameRelease



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | Required resource name |
| languages | [string](#string) | repeated | List of languages the release is localized in |
| release_date | [google.type.Date](#google.type.Date) |  | The release date in homeland of the content

repeated Media media = 4; |
| censorship | [string](#string) |  | Valid Censorships Unknown censorship UNKNOWN

No censorship NONE

Censorship applied CENSORED |
| publishing_type | [string](#string) |  | Publishin Type specifies wether the content has been produced by a self published creator or if it&#39;s backed by a corporation Valid Publishing types:

Unknown status UNKNOWN

Self publishing SELF

Published by a corporation CORPORATE |
| asin | [string](#string) |  | Amazon identifier of the good |
| gtin | [string](#string) |  | Global Trade identifier of the good |
| type | [string](#string) |  | valid game release types: Unknown game release type UNKNOWN

The release is complete COMPLETE

The release is only a part of the content PARTIAL

The release is just trial TRIAL

The release is a dlc DLC |
| IsPatch | [string](#string) |  | If patch the release is not sold alone and it&#39;s ment to be applied to an existing game Valid values:

TRUE FALSE UNKNOWN |
| dub_degree | [string](#string) |  | dub_degree describes how much of the game is dubbed Valid game dub degree

Unknown DUB degree UNKNOWN

Not dubbed NONE

Only erotic scenes are dubbed ERO_ONLY

Partially dubbed PARTIAL

Full dubbed FULL |
| story_animation_degree | [string](#string) |  | story_animation_degree specifies how well the story scenes are animated Valid game animation degrees:

Unknown animation degree UNKNOWN

No animation NONE

Simple animations SIMPLE

Partial animation - Some fully animated scenes PARTIAL

Fully animated FULL |
| ero_animation_degree | [string](#string) |  | ero_animation_degree specifies how well the erotic scenes are animated Valid game animation degrees:

Unknown animation degree UNKNOWN

No animation NONE

Simple animations SIMPLE

Partial animation - Some fully animated scenes PARTIAL

Fully animated FULL |
| engine | [string](#string) |  |  |
| platforms | [string](#string) | repeated | Valid Platforms: Unknown platform UNKNOWN 

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
| names | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized names of the entity |
| aliases | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized aliases of the entity |
| descriptions | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized descriptions of the entity |
| synopsys | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized synopsys of the entity |
| cover_image_id | [string](#string) |  | Cover Image id of the entity |
| banner_image_id | [string](#string) |  | Banner Image id of the entity |
| websites | [Website](#animeshon.knowledge.v1alpha1.Website) | repeated | List of websiste related to the entity. Websites might be official websites, Social, Wiki Entries |
| marketplaces | [Marketplace](#animeshon.knowledge.v1alpha1.Marketplace) | repeated | List of marketplaces related to the entry. Maketplaces tells where to buy / consume / read the entity |
| starring | [Cast](#animeshon.knowledge.v1alpha1.Cast) | repeated | List of characters starred in the content |
| staff | [Collaboration](#animeshon.knowledge.v1alpha1.Collaboration) | repeated | List of people/organizations which contributed to the production/distribution of the content |
| soundtracks | [Soundtrack](#animeshon.knowledge.v1alpha1.Soundtrack) | repeated | List of soundtracks in the content |
| voiceactings | [VoiceActing](#animeshon.knowledge.v1alpha1.VoiceActing) | repeated | List of voice actors giving voice to the characters in the content |
| maturity_ratings | [string](#string) | repeated | Maturity ratings describes what it the minum age to legally consume a content Valid maturity Ratings:

Over 18 in USA MTR_RTN_USA_NC17

Over 18 in USA MTR_RTN_USA_R

Over 13 in USA MTR_RTN_USA_PG13

Over 3 in USA MTR_RTN_USA_PG

Safe in USA MTR_RTN_USA_G |
| region_restrictions | [string](#string) | repeated | Region restrictions mark the content as illegal in some region given the local regulations Valid Region Restrictions:

No Region Restriction NONE

The Entity is illegal following the U.N. guidelines ILLEGAL |
| original | [string](#string) |  | Original specifies if the idea behind the content is original or if it&#39;s base on an existing opera. Parodies of other content are normally not original, because charactes/settings/storyline are not owned by the creator.

Valid values: TRUE FALSE UNKNOWN |






<a name="animeshon.knowledge.v1alpha1.GetContributionChangesRequest"></a>

### GetContributionChangesRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The resource name of the requested contribution. Required resource name |






<a name="animeshon.knowledge.v1alpha1.GetContributionRequest"></a>

### GetContributionRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The resource name of the requested contribution. Required resource name |






<a name="animeshon.knowledge.v1alpha1.GraphicNovel"></a>

### GraphicNovel



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | Required resource name |
| type | [string](#string) |  | Type of the graphic novel Valid Graphic Novel types:

Unknown graphic novel type UNKNOWN

Japanese GraphicNovel MANGA

One shot (only one volume) ONE_SHOT

Cinese GraphicNovel MANHUA

Korean GraphicNovel MANHWA

Original English Language OEL

Web native comic (webtoon) WEB_COMIC

GraphicNovel consisting of 4 pannels YON_KOMA

Other OTHER |
| chapters | [Edge](#animeshon.knowledge.v1alpha1.Edge) | repeated | List of chaters part of the graphic novel |
| chapter_count | [int32](#int32) |  | Number of scheduled chapters This field is useful for graphic novels which already announced how many chapter will be published |
| names | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized names of the entity |
| aliases | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized aliases of the entity |
| descriptions | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized descriptions of the entity |
| synopsys | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized synopsys of the entity |
| cover_image_id | [string](#string) |  | Cover Image id of the entity |
| banner_image_id | [string](#string) |  | Banner Image id of the entity |
| websites | [Website](#animeshon.knowledge.v1alpha1.Website) | repeated | List of websiste related to the entity. Websites might be official websites, Social, Wiki Entries |
| marketplaces | [Marketplace](#animeshon.knowledge.v1alpha1.Marketplace) | repeated | List of marketplaces related to the entry. Maketplaces tells where to buy / consume / read the entity |
| status | [string](#string) |  | Status of the content Valid content statuses:

Unknown status UNKNOWN

Publishing or airing is still ongoing. ONGOING

Publishing or airing has been completed. COMPLETED

Publishing or airing has been scheduled. SCHEDULED

Publishing or airing started but never finished. INTERRUPTED

Publishing or airing was scheduled but later canceled. CANCELED

Publishing or airing has been suspended / has been put on hold. SUSPENDED

The content is in work in progress WORK_IN_PROGRESS |
| content_relations | [ContentRelation](#animeshon.knowledge.v1alpha1.ContentRelation) | repeated | List of relations with other content |
| publishing_type | [string](#string) |  | Publishin Type specifies wether the content has been produced by a self published creator or if it&#39;s backed by a corporation Valid Publishing types: Unknown status UNKNOWN

Self publishing SELF

Published by a corporation CORPORATE |
| original | [string](#string) |  | Original specifies if the idea behind the content is original or if it&#39;s base on an existing opera. Parodies of other content are normally not original, because charactes/settings/storyline are not owned by the creator.

Valid values: TRUE FALSE UNKNOWN |
| runnings | [Running](#animeshon.knowledge.v1alpha1.Running) | repeated | List of localized airing/publishing periods of the content |
| release_date | [google.type.Date](#google.type.Date) |  | The release date in homeland of the content |
| starring | [Cast](#animeshon.knowledge.v1alpha1.Cast) | repeated | List of characters starred in the content |
| staff | [Collaboration](#animeshon.knowledge.v1alpha1.Collaboration) | repeated | List of people/organizations which contributed to the production/distribution of the content |
| maturity_ratings | [string](#string) | repeated | Maturity ratings describes what it the minum age to legally consume a content Valid maturity Ratings:

Over 18 in USA MTR_RTN_USA_NC17

Over 18 in USA MTR_RTN_USA_R

Over 13 in USA MTR_RTN_USA_PG13

Over 3 in USA MTR_RTN_USA_PG

Safe in USA MTR_RTN_USA_G |
| region_restrictions | [string](#string) | repeated | Region restrictions mark the content as illegal in some region given the local regulations Valid Region Restrictions:

No Region Restriction NONE

The Entity is illegal following the U.N. guidelines ILLEGAL |






<a name="animeshon.knowledge.v1alpha1.LightNovel"></a>

### LightNovel



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | Required resource name |
| chapters | [Edge](#animeshon.knowledge.v1alpha1.Edge) | repeated | List of chaters part of the light novel |
| chapter_count | [int32](#int32) |  | Number of scheduled chapters This field is useful for light novels which already announced how many chapter will be published |
| names | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized names of the entity |
| aliases | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized aliases of the entity |
| descriptions | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized descriptions of the entity |
| synopsys | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized synopsys of the entity |
| cover_image_id | [string](#string) |  | Cover Image id of the entity |
| banner_image_id | [string](#string) |  | Banner Image id of the entity |
| websites | [Website](#animeshon.knowledge.v1alpha1.Website) | repeated | List of websiste related to the entity. Websites might be official websites, Social, Wiki Entries |
| marketplaces | [Marketplace](#animeshon.knowledge.v1alpha1.Marketplace) | repeated | List of marketplaces related to the entry. Maketplaces tells where to buy / consume / read the entity |
| status | [string](#string) |  | Status of the content Valid content statuses:

Unknown status UNKNOWN

Publishing or airing is still ongoing. ONGOING

Publishing or airing has been completed. COMPLETED

Publishing or airing has been scheduled. SCHEDULED

Publishing or airing started but never finished. INTERRUPTED

Publishing or airing was scheduled but later canceled. CANCELED

Publishing or airing has been suspended / has been put on hold. SUSPENDED

The content is in work in progress WORK_IN_PROGRESS |
| content_relations | [ContentRelation](#animeshon.knowledge.v1alpha1.ContentRelation) | repeated | List of relations with other content |
| publishing_type | [string](#string) |  | Publishin Type specifies wether the content has been produced by a self published creator or if it&#39;s backed by a corporation Valid Publishing types:

Unknown status UNKNOWN

Self publishing SELF

Published by a corporation CORPORATE |
| original | [string](#string) |  | Original specifies if the idea behind the content is original or if it&#39;s base on an existing opera. Parodies of other content are normally not original, because charactes/settings/storyline are not owned by the creator.

Valid values: TRUE FALSE UNKNOWN |
| runnings | [Running](#animeshon.knowledge.v1alpha1.Running) | repeated | List of localized airing/publishing periods of the content |
| release_date | [google.type.Date](#google.type.Date) |  | The release date in homeland of the content |
| starring | [Cast](#animeshon.knowledge.v1alpha1.Cast) | repeated | List of characters starred in the content |
| staff | [Collaboration](#animeshon.knowledge.v1alpha1.Collaboration) | repeated | List of people/organizations which contributed to the production/distribution of the content |
| maturity_ratings | [string](#string) | repeated | Maturity ratings describes what it the minum age to legally consume a content Valid maturity Ratings:

Over 18 in USA MTR_RTN_USA_NC17

Over 18 in USA MTR_RTN_USA_R

Over 13 in USA MTR_RTN_USA_PG13

Over 3 in USA MTR_RTN_USA_PG

Safe in USA MTR_RTN_USA_G |
| region_restrictions | [string](#string) | repeated | Region restrictions mark the content as illegal in some region given the local regulations Valid Region Restrictions:

No Region Restriction NONE

The Entity is illegal following the U.N. guidelines ILLEGAL |






<a name="animeshon.knowledge.v1alpha1.ListContributionsRequest"></a>

### ListContributionsRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| parent | [string](#string) |  | The parent, which owns this collection of contributions. |
| page_size | [int32](#int32) |  | The maximum number of users to return. Server may return fewer users than requested. If unspecified, server will pick an appropriate default. |
| page_token | [string](#string) |  | The value returned from the previous call. |
| filter | [string](#string) |  | A filter to be applied to results. |






<a name="animeshon.knowledge.v1alpha1.ListContributionsResponse"></a>

### ListContributionsResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| contributions | [Contribution](#animeshon.knowledge.v1alpha1.Contribution) | repeated | The list of contributions. |
| next_page_token | [string](#string) |  | A token to retrieve next page of results. |






<a name="animeshon.knowledge.v1alpha1.Marketplace"></a>

### Marketplace
Marketplace is where to consume the content.
The name field must point to a valid valid marketplace id in order to load icon and name of the marketplace.
If the marketplace is limited to some specific country, add them to the field region following the IOS3 standard


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | Required resource name |
| url | [string](#string) |  | Marketplace url |
| region | [string](#string) |  | region in which the marketplace distributes |






<a name="animeshon.knowledge.v1alpha1.Organization"></a>

### Organization



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | Required resource name |
| type | [string](#string) |  | Type of the organization Valid Organization types:

Uunknown organization type UNKNOWN

Coorporation / company CORPORATE

Circle of people CIRCLE |
| foundation_date | [google.type.Date](#google.type.Date) |  | Foundation date of the organization |
| names | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized names of the entity |
| aliases | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized aliases of the entity |
| descriptions | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized descriptions of the entity |
| synopsys | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized synopsys of the entity |
| cover_image_id | [string](#string) |  | Cover Image id of the entity |
| banner_image_id | [string](#string) |  | Banner Image id of the entity |
| websites | [Website](#animeshon.knowledge.v1alpha1.Website) | repeated | List of websiste related to the entity. Websites might be official websites, Social, Wiki Entries |






<a name="animeshon.knowledge.v1alpha1.Person"></a>

### Person



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | Required resource name |
| birthday | [google.type.Date](#google.type.Date) |  | Birthday of the person |
| gender | [string](#string) |  | Gender Valid Gender values:

Unknown gender UNKNOWN 

Male MALE 

Female FEMALE |
| blood_type | [string](#string) |  | Blod Type Valid blood types:

Unknown blood type UNKNOWN

A (no Rh info) A

B (no Rh info) B

AB (no Rh info) AB

O (no Rh info) O

A&#43; A_PLUS

B&#43; B_PLUS

AB&#43; AB_PLUS

O&#43; O_PLUS

A- A_MINUS

B- B_MINUS

AB- AB_MINUS

O- O_MINUS |
| names | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized names of the entity |
| aliases | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized aliases of the entity |
| descriptions | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized descriptions of the entity |
| synopsys | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized synopsys of the entity |
| cover_image_id | [string](#string) |  | Cover Image id of the entity |
| banner_image_id | [string](#string) |  | Banner Image id of the entity |
| websites | [Website](#animeshon.knowledge.v1alpha1.Website) | repeated | List of websiste related to the entity. Websites might be official websites, Social, Wiki Entries |






<a name="animeshon.knowledge.v1alpha1.RejectContributionRequest"></a>

### RejectContributionRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | Required resource name |






<a name="animeshon.knowledge.v1alpha1.ReviewContributionRequest"></a>

### ReviewContributionRequest
ReviewContributionRequest specifies the edit to apply to an existing contribution


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | Name of the contribution |
| comment | [string](#string) |  | Optional comment on the review |
| changes | [ContributionChanges](#animeshon.knowledge.v1alpha1.ContributionChanges) |  | Changes to the existing contribution New changes will be added on top of the existing ones |
| discards | [ContributionChanges](#animeshon.knowledge.v1alpha1.ContributionChanges) |  | Changes to discard from the contribution Discarded changes will be completely removed from the contribution |






<a name="animeshon.knowledge.v1alpha1.Running"></a>

### Running
Period in which the content has been aired/released/published for a particular localization


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| start_time | [google.type.Date](#google.type.Date) |  | Start of the publishing/airing/release |
| end_time | [google.type.Date](#google.type.Date) |  | End of the publishing/airing/release Omitted if the content is still ONGOING |
| localization | [string](#string) |  | Valid ISO3 localization |






<a name="animeshon.knowledge.v1alpha1.Soundtrack"></a>

### Soundtrack
Soundtrack exposes the information about which Track has been used in which Content in which localization and for what.
The localization must be a valid ISO3 localization which identifies the language/full localization of the content&#39;s version 
for which the Track is used


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| track | [Edge](#animeshon.knowledge.v1alpha1.Edge) |  | Track used as soundtrack |
| type | [string](#string) |  | Type describes for what purpose the track was used Valid Soundtrack types:

Unknown type UNKNOWN

The track is used as ending ENDING

The track is used as opening OPENING

The track is used as insert song INSERT

The track is used as background song BACKGROUND

The track is used as image song IMAGE

The track is used as theme song THEME |
| localization | [string](#string) |  | Valid ISO3 localization in which the track was used |






<a name="animeshon.knowledge.v1alpha1.Track"></a>

### Track



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | Required resource name |
| release_date | [google.type.Date](#google.type.Date) |  | The release date in homeland of the content |
| names | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized names of the entity |
| aliases | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized aliases of the entity |
| descriptions | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized descriptions of the entity |
| synopsys | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized synopsys of the entity |
| cover_image_id | [string](#string) |  | Cover Image id of the entity |
| banner_image_id | [string](#string) |  | Banner Image id of the entity |
| websites | [Website](#animeshon.knowledge.v1alpha1.Website) | repeated | List of websiste related to the entity. Websites might be official websites, Social, Wiki Entries |
| marketplaces | [Marketplace](#animeshon.knowledge.v1alpha1.Marketplace) | repeated | List of marketplaces related to the entry. Maketplaces tells where to buy / consume / read the entity |
| staff | [Collaboration](#animeshon.knowledge.v1alpha1.Collaboration) | repeated | List of people/organizations which contributed to the production/distribution of the content |






<a name="animeshon.knowledge.v1alpha1.Universe"></a>

### Universe



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | Required resource name |
| names | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized names of the entity |
| aliases | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized aliases of the entity |
| descriptions | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized descriptions of the entity |
| synopsys | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized synopsys of the entity |
| cover_image_id | [string](#string) |  | Cover Image id of the entity |
| banner_image_id | [string](#string) |  | Banner Image id of the entity |
| websites | [Website](#animeshon.knowledge.v1alpha1.Website) | repeated | List of websiste related to the entity. Websites might be official websites, Social, Wiki Entries |
| marketplaces | [Marketplace](#animeshon.knowledge.v1alpha1.Marketplace) | repeated | List of marketplaces related to the entry. Maketplaces tells where to buy / consume / read the entity |
| contents | [Edge](#animeshon.knowledge.v1alpha1.Edge) | repeated | List of contents part of the universe Universes can include Anime, GraphicNovels, LightNovels and VisualNovels |
| canonicals | [Edge](#animeshon.knowledge.v1alpha1.Edge) | repeated | List of canonicals part of the universe |






<a name="animeshon.knowledge.v1alpha1.VisualNovel"></a>

### VisualNovel



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | Required resource name |
| length | [string](#string) |  | Valid Visual Novel lengths: Unknown length UNKNOWN

&lt; 2 hours VERY_SHORT

20 - 10 hours SHORT

10 - 30 hours MEDIUM

30 - 50 hours LONG

&gt; 50 hours VERY_LONG |
| names | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized names of the entity |
| aliases | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized aliases of the entity |
| descriptions | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized descriptions of the entity |
| synopsys | [google.type.LocalizedText](#google.type.LocalizedText) | repeated | List of localized synopsys of the entity |
| cover_image_id | [string](#string) |  | Cover Image id of the entity |
| banner_image_id | [string](#string) |  | Banner Image id of the entity |
| websites | [Website](#animeshon.knowledge.v1alpha1.Website) | repeated | List of websiste related to the entity. Websites might be official websites, Social, Wiki Entries |
| marketplaces | [Marketplace](#animeshon.knowledge.v1alpha1.Marketplace) | repeated | List of marketplaces related to the entry. Maketplaces tells where to buy / consume / read the entity |
| status | [string](#string) |  | Status of the content Valid content statuses:

Unknown status UNKNOWN

Publishing or airing is still ongoing. ONGOING

Publishing or airing has been completed. COMPLETED

Publishing or airing has been scheduled. SCHEDULED

Publishing or airing started but never finished. INTERRUPTED

Publishing or airing was scheduled but later canceled. CANCELED

Publishing or airing has been suspended / has been put on hold. SUSPENDED

The content is in work in progress WORK_IN_PROGRESS |
| content_relations | [ContentRelation](#animeshon.knowledge.v1alpha1.ContentRelation) | repeated | List of relations with other content |
| publishing_type | [string](#string) |  | Publishin Type specifies wether the content has been produced by a self published creator or if it&#39;s backed by a corporation Valid Publishing types:

Unknown status UNKNOWN

Self publishing SELF

Published by a corporation CORPORATE |
| original | [string](#string) |  | Original specifies if the idea behind the content is original or if it&#39;s base on an existing opera. Parodies of other content are normally not original, because charactes/settings/storyline are not owned by the creator.

Valid values: TRUE FALSE UNKNOWN |
| runnings | [Running](#animeshon.knowledge.v1alpha1.Running) | repeated | List of localized airing/publishing periods of the content |
| release_date | [google.type.Date](#google.type.Date) |  | The release date in homeland of the content |
| starring | [Cast](#animeshon.knowledge.v1alpha1.Cast) | repeated | List of characters starred in the content |
| staff | [Collaboration](#animeshon.knowledge.v1alpha1.Collaboration) | repeated | List of people/organizations which contributed to the production/distribution of the content |
| soundtracks | [Soundtrack](#animeshon.knowledge.v1alpha1.Soundtrack) | repeated | List of soundtracks in the content |
| voiceactings | [VoiceActing](#animeshon.knowledge.v1alpha1.VoiceActing) | repeated | List of voice actors giving voice to the characters in the content |
| maturity_ratings | [string](#string) | repeated | Maturity ratings describes what it the minum age to legally consume a content Valid maturity Ratings:

Over 18 in USA MTR_RTN_USA_NC17

Over 18 in USA MTR_RTN_USA_R

Over 13 in USA MTR_RTN_USA_PG13

Over 3 in USA MTR_RTN_USA_PG

Safe in USA MTR_RTN_USA_G |
| region_restrictions | [string](#string) | repeated | Region restrictions mark the content as illegal in some region given the local regulations Valid Region Restrictions:

No Region Restriction NONE

The Entity is illegal following the U.N. guidelines ILLEGAL |
| releases | [Edge](#animeshon.knowledge.v1alpha1.Edge) | repeated | Releases are all those entities which practically make the content consumable Some examples are: Volumes for GraphicNovels/LightNovels/Chapters, BlueRays for Anime, Collector Editions... |






<a name="animeshon.knowledge.v1alpha1.VoiceActing"></a>

### VoiceActing
Voice Acting represent voice given by a person to a voiced entity in a specific content
The Voice Acting is always field of the content and it must be localized.
The localization must be a valid ISO3 localization which identifies the language/full localization of the content&#39;s version 
for which the actor gave the voice to the entity


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| voiced | [Edge](#animeshon.knowledge.v1alpha1.Edge) |  | The entity receiving the voice Character or VoiceOver |
| actor | [Edge](#animeshon.knowledge.v1alpha1.Edge) |  | Who gave the voice |
| localization | [string](#string) |  | Valid ISO3 localization for which the voice was given |
| primary | [string](#string) |  | Voices can be primary or not. Primary voices are those lasting for the majority of the conte While Secondary voices are normally used in flashbacks or side events

Valid values: TRUE FALSE UNKNOWN |






<a name="animeshon.knowledge.v1alpha1.Website"></a>

### Website
Any kind of website related to the entity.
Could be official website, twitter, or external resources such as wikipedia


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| url | [string](#string) |  | Website url |





 


<a name="animeshon.knowledge.v1alpha1.Contribution.State"></a>

### Contribution.State


| Name | Number | Description |
| ---- | ------ | ----------- |
| PENDING | 0 |  |
| APPROVED | 1 |  |
| REJECTED | 2 |  |
| DRAFT | 3 |  |


 

 


<a name="animeshon.knowledge.v1alpha1.Knowledge"></a>

### Knowledge


| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| GetContribution | [GetContributionRequest](#animeshon.knowledge.v1alpha1.GetContributionRequest) | [Contribution](#animeshon.knowledge.v1alpha1.Contribution) |  |
| ListContributions | [ListContributionsRequest](#animeshon.knowledge.v1alpha1.ListContributionsRequest) | [ListContributionsResponse](#animeshon.knowledge.v1alpha1.ListContributionsResponse) |  |
| CreateContribution | [CreateContributionRequest](#animeshon.knowledge.v1alpha1.CreateContributionRequest) | [Contribution](#animeshon.knowledge.v1alpha1.Contribution) |  |
| GetContributionChanges | [GetContributionChangesRequest](#animeshon.knowledge.v1alpha1.GetContributionChangesRequest) | [ContributionChanges](#animeshon.knowledge.v1alpha1.ContributionChanges) |  |
| ReviewContribution | [ReviewContributionRequest](#animeshon.knowledge.v1alpha1.ReviewContributionRequest) | [Contribution](#animeshon.knowledge.v1alpha1.Contribution) | ReviewContribution allows moderators or the owner to modify and correct the contribution while in the PENDING or DRAFT state |
| ApproveContribution | [ApproveContributionRequest](#animeshon.knowledge.v1alpha1.ApproveContributionRequest) | [Contribution](#animeshon.knowledge.v1alpha1.Contribution) | ApproveContribution approves the contribution and applies the changes |
| RejectContribution | [RejectContributionRequest](#animeshon.knowledge.v1alpha1.RejectContributionRequest) | [Contribution](#animeshon.knowledge.v1alpha1.Contribution) | RejectContribution rejects the contribution and DESTROYS all the changes |
| AllocateResourceName | [AllocateResourceNameRequest](#animeshon.knowledge.v1alpha1.AllocateResourceNameRequest) | [AllocateResourceNameResponse](#animeshon.knowledge.v1alpha1.AllocateResourceNameResponse) | AllocateResourceName reserves a new resource name for entities which are not already part of Animeshon&#39;s Encyclopedia |

 



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

