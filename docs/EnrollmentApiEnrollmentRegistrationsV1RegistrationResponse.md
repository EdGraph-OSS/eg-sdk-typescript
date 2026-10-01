# EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional] [default to undefined]
**tenantId** | **string** |  | [optional] [default to undefined]
**pathway** | [**EnrollmentApiEnrollmentRegistrationsV1PathwayMessage**](EnrollmentApiEnrollmentRegistrationsV1PathwayMessage.md) |  | [optional] [default to undefined]
**currentScreenCode** | **string** |  | [optional] [default to undefined]
**progress** | **string** | Decimal progress (0-100, 2dp) carried as an invariant-culture string,  mirroring the legacy enrollmentresults.proto completedProgress convention. | [optional] [default to undefined]
**languageCode** | **string** |  | [optional] [default to undefined]
**contacts** | [**Array&lt;EnrollmentApiEnrollmentRegistrationsV1RegistrationContactMessage&gt;**](EnrollmentApiEnrollmentRegistrationsV1RegistrationContactMessage.md) |  | [optional] [readonly] [default to undefined]
**screens** | [**Array&lt;EnrollmentApiEnrollmentRegistrationsV1RegistrationScreenMessage&gt;**](EnrollmentApiEnrollmentRegistrationsV1RegistrationScreenMessage.md) |  | [optional] [readonly] [default to undefined]
**createdBy** | **string** |  | [optional] [default to undefined]
**createdDateTime** | **string** |  | [optional] [default to undefined]
**lastModifiedBy** | **string** |  | [optional] [default to undefined]
**lastModifiedDateTime** | **string** |  | [optional] [default to undefined]
**deletedBy** | **string** |  | [optional] [default to undefined]
**deletedDateTime** | **string** |  | [optional] [default to undefined]
**isDeleted** | **boolean** |  | [optional] [default to undefined]
**status** | **string** |  | [optional] [default to undefined]
**nextSchoolStateShortCode** | **string** |  | [optional] [default to undefined]
**nextSchoolName** | **string** |  | [optional] [default to undefined]
**student** | [**EnrollmentApiEnrollmentRegistrationsV1RegistrationStudentMessage**](EnrollmentApiEnrollmentRegistrationsV1RegistrationStudentMessage.md) |  | [optional] [default to undefined]
**applications** | [**Array&lt;EnrollmentApiEnrollmentRegistrationsV1RegistrationApplicationMessage&gt;**](EnrollmentApiEnrollmentRegistrationsV1RegistrationApplicationMessage.md) |  | [optional] [readonly] [default to undefined]

## Example

```typescript
import { EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse } from '@edgraph-oss/platform-client';

const instance: EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse = {
    id,
    tenantId,
    pathway,
    currentScreenCode,
    progress,
    languageCode,
    contacts,
    screens,
    createdBy,
    createdDateTime,
    lastModifiedBy,
    lastModifiedDateTime,
    deletedBy,
    deletedDateTime,
    isDeleted,
    status,
    nextSchoolStateShortCode,
    nextSchoolName,
    student,
    applications,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
