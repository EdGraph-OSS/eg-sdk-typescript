# EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminRegistrationApproveContactDto

One contact to upsert into the Registration\'s Contacts collection as part of an approve call,  matched by EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.RegistrationApproveContactDto.ContactId - the EnrollmentContact record id. An entry without one is  appended as a new contact.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**contactId** | **string** |  | [optional] [default to undefined]
**contactEmail** | **string** |  | [optional] [default to undefined]
**contactPhone** | **string** |  | [optional] [default to undefined]
**externalDataSourceContactId** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminRegistrationApproveContactDto } from '@edgraph-oss/platform-client';

const instance: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminRegistrationApproveContactDto = {
    contactId,
    contactEmail,
    contactPhone,
    externalDataSourceContactId,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
