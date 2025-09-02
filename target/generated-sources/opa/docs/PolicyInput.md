

# PolicyInput


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**userId** | **String** |  |  [optional] |
|**paymentId** | **String** |  |  [optional] |
|**action** | [**ActionEnum**](#ActionEnum) |  |  |
|**amountCents** | **Long** |  |  |
|**currency** | **String** |  |  [optional] |
|**context** | **Map&lt;String, String&gt;** |  |  [optional] |



## Enum: ActionEnum

| Name | Value |
|---- | -----|
| CREATE | &quot;create&quot; |
| REFUND | &quot;refund&quot; |
| CANCEL | &quot;cancel&quot; |



