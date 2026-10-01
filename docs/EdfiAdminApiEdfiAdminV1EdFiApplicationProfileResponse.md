# EdfiAdminApiEdfiAdminV1EdFiApplicationProfileResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tenantId** | **string** |  | [optional] [default to undefined]
**instanceId** | **string** |  | [optional] [default to undefined]
**applicationId** | **number** |  | [optional] [default to undefined]
**applicationName** | **string** |  | [optional] [default to undefined]
**claimSetName** | **string** |  | [optional] [default to undefined]
**vendorId** | **number** |  | [optional] [default to undefined]
**vendor** | [**EdfiAdminApiEdfiAdminV1Vendor**](EdfiAdminApiEdfiAdminV1Vendor.md) |  | [optional] [default to undefined]
**educationOrganizations** | [**Array&lt;EdfiAdminApiEdfiAdminV1EducationOrganization&gt;**](EdfiAdminApiEdfiAdminV1EducationOrganization.md) | TODO Is adding Vendor object which also has application object correct ? | [optional] [readonly] [default to undefined]
**operationalContextUri** | **string** |  | [optional] [default to undefined]
**years** | **Array&lt;number&gt;** |  | [optional] [readonly] [default to undefined]

## Example

```typescript
import { EdfiAdminApiEdfiAdminV1EdFiApplicationProfileResponse } from '@edgraph-oss/platform-client';

const instance: EdfiAdminApiEdfiAdminV1EdFiApplicationProfileResponse = {
    tenantId,
    instanceId,
    applicationId,
    applicationName,
    claimSetName,
    vendorId,
    vendor,
    educationOrganizations,
    operationalContextUri,
    years,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
