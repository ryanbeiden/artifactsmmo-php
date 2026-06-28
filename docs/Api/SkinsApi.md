# ArtifactsMmo\SkinsApi



All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getAllSkinsSkinsGet()**](SkinsApi.md#getAllSkinsSkinsGet) | **GET** /skins | Get All Skins |
| [**getSkinSkinsCodeGet()**](SkinsApi.md#getSkinSkinsCodeGet) | **GET** /skins/{code} | Get Skin |


## `getAllSkinsSkinsGet()`

```php
getAllSkinsSkinsGet($page, $size): \ArtifactsMmo\Model\StaticDataPageSkinSchema
```

Get All Skins

List of all skins available in the game.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\SkinsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$page = 1; // int | Page number
$size = 50; // int | Page size

try {
    $result = $apiInstance->getAllSkinsSkinsGet($page, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SkinsApi->getAllSkinsSkinsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**| Page number | [optional] [default to 1] |
| **size** | **int**| Page size | [optional] [default to 50] |

### Return type

[**\ArtifactsMmo\Model\StaticDataPageSkinSchema**](../Model/StaticDataPageSkinSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getSkinSkinsCodeGet()`

```php
getSkinSkinsCodeGet($code): \ArtifactsMmo\Model\SkinResponseSchema
```

Get Skin

Retrieve the details of a skin.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\SkinsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$code = 'code_example'; // string | The code of the skin.

try {
    $result = $apiInstance->getSkinSkinsCodeGet($code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SkinsApi->getSkinSkinsCodeGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**| The code of the skin. | |

### Return type

[**\ArtifactsMmo\Model\SkinResponseSchema**](../Model/SkinResponseSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
