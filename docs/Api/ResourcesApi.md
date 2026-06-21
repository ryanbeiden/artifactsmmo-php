# ArtifactsMmo\ResourcesApi



All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getAllResourcesResourcesGet()**](ResourcesApi.md#getAllResourcesResourcesGet) | **GET** /resources | Get All Resources |
| [**getResourceResourcesCodeGet()**](ResourcesApi.md#getResourceResourcesCodeGet) | **GET** /resources/{code} | Get Resource |


## `getAllResourcesResourcesGet()`

```php
getAllResourcesResourcesGet($minLevel, $maxLevel, $skill, $drop, $page, $size): \ArtifactsMmo\Model\StaticDataPageResourceSchema
```

Get All Resources

Fetch resources details.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\ResourcesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$minLevel = 56; // int | Minimum level.
$maxLevel = 56; // int | Maximum level.
$skill = new \ArtifactsMmo\Model\\ArtifactsMmoModelGatheringSkill(); // \ArtifactsMmoModelGatheringSkill | Skill of resources.
$drop = 'drop_example'; // string | Item code of the drop.
$page = 1; // int | Page number
$size = 50; // int | Page size

try {
    $result = $apiInstance->getAllResourcesResourcesGet($minLevel, $maxLevel, $skill, $drop, $page, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesApi->getAllResourcesResourcesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **minLevel** | **int**| Minimum level. | [optional] |
| **maxLevel** | **int**| Maximum level. | [optional] |
| **skill** | [**\ArtifactsMmoModelGatheringSkill**](../Model/.md)| Skill of resources. | [optional] |
| **drop** | **string**| Item code of the drop. | [optional] |
| **page** | **int**| Page number | [optional] [default to 1] |
| **size** | **int**| Page size | [optional] [default to 50] |

### Return type

[**\ArtifactsMmo\Model\StaticDataPageResourceSchema**](../Model/StaticDataPageResourceSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getResourceResourcesCodeGet()`

```php
getResourceResourcesCodeGet($code): \ArtifactsMmo\Model\ResourceResponseSchema
```

Get Resource

Retrieve the details of a resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\ResourcesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$code = 'code_example'; // string | The code of the resource.

try {
    $result = $apiInstance->getResourceResourcesCodeGet($code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesApi->getResourceResourcesCodeGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**| The code of the resource. | |

### Return type

[**\ArtifactsMmo\Model\ResourceResponseSchema**](../Model/ResourceResponseSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
