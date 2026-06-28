# MyAccountDetails

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**username** | **string** | Username. |
**email** | **string** | Email. |
**member** | **bool** | Member status. |
**memberExpiration** | **\DateTime** | Membership expiration date. | [optional]
**status** | [**\ArtifactsMmo\Model\AccountStatus**](AccountStatus.md) | Account status. |
**badges** | **string[]** | Account badges. | [optional]
**skins** | **string[]** | Skins owned. |
**gems** | **int** | Gems. |
**memberToken** | **int** | Member tokens manually granted as rewards for events. Each token can be redeemed for one month of membership. | [optional] [default to 0]
**achievementsPoints** | **int** | Achievement points. |
**banned** | **bool** | Banned. |
**banReason** | **string** | Ban reason. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
