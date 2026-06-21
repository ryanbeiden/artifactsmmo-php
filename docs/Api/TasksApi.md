# ArtifactsMmo\TasksApi



All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getAllTasksRewardsTasksRewardsGet()**](TasksApi.md#getAllTasksRewardsTasksRewardsGet) | **GET** /tasks/rewards | Get All Tasks Rewards |
| [**getAllTasksTasksListGet()**](TasksApi.md#getAllTasksTasksListGet) | **GET** /tasks/list | Get All Tasks |
| [**getTaskTasksListCodeGet()**](TasksApi.md#getTaskTasksListCodeGet) | **GET** /tasks/list/{code} | Get Task |
| [**getTasksRewardTasksRewardsCodeGet()**](TasksApi.md#getTasksRewardTasksRewardsCodeGet) | **GET** /tasks/rewards/{code} | Get Tasks Reward |


## `getAllTasksRewardsTasksRewardsGet()`

```php
getAllTasksRewardsTasksRewardsGet($page, $size): \ArtifactsMmo\Model\StaticDataPageDropRateSchema
```

Get All Tasks Rewards

Fetch the list of all tasks rewards. To obtain these rewards, you must exchange 6 task coins with a tasks master.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\TasksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$page = 1; // int | Page number
$size = 50; // int | Page size

try {
    $result = $apiInstance->getAllTasksRewardsTasksRewardsGet($page, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TasksApi->getAllTasksRewardsTasksRewardsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**| Page number | [optional] [default to 1] |
| **size** | **int**| Page size | [optional] [default to 50] |

### Return type

[**\ArtifactsMmo\Model\StaticDataPageDropRateSchema**](../Model/StaticDataPageDropRateSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAllTasksTasksListGet()`

```php
getAllTasksTasksListGet($minLevel, $maxLevel, $skill, $type, $page, $size): \ArtifactsMmo\Model\StaticDataPageTaskFullSchema
```

Get All Tasks

Fetch the list of all tasks.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\TasksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$minLevel = 56; // int | Minimum level.
$maxLevel = 56; // int | Maximum level.
$skill = new \ArtifactsMmo\Model\\ArtifactsMmoModelSkill(); // \ArtifactsMmoModelSkill | Skill of tasks.
$type = new \ArtifactsMmo\Model\\ArtifactsMmoModelTaskType(); // \ArtifactsMmoModelTaskType | Type of tasks.
$page = 1; // int | Page number
$size = 50; // int | Page size

try {
    $result = $apiInstance->getAllTasksTasksListGet($minLevel, $maxLevel, $skill, $type, $page, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TasksApi->getAllTasksTasksListGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **minLevel** | **int**| Minimum level. | [optional] |
| **maxLevel** | **int**| Maximum level. | [optional] |
| **skill** | [**\ArtifactsMmoModelSkill**](../Model/.md)| Skill of tasks. | [optional] |
| **type** | [**\ArtifactsMmoModelTaskType**](../Model/.md)| Type of tasks. | [optional] |
| **page** | **int**| Page number | [optional] [default to 1] |
| **size** | **int**| Page size | [optional] [default to 50] |

### Return type

[**\ArtifactsMmo\Model\StaticDataPageTaskFullSchema**](../Model/StaticDataPageTaskFullSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTaskTasksListCodeGet()`

```php
getTaskTasksListCodeGet($code): \ArtifactsMmo\Model\TaskFullResponseSchema
```

Get Task

Retrieve the details of a task.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\TasksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$code = 'code_example'; // string | The code of the task.

try {
    $result = $apiInstance->getTaskTasksListCodeGet($code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TasksApi->getTaskTasksListCodeGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**| The code of the task. | |

### Return type

[**\ArtifactsMmo\Model\TaskFullResponseSchema**](../Model/TaskFullResponseSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTasksRewardTasksRewardsCodeGet()`

```php
getTasksRewardTasksRewardsCodeGet($code): \ArtifactsMmo\Model\RewardResponseSchema
```

Get Tasks Reward

Retrieve the details of a tasks reward.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\TasksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$code = 'code_example'; // string | The code of the tasks reward.

try {
    $result = $apiInstance->getTasksRewardTasksRewardsCodeGet($code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TasksApi->getTasksRewardTasksRewardsCodeGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**| The code of the tasks reward. | |

### Return type

[**\ArtifactsMmo\Model\RewardResponseSchema**](../Model/RewardResponseSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
