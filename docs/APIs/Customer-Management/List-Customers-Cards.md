# List Customers' Cards

 The service provides list of cards associated with the customer.

## Endpoint

`GET /v1/customers/{customerNumber}/cardList/`

## Payload Example

### Request Payload

>Shoud be empty.  
***Customer Number should be sent as Path Variable.***  

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/customers/{customerNumber}/cardList).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `customerNumber` | Path Variable | *string* | 19 | An identifier of the customer. |

### Successful Response Payload

```json
{
  "addressLine1": "62 CHARTERIS DR",
  "addressLine2": "",
  "addressLine3": "",
  "addressLine4": "",
  "billingLvl": "0",
  "businessUnit": "0",
  "cardList": [
    {
      "atmflag": "Y",
      "blockcode": " ",
      "blockdate": "00/00/0000",
      "businessunit": "100",
      "cardactivateddate": "00/00/0000",
      "cardexpirationdate": "16/09/2023",
      "cardholdertype": "1",
      "cardissuedate": "28/09/2020",
      "cardnumber": "0009846801010009405",
      "cardsequence": "1",
      "cardtechnology": "3",
      "cashbacktranflag": "Y",
      "chequeaccountnbr": " ",
      "currcardaction": "0",
      "currentcardneedactivation": "Y",
      "datelastplasticsupresed": "0",
      "datelastplasticused": "0",
      "datelastwalletused": "0",
      "dateopened": "17/09/2020",
      "digitalid": " ",
      "e-comactflag": "1",
      "embosserrecordstatus": "0",
      "embrname2": " ",
      "intatmposflag": "Y",
      "lastcardaction": "1",
      "lastcardexpirationdate": "00/00/0000",
      "lastcardneedactivation": "Y",
      "maskcardnumber": "000984680XXXXXX9405",
      "mcclimit-1": "$0.01",
      "mcclimit-10": "$0.00",
      "mcclimit-2": "$0.00",
      "mcclimit-3": "$0.00",
      "mcclimit-4": "$0.00",
      "mcclimit-5": "$0.00",
      "mcclimit-6": "$0.00",
      "mcclimit-7": "$0.00",
      "mcclimit-8": "$0.00",
      "mcclimit-9": "$0.00",
      "motoflag": " ",
      "nameoncard": "U T UATMLNCUST448",
      "numberofcards": "0",
      "paywaveflag": "Y",
      "pinoffset": "329861",
      "plasticsuppressstatus": "N",
      "posflag": "Y",
      "posttoaccount": "0001000011000052268",
      "product": "1",
      "productdescription": "VISA PLATINUM DEBIT",
      "savingsaccountnbr": " ",
      "timelastplasticissue": "13815",
      "warningcode": "0"
    }
  ],
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
  "errorMessage": "Cust Nbr not found"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5DB4001AS` |Cust Nbr not found|
