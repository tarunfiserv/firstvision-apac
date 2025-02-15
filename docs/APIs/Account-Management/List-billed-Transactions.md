# List billed Transactions

 The service provides list of transactions along with detail information of transactions posted in the last statement cycle.

## Endpoint

`GET /v1/accounts/{accountNumber}/transactions/lastStatement`

## Payload Example

### Request Payload

```json
{
Shoud be empty.
***The Business Unit/Product/Statement date and Account Number should be sent as query parameters and path variable.***
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountNumber}/transactions/lastStatement).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountNumber` | Path Variable | *string* | 19 | Account Number of the cardholder. | 
| `businessUnit` | Query Parameter | *number* | 3 | Identification number of the organization associated with the account. |
| `product` | Query Parameter | *number* | 3 | Product associated with the Account. |
| `statementDate` | Query Parameter | *Date* | DD/MM/YYYY | Date the statement is produced for the account holder |

### Successful Response Payload

```json

{
  "tranPrevToken": "2000002000010000001211202109y50003",
  "planNextTokenLast": " ",
  "transactionList": [
    {
      "recordNumber": 0,
      "amount": "$61.40",
      "businessUnit": 200,
      "authorizationCode": 49461,
      "description": "MBS SPORT Paya Lebar SG ",
      "postingDate": "26/03/2021",
      "transactionCode": 0,
      "reference": "VT210850003000020000014",
      "transactionType": "M",
      "creditPlan": 10002,
      "logo": 1,
      "logicModule": 1,
      "effectiveDate": "26/03/2021"
    }
  ],
  "tranNextToken": "2000002000010000001211202109y50052",
  "accountRelationship": 2000010000001211,
  "planPrevTokenLast": " ",
  "statementDate": "2021-09-03"
}
```

### Error Response Payload

```json
{
  "errorCode": "V5S34003SA",
  "errorMessage": "No Statement History information found on file"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0011SF` |Update Request - Record Add Pending|
| `V5BS4001EA` |Invalid Business Unit|
| `V5BS4001SC` |Business Unit is in Purged Status|
| `V5BS4002SA` |Invalid Account Number|  
| `V5S34003SA` |No Statement History information found on file|
