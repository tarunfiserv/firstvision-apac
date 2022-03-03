# Update Card Controls

This service updates the card controls for a given card number like ECOM Active switch, ATM Flag, International ATM POS Flag, MOTO Flag and max Amount ATM/OTC/Retail etc.

  
## Endpoint

`PUT /v1/cards/{cardNumber}/controls`

## Payload Example

### Request Payload

```json
{
"maximumAmountOtcCashAuthorizationsAllowed": 1000,
"maximumNumberRetailAuthorizationsAllowed": 2,
"motoFlag": "Y",
"payWaveSwitch": "N",
"maximumNumberOtcAuthorizationsAllowed": 5,
"cashBackTranFlag": "Y",
"maximumNumberAtmCashAuthorizationsAllowed": 10,
"singleOtcCashAuthorizationAllowed": 1200,
"maximumAmountSingleAtmTransactionAllowed": 1000,
"singleRetailAuthorizationAllowed": 1600,
"maximumAmountRetailAuthorizationsAllowed": 1000,
"ecomActiveSwitch": 0,
"atmFlag": "Y",
"posFlag": "N",
"maximumAmountAtmCashAuthorizationsAllowed": 1000,
"maximumAuthorizationsFrequnecy": 1,
"intAtmPosFlag": "Y"
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/cards/{cardNumber}/controls).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 3 | Identification number of the organization associated with the account. |
| `cardNumber` | Path Variable | *string* | 19 | Token Number associated with the clear PAN. | 
| `ecomActSW` | Payload | *string* | 1 |  ECOM Active switch. | 
| `aTMFlag` | Payload | *string* | 1 | ATM Flag. | 
| `iNTATMPOSFlag` | Payload | *string* | 1 | International ATM POS Flag. | 
| `mOTOFlag` | Payload | *string* | 1 | MOTO Flag. | 
| `pOSFlag` | Payload | *string* | 1 | POS Flag. | 
| `cashBackTranFlag` | Payload | *string* | 1 | Cash Back Transaction Flag. | 
| `pAYwaveFlag` | Payload | *string* | 1 | Pay Wave Switch. | 
| `maximumAuthorizationsFrequency` | Payload | *number* | 1 | Limit frequency to update. Valid values are a) "1"  Daily limits b) "2" Cycle to Date limits c) "3" Year to Date limits  |
| `maximumAmountSingle***TransactionAllowed` | Payload | *number* | 09 | Maximum amount of the Single ***(ATM / OTC / Retail) transaction allowed. |
| `maximumNumber***AuthorizationsAllowed` | Payload | *number* | 09 | Maximum number of the cumulatative ***(ATM / OTC / Retail) transaction allowed for a given frequency (daily / CTD/ YTD). |
| `maximumAmount***AuthorizationsAllowed` | Payload | *number* | 17 | Maximum amount of the cumulatative ***(ATM / OTC / Retail) transaction allowed for a given frequency (daily / CTD/ YTD). |


### Successful Response Payload

```json
{
  "maximumAmountOtcCashAuthorizationsAllowed": 1000,
  "businessUnit": 100,
  "maximumNumberRetailAuthorizationsAllowed": 2,
  "motoFlag": "Y",
  "payWaveSwitch": "N",
  "maximumNumberOtcAuthorizationsAllowed": 5,
  "cashBackTranFlag": "Y",
  "maximumNumberAtmCashAuthorizationsAllowed": 10,
  "singleOtcCashAuthorizationAllowed": 1200,
  "maximumAmountSingleAtmTransactionAllowed": 1000,
  "singleRetailAuthorizationAllowed": 1600,
  "maximumAmountRetailAuthorizationsAllowed": 1000,
  "ecomActiveSwitch": 0,
  "atmFlag": "Y",
  "posFlag": "N",
  "maximumAmountAtmCashAuthorizationsAllowed": 1000,
  "maximumAuthorizationsFrequnecy": 1,
  "intAtmPosFlag": "Y",
  "cardNumber": 9846801010434752
}
```

### Error Response Payload

```json
{
  "errorCode": "V5ED8120CX",
  "errorMessage": "Saving Acct nbr(or)Cheque Acct Any One Should Be Value"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5ED8120CX` | Saving Acct nbr(or)Cheque Acct Any One Should Be Value |        
| `V5ED0328EA` | Maximum Freq Input Not Allowed When No Auth Limit Overrd | 
| `V5ED0319ED` | Atm Cash Amt Field Update Is Not Allowed | 
| `V5ED0319EF` | New Atm Cash Amt Is Greater Than Allowable Limit | 
| `V5ED0320EE` | Atm Cash Nbr Field Update Is Not Allowed | 
| `V5ED0321EH` | Txn Limit Atm Field Update Is Not Allowed | 
| `V5ED0322EF` | Otc Cash Amt Field Update Is Not Allowed | 
| `V5ED0323EG` | Otc Cash Nbr Field Update Is Not Allowed | 
| `V5ED0324EI` | Txn Limit Otc Field Update Is Not Allowed | 
| `V5ED0325EB` | Retail Amt Field Update Is Not Allowed | 
| `V5ED0325EC` | New Retail Amt Is Greater Than Allowable Limit | 
| `V5ED0326EC` | Retail Nbr Field Update Is Not Allowed | 
| `V5ED0327EJ` | Txn Limit Retail Field Update Is Not Allowed  | 