# Planfix\ContactApi

All URIs are relative to *https://your-account.planfix.com/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getContactById**](ContactApi.md#getcontactbyid) | **GET** /contact/{id} | Get contact by number
[**getContactComments**](ContactApi.md#getcontactcomments) | **POST** /contact/{id}/comments/list | Get list of comments added to contact
[**getContactList**](ContactApi.md#getcontactlist) | **POST** /contact/list | Get list of contacts and companies
[**getContactListGroups**](ContactApi.md#getcontactlistgroups) | **GET** /contact/groups | Get list of contact groups
[**getContactListTemplates**](ContactApi.md#getcontactlisttemplates) | **GET** /contact/templates | Get list of contact or company templates
[**postContact**](ContactApi.md#postcontact) | **POST** /contact/ | Create contact or company
[**postContactAddComment**](ContactApi.md#postcontactaddcomment) | **POST** /contact/{id}/comments/ | Add comment
[**postContactAddDataTagEntryExistingComment**](ContactApi.md#postcontactadddatatagentryexistingcomment) | **POST** /contact/{id}/datatags/{commentId} | Add a data tag entry to an existing comment
[**postContactAddDataTagEntryNewComment**](ContactApi.md#postcontactadddatatagentrynewcomment) | **POST** /contact/{id}/datatags/ | Add a data tag entry with a new comment
[**postContactById**](ContactApi.md#postcontactbyid) | **POST** /contact/{id} | Update contact by number
[**postContactFilters**](ContactApi.md#postcontactfilters) | **POST** /contact/filters | Get list contact filters
[**postContactImport**](ContactApi.md#postcontactimport) | **POST** /contact/import | Import contact list
[**postContactUpdateComment**](ContactApi.md#postcontactupdatecomment) | **POST** /contact/{id}/comments/{commentId} | Update comment

# **getContactById**
> \Planfix\Model\InlineResponse200 getContactById($id, $fields, $sourceId)

Get contact by number

This method lets you get a contact or company by number

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\ContactApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Number of contact
$fields = "fields_example"; // string | Fields returned - custom field identifiers, system field names, comma-delimited
$sourceId = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Unique identifier of external application

try {
    $result = $apiInstance->getContactById($id, $fields, $sourceId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactApi->getContactById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Number of contact |
 **fields** | **string**| Fields returned - custom field identifiers, system field names, comma-delimited | [optional]
 **sourceId** | [**string**](../Model/.md)| Unique identifier of external application | [optional]

### Return type

[**\Planfix\Model\InlineResponse200**](../Model/InlineResponse200.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getContactComments**
> \Planfix\Model\InlineResponse2002 getContactComments($id, $body)

Get list of comments added to contact

This method lets you get a list of comments added to a contact

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\ContactApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Number of contact
$body = new \Planfix\Model\CommentsListBody(); // \Planfix\Model\CommentsListBody | 

try {
    $result = $apiInstance->getContactComments($id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactApi->getContactComments: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Number of contact |
 **body** | [**\Planfix\Model\CommentsListBody**](../Model/CommentsListBody.md)|  | [optional]

### Return type

[**\Planfix\Model\InlineResponse2002**](../Model/InlineResponse2002.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getContactList**
> \Planfix\Model\InlineResponse2001 getContactList($body)

Get list of contacts and companies

This method lets you get a list of contacts and companies

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\ContactApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Planfix\Model\ContactListBody(); // \Planfix\Model\ContactListBody | 

try {
    $result = $apiInstance->getContactList($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactApi->getContactList: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Planfix\Model\ContactListBody**](../Model/ContactListBody.md)|  | [optional]

### Return type

[**\Planfix\Model\InlineResponse2001**](../Model/InlineResponse2001.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getContactListGroups**
> \Planfix\Model\InlineResponse2004 getContactListGroups($fields)

Get list of contact groups

This method lets you get a list of all company groups

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\ContactApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$fields = "fields_example"; // string | Fields returned - system field names, comma-delimited

try {
    $result = $apiInstance->getContactListGroups($fields);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactApi->getContactListGroups: ', $e->getMessage(), PHP_EOL;
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

# **getContactListTemplates**
> \Planfix\Model\InlineResponse2003 getContactListTemplates($offset, $pageSize, $isCompany, $sourceId, $fields)

Get list of contact or company templates

This method lets you get a list of all contact or company templates

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\ContactApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$offset = 0; // float | Offset from beginning of list
$pageSize = 100; // float | Size of requested list
$isCompany = false; // bool | True for companies / false for contacts
$sourceId = "sourceId_example"; // string | Unique identifier of external application
$fields = "fields_example"; // string | Fields returned - custom field identifiers, system field names, comma-delimited

try {
    $result = $apiInstance->getContactListTemplates($offset, $pageSize, $isCompany, $sourceId, $fields);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactApi->getContactListTemplates: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **offset** | **float**| Offset from beginning of list | [optional] [default to 0]
 **pageSize** | **float**| Size of requested list | [optional] [default to 100]
 **isCompany** | **bool**| True for companies / false for contacts | [optional] [default to false]
 **sourceId** | **string**| Unique identifier of external application | [optional]
 **fields** | **string**| Fields returned - custom field identifiers, system field names, comma-delimited | [optional]

### Return type

[**\Planfix\Model\InlineResponse2003**](../Model/InlineResponse2003.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postContact**
> \Planfix\Model\InlineResponse201 postContact($body)

Create contact or company

This method lets you create a new contact or company

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\ContactApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Planfix\Model\ContactRequest(); // \Planfix\Model\ContactRequest | 

try {
    $result = $apiInstance->postContact($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactApi->postContact: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Planfix\Model\ContactRequest**](../Model/ContactRequest.md)|  | [optional]

### Return type

[**\Planfix\Model\InlineResponse201**](../Model/InlineResponse201.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postContactAddComment**
> \Planfix\Model\InlineResponse201 postContactAddComment($id, $body)

Add comment

This method lets you add a new comment to a contact

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\ContactApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Number of contact
$body = new \Planfix\Model\CommentCreateRequest(); // \Planfix\Model\CommentCreateRequest | 

try {
    $result = $apiInstance->postContactAddComment($id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactApi->postContactAddComment: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Number of contact |
 **body** | [**\Planfix\Model\CommentCreateRequest**](../Model/CommentCreateRequest.md)|  | [optional]

### Return type

[**\Planfix\Model\InlineResponse201**](../Model/InlineResponse201.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postContactAddDataTagEntryExistingComment**
> \Planfix\Model\InlineResponse2012 postContactAddDataTagEntryExistingComment($id, $commentId, $body)

Add a data tag entry to an existing comment

This method lets you add a data tag entry to an existing comment

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\ContactApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Number of contact
$commentId = 56; // int | Number of comment
$body = new \Planfix\Model\DataTagEntryCreateRequest(); // \Planfix\Model\DataTagEntryCreateRequest | 

try {
    $result = $apiInstance->postContactAddDataTagEntryExistingComment($id, $commentId, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactApi->postContactAddDataTagEntryExistingComment: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Number of contact |
 **commentId** | **int**| Number of comment |
 **body** | [**\Planfix\Model\DataTagEntryCreateRequest**](../Model/DataTagEntryCreateRequest.md)|  | [optional]

### Return type

[**\Planfix\Model\InlineResponse2012**](../Model/InlineResponse2012.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postContactAddDataTagEntryNewComment**
> \Planfix\Model\InlineResponse2011 postContactAddDataTagEntryNewComment($id, $body)

Add a data tag entry with a new comment

This method lets you add a data tag entry with a new comment

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\ContactApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Number of contact
$body = new \Planfix\Model\DataTagEntryCreateRequest(); // \Planfix\Model\DataTagEntryCreateRequest | 

try {
    $result = $apiInstance->postContactAddDataTagEntryNewComment($id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactApi->postContactAddDataTagEntryNewComment: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Number of contact |
 **body** | [**\Planfix\Model\DataTagEntryCreateRequest**](../Model/DataTagEntryCreateRequest.md)|  | [optional]

### Return type

[**\Planfix\Model\InlineResponse2011**](../Model/InlineResponse2011.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postContactById**
> postContactById($id, $body)

Update contact by number

This method lets you update a contact or company by number

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\ContactApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Number of contact
$body = new \Planfix\Model\ContactRequest(); // \Planfix\Model\ContactRequest | Successful operation

try {
    $apiInstance->postContactById($id, $body);
} catch (Exception $e) {
    echo 'Exception when calling ContactApi->postContactById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Number of contact |
 **body** | [**\Planfix\Model\ContactRequest**](../Model/ContactRequest.md)| Successful operation | [optional]

### Return type

void (empty response body)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postContactFilters**
> \Planfix\Model\InlineResponse2005 postContactFilters()

Get list contact filters

This method lets you get list contact filters

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\ContactApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->postContactFilters();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactApi->postContactFilters: ', $e->getMessage(), PHP_EOL;
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

# **postContactImport**
> postContactImport($body)

Import contact list

This method lets you import a list of companies or contacts into Planfix

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\ContactApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Planfix\Model\ContactImportBody(); // \Planfix\Model\ContactImportBody | 

try {
    $apiInstance->postContactImport($body);
} catch (Exception $e) {
    echo 'Exception when calling ContactApi->postContactImport: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Planfix\Model\ContactImportBody**](../Model/ContactImportBody.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postContactUpdateComment**
> postContactUpdateComment($id, $commentId, $body)

Update comment

This method lets you update a comment

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\ContactApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Number of contact
$commentId = 56; // int | Number of comment
$body = new \Planfix\Model\CommentUpdateRequest(); // \Planfix\Model\CommentUpdateRequest | 

try {
    $apiInstance->postContactUpdateComment($id, $commentId, $body);
} catch (Exception $e) {
    echo 'Exception when calling ContactApi->postContactUpdateComment: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Number of contact |
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

