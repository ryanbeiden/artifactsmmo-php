# MonsterSchema

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Name of the monster. |
**code** | **string** | The code of the monster. This is the monster&#39;s unique identifier (ID). |
**level** | **int** | Monster level. |
**type** | [**\ArtifactsMmo\Model\MonsterType**](MonsterType.md) | Monster type. |
**hp** | **int** | Monster hit points. |
**attackFire** | **int** | Monster fire attack. |
**attackEarth** | **int** | Monster earth attack. |
**attackWater** | **int** | Monster water attack. |
**attackAir** | **int** | Monster air attack. |
**resFire** | **int** | Monster % fire resistance. |
**resEarth** | **int** | Monster % earth resistance. |
**resWater** | **int** | Monster % water resistance. |
**resAir** | **int** | Monster % air resistance. |
**criticalStrike** | **int** | Monster % critical strike. |
**initiative** | **int** | Monster initiative for turn order. |
**effects** | [**\ArtifactsMmo\Model\SimpleEffectSchema[]**](SimpleEffectSchema.md) | List of effects. | [optional]
**minGold** | **int** | Monster minimum gold drop. |
**maxGold** | **int** | Monster maximum gold drop. |
**drops** | [**\ArtifactsMmo\Model\DropRateSchema[]**](DropRateSchema.md) | Monster drops. This is a list of items that the monster drops after killing the monster. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
