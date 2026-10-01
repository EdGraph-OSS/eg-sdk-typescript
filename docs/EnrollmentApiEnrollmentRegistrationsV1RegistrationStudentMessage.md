# EnrollmentApiEnrollmentRegistrationsV1RegistrationStudentMessage

The student a registration is for. studentId is the EnrollmentStudent record id, all zeros until  the registration is linked; the local/state/external ids and names are denormalized from the  student or supplied by the registration flow. No id of its own.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**studentId** | **string** |  | [optional] [default to undefined]
**studentLocalCode** | **string** |  | [optional] [default to undefined]
**studentStateCode** | **string** |  | [optional] [default to undefined]
**studentFirstName** | **string** |  | [optional] [default to undefined]
**studentLastName** | **string** |  | [optional] [default to undefined]
**externalDataSourceStudentId** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { EnrollmentApiEnrollmentRegistrationsV1RegistrationStudentMessage } from '@edgraph-oss/platform-client';

const instance: EnrollmentApiEnrollmentRegistrationsV1RegistrationStudentMessage = {
    studentId,
    studentLocalCode,
    studentStateCode,
    studentFirstName,
    studentLastName,
    externalDataSourceStudentId,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
