# Planfix\EmployeeApi

All URIs are relative to *https://your-account.planfix.com/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getUserId**](EmployeeApi.md#getuserid) | **GET** /user/{id} | Get employee by number
[**getUserList**](EmployeeApi.md#getuserlist) | **POST** /user/list | Get list of employees
[**getUserListGroups**](EmployeeApi.md#getuserlistgroups) | **GET** /user/groups | Get list of employee groups
[**getUserPosts**](EmployeeApi.md#getuserposts) | **GET** /user/posts | Get list of employee posts
[**postUser**](EmployeeApi.md#postuser) | **POST** /user/ | Create employee
[**postUserId**](EmployeeApi.md#postuserid) | **POST** /user/{id} | Update employee by number

# **getUserId**
> \Planfix\Model\InlineResponse20019 getUserId($id, $fields, $sourceId)

Get employee by number

This method lets you get an employee by number

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\EmployeeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Number of employee
$fields = "fields_example"; // string | Fields returned - custom field identifiers, system field names, comma-delimited
$sourceId = "sourceId_example"; // string | Unique identifier of external application

try {
    $result = $apiInstance->getUserId($id, $fields, $sourceId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmployeeApi->getUserId: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Number of employee |
 **fields** | **string**| Fields returned - custom field identifiers, system field names, comma-delimited | [optional]
 **sourceId** | **string**| Unique identifier of external application | [optional]

### Return type

[**\Planfix\Model\InlineResponse20019**](../Model/InlineResponse20019.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getUserList**
> \Planfix\Model\InlineResponse20020 getUserList($body)

Get list of employees

This method lets you get a list of employees

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\EmployeeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Planfix\Model\UserListBody(); // \Planfix\Model\UserListBody | 

try {
    $result = $apiInstance->getUserList($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmployeeApi->getUserList: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Planfix\Model\UserListBody**](../Model/UserListBody.md)|  | [optional]

### Return type

[**\Planfix\Model\InlineResponse20020**](../Model/InlineResponse20020.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getUserListGroups**
> \Planfix\Model\InlineResponse2004 getUserListGroups($fields)

Get list of employee groups

This method lets you get a list of employee groups

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\EmployeeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$fields = "fields_example"; // string | Fields returned - system field names, comma-delimited

try {
    $result = $apiInstance->getUserListGroups($fields);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmployeeApi->getUserListGroups: ', $e->getMessage(), PHP_EOL;
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

# **getUserPosts**
> \Planfix\Model\InlineResponse20021 getUserPosts($fields)

Get list of employee posts

This method lets you get a list of employee posts

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\EmployeeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$fields = "fields_example"; // string | Fields returned - system field names, comma-delimited

try {
    $result = $apiInstance->getUserPosts($fields);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmployeeApi->getUserPosts: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **fields** | **string**| Fields returned - system field names, comma-delimited | [optional]

### Return type

[**\Planfix\Model\InlineResponse20021**](../Model/InlineResponse20021.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postUser**
> \Planfix\Model\InlineResponse201 postUser($body)

Create employee

This method lets you create a new employee

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\EmployeeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Planfix\Model\UserRequest(); // \Planfix\Model\UserRequest | 

try {
    $result = $apiInstance->postUser($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmployeeApi->postUser: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Planfix\Model\UserRequest**](../Model/UserRequest.md)|  | [optional]

### Return type

[**\Planfix\Model\InlineResponse201**](../Model/InlineResponse201.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postUserId**
> postUserId($id, $body)

Update employee by number

This method lets you update an employee by number

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\EmployeeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Number of employee
$body = new \Planfix\Model\UserRequest(); // \Planfix\Model\UserRequest | 

try {
    $apiInstance->postUserId($id, $body);
} catch (Exception $e) {
    echo 'Exception when calling EmployeeApi->postUserId: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Number of employee |
 **body** | [**\Planfix\Model\UserRequest**](../Model/UserRequest.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

