# Planfix\CustomFieldsApi

All URIs are relative to *https://your-account.planfix.com/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getCustomfieldContact**](CustomFieldsApi.md#getcustomfieldcontact) | **GET** /customfield/contact | Get a list of a custom contact fields
[**getCustomfieldGeneric**](CustomFieldsApi.md#getcustomfieldgeneric) | **GET** /customfield/main | Get list of custom main fields
[**getCustomfieldProject**](CustomFieldsApi.md#getcustomfieldproject) | **GET** /customfield/project | Get a list of custom project fields
[**getCustomfieldTask**](CustomFieldsApi.md#getcustomfieldtask) | **GET** /customfield/task | Get list of custom task fields
[**getCustomfieldUser**](CustomFieldsApi.md#getcustomfielduser) | **GET** /customfield/user | Get list of custom employee fields
[**getCustomfieldsForContact**](CustomFieldsApi.md#getcustomfieldsforcontact) | **GET** /customfield/contact/{id} | Get a list of a custom fields for contact
[**getCustomfieldsForDatatag**](CustomFieldsApi.md#getcustomfieldsfordatatag) | **GET** /customfield/datatag/{id} | Get list of custom fields for data tag
[**getCustomfieldsForDirectory**](CustomFieldsApi.md#getcustomfieldsfordirectory) | **GET** /customfield/directory/{id} | Get list of custom fields for directory
[**getCustomfieldsForProject**](CustomFieldsApi.md#getcustomfieldsforproject) | **GET** /customfield/project/{id} | Get list of custom fields for project
[**getCustomfieldsForTask**](CustomFieldsApi.md#getcustomfieldsfortask) | **GET** /customfield/task/{id} | Get list of custom fields for task
[**getCustomfieldsForUser**](CustomFieldsApi.md#getcustomfieldsforuser) | **GET** /customfield/user/{id} | Get list of custom fields for employee

# **getCustomfieldContact**
> \Planfix\Model\InlineResponse20026 getCustomfieldContact($fields)

Get a list of a custom contact fields

This method lets you get a list of custom contact and company fields

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\CustomFieldsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$fields = "fields_example"; // string | Fields returned - names, comma-delimited

try {
    $result = $apiInstance->getCustomfieldContact($fields);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomFieldsApi->getCustomfieldContact: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **fields** | **string**| Fields returned - names, comma-delimited | [optional]

### Return type

[**\Planfix\Model\InlineResponse20026**](../Model/InlineResponse20026.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getCustomfieldGeneric**
> \Planfix\Model\InlineResponse20026 getCustomfieldGeneric($fields)

Get list of custom main fields

This method lets you get a list of custom main fields

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\CustomFieldsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$fields = "fields_example"; // string | Fields returned - names, comma-delimited

try {
    $result = $apiInstance->getCustomfieldGeneric($fields);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomFieldsApi->getCustomfieldGeneric: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **fields** | **string**| Fields returned - names, comma-delimited | [optional]

### Return type

[**\Planfix\Model\InlineResponse20026**](../Model/InlineResponse20026.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getCustomfieldProject**
> \Planfix\Model\InlineResponse20026 getCustomfieldProject($fields)

Get a list of custom project fields

This method lets you get a list of custom project fields

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\CustomFieldsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$fields = "fields_example"; // string | Fields returned - custom field identifiers, system field names, comma-delimited

try {
    $result = $apiInstance->getCustomfieldProject($fields);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomFieldsApi->getCustomfieldProject: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **fields** | **string**| Fields returned - custom field identifiers, system field names, comma-delimited | [optional]

### Return type

[**\Planfix\Model\InlineResponse20026**](../Model/InlineResponse20026.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getCustomfieldTask**
> \Planfix\Model\InlineResponse20026 getCustomfieldTask($fields)

Get list of custom task fields

This method lets you get a list of custom task fields

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\CustomFieldsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$fields = "fields_example"; // string | Fields returned - names, comma-delimited

try {
    $result = $apiInstance->getCustomfieldTask($fields);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomFieldsApi->getCustomfieldTask: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **fields** | **string**| Fields returned - names, comma-delimited | [optional]

### Return type

[**\Planfix\Model\InlineResponse20026**](../Model/InlineResponse20026.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getCustomfieldUser**
> \Planfix\Model\InlineResponse20026 getCustomfieldUser($fields)

Get list of custom employee fields

This method lets you get a list of custom employee fields

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\CustomFieldsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$fields = "fields_example"; // string | Fields returned - names, comma-delimited

try {
    $result = $apiInstance->getCustomfieldUser($fields);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomFieldsApi->getCustomfieldUser: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **fields** | **string**| Fields returned - names, comma-delimited | [optional]

### Return type

[**\Planfix\Model\InlineResponse20026**](../Model/InlineResponse20026.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getCustomfieldsForContact**
> \Planfix\Model\InlineResponse20026 getCustomfieldsForContact($id, $fields)

Get a list of a custom fields for contact

This method lets you get a list of custom fields for contact or company

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\CustomFieldsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Number of contact
$fields = "fields_example"; // string | Fields returned - names, comma-delimited

try {
    $result = $apiInstance->getCustomfieldsForContact($id, $fields);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomFieldsApi->getCustomfieldsForContact: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Number of contact |
 **fields** | **string**| Fields returned - names, comma-delimited | [optional]

### Return type

[**\Planfix\Model\InlineResponse20026**](../Model/InlineResponse20026.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getCustomfieldsForDatatag**
> \Planfix\Model\InlineResponse20026 getCustomfieldsForDatatag($id, $fields)

Get list of custom fields for data tag

This method lets you get a list of custom fields for data tag

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\CustomFieldsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Data tag ID
$fields = "fields_example"; // string | Fields returned - names, comma-delimited

try {
    $result = $apiInstance->getCustomfieldsForDatatag($id, $fields);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomFieldsApi->getCustomfieldsForDatatag: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Data tag ID |
 **fields** | **string**| Fields returned - names, comma-delimited | [optional]

### Return type

[**\Planfix\Model\InlineResponse20026**](../Model/InlineResponse20026.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getCustomfieldsForDirectory**
> \Planfix\Model\InlineResponse20026 getCustomfieldsForDirectory($id, $fields)

Get list of custom fields for directory

This method lets you get a list of custom fields for directory

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\CustomFieldsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Directory ID
$fields = "fields_example"; // string | Fields returned - names, comma-delimited

try {
    $result = $apiInstance->getCustomfieldsForDirectory($id, $fields);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomFieldsApi->getCustomfieldsForDirectory: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Directory ID |
 **fields** | **string**| Fields returned - names, comma-delimited | [optional]

### Return type

[**\Planfix\Model\InlineResponse20026**](../Model/InlineResponse20026.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getCustomfieldsForProject**
> \Planfix\Model\InlineResponse20026 getCustomfieldsForProject($id, $fields)

Get list of custom fields for project

This method lets you get a list of custom fields for project

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\CustomFieldsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 789; // int | Number of task
$fields = "fields_example"; // string | Fields returned - names, comma-delimited

try {
    $result = $apiInstance->getCustomfieldsForProject($id, $fields);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomFieldsApi->getCustomfieldsForProject: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Number of task |
 **fields** | **string**| Fields returned - names, comma-delimited | [optional]

### Return type

[**\Planfix\Model\InlineResponse20026**](../Model/InlineResponse20026.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getCustomfieldsForTask**
> \Planfix\Model\InlineResponse20026 getCustomfieldsForTask($id, $fields)

Get list of custom fields for task

This method lets you get a list of custom fields for task

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\CustomFieldsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 789; // int | Number of task
$fields = "fields_example"; // string | Fields returned - names, comma-delimited

try {
    $result = $apiInstance->getCustomfieldsForTask($id, $fields);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomFieldsApi->getCustomfieldsForTask: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Number of task |
 **fields** | **string**| Fields returned - names, comma-delimited | [optional]

### Return type

[**\Planfix\Model\InlineResponse20026**](../Model/InlineResponse20026.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getCustomfieldsForUser**
> \Planfix\Model\InlineResponse20026 getCustomfieldsForUser($id, $fields)

Get list of custom fields for employee

This method lets you get a list of custom fields for employee

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\CustomFieldsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Number of employee
$fields = "fields_example"; // string | Fields returned - names, comma-delimited

try {
    $result = $apiInstance->getCustomfieldsForUser($id, $fields);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomFieldsApi->getCustomfieldsForUser: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Number of employee |
 **fields** | **string**| Fields returned - names, comma-delimited | [optional]

### Return type

[**\Planfix\Model\InlineResponse20026**](../Model/InlineResponse20026.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

