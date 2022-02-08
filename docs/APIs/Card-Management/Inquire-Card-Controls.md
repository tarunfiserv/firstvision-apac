# Inquire Card Controls

This service fetches the card controls for a given card number like maximum number and amount of retail/OTC/Single ATM authorization allowed on card number as well as single otc cash/Retail authorization allowed.

## Endpoint

`GET v1/cards/{cardNumber}/controlDetails`

## Payload Example

### Request Payload

>Shoud be empty.  
***The Business Unit and Card Number should be sent as query parameters and path variable.***

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/cards/{cardNumber}/controlDetails).

The below table identifies the required query parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 3 | Identification number of the organization associated with the account. |
| `cardNumber` | Path Variable | *string* | 19 | Token Number associated with the clear PAN. |

### Successful Response Payload

```json
{
  "businessUnit": 600,
  "cardSequence": 1,
  "maximumNumberRetailAuthorizationsAllowed": 999999999,
  "maximumAmountSingleATMTransactionAllowed": "$2,000.00",
  "singleOTCCashAuthorizationAllowed": "$0.00",
  "postToAccountNumber": "0006000022000000076",
  "maximumAmountATMCashAuthorizationsAllowed": "$1,000.00",
  "maximumNumberOTCAuthorizationsAllowed": 999999999,
  "maximumNumberATMCashAuthorizationsAllowed": 999999999,
  "singleRetailAuthorizationAllowed": "$999,999,999,999,999.99",
  "maximumAmountRetailAuthorizationsAllowed": "$1,000.00",
  "maximumAuthorizationsFrequnecy": 1,
  "maximumAmountOTCCashAuthorizationsAllowed": "string"
}
```

### Error Response Payload

```json
{
  "errorCode": "V5ED4003EQ",
  "errorMessage": "Post to acct for dual org not on file"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
|`V5ED4001EC` |Dual org not found or add pending|
|`V5ED4003EQ` |Post to acct for dual org not on file|