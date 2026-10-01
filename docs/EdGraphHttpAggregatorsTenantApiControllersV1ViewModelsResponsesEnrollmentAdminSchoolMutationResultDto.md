# EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolMutationResultDto

Created is true only for an upsert that inserted a new school; it drives the              controller\'s 201-vs-200 split. An update result always reports false.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional] [default to undefined]
**tenantId** | **string** |  | [optional] [default to undefined]
**created** | **boolean** |  | [optional] [default to undefined]

## Example

```typescript
import { EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolMutationResultDto } from '@edgraph-oss/platform-client';

const instance: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolMutationResultDto = {
    id,
    tenantId,
    created,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
