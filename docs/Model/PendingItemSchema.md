# PendingItemSchema

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Pending item ID. |
**account** | **string** | Account username. |
**source** | [**\ArtifactsMmo\Model\PendingItemSource**](PendingItemSource.md) | Source of the pending item. |
**sourceId** | **string** | ID reference for the source (e.g., achievement code, order id). | [optional]
**description** | **string** | Description for display. |
**gold** | **int** | Gold amount. | [optional] [default to 0]
**items** | [**\ArtifactsMmo\Model\SimpleItemSchema[]**](SimpleItemSchema.md) | List of items to be claimed. | [optional]
**createdAt** | **\DateTime** | When the pending item was created. |
**claimedAt** | **\DateTime** | When the pending item was claimed. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
