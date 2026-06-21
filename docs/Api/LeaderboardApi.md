# ArtifactsMmo\LeaderboardApi



All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getAccountsLeaderboardLeaderboardAccountsGet()**](LeaderboardApi.md#getAccountsLeaderboardLeaderboardAccountsGet) | **GET** /leaderboard/accounts | Get Accounts Leaderboard |
| [**getCharactersLeaderboardLeaderboardCharactersGet()**](LeaderboardApi.md#getCharactersLeaderboardLeaderboardCharactersGet) | **GET** /leaderboard/characters | Get Characters Leaderboard |


## `getAccountsLeaderboardLeaderboardAccountsGet()`

```php
getAccountsLeaderboardLeaderboardAccountsGet($sort, $name, $page, $size): \ArtifactsMmo\Model\DataPageAccountLeaderboardSchema
```

Get Accounts Leaderboard

Fetch leaderboard details.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\LeaderboardApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$sort = new \ArtifactsMmo\Model\\ArtifactsMmoModelAccountLeaderboardType(); // \ArtifactsMmoModelAccountLeaderboardType | Sort of account leaderboards.
$name = 'name_example'; // string | Account name.
$page = 1; // int | Page number
$size = 50; // int | Page size

try {
    $result = $apiInstance->getAccountsLeaderboardLeaderboardAccountsGet($sort, $name, $page, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LeaderboardApi->getAccountsLeaderboardLeaderboardAccountsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sort** | [**\ArtifactsMmoModelAccountLeaderboardType**](../Model/.md)| Sort of account leaderboards. | [optional] |
| **name** | **string**| Account name. | [optional] |
| **page** | **int**| Page number | [optional] [default to 1] |
| **size** | **int**| Page size | [optional] [default to 50] |

### Return type

[**\ArtifactsMmo\Model\DataPageAccountLeaderboardSchema**](../Model/DataPageAccountLeaderboardSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getCharactersLeaderboardLeaderboardCharactersGet()`

```php
getCharactersLeaderboardLeaderboardCharactersGet($sort, $name, $page, $size): \ArtifactsMmo\Model\DataPageCharacterLeaderboardSchema
```

Get Characters Leaderboard

Fetch leaderboard details.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\LeaderboardApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$sort = new \ArtifactsMmo\Model\\ArtifactsMmoModelCharacterLeaderboardType(); // \ArtifactsMmoModelCharacterLeaderboardType | Sort of character leaderboards.
$name = 'name_example'; // string | Character name.
$page = 1; // int | Page number
$size = 50; // int | Page size

try {
    $result = $apiInstance->getCharactersLeaderboardLeaderboardCharactersGet($sort, $name, $page, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LeaderboardApi->getCharactersLeaderboardLeaderboardCharactersGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sort** | [**\ArtifactsMmoModelCharacterLeaderboardType**](../Model/.md)| Sort of character leaderboards. | [optional] |
| **name** | **string**| Character name. | [optional] |
| **page** | **int**| Page number | [optional] [default to 1] |
| **size** | **int**| Page size | [optional] [default to 50] |

### Return type

[**\ArtifactsMmo\Model\DataPageCharacterLeaderboardSchema**](../Model/DataPageCharacterLeaderboardSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
