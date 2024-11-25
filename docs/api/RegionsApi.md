# RegionsApi

All URIs are relative to *https://s3.ionos.com*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**regionsFindByRegion**](RegionsApi.md#regionsfindbyregion) | **GET** /regions/{region} | Retrieve Region |
| [**regionsGet**](RegionsApi.md#regionsget) | **GET** /regions | Retrieve all Regions |


<a name="regionsFindByRegion"></a>
# **regionsFindByRegion**
> RegionRead regionsFindByRegion(region)

Retrieve Region

Returns the Region by Region.

### Example
```java
// Import classes:
import com.ionoscloud.objectstoragemanagement.ApiClient;
import com.ionoscloud.objectstoragemanagement.ApiException;
import com.ionoscloud.objectstoragemanagement.ApiResponse;
import com.ionoscloud.objectstoragemanagement.Configuration;
import com.ionoscloud.objectstoragemanagement.auth.*;
import com.ionoscloud.objectstoragemanagement.model.*;
import com.ionoscloud.objectstoragemanagement.api.RegionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    
    RegionsApi apiInstance = new RegionsApi(defaultClient);
    String region = "eu-central-3"; // String | The Region of the Region.
    try {
      ApiResponse<RegionRead> result = apiInstance.regionsFindByRegionWithHttpInfo(region);
      System.out.println("Response: " + result.getData());
      System.out.println("Status Code: " + result.getStatusCode());
      System.out.println("Headers: " + result.getHeaders());
    } catch (ApiException e) {
      System.err.println("Exception when calling RegionsApi#regionsFindByRegion");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```
⚠️ **Note**: for the example above, you need to provide all parameters to the method call. Null values will resolve to the API defaults.

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **region** | **String**| The Region of the Region. |

### Return type

[**RegionRead**](../models/RegionRead.md)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="regionsGet"></a>
# **regionsGet**
> RegionReadList regionsGet(offset, limit)

Retrieve all Regions

This endpoint enables retrieving all Regions using pagination and optional filters. 

### Example
```java
// Import classes:
import com.ionoscloud.objectstoragemanagement.ApiClient;
import com.ionoscloud.objectstoragemanagement.ApiException;
import com.ionoscloud.objectstoragemanagement.ApiResponse;
import com.ionoscloud.objectstoragemanagement.Configuration;
import com.ionoscloud.objectstoragemanagement.auth.*;
import com.ionoscloud.objectstoragemanagement.model.*;
import com.ionoscloud.objectstoragemanagement.api.RegionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    
    RegionsApi apiInstance = new RegionsApi(defaultClient);
    Integer offset = 0; // Integer | The first element (of the total list of elements) to include in the response. Use together with limit for pagination.
    Integer limit = 100; // Integer | The maximum number of elements to return. Use together with offset for pagination.
    String orderBy = "orderBy_example"; // String | Order by field
    Integer maxResults = "maxResults_example"; // Integer | Maximum number of results to return
    try {
      ApiResponse<RegionReadList> result = apiInstance.regionsGetWithHttpInfo(offset, limit, orderBy, maxResults, filters);
      System.out.println("Response: " + result.getData());
      System.out.println("Status Code: " + result.getStatusCode());
      System.out.println("Headers: " + result.getHeaders());
    } catch (ApiException e) {
      System.err.println("Exception when calling RegionsApi#regionsGet");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```
⚠️ **Note**: for the example above, you need to provide all parameters to the method call. Null values will resolve to the API defaults.

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **offset** | **Integer**| The first element (of the total list of elements) to include in the response. Use together with limit for pagination. | [optional] [default to 0]
| **limit** | **Integer**| The maximum number of elements to return. Use together with offset for pagination. | [optional] [default to 100]

### Return type

[**RegionReadList**](../models/RegionReadList.md)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

