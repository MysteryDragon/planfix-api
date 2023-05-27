# TaskListBody

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**offset** | **int** | Offset from beginning of list | [optional] [default to 0]
**pageSize** | **int** | Size of requested list | [optional] [default to 100]
**filterId** | **string** | Id for task filter, get list by method &#x27;/task/filters&#x27; | [optional] 
**filters** | [**\Planfix\Model\ComplexTaskFilter[]**](ComplexTaskFilter.md) |  | [optional] 
**fields** | **string** | Fields returned - custom field identifiers, system field names, comma-delimited | [optional] 
**sourceId** | **string** | Unique identifier of external application | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

