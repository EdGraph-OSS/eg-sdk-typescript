# EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateRequirementRequestDto

The body of a requirement creation. The route names the tenant, so the body carries only the  requirement\'s own fields. EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.CreateRequirementRequestDto.RequirementType is one of `document`, `url`,  `information` or `event`, lowercase as stored. EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.CreateRequirementRequestDto.IsRequired left out  creates a required requirement. EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.CreateRequirementRequestDto.IsUploadEnabled left out is false, and the service  forces it false for a `url` or `information` requirement. EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.CreateRequirementRequestDto.Url is required  for a `url` requirement (an absolute http or https link) and not used for other types. A code  already used in the tenant (deleted rows included) is refused with 409.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**requirementType** | **string** |  | [optional] [default to undefined]
**requirementCode** | **string** |  | [optional] [default to undefined]
**requirementTitle** | **string** |  | [optional] [default to undefined]
**requirementDescription** | **string** |  | [optional] [default to undefined]
**isUploadEnabled** | **boolean** |  | [optional] [default to undefined]
**isRequired** | **boolean** |  | [optional] [default to undefined]
**url** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateRequirementRequestDto } from '@edgraph-oss/platform-client';

const instance: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateRequirementRequestDto = {
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
