# TaskUpdateRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | [optional] 
**sourceObjectId** | **string** |  | [optional] 
**sourceDataVersion** | **string** |  | [optional] 
**name** | **string** |  | [optional] 
**description** | **string** |  | [optional] 
**priority** | **string** |  | [optional] 
**status** | [**\Planfix\Model\BaseEntity**](BaseEntity.md) |  | [optional] 
**processId** | **int** |  | [optional] 
**resultChecking** | **bool** |  | [optional] 
**assigner** | [**\Planfix\Model\PersonRequest**](PersonRequest.md) |  | [optional] 
**parent** | [**\Planfix\Model\BaseEntity**](BaseEntity.md) |  | [optional] 
**template** | [**\Planfix\Model\BaseEntity**](BaseEntity.md) |  | [optional] 
**project** | [**\Planfix\Model\BaseEntity**](BaseEntity.md) |  | [optional] 
**counterparty** | [**\Planfix\Model\PersonRequest**](PersonRequest.md) |  | [optional] 
**dateTime** | [**\Planfix\Model\TimePoint**](TimePoint.md) |  | [optional] 
**startDateTime** | [**\Planfix\Model\TimePoint**](TimePoint.md) |  | [optional] 
**endDateTime** | [**\Planfix\Model\TimePoint**](TimePoint.md) |  | [optional] 
**hasStartDate** | **bool** |  | [optional] 
**hasEndDate** | **bool** |  | [optional] 
**hasStartTime** | **bool** |  | [optional] 
**hasEndTime** | **bool** |  | [optional] 
**delayedTillDate** | [**\Planfix\Model\TimePoint**](TimePoint.md) |  | [optional] 
**duration** | **int** |  | [optional] 
**durationUnit** | **string** |  | [optional] 
**durationType** | **string** |  | [optional] 
**overdue** | **bool** |  | [optional] 
**closeToDeadLine** | **bool** |  | [optional] 
**notAcceptedInTime** | **bool** |  | [optional] 
**inFavorites** | **bool** |  | [optional] 
**isSummary** | **bool** |  | [optional] 
**isSequential** | **bool** |  | [optional] 
**assignees** | [**\Planfix\Model\PeopleRequest**](PeopleRequest.md) |  | [optional] 
**participants** | [**\Planfix\Model\PeopleRequest**](PeopleRequest.md) |  | [optional] 
**auditors** | [**\Planfix\Model\PeopleRequest**](PeopleRequest.md) |  | [optional] 
**isDeleted** | **bool** |  | [optional] 
**customFieldData** | [**\Planfix\Model\CustomFieldValueRequest[]**](CustomFieldValueRequest.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

