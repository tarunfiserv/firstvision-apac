# List unbilled transactions

This service provides details of the unbilled transactions posted on a given account.

## Endpoint

`GET /v1/accounts/{accountRelationshipNBR}/transactions/cycleToDate`

## Payload Example

### Request Payload

```json
{
Shoud be empty.
***The Business Unit and Account Number should be sent as query parameters and path variable.***
}
``` 

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountRelationshipNBR}/transactions/cycleToDate).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountNumber` | Path Variable | *string* | 19 | Account Number of the cardholder. |
| `businessUnit` | Query Parameter | *number* | 3 | Identification number of the organization associated with the account. |

### Successful Response Payload

```json
{
  "aRIndicator": "A",
  "accountNumber": "0000000001000000073",
  "businessUnit": "600",
  "fileFlag": "",
  "fileFlag1": "Y",
  "product": "600",
  "transactionList": [
    {
      "amount": "$8,200.00",
      "authorizationCode": " ",
      "creditPlan": "70001",
      "date": "0",
      "description": "INTEREST/PRIN DEBIT8",
      "effectiveDate": "18/08/2021",
      "logicModule": "1",
      "postingDate": "18/08/2021",
      "recordNumber": "10",
      "reference": "19999999980818199970020",
      "time": "0",
      "transactionCode": "1614",
      "typeOfTransaction": "D"
    },
    {
      "amount": "$8,200.00",
      "authorizationCode": " ",
      "creditPlan": "70001",
      "date": "0",
      "description": "INTEREST/PRIN DEBIT8",
      "effectiveDate": "18/08/2021",
      "logicModule": "1",
      "postingDate": "18/08/2021",
      "recordNumber": "10",
      "reference": "19999999980818199970020",
      "time": "0",
      "transactionCode": "1614",
      "typeOfTransaction": "D"
    },
    {
      "amount": "$8,200.00",
      "authorizationCode": " ",
      "creditPlan": "70001",
      "date": "0",
      "description": "INTEREST/PRIN DEBIT8",
      "effectiveDate": "18/08/2021",
      "logicModule": "1",
      "postingDate": "18/08/2021",
      "recordNumber": "10",
      "reference": "19999999980818199970020",
      "time": "0",
      "transactionCode": "1614",
      "typeOfTransaction": "D"
    },
    {
      "amount": "$8,200.00",
      "authorizationCode": " ",
      "creditPlan": "70001",
      "date": "0",
      "description": "INTEREST/PRIN DEBIT8",
      "effectiveDate": "18/08/2021",
      "logicModule": "1",
      "postingDate": "18/08/2021",
      "recordNumber": "10",
      "reference": "19999999980818199970020",
      "time": "0",
      "transactionCode": "1614",
      "typeOfTransaction": "D"
    },
    {
      "amount": "$8,200.00",
      "authorizationCode": " ",
      "creditPlan": "70001",
      "date": "0",
      "description": "INTEREST/PRIN DEBIT8",
      "effectiveDate": "18/08/2021",
      "logicModule": "1",
      "postingDate": "18/08/2021",
      "recordNumber": "10",
      "reference": "19999999980818199970020",
      "time": "0",
      "transactionCode": "1614",
      "typeOfTransaction": "D"
    },
    {
      "amount": "$8,200.00",
      "authorizationCode": " ",
      "creditPlan": "70001",
      "date": "0",
      "description": "INTEREST/PRIN DEBIT8",
      "effectiveDate": "18/08/2021",
      "logicModule": "1",
      "postingDate": "18/08/2021",
      "recordNumber": "10",
      "reference": "19999999980818199970020",
      "time": "0",
      "transactionCode": "1614",
      "typeOfTransaction": "D"
    },
    {
      "amount": "$8,200.00",
      "authorizationCode": " ",
      "creditPlan": "70001",
      "date": "0",
      "description": "INTEREST/PRIN DEBIT8",
      "effectiveDate": "18/08/2021",
      "logicModule": "1",
      "postingDate": "18/08/2021",
      "recordNumber": "10",
      "reference": "19999999980818199970020",
      "time": "0",
      "transactionCode": "1614",
      "typeOfTransaction": "D"
    },
    {
      "amount": "$8,200.00",
      "authorizationCode": " ",
      "creditPlan": "70001",
      "date": "0",
      "description": "INTEREST/PRIN DEBIT8",
      "effectiveDate": "18/08/2021",
      "logicModule": "1",
      "postingDate": "18/08/2021",
      "recordNumber": "10",
      "reference": "19999999980818199970020",
      "time": "0",
      "transactionCode": "1614",
      "typeOfTransaction": "D"
    },
    {
      "amount": "$8,200.00",
      "authorizationCode": " ",
      "creditPlan": "70001",
      "date": "0",
      "description": "INTEREST/PRIN DEBIT8",
      "effectiveDate": "18/08/2021",
      "logicModule": "1",
      "postingDate": "18/08/2021",
      "recordNumber": "10",
      "reference": "19999999980818199970020",
      "time": "0",
      "transactionCode": "1614",
      "typeOfTransaction": "D"
    },
    {
      "amount": "$8,200.00",
      "authorizationCode": " ",
      "creditPlan": "70001",
      "date": "0",
      "description": "INTEREST/PRIN DEBIT8",
      "effectiveDate": "18/08/2021",
      "logicModule": "1",
      "postingDate": "18/08/2021",
      "recordNumber": "10",
      "reference": "19999999980818199970020",
      "time": "0",
      "transactionCode": "1614",
      "typeOfTransaction": "D"
    }
  ],
  "transactionType": "CYCLE-TO-DATE TRANSACTION"
}
```

