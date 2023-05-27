# Planfix\FileApi

All URIs are relative to *https://your-account.planfix.com/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteFileId**](FileApi.md#deletefileid) | **DELETE** /file/{id} | Delete file
[**getFileId**](FileApi.md#getfileid) | **GET** /file/{id} | Get file by identifier
[**getFileIdDownload**](FileApi.md#getfileiddownload) | **GET** /file/{id}/download | Download file
[**postFileUpload**](FileApi.md#postfileupload) | **POST** /file/ | Upload file
[**postFileUploadByUrl**](FileApi.md#postfileuploadbyurl) | **POST** /file/from-url/ | Upload file by link

# **deleteFileId**
> deleteFileId($id)

Delete file

This method lets you delete a file by its ID

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\FileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | File identifier

try {
    $apiInstance->deleteFileId($id);
} catch (Exception $e) {
    echo 'Exception when calling FileApi->deleteFileId: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| File identifier |

### Return type

void (empty response body)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getFileId**
> \Planfix\Model\InlineResponse20014 getFileId($id)

Get file by identifier

This method lets you get a file by its ID

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\FileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | File identifier

try {
    $result = $apiInstance->getFileId($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FileApi->getFileId: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| File identifier |

### Return type

[**\Planfix\Model\InlineResponse20014**](../Model/InlineResponse20014.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getFileIdDownload**
> getFileIdDownload($id)

Download file

This method lets you download file

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\FileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | File ID

try {
    $apiInstance->getFileIdDownload($id);
} catch (Exception $e) {
    echo 'Exception when calling FileApi->getFileIdDownload: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| File ID |

### Return type

void (empty response body)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postFileUpload**
> \Planfix\Model\InlineResponse20015 postFileUpload($file)

Upload file

This method lets you upload file to Planfix

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\FileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$file = new \Planfix\Model\null(); //  | 

try {
    $result = $apiInstance->postFileUpload($file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FileApi->postFileUpload: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file** | [****](../Model/.md)|  | [optional]

### Return type

[**\Planfix\Model\InlineResponse20015**](../Model/InlineResponse20015.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postFileUploadByUrl**
> \Planfix\Model\InlineResponse20015 postFileUploadByUrl($body)

Upload file by link

This method lets you upload a file to Planfix using a link

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: rest_auth
    $config = Planfix\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Planfix\Api\FileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Planfix\Model\FileUploadRequest(); // \Planfix\Model\FileUploadRequest | 

try {
    $result = $apiInstance->postFileUploadByUrl($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FileApi->postFileUploadByUrl: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Planfix\Model\FileUploadRequest**](../Model/FileUploadRequest.md)|  | [optional]

### Return type

[**\Planfix\Model\InlineResponse20015**](../Model/InlineResponse20015.md)

### Authorization

[rest_auth](../../README.md#rest_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

