# EdGraphHttpAggregatorsTenantApiServicesObservationsObservationUserResponse

ObservationAccess is null only when Identity has no ObservationAccessScope bulk result for that user  (e.g. the user has no tenant membership matching the request\'s tenantId).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**userId** | **string** |  | [optional] [default to undefined]
**firstName** | **string** |  | [optional] [default to undefined]
**lastName** | **string** |  | [optional] [default to undefined]
**email** | **string** |  | [optional] [default to undefined]
**status** | **string** |  | [optional] [default to undefined]
**source** | **string** |  | [optional] [default to undefined]
**instructionalInsightsRole** | **string** |  | [optional] [default to undefined]
**seoaas** | [**Array&lt;EdGraphHttpAggregatorsTenantApiServicesObservationsSeoaaResponse&gt;**](EdGraphHttpAggregatorsTenantApiServicesObservationsSeoaaResponse.md) |  | [optional] [default to undefined]
**observationAccess** | [**EdGraphHttpAggregatorsTenantApiServicesObservationsObservationUserAccessResponse**](EdGraphHttpAggregatorsTenantApiServicesObservationsObservationUserAccessResponse.md) |  | [optional] [default to undefined]

## Example

```typescript
import { EdGraphHttpAggregatorsTenantApiServicesObservationsObservationUserResponse } from '@edgraph-oss/platform-client';

const instance: EdGraphHttpAggregatorsTenantApiServicesObservationsObservationUserResponse = {
    userId,
    firstName,
    lastName,
    email,
    status,
    source,
    instructionalInsightsRole,
    seoaas,
    observationAccess,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
