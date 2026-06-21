# AccountAchievementSchema

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Name of the achievement. |
**code** | **string** | Code of the achievement. |
**description** | **string** | Description of the achievement. |
**points** | **int** | Points of the achievement. Used for the leaderboard. |
**objectives** | [**\ArtifactsMmo\Model\AccountAchievementObjectiveSchema[]**](AccountAchievementObjectiveSchema.md) | List of objectives with progress. |
**rewards** | [**\ArtifactsMmo\Model\AchievementRewardsSchema**](AchievementRewardsSchema.md) | Rewards. |
**completedAt** | **\DateTime** | Completion timestamp. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
