# Update Credit Limit

This service is used to update the credit limit of the cardholder’s account. 

## Endpoint

`PUT /v1/accounts/{accountNumber}/creditLimit?businessUnit=nnn`

## Payload Example

### Request Payload

```json
{
  "creditLimit": 50   
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/accounts/{accountNumber}/creditLimit).

The below table identifies the required parameters in the request payload.

| Variable | Type | Length | Description/Values |
| -------- | :--: | :------------: | ------------------ |
| `businessUnit` | *number* | 3 | Identification number of the organization associated with the account. |
| `accountNumber` | *string* | 19 | Account Number of the cardholder. | 
| `creditLimit` | *string* | 17 | Credit limit of the account. |

### Successful Response Payload

```json
{
  "accountNumber": "0006000011000000103",
  "businessUnit": "600",
  "creditLimit": "$10.00",
  "creditLimitDate": "19/08/2021"
}
```

### Error Response Payload

```json
{
  "errorCode": "V5BS0010SF",
  "errorMessage": " Update Request - Record not found "
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0103SA` | Credit limit not maintained if AMRM-CLM-SUB-NOT-ALLOWED|
| `V5BS0103SC` | Input Credit limit cannot be greater than logo credit limit |
| `V5BS0103SD` | Credit limit exceeds secured amount use |
| `V5BS0103SE` | Credit limit does not conform to currency NOD |  
| `V5BS0103SF` | Credit limit required |
| `V5BS0010SF` | Update Request - Record not found |
