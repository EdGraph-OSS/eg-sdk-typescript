# EdfiAdminApiEdfiAdminV1AddSchoolYearRangeRequestEntry


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**year** | **number** |  | [optional] [default to undefined]
**selectedTierId** | **string** |  | [optional] [default to undefined]
**odsBackupCode** | **string** |  | [optional] [default to undefined]
**applicationIds** | **Array&lt;number&gt;** | Per-year pending grants are applied only after this ODS finishes provisioning.  Keep field 4 aligned in every source and consumer copy to preserve the wire contract. | [optional] [readonly] [default to undefined]

## Example

```typescript
import { EdfiAdminApiEdfiAdminV1AddSchoolYearRangeRequestEntry } from '@edgraph-oss/platform-client';

const instance: EdfiAdminApiEdfiAdminV1AddSchoolYearRangeRequestEntry = {
    year,
    selectedTierId,
    odsBackupCode,
    applicationIds,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
