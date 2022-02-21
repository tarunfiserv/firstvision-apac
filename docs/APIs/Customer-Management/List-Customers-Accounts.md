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
  "accountList": [
    {
      "accountnumber": "0001000011000052268",
      "amountmemocredit": "$0.00",
      "amountmemodebit": "$0.00",
      "blockcode1": " ",
      "blockcode1date": "00/00/0000",
      "blockcode2": " ",
      "blockcode2date": "00/00/0000",
      "businessunit": "100",
      "ddaaccountnumber": "890005226",
      "internalstatus": "D",
      "mailingindicator": " ",
      "nbroftokenizedcards": "0",
      "product": "1",
      "reisscontolmethod": "0",
      "suppresstoken": "0"
    }
  ],
  "addressLine1": "62 CHARTERIS DR",
  "addressLine2": "",
  "addressLine3": "",
  "addressLine4": "",
  "billingLvl": "0",
  "businessUnit": "0",
  "creditLimit": "$0.00",
  "customerName": "UATMFNCU448",
  "customerNumber": "0001000000000113902",
  "dateOfBirth": "14/11/1940",
  "emailAddress": "UATMFNCU448@GMAIL.COM",
  "gender": "0",
  "homeDistricName": "",
  "homePhoneNumber": "++61430010348",
  "mobileNumber": "++61430010348",
  "nameLine1": "UATMFNCU448 TWOPPPUATMLNCUST448",
  "numberOfAccounts": "1",
  "numberOfCards": "1",
  "relName": "",
  "relationshipNbr": "",
  "ssnId": "113902",
  "status": "",
  "totalAvailable": "$0.00",
  "userDefinedField4": "",
  "workPhoneNumber": "++61430010348"
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
