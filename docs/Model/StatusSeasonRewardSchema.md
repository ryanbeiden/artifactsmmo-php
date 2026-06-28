# StatusSeasonRewardSchema

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | **string** | Unique code identifying this reward. |
**type** | [**\ArtifactsMmo\Model\RewardType**](RewardType.md) | Type of the reward. |
**description** | **string** | Description of how to earn this reward. |
**requiredPoints** | **int** | Number of achievement points required to earn this reward. |
**quantity** | **int** | Quantity of the reward (e.g., gold amount, item quantity). | [optional] [default to 1]
**memberRequired** | **bool** | Whether member status is required to earn this reward. | [optional] [default to false]
**firstOnly** | **bool** | Whether this reward is only for the first player to reach the required points. | [optional] [default to false]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
