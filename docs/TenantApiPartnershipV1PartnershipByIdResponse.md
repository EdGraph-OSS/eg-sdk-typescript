# TenantApiPartnershipV1PartnershipByIdResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional] [default to undefined]
**partnerTenantId** | **string** |  | [optional] [default to undefined]
**partnershipType** | **string** |  | [optional] [default to undefined]
**relatedTenantsIds** | **Array&lt;string&gt;** |  | [optional] [readonly] [default to undefined]
**partnershipSync** | [**TenantApiPartnershipV1PartnershipSyncDTO**](TenantApiPartnershipV1PartnershipSyncDTO.md) |  | [optional] [default to undefined]
**createdDateTime** | **string** |  | [optional] [default to undefined]
**createdBy** | **string** |  | [optional] [default to undefined]
**lastModifiedDateTime** | **string** |  | [optional] [default to undefined]
**lastModifiedBy** | **string** |  | [optional] [default to undefined]
**deletedBy** | **string** |  | [optional] [default to undefined]
**deletedDateTime** | **string** |  | [optional] [default to undefined]
**isDeleted** | **boolean** |  | [optional] [default to undefined]
**roleMappings** | [**Array&lt;TenantApiPartnershipV1RoleMappingDTO&gt;**](TenantApiPartnershipV1RoleMappingDTO.md) |  | [optional] [readonly] [default to undefined]
**scope** | [**TenantApiPartnershipV1PartnershipScope**](TenantApiPartnershipV1PartnershipScope.md) |  | [optional] [default to undefined]
**optedOutTenantIds** | **Array&lt;string&gt;** |  | [optional] [readonly] [default to undefined]

## Example

```typescript
import { TenantApiPartnershipV1PartnershipByIdResponse } from '@edgraph-oss/platform-client';

const instance: TenantApiPartnershipV1PartnershipByIdResponse = {
    id,
    partnerTenantId,
    partnershipType,
    relatedTenantsIds,
    partnershipSync,
    createdDateTime,
    createdBy,
    lastModifiedDateTime,
    lastModifiedBy,
    deletedBy,
    deletedDateTime,
    isDeleted,
    roleMappings,
    scope,
    optedOutTenantIds,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
