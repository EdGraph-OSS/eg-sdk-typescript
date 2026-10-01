# EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminRequirementRefDto

One requirement, as embedded on the program. EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Responses.EnrollmentAdmin.RequirementRefDto.RequirementId is the requirements row.  EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Responses.EnrollmentAdmin.RequirementRefDto.IsRequired is copied from that row when the program is saved; false means optional.  EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Responses.EnrollmentAdmin.RequirementRefDto.Url is copied the same way, and set only on a `url` requirement.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional] [default to undefined]
**requirementId** | **string** |  | [optional] [default to undefined]
**requirementType** | **string** |  | [optional] [default to undefined]
**requirementCode** | **string** |  | [optional] [default to undefined]
**requirementTitle** | **string** |  | [optional] [default to undefined]
**requirementDescription** | **string** |  | [optional] [default to undefined]
**isUploadEnabled** | **boolean** |  | [optional] [default to undefined]
**isRequired** | **boolean** |  | [optional] [default to undefined]
**url** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminRequirementRefDto } from '@edgraph-oss/platform-client';

const instance: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminRequirementRefDto = {
    id,
    requirementId,
    requirementType,
    requirementCode,
    requirementTitle,
    requirementDescription,
    isUploadEnabled,
    isRequired,
    url,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
