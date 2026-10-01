# EnrollmentAdminContactsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**addEnrollmentContactStudent**](#addenrollmentcontactstudent) | **POST** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/students | Links a student to a contact.|
|[**createEnrollmentContact**](#createenrollmentcontact) | **POST** /tenants/{tenantId}/enrollmentadmin/contacts | Creates or updates an Enrollment Contact by its source-system &#x60;contactId&#x60;.|
|[**getEnrollmentContactById**](#getenrollmentcontactbyid) | **GET** /tenants/{tenantId}/enrollmentadmin/contacts/{id} | Gets an Enrollment Contact by its record id, with its linked students.|
|[**getEnrollmentContactChangelogs**](#getenrollmentcontactchangelogs) | **GET** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/changelogs | Reads every lifecycle event for a contact - create, update, delete, overrides and sign-in  unlocks - newest first.|
|[**getEnrollmentContactOverrides**](#getenrollmentcontactoverrides) | **GET** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/overrides | Reads a contact\&#39;s override history, newest first.|
|[**getEnrollmentContactRegistrations**](#getenrollmentcontactregistrations) | **GET** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/registrations | Gets a contact\&#39;s Registrations.|
|[**getEnrollmentContactStudents**](#getenrollmentcontactstudents) | **GET** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/students | Gets a contact\&#39;s linked students, with each link\&#39;s association attributes.|
|[**getEnrollmentContacts**](#getenrollmentcontacts) | **GET** /tenants/{tenantId}/enrollmentadmin/contacts | Searches Enrollment Contacts.|
|[**overrideEnrollmentContactEmail**](#overrideenrollmentcontactemail) | **PUT** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/overrides/emails | Overrides a contact\&#39;s email address.|
|[**overrideEnrollmentContactPhone**](#overrideenrollmentcontactphone) | **PUT** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/overrides/phones | Overrides a contact\&#39;s phone number.|
|[**removeEnrollmentContactEmailOverride**](#removeenrollmentcontactemailoverride) | **DELETE** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/overrides/emails | Removes a contact\&#39;s email override, letting the SIS value show through again.|
|[**removeEnrollmentContactPhoneOverride**](#removeenrollmentcontactphoneoverride) | **DELETE** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/overrides/phones | Removes a contact\&#39;s phone override, letting the SIS value show through again.|
|[**removeEnrollmentContactStudent**](#removeenrollmentcontactstudent) | **DELETE** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/students/{studentId} | Removes a student\&#39;s link to a contact.|
|[**unlockEnrollmentContactSignIn**](#unlockenrollmentcontactsignin) | **POST** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/unlock | Unlocks a contact\&#39;s sign-in, resetting exhausted parent-verification tries.|
|[**updateEnrollmentContact**](#updateenrollmentcontact) | **PUT** /tenants/{tenantId}/enrollmentadmin/contacts/{id} | Updates an Enrollment Contact\&#39;s name.|
|[**updateEnrollmentContactStudent**](#updateenrollmentcontactstudent) | **PUT** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/students/{studentId} | Updates a contact-student association\&#39;s attributes.|
|[**verifyEnrollmentContact**](#verifyenrollmentcontact) | **PUT** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/verify | Verifies a contact.|

# **addEnrollmentContactStudent**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactStudentAssociatedResultDto addEnrollmentContactStudent()

Send `studentId` (the SIS code) to resolve or create the linked EnrollmentStudent  document server-side, or `id` (an existing student\'s own internal id, as returned by  this same route\'s GET) to link that exact student directly - `id` wins if both are  given, and never creates anything, 404ing instead if it does not exist. Set the association  attributes (priority, relationship, etc.) with a follow-up PUT to  `.../students/{studentId}`.

### Example

```typescript
import {
    EnrollmentAdminContactsApi,
    Configuration,
    EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminAddContactStudentRequestDto
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminContactsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)
let edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminAddContactStudentRequestDto: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminAddContactStudentRequestDto; // (optional)

const { status, data } = await apiInstance.addEnrollmentContactStudent(
    tenantId,
    id,
    edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminAddContactStudentRequestDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminAddContactStudentRequestDto** | **EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminAddContactStudentRequestDto**|  | |
| **tenantId** | [**string**] |  | defaults to undefined|
| **id** | [**string**] |  | defaults to undefined|


### Return type

**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactStudentAssociatedResultDto**

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
|**201** | The student was linked to the contact. |  -  |
|**400** | Bad Request. The request was invalid and cannot be completed. |  -  |
|**404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createEnrollmentContact**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactMutationResultDto createEnrollmentContact()

<br>              Upsert semantics: unique per `contactId`. A first call creates the contact; a later call              for the same `contactId` overwrites the SIS-sourced fields where they differ, and no-ops              when they are identical. An existing email/phone override is never touched by this call - see              the `overrides/emails` and `overrides/phones` routes for that.                <br>    `email` and `phone` here are the SIS-sourced values, which is what a contact starts              with. Changing either afterwards is an override rather than an update - see the              `overrides/emails` and `overrides/phones` routes.              

### Example

```typescript
import {
    EnrollmentAdminContactsApi,
    Configuration,
    EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateContactRequestDto
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminContactsApi(configuration);

let tenantId: string; // (default to undefined)
let edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateContactRequestDto: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateContactRequestDto; // (optional)

const { status, data } = await apiInstance.createEnrollmentContact(
    tenantId,
    edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateContactRequestDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateContactRequestDto** | **EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateContactRequestDto**|  | |
| **tenantId** | [**string**] |  | defaults to undefined|


### Return type

**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactMutationResultDto**

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
|**201** | The contact was created or updated. |  -  |
|**400** | Bad Request. The request was invalid and cannot be completed. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getEnrollmentContactById**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactResponseDto getEnrollmentContactById()


### Example

```typescript
import {
    EnrollmentAdminContactsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminContactsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)

const { status, data } = await apiInstance.getEnrollmentContactById(
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

**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactResponseDto**

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

# **getEnrollmentContactChangelogs**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideHistoryEntryDtoPaginatedItemsViewModel getEnrollmentContactChangelogs()

<br>              Eventually consistent, on the same terms as M:EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.EnrollmentAdminController.GetEnrollmentContactOverrides(System.String,System.Guid,System.Int32,System.Int32,System.String,System.Threading.CancellationToken).                <br>    `EventType` on `GetAllChangesRequest` is a single optional string, so it cannot              express \"any of these event types\" on its own. The filter is built through `Filter`              instead - a raw Elasticsearch `query_string` - while `EntityType` and              `EntityId` stay the typed fields M:EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.EnrollmentAdminController.GetEnrollmentContactOverrides(System.String,System.Guid,System.Int32,System.Int32,System.String,System.Threading.CancellationToken) already uses.              The change log applies the typed fields as `filter` clauses and `Filter` as a              `must` clause on the same bool query, so the two combine as an AND: this call still never              leaves this contact\'s own entity scope.                <br>              The event types covered are EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Responses.EnrollmentAdmin.ContactOverrideHistoryExtensions.ContactEventTypes,              which tracks what the Enrollment outbox publishes against a contact.              

### Example

```typescript
import {
    EnrollmentAdminContactsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminContactsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)
let pageSize: number; // (optional) (default to 20)
let pageIndex: number; // (optional) (default to 0)
let studentId: string; //Narrows to changes affecting one linked student. (optional) (default to '')

const { status, data } = await apiInstance.getEnrollmentContactChangelogs(
    tenantId,
    id,
    pageSize,
    pageIndex,
    studentId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **tenantId** | [**string**] |  | defaults to undefined|
| **id** | [**string**] |  | defaults to undefined|
| **pageSize** | [**number**] |  | (optional) defaults to 20|
| **pageIndex** | [**number**] |  | (optional) defaults to 0|
| **studentId** | [**string**] | Narrows to changes affecting one linked student. | (optional) defaults to ''|


### Return type

**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideHistoryEntryDtoPaginatedItemsViewModel**

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
|**400** | Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getEnrollmentContactOverrides**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideHistoryEntryDtoPaginatedItemsViewModel getEnrollmentContactOverrides()

<br>              Eventually consistent. A change reaches the log through Enrollment\'s outbox, so an entry can              be a few seconds behind a write that has already succeeded. Render the current value from the              contact itself and use this for what preceded it.                <br>              One route for both details, unlike the writes: this is a single ordered log and each entry              names its own detail, so splitting it would mean two requests to render one contact\'s              timeline and two page counts to reconcile.              

### Example

```typescript
import {
    EnrollmentAdminContactsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminContactsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)
let pageSize: number; // (optional) (default to 20)
let pageIndex: number; // (optional) (default to 0)
let studentId: string; //Narrows to changes affecting one linked student. (optional) (default to '')

const { status, data } = await apiInstance.getEnrollmentContactOverrides(
    tenantId,
    id,
    pageSize,
    pageIndex,
    studentId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **tenantId** | [**string**] |  | defaults to undefined|
| **id** | [**string**] |  | defaults to undefined|
| **pageSize** | [**number**] |  | (optional) defaults to 20|
| **pageIndex** | [**number**] |  | (optional) defaults to 0|
| **studentId** | [**string**] | Narrows to changes affecting one linked student. | (optional) defaults to ''|


### Return type

**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideHistoryEntryDtoPaginatedItemsViewModel**

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
|**400** | Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getEnrollmentContactRegistrations**
> Array<EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse> getEnrollmentContactRegistrations()


### Example

```typescript
import {
    EnrollmentAdminContactsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminContactsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)

const { status, data } = await apiInstance.getEnrollmentContactRegistrations(
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

**Array<EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse>**

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

# **getEnrollmentContactStudents**
> Array<EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactStudentDetailDto> getEnrollmentContactStudents()


### Example

```typescript
import {
    EnrollmentAdminContactsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminContactsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)

const { status, data } = await apiInstance.getEnrollmentContactStudents(
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

**Array<EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactStudentDetailDto>**

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

# **getEnrollmentContacts**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactResponseDtoPaginatedItemsViewModel getEnrollmentContacts()


### Example

```typescript
import {
    EnrollmentAdminContactsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminContactsApi(configuration);

let tenantId: string; // (default to undefined)
let pageSize: number; // (optional) (default to 50)
let pageIndex: number; // (optional) (default to 0)
let orderBy: string; // (optional) (default to '')
let filter: string; // (optional) (default to '')
let search: string; //Free-text match on contact name, email, or phone. (optional) (default to '')
let nextSchoolStateShortCode: string; //Narrows to contacts with at least one linked student whose next school has this state short code. (optional) (default to '')
let locked: boolean; //Narrows to contacts by sign-in lock status. Unset returns every contact. (optional) (default to undefined)

const { status, data } = await apiInstance.getEnrollmentContacts(
    tenantId,
    pageSize,
    pageIndex,
    orderBy,
    filter,
    search,
    nextSchoolStateShortCode,
    locked
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
| **search** | [**string**] | Free-text match on contact name, email, or phone. | (optional) defaults to ''|
| **nextSchoolStateShortCode** | [**string**] | Narrows to contacts with at least one linked student whose next school has this state short code. | (optional) defaults to ''|
| **locked** | [**boolean**] | Narrows to contacts by sign-in lock status. Unset returns every contact. | (optional) defaults to undefined|


### Return type

**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactResponseDtoPaginatedItemsViewModel**

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

# **overrideEnrollmentContactEmail**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideResultDto overrideEnrollmentContactEmail()

The override is an enrollment-local annotation over SIS data, not a writeback. The SIS value  is kept and returned alongside it, and the correction keeps winning over later SIS imports  until staff revisit it.  <br>  The corrected value is shared by every student linked to the contact. `studentId` in the  body only records whose screen the edit came from.  

### Example

```typescript
import {
    EnrollmentAdminContactsApi,
    Configuration,
    EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactEmailOverrideRequestDto
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminContactsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)
let edGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactEmailOverrideRequestDto: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactEmailOverrideRequestDto; // (optional)

const { status, data } = await apiInstance.overrideEnrollmentContactEmail(
    tenantId,
    id,
    edGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactEmailOverrideRequestDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactEmailOverrideRequestDto** | **EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactEmailOverrideRequestDto**|  | |
| **tenantId** | [**string**] |  | defaults to undefined|
| **id** | [**string**] |  | defaults to undefined|


### Return type

**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideResultDto**

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
|**200** | The override was applied. |  -  |
|**400** | Bad Request |  -  |
|**404** | Not Found |  -  |
|**412** | The contact changed while it was being edited; the write was refused. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **overrideEnrollmentContactPhone**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideResultDto overrideEnrollmentContactPhone()

The override is an enrollment-local annotation over SIS data, not a writeback. The SIS value  is kept and returned alongside it, and the correction keeps winning over later SIS imports  until staff revisit it.  <br>  The corrected value is shared by every student linked to the contact. `studentId` in the  body only records whose screen the edit came from.  

### Example

```typescript
import {
    EnrollmentAdminContactsApi,
    Configuration,
    EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactPhoneOverrideRequestDto
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminContactsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)
let edGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactPhoneOverrideRequestDto: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactPhoneOverrideRequestDto; // (optional)

const { status, data } = await apiInstance.overrideEnrollmentContactPhone(
    tenantId,
    id,
    edGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactPhoneOverrideRequestDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactPhoneOverrideRequestDto** | **EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactPhoneOverrideRequestDto**|  | |
| **tenantId** | [**string**] |  | defaults to undefined|
| **id** | [**string**] |  | defaults to undefined|


### Return type

**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideResultDto**

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
|**200** | The override was applied. |  -  |
|**400** | Bad Request |  -  |
|**404** | Not Found |  -  |
|**412** | The contact changed while it was being edited; the write was refused. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **removeEnrollmentContactEmailOverride**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideResultDto removeEnrollmentContactEmailOverride()

The removal is itself recorded in the history - the superseded value stays recoverable.

### Example

```typescript
import {
    EnrollmentAdminContactsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminContactsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)
let studentLocalCode: string; //The local code of the student whose screen the removal was made from. (optional) (default to '')
let expectedVersion: string; //The `lastUpdatedDateTime` this edit started from. (optional) (default to '')

const { status, data } = await apiInstance.removeEnrollmentContactEmailOverride(
    tenantId,
    id,
    studentLocalCode,
    expectedVersion
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **tenantId** | [**string**] |  | defaults to undefined|
| **id** | [**string**] |  | defaults to undefined|
| **studentLocalCode** | [**string**] | The local code of the student whose screen the removal was made from. | (optional) defaults to ''|
| **expectedVersion** | [**string**] | The &#x60;lastUpdatedDateTime&#x60; this edit started from. | (optional) defaults to ''|


### Return type

**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideResultDto**

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
|**200** | The override was removed, or there was none to remove. |  -  |
|**404** | Not Found |  -  |
|**412** | The contact changed while it was being edited; the write was refused. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **removeEnrollmentContactPhoneOverride**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideResultDto removeEnrollmentContactPhoneOverride()

The removal is itself recorded in the history - the superseded value stays recoverable.

### Example

```typescript
import {
    EnrollmentAdminContactsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminContactsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)
let studentLocalCode: string; //The local code of the student whose screen the removal was made from. (optional) (default to '')
let expectedVersion: string; //The `lastUpdatedDateTime` this edit started from. (optional) (default to '')

const { status, data } = await apiInstance.removeEnrollmentContactPhoneOverride(
    tenantId,
    id,
    studentLocalCode,
    expectedVersion
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **tenantId** | [**string**] |  | defaults to undefined|
| **id** | [**string**] |  | defaults to undefined|
| **studentLocalCode** | [**string**] | The local code of the student whose screen the removal was made from. | (optional) defaults to ''|
| **expectedVersion** | [**string**] | The &#x60;lastUpdatedDateTime&#x60; this edit started from. | (optional) defaults to ''|


### Return type

**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideResultDto**

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
|**200** | The override was removed, or there was none to remove. |  -  |
|**404** | Not Found |  -  |
|**412** | The contact changed while it was being edited; the write was refused. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **removeEnrollmentContactStudent**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactStudentRemovedResultDto removeEnrollmentContactStudent()


### Example

```typescript
import {
    EnrollmentAdminContactsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminContactsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)
let studentId: string; // (default to undefined)

const { status, data } = await apiInstance.removeEnrollmentContactStudent(
    tenantId,
    id,
    studentId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **tenantId** | [**string**] |  | defaults to undefined|
| **id** | [**string**] |  | defaults to undefined|
| **studentId** | [**string**] |  | defaults to undefined|


### Return type

**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactStudentRemovedResultDto**

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
|**200** | The link was removed, or there was none to remove. |  -  |
|**404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **unlockEnrollmentContactSignIn**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactSignInUnlockedResultDto unlockEnrollmentContactSignIn()

Idempotent: unlocking an already-unlocked contact, or one with no rows at all, is a 200 with  `resetCount: 0`, not an error.

### Example

```typescript
import {
    EnrollmentAdminContactsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminContactsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)

const { status, data } = await apiInstance.unlockEnrollmentContactSignIn(
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

**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactSignInUnlockedResultDto**

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
|**200** | The contact\&#39;s sign-in was unlocked, or there was nothing to unlock. |  -  |
|**404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateEnrollmentContact**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactMutationResultDto updateEnrollmentContact()

Email and phone cannot be changed here. Correcting either is an override, which records who  changed it and keeps the SIS value beside the correction; a body carrying `email` or  `phone` is rejected with a 400 naming the route to use instead. Note that a contact whose  email is overridden keeps that override across this call - an update to the name leaves a  standing correction alone. Student association is managed exclusively through the  `/contacts/{id}/students` sub-resource, not through this call.

### Example

```typescript
import {
    EnrollmentAdminContactsApi,
    Configuration,
    EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateContactRequestDto
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminContactsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)
let edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateContactRequestDto: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateContactRequestDto; // (optional)

const { status, data } = await apiInstance.updateEnrollmentContact(
    tenantId,
    id,
    edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateContactRequestDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateContactRequestDto** | **EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateContactRequestDto**|  | |
| **tenantId** | [**string**] |  | defaults to undefined|
| **id** | [**string**] |  | defaults to undefined|


### Return type

**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactMutationResultDto**

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
|**200** | The contact was updated. |  -  |
|**400** | Bad Request. The request was invalid and cannot be completed. |  -  |
|**404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateEnrollmentContactStudent**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactStudentAssociatedResultDto updateEnrollmentContactStudent()


### Example

```typescript
import {
    EnrollmentAdminContactsApi,
    Configuration,
    EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateContactStudentRequestDto
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminContactsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)
let studentId: string; // (default to undefined)
let edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateContactStudentRequestDto: EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateContactStudentRequestDto; // (optional)

const { status, data } = await apiInstance.updateEnrollmentContactStudent(
    tenantId,
    id,
    studentId,
    edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateContactStudentRequestDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateContactStudentRequestDto** | **EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateContactStudentRequestDto**|  | |
| **tenantId** | [**string**] |  | defaults to undefined|
| **id** | [**string**] |  | defaults to undefined|
| **studentId** | [**string**] |  | defaults to undefined|


### Return type

**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactStudentAssociatedResultDto**

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
|**200** | The association was updated. |  -  |
|**400** | Bad Request. The request was invalid and cannot be completed. |  -  |
|**404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **verifyEnrollmentContact**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactVerifiedResultDto verifyEnrollmentContact()


### Example

```typescript
import {
    EnrollmentAdminContactsApi,
    Configuration
} from '@edgraph-oss/platform-client';

const configuration = new Configuration();
const apiInstance = new EnrollmentAdminContactsApi(configuration);

let tenantId: string; // (default to undefined)
let id: string; // (default to undefined)

const { status, data } = await apiInstance.verifyEnrollmentContact(
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

**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactVerifiedResultDto**

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
|**200** | The contact was verified. |  -  |
|**404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

