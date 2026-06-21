# StatusSchema

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**version** | **string** | Game version. |
**serverTime** | **\DateTime** | Server time. |
**maxLevel** | **int** | Maximum level. |
**maxSkillLevel** | **int** | Maximum skill level. |
**charactersOnline** | **int** | Characters online. |
**season** | [**\ArtifactsMmo\Model\SeasonSchema**](SeasonSchema.md) | Current season details. | [optional]
**rateLimits** | [**\ArtifactsMmo\Model\RateLimitSchema[]**](RateLimitSchema.md) | Rate limits. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
