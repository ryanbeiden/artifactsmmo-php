# SubscriptionSchema

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**plan** | [**\ArtifactsMmo\Model\SubscriptionPlan**](SubscriptionPlan.md) | Subscription plan (monthly, annual, or prepaid). |
**purchaseSource** | **string** | How the subscription was purchased. Mixed means both gems and member tokens were used. |
**status** | **string** | Subscription status (active, cancelled, past_due, expired). |
**currentPeriodStart** | **\DateTime** | Start of the current billing period. |
**currentPeriodEnd** | **\DateTime** | End of the current billing period. |
**createdAt** | **\DateTime** | When the subscription was created. |
**cancelledAt** | **\DateTime** | When the subscription was cancelled. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
