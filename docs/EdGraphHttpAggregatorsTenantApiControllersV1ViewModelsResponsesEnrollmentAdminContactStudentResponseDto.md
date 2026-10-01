# EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactStudentResponseDto

One student linked to a contact. `_id` is the link entry\'s own id, NOT the student: read  `studentId` for the student record id and `studentLocalCode` for the SIS code.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional] [default to undefined]
**studentId** | **string** |  | [optional] [default to undefined]
**studentLocalCode** | **string** |  | [optional] [default to undefined]
**studentStateCode** | **string** |  | [optional] [default to undefined]
**studentFirstName** | **string** |  | [optional] [default to undefined]
**studentMiddleName** | **string** |  | [optional] [default to undefined]
**studentLastName** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactStudentResponseDto } from '@edgraph-oss/platform-client';

const instance: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactStudentResponseDto = {
    id,
    studentId,
    studentLocalCode,
    studentStateCode,
    studentFirstName,
    studentMiddleName,
    studentLastName,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
