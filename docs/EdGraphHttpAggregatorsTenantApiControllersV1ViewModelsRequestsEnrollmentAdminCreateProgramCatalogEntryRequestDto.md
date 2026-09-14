# EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateProgramCatalogEntryRequestDto

The body of a district catalog entry creation. No school-identifying field - that is what  distinguishes a catalog entry from a school program; see  EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.CreateSchoolProgramRequestDto for adding it to a school.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tenantId** | **string** |  | [optional] [default to undefined]
**code** | **string** |  | [optional] [default to undefined]
**name** | **string** |  | [optional] [default to undefined]
**programType** | **string** |  | [optional] [default to undefined]
**eligibilityCriteria** | **string** |  | [optional] [default to undefined]
**requiredDocuments** | **Array&lt;string&gt;** |  | [optional] [default to undefined]
**internalDisplayName** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateProgramCatalogEntryRequestDto } from '@edgraph-oss/platform-client';

const instance: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateProgramCatalogEntryRequestDto = {
    tenantId,
    code,
    name,
    programType,
    eligibilityCriteria,
    requiredDocuments,
    internalDisplayName,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
