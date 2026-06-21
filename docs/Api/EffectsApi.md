# ArtifactsMmo\EffectsApi



All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getAllEffectsEffectsGet()**](EffectsApi.md#getAllEffectsEffectsGet) | **GET** /effects | Get All Effects |
| [**getEffectEffectsCodeGet()**](EffectsApi.md#getEffectEffectsCodeGet) | **GET** /effects/{code} | Get Effect |


## `getAllEffectsEffectsGet()`

```php
getAllEffectsEffectsGet($page, $size): \ArtifactsMmo\Model\StaticDataPageEffectSchema
```

Get All Effects

List of all effects. Effects are used by equipment, tools, runes, consumables and monsters. An effect is an action that produces an effect on the game.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\EffectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$page = 1; // int | Page number
$size = 50; // int | Page size

try {
    $result = $apiInstance->getAllEffectsEffectsGet($page, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EffectsApi->getAllEffectsEffectsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**| Page number | [optional] [default to 1] |
| **size** | **int**| Page size | [optional] [default to 50] |

### Return type

[**\ArtifactsMmo\Model\StaticDataPageEffectSchema**](../Model/StaticDataPageEffectSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getEffectEffectsCodeGet()`

```php
getEffectEffectsCodeGet($code): \ArtifactsMmo\Model\EffectResponseSchema
```

Get Effect

Retrieve the details of an effect.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\EffectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$code = 'code_example'; // string | The code of the effect.

try {
    $result = $apiInstance->getEffectEffectsCodeGet($code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EffectsApi->getEffectEffectsCodeGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**| The code of the effect. | |

### Return type

[**\ArtifactsMmo\Model\EffectResponseSchema**](../Model/EffectResponseSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
