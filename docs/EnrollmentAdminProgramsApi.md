# EnrollmentAdminProgramsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createProgram**](#createprogram) | **POST** /tenants/{tenantId}/enrollmentadmin/programs | Creates a Program at a school. The body names the school, the program type and the  requirements by id; the service copies their display fields onto the row.|
|[**deleteProgram**](#deleteprogram) | **DELETE** /tenants/{tenantId}/enrollmentadmin/programs/{id} | Removes a Program (soft delete).|
|[**getProgramApplications**](#getprogramapplications) | **GET** /tenants/{tenantId}/enrollmentadmin/programs/{id}/applications | Gets the Registration Applications referencing a Program.|
|[**getProgramById**](#getprogrambyid) | **GET** /tenants/{tenantId}/enrollmentadmin/programs/{id} | Gets a Program by its record id.|
|[**getPrograms**](#getprograms) | **GET** /tenants/{tenantId}/enrollmentadmin/programs | Searches Programs. Every row is one school\&#39;s offering of a program: the school, the program  type and the requirements are embedded on it, each with its own &#x60;_id&#x60; beside the id of  the row it was copied from.|
|[**updateProgram**](#updateprogram) | **PUT** /tenants/{tenantId}/enrollmentadmin/programs/{id} | Updates a Program. The school a program runs at never changes; everything else, including  the program type and the requirement set, is replaced from the body.|

# **createProgram**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramMutationResultDto createProgram()


### Example

```typescript
import {
    EnrollmentAdminProgramsApi,
    Configuration,
    EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateProgramRequestDto
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminProgramsApi(configuration);

let tenantId: string; // (default to undefined)
let edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateProgramRequestDto: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateProgramRequestDto; // (optional)

const { status, data } = await apiInstance.createProgram(
    tenantId,
    edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateProgramRequestDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateProgramRequestDto** | **EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateProgramRequestDto**|  | |
| **tenantId** | [**string**] |  | defaults to undefined|


### Return type

**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramMutationResultDto**

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
|**201** | The program was created. |  -  |
|**400** | Bad Request. The request was invalid, or named a school, program type or requirement that does not exist. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteProgram**
> deleteProgram()


### Example

```typescript
import {
    EnrollmentAdminProgramsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminProgramsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)

const { status, data } = await apiInstance.deleteProgram(
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
|**204** | The program was removed. |  -  |
|**404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getProgramApplications**
> Array<EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramApplicationDto> getProgramApplications()


### Example

```typescript
import {
    EnrollmentAdminProgramsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminProgramsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)

const { status, data } = await apiInstance.getProgramApplications(
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

**Array<EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramApplicationDto>**

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

# **getProgramById**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramDetailDto getProgramById()


### Example

```typescript
import {
    EnrollmentAdminProgramsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminProgramsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)

const { status, data } = await apiInstance.getProgramById(
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

**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramDetailDto**

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

# **getPrograms**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramListItemDtoPaginatedItemsViewModel getPrograms()


### Example

```typescript
import {
    EnrollmentAdminProgramsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminProgramsApi(configuration);

let tenantId: string; // (default to undefined)
let pageSize: number; // (optional) (default to 50)
let pageIndex: number; // (optional) (default to 0)
let orderBy: string; // (optional) (default to '')
let filter: string; // (optional) (default to '')
let search: string; //Free-text match on program name/code. (optional) (default to '')
let schoolLocalCode: string; //Narrows to programs offered at this school. Not a security boundary. (optional) (default to '')
let programTypeId: string; //Narrows to programs of this program type (its record id). (optional) (default to '')

const { status, data } = await apiInstance.getPrograms(
    tenantId,
    pageSize,
    pageIndex,
    orderBy,
    filter,
    search,
    schoolLocalCode,
    programTypeId
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
| **search** | [**string**] | Free-text match on program name/code. | (optional) defaults to ''|
| **schoolLocalCode** | [**string**] | Narrows to programs offered at this school. Not a security boundary. | (optional) defaults to ''|
| **programTypeId** | [**string**] | Narrows to programs of this program type (its record id). | (optional) defaults to ''|


### Return type

**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramListItemDtoPaginatedItemsViewModel**

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

# **updateProgram**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramMutationResultDto updateProgram()


### Example

```typescript
import {
    EnrollmentAdminProgramsApi,
    Configuration,
    EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateProgramRequestDto
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminProgramsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)
let edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateProgramRequestDto: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateProgramRequestDto; // (optional)

const { status, data } = await apiInstance.updateProgram(
    tenantId,
    id,
    edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateProgramRequestDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateProgramRequestDto** | **EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateProgramRequestDto**|  | |
| **tenantId** | [**string**] |  | defaults to undefined|
| **id** | [**string**] |  | defaults to undefined|


### Return type

**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramMutationResultDto**

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
|**200** | The program was updated. |  -  |
|**400** | Bad Request. The request was invalid and cannot be completed. |  -  |
|**404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

