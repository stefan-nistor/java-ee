# EmployeeApi

All URIs are relative to *http://localhost/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getEmployeeDetails**](EmployeeApi.md#getEmployeeDetails) | **GET** /findEmployeeDetails/{employeeId} | Find employee by ID


<a name="getEmployeeDetails"></a>
# **getEmployeeDetails**
> Employee getEmployeeDetails(employeeId)

Find employee by ID

Returns a single Employee

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EmployeeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost/v1");

    EmployeeApi apiInstance = new EmployeeApi(defaultClient);
    Long employeeId = 56L; // Long | ID of Employee to return
    try {
      Employee result = apiInstance.getEmployeeDetails(employeeId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmployeeApi#getEmployeeDetails");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **employeeId** | **Long**| ID of Employee to return |

### Return type

[**Employee**](Employee.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | successful operation |  -  |
**400** | Invalid Employee ID supplied |  -  |
**404** | Employee not found |  -  |

