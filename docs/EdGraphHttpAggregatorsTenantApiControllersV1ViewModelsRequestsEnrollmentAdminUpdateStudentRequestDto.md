# EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateStudentRequestDto

The body of a student update. As EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.UpsertStudentRequestDto, contact association is  managed exclusively through the `/students/{id}/contacts` sub-resource, not through this call.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional] [default to undefined]
**tenantId** | **string** |  | [optional] [default to undefined]
**studentStateCode** | **string** |  | [optional] [default to undefined]
**externalDataSourceStudentId** | **string** |  | [optional] [default to undefined]
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

## Example

```typescript
import { EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateStudentRequestDto } from '@edgraph-oss/platform-client';

const instance: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateStudentRequestDto = {
    id,
    tenantId,
    studentStateCode,
    externalDataSourceStudentId,
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
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
