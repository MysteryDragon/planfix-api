# ContactImportBody

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**sourceId** | **string** |  | [optional] 
**contactTemplateId** | **int** |  | [optional] 
**companyTemplateId** | **int** |  | [optional] 
**optionImportDuplicate** | **string** | Enum: ignore, update, none | [optional] 
**optionImportUniqueField** | **string** | Enum: email-phone-name-ifnot, email-phone-name, email-phone, phone, name, email-and-phone-and-name, number, custom  OR custom:{fieldId} | [optional] 
**optionImportUniqueDefaultField** | **string** | Enum: name, email-phone-name | [optional] 
**contacts** | [**\Planfix\Model\ContactRequest[]**](ContactRequest.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

