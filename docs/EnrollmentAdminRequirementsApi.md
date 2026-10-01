# EnrollmentAdminRequirementsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createRequirement**](#createrequirement) | **POST** /tenants/{tenantId}/enrollmentadmin/requirements | Creates a requirement. Leave &#x60;isRequired&#x60; out to create a required one. A &#x60;url&#x60;  requirement needs &#x60;url&#x60;, an absolute http or https link.|
|[**deleteRequirement**](#deleterequirement) | **DELETE** /tenants/{tenantId}/enrollmentadmin/requirements/{id} | Removes a requirement (soft delete). Programs that embed it keep their copy.|
|[**getRequirementById**](#getrequirementbyid) | **GET** /tenants/{tenantId}/enrollmentadmin/requirements/{id} | Gets a requirement by its record id.|
|[**getRequirements**](#getrequirements) | **GET** /tenants/{tenantId}/enrollmentadmin/requirements | Lists the tenant\&#39;s requirements, sorted by code. Unpaged. A program names the ones it asks  for by id (&#x60;requirementIds&#x60;) and embeds a copy of each, taken when the program is saved.|
|[**updateRequirement**](#updaterequirement) | **PUT** /tenants/{tenantId}/enrollmentadmin/requirements/{id} | Updates a requirement. Every field is replaced except &#x60;isRequired&#x60;, which keeps the  stored value when left out; &#x60;isUploadEnabled&#x60; must be sent. Programs keep the copy  taken when they were last saved, so a change shows on a program only after it is re-saved.|

# **createRequirement**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminRequirementMutationResultDto createRequirement()


### Example

```typescript
import {
    EnrollmentAdminRequirementsApi,
    Configuration,
    EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateRequirementRequestDto
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminRequirementsApi(configuration);

let tenantId: string; // (default to undefined)
let edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateRequirementRequestDto: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateRequirementRequestDto; // (optional)

const { status, data } = await apiInstance.createRequirement(
    tenantId,
    edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateRequirementRequestDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateRequirementRequestDto** | **EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateRequirementRequestDto**|  | |
| **tenantId** | [**string**] |  | defaults to undefined|


### Return type

**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminRequirementMutationResultDto**

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
|**201** | The requirement was created. |  -  |
|**400** | Bad Request. The request was invalid and cannot be completed. |  -  |
|**409** | A requirement with this code already exists in the tenant (deleted ones included). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteRequirement**
> deleteRequirement()


### Example

```typescript
import {
    EnrollmentAdminRequirementsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminRequirementsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)

const { status, data } = await apiInstance.deleteRequirement(
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
|**204** | The requirement was removed. |  -  |
|**404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getRequirementById**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminRequirementResponseDto getRequirementById()


### Example

```typescript
import {
    EnrollmentAdminRequirementsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminRequirementsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)

const { status, data } = await apiInstance.getRequirementById(
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

**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminRequirementResponseDto**

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

# **getRequirements**
> Array<EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminRequirementResponseDto> getRequirements()


### Example

```typescript
import {
    EnrollmentAdminRequirementsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminRequirementsApi(configuration);

let tenantId: string; // (default to undefined)

const { status, data } = await apiInstance.getRequirements(
    tenantId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **tenantId** | [**string**] |  | defaults to undefined|


### Return type

**Array<EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminRequirementResponseDto>**

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

# **updateRequirement**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminRequirementMutationResultDto updateRequirement()


### Example

```typescript
import {
    EnrollmentAdminRequirementsApi,
    Configuration,
    EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateRequirementRequestDto
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminRequirementsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)
let edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateRequirementRequestDto: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateRequirementRequestDto; // (optional)

const { status, data } = await apiInstance.updateRequirement(
    tenantId,
    id,
    edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateRequirementRequestDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateRequirementRequestDto** | **EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateRequirementRequestDto**|  | |
| **tenantId** | [**string**] |  | defaults to undefined|
| **id** | [**string**] |  | defaults to undefined|


### Return type

**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminRequirementMutationResultDto**

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
|**200** | The requirement was updated. |  -  |
|**400** | Bad Request. The request was invalid and cannot be completed. |  -  |
|**404** | The resource could not be found. |  -  |
|**409** | Another requirement in the tenant already has this code. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

