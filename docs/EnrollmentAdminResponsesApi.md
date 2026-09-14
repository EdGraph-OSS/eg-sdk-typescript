# EnrollmentAdminResponsesApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getEnrollmentApplicationResponse**](#getenrollmentapplicationresponse) | **GET** /tenants/{tenantId}/enrollmentadmin/responses/{responseId} | Gets an Enrollment Application Response.|
|[**getEnrollmentApplicationResponses**](#getenrollmentapplicationresponses) | **GET** /tenants/{tenantId}/enrollmentadmin/responses | Searches Enrollment Application Responses.|

# **getEnrollmentApplicationResponse**
> EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponseResponse getEnrollmentApplicationResponse()


### Example

```typescript
import {
    EnrollmentAdminResponsesApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminResponsesApi(configuration);

let tenantId: string; // (default to undefined)
let responseId: string; // (default to undefined)

const { status, data } = await apiInstance.getEnrollmentApplicationResponse(
    tenantId,
    responseId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **tenantId** | [**string**] |  | defaults to undefined|
| **responseId** | [**string**] |  | defaults to undefined|


### Return type

**EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponseResponse**

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

# **getEnrollmentApplicationResponses**
> EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponsesSearchResponse getEnrollmentApplicationResponses()


### Example

```typescript
import {
    EnrollmentAdminResponsesApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminResponsesApi(configuration);

let tenantId: string; // (default to undefined)
let pageIndex: number; // (optional) (default to undefined)
let pageSize: number; // (optional) (default to undefined)
let filter: string; // (optional) (default to undefined)
let orderBy: string; // (optional) (default to undefined)

const { status, data } = await apiInstance.getEnrollmentApplicationResponses(
    tenantId,
    pageIndex,
    pageSize,
    filter,
    orderBy
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **tenantId** | [**string**] |  | defaults to undefined|
| **pageIndex** | [**number**] |  | (optional) defaults to undefined|
| **pageSize** | [**number**] |  | (optional) defaults to undefined|
| **filter** | [**string**] |  | (optional) defaults to undefined|
| **orderBy** | [**string**] |  | (optional) defaults to undefined|


### Return type

**EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponsesSearchResponse**

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

