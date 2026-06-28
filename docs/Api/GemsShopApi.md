# ArtifactsMmo\GemsShopApi



All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**buyCustomDesignGemsShopBuyCustomDesignPost()**](GemsShopApi.md#buyCustomDesignGemsShopBuyCustomDesignPost) | **POST** /gems_shop/buy_custom_design | Buy Custom Design |
| [**buySkinGemsShopSkinPost()**](GemsShopApi.md#buySkinGemsShopSkinPost) | **POST** /gems_shop/skin | Buy Skin |
| [**buySpawnEventGemsShopSpawnEventPost()**](GemsShopApi.md#buySpawnEventGemsShopSpawnEventPost) | **POST** /gems_shop/spawn_event | Buy Spawn Event |
| [**buySubscriptionGemsShopSubscriptionPost()**](GemsShopApi.md#buySubscriptionGemsShopSubscriptionPost) | **POST** /gems_shop/subscription | Buy Subscription |
| [**getCatalogGemsShopGet()**](GemsShopApi.md#getCatalogGemsShopGet) | **GET** /gems_shop/ | Get Catalog |


## `buyCustomDesignGemsShopBuyCustomDesignPost()`

```php
buyCustomDesignGemsShopBuyCustomDesignPost($buyCustomDesignRequestSchema): \ArtifactsMmo\Model\GemShopCustomDesignPurchaseResponseSchema
```

Buy Custom Design

Buy a custom design using gems.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: JWTBearer
$config = ArtifactsMmo\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new ArtifactsMmo\Api\GemsShopApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$buyCustomDesignRequestSchema = new \ArtifactsMmo\Model\BuyCustomDesignRequestSchema(); // \ArtifactsMmo\Model\BuyCustomDesignRequestSchema

try {
    $result = $apiInstance->buyCustomDesignGemsShopBuyCustomDesignPost($buyCustomDesignRequestSchema);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GemsShopApi->buyCustomDesignGemsShopBuyCustomDesignPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **buyCustomDesignRequestSchema** | [**\ArtifactsMmo\Model\BuyCustomDesignRequestSchema**](../Model/BuyCustomDesignRequestSchema.md)|  | |

### Return type

[**\ArtifactsMmo\Model\GemShopCustomDesignPurchaseResponseSchema**](../Model/GemShopCustomDesignPurchaseResponseSchema.md)

### Authorization

[JWTBearer](../../README.md#JWTBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `buySkinGemsShopSkinPost()`

```php
buySkinGemsShopSkinPost($buySkinRequestSchema): \ArtifactsMmo\Model\BuySkinResponseSchema
```

Buy Skin

Buy a skin from the gems shop using gems.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: JWTBearer
$config = ArtifactsMmo\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new ArtifactsMmo\Api\GemsShopApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$buySkinRequestSchema = new \ArtifactsMmo\Model\BuySkinRequestSchema(); // \ArtifactsMmo\Model\BuySkinRequestSchema

try {
    $result = $apiInstance->buySkinGemsShopSkinPost($buySkinRequestSchema);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GemsShopApi->buySkinGemsShopSkinPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **buySkinRequestSchema** | [**\ArtifactsMmo\Model\BuySkinRequestSchema**](../Model/BuySkinRequestSchema.md)|  | |

### Return type

[**\ArtifactsMmo\Model\BuySkinResponseSchema**](../Model/BuySkinResponseSchema.md)

### Authorization

[JWTBearer](../../README.md#JWTBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `buySpawnEventGemsShopSpawnEventPost()`

```php
buySpawnEventGemsShopSpawnEventPost($spawnEventRequestSchema): \ArtifactsMmo\Model\ActiveEventResponseSchema
```

Buy Spawn Event

Spawn an event from the gems shop using gems.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: JWTBearer
$config = ArtifactsMmo\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new ArtifactsMmo\Api\GemsShopApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$spawnEventRequestSchema = new \ArtifactsMmo\Model\SpawnEventRequestSchema(); // \ArtifactsMmo\Model\SpawnEventRequestSchema

try {
    $result = $apiInstance->buySpawnEventGemsShopSpawnEventPost($spawnEventRequestSchema);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GemsShopApi->buySpawnEventGemsShopSpawnEventPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **spawnEventRequestSchema** | [**\ArtifactsMmo\Model\SpawnEventRequestSchema**](../Model/SpawnEventRequestSchema.md)|  | |

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

## `buySubscriptionGemsShopSubscriptionPost()`

```php
buySubscriptionGemsShopSubscriptionPost(): \ArtifactsMmo\Model\GemShopSubscriptionResponseSchema
```

Buy Subscription

Buy or extend membership by 30 days using gems. Unavailable while a Stripe subscription is active.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: JWTBearer
$config = ArtifactsMmo\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new ArtifactsMmo\Api\GemsShopApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->buySubscriptionGemsShopSubscriptionPost();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GemsShopApi->buySubscriptionGemsShopSubscriptionPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\ArtifactsMmo\Model\GemShopSubscriptionResponseSchema**](../Model/GemShopSubscriptionResponseSchema.md)

### Authorization

[JWTBearer](../../README.md#JWTBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getCatalogGemsShopGet()`

```php
getCatalogGemsShopGet(): \ArtifactsMmo\Model\GemShopCatalogResponseSchema
```

Get Catalog

Return the gems shop catalog.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\GemsShopApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->getCatalogGemsShopGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GemsShopApi->getCatalogGemsShopGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\ArtifactsMmo\Model\GemShopCatalogResponseSchema**](../Model/GemShopCatalogResponseSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
