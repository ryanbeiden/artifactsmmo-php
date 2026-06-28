# ArtifactsMmo\GameAssistantApi



All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**askGameAssistantGameAssistantAskPost()**](GameAssistantApi.md#askGameAssistantGameAssistantAskPost) | **POST** /game_assistant/ask | Ask Game Assistant |


## `askGameAssistantGameAssistantAskPost()`

```php
askGameAssistantGameAssistantAskPost($assistantQuestionSchema): \ArtifactsMmo\Model\AssistantAnswerSchema
```

Ask Game Assistant

Ask the game assistant a question about game mechanics or public API usage. An active membership is required. Members receive a limited number of free questions per day. When no free question is available, the request can spend 1 gem with pay_with_gems=true.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: JWTBearer
$config = ArtifactsMmo\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new ArtifactsMmo\Api\GameAssistantApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$assistantQuestionSchema = new \ArtifactsMmo\Model\AssistantQuestionSchema(); // \ArtifactsMmo\Model\AssistantQuestionSchema

try {
    $result = $apiInstance->askGameAssistantGameAssistantAskPost($assistantQuestionSchema);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GameAssistantApi->askGameAssistantGameAssistantAskPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **assistantQuestionSchema** | [**\ArtifactsMmo\Model\AssistantQuestionSchema**](../Model/AssistantQuestionSchema.md)|  | |

### Return type

[**\ArtifactsMmo\Model\AssistantAnswerSchema**](../Model/AssistantAnswerSchema.md)

### Authorization

[JWTBearer](../../README.md#JWTBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
