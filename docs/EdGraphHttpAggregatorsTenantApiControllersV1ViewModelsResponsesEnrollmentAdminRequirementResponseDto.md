# EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminRequirementResponseDto

Something a family must satisfy for a program. Programs embed a copy of it  (EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Responses.EnrollmentAdmin.RequirementRefDto), where `requirementId` is this row\'s EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Responses.EnrollmentAdmin.RequirementResponseDto.Id.  EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Responses.EnrollmentAdmin.RequirementResponseDto.RequirementType is one of `document`, `url`, `information` or  `event`. EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Responses.EnrollmentAdmin.RequirementResponseDto.IsUploadEnabled can only be true for a `document` or an `event`.  EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Responses.EnrollmentAdmin.RequirementResponseDto.IsRequired false means the requirement is optional. EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Responses.EnrollmentAdmin.RequirementResponseDto.Url is the online  form of a `url` requirement, absent for other types.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional] [default to undefined]
**tenantId** | **string** |  | [optional] [default to undefined]
**requirementType** | **string** |  | [optional] [default to undefined]
**requirementCode** | **string** |  | [optional] [default to undefined]
**requirementTitle** | **string** |  | [optional] [default to undefined]
**requirementDescription** | **string** |  | [optional] [default to undefined]
**isUploadEnabled** | **boolean** |  | [optional] [default to undefined]
**isRequired** | **boolean** |  | [optional] [default to undefined]
**url** | **string** |  | [optional] [default to undefined]
**createdBy** | **string** |  | [optional] [default to undefined]
**createdDateTime** | **string** |  | [optional] [default to undefined]
**lastModifiedBy** | **string** |  | [optional] [default to undefined]
**lastModifiedDateTime** | **string** |  | [optional] [default to undefined]
**isDeleted** | **boolean** |  | [optional] [default to undefined]

## Example

```typescript
import { EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminRequirementResponseDto } from '@edgraph-oss/platform-client';

const instance: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminRequirementResponseDto = {
    id,
    tenantId,
    requirementType,
    requirementCode,
    requirementTitle,
    requirementDescription,
    isUploadEnabled,
    isRequired,
    url,
    createdBy,
    createdDateTime,
    lastModifiedBy,
    lastModifiedDateTime,
    isDeleted,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
