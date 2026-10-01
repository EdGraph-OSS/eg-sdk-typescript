# InstancesApplicationsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createApplicationAsync**](#createapplicationasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications | Creates an Application.|
|[**createApplicationUserAccessAsync**](#createapplicationuseraccessasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId}/access | Creates a new application access.|
|[**deleteApplicationAsync**](#deleteapplicationasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId} | Deletes an Application.|
|[**deleteApplicationUserAccessAsync**](#deleteapplicationuseraccessasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId}/access/{accessId} | Deletes an application user access.|
|[**getApplicationAccessAsync**](#getapplicationaccessasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId}/access | Retrieves a list of application accesses.|
|[**getApplicationAccessByIdAsync**](#getapplicationaccessbyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId}/access/{accessId} | Retrieves an application access by ID.|
|[**getApplicationApiClientByIdAsync**](#getapplicationapiclientbyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId} | Retrieves an API Client of an Application by ID.|
|[**getApplicationApiClientsAsync**](#getapplicationapiclientsasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients | Retrieves the API Clients of an Application.|
|[**getApplicationByIdAsync**](#getapplicationbyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId} | Retrieves an Application by ID.|
|[**getApplicationsAsync**](#getapplicationsasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications | Retrieves a list of Applications.|
|[**regenerateApiClientSecretAsync**](#regenerateapiclientsecretasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId}/regenerate | Regenerates the secret of an API Client.|
|[**regenerateApplicationApiClientCredentials**](#regenerateapplicationapiclientcredentials) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/regenerate | Regenerates an application\&#39;s API Client Credentials|
|[**syncApplicationAsync**](#syncapplicationasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/sync | Copies an Application from one instance to another/other instance(s)|
|[**updateApplicationAsync**](#updateapplicationasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId} | Updates an Application.|
|[**updateApplicationUserAccessAsync**](#updateapplicationuseraccessasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId}/access/{accessId} | Updates a new application access.|

# **createApplicationAsync**
> EdfiAdminApiEdfiAdminV1EdFiApplicationCreatedResponse createApplicationAsync()


### Example

```typescript
import {
    InstancesApplicationsApi,
    Configuration,
    EdfiAdminApiEdfiAdminV1CreateEdFiApplicationRequest
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new InstancesApplicationsApi(configuration);

let tenantId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let edfiAdminApiEdfiAdminV1CreateEdFiApplicationRequest: EdfiAdminApiEdfiAdminV1CreateEdFiApplicationRequest; // (optional)

const { status, data } = await apiInstance.createApplicationAsync(
    tenantId,
    instanceId,
    edfiAdminApiEdfiAdminV1CreateEdFiApplicationRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **edfiAdminApiEdfiAdminV1CreateEdFiApplicationRequest** | **EdfiAdminApiEdfiAdminV1CreateEdFiApplicationRequest**|  | |
| **tenantId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|


### Return type

**EdfiAdminApiEdfiAdminV1EdFiApplicationCreatedResponse**

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json-patch+json, application/json, text/json, application/*+json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthorized. The request requires authentication. The OAuth bearer token was either not provided or is invalid. The operation may succeed once authentication has been successfully completed. |  -  |
|**403** | Forbidden. The request cannot be completed in the current authorization context. Contact your administrator if you believe this operation should be allowed. |  -  |
|**500** | An unhandled error occurred on the server.See the response body for details. |  -  |
|**201** | The resource was created. The location of the resource is available in the Location header of the response. |  -  |
|**400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
|**404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createApplicationUserAccessAsync**
> createApplicationUserAccessAsync()


### Example

```typescript
import {
    InstancesApplicationsApi,
    Configuration,
    EdFiAdminApiApplicationAccessV1CreateApplicationAccessRequest
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new InstancesApplicationsApi(configuration);

let tenantId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let applicationId: string; // (default to undefined)
let apiClientId: string; // (default to undefined)
let edFiAdminApiApplicationAccessV1CreateApplicationAccessRequest: EdFiAdminApiApplicationAccessV1CreateApplicationAccessRequest; // (optional)

const { status, data } = await apiInstance.createApplicationUserAccessAsync(
    tenantId,
    instanceId,
    applicationId,
    apiClientId,
    edFiAdminApiApplicationAccessV1CreateApplicationAccessRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **edFiAdminApiApplicationAccessV1CreateApplicationAccessRequest** | **EdFiAdminApiApplicationAccessV1CreateApplicationAccessRequest**|  | |
| **tenantId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|
| **applicationId** | [**string**] |  | defaults to undefined|
| **apiClientId** | [**string**] |  | defaults to undefined|


### Return type

void (empty response body)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json-patch+json, application/json, text/json, application/*+json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthorized. The request requires authentication. The OAuth bearer token was either not provided or is invalid. The operation may succeed once authentication has been successfully completed. |  -  |
|**403** | Forbidden. The request cannot be completed in the current authorization context. Contact your administrator if you believe this operation should be allowed. |  -  |
|**500** | An unhandled error occurred on the server.See the response body for details. |  -  |
|**200** | Success |  -  |
|**400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
|**201** | The resource was created. The location of the resource is available in the Location header of the response. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteApplicationAsync**
> deleteApplicationAsync()


### Example

```typescript
import {
    InstancesApplicationsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new InstancesApplicationsApi(configuration);

let tenantId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let applicationId: number; // (default to undefined)

const { status, data } = await apiInstance.deleteApplicationAsync(
    tenantId,
    instanceId,
    applicationId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **tenantId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|
| **applicationId** | [**number**] |  | defaults to undefined|


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
|**401** | Unauthorized. The request requires authentication. The OAuth bearer token was either not provided or is invalid. The operation may succeed once authentication has been successfully completed. |  -  |
|**403** | Forbidden. The request cannot be completed in the current authorization context. Contact your administrator if you believe this operation should be allowed. |  -  |
|**500** | An unhandled error occurred on the server.See the response body for details. |  -  |
|**204** | The resource was successfully deleted. |  -  |
|**400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
|**404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteApplicationUserAccessAsync**
> deleteApplicationUserAccessAsync()


### Example

```typescript
import {
    InstancesApplicationsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new InstancesApplicationsApi(configuration);

let tenantId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let applicationId: string; // (default to undefined)
let apiClientId: string; // (default to undefined)
let accessId: string; // (default to undefined)

const { status, data } = await apiInstance.deleteApplicationUserAccessAsync(
    tenantId,
    instanceId,
    applicationId,
    apiClientId,
    accessId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **tenantId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|
| **applicationId** | [**string**] |  | defaults to undefined|
| **apiClientId** | [**string**] |  | defaults to undefined|
| **accessId** | [**string**] |  | defaults to undefined|


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
|**401** | Unauthorized. The request requires authentication. The OAuth bearer token was either not provided or is invalid. The operation may succeed once authentication has been successfully completed. |  -  |
|**403** | Forbidden. The request cannot be completed in the current authorization context. Contact your administrator if you believe this operation should be allowed. |  -  |
|**500** | An unhandled error occurred on the server.See the response body for details. |  -  |
|**204** | The resource was successfully deleted. |  -  |
|**400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
|**404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getApplicationAccessAsync**
> EdFiAdminApiApplicationAccessV1ApplicationAccessResponsePaginatedItemsViewModel getApplicationAccessAsync()


### Example

```typescript
import {
    InstancesApplicationsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new InstancesApplicationsApi(configuration);

let tenantId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let applicationId: string; // (default to undefined)
let apiClientId: string; // (default to undefined)
let pageSize: number; // (optional) (default to 10)
let pageIndex: number; // (optional) (default to 0)
let orderBy: string; // (optional) (default to '')
let filter: string; // (optional) (default to '')

const { status, data } = await apiInstance.getApplicationAccessAsync(
    tenantId,
    instanceId,
    applicationId,
    apiClientId,
    pageSize,
    pageIndex,
    orderBy,
    filter
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **tenantId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|
| **applicationId** | [**string**] |  | defaults to undefined|
| **apiClientId** | [**string**] |  | defaults to undefined|
| **pageSize** | [**number**] |  | (optional) defaults to 10|
| **pageIndex** | [**number**] |  | (optional) defaults to 0|
| **orderBy** | [**string**] |  | (optional) defaults to ''|
| **filter** | [**string**] |  | (optional) defaults to ''|


### Return type

**EdFiAdminApiApplicationAccessV1ApplicationAccessResponsePaginatedItemsViewModel**

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthorized. The request requires authentication. The OAuth bearer token was either not provided or is invalid. The operation may succeed once authentication has been successfully completed. |  -  |
|**403** | Forbidden. The request cannot be completed in the current authorization context. Contact your administrator if you believe this operation should be allowed. |  -  |
|**500** | An unhandled error occurred on the server.See the response body for details. |  -  |
|**200** | The requested resource was successfully retrieved. |  -  |
|**400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getApplicationAccessByIdAsync**
> EdFiAdminApiApplicationAccessV1ApplicationAccessResponse getApplicationAccessByIdAsync()


### Example

```typescript
import {
    InstancesApplicationsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new InstancesApplicationsApi(configuration);

let tenantId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let applicationId: number; // (default to undefined)
let apiClientId: number; // (default to undefined)
let accessId: string; // (default to undefined)

const { status, data } = await apiInstance.getApplicationAccessByIdAsync(
    tenantId,
    instanceId,
    applicationId,
    apiClientId,
    accessId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **tenantId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|
| **applicationId** | [**number**] |  | defaults to undefined|
| **apiClientId** | [**number**] |  | defaults to undefined|
| **accessId** | [**string**] |  | defaults to undefined|


### Return type

**EdFiAdminApiApplicationAccessV1ApplicationAccessResponse**

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthorized. The request requires authentication. The OAuth bearer token was either not provided or is invalid. The operation may succeed once authentication has been successfully completed. |  -  |
|**403** | Forbidden. The request cannot be completed in the current authorization context. Contact your administrator if you believe this operation should be allowed. |  -  |
|**500** | An unhandled error occurred on the server.See the response body for details. |  -  |
|**200** | The requested resource was successfully retrieved. |  -  |
|**400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
|**404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getApplicationApiClientByIdAsync**
> EdfiAdminApiEdfiAdminV1EdFiApplicationApiClientProfileResponse getApplicationApiClientByIdAsync()


### Example

```typescript
import {
    InstancesApplicationsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new InstancesApplicationsApi(configuration);

let tenantId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let applicationId: string; // (default to undefined)
let apiClientId: number; // (default to undefined)

const { status, data } = await apiInstance.getApplicationApiClientByIdAsync(
    tenantId,
    instanceId,
    applicationId,
    apiClientId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **tenantId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|
| **applicationId** | [**string**] |  | defaults to undefined|
| **apiClientId** | [**number**] |  | defaults to undefined|


### Return type

**EdfiAdminApiEdfiAdminV1EdFiApplicationApiClientProfileResponse**

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthorized. The request requires authentication. The OAuth bearer token was either not provided or is invalid. The operation may succeed once authentication has been successfully completed. |  -  |
|**403** | Forbidden. The request cannot be completed in the current authorization context. Contact your administrator if you believe this operation should be allowed. |  -  |
|**500** | An unhandled error occurred on the server.See the response body for details. |  -  |
|**200** | The requested resource was successfully retrieved. |  -  |
|**400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
|**404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getApplicationApiClientsAsync**
> EdfiAdminApiEdfiAdminV1EdFiApplicationApiClientProfileResponsePaginatedItemsViewModel getApplicationApiClientsAsync()


### Example

```typescript
import {
    InstancesApplicationsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new InstancesApplicationsApi(configuration);

let tenantId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let applicationId: string; // (default to undefined)

const { status, data } = await apiInstance.getApplicationApiClientsAsync(
    tenantId,
    instanceId,
    applicationId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **tenantId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|
| **applicationId** | [**string**] |  | defaults to undefined|


### Return type

**EdfiAdminApiEdfiAdminV1EdFiApplicationApiClientProfileResponsePaginatedItemsViewModel**

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthorized. The request requires authentication. The OAuth bearer token was either not provided or is invalid. The operation may succeed once authentication has been successfully completed. |  -  |
|**403** | Forbidden. The request cannot be completed in the current authorization context. Contact your administrator if you believe this operation should be allowed. |  -  |
|**500** | An unhandled error occurred on the server.See the response body for details. |  -  |
|**200** | The requested resource was successfully retrieved. |  -  |
|**400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
|**404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getApplicationByIdAsync**
> EdfiAdminApiEdfiAdminV1EdFiApplicationProfileResponse getApplicationByIdAsync()


### Example

```typescript
import {
    InstancesApplicationsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new InstancesApplicationsApi(configuration);

let tenantId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let applicationId: number; // (default to undefined)
let loadEducationOrganizations: boolean; // (optional) (default to undefined)

const { status, data } = await apiInstance.getApplicationByIdAsync(
    tenantId,
    instanceId,
    applicationId,
    loadEducationOrganizations
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **tenantId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|
| **applicationId** | [**number**] |  | defaults to undefined|
| **loadEducationOrganizations** | [**boolean**] |  | (optional) defaults to undefined|


### Return type

**EdfiAdminApiEdfiAdminV1EdFiApplicationProfileResponse**

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthorized. The request requires authentication. The OAuth bearer token was either not provided or is invalid. The operation may succeed once authentication has been successfully completed. |  -  |
|**403** | Forbidden. The request cannot be completed in the current authorization context. Contact your administrator if you believe this operation should be allowed. |  -  |
|**500** | An unhandled error occurred on the server.See the response body for details. |  -  |
|**200** | The requested resource was successfully retrieved. |  -  |
|**400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
|**404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getApplicationsAsync**
> EdfiAdminApiEdfiAdminV1EdFiApplicationListResponsePaginatedItemsViewModel getApplicationsAsync()


### Example

```typescript
import {
    InstancesApplicationsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new InstancesApplicationsApi(configuration);

let tenantId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let pageSize: number; // (optional) (default to 10)
let pageIndex: number; // (optional) (default to 0)
let orderBy: string; // (optional) (default to '')
let filter: string; // (optional) (default to '')

const { status, data } = await apiInstance.getApplicationsAsync(
    tenantId,
    instanceId,
    pageSize,
    pageIndex,
    orderBy,
    filter
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **tenantId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|
| **pageSize** | [**number**] |  | (optional) defaults to 10|
| **pageIndex** | [**number**] |  | (optional) defaults to 0|
| **orderBy** | [**string**] |  | (optional) defaults to ''|
| **filter** | [**string**] |  | (optional) defaults to ''|


### Return type

**EdfiAdminApiEdfiAdminV1EdFiApplicationListResponsePaginatedItemsViewModel**

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthorized. The request requires authentication. The OAuth bearer token was either not provided or is invalid. The operation may succeed once authentication has been successfully completed. |  -  |
|**403** | Forbidden. The request cannot be completed in the current authorization context. Contact your administrator if you believe this operation should be allowed. |  -  |
|**500** | An unhandled error occurred on the server.See the response body for details. |  -  |
|**200** | The requested resource was successfully retrieved. |  -  |
|**400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
|**404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **regenerateApiClientSecretAsync**
> EdfiAdminApiEdfiAdminV1RegenerateApiClientSecretResponse regenerateApiClientSecretAsync()


### Example

```typescript
import {
    InstancesApplicationsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new InstancesApplicationsApi(configuration);

let tenantId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let applicationId: number; // (default to undefined)
let apiClientId: number; // (default to undefined)

const { status, data } = await apiInstance.regenerateApiClientSecretAsync(
    tenantId,
    instanceId,
    applicationId,
    apiClientId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **tenantId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|
| **applicationId** | [**number**] |  | defaults to undefined|
| **apiClientId** | [**number**] |  | defaults to undefined|


### Return type

**EdfiAdminApiEdfiAdminV1RegenerateApiClientSecretResponse**

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthorized. The request requires authentication. The OAuth bearer token was either not provided or is invalid. The operation may succeed once authentication has been successfully completed. |  -  |
|**403** | Forbidden. The request cannot be completed in the current authorization context. Contact your administrator if you believe this operation should be allowed. |  -  |
|**500** | An unhandled error occurred on the server.See the response body for details. |  -  |
|**200** | The requested resource was successfully retrieved. |  -  |
|**400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
|**404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **regenerateApplicationApiClientCredentials**
> EdfiAdminApiEdfiAdminV1RegenerateApiClientSecretResponse regenerateApplicationApiClientCredentials()


### Example

```typescript
import {
    InstancesApplicationsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new InstancesApplicationsApi(configuration);

let tenantId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let applicationId: number; // (default to undefined)

const { status, data } = await apiInstance.regenerateApplicationApiClientCredentials(
    tenantId,
    instanceId,
    applicationId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **tenantId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|
| **applicationId** | [**number**] |  | defaults to undefined|


### Return type

**EdfiAdminApiEdfiAdminV1RegenerateApiClientSecretResponse**

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthorized. The request requires authentication. The OAuth bearer token was either not provided or is invalid. The operation may succeed once authentication has been successfully completed. |  -  |
|**403** | Forbidden. The request cannot be completed in the current authorization context. Contact your administrator if you believe this operation should be allowed. |  -  |
|**500** | An unhandled error occurred on the server.See the response body for details. |  -  |
|**200** | The requested resource was successfully retrieved. |  -  |
|**400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
|**404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **syncApplicationAsync**
> syncApplicationAsync()


### Example

```typescript
import {
    InstancesApplicationsApi,
    Configuration,
    EdfiAdminApiEdfiAdminV1SyncApplicationRequest
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new InstancesApplicationsApi(configuration);

let tenantId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let applicationId: number; // (default to undefined)
let edfiAdminApiEdfiAdminV1SyncApplicationRequest: EdfiAdminApiEdfiAdminV1SyncApplicationRequest; // (optional)

const { status, data } = await apiInstance.syncApplicationAsync(
    tenantId,
    instanceId,
    applicationId,
    edfiAdminApiEdfiAdminV1SyncApplicationRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **edfiAdminApiEdfiAdminV1SyncApplicationRequest** | **EdfiAdminApiEdfiAdminV1SyncApplicationRequest**|  | |
| **tenantId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|
| **applicationId** | [**number**] |  | defaults to undefined|


### Return type

void (empty response body)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json-patch+json, application/json, text/json, application/*+json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthorized. The request requires authentication. The OAuth bearer token was either not provided or is invalid. The operation may succeed once authentication has been successfully completed. |  -  |
|**403** | Forbidden. The request cannot be completed in the current authorization context. Contact your administrator if you believe this operation should be allowed. |  -  |
|**500** | An unhandled error occurred on the server.See the response body for details. |  -  |
|**200** | The requested resource was successfully retrieved. |  -  |
|**400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
|**404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateApplicationAsync**
> updateApplicationAsync()


### Example

```typescript
import {
    InstancesApplicationsApi,
    Configuration,
    EdfiAdminApiEdfiAdminV1UpdateEdFiApplicationRequest
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new InstancesApplicationsApi(configuration);

let tenantId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let applicationId: string; // (default to undefined)
let edfiAdminApiEdfiAdminV1UpdateEdFiApplicationRequest: EdfiAdminApiEdfiAdminV1UpdateEdFiApplicationRequest; // (optional)

const { status, data } = await apiInstance.updateApplicationAsync(
    tenantId,
    instanceId,
    applicationId,
    edfiAdminApiEdfiAdminV1UpdateEdFiApplicationRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **edfiAdminApiEdfiAdminV1UpdateEdFiApplicationRequest** | **EdfiAdminApiEdfiAdminV1UpdateEdFiApplicationRequest**|  | |
| **tenantId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|
| **applicationId** | [**string**] |  | defaults to undefined|


### Return type

void (empty response body)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json-patch+json, application/json, text/json, application/*+json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthorized. The request requires authentication. The OAuth bearer token was either not provided or is invalid. The operation may succeed once authentication has been successfully completed. |  -  |
|**403** | Forbidden. The request cannot be completed in the current authorization context. Contact your administrator if you believe this operation should be allowed. |  -  |
|**500** | An unhandled error occurred on the server.See the response body for details. |  -  |
|**200** | The requested resource was successfully retrieved. |  -  |
|**400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
|**404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateApplicationUserAccessAsync**
> updateApplicationUserAccessAsync()


### Example

```typescript
import {
    InstancesApplicationsApi,
    Configuration,
    EdFiAdminApiApplicationAccessV1UpdateApplicationAccessRequest
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new InstancesApplicationsApi(configuration);

let tenantId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let applicationId: string; // (default to undefined)
let apiClientId: string; // (default to undefined)
let accessId: string; // (default to undefined)
let edFiAdminApiApplicationAccessV1UpdateApplicationAccessRequest: EdFiAdminApiApplicationAccessV1UpdateApplicationAccessRequest; // (optional)

const { status, data } = await apiInstance.updateApplicationUserAccessAsync(
    tenantId,
    instanceId,
    applicationId,
    apiClientId,
    accessId,
    edFiAdminApiApplicationAccessV1UpdateApplicationAccessRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **edFiAdminApiApplicationAccessV1UpdateApplicationAccessRequest** | **EdFiAdminApiApplicationAccessV1UpdateApplicationAccessRequest**|  | |
| **tenantId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|
| **applicationId** | [**string**] |  | defaults to undefined|
| **apiClientId** | [**string**] |  | defaults to undefined|
| **accessId** | [**string**] |  | defaults to undefined|


### Return type

void (empty response body)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json-patch+json, application/json, text/json, application/*+json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthorized. The request requires authentication. The OAuth bearer token was either not provided or is invalid. The operation may succeed once authentication has been successfully completed. |  -  |
|**403** | Forbidden. The request cannot be completed in the current authorization context. Contact your administrator if you believe this operation should be allowed. |  -  |
|**500** | An unhandled error occurred on the server.See the response body for details. |  -  |
|**200** | Success |  -  |
|**400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
|**201** | The resource was created. The location of the resource is available in the Location header of the response. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

