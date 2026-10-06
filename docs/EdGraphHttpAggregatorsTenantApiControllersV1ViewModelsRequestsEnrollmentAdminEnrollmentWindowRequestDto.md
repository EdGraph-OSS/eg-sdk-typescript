# EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminEnrollmentWindowRequestDto

A window as written. EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.EnrollmentWindowRequestDto.OpensAt and EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.EnrollmentWindowRequestDto.ClosesAt are ISO-8601 instants with  their offset (\"2026-06-01T08:00:00-05:00\" or \"...Z\"); they are passed to the Enrollment Service  verbatim, which refuses one without an offset. EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.EnrollmentWindowRequestDto.OpensAt may be omitted only when  EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.EnrollmentWindowRequestDto.DependsOn is set.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**kind** | **string** |  | [optional] [default to undefined]
**opensAt** | **string** |  | [optional] [default to undefined]
**closesAt** | **string** |  | [optional] [default to undefined]
**timeZone** | **string** |  | [optional] [default to undefined]
**dependsOn** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminWindowDependencyRequestDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminWindowDependencyRequestDto.md) |  | [optional] [default to undefined]

## Example

```typescript
import { EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminEnrollmentWindowRequestDto } from '@edgraph-oss/platform-client';

const instance: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminEnrollmentWindowRequestDto = {
    kind,
    opensAt,
    closesAt,
    timeZone,
    dependsOn,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
