# ArtifactsMmo\ServerDetailsApi



All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getServerDetailsGet()**](ServerDetailsApi.md#getServerDetailsGet) | **GET** / | Get Server Details |


## `getServerDetailsGet()`

```php
getServerDetailsGet(): \ArtifactsMmo\Model\StatusResponseSchema
```

Get Server Details

Return the status of the game server.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\ServerDetailsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->getServerDetailsGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ServerDetailsApi->getServerDetailsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\ArtifactsMmo\Model\StatusResponseSchema**](../Model/StatusResponseSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
