# Spend Limit Updates

This service is used to update the spending limits to control the card usage.  These limits are set at individual card level.

## Endpoint

`PUT /v1/cards/{cardNumber}/spendLimits`

## Payload Example

### Request Payload

```json
{
  "maximumAuthorizationsFrequency": "1",
  "maximumAmountATMCashAuthorizationsAllowed": "10000",
  "maximumNumberATMCashAuthorizationsAllowed": 1,
  "maximumAmountSingleATMTransactionAllowed": 10000,
  "maximumNumberOTCAuthorizationsAllowed": 1,
  "maximumAmountOTCCashAuthorizationsAllowed": 2000,
  "singleOTCCashAuthorizationAllowed": 10000,
  "maximumAmountRetailAuthorizationsAllowed": 1000,
  "maximumNumberRetailAuthorizationsAllowed": 1,
  "singleRetailAuthorizationAllowed": "0000"  
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/cards/{cardNumber}/spendLimits).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 3 | Identification number of the organization associated with the account. |
| `cardNumber` | Path Variable | *string* | 19 | Token Number associated with the clear PAN. |
| `maximumAuthorizationsFrequency` | Payload | *number* | 1 | Limit frequency to update. Valid values are a) "1"  Daily limits b) "2" Cycle to Date limits c) "3" Year to Date limits  |
| `maximumAmountSingle***TransactionAllowed` | Payload | *number* | 09 | Maximum amount of the Single ***(ATM / OTC / Retail) transaction allowed. |
| `maximumNumber***AuthorizationsAllowed` | Payload | *number* | 09 | Maximum number of the cumulatative ***(ATM / OTC / Retail) transaction allowed for a given frequency (daily / CTD/ YTD). |
| `maximumAmount***AuthorizationsAllowed` | Payload | *number* | 17 | Maximum amount of the cumulatative ***(ATM / OTC / Retail) transaction allowed for a given frequency (daily / CTD/ YTD). |

### Successful Response Payload

```json
{
  "businessUnit": 100,
  "cardSequence": 0,
  "maximumNumberRetailAuthorizationsAllowed": 1,
  "maximumAmountSingleATMTransactionAllowed": "1000",
  "singleOTCCashAuthorizationAllowed": "100",
  "postToAccountNumber": "0001000CCCCCC510760",
  "maximumAmountATMCashAuthorizationsAllowed": "100",
  "maximumNumberOTCAuthorizationsAllowed": 1,
  "maximumNumberATMCashAuthorizationsAllowed": 1,
  "singleRetailAuthorizationAllowed": "0",
  "maximumAmountRetailAuthorizationsAllowed": "1000",
  "maximumAuthorizationsFrequnecy": "1",
  "maximumAmountOTCCashAuthorizationsAllowed": "2000",
  "cardNumber": "00098468CCCCC273605"    
}
```

### Error Response Payload

```json
{
  "errorCode": "V5ED0319ED",
  "errorMessage": "Atm cash amt field update is not allowed"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
|`V5ED4001SA` |Business Unit not found|
|`V5ED4001SB` |Business Unit is in add pending status|
|`V5ED4001SC` |Business Unit is in purged status|
|`V5ED4001SE` |Invalid Business Unit|
|`V5ED0010SF` |Update request - record not found|
|`V5ED0011SF` |Update request - record add pending|
|`V5ED4003ED` |Card seq number must be greater than zero|
|`V5ED4004SF` |Invalid card sequence|
|`V5ED0319ED` |Atm cash amt field update is not allowed|
|`V5ED0328EA` |Maximum freq input not allowed when no auth limit overrd|
|`V5ED0320EE` |Atm cash nbr field update is not allowed |
|`V5ED0321EH` |Txn limit atm field update is not allowed |
|`V5ED0322EF` |OTC cash amt field update is not allowed|  
|`V5ED0323EG` |OTC cash nbr field update is not allowed|
|`V5ED0324EI` |Txn limit otc field update is not allowed |
|`V5ED0325EB` |Retail amt field update is not allowed |
|`V5ED0326EC` |Retail nbr field update is not allowed|
|`V5ED0327EJ` |Txn limit retail field update is not allowed|  
