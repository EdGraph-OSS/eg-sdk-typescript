# EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateRequirementRequestDto

The body of a requirement update: every field is replaced, except EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.UpdateRequirementRequestDto.IsRequired, which  keeps the stored value when left out. EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.UpdateRequirementRequestDto.IsUploadEnabled must be sent, because the  service reads a missing value as false. EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.UpdateRequirementRequestDto.Url is replaced like the title, under the create  rule. Programs keep the copy of a requirement taken when they were last saved; changing a requirement  does not rewrite those copies.

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
import { EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateRequirementRequestDto } from '@edgraph-oss/platform-client';

const instance: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateRequirementRequestDto = {
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
