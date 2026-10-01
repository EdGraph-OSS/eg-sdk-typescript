# EnrollmentAdminSettingsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**publishEnrollmentSettings**](#publishenrollmentsettings) | **POST** /tenants/{tenantId}/enrollmentadmin/settings/publish | Publishes the tenant\&#39;s current enrollment settings (custom branding, global configuration,  policy acknowledgement URLs) to the public enrollment site.|

# **publishEnrollmentSettings**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminPublishEnrollmentSettingsResultDto publishEnrollmentSettings()


### Example

```typescript
import {
    EnrollmentAdminSettingsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminSettingsApi(configuration);

let tenantId: string; // (default to undefined)

const { status, data } = await apiInstance.publishEnrollmentSettings(
    tenantId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **tenantId** | [**string**] |  | defaults to undefined|


### Return type

**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminPublishEnrollmentSettingsResultDto**

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

