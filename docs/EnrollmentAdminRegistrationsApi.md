# EnrollmentAdminRegistrationsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**addEnrollmentRegistrationApplication**](#addenrollmentregistrationapplication) | **POST** /tenants/{tenantId}/enrollmentadmin/registrations/{id}/applications | Adds one Program-seat choice to an existing Registration - the standalone counterpart to  passing initial choices at creation time.|
|[**approveEnrollmentRegistration**](#approveenrollmentregistration) | **PUT** /tenants/{tenantId}/enrollmentadmin/registrations/{id}/approve | Approves a Registration - assigns the linked Student and Contacts and flips its status.|
|[**approveEnrollmentRegistrationApplication**](#approveenrollmentregistrationapplication) | **PUT** /tenants/{tenantId}/enrollmentadmin/registrations/{id}/applications/{applicationId}/approve | Approves a single Application on a Registration, independently of its siblings.|
|[**createEnrollmentRegistration**](#createenrollmentregistration) | **POST** /tenants/{tenantId}/enrollmentadmin/registrations | Creates a Registration.|
|[**deleteEnrollmentRegistration**](#deleteenrollmentregistration) | **DELETE** /tenants/{tenantId}/enrollmentadmin/registrations/{id} | Removes a Registration.|
|[**getEnrollmentRegistration**](#getenrollmentregistration) | **GET** /tenants/{tenantId}/enrollmentadmin/registrations/{id} | Gets a Registration by its id.|
|[**getEnrollmentRegistrationApplications**](#getenrollmentregistrationapplications) | **GET** /tenants/{tenantId}/enrollmentadmin/registrations/{id}/applications | Gets a Registration\&#39;s Applications - each a zero-to-many, independently approvable  Program-seat choice.|
|[**getEnrollmentRegistrations**](#getenrollmentregistrations) | **GET** /tenants/{tenantId}/enrollmentadmin/registrations | Searches Registrations - a parent\&#39;s enrollment submission requesting a seat in a School/District  Program.|
|[**rejectEnrollmentRegistration**](#rejectenrollmentregistration) | **PUT** /tenants/{tenantId}/enrollmentadmin/registrations/{id}/reject | Explicitly rejects a Registration - sets its status to Rejected. Terminal, like approve: a  later Update/UpdateScreen/StartOver progress recompute does not revert it.|
|[**submitEnrollmentRegistration**](#submitenrollmentregistration) | **PUT** /tenants/{tenantId}/enrollmentadmin/registrations/{id}/submit | Explicitly submits a Registration - sets its status to Submitted. Terminal, like approve: a  later Update/UpdateScreen/StartOver progress recompute does not revert it.|
|[**updateEnrollmentRegistration**](#updateenrollmentregistration) | **PUT** /tenants/{tenantId}/enrollmentadmin/registrations/{id} | Updates a Registration.|

# **addEnrollmentRegistrationApplication**
> EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse addEnrollmentRegistrationApplication()


### Example

```typescript
import {
    EnrollmentAdminRegistrationsApi,
    Configuration,
    EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminAddRegistrationApplicationRequestDto
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminRegistrationsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)
let edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminAddRegistrationApplicationRequestDto: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminAddRegistrationApplicationRequestDto; // (optional)

const { status, data } = await apiInstance.addEnrollmentRegistrationApplication(
    tenantId,
    id,
    edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminAddRegistrationApplicationRequestDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminAddRegistrationApplicationRequestDto** | **EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminAddRegistrationApplicationRequestDto**|  | |
| **tenantId** | [**string**] |  | defaults to undefined|
| **id** | [**string**] |  | defaults to undefined|


### Return type

**EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse**

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
|**200** | The application was added. |  -  |
|**400** | Bad Request. The request was invalid and cannot be completed. |  -  |
|**404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **approveEnrollmentRegistration**
> EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse approveEnrollmentRegistration()

The `contacts` array replaces/merges into the Registration\'s existing Contacts collection,  matched by `contactId` (upsert semantics) - there is no separate scalar contactId field.  The `choices` array sets the status of the Registration\'s Applications; each Application is  independently approvable - see the `applications/{applicationId}/approve` route to approve  just one without touching the others.

### Example

```typescript
import {
    EnrollmentAdminRegistrationsApi,
    Configuration,
    EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminRegistrationApproveRequestDto
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminRegistrationsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)
let edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminRegistrationApproveRequestDto: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminRegistrationApproveRequestDto; // (optional)

const { status, data } = await apiInstance.approveEnrollmentRegistration(
    tenantId,
    id,
    edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminRegistrationApproveRequestDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminRegistrationApproveRequestDto** | **EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminRegistrationApproveRequestDto**|  | |
| **tenantId** | [**string**] |  | defaults to undefined|
| **id** | [**string**] |  | defaults to undefined|


### Return type

**EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse**

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
|**200** | The registration was approved. |  -  |
|**400** | Bad Request. The request was invalid and cannot be completed. |  -  |
|**404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **approveEnrollmentRegistrationApplication**
> EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse approveEnrollmentRegistrationApplication()

Same request body shape as `PUT .../registrations/{id}/approve`. Future Phase 99:  `PUT .../registrations/{id}/contacts/{id}/match` is out of scope and not implemented here.

### Example

```typescript
import {
    EnrollmentAdminRegistrationsApi,
    Configuration,
    EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminRegistrationApproveRequestDto
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminRegistrationsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)
let applicationId: string; // (default to undefined)
let edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminRegistrationApproveRequestDto: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminRegistrationApproveRequestDto; // (optional)

const { status, data } = await apiInstance.approveEnrollmentRegistrationApplication(
    tenantId,
    id,
    applicationId,
    edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminRegistrationApproveRequestDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminRegistrationApproveRequestDto** | **EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminRegistrationApproveRequestDto**|  | |
| **tenantId** | [**string**] |  | defaults to undefined|
| **id** | [**string**] |  | defaults to undefined|
| **applicationId** | [**string**] |  | defaults to undefined|


### Return type

**EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse**

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
|**200** | The application was approved. |  -  |
|**400** | Bad Request. The request was invalid and cannot be completed. |  -  |
|**404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createEnrollmentRegistration**
> EnrollmentApiEnrollmentRegistrationsV1RegistrationCreatedResponse createEnrollmentRegistration()


### Example

```typescript
import {
    EnrollmentAdminRegistrationsApi,
    Configuration,
    EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateRegistrationRequestDto
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminRegistrationsApi(configuration);

let tenantId: string; // (default to undefined)
let edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateRegistrationRequestDto: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateRegistrationRequestDto; // (optional)

const { status, data } = await apiInstance.createEnrollmentRegistration(
    tenantId,
    edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateRegistrationRequestDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateRegistrationRequestDto** | **EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateRegistrationRequestDto**|  | |
| **tenantId** | [**string**] |  | defaults to undefined|


### Return type

**EnrollmentApiEnrollmentRegistrationsV1RegistrationCreatedResponse**

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
|**201** | The registration was created. |  -  |
|**400** | Bad Request. The request was invalid and cannot be completed. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteEnrollmentRegistration**
> deleteEnrollmentRegistration()


### Example

```typescript
import {
    EnrollmentAdminRegistrationsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminRegistrationsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)

const { status, data } = await apiInstance.deleteEnrollmentRegistration(
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
|**204** | The registration was removed. |  -  |
|**404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getEnrollmentRegistration**
> EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse getEnrollmentRegistration()


### Example

```typescript
import {
    EnrollmentAdminRegistrationsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminRegistrationsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)

const { status, data } = await apiInstance.getEnrollmentRegistration(
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

**EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse**

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

# **getEnrollmentRegistrationApplications**
> EnrollmentApiEnrollmentRegistrationsV1RegistrationApplicationsListResponse getEnrollmentRegistrationApplications()


### Example

```typescript
import {
    EnrollmentAdminRegistrationsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminRegistrationsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)

const { status, data } = await apiInstance.getEnrollmentRegistrationApplications(
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

**EnrollmentApiEnrollmentRegistrationsV1RegistrationApplicationsListResponse**

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

# **getEnrollmentRegistrations**
> EnrollmentApiEnrollmentRegistrationsV1RegistrationsSearchResponse getEnrollmentRegistrations()


### Example

```typescript
import {
    EnrollmentAdminRegistrationsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminRegistrationsApi(configuration);

let tenantId: string; // (default to undefined)
let pageIndex: number; // (optional) (default to undefined)
let pageSize: number; // (optional) (default to undefined)
let filter: string; // (optional) (default to undefined)
let orderBy: string; // (optional) (default to undefined)

const { status, data } = await apiInstance.getEnrollmentRegistrations(
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

**EnrollmentApiEnrollmentRegistrationsV1RegistrationsSearchResponse**

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

# **rejectEnrollmentRegistration**
> EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse rejectEnrollmentRegistration()


### Example

```typescript
import {
    EnrollmentAdminRegistrationsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminRegistrationsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)
let body: object; // (optional)

const { status, data } = await apiInstance.rejectEnrollmentRegistration(
    tenantId,
    id,
    body
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **body** | **object**|  | |
| **tenantId** | [**string**] |  | defaults to undefined|
| **id** | [**string**] |  | defaults to undefined|


### Return type

**EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse**

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
|**200** | The registration was rejected. |  -  |
|**400** | Bad Request. The request was invalid and cannot be completed. |  -  |
|**404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **submitEnrollmentRegistration**
> EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse submitEnrollmentRegistration()


### Example

```typescript
import {
    EnrollmentAdminRegistrationsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminRegistrationsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)
let body: object; // (optional)

const { status, data } = await apiInstance.submitEnrollmentRegistration(
    tenantId,
    id,
    body
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **body** | **object**|  | |
| **tenantId** | [**string**] |  | defaults to undefined|
| **id** | [**string**] |  | defaults to undefined|


### Return type

**EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse**

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
|**200** | The registration was submitted. |  -  |
|**400** | Bad Request. The request was invalid and cannot be completed. |  -  |
|**404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateEnrollmentRegistration**
> EnrollmentApiEnrollmentRegistrationsV1RegistrationUpdatedResponse updateEnrollmentRegistration()


### Example

```typescript
import {
    EnrollmentAdminRegistrationsApi,
    Configuration,
    EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateRegistrationRequestDto
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminRegistrationsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)
let edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateRegistrationRequestDto: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateRegistrationRequestDto; // (optional)

const { status, data } = await apiInstance.updateEnrollmentRegistration(
    tenantId,
    id,
    edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateRegistrationRequestDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateRegistrationRequestDto** | **EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateRegistrationRequestDto**|  | |
| **tenantId** | [**string**] |  | defaults to undefined|
| **id** | [**string**] |  | defaults to undefined|


### Return type

**EnrollmentApiEnrollmentRegistrationsV1RegistrationUpdatedResponse**

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
|**200** | The registration was updated. |  -  |
|**400** | Bad Request. The request was invalid and cannot be completed. |  -  |
|**404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

