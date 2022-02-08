# Update Card Controls

This service updates the card controls for a given card number like ECOM Active switch, ATM Flag, International ATM POS Flag, MOTO Flag etc.

  
## Endpoint

`PUT /v1/cards/{cardNumber}/controls`

## Payload Example

### Request Payload

```json
{
  "ecomActSW": "",
  "aTMFlag": " ",
  "iNTATMPOSFlag": "Y",
  "mOTOFlag": "Y",
  "pOSFlag": " ",
  "cashBackTranFlag": "Y",
  "pAYwaveFlag": "N"
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

### Successful Response Payload

```json
{
  "ecomActSW": "string",
  "businessUnit": 600,
  "cardSequence": 1,
  "aTMFlag": " ",
  "iNTATMPOSFlag": "Y",
  "mOTOFlag": "Y",
  "pOSFlag": " ",
  "cashBackTranFlag": "Y",
  "postToAccountNumber": "0006000022000000076",
  "cardNumber": "0000000001000000115",
  "pAYwaveFlag": "N"
}
```

### Error Response Payload

```json
{
  "errorCode": "V5ED4001EC",
  "errorMessage": "Dual Org Not Found Or Add Pending"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5ED4001EC` | Dual Org Not Found Or Add Pending |         
| `V5ED4003EQ` | Post To Acct For Dual Org Not On File |
| `V5ED8117EA` | Ecommerce Act Flag Should Be 0 Or 1 |
| `V5ED8120CX` | Saving Acct Nbr(Or)Cheque Acct Any One Should Be Value |
