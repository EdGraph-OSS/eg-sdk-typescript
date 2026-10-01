# EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateProgramRequestDto

The body of a Program update. The school never changes; the program type and the requirement  set are replaced from the ids given here (an empty list clears the requirements).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional] [default to undefined]
**tenantId** | **string** |  | [optional] [default to undefined]
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
import { EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateProgramRequestDto } from '@edgraph-oss/platform-client';

const instance: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateProgramRequestDto = {
    id,
    tenantId,
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
