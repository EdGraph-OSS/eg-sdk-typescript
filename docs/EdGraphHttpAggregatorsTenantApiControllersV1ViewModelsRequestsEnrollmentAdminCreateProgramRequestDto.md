# EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateProgramRequestDto

The body of a Program creation. EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.CreateProgramRequestDto.SchoolId, EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.CreateProgramRequestDto.ProgramTypeId and  EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.CreateProgramRequestDto.RequirementIds are record ids of existing rows; the service copies their display  fields onto the program and rejects an id it cannot find.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tenantId** | **string** |  | [optional] [default to undefined]
**schoolId** | **string** |  | [optional] [default to undefined]
**programCode** | **string** |  | [optional] [default to undefined]
**programName** | **string** |  | [optional] [default to undefined]
**programTypeId** | **string** |  | [optional] [default to undefined]
**eligibilityCriteria** | **string** |  | [optional] [default to undefined]
**requirementIds** | **Array&lt;string&gt;** |  | [optional] [default to undefined]
**grades** | **Array&lt;string&gt;** |  | [optional] [default to undefined]
**capacityByGrade** | [**Array&lt;EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminGradeCapacityRequestDto&gt;**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminGradeCapacityRequestDto.md) |  | [optional] [default to undefined]
**zone** | **string** |  | [optional] [default to undefined]
**latitude** | **number** |  | [optional] [default to undefined]
**longitude** | **number** |  | [optional] [default to undefined]

## Example

```typescript
import { EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateProgramRequestDto } from '@edgraph-oss/platform-client';

const instance: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateProgramRequestDto = {
    tenantId,
    schoolId,
    programCode,
    programName,
    programTypeId,
    eligibilityCriteria,
    requirementIds,
    grades,
    capacityByGrade,
    zone,
    latitude,
    longitude,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
