vim.profile.ProfileMetadata
===========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This data object represents the metadata information of a Profile.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | Type of the Profile |
| profileTypeName | string | true | None | Type identifier for the ApplyProfile |
| description | [vim.ExtendedDescription](vim.ExtendedDescription.md "vim.ExtendedDescription") | true | None | Property which describes the profile |
| sortSpec | [vim.profile.ProfileMetadata.ProfileSortSpec](vim.profile.ProfileMetadata.ProfileSortSpec.md "vim.profile.ProfileMetadata.ProfileSortSpec") | true | None | Property that determines a sorting order for display purposes. If  the list contains more than one sort spec, then the precedence should  be determined by the list order (i.e. sort first by the first spec in  the list, then sort by the second spec in the list, etc). |
| profileCategory | string | true | None | Identifies the profile category that this subprofile is a part of. The  value of this string should correspond to the key value of a  <a href="vim.profile.ProfileCategoryMetadata.md">ProfileCategoryMetadata</a> object's <a href="vim.ElementDescription.md#key">key</a>  in its <a href="vim.profile.ProfileCategoryMetadata.md#id">id</a> property. |
| profileComponent | string | true | None | Property indicating that the subprofile described by this  <code>ProfileMetadata</code> object is declared in the  <a href="vim.profile.ProfileComponentMetadata.md#profileTypeNames">profileTypeNames</a> of the specified  profile component. The value of this property should correspond to the key  value of the <a href="vim.profile.ProfileComponentMetadata.md">ProfileComponentMetadata</a> object's  <a href="vim.ElementDescription.md#key">key</a> in its  <a href="vim.profile.ProfileComponentMetadata.md#id">id</a> property.   This property should not be present for subprofiles that are not directly  declared in the <a href="vim.profile.ProfileComponentMetadata.md#profileTypeNames">profileTypeNames</a>  property of a <a href="vim.profile.ProfileComponentMetadata.md">ProfileComponentMetadata</a> object. |


