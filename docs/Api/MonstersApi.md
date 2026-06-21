# ArtifactsMmo\MonstersApi



All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getAllMonstersMonstersGet()**](MonstersApi.md#getAllMonstersMonstersGet) | **GET** /monsters | Get All Monsters |
| [**getMonsterMonstersCodeGet()**](MonstersApi.md#getMonsterMonstersCodeGet) | **GET** /monsters/{code} | Get Monster |


## `getAllMonstersMonstersGet()`

```php
getAllMonstersMonstersGet($name, $minLevel, $maxLevel, $drop, $page, $size): \ArtifactsMmo\Model\StaticDataPageMonsterSchema
```

Get All Monsters

Fetch monsters details.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\MonstersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$name = 'name_example'; // string | Name of the monster.
$minLevel = 56; // int | Minimum level.
$maxLevel = 56; // int | Maximum level.
$drop = 'drop_example'; // string | Item code of the drop.
$page = 1; // int | Page number
$size = 50; // int | Page size

try {
    $result = $apiInstance->getAllMonstersMonstersGet($name, $minLevel, $maxLevel, $drop, $page, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MonstersApi->getAllMonstersMonstersGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **name** | **string**| Name of the monster. | [optional] |
| **minLevel** | **int**| Minimum level. | [optional] |
| **maxLevel** | **int**| Maximum level. | [optional] |
| **drop** | **string**| Item code of the drop. | [optional] |
| **page** | **int**| Page number | [optional] [default to 1] |
| **size** | **int**| Page size | [optional] [default to 50] |

### Return type

[**\ArtifactsMmo\Model\StaticDataPageMonsterSchema**](../Model/StaticDataPageMonsterSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getMonsterMonstersCodeGet()`

```php
getMonsterMonstersCodeGet($code): \ArtifactsMmo\Model\MonsterResponseSchema
```

Get Monster

Retrieve the details of a monster.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\MonstersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$code = 'code_example'; // string | The code of the monster.

try {
    $result = $apiInstance->getMonsterMonstersCodeGet($code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MonstersApi->getMonsterMonstersCodeGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**| The code of the monster. | |

### Return type

[**\ArtifactsMmo\Model\MonsterResponseSchema**](../Model/MonsterResponseSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
