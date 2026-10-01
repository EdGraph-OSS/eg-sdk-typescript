# EdfiAdminApiEdfiAdminV1Instance


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Details | [optional] [default to undefined]
**instanceName** | **string** |  | [optional] [default to undefined]
**useCustomId** | **boolean** |  | [optional] [default to undefined]
**customId** | **string** |  | [optional] [default to undefined]
**description** | **string** |  | [optional] [default to undefined]
**connectionName** | **string** |  | [optional] [default to undefined]
**selectedConnectionId** | **string** | Connection | [optional] [default to undefined]
**selectedConnection** | [**EdfiAdminApiEdfiAdminV1EdFiConnection**](EdfiAdminApiEdfiAdminV1EdFiConnection.md) |  | [optional] [default to undefined]
**databases** | [**EdfiAdminApiEdfiAdminV1InstanceDatabases**](EdfiAdminApiEdfiAdminV1InstanceDatabases.md) |  | [optional] [default to undefined]
**password** | **string** | API Client | [optional] [default to undefined]
**apiClientKey** | **string** |  | [optional] [default to undefined]
**apiClientSecret** | **string** |  | [optional] [default to undefined]
**isApiClientSecretSecured** | **string** |  | [optional] [default to undefined]
**tenantId** | **string** | Metadata | [optional] [default to undefined]
**createdBy** | **string** |  | [optional] [default to undefined]
**createdDateTime** | **string** |  | [optional] [default to undefined]
**isDeleted** | **boolean** |  | [optional] [default to undefined]
**lastModifiedBy** | **string** |  | [optional] [default to undefined]
**lastModifiedDateTime** | **string** |  | [optional] [default to undefined]
**apiAuthUrl** | **string** | URLs | [optional] [default to undefined]
**apiResourcesUrls** | **Array&lt;string&gt;** |  | [optional] [readonly] [default to undefined]
**apiCompositesUrls** | **Array&lt;string&gt;** |  | [optional] [readonly] [default to undefined]
**selectedConnectionType** | **string** | Connection | [optional] [default to undefined]
**isDefault** | **boolean** | IsDefault | [optional] [default to undefined]
**provider** | **string** | Provider | [optional] [default to undefined]
**onboarding** | [**EdfiAdminApiEdfiAdminV1Onboarding**](EdfiAdminApiEdfiAdminV1Onboarding.md) |  | [optional] [default to undefined]
**applications** | [**Array&lt;EdfiAdminApiEdfiAdminV1InstanceApplicationProfileResponse&gt;**](EdfiAdminApiEdfiAdminV1InstanceApplicationProfileResponse.md) | Applications | [optional] [readonly] [default to undefined]
**relatedInstances** | [**Array&lt;EdfiAdminApiEdfiAdminV1RelatedInstance&gt;**](EdfiAdminApiEdfiAdminV1RelatedInstance.md) |  | [optional] [readonly] [default to undefined]
**enableAdminApi** | **boolean** | Enable Admin API | [optional] [default to undefined]
**state** | **string** |  | [optional] [default to undefined]
**requiresSchoolYearSelection** | **boolean** |  | [optional] [default to undefined]

## Example

```typescript
import { EdfiAdminApiEdfiAdminV1Instance } from '@edgraph-oss/platform-client';

const instance: EdfiAdminApiEdfiAdminV1Instance = {
    id,
    instanceName,
    useCustomId,
    customId,
    description,
    connectionName,
    selectedConnectionId,
    selectedConnection,
    databases,
    password,
    apiClientKey,
    apiClientSecret,
    isApiClientSecretSecured,
    tenantId,
    createdBy,
    createdDateTime,
    isDeleted,
    lastModifiedBy,
    lastModifiedDateTime,
    apiAuthUrl,
    apiResourcesUrls,
    apiCompositesUrls,
    selectedConnectionType,
    isDefault,
    provider,
    onboarding,
    applications,
    relatedInstances,
    enableAdminApi,
    state,
    requiresSchoolYearSelection,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
