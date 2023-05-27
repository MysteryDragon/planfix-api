# Planfix\TaskApi

All URIs are relative to *https://your-account.planfix.com/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getTaskById**](TaskApi.md#gettaskbyid) | **GET** /task/{id} | Get task by number
[**getTaskComments**](TaskApi.md#gettaskcomments) | **POST** /task/{id}/comments/list | Get task comments
[**getTaskList**](TaskApi.md#gettasklist) | **POST** /task/list | Get list of tasks
[**getTaskListTemplates**](TaskApi.md#gettasklisttemplates) | **GET** /task/templates | Get list of task templates
[**postTask**](TaskApi.md#posttask) | **POST** /task/ | Create task
[**postTaskAddComment**](TaskApi.md#posttaskaddcomment) | **POST** /task/{id}/comments/ | Add comment
[**postTaskAddDataTagEntryExistingComment**](TaskApi.md#posttaskadddatatagentryexistingcomment) | **POST** /task/{id}/datatags/{commentId} | Add a data tag entry to an existing comment
[**postTaskAddDataTagEntryNewComment**](TaskApi.md#posttaskadddatatagentrynewcomment) | **POST** /task/{id}/datatags/ | Add data tag entry as new comment
[**postTaskById**](TaskApi.md#posttaskbyid) | **POST** /task/{id} | Update task by number
[**postTaskFilters**](TaskApi.md#posttaskfilters) | **POST** /task/filters | Get list task filters
[**postTaskUpdateComment**](TaskApi.md#posttaskupdatecomment) | **POST** /task/{id}/comments/{commentId} | Updating comments

# **getTaskById**
> \Planfix\Model\InlineResponse2006 getTaskById($id, $fields, $sourceId)

Get task by number

This method lets you get a task by number

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\TaskApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 789; // int | Number of the requested task
$fields = "fields_example"; // string | Fields returned - custom field identifiers, system field names, comma-delimited
$sourceId = "sourceId_example"; // string | Unique identifier of external application

try {
    $result = $apiInstance->getTaskById($id, $fields, $sourceId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TaskApi->getTaskById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Number of the requested task |
 **fields** | **string**| Fields returned - custom field identifiers, system field names, comma-delimited | [optional]
 **sourceId** | **string**| Unique identifier of external application | [optional]

### Return type

[**\Planfix\Model\InlineResponse2006**](../Model/InlineResponse2006.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getTaskComments**
> \Planfix\Model\InlineResponse2002 getTaskComments($id, $body)

Get task comments

This method lets you get a list of comments on a task

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\TaskApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 789; // int | Number of the requested task
$body = new \Planfix\Model\CommentsListBody1(); // \Planfix\Model\CommentsListBody1 | 

try {
    $result = $apiInstance->getTaskComments($id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TaskApi->getTaskComments: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Number of the requested task |
 **body** | [**\Planfix\Model\CommentsListBody1**](../Model/CommentsListBody1.md)|  | [optional]

### Return type

[**\Planfix\Model\InlineResponse2002**](../Model/InlineResponse2002.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getTaskList**
> \Planfix\Model\InlineResponse2007 getTaskList($body)

Get list of tasks

This method lets you get a list of tasks

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\TaskApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Planfix\Model\TaskListBody(); // \Planfix\Model\TaskListBody | 

try {
    $result = $apiInstance->getTaskList($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TaskApi->getTaskList: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Planfix\Model\TaskListBody**](../Model/TaskListBody.md)|  | [optional]

### Return type

[**\Planfix\Model\InlineResponse2007**](../Model/InlineResponse2007.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getTaskListTemplates**
> \Planfix\Model\InlineResponse2008 getTaskListTemplates($offset, $pageSize, $sourceId, $fields)

Get list of task templates

This method lets you get a list of all task templates

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\TaskApi(
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
    $result = $apiInstance->getTaskListTemplates($offset, $pageSize, $sourceId, $fields);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TaskApi->getTaskListTemplates: ', $e->getMessage(), PHP_EOL;
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

[**\Planfix\Model\InlineResponse2008**](../Model/InlineResponse2008.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postTask**
> \Planfix\Model\InlineResponse201 postTask($body)

Create task

This method lets you create a new task

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\TaskApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Planfix\Model\TaskCreateRequest(); // \Planfix\Model\TaskCreateRequest | 

try {
    $result = $apiInstance->postTask($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TaskApi->postTask: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Planfix\Model\TaskCreateRequest**](../Model/TaskCreateRequest.md)|  | [optional]

### Return type

[**\Planfix\Model\InlineResponse201**](../Model/InlineResponse201.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postTaskAddComment**
> \Planfix\Model\InlineResponse201 postTaskAddComment($id, $body)

Add comment

This method lets you add a new comment to a task

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\TaskApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Number of task
$body = new \Planfix\Model\CommentCreateRequest(); // \Planfix\Model\CommentCreateRequest | 

try {
    $result = $apiInstance->postTaskAddComment($id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TaskApi->postTaskAddComment: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Number of task |
 **body** | [**\Planfix\Model\CommentCreateRequest**](../Model/CommentCreateRequest.md)|  | [optional]

### Return type

[**\Planfix\Model\InlineResponse201**](../Model/InlineResponse201.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postTaskAddDataTagEntryExistingComment**
> \Planfix\Model\InlineResponse2014 postTaskAddDataTagEntryExistingComment($id, $commentId, $body)

Add a data tag entry to an existing comment

This method lets you add a data tag entry to an existing comment

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\TaskApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Number of task
$commentId = 56; // int | Number of comment
$body = new \Planfix\Model\DataTagEntryCreateRequest(); // \Planfix\Model\DataTagEntryCreateRequest | 

try {
    $result = $apiInstance->postTaskAddDataTagEntryExistingComment($id, $commentId, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TaskApi->postTaskAddDataTagEntryExistingComment: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Number of task |
 **commentId** | **int**| Number of comment |
 **body** | [**\Planfix\Model\DataTagEntryCreateRequest**](../Model/DataTagEntryCreateRequest.md)|  | [optional]

### Return type

[**\Planfix\Model\InlineResponse2014**](../Model/InlineResponse2014.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postTaskAddDataTagEntryNewComment**
> \Planfix\Model\InlineResponse2013 postTaskAddDataTagEntryNewComment($id, $body)

Add data tag entry as new comment

This method lets you add data tag entry as new comment

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\TaskApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Number of task
$body = new \Planfix\Model\DataTagEntryCreateRequest(); // \Planfix\Model\DataTagEntryCreateRequest | 

try {
    $result = $apiInstance->postTaskAddDataTagEntryNewComment($id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TaskApi->postTaskAddDataTagEntryNewComment: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Number of task |
 **body** | [**\Planfix\Model\DataTagEntryCreateRequest**](../Model/DataTagEntryCreateRequest.md)|  | [optional]

### Return type

[**\Planfix\Model\InlineResponse2013**](../Model/InlineResponse2013.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postTaskById**
> postTaskById($id, $body)

Update task by number

This method lets you update a task by number

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\TaskApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 789; // int | Number of task
$body = new \Planfix\Model\TaskUpdateRequest(); // \Planfix\Model\TaskUpdateRequest | 

try {
    $apiInstance->postTaskById($id, $body);
} catch (Exception $e) {
    echo 'Exception when calling TaskApi->postTaskById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Number of task |
 **body** | [**\Planfix\Model\TaskUpdateRequest**](../Model/TaskUpdateRequest.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postTaskFilters**
> \Planfix\Model\InlineResponse2005 postTaskFilters()

Get list task filters

This method lets you get list task filters

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\TaskApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->postTaskFilters();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TaskApi->postTaskFilters: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Planfix\Model\InlineResponse2005**](../Model/InlineResponse2005.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postTaskUpdateComment**
> postTaskUpdateComment($id, $commentId, $body)

Updating comments

This method lets you update a comment

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\TaskApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Number of task
$commentId = 56; // int | Number of comment
$body = new \Planfix\Model\CommentUpdateRequest(); // \Planfix\Model\CommentUpdateRequest | 

try {
    $apiInstance->postTaskUpdateComment($id, $commentId, $body);
} catch (Exception $e) {
    echo 'Exception when calling TaskApi->postTaskUpdateComment: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Number of task |
 **commentId** | **int**| Number of comment |
 **body** | [**\Planfix\Model\CommentUpdateRequest**](../Model/CommentUpdateRequest.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

