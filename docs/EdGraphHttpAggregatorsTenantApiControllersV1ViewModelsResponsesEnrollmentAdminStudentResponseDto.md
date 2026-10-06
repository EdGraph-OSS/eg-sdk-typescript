# EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminStudentResponseDto

One Enrollment Student, from the list and the get-by-id route alike. `registrationId` is set only on  a list row that stands for a registration not yet linked to a student (a new student): that row\'s  `id` is the registration\'s id, which the get-by-id route cannot resolve, so a client must not open a  student profile from it. Absent on every real student.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional] [default to undefined]
**tenantId** | **string** |  | [optional] [default to undefined]
**studentLocalCode** | **string** |  | [optional] [default to undefined]
**studentStateCode** | **string** |  | [optional] [default to undefined]
**externalDataSourceStudentId** | **string** |  | [optional] [default to undefined]
**allowedPathwayIds** | [**Array&lt;EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminAllowedPathwayIdDto&gt;**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminAllowedPathwayIdDto.md) |  | [optional] [default to undefined]
**firstName** | **string** |  | [optional] [default to undefined]
**middleName** | **string** |  | [optional] [default to undefined]
**lastName** | **string** |  | [optional] [default to undefined]
**birthdate** | **string** |  | [optional] [default to undefined]
**last4SSN** | **string** |  | [optional] [default to undefined]
**nextAddress** | **string** |  | [optional] [default to undefined]
**nextGradeLevel** | **string** |  | [optional] [default to undefined]
**nextSchoolStateShortCode** | **string** |  | [optional] [default to undefined]
**nextSchoolStateCode** | **string** |  | [optional] [default to undefined]
**nextSchoolName** | **string** |  | [optional] [default to undefined]
**nextSchoolAddress** | **string** |  | [optional] [default to undefined]
**eligibilityCode** | **string** |  | [optional] [default to undefined]
**eligibilityDescription** | **string** |  | [optional] [default to undefined]
**contacts** | [**Array&lt;EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminStudentContactResponseDto&gt;**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminStudentContactResponseDto.md) |  | [optional] [default to undefined]
**createdBy** | **string** |  | [optional] [default to undefined]
**createdDateTime** | **string** |  | [optional] [default to undefined]
**lastModifiedBy** | **string** |  | [optional] [default to undefined]
**lastModifiedDateTime** | **string** |  | [optional] [default to undefined]
**deletedBy** | **string** |  | [optional] [default to undefined]
**deletedDateTime** | **string** |  | [optional] [default to undefined]
**isDeleted** | **boolean** |  | [optional] [default to undefined]
**registrationId** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminStudentResponseDto } from '@edgraph-oss/platform-client';

const instance: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminStudentResponseDto = {
    id,
    tenantId,
    studentLocalCode,
    studentStateCode,
    externalDataSourceStudentId,
    allowedPathwayIds,
    firstName,
    middleName,
    lastName,
    birthdate,
    last4SSN,
    nextAddress,
    nextGradeLevel,
    nextSchoolStateShortCode,
    nextSchoolStateCode,
    nextSchoolName,
    nextSchoolAddress,
    eligibilityCode,
    eligibilityDescription,
    contacts,
    createdBy,
    createdDateTime,
    lastModifiedBy,
    lastModifiedDateTime,
    deletedBy,
    deletedDateTime,
    isDeleted,
    registrationId,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
