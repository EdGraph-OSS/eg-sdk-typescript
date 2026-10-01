# EnrollmentAdminFeederPatternsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createFeederPattern**](#createfeederpattern) | **POST** /tenants/{tenantId}/enrollmentadmin/feederpatterns | Creates a feeder pattern.|
|[**deleteFeederPattern**](#deletefeederpattern) | **DELETE** /tenants/{tenantId}/enrollmentadmin/feederpatterns/{id} | Soft-deletes a feeder pattern.|
|[**getFeederPatternById**](#getfeederpatternbyid) | **GET** /tenants/{tenantId}/enrollmentadmin/feederpatterns/{id} | Gets a feeder pattern by id.|
|[**getFeederPatterns**](#getfeederpatterns) | **GET** /tenants/{tenantId}/enrollmentadmin/feederpatterns | Searches feeder patterns: which High/Middle/Elementary school code a point falls into.|
|[**updateFeederPattern**](#updatefeederpattern) | **PUT** /tenants/{tenantId}/enrollmentadmin/feederpatterns/{id} | Updates a feeder pattern\&#39;s geometry and properties.|

# **createFeederPattern**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminFeederPatternMutationResultDto createFeederPattern()


### Example

```typescript
import {
    EnrollmentAdminFeederPatternsApi,
    Configuration,
    EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateFeederPatternRequestDto
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminFeederPatternsApi(configuration);

let tenantId: string; // (default to undefined)
let edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateFeederPatternRequestDto: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateFeederPatternRequestDto; // (optional)

const { status, data } = await apiInstance.createFeederPattern(
    tenantId,
    edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateFeederPatternRequestDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateFeederPatternRequestDto** | **EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateFeederPatternRequestDto**|  | |
| **tenantId** | [**string**] |  | defaults to undefined|


### Return type

**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminFeederPatternMutationResultDto**

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json-patch+json, application/json, text/json, application/*+json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthorized |  -  |
|**403** | Forbidden |  -  |
|**500** | Server Error |  -  |
|**201** | The feeder pattern was created. |  -  |
|**400** | Bad Request. The request was invalid and cannot be completed. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteFeederPattern**
> deleteFeederPattern()


### Example

```typescript
import {
    EnrollmentAdminFeederPatternsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminFeederPatternsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)

const { status, data } = await apiInstance.deleteFeederPattern(
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

void (empty response body)

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
|**204** | The feeder pattern was removed. |  -  |
|**404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getFeederPatternById**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminFeederPatternDto getFeederPatternById()


### Example

```typescript
import {
    EnrollmentAdminFeederPatternsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminFeederPatternsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)

const { status, data } = await apiInstance.getFeederPatternById(
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

**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminFeederPatternDto**

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

# **getFeederPatterns**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminFeederPatternDtoPaginatedItemsViewModel getFeederPatterns()


### Example

```typescript
import {
    EnrollmentAdminFeederPatternsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminFeederPatternsApi(configuration);

let tenantId: string; // (default to undefined)
let pageSize: number; // (optional) (default to 50)
let pageIndex: number; // (optional) (default to 0)
let orderBy: string; // (optional) (default to '')
let filter: string; // (optional) (default to '')
let search: string; //Free-text match on feederPattern/highSchool/middleSchool/elementary. (optional) (default to '')

const { status, data } = await apiInstance.getFeederPatterns(
    tenantId,
    pageSize,
    pageIndex,
    orderBy,
    filter,
    search
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **tenantId** | [**string**] |  | defaults to undefined|
| **pageSize** | [**number**] |  | (optional) defaults to 50|
| **pageIndex** | [**number**] |  | (optional) defaults to 0|
| **orderBy** | [**string**] |  | (optional) defaults to ''|
| **filter** | [**string**] |  | (optional) defaults to ''|
| **search** | [**string**] | Free-text match on feederPattern/highSchool/middleSchool/elementary. | (optional) defaults to ''|


### Return type

**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminFeederPatternDtoPaginatedItemsViewModel**

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

# **updateFeederPattern**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminFeederPatternMutationResultDto updateFeederPattern()


### Example

```typescript
import {
    EnrollmentAdminFeederPatternsApi,
    Configuration,
    EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateFeederPatternRequestDto
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminFeederPatternsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)
let edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateFeederPatternRequestDto: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateFeederPatternRequestDto; // (optional)

const { status, data } = await apiInstance.updateFeederPattern(
    tenantId,
    id,
    edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateFeederPatternRequestDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateFeederPatternRequestDto** | **EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateFeederPatternRequestDto**|  | |
| **tenantId** | [**string**] |  | defaults to undefined|
| **id** | [**string**] |  | defaults to undefined|


### Return type

**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminFeederPatternMutationResultDto**

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json-patch+json, application/json, text/json, application/*+json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthorized |  -  |
|**403** | Forbidden |  -  |
|**500** | Server Error |  -  |
|**200** | The feeder pattern was updated. |  -  |
|**400** | Bad Request. The request was invalid and cannot be completed. |  -  |
|**404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

