# AccesskeysApi

All URIs are relative to *https://s3.ionos.com*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**accesskeysDelete**](AccesskeysApi.md#accesskeysdelete) | **DELETE** /accesskeys/{accesskeyId} | Delete AccessKey |
| [**accesskeysFindById**](AccesskeysApi.md#accesskeysfindbyid) | **GET** /accesskeys/{accesskeyId} | Retrieve AccessKey |
| [**accesskeysGet**](AccesskeysApi.md#accesskeysget) | **GET** /accesskeys | Retrieve all Accesskeys |
| [**accesskeysPost**](AccesskeysApi.md#accesskeyspost) | **POST** /accesskeys | Create AccessKey |
| [**accesskeysPut**](AccesskeysApi.md#accesskeysput) | **PUT** /accesskeys/{accesskeyId} | Ensure AccessKey |
| [**accesskeysRenew**](AccesskeysApi.md#accesskeysrenew) | **PUT** /accesskeys/{accesskeyId}/renew | Ensure AccessKey |


<a name="accesskeysDelete"></a>
# **accesskeysDelete**
> accesskeysDelete(accesskeyId)

Delete AccessKey

Deletes the specified AccessKey.

### Example
```java
// Import classes:
import com.ionoscloud.objectstoragemanagement.ApiClient;
import com.ionoscloud.objectstoragemanagement.ApiException;
import com.ionoscloud.objectstoragemanagement.ApiResponse;
import com.ionoscloud.objectstoragemanagement.Configuration;
import com.ionoscloud.objectstoragemanagement.auth.*;
import com.ionoscloud.objectstoragemanagement.model.*;
import com.ionoscloud.objectstoragemanagement.api.AccesskeysApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    
    AccesskeysApi apiInstance = new AccesskeysApi(defaultClient);
    UUID accesskeyId = new UUID(); // UUID | The ID (UUID) of the AccessKey.
    try {
      apiInstance.accesskeysDeleteWithHttpInfo(accesskeyId);
    } catch (ApiException e) {
      System.err.println("Exception when calling AccesskeysApi#accesskeysDelete");
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
| **accesskeyId** |  [**UUID**](../models/.md)| The ID (UUID) of the AccessKey. |

### Return type

null (empty response body)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="accesskeysFindById"></a>
# **accesskeysFindById**
> AccessKeyRead accesskeysFindById(accesskeyId)

Retrieve AccessKey

Returns the AccessKey by ID.

### Example
```java
// Import classes:
import com.ionoscloud.objectstoragemanagement.ApiClient;
import com.ionoscloud.objectstoragemanagement.ApiException;
import com.ionoscloud.objectstoragemanagement.ApiResponse;
import com.ionoscloud.objectstoragemanagement.Configuration;
import com.ionoscloud.objectstoragemanagement.auth.*;
import com.ionoscloud.objectstoragemanagement.model.*;
import com.ionoscloud.objectstoragemanagement.api.AccesskeysApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    
    AccesskeysApi apiInstance = new AccesskeysApi(defaultClient);
    UUID accesskeyId = new UUID(); // UUID | The ID (UUID) of the AccessKey.
    try {
      ApiResponse<AccessKeyRead> result = apiInstance.accesskeysFindByIdWithHttpInfo(accesskeyId);
      System.out.println("Response: " + result.getData());
      System.out.println("Status Code: " + result.getStatusCode());
      System.out.println("Headers: " + result.getHeaders());
    } catch (ApiException e) {
      System.err.println("Exception when calling AccesskeysApi#accesskeysFindById");
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
| **accesskeyId** |  [**UUID**](../models/.md)| The ID (UUID) of the AccessKey. |

### Return type

[**AccessKeyRead**](../models/AccessKeyRead.md)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="accesskeysGet"></a>
# **accesskeysGet**
> AccessKeyReadList accesskeysGet(offset, limit, filterAccesskeyId)

Retrieve all Accesskeys

This endpoint enables retrieving all Accesskeys using pagination and optional filters. 

### Example
```java
// Import classes:
import com.ionoscloud.objectstoragemanagement.ApiClient;
import com.ionoscloud.objectstoragemanagement.ApiException;
import com.ionoscloud.objectstoragemanagement.ApiResponse;
import com.ionoscloud.objectstoragemanagement.Configuration;
import com.ionoscloud.objectstoragemanagement.auth.*;
import com.ionoscloud.objectstoragemanagement.model.*;
import com.ionoscloud.objectstoragemanagement.api.AccesskeysApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    
    AccesskeysApi apiInstance = new AccesskeysApi(defaultClient);
    Integer offset = 0; // Integer | The first element (of the total list of elements) to include in the response. Use together with limit for pagination.
    Integer limit = 100; // Integer | The maximum number of elements to return. Use together with offset for pagination.
    String filterAccesskeyId = "filterAccesskeyId_example"; // String | The accesskey ID to filter by.
    String orderBy = "orderBy_example"; // String | Order by field
    Integer maxResults = "maxResults_example"; // Integer | Maximum number of results to return
    try {
      ApiResponse<AccessKeyReadList> result = apiInstance.accesskeysGetWithHttpInfo(offset, limit, filterAccesskeyId, orderBy, maxResults, filters);
      System.out.println("Response: " + result.getData());
      System.out.println("Status Code: " + result.getStatusCode());
      System.out.println("Headers: " + result.getHeaders());
    } catch (ApiException e) {
      System.err.println("Exception when calling AccesskeysApi#accesskeysGet");
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
| **filterAccesskeyId** | **String**| The accesskey ID to filter by. | [optional]

### Return type

[**AccessKeyReadList**](../models/AccessKeyReadList.md)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="accesskeysPost"></a>
# **accesskeysPost**
> AccessKeyRead accesskeysPost(accessKeyCreate)

Create AccessKey

Creates a new AccessKey.  The full AccessKey needs to be provided to create the object. Optional data will be filled with defaults or left empty. 

### Example
```java
// Import classes:
import com.ionoscloud.objectstoragemanagement.ApiClient;
import com.ionoscloud.objectstoragemanagement.ApiException;
import com.ionoscloud.objectstoragemanagement.ApiResponse;
import com.ionoscloud.objectstoragemanagement.Configuration;
import com.ionoscloud.objectstoragemanagement.auth.*;
import com.ionoscloud.objectstoragemanagement.model.*;
import com.ionoscloud.objectstoragemanagement.api.AccesskeysApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    
    AccesskeysApi apiInstance = new AccesskeysApi(defaultClient);
    AccessKeyCreate accessKeyCreate = new AccessKeyCreate(); // AccessKeyCreate | AccessKey to create.
    try {
      ApiResponse<AccessKeyRead> result = apiInstance.accesskeysPostWithHttpInfo(accessKeyCreate);
      System.out.println("Response: " + result.getData());
      System.out.println("Status Code: " + result.getStatusCode());
      System.out.println("Headers: " + result.getHeaders());
    } catch (ApiException e) {
      System.err.println("Exception when calling AccesskeysApi#accesskeysPost");
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
| **accessKeyCreate** |  [**AccessKeyCreate**](../models/AccessKeyCreate.md)| AccessKey to create. |

### Return type

[**AccessKeyRead**](../models/AccessKeyRead.md)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="accesskeysPut"></a>
# **accesskeysPut**
> AccessKeyRead accesskeysPut(accesskeyId, accessKeyEnsure)

Ensure AccessKey

Ensures that the AccessKey with the provided ID is created or modified. The full AccessKey needs to be provided to ensure (either update or create) the AccessKey. Non present data will only be filled with defaults or left empty, but not take previous values into consideration. 

### Example
```java
// Import classes:
import com.ionoscloud.objectstoragemanagement.ApiClient;
import com.ionoscloud.objectstoragemanagement.ApiException;
import com.ionoscloud.objectstoragemanagement.ApiResponse;
import com.ionoscloud.objectstoragemanagement.Configuration;
import com.ionoscloud.objectstoragemanagement.auth.*;
import com.ionoscloud.objectstoragemanagement.model.*;
import com.ionoscloud.objectstoragemanagement.api.AccesskeysApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    
    AccesskeysApi apiInstance = new AccesskeysApi(defaultClient);
    UUID accesskeyId = new UUID(); // UUID | The ID (UUID) of the AccessKey.
    AccessKeyEnsure accessKeyEnsure = new AccessKeyEnsure(); // AccessKeyEnsure | update AccessKey
    try {
      ApiResponse<AccessKeyRead> result = apiInstance.accesskeysPutWithHttpInfo(accesskeyId, accessKeyEnsure);
      System.out.println("Response: " + result.getData());
      System.out.println("Status Code: " + result.getStatusCode());
      System.out.println("Headers: " + result.getHeaders());
    } catch (ApiException e) {
      System.err.println("Exception when calling AccesskeysApi#accesskeysPut");
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
| **accesskeyId** |  [**UUID**](../models/.md)| The ID (UUID) of the AccessKey. |
| **accessKeyEnsure** |  [**AccessKeyEnsure**](../models/AccessKeyEnsure.md)| update AccessKey |

### Return type

[**AccessKeyRead**](../models/AccessKeyRead.md)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="accesskeysRenew"></a>
# **accesskeysRenew**
> AccessKeyRead accesskeysRenew(accesskeyId)

Ensure AccessKey

Renew will replace the existing secret access key with a new one. 

### Example
```java
// Import classes:
import com.ionoscloud.objectstoragemanagement.ApiClient;
import com.ionoscloud.objectstoragemanagement.ApiException;
import com.ionoscloud.objectstoragemanagement.ApiResponse;
import com.ionoscloud.objectstoragemanagement.Configuration;
import com.ionoscloud.objectstoragemanagement.auth.*;
import com.ionoscloud.objectstoragemanagement.model.*;
import com.ionoscloud.objectstoragemanagement.api.AccesskeysApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    
    AccesskeysApi apiInstance = new AccesskeysApi(defaultClient);
    UUID accesskeyId = new UUID(); // UUID | The ID (UUID) of the AccessKey that should be ensured.
    try {
      ApiResponse<AccessKeyRead> result = apiInstance.accesskeysRenewWithHttpInfo(accesskeyId);
      System.out.println("Response: " + result.getData());
      System.out.println("Status Code: " + result.getStatusCode());
      System.out.println("Headers: " + result.getHeaders());
    } catch (ApiException e) {
      System.err.println("Exception when calling AccesskeysApi#accesskeysRenew");
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
| **accesskeyId** |  [**UUID**](../models/.md)| The ID (UUID) of the AccessKey that should be ensured. |

### Return type

[**AccessKeyRead**](../models/AccessKeyRead.md)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

