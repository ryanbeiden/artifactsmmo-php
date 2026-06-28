# ArtifactsMmo\CharactersApi



All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createCharacterCharactersCreatePost()**](CharactersApi.md#createCharacterCharactersCreatePost) | **POST** /characters/create | Create Character |
| [**deleteCharacterCharactersDeletePost()**](CharactersApi.md#deleteCharacterCharactersDeletePost) | **POST** /characters/delete | Delete Character |
| [**getActiveCharactersCharactersActiveGet()**](CharactersApi.md#getActiveCharactersCharactersActiveGet) | **GET** /characters/active | Get Active Characters |
| [**getCharacterCharactersNameGet()**](CharactersApi.md#getCharacterCharactersNameGet) | **GET** /characters/{name} | Get Character |
| [**getCharacterStatsCharactersNameStatsGet()**](CharactersApi.md#getCharacterStatsCharactersNameStatsGet) | **GET** /characters/{name}/stats | Get Character Stats |


## `createCharacterCharactersCreatePost()`

```php
createCharacterCharactersCreatePost($addCharacterSchema): \ArtifactsMmo\Model\CharacterResponseSchema
```

Create Character

Create new character on your account. You can create up to 5 characters.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: JWTBearer
$config = ArtifactsMmo\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new ArtifactsMmo\Api\CharactersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$addCharacterSchema = new \ArtifactsMmo\Model\AddCharacterSchema(); // \ArtifactsMmo\Model\AddCharacterSchema

try {
    $result = $apiInstance->createCharacterCharactersCreatePost($addCharacterSchema);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CharactersApi->createCharacterCharactersCreatePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **addCharacterSchema** | [**\ArtifactsMmo\Model\AddCharacterSchema**](../Model/AddCharacterSchema.md)|  | |

### Return type

[**\ArtifactsMmo\Model\CharacterResponseSchema**](../Model/CharacterResponseSchema.md)

### Authorization

[JWTBearer](../../README.md#JWTBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteCharacterCharactersDeletePost()`

```php
deleteCharacterCharactersDeletePost($deleteCharacterSchema): \ArtifactsMmo\Model\CharacterResponseSchema
```

Delete Character

Delete character on your account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: JWTBearer
$config = ArtifactsMmo\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new ArtifactsMmo\Api\CharactersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$deleteCharacterSchema = new \ArtifactsMmo\Model\DeleteCharacterSchema(); // \ArtifactsMmo\Model\DeleteCharacterSchema

try {
    $result = $apiInstance->deleteCharacterCharactersDeletePost($deleteCharacterSchema);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CharactersApi->deleteCharacterCharactersDeletePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **deleteCharacterSchema** | [**\ArtifactsMmo\Model\DeleteCharacterSchema**](../Model/DeleteCharacterSchema.md)|  | |

### Return type

[**\ArtifactsMmo\Model\CharacterResponseSchema**](../Model/CharacterResponseSchema.md)

### Authorization

[JWTBearer](../../README.md#JWTBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getActiveCharactersCharactersActiveGet()`

```php
getActiveCharactersCharactersActiveGet($page, $size): \ArtifactsMmo\Model\DataPageActiveCharacterSchema
```

Get Active Characters

Fetch active characters details.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\CharactersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$page = 1; // int | Page number
$size = 50; // int | Page size

try {
    $result = $apiInstance->getActiveCharactersCharactersActiveGet($page, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CharactersApi->getActiveCharactersCharactersActiveGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**| Page number | [optional] [default to 1] |
| **size** | **int**| Page size | [optional] [default to 50] |

### Return type

[**\ArtifactsMmo\Model\DataPageActiveCharacterSchema**](../Model/DataPageActiveCharacterSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getCharacterCharactersNameGet()`

```php
getCharacterCharactersNameGet($name): \ArtifactsMmo\Model\CharacterResponseSchema
```

Get Character

Retrieve the details of a character.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\CharactersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$name = 'name_example'; // string | The name of the character.

try {
    $result = $apiInstance->getCharacterCharactersNameGet($name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CharactersApi->getCharacterCharactersNameGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **name** | **string**| The name of the character. | |

### Return type

[**\ArtifactsMmo\Model\CharacterResponseSchema**](../Model/CharacterResponseSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getCharacterStatsCharactersNameStatsGet()`

```php
getCharacterStatsCharactersNameStatsGet($name): \ArtifactsMmo\Model\CharacterStatsResponseSchema
```

Get Character Stats

Retrieve gameplay statistics for a character.  Stats are only visible if the character's account has an active subscription. Statistics are still collected for all accounts regardless of subscription status.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\CharactersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$name = 'name_example'; // string | The name of the character.

try {
    $result = $apiInstance->getCharacterStatsCharactersNameStatsGet($name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CharactersApi->getCharacterStatsCharactersNameStatsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **name** | **string**| The name of the character. | |

### Return type

[**\ArtifactsMmo\Model\CharacterStatsResponseSchema**](../Model/CharacterStatsResponseSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
