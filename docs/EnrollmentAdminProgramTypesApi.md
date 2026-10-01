# EnrollmentAdminProgramTypesApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getProgramTypeById**](#getprogramtypebyid) | **GET** /tenants/{tenantId}/enrollmentadmin/programtypes/{id} | Gets a program type by its record id.|
|[**getProgramTypes**](#getprogramtypes) | **GET** /tenants/{tenantId}/enrollmentadmin/programtypes | Lists the tenant\&#39;s program types, sorted by name. Unpaged: a district has a handful. A  program\&#39;s &#x60;programType.programTypeId&#x60; is one of these ids, and the programs search  filters on it (&#x60;programTypeId&#x60;).|

# **getProgramTypeById**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramTypeResponseDto getProgramTypeById()


### Example

```typescript
import {
    EnrollmentAdminProgramTypesApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminProgramTypesApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)

const { status, data } = await apiInstance.getProgramTypeById(
    tenantId,
    id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **tenantId** | [**string**] |  | defaults to undefined|
| **id** | [**string**] |  | defaults to undefined|


### Return type

**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramTypeResponseDto**

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
|**404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getProgramTypes**
> Array<EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramTypeResponseDto> getProgramTypes()


### Example

```typescript
import {
    EnrollmentAdminProgramTypesApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminProgramTypesApi(configuration);

let tenantId: string; // (default to undefined)

const { status, data } = await apiInstance.getProgramTypes(
    tenantId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **tenantId** | [**string**] |  | defaults to undefined|


### Return type

**Array<EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramTypeResponseDto>**

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

