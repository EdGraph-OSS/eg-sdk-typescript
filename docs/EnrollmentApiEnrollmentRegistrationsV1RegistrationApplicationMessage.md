# EnrollmentApiEnrollmentRegistrationsV1RegistrationApplicationMessage

One Program-seat choice on a Registration - zero-to-many, independently approvable. See  ApproveRegistrationApplication / GetRegistrationApplications.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**applicationId** | **string** |  | [optional] [default to undefined]
**applicationStatus** | **string** |  | [optional] [default to undefined]
**programId** | **string** | enrollment-svc-programs._id - one school\&#39;s offering of a program. | [optional] [default to undefined]
**rank** | **number** | The family\&#39;s preference order within the round. 1-based and contiguous across the  registration - the matcher\&#39;s contract. Assigned server-side, never supplied by a caller. | [optional] [default to undefined]
**priority** | **number** | The priority tier - sibling, staff, feeder, PreK. Unset until the priority engine stamps it. | [optional] [default to undefined]
**applicationRoundId** | **string** | Foreign key into the application round this entry was submitted to. | [optional] [default to undefined]

## Example

```typescript
import { EnrollmentApiEnrollmentRegistrationsV1RegistrationApplicationMessage } from '@edgraph-oss/platform-client';

const instance: EnrollmentApiEnrollmentRegistrationsV1RegistrationApplicationMessage = {
    applicationId,
    applicationStatus,
    programId,
    rank,
    priority,
    applicationRoundId,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
