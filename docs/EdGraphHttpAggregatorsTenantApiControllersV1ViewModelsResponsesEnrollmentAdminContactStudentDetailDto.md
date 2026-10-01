# EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactStudentDetailDto

A student linked to a contact, with the association attributes read from that student\'s own  EnrollmentStudentContact entry for this contact. `studentId` is the student record id;  `studentLocalCode` is the SIS code.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**studentId** | **string** |  | [optional] [default to undefined]
**studentLocalCode** | **string** |  | [optional] [default to undefined]
**studentStateCode** | **string** |  | [optional] [default to undefined]
**studentFirstName** | **string** |  | [optional] [default to undefined]
**studentMiddleName** | **string** |  | [optional] [default to undefined]
**studentLastName** | **string** |  | [optional] [default to undefined]
**priority** | **number** |  | [optional] [default to undefined]
**relationship** | **string** |  | [optional] [default to undefined]
**livesWithStudent** | **boolean** |  | [optional] [default to undefined]
**hasLegalCustody** | **boolean** |  | [optional] [default to undefined]
**canPickUp** | **boolean** |  | [optional] [default to undefined]
**isEmergency** | **boolean** |  | [optional] [default to undefined]

## Example

```typescript
import { EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactStudentDetailDto } from '@edgraph-oss/platform-client';

const instance: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactStudentDetailDto = {
    studentId,
    studentLocalCode,
    studentStateCode,
    studentFirstName,
    studentMiddleName,
    studentLastName,
    priority,
    relationship,
    livesWithStudent,
    hasLegalCustody,
    canPickUp,
    isEmergency,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
