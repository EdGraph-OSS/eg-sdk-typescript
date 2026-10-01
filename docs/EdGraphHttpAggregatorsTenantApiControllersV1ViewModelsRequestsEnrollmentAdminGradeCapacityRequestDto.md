# EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminGradeCapacityRequestDto

One grade\'s seats. EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.GradeCapacityRequestDto.SeatsAvailable, EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.GradeCapacityRequestDto.LotteryEligible and  EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.GradeCapacityRequestDto.SchoolYear are what the lottery reads; the Salesforce sync normally supplies  them, and an admin edit may leave them null to keep whatever the row already has unset.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**grade** | **string** |  | [optional] [default to undefined]
**capacity** | **number** |  | [optional] [default to undefined]
**enrolled** | **number** |  | [optional] [default to undefined]
**seatsAvailable** | **number** |  | [optional] [default to undefined]
**lotteryEligible** | **boolean** |  | [optional] [default to undefined]
**schoolYear** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminGradeCapacityRequestDto } from '@edgraph-oss/platform-client';

const instance: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminGradeCapacityRequestDto = {
    grade,
    capacity,
    enrolled,
    seatsAvailable,
    lotteryEligible,
    schoolYear,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
