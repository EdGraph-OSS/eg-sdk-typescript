# EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminAddOrCreateStudentContactRequestDto

The body of a student-contact link where the contact is created if its  EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.AddOrCreateStudentContactRequestDto.ExternalDataSourceContactId (the SIS id) does not already exist. When it does, the submitted name/email/phone are ignored - an existing  contact is only linked, never overwritten, by this route.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**externalDataSourceContactId** | **string** |  | [optional] [default to undefined]
**firstName** | **string** |  | [optional] [default to undefined]
**lastName** | **string** |  | [optional] [default to undefined]
**email** | **string** |  | [optional] [default to undefined]
**phone** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminAddOrCreateStudentContactRequestDto } from '@edgraph-oss/platform-client';

const instance: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminAddOrCreateStudentContactRequestDto = {
    externalDataSourceContactId,
    firstName,
    lastName,
    email,
    phone,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
