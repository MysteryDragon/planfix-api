# CommentResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | [optional] 
**sourceObjectId** | **string** |  | [optional] 
**sourceDataVersion** | **string** |  | [optional] 
**dateTime** | [**\Planfix\Model\TimePoint**](TimePoint.md) |  | [optional] 
**type** | **string** |  | [optional] 
**fromType** | **string** |  | [optional] 
**description** | **string** |  | [optional] 
**task** | [**\Planfix\Model\BaseEntity**](BaseEntity.md) |  | [optional] 
**project** | [**\Planfix\Model\BaseEntity**](BaseEntity.md) |  | [optional] 
**contact** | [**\Planfix\Model\PersonResponse**](PersonResponse.md) |  | [optional] 
**owner** | [**\Planfix\Model\PersonResponse**](PersonResponse.md) |  | [optional] 
**isDeleted** | **bool** |  | [optional] 
**isPinned** | **bool** |  | [optional] 
**isHidden** | **bool** |  | [optional] 
**isNotRead** | **bool** |  | [optional] 
**recipients** | [**\Planfix\Model\PeopleResponse**](PeopleResponse.md) |  | [optional] 
**reminders** | [**\Planfix\Model\Reminder[]**](Reminder.md) |  | [optional] 
**dataTags** | [**\Planfix\Model\CommentResponseDataTags[]**](CommentResponseDataTags.md) |  | [optional] 
**files** | [**\Planfix\Model\FileResponse[]**](FileResponse.md) |  | [optional] 
**changeTaskStartDate** | [**\Planfix\Model\ChangeDate**](ChangeDate.md) |  | [optional] 
**changeTaskExpectDate** | [**\Planfix\Model\ChangeDate**](ChangeDate.md) |  | [optional] 
**changeStatus** | [**\Planfix\Model\CommentResponseChangeStatus**](CommentResponseChangeStatus.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

