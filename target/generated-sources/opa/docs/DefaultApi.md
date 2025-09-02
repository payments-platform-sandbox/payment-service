# DefaultApi

All URIs are relative to *http://localhost:8081*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**evaluatePaymentPolicy**](DefaultApi.md#evaluatePaymentPolicy) | **POST** /v1/decision/payments/allow | Evaluate payment policy |



## evaluatePaymentPolicy

> PolicyDecision evaluatePaymentPolicy(policyInput)

Evaluate payment policy

### Example

```java
// Import classes:
import com.pps.sdk.opa.ApiClient;
import com.pps.sdk.opa.ApiException;
import com.pps.sdk.opa.Configuration;
import com.pps.sdk.opa.models.*;
import com.pps.sdk.opa.api.DefaultApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("http://localhost:8081");

        DefaultApi apiInstance = new DefaultApi(defaultClient);
        PolicyInput policyInput = new PolicyInput(); // PolicyInput | 
        try {
            PolicyDecision result = apiInstance.evaluatePaymentPolicy(policyInput);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling DefaultApi#evaluatePaymentPolicy");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Reason: " + e.getResponseBody());
            System.err.println("Response headers: " + e.getResponseHeaders());
            e.printStackTrace();
        }
    }
}
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **policyInput** | [**PolicyInput**](PolicyInput.md)|  | |

### Return type

[**PolicyDecision**](PolicyDecision.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Decision |  -  |

