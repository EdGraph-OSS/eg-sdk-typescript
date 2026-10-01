# EnrollmentAdminSchoolsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**deleteEnrollmentSchool**](#deleteenrollmentschool) | **DELETE** /tenants/{tenantId}/enrollmentadmin/schools/{id} | Deletes an Enrollment School.|
|[**disableEnrollmentSchool**](#disableenrollmentschool) | **PUT** /tenants/{tenantId}/enrollmentadmin/schools/{id}/disable | Disables an Enrollment School.|
|[**enableEnrollmentSchool**](#enableenrollmentschool) | **PUT** /tenants/{tenantId}/enrollmentadmin/schools/{id}/enable | Enables an Enrollment School.|
|[**getEnrollmentSchoolById**](#getenrollmentschoolbyid) | **GET** /tenants/{tenantId}/enrollmentadmin/schools/{id} | Gets an Enrollment School by its record id, with the programs it runs.|
|[**getEnrollmentSchools**](#getenrollmentschools) | **GET** /tenants/{tenantId}/enrollmentadmin/schools | Searches Enrollment Schools.|
|[**updateEnrollmentSchool**](#updateenrollmentschool) | **PUT** /tenants/{tenantId}/enrollmentadmin/schools/{id} | Replaces an Enrollment School by its record id.|
|[**upsertEnrollmentSchool**](#upsertenrollmentschool) | **POST** /tenants/{tenantId}/enrollmentadmin/schools | Creates or updates an Enrollment School, keyed on &#x60;externalDataSourceSchoolId&#x60;.|

# **deleteEnrollmentSchool**
> deleteEnrollmentSchool()


### Example

```typescript
import {
    EnrollmentAdminSchoolsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminSchoolsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)

const { status, data } = await apiInstance.deleteEnrollmentSchool(
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
|**204** | The resource was successfully deleted. |  -  |
|**404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **disableEnrollmentSchool**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolEnabledResponseDto disableEnrollmentSchool()


### Example

```typescript
import {
    EnrollmentAdminSchoolsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminSchoolsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)

const { status, data } = await apiInstance.disableEnrollmentSchool(
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

**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolEnabledResponseDto**

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
|**200** | The resource was successfully updated. |  -  |
|**404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **enableEnrollmentSchool**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolEnabledResponseDto enableEnrollmentSchool()


### Example

```typescript
import {
    EnrollmentAdminSchoolsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminSchoolsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)

const { status, data } = await apiInstance.enableEnrollmentSchool(
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

**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolEnabledResponseDto**

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
|**200** | The resource was successfully updated. |  -  |
|**404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getEnrollmentSchoolById**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolResponseDto getEnrollmentSchoolById()


### Example

```typescript
import {
    EnrollmentAdminSchoolsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminSchoolsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)

const { status, data } = await apiInstance.getEnrollmentSchoolById(
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

**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolResponseDto**

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

# **getEnrollmentSchools**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolListItemResponseDtoPaginatedItemsViewModel getEnrollmentSchools()


### Example

```typescript
import {
    EnrollmentAdminSchoolsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminSchoolsApi(configuration);

let tenantId: string; // (default to undefined)
let pageSize: number; // (optional) (default to 50)
let pageIndex: number; // (optional) (default to 0)
let orderBy: string; // (optional) (default to '')
let filter: string; // (optional) (default to '')
let search: string; //Free-text match on school name or school code. (optional) (default to '')

const { status, data } = await apiInstance.getEnrollmentSchools(
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
| **search** | [**string**] | Free-text match on school name or school code. | (optional) defaults to ''|


### Return type

**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolListItemResponseDtoPaginatedItemsViewModel**

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

# **updateEnrollmentSchool**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolMutationResultDto updateEnrollmentSchool()

Full replace, not keyed on `externalDataSourceSchoolId` - use the id in the route.  `isEnabled` is never moved by this call - use `PUT .../schools/{id}/enable` or  `.../disable` instead.

### Example

```typescript
import {
    EnrollmentAdminSchoolsApi,
    Configuration,
    EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateSchoolRequestDto
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminSchoolsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)
let edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateSchoolRequestDto: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateSchoolRequestDto; // (optional)

const { status, data } = await apiInstance.updateEnrollmentSchool(
    tenantId,
    id,
    edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateSchoolRequestDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateSchoolRequestDto** | **EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateSchoolRequestDto**|  | |
| **tenantId** | [**string**] |  | defaults to undefined|
| **id** | [**string**] |  | defaults to undefined|


### Return type

**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolMutationResultDto**

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
|**200** | The school was updated. |  -  |
|**400** | Bad Request. The request was invalid and cannot be completed. |  -  |
|**404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **upsertEnrollmentSchool**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolMutationResultDto upsertEnrollmentSchool()

Upsert semantics: when `externalDataSourceSchoolId` is present and matches a live school  in the tenant, that school is updated - every field, including `schoolStateShortCode`, is  overwritten. A soft-deleted match is refused (recover it first). Otherwise a new school is  always inserted, keeping the external id if one was given; a `schoolStateShortCode`  collision on insert is rejected as AlreadyExists (409) rather than overwriting the existing  school - a POST with no external id no longer overwrites by code. `isEnabled` is never  moved by this call - use `PUT .../schools/{id}/enable` or `.../disable` instead.

### Example

```typescript
import {
    EnrollmentAdminSchoolsApi,
    Configuration,
    EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpsertSchoolRequestDto
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminSchoolsApi(configuration);

let tenantId: string; // (default to undefined)
let edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpsertSchoolRequestDto: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpsertSchoolRequestDto; // (optional)

const { status, data } = await apiInstance.upsertEnrollmentSchool(
    tenantId,
    edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpsertSchoolRequestDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpsertSchoolRequestDto** | **EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpsertSchoolRequestDto**|  | |
| **tenantId** | [**string**] |  | defaults to undefined|


### Return type

**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolMutationResultDto**

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
|**201** | A new school was created. |  -  |
|**200** | An existing school (matched by external id) was updated. |  -  |
|**400** | Bad Request. The request was invalid and cannot be completed. |  -  |
|**409** | A school with this &#x60;schoolStateShortCode&#x60; already exists. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

