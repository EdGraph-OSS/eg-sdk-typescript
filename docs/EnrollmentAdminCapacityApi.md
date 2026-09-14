# EnrollmentAdminCapacityApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getCapacity**](#getcapacity) | **GET** /tenants/{tenantId}/enrollmentadmin/schools/{schoolCode}/capacity | Searches Capacity for one school - one row per program x grade x school year.|

# **getCapacity**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminCapacityListItemDtoPaginatedItemsViewModel getCapacity()


### Example

```typescript
import {
    EnrollmentAdminCapacityApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminCapacityApi(configuration);

let tenantId: string; // (default to undefined)
let schoolCode: string; //Required - a seat count is meaningless without a school. (default to undefined)
let pageSize: number; // (optional) (default to 50)
let pageIndex: number; // (optional) (default to 0)
let orderBy: string; // (optional) (default to '')
let filter: string; // (optional) (default to '')
let grade: string; //Optional exact match. (optional) (default to '')
let search: string; //Free-text match on program name/code. (optional) (default to '')

const { status, data } = await apiInstance.getCapacity(
    tenantId,
    schoolCode,
    pageSize,
    pageIndex,
    orderBy,
    filter,
    grade,
    search
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **tenantId** | [**string**] |  | defaults to undefined|
| **schoolCode** | [**string**] | Required - a seat count is meaningless without a school. | defaults to undefined|
| **pageSize** | [**number**] |  | (optional) defaults to 50|
| **pageIndex** | [**number**] |  | (optional) defaults to 0|
| **orderBy** | [**string**] |  | (optional) defaults to ''|
| **filter** | [**string**] |  | (optional) defaults to ''|
| **grade** | [**string**] | Optional exact match. | (optional) defaults to ''|
| **search** | [**string**] | Free-text match on program name/code. | (optional) defaults to ''|


### Return type

**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminCapacityListItemDtoPaginatedItemsViewModel**

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthorized |  -  |
|**403** | Forbidden |  -  |
|**500** | Server Error |  -  |
|**200** | The requested resource was successfully retrieved. |  -  |
|**400** | Bad Request. The request was invalid and cannot be completed. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

