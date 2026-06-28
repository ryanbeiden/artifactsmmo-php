# EventSchema

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Name of the event. |
**code** | **string** | Code of the event. |
**content** | [**\ArtifactsMmo\Model\EventContentSchema**](EventContentSchema.md) | Content of the event. | [optional]
**maps** | [**\ArtifactsMmo\Model\EventMapSchema[]**](EventMapSchema.md) | Map list of the event. |
**duration** | **int** | Duration in minutes. |
**rate** | **int** | Rate spawn of the event. (1/rate every minute) |
**cooldown** | **int** | Cooldown in minutes before the event can be spawned with gems. | [optional] [default to 0]
**price** | **int** | Price in gems to spawn the event. Null if not purchasable. | [optional]
**transition** | [**\ArtifactsMmo\Model\TransitionSchema**](TransitionSchema.md) | Transition to add to the map when event is active. | [optional]
**cooldownExpiration** | **\DateTime** | Gems spawn cooldown expiration datetime (null if not on cooldown). | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
