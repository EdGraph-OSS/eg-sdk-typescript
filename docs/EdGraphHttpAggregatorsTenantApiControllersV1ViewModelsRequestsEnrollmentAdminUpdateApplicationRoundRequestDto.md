# EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateApplicationRoundRequestDto

Replaces label, grades and program types. Code and school year are the round\'s identity and  cannot change - duplicate the round into another school year instead.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional] [default to undefined]
**tenantId** | **string** |  | [optional] [default to undefined]
**label** | **string** |  | [optional] [default to undefined]
**grades** | **Array&lt;string&gt;** |  | [optional] [default to undefined]
**programTypeIds** | **Array&lt;string&gt;** |  | [optional] [default to undefined]

## Example

```typescript
import { EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateApplicationRoundRequestDto } from '@edgraph-oss/platform-client';

const instance: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateApplicationRoundRequestDto = {
    id,
    tenantId,
    label,
    grades,
    programTypeIds,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
