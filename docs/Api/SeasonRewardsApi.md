# ArtifactsMmo\SeasonRewardsApi



All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getAllSeasonRewardsSeasonRewardsGet()**](SeasonRewardsApi.md#getAllSeasonRewardsSeasonRewardsGet) | **GET** /season_rewards | Get All Season Rewards |
| [**getSeasonRewardsByCodeSeasonRewardsCodeGet()**](SeasonRewardsApi.md#getSeasonRewardsByCodeSeasonRewardsCodeGet) | **GET** /season_rewards/{code} | Get Season Rewards By Code |


## `getAllSeasonRewardsSeasonRewardsGet()`

```php
getAllSeasonRewardsSeasonRewardsGet($type, $page, $size): \ArtifactsMmo\Model\StaticDataPageSeasonRewardSchema
```

Get All Season Rewards

List of all rewards for the current season.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\SeasonRewardsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$type = new \ArtifactsMmo\Model\\ArtifactsMmoModelRewardType(); // \ArtifactsMmoModelRewardType | Filter by reward type.
$page = 1; // int | Page number
$size = 50; // int | Page size

try {
    $result = $apiInstance->getAllSeasonRewardsSeasonRewardsGet($type, $page, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SeasonRewardsApi->getAllSeasonRewardsSeasonRewardsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **type** | [**\ArtifactsMmoModelRewardType**](../Model/.md)| Filter by reward type. | [optional] |
| **page** | **int**| Page number | [optional] [default to 1] |
| **size** | **int**| Page size | [optional] [default to 50] |

### Return type

[**\ArtifactsMmo\Model\StaticDataPageSeasonRewardSchema**](../Model/StaticDataPageSeasonRewardSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getSeasonRewardsByCodeSeasonRewardsCodeGet()`

```php
getSeasonRewardsByCodeSeasonRewardsCodeGet($code, $page, $size): \ArtifactsMmo\Model\StaticDataPageSeasonRewardSchema
```

Get Season Rewards By Code

List all season rewards matching a specific code.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\SeasonRewardsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$code = 'code_example'; // string | The code of the season reward.
$page = 1; // int | Page number
$size = 50; // int | Page size

try {
    $result = $apiInstance->getSeasonRewardsByCodeSeasonRewardsCodeGet($code, $page, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SeasonRewardsApi->getSeasonRewardsByCodeSeasonRewardsCodeGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**| The code of the season reward. | |
| **page** | **int**| Page number | [optional] [default to 1] |
| **size** | **int**| Page size | [optional] [default to 50] |

### Return type

[**\ArtifactsMmo\Model\StaticDataPageSeasonRewardSchema**](../Model/StaticDataPageSeasonRewardSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
