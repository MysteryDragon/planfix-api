# Planfix\CommentsApi

All URIs are relative to *https://your-account.planfix.com/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteCommentId**](CommentsApi.md#deletecommentid) | **DELETE** /comment/{id} | Delete comment
[**getCommentId**](CommentsApi.md#getcommentid) | **GET** /comment/{id} | Get comment by number

# **deleteCommentId**
> deleteCommentId($id)

Delete comment

This method lets you delete a comment by number

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\CommentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | 

try {
    $apiInstance->deleteCommentId($id);
} catch (Exception $e) {
    echo 'Exception when calling CommentsApi->deleteCommentId: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**|  |

### Return type

void (empty response body)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getCommentId**
> \Planfix\Model\InlineResponse2009 getCommentId($id, $fields, $sourceId)

Get comment by number

This method lets you get a comment by number

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\CommentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Number of comment
$fields = "fields_example"; // string | Fields returned - custom field identifiers, system field names, comma-delimited
$sourceId = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Unique identifier of external application

try {
    $result = $apiInstance->getCommentId($id, $fields, $sourceId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommentsApi->getCommentId: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Number of comment |
 **fields** | **string**| Fields returned - custom field identifiers, system field names, comma-delimited | [optional]
 **sourceId** | [**string**](../Model/.md)| Unique identifier of external application | [optional]

### Return type

[**\Planfix\Model\InlineResponse2009**](../Model/InlineResponse2009.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

