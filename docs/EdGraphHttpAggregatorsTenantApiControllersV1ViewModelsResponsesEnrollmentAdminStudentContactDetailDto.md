# EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminStudentContactDetailDto

A contact linked to a student, joined with that contact\'s own live name/email/phone, plus the  association attributes read from this student\'s own EnrollmentStudentContact entry for the  contact. The reverse-direction sibling of EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Responses.EnrollmentAdmin.ContactStudentDetailDto. `id` is the  contact record id; `externalDataSourceContactId` is its SIS id, when it has one.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional] [default to undefined]
**externalDataSourceContactId** | **string** |  | [optional] [default to undefined]
**firstName** | **string** |  | [optional] [default to undefined]
**lastName** | **string** |  | [optional] [default to undefined]
**email** | **string** |  | [optional] [default to undefined]
**phone** | **string** |  | [optional] [default to undefined]
**priority** | **number** |  | [optional] [default to undefined]
**relationship** | **string** |  | [optional] [default to undefined]
**livesWithStudent** | **boolean** |  | [optional] [default to undefined]
**hasLegalCustody** | **boolean** |  | [optional] [default to undefined]
**canPickUp** | **boolean** |  | [optional] [default to undefined]
**isEmergency** | **boolean** |  | [optional] [default to undefined]

## Example

```typescript
import { EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminStudentContactDetailDto } from '@edgraph-oss/platform-client';

const instance: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminStudentContactDetailDto = {
    id,
    externalDataSourceContactId,
    firstName,
    lastName,
    email,
    phone,
    priority,
    relationship,
    livesWithStudent,
    hasLegalCustody,
    canPickUp,
    isEmergency,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
