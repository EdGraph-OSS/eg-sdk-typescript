# EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateSchoolRequestDto

The body of a full school replace by id (not keyed on ExternalDataSourceSchoolId).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Must match the id in the route. | [optional] [default to undefined]
**tenantId** | **string** | Must match the tenant in the route. | [optional] [default to undefined]
**externalDataSourceSchoolId** | **string** |  | [optional] [default to undefined]
**schoolStateShortCode** | **string** | Required. | [optional] [default to undefined]
**schoolName** | **string** | Required. | [optional] [default to undefined]
**districtStateShortCode** | **string** |  | [optional] [default to undefined]
**schoolStateLongCode** | **string** |  | [optional] [default to undefined]
**schoolLocalCode** | **string** |  | [optional] [default to undefined]
**districtLocalCode** | **string** |  | [optional] [default to undefined]
**districtStateCode** | **string** |  | [optional] [default to undefined]
**districtName** | **string** |  | [optional] [default to undefined]
**gradesServed** | **Array&lt;string&gt;** |  | [optional] [default to undefined]
**address** | **string** |  | [optional] [default to undefined]
**lat** | **number** |  | [optional] [default to undefined]
**lon** | **number** |  | [optional] [default to undefined]
**phone** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateSchoolRequestDto } from '@edgraph-oss/platform-client';

const instance: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateSchoolRequestDto = {
    id,
    tenantId,
    externalDataSourceSchoolId,
    schoolStateShortCode,
    schoolName,
    districtStateShortCode,
    schoolStateLongCode,
    schoolLocalCode,
    districtLocalCode,
    districtStateCode,
    districtName,
    gradesServed,
    address,
    lat,
    lon,
    phone,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
