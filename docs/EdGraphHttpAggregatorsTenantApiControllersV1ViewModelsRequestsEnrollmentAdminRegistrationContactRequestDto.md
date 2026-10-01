# EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminRegistrationContactRequestDto

A contact carried on a Registration create call. EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.RegistrationContactRequestDto.Id is the entry\'s own id (minted when  omitted); EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.RegistrationContactRequestDto.ContactId is the EnrollmentContact record id, resolved server-side from the  email/phone when omitted; EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.RegistrationContactRequestDto.ExternalDataSourceContactId is the SIS id, when known.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional] [default to undefined]
**contactId** | **string** |  | [optional] [default to undefined]
**contactName** | **string** |  | [optional] [default to undefined]
**contactPhone** | **string** |  | [optional] [default to undefined]
**contactEmail** | **string** |  | [optional] [default to undefined]
**externalDataSourceContactId** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminRegistrationContactRequestDto } from '@edgraph-oss/platform-client';

const instance: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminRegistrationContactRequestDto = {
    id,
    contactId,
    contactName,
    contactPhone,
    contactEmail,
    externalDataSourceContactId,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
