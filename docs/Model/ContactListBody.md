# ContactListBody

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**offset** | **int** | Offset from beginning of list | [optional] [default to 0]
**pageSize** | **int** | Size of requested list | [optional] [default to 100]
**filterId** | **string** | Id for contact filter, get list by method &#x27;/contact/filters&#x27; | [optional] 
**filters** | [**\Planfix\Model\ComplexContactFilter[]**](ComplexContactFilter.md) |  | [optional] 
**isCompany** | **bool** | True for companies / false for contacts | [optional] [default to false]
**onlyChanged** | **bool** | Flag for retrieving only data modified since last sync with external application | [optional] [default to false]
**prefixedId** | **bool** | Flag for retrieving id with a prefix | [optional] 
**fields** | **string** | Fields returned - custom field identifiers, system field names, comma-delimited | [optional] 
**sourceId** | **string** | Unique identifier of external application | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

