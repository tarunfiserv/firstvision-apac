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
  "businessUnit": 100,
  "customerNumber": "0001000000333113902",
  "customerName": "UATMFNXCX48",
  "sSNID": "1139XX",
  "dateofBirth": "00/00/0000",
  "nameLine1": "UATMFNCU448 TWOPPPUAXXXNCUST448",
  "addressLine1": "62 CHARTERIS DR",
  "addressLine2": "string",
  "addressLine3": "string",
  "addressLine4": "string",
  "homeDistricName": "string",
  "emailAddress": "UATMXXXU448@GMAIL.COM",
  "homePhoneNumber": "++61430010000",
  "workPhoneNumber": "++61430010000",
  "mobileNumber": "++61430010000",
  "numberofCards": "1",
  "numberofAccounts": "1",
  "userDefinedField4": "string",
  "cardList": [
    {
      "businessUnit": 100,
      "cardNumber": "0009846999010009405",
      "cardSequence": 1,
      "posttoAccount": "000100001100000068",
      "nameOnCard": "U T UATMLNCUS9999",
      "product": 1,
      "productDescription": "VISA XXXXXXXX DEBIT",
      "cardholderType": 1,
      "dateOpened": "string",
      "embosserRecordStatus": "0",
      "blockCode": " ",
      "blockDate": "string",
      "currentCardNeedActivation": "Y",
      "currCardAction": "0",
      "lastCardAction": "1",
      "cardActivatedDate": "string",
      "cardTechnology": "3",
      "cardIssueDate": "string",
      "warningCode": "0",
      "lastCardExpirationDate": "string",
      "lastCardNeedActivation": "Y",
      "timeLastPlasticIssue": 0,
      "maskCardnumber": "000XXXXXXX",
      "pinoffset": "3290000",
      "numberofcards": "0",
      "digitalid": "  ",
      "mOTOFlag": "   ",
      "pAYwaveFlag": "Y",
      "iNTATMPOSFlag": "Y",
      "cashBackTranFlag": "Y",
      "cHEQUEACCOUNTNBR": "   ",
      "sAVINGSACCOUNTNBR": "   ",
      "dATELASTPLASTICUSED": "0",
      "dATELASTWALLETUSED": "0",
      "dATELASTPLASTICSUPRESED": "0",
      "pLASTICSUPPRESSSTATUS": "N",
      "aTMFlag": "Y",
      "pOSFlag": "Y",
      "e-COMACTFlag": "1",
      "eMBRNAME2": "   ",
      "mCCLIMIT-1": "$0.01",
      "mCCLIMIT-2": "$0.01",
      "mCCLIMIT-3": "$0.01",
      "mCCLIMIT-4": "$0.01",
      "mCCLIMIT-5": "$0.01",
      "mCCLIMIT-6": "$0.01",
      "mCCLIMIT-7": "$0.01",
      "mCCLIMIT-8": "$0.01",
      "mCCLIMIT-9": "$0.01",
      "mCCLIMIT-10": "$0.01"
    }
  ]
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
