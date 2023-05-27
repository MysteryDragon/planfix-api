# Planfix\DataTagsApi

All URIs are relative to *https://your-account.planfix.com/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteDatatagEntryKey**](DataTagsApi.md#deletedatatagentrykey) | **DELETE** /datatag/entry/{key} | Delete data tag entry
[**getDataTags**](DataTagsApi.md#getdatatags) | **POST** /datatag/list | Get data tags
[**getDatatagEntryKey**](DataTagsApi.md#getdatatagentrykey) | **GET** /datatag/entry/{key} | Get data tag entry
[**getDatatagId**](DataTagsApi.md#getdatatagid) | **GET** /datatag/{id} | Get data tag by identifier
[**postListDataTagEntrys**](DataTagsApi.md#postlistdatatagentrys) | **POST** /datatag/{id}/entry/list | Get list of data tag entries
[**postUpdateDataTagEntry**](DataTagsApi.md#postupdatedatatagentry) | **POST** /datatag/entry/{key} | Update data tag entry

# **deleteDatatagEntryKey**
> deleteDatatagEntryKey($key)

Delete data tag entry

This method lets you delete a data tag entry by key

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\DataTagsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$key = 56; // int | Key of the data tag entry

try {
    $apiInstance->deleteDatatagEntryKey($key);
} catch (Exception $e) {
    echo 'Exception when calling DataTagsApi->deleteDatatagEntryKey: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **key** | **int**| Key of the data tag entry |

### Return type

void (empty response body)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getDataTags**
> \Planfix\Model\InlineResponse20011 getDataTags($body)

Get data tags

This method lets you get a list of data tags

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\DataTagsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Planfix\Model\DatatagListBody(); // \Planfix\Model\DatatagListBody | 

try {
    $result = $apiInstance->getDataTags($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DataTagsApi->getDataTags: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Planfix\Model\DatatagListBody**](../Model/DatatagListBody.md)|  | [optional]

### Return type

[**\Planfix\Model\InlineResponse20011**](../Model/InlineResponse20011.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getDatatagEntryKey**
> \Planfix\Model\InlineResponse20012 getDatatagEntryKey($key, $fields)

Get data tag entry

This method lets you get a data tag entry by key

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\DataTagsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$key = 56; // int | Key of the data tag entry
$fields = "fields_example"; // string | Fields returned - custom field identifiers, system field names, comma-delimited

try {
    $result = $apiInstance->getDatatagEntryKey($key, $fields);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DataTagsApi->getDatatagEntryKey: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **key** | **int**| Key of the data tag entry |
 **fields** | **string**| Fields returned - custom field identifiers, system field names, comma-delimited | [optional]

### Return type

[**\Planfix\Model\InlineResponse20012**](../Model/InlineResponse20012.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getDatatagId**
> \Planfix\Model\InlineResponse20010 getDatatagId($id, $fields)

Get data tag by identifier

This method lets you get a data tag by its ID

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\DataTagsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Data tag ID
$fields = "fields_example"; // string | Fields returned - system field names, comma-delimited

try {
    $result = $apiInstance->getDatatagId($id, $fields);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DataTagsApi->getDatatagId: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Data tag ID |
 **fields** | **string**| Fields returned - system field names, comma-delimited | [optional]

### Return type

[**\Planfix\Model\InlineResponse20010**](../Model/InlineResponse20010.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postListDataTagEntrys**
> \Planfix\Model\InlineResponse20013 postListDataTagEntrys($id, $body)

Get list of data tag entries

This method lets you get a list of data tag entries

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\DataTagsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Identifier of requested data tag
$body = new \Planfix\Model\EntryListBody(); // \Planfix\Model\EntryListBody | 

try {
    $result = $apiInstance->postListDataTagEntrys($id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DataTagsApi->postListDataTagEntrys: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Identifier of requested data tag |
 **body** | [**\Planfix\Model\EntryListBody**](../Model/EntryListBody.md)|  | [optional]

### Return type

[**\Planfix\Model\InlineResponse20013**](../Model/InlineResponse20013.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postUpdateDataTagEntry**
> postUpdateDataTagEntry($key, $body)

Update data tag entry

This method lets you update a data tag entry

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\DataTagsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$key = 56; // int | Key of the data tag entry
$body = new \Planfix\Model\DataTagEntryUpdateRequest(); // \Planfix\Model\DataTagEntryUpdateRequest | 

try {
    $apiInstance->postUpdateDataTagEntry($key, $body);
} catch (Exception $e) {
    echo 'Exception when calling DataTagsApi->postUpdateDataTagEntry: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **key** | **int**| Key of the data tag entry |
 **body** | [**\Planfix\Model\DataTagEntryUpdateRequest**](../Model/DataTagEntryUpdateRequest.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

