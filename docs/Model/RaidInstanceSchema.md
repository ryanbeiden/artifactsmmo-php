# RaidInstanceSchema

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**startsAt** | **\DateTime** | Weekly raid opening datetime in UTC. |
**endsAt** | **\DateTime** | Weekly raid planned closing datetime in UTC. |
**status** | [**\ArtifactsMmo\Model\RaidStatus**](RaidStatus.md) | Current status of this weekly raid instance. |
**totalHp** | **int** | Shared HP pool when this raid instance starts. |
**remainingHp** | **int** | Remaining shared HP pool for this raid instance. |
**participantCount** | **int** | Number of accounts that contributed during this raid instance. | [optional] [default to 0]
**endedAt** | **\DateTime** | Datetime when this raid instance actually ended. | [optional]
**result** | [**\ArtifactsMmo\Model\RaidInstanceResult**](RaidInstanceResult.md) | Final result for this raid instance. | [optional]
**rewardsDistributedAt** | **\DateTime** | Datetime when rewards were distributed for this raid instance. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
