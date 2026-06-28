# ArtifactsMmo\NPCsApi



All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getAllNpcsItemsNpcsItemsGet()**](NPCsApi.md#getAllNpcsItemsNpcsItemsGet) | **GET** /npcs/items | Get All Npcs Items |
| [**getAllNpcsNpcsDetailsGet()**](NPCsApi.md#getAllNpcsNpcsDetailsGet) | **GET** /npcs/details | Get All Npcs |
| [**getNpcItemsNpcsItemsCodeGet()**](NPCsApi.md#getNpcItemsNpcsItemsCodeGet) | **GET** /npcs/items/{code} | Get Npc Items |
| [**getNpcNpcsDetailsCodeGet()**](NPCsApi.md#getNpcNpcsDetailsCodeGet) | **GET** /npcs/details/{code} | Get Npc |


## `getAllNpcsItemsNpcsItemsGet()`

```php
getAllNpcsItemsNpcsItemsGet($code, $npc, $currency, $page, $size): \ArtifactsMmo\Model\StaticDataPageNPCItemSchema
```

Get All Npcs Items

Retrieve the list of all NPC items.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\NPCsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$code = 'code_example'; // string | Item code.
$npc = 'npc_example'; // string | NPC code.
$currency = 'currency_example'; // string | Currency code.
$page = 1; // int | Page number
$size = 50; // int | Page size

try {
    $result = $apiInstance->getAllNpcsItemsNpcsItemsGet($code, $npc, $currency, $page, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NPCsApi->getAllNpcsItemsNpcsItemsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**| Item code. | [optional] |
| **npc** | **string**| NPC code. | [optional] |
| **currency** | **string**| Currency code. | [optional] |
| **page** | **int**| Page number | [optional] [default to 1] |
| **size** | **int**| Page size | [optional] [default to 50] |

### Return type

[**\ArtifactsMmo\Model\StaticDataPageNPCItemSchema**](../Model/StaticDataPageNPCItemSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAllNpcsNpcsDetailsGet()`

```php
getAllNpcsNpcsDetailsGet($name, $type, $currency, $item, $page, $size): \ArtifactsMmo\Model\StaticDataPageNPCSchema
```

Get All Npcs

Fetch NPCs details.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\NPCsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$name = 'name_example'; // string | NPC name.
$type = new \ArtifactsMmo\Model\\ArtifactsMmoModelNPCType(); // \ArtifactsMmoModelNPCType | Type of NPCs.
$currency = 'currency_example'; // string | Currency code to filter NPCs that trade with this currency.
$item = 'item_example'; // string | Item code to filter NPCs that trade this item.
$page = 1; // int | Page number
$size = 50; // int | Page size

try {
    $result = $apiInstance->getAllNpcsNpcsDetailsGet($name, $type, $currency, $item, $page, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NPCsApi->getAllNpcsNpcsDetailsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **name** | **string**| NPC name. | [optional] |
| **type** | [**\ArtifactsMmoModelNPCType**](../Model/.md)| Type of NPCs. | [optional] |
| **currency** | **string**| Currency code to filter NPCs that trade with this currency. | [optional] |
| **item** | **string**| Item code to filter NPCs that trade this item. | [optional] |
| **page** | **int**| Page number | [optional] [default to 1] |
| **size** | **int**| Page size | [optional] [default to 50] |

### Return type

[**\ArtifactsMmo\Model\StaticDataPageNPCSchema**](../Model/StaticDataPageNPCSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getNpcItemsNpcsItemsCodeGet()`

```php
getNpcItemsNpcsItemsCodeGet($code, $page, $size): \ArtifactsMmo\Model\StaticDataPageNPCItemSchema
```

Get Npc Items

Retrieve the items list of a NPC. If the NPC has items to buy, sell or trade, they will be displayed.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\NPCsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$code = 'code_example'; // string | The code of the NPC.
$page = 1; // int | Page number
$size = 50; // int | Page size

try {
    $result = $apiInstance->getNpcItemsNpcsItemsCodeGet($code, $page, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NPCsApi->getNpcItemsNpcsItemsCodeGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**| The code of the NPC. | |
| **page** | **int**| Page number | [optional] [default to 1] |
| **size** | **int**| Page size | [optional] [default to 50] |

### Return type

[**\ArtifactsMmo\Model\StaticDataPageNPCItemSchema**](../Model/StaticDataPageNPCItemSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getNpcNpcsDetailsCodeGet()`

```php
getNpcNpcsDetailsCodeGet($code): \ArtifactsMmo\Model\NPCResponseSchema
```

Get Npc

Retrieve the details of a NPC.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\NPCsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$code = 'code_example'; // string | The code of the NPC.

try {
    $result = $apiInstance->getNpcNpcsDetailsCodeGet($code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NPCsApi->getNpcNpcsDetailsCodeGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**| The code of the NPC. | |

### Return type

[**\ArtifactsMmo\Model\NPCResponseSchema**](../Model/NPCResponseSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
