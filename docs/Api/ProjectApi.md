# Planfix\ProjectApi

All URIs are relative to *https://your-account.planfix.com/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getProjectById**](ProjectApi.md#getprojectbyid) | **GET** /project/{id} | Get project by number
[**getProjectList**](ProjectApi.md#getprojectlist) | **POST** /project/list | Get list of projects
[**getProjectListTemplates**](ProjectApi.md#getprojectlisttemplates) | **GET** /project /templates | Get list of project templates
[**getUserListGroups**](ProjectApi.md#getuserlistgroups) | **GET** /project/groups | Get list of project groups
[**postProject**](ProjectApi.md#postproject) | **POST** /project/ | Create project
[**postProjectById**](ProjectApi.md#postprojectbyid) | **POST** /project/{id} | Update project by number

# **getProjectById**
> \Planfix\Model\InlineResponse20016 getProjectById($id, $fields, $sourceId)

Get project by number

This method lets you get a project by number

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\ProjectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 789; // int | Number of the requested project
$fields = "fields_example"; // string | Fields returned - custom field identifiers, system field names, comma-delimited
$sourceId = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Unique identifier of external application

try {
    $result = $apiInstance->getProjectById($id, $fields, $sourceId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectApi->getProjectById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Number of the requested project |
 **fields** | **string**| Fields returned - custom field identifiers, system field names, comma-delimited | [optional]
 **sourceId** | [**string**](../Model/.md)| Unique identifier of external application | [optional]

### Return type

[**\Planfix\Model\InlineResponse20016**](../Model/InlineResponse20016.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getProjectList**
> \Planfix\Model\InlineResponse20017 getProjectList($body)

Get list of projects

This method lets you get a list of projects

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\ProjectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Planfix\Model\ProjectListBody(); // \Planfix\Model\ProjectListBody | 

try {
    $result = $apiInstance->getProjectList($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectApi->getProjectList: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Planfix\Model\ProjectListBody**](../Model/ProjectListBody.md)|  | [optional]

### Return type

[**\Planfix\Model\InlineResponse20017**](../Model/InlineResponse20017.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getProjectListTemplates**
> \Planfix\Model\InlineResponse20018 getProjectListTemplates($offset, $pageSize, $sourceId, $fields)

Get list of project templates

This method lets you get a list of all project templates

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\ProjectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$offset = 0; // float | Offset from beginning of list
$pageSize = 100; // float | Size of requested list
$sourceId = "sourceId_example"; // string | Unique identifier of external application
$fields = "fields_example"; // string | Fields returned - custom field identifiers, system field names, comma-delimited

try {
    $result = $apiInstance->getProjectListTemplates($offset, $pageSize, $sourceId, $fields);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectApi->getProjectListTemplates: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **offset** | **float**| Offset from beginning of list | [optional] [default to 0]
 **pageSize** | **float**| Size of requested list | [optional] [default to 100]
 **sourceId** | **string**| Unique identifier of external application | [optional]
 **fields** | **string**| Fields returned - custom field identifiers, system field names, comma-delimited | [optional]

### Return type

[**\Planfix\Model\InlineResponse20018**](../Model/InlineResponse20018.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getUserListGroups**
> \Planfix\Model\InlineResponse2004 getUserListGroups($fields)

Get list of project groups

This method lets you get a list of project groups

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\ProjectApi(
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
    echo 'Exception when calling ProjectApi->getUserListGroups: ', $e->getMessage(), PHP_EOL;
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

# **postProject**
> \Planfix\Model\InlineResponse201 postProject($body)

Create project

This method lets you create a new project

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\ProjectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Planfix\Model\ProjectRequest(); // \Planfix\Model\ProjectRequest | 

try {
    $result = $apiInstance->postProject($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectApi->postProject: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Planfix\Model\ProjectRequest**](../Model/ProjectRequest.md)|  | [optional]

### Return type

[**\Planfix\Model\InlineResponse201**](../Model/InlineResponse201.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postProjectById**
> postProjectById($id, $body)

Update project by number

This method lets you update the project data by number

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\ProjectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Number of project
$body = new \Planfix\Model\ProjectRequest(); // \Planfix\Model\ProjectRequest | 

try {
    $apiInstance->postProjectById($id, $body);
} catch (Exception $e) {
    echo 'Exception when calling ProjectApi->postProjectById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Number of project |
 **body** | [**\Planfix\Model\ProjectRequest**](../Model/ProjectRequest.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

