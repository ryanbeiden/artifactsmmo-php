# ItemSchema

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Item name. |
**code** | **string** | Item code. This is the item&#39;s unique identifier (ID). |
**level** | **int** | Item level. |
**type** | **string** | Item type. |
**subtype** | **string** | Item subtype. |
**description** | **string** | Item description. |
**conditions** | [**\ArtifactsMmo\Model\ConditionSchema[]**](ConditionSchema.md) | Item conditions. If applicable. Conditions for using or equipping the item. | [optional]
**effects** | [**\ArtifactsMmo\Model\SimpleEffectSchema[]**](SimpleEffectSchema.md) | List of object effects. For equipment, it will include item stats. | [optional]
**craft** | [**\ArtifactsMmo\Model\CraftSchema**](CraftSchema.md) | Craft information. If applicable. | [optional]
**tradeable** | **bool** | Item tradeable status. A non-tradeable item cannot be exchanged or sold. |
**recyclable** | **bool** | Item recyclable status. A recyclable item can be recycled at the matching workshop. | [optional] [default to false]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
