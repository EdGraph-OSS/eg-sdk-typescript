# EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpsertSchoolRequestDto

The body of a school creation or update.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tenantId** | **string** | Must match the tenant in the route. | [optional] [default to undefined]
**externalDataSourceSchoolId** | **string** | When present, the upsert is keyed on this id rather than SchoolStateShortCode:  a live school with a matching external id is updated; a soft-deleted one is refused (recover it  first). When absent, a new school is always inserted, and a SchoolStateShortCode  collision on insert is rejected as AlreadyExists. | [optional] [default to undefined]
**schoolStateShortCode** | **string** | Required. Unique per tenant. | [optional] [default to undefined]
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
**addressStateAbbreviation** | **string** | Two-letter US state code, e.g. &#x60;TX&#x60;. Required when AddressState is sent. | [optional] [default to undefined]
**addressState** | **string** | Full name of the state in AddressStateAbbreviation, e.g. &#x60;Texas&#x60;. | [optional] [default to undefined]

## Example

```typescript
import { EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpsertSchoolRequestDto } from '@edgraph-oss/platform-client';

const instance: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpsertSchoolRequestDto = {
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
    addressStateAbbreviation,
    addressState,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
