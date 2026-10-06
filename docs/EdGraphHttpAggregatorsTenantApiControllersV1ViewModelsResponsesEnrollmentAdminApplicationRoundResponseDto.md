# EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminApplicationRoundResponseDto

An application round: a named enrollment period in a school year, identified by  (EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Responses.EnrollmentAdmin.ApplicationRoundResponseDto.Code, EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Responses.EnrollmentAdmin.ApplicationRoundResponseDto.SchoolYear). EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Responses.EnrollmentAdmin.ApplicationRoundResponseDto.State and each window\'s state are  derived by the service at the moment of the read - NotYetOpen, Open or Closed - and never stored.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional] [default to undefined]
**tenantId** | **string** |  | [optional] [default to undefined]
**code** | **string** |  | [optional] [default to undefined]
**schoolYear** | **string** |  | [optional] [default to undefined]
**label** | **string** |  | [optional] [default to undefined]
**grades** | **Array&lt;string&gt;** |  | [optional] [default to undefined]
**programTypes** | [**Array&lt;EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramTypeRefDto&gt;**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramTypeRefDto.md) |  | [optional] [default to undefined]
**windows** | [**Array&lt;EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminEnrollmentWindowDto&gt;**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminEnrollmentWindowDto.md) |  | [optional] [default to undefined]
**state** | **string** |  | [optional] [default to undefined]
**createdBy** | **string** |  | [optional] [default to undefined]
**createdDateTime** | **string** |  | [optional] [default to undefined]
**lastModifiedBy** | **string** |  | [optional] [default to undefined]
**lastModifiedDateTime** | **string** |  | [optional] [default to undefined]
**isDeleted** | **boolean** |  | [optional] [default to undefined]

## Example

```typescript
import { EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminApplicationRoundResponseDto } from '@edgraph-oss/platform-client';

const instance: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminApplicationRoundResponseDto = {
    id,
    tenantId,
    code,
    schoolYear,
    label,
    grades,
    programTypes,
    windows,
    state,
    createdBy,
    createdDateTime,
    lastModifiedBy,
    lastModifiedDateTime,
    isDeleted,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
