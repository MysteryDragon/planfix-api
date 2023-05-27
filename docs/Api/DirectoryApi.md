# Planfix\DirectoryApi

All URIs are relative to *https://your-account.planfix.com/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteDirectoryEntryKey**](DirectoryApi.md#deletedirectoryentrykey) | **DELETE** /directory/{id}/entry/{key} | Delete directory entry
[**getDirectoriesGroups**](DirectoryApi.md#getdirectoriesgroups) | **GET** /directory/groups | Get list of directory groups
[**getDirectoryById**](DirectoryApi.md#getdirectorybyid) | **GET** /directory/{id} | Get directory by identifier
[**getDirectoryIdEntryKey**](DirectoryApi.md#getdirectoryidentrykey) | **GET** /directory/{id}/entry/{key} | Get directory entry
[**getListDirectories**](DirectoryApi.md#getlistdirectories) | **POST** /directory/list | Get list of directories
[**postAddDirectoryEntry**](DirectoryApi.md#postadddirectoryentry) | **POST** /directory/{id}/entry/ | Add directory entry
[**postListDirectoryEntries**](DirectoryApi.md#postlistdirectoryentries) | **POST** /directory/{id}/entry/list | Get list of directory entries
[**postUpdateDirectoryEntry**](DirectoryApi.md#postupdatedirectoryentry) | **POST** /directory/{id}/entry/{key} | Update directory entry

# **deleteDirectoryEntryKey**
> deleteDirectoryEntryKey($key, $id)

Delete directory entry

This method lets you delete a directory entry by key

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\DirectoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$key = 56; // int | Key of the directory entry
$id = "id_example"; // string | Directory ID

try {
    $apiInstance->deleteDirectoryEntryKey($key, $id);
} catch (Exception $e) {
    echo 'Exception when calling DirectoryApi->deleteDirectoryEntryKey: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **key** | **int**| Key of the directory entry |
 **id** | **string**| Directory ID |

### Return type

void (empty response body)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getDirectoriesGroups**
> \Planfix\Model\InlineResponse2004 getDirectoriesGroups($fields)

Get list of directory groups

This method lets you get a list of directory groups

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\DirectoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$fields = "fields_example"; // string | Fields returned - system field names, comma-delimited

try {
    $result = $apiInstance->getDirectoriesGroups($fields);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DirectoryApi->getDirectoriesGroups: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **fields** | **string**| Fields returned - system field names, comma-delimited | [optional]

### Return type

[**\Planfix\Model\InlineResponse2004**](../Model/InlineResponse2004.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getDirectoryById**
> \Planfix\Model\InlineResponse20022 getDirectoryById($id, $fields)

Get directory by identifier

This method lets you get a directory from its ID

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\DirectoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Directory ID
$fields = "fields_example"; // string | Fields returned - system field names, comma-delimited

try {
    $result = $apiInstance->getDirectoryById($id, $fields);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DirectoryApi->getDirectoryById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Directory ID |
 **fields** | **string**| Fields returned - system field names, comma-delimited | [optional]

### Return type

[**\Planfix\Model\InlineResponse20022**](../Model/InlineResponse20022.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getDirectoryIdEntryKey**
> \Planfix\Model\InlineResponse20024 getDirectoryIdEntryKey($key, $id, $fields)

Get directory entry

This method lets you geta directory entry by its key

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\DirectoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$key = 56; // int | Key of the directory entry
$id = "id_example"; // string | Directory ID
$fields = "fields_example"; // string | Fields returned - custom field identifiers, system field names, comma-delimited

try {
    $result = $apiInstance->getDirectoryIdEntryKey($key, $id, $fields);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DirectoryApi->getDirectoryIdEntryKey: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **key** | **int**| Key of the directory entry |
 **id** | **string**| Directory ID |
 **fields** | **string**| Fields returned - custom field identifiers, system field names, comma-delimited | [optional]

### Return type

[**\Planfix\Model\InlineResponse20024**](../Model/InlineResponse20024.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getListDirectories**
> \Planfix\Model\InlineResponse20023 getListDirectories($body)

Get list of directories

This method lets you get a list of directories

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\DirectoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Planfix\Model\DirectoryListBody(); // \Planfix\Model\DirectoryListBody | 

try {
    $result = $apiInstance->getListDirectories($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DirectoryApi->getListDirectories: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Planfix\Model\DirectoryListBody**](../Model/DirectoryListBody.md)|  | [optional]

### Return type

[**\Planfix\Model\InlineResponse20023**](../Model/InlineResponse20023.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postAddDirectoryEntry**
> postAddDirectoryEntry($id, $body)

Add directory entry

This method lets you add a directory entry

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\DirectoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Directory ID
$body = new \Planfix\Model\DirectoryEntryRequest(); // \Planfix\Model\DirectoryEntryRequest | 

try {
    $apiInstance->postAddDirectoryEntry($id, $body);
} catch (Exception $e) {
    echo 'Exception when calling DirectoryApi->postAddDirectoryEntry: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Directory ID |
 **body** | [**\Planfix\Model\DirectoryEntryRequest**](../Model/DirectoryEntryRequest.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postListDirectoryEntries**
> \Planfix\Model\InlineResponse20025 postListDirectoryEntries($id, $body)

Get list of directory entries

This method lets you to get a list of directory entries

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\DirectoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Directory ID
$body = new \Planfix\Model\EntryListBody1(); // \Planfix\Model\EntryListBody1 | 

try {
    $result = $apiInstance->postListDirectoryEntries($id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DirectoryApi->postListDirectoryEntries: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Directory ID |
 **body** | [**\Planfix\Model\EntryListBody1**](../Model/EntryListBody1.md)|  | [optional]

### Return type

[**\Planfix\Model\InlineResponse20025**](../Model/InlineResponse20025.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postUpdateDirectoryEntry**
> postUpdateDirectoryEntry($key, $id, $body)

Update directory entry

This method lets you update a directory entry

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\DirectoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$key = 56; // int | Key of the directory entry
$id = "id_example"; // string | Directory ID
$body = new \Planfix\Model\DirectoryEntryRequest(); // \Planfix\Model\DirectoryEntryRequest | 

try {
    $apiInstance->postUpdateDirectoryEntry($key, $id, $body);
} catch (Exception $e) {
    echo 'Exception when calling DirectoryApi->postUpdateDirectoryEntry: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **key** | **int**| Key of the directory entry |
 **id** | **string**| Directory ID |
 **body** | [**\Planfix\Model\DirectoryEntryRequest**](../Model/DirectoryEntryRequest.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

