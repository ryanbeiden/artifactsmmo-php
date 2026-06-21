# ArtifactsMmo\BadgesApi



All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getAllBadgesBadgesGet()**](BadgesApi.md#getAllBadgesBadgesGet) | **GET** /badges | Get All Badges |
| [**getBadgeBadgesCodeGet()**](BadgesApi.md#getBadgeBadgesCodeGet) | **GET** /badges/{code} | Get Badge |


## `getAllBadgesBadgesGet()`

```php
getAllBadgesBadgesGet($page, $size): \ArtifactsMmo\Model\StaticDataPageBadgeSchema
```

Get All Badges

List of all badges.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\BadgesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$page = 1; // int | Page number
$size = 50; // int | Page size

try {
    $result = $apiInstance->getAllBadgesBadgesGet($page, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BadgesApi->getAllBadgesBadgesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**| Page number | [optional] [default to 1] |
| **size** | **int**| Page size | [optional] [default to 50] |

### Return type

[**\ArtifactsMmo\Model\StaticDataPageBadgeSchema**](../Model/StaticDataPageBadgeSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getBadgeBadgesCodeGet()`

```php
getBadgeBadgesCodeGet($code): \ArtifactsMmo\Model\BadgeResponseSchema
```

Get Badge

Retrieve the details of a badge.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\BadgesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$code = 'code_example'; // string | The code of the badge.

try {
    $result = $apiInstance->getBadgeBadgesCodeGet($code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BadgesApi->getBadgeBadgesCodeGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**| The code of the badge. | |

### Return type

[**\ArtifactsMmo\Model\BadgeResponseSchema**](../Model/BadgeResponseSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
