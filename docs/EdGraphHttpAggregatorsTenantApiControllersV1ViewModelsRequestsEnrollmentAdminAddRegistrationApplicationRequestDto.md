# EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminAddRegistrationApplicationRequestDto

The body of adding one Program-seat choice to an existing Registration. See  EnrollmentAdminController.Registrations.AddEnrollmentRegistrationApplication.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tenantId** | **string** |  | [optional] [default to undefined]
**programId** | **string** | The target Program\&#39;s record id (as returned in &#x60;ProgramMutationResultDto.Id&#x60; /  &#x60;ProgramDetailDto.Id&#x60;), not its business ProgramId/code - unlike every other  &#x60;ProgramId&#x60; field on the Programs DTOs. | [optional] [default to undefined]

## Example

```typescript
import { EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminAddRegistrationApplicationRequestDto } from '@edgraph-oss/platform-client';

const instance: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminAddRegistrationApplicationRequestDto = {
    tenantId,
    programId,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
