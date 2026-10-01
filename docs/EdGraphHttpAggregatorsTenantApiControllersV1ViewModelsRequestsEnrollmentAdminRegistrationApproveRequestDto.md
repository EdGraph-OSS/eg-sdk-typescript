# EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminRegistrationApproveRequestDto

The shared body shape for both the registration-level and application-level approve calls.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**studentLocalCode** | **string** |  | [optional] [default to undefined]
**registrationStatus** | **string** |  | [optional] [default to undefined]
**contacts** | [**Array&lt;EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminRegistrationApproveContactDto&gt;**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminRegistrationApproveContactDto.md) |  | [optional] [default to undefined]
**choices** | [**Array&lt;EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminRegistrationApproveChoiceDto&gt;**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminRegistrationApproveChoiceDto.md) |  | [optional] [default to undefined]

## Example

```typescript
import { EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminRegistrationApproveRequestDto } from '@edgraph-oss/platform-client';

const instance: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminRegistrationApproveRequestDto = {
    studentLocalCode,
    registrationStatus,
    contacts,
    choices,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
