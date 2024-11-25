

# Region

IONOS Cloud object storage regions they define the location of the bucket, can also be used as `LocationConstraint` for bucket creation. 
## Properties

| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **version** | **Integer** | The version of the region properties |  |
| **endpoint** | **String** | The endpoint URL for the region |  |
| **website** | **String** | The website URL for the region |  |
| **capability** | [**RegionCapability**](RegionCapability.md) |  |  |
| **storageClasses** | **List&lt;String&gt;** | The available classes in the region |  [optional] |
| **location** | **String** | The data center location of the region as per [Get Location](/docs/cloud/v6/#tag/Locations/operation/locationsGet). *Can&#39;t be used as &#x60;LocationConstraint&#x60; on bucket creation.*  |  |


