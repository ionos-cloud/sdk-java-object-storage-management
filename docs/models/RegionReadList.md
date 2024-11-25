

# RegionReadList

## Properties

| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **id** | [**UUID**](UUID.md) | ID of the list of Region resources. |  |
| **type** | [**TypeEnum**](#TypeEnum) | The type of the resource. |  |
| **href** | **String** | The URL of the list of Region resources. |  |
| **items** | [**List&lt;RegionRead&gt;**](RegionRead.md) | The list of Region resources. |  [optional] |
| **offset** | **Integer** | The offset specified in the request (if none was specified, the default offset is 0).  |  [readonly] |
| **limit** | **Integer** | The limit specified in the request (if none was specified, use the endpoint&#39;s default pagination limit).  |  [readonly] |
| **links** | [**Links**](Links.md) |  |  |



## Enum: TypeEnum

| Name | Value |
| ---- | -----
| COLLECTION | &quot;collection&quot; |


