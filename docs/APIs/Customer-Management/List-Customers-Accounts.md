# List Customers' Accounts

 The service provides list of accounts associated with the customer.

## Endpoint

`GET /v1/customers/{customerNumber}/accountList`

## Payload Example

### Request Payload

>Shoud be empty.  
***Customer Number should be sent as Path Variable.***  

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/customers/{customerNumber}/accountList).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `customerNumber` | Path Variable | *string* | 19 | An identifier of the customer. |

### Successful Response Payload

```json
{
  "totalAvailable": "$0.00",
  "businessUnit": "string",
  "homePhoneNumber": "string",
  "ssnId": "string",
  "gender": "string",
  "mobileNumber": "string",
  "nameLine1": "string",
  "emailAddress": "string",
  "workPhoneNumber": "string",
  "addressLine1": "string",
  "creditLimit": "$0.00\"",
  "addressLine2": "string",
  "addressLine3": "string",
  "addressLine4": "string",
  "billingLvl": 0,
  "userDefinedField4": "string",
  "numberOfAccounts": "string",
  "dateOfBirth": "string",
  "customerNumber": "string",
  "customerName": "string",
  "homeDistricName": "string",
  "relName": " ",
  "accountList": [
    {
      "product": 1,
      "businessUnit": "string",
      "amountMemoCredit": "string",
      "ddaAccountNumber": "string",
      "mailingIndicator": "string",
      "blockCode2Date": "string",
      "accountNumber": "string",
      "suppressToken": "string",
      "internalStatus": "string",
      "reissContolMethod": 0,
      "amountMemoDebit": "string",
      "nbrOfTokenizedCards": 0,
      "blockCode1": "string",
      "blockCode2": "string",
      "blockCode1Date": "string"
    }
  ],
  "numberOfCards": "string",
  "relationshipNbr": "string",
  "status": ""
}

```

### Error Response Payload

```json
{
  "errorCode": "V5DB4001AS",
  "errorMessage": "Cust nbr not found"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5DB4001AS` |Cust nbr not found|
