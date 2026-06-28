# RaidSchema

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | **string** | Raid code. |
**name** | **string** | Raid name. |
**description** | **string** | Raid description. | [optional]
**monster** | **string** | Monster code used for raid combat simulation. |
**schedule** | [**\ArtifactsMmo\Model\RaidScheduleSchema**](RaidScheduleSchema.md) | Weekly raid opening schedule. |
**rewards** | [**\ArtifactsMmo\Model\RaidRewardsSchema**](RaidRewardsSchema.md) | Reward rules for the raid. | [optional]
**status** | [**\ArtifactsMmo\Model\RaidStatus**](RaidStatus.md) | Current overall raid status. |
**nextStartAt** | **\DateTime** | Datetime for the next scheduled raid opening in UTC. |
**participantCount** | **int** | Number of distinct accounts that contributed to the active or latest raid instance. | [optional] [default to 0]
**activeInstance** | [**\ArtifactsMmo\Model\RaidInstanceSchema**](RaidInstanceSchema.md) | Currently active weekly raid instance, if any. | [optional]
**latestInstance** | [**\ArtifactsMmo\Model\RaidInstanceSchema**](RaidInstanceSchema.md) | Latest weekly raid instance, active or finished. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
