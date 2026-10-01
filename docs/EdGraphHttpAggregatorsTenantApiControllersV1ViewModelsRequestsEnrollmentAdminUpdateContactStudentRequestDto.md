# EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateContactStudentRequestDto

The body of a contact-student association update - the association attributes only. Neither the  contact nor the student themselves are editable through this route.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**priority** | **number** |  | [optional] [default to undefined]
**relationship** | **string** |  | [optional] [default to undefined]
**livesWithStudent** | **boolean** |  | [optional] [default to undefined]
**hasLegalCustody** | **boolean** |  | [optional] [default to undefined]
**canPickUp** | **boolean** |  | [optional] [default to undefined]
**isEmergency** | **boolean** |  | [optional] [default to undefined]

## Example

```typescript
import { EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateContactStudentRequestDto } from '@edgraph-oss/platform-client';

const instance: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateContactStudentRequestDto = {
    priority,
    relationship,
    livesWithStudent,
    hasLegalCustody,
    canPickUp,
    isEmergency,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
