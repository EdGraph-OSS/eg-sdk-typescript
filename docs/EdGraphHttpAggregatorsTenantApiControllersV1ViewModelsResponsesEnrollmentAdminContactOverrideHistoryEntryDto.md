# EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideHistoryEntryDto

One entry in a contact\'s override history.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**eventId** | **string** |  | [optional] [default to undefined]
**detail** | **string** | Which detail this entry is about: &#x60;email&#x60; or &#x60;phone&#x60;. | [optional] [default to undefined]
**action** | **string** | &#x60;set&#x60; or &#x60;removed&#x60;. A removal returns the detail to its SIS value. | [optional] [default to undefined]
**previousValue** | **string** | The value this entry superseded, if any. Superseded values are kept, never deleted. | [optional] [default to undefined]
**newValue** | **string** |  | [optional] [default to undefined]
**sisValue** | **string** |  | [optional] [default to undefined]
**overriddenBy** | **string** |  | [optional] [default to undefined]
**overriddenAt** | **string** |  | [optional] [default to undefined]
**actingStudentId** | **string** | The student whose screen the change was made from, when one was recorded. | [optional] [default to undefined]
**studentIds** | **Array&lt;string&gt;** |  | [optional] [default to undefined]

## Example

```typescript
import { EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideHistoryEntryDto } from '@edgraph-oss/platform-client';

const instance: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideHistoryEntryDto = {
    eventId,
    detail,
    action,
    previousValue,
    newValue,
    sisValue,
    overriddenBy,
    overriddenAt,
    actingStudentId,
    studentIds,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
