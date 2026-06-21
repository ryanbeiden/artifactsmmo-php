# ArtifactsMmo\EventsApi



All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getAllActiveEventsEventsActiveGet()**](EventsApi.md#getAllActiveEventsEventsActiveGet) | **GET** /events/active | Get All Active Events |
| [**getAllEventsEventsGet()**](EventsApi.md#getAllEventsEventsGet) | **GET** /events | Get All Events |
| [**spawnEventEventsSpawnPost()**](EventsApi.md#spawnEventEventsSpawnPost) | **POST** /events/spawn | Spawn Event |


## `getAllActiveEventsEventsActiveGet()`

```php
getAllActiveEventsEventsActiveGet($page, $size): \ArtifactsMmo\Model\StaticDataPageActiveEventSchema
```

Get All Active Events

Fetch active events details.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\EventsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$page = 1; // int | Page number
$size = 50; // int | Page size

try {
    $result = $apiInstance->getAllActiveEventsEventsActiveGet($page, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EventsApi->getAllActiveEventsEventsActiveGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**| Page number | [optional] [default to 1] |
| **size** | **int**| Page size | [optional] [default to 50] |

### Return type

[**\ArtifactsMmo\Model\StaticDataPageActiveEventSchema**](../Model/StaticDataPageActiveEventSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAllEventsEventsGet()`

```php
getAllEventsEventsGet($type, $page, $size): \ArtifactsMmo\Model\StaticDataPageEventSchema
```

Get All Events

Fetch events details.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\EventsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$type = new \ArtifactsMmo\Model\\ArtifactsMmoModelMapContentType(); // \ArtifactsMmoModelMapContentType | Type of events.
$page = 1; // int | Page number
$size = 50; // int | Page size

try {
    $result = $apiInstance->getAllEventsEventsGet($type, $page, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EventsApi->getAllEventsEventsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **type** | [**\ArtifactsMmoModelMapContentType**](../Model/.md)| Type of events. | [optional] |
| **page** | **int**| Page number | [optional] [default to 1] |
| **size** | **int**| Page size | [optional] [default to 50] |

### Return type

[**\ArtifactsMmo\Model\StaticDataPageEventSchema**](../Model/StaticDataPageEventSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `spawnEventEventsSpawnPost()`

```php
spawnEventEventsSpawnPost($spawnEventRequest): \ArtifactsMmo\Model\ActiveEventResponseSchema
```

Spawn Event

Spawn a specific event by consuming 1 event token. Member or founder account required.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: JWTBearer
$config = ArtifactsMmo\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new ArtifactsMmo\Api\EventsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$spawnEventRequest = new \ArtifactsMmo\Model\SpawnEventRequest(); // \ArtifactsMmo\Model\SpawnEventRequest

try {
    $result = $apiInstance->spawnEventEventsSpawnPost($spawnEventRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EventsApi->spawnEventEventsSpawnPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **spawnEventRequest** | [**\ArtifactsMmo\Model\SpawnEventRequest**](../Model/SpawnEventRequest.md)|  | |

### Return type

[**\ArtifactsMmo\Model\ActiveEventResponseSchema**](../Model/ActiveEventResponseSchema.md)

### Authorization

[JWTBearer](../../README.md#JWTBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
