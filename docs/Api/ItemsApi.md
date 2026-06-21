# ArtifactsMmo\ItemsApi



All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getAllItemsItemsGet()**](ItemsApi.md#getAllItemsItemsGet) | **GET** /items | Get All Items |
| [**getItemItemsCodeGet()**](ItemsApi.md#getItemItemsCodeGet) | **GET** /items/{code} | Get Item |


## `getAllItemsItemsGet()`

```php
getAllItemsItemsGet($name, $minLevel, $maxLevel, $type, $craftSkill, $craftMaterial, $page, $size): \ArtifactsMmo\Model\StaticDataPageItemSchema
```

Get All Items

Fetch items details.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\ItemsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$name = 'name_example'; // string | Name of the item.
$minLevel = 56; // int | Minimum level.
$maxLevel = 56; // int | Maximum level.
$type = new \ArtifactsMmo\Model\\ArtifactsMmoModelItemType(); // \ArtifactsMmoModelItemType | Type of items.
$craftSkill = new \ArtifactsMmo\Model\\ArtifactsMmoModelCraftSkill(); // \ArtifactsMmoModelCraftSkill | Skill to craft items.
$craftMaterial = 'craftMaterial_example'; // string | Item code of items used as material for crafting.
$page = 1; // int | Page number
$size = 50; // int | Page size

try {
    $result = $apiInstance->getAllItemsItemsGet($name, $minLevel, $maxLevel, $type, $craftSkill, $craftMaterial, $page, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ItemsApi->getAllItemsItemsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **name** | **string**| Name of the item. | [optional] |
| **minLevel** | **int**| Minimum level. | [optional] |
| **maxLevel** | **int**| Maximum level. | [optional] |
| **type** | [**\ArtifactsMmoModelItemType**](../Model/.md)| Type of items. | [optional] |
| **craftSkill** | [**\ArtifactsMmoModelCraftSkill**](../Model/.md)| Skill to craft items. | [optional] |
| **craftMaterial** | **string**| Item code of items used as material for crafting. | [optional] |
| **page** | **int**| Page number | [optional] [default to 1] |
| **size** | **int**| Page size | [optional] [default to 50] |

### Return type

[**\ArtifactsMmo\Model\StaticDataPageItemSchema**](../Model/StaticDataPageItemSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getItemItemsCodeGet()`

```php
getItemItemsCodeGet($code): \ArtifactsMmo\Model\ItemResponseSchema
```

Get Item

Retrieve the details of a item.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\ItemsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$code = 'code_example'; // string | The code of the item.

try {
    $result = $apiInstance->getItemItemsCodeGet($code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ItemsApi->getItemItemsCodeGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**| The code of the item. | |

### Return type

[**\ArtifactsMmo\Model\ItemResponseSchema**](../Model/ItemResponseSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
