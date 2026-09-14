# EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponseResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional] [default to undefined]
**tenantId** | **string** |  | [optional] [default to undefined]
**applicationPathway** | [**EnrollmentApiEnrollmentApplicationResponsesV1ApplicationPathwayMessage**](EnrollmentApiEnrollmentApplicationResponsesV1ApplicationPathwayMessage.md) |  | [optional] [default to undefined]
**currentScreenCode** | **string** |  | [optional] [default to undefined]
**progress** | **string** | Decimal progress (0-100, 2dp) carried as an invariant-culture string,  mirroring the legacy enrollmentresults.proto completedProgress convention. | [optional] [default to undefined]
**studentId** | **string** |  | [optional] [default to undefined]
**languageCode** | **string** |  | [optional] [default to undefined]
**contacts** | [**Array&lt;EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponseContactMessage&gt;**](EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponseContactMessage.md) |  | [optional] [readonly] [default to undefined]
**screens** | [**Array&lt;EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponseScreenMessage&gt;**](EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponseScreenMessage.md) |  | [optional] [readonly] [default to undefined]
**createdBy** | **string** |  | [optional] [default to undefined]
**createdDateTime** | **string** |  | [optional] [default to undefined]
**lastModifiedBy** | **string** |  | [optional] [default to undefined]
**lastModifiedDateTime** | **string** |  | [optional] [default to undefined]
**deletedBy** | **string** |  | [optional] [default to undefined]
**deletedDateTime** | **string** |  | [optional] [default to undefined]
**isDeleted** | **boolean** |  | [optional] [default to undefined]
**status** | **string** |  | [optional] [default to undefined]
**studentFirstName** | **string** |  | [optional] [default to undefined]
**studentLastName** | **string** |  | [optional] [default to undefined]
**studentLocalId** | **string** |  | [optional] [default to undefined]
**nextSchoolCode** | **string** |  | [optional] [default to undefined]
**nextSchoolName** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponseResponse } from '@edgraph-oss/platform-client';

const instance: EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponseResponse = {
    id,
    tenantId,
    applicationPathway,
    currentScreenCode,
    progress,
    studentId,
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
    studentFirstName,
    studentLastName,
    studentLocalId,
    nextSchoolCode,
    nextSchoolName,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
