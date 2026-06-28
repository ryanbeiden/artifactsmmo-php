# ArtifactsMmo\RaidsApi



All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getAllRaidsRaidsGet()**](RaidsApi.md#getAllRaidsRaidsGet) | **GET** /raids | Get All Raids |
| [**getRaidLeaderboardRaidsCodeLeaderboardGet()**](RaidsApi.md#getRaidLeaderboardRaidsCodeLeaderboardGet) | **GET** /raids/{code}/leaderboard | Get Raid Leaderboard |
| [**getRaidRaidsCodeGet()**](RaidsApi.md#getRaidRaidsCodeGet) | **GET** /raids/{code} | Get Raid |


## `getAllRaidsRaidsGet()`

```php
getAllRaidsRaidsGet($name, $active, $page, $size): \ArtifactsMmo\Model\StaticDataPageRaidSchema
```

Get All Raids

Fetch the list of all raids.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\RaidsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$name = 'name_example'; // string | Name of the raid.
$active = True; // bool | Filter raids by active status.
$page = 1; // int | Page number
$size = 50; // int | Page size

try {
    $result = $apiInstance->getAllRaidsRaidsGet($name, $active, $page, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RaidsApi->getAllRaidsRaidsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **name** | **string**| Name of the raid. | [optional] |
| **active** | **bool**| Filter raids by active status. | [optional] |
| **page** | **int**| Page number | [optional] [default to 1] |
| **size** | **int**| Page size | [optional] [default to 50] |

### Return type

[**\ArtifactsMmo\Model\StaticDataPageRaidSchema**](../Model/StaticDataPageRaidSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getRaidLeaderboardRaidsCodeLeaderboardGet()`

```php
getRaidLeaderboardRaidsCodeLeaderboardGet($code, $page, $size): \ArtifactsMmo\Model\DataPageRaidLeaderboardEntrySchema
```

Get Raid Leaderboard

Retrieve the leaderboard for the active or latest raid instance.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\RaidsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$code = 'code_example'; // string | The code of the raid.
$page = 1; // int | Page number
$size = 50; // int | Page size

try {
    $result = $apiInstance->getRaidLeaderboardRaidsCodeLeaderboardGet($code, $page, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RaidsApi->getRaidLeaderboardRaidsCodeLeaderboardGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**| The code of the raid. | |
| **page** | **int**| Page number | [optional] [default to 1] |
| **size** | **int**| Page size | [optional] [default to 50] |

### Return type

[**\ArtifactsMmo\Model\DataPageRaidLeaderboardEntrySchema**](../Model/DataPageRaidLeaderboardEntrySchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getRaidRaidsCodeGet()`

```php
getRaidRaidsCodeGet($code): \ArtifactsMmo\Model\RaidResponseSchema
```

Get Raid

Retrieve the details of a specific raid.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\RaidsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$code = 'code_example'; // string | The code of the raid.

try {
    $result = $apiInstance->getRaidRaidsCodeGet($code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RaidsApi->getRaidRaidsCodeGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**| The code of the raid. | |

### Return type

[**\ArtifactsMmo\Model\RaidResponseSchema**](../Model/RaidResponseSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
