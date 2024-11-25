

# MetadataWithStatus

## Properties

| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **createdDate** | [**OffsetDateTime**](OffsetDateTime.md) | The ISO 8601 creation timestamp. |  [optional] [readonly] |
| **createdBy** | **String** | Unique name of the identity that created the resource. |  [optional] [readonly] |
| **createdByUserId** | **String** | Unique id of the identity that created the resource. |  [optional] [readonly] |
| **lastModifiedDate** | [**OffsetDateTime**](OffsetDateTime.md) | The ISO 8601 modified timestamp. |  [optional] [readonly] |
| **lastModifiedBy** | **String** | Unique name of the identity that last modified the resource. |  [optional] [readonly] |
| **lastModifiedByUserId** | **String** | Unique id of the identity that last modified the resource. |  [optional] [readonly] |
| **resourceURN** | **String** | Unique name of the resource. |  [optional] [readonly] |
| **status** | [**StatusEnum**](#StatusEnum) | The status of the object. The status can be: * &#x60;AVAILABLE&#x60; - resource exists and is healthy. * &#x60;PROVISIONING&#x60; - resource is being created or updated. * &#x60;DESTROYING&#x60; - delete command was issued, the resource is being deleted. * &#x60;FAILED&#x60; - resource failed, details in &#x60;failureMessage&#x60;.  |  [readonly] |
| **statusMessage** | **String** | The message of the failure if the status is &#x60;FAILED&#x60;.  |  [optional] [readonly] |
| **administrative** | **Boolean** | Indicates if the key is an administrative key. Administrative keys can create buckets and set bucket policies.  |  [optional] [readonly] |



## Enum: StatusEnum

| Name | Value |
| ---- | -----
| PROVISIONING | &quot;PROVISIONING&quot; |
| DESTROYING | &quot;DESTROYING&quot; |
| AVAILABLE | &quot;AVAILABLE&quot; |
| FAILED | &quot;FAILED&quot; |


