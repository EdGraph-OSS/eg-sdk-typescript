# EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateContactRequestDto

The body of a contact creation.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tenantId** | **string** | Must match the tenant in the route. | [optional] [default to undefined]
**contactId** | **string** | The contact\&#39;s identifier in the source system. Distinct from the record id, which the service  assigns and returns in the response. | [optional] [default to undefined]
**firstName** | **string** | Required. Never overridable - only email and phone are. | [optional] [default to undefined]
**lastName** | **string** | Required. Never overridable - only email and phone are. | [optional] [default to undefined]
**email** | **string** | The SIS-sourced email. Correcting it later is an override and goes through the  &#x60;email-override&#x60; route instead - see EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.UpdateContactRequestDto. | [optional] [default to undefined]
**phone** | **string** | The SIS-sourced phone, on the same terms as Email. | [optional] [default to undefined]
**students** | [**Array&lt;EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminContactStudentRequestDto&gt;**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminContactStudentRequestDto.md) | The students to link the contact to. Optional; omit or send an empty list for a contact with no  links yet. | [optional] [default to undefined]

## Example

```typescript
import { EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateContactRequestDto } from '@edgraph-oss/platform-client';

const instance: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateContactRequestDto = {
    tenantId,
    contactId,
    firstName,
    lastName,
    email,
    phone,
    students,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
