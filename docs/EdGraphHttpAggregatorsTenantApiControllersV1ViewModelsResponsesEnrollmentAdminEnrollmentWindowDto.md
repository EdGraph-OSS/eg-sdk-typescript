# EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminEnrollmentWindowDto

A window the round owns. Instants are UTC; EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Responses.EnrollmentAdmin.EnrollmentWindowDto.TimeZone is the IANA zone they are  shown in. EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Responses.EnrollmentAdmin.EnrollmentWindowDto.OpensAt is absent when EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Responses.EnrollmentAdmin.EnrollmentWindowDto.DependsOn sets the open moment.  EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Responses.EnrollmentAdmin.EnrollmentWindowDto.UnavailableReason is present only while the dependency keeps the window closed.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional] [default to undefined]
**kind** | **string** |  | [optional] [default to undefined]
**opensAt** | **string** |  | [optional] [default to undefined]
**closesAt** | **string** |  | [optional] [default to undefined]
**timeZone** | **string** |  | [optional] [default to undefined]
**dependsOn** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminWindowDependencyDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminWindowDependencyDto.md) |  | [optional] [default to undefined]
**state** | **string** |  | [optional] [default to undefined]
**unavailableReason** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminEnrollmentWindowDto } from '@edgraph-oss/platform-client';

const instance: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminEnrollmentWindowDto = {
    id,
    kind,
    opensAt,
    closesAt,
    timeZone,
    dependsOn,
    state,
    unavailableReason,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
