# ArtifactsMmo\TokenApi



All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**generateTokenTokenPost()**](TokenApi.md#generateTokenTokenPost) | **POST** /token | Generate Token |


## `generateTokenTokenPost()`

```php
generateTokenTokenPost(): \ArtifactsMmo\Model\TokenResponseSchema
```

Generate Token

Use your account as HTTPBasic Auth to generate your token to use the API. You can also generate your token directly on the website.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasic
$config = ArtifactsMmo\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new ArtifactsMmo\Api\TokenApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->generateTokenTokenPost();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TokenApi->generateTokenTokenPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\ArtifactsMmo\Model\TokenResponseSchema**](../Model/TokenResponseSchema.md)

### Authorization

[HTTPBasic](../../README.md#HTTPBasic)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
