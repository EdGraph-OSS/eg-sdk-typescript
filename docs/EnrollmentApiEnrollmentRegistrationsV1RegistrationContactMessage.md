# EnrollmentApiEnrollmentRegistrationsV1RegistrationContactMessage

One contact on a registration. id is the entry\'s own identity (minted once, never overwritten);  contactId is the EnrollmentContact record id the entry resolved to (the key every join goes  through; unset until resolved); externalDataSourceContactId is the SIS-side code, when known.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional] [default to undefined]
**contactId** | **string** |  | [optional] [default to undefined]
**contactName** | **string** |  | [optional] [default to undefined]
**contactPhone** | **string** |  | [optional] [default to undefined]
**contactEmail** | **string** |  | [optional] [default to undefined]
**externalDataSourceContactId** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { EnrollmentApiEnrollmentRegistrationsV1RegistrationContactMessage } from '@edgraph-oss/platform-client';

const instance: EnrollmentApiEnrollmentRegistrationsV1RegistrationContactMessage = {
    id,
    contactId,
    contactName,
    contactPhone,
    contactEmail,
    externalDataSourceContactId,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
