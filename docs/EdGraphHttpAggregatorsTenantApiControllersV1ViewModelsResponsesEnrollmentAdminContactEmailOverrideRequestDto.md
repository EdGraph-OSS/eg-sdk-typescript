# EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactEmailOverrideRequestDto

The body of an override write.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**value** | **string** | The corrected detail. The DELETE route removes an override instead; this is never blank. | [optional] [default to undefined]
**studentLocalCode** | **string** |  | [optional] [default to undefined]
**expectedVersion** | **string** | The &#x60;lastUpdatedDateTime&#x60; the client read, round-tripped back. When it no longer matches the  write is refused with 412 rather than winning because it arrived second. Omit to skip the check. | [optional] [default to undefined]

## Example

```typescript
import { EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactEmailOverrideRequestDto } from '@edgraph-oss/platform-client';

const instance: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactEmailOverrideRequestDto = {
    value,
    studentLocalCode,
    expectedVersion,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
