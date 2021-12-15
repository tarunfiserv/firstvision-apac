# Inquire Account Details

 The service provides the basic details of the account associated with the customer.

## Endpoint

`GET /v1/accounts/{accountNumber}/details`

## Payload Example

### Request Payload

> Empty.  

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountNumber}/details).

The below table identifies the required parameters in the request payload.

| Variable | Type | Length | Description/Values |
| -------- | :--: | :------------: | ------------------ |
| `businessUnit` | *number* | 3 | Identification number of the organization associated with the account. |
| `accountNumber` | *string* | 19 | Account Number of the cardholder. |

### Successful Response Payload

```json
{
  "accountDisplayRequest": "N",
  "accountNumber": "0002000010000403266",
  "altCustomerExpiryDate": "00/00/0000",
  "altCustomeraddressEffectiveDate": "00/00/0000",
  "alternateCustomerNumber": "0000000000000000000",
  "alternateCustomerNumberFlag": "",
  "applicationDate": "00/00/0000",
  "billingAcctInd": "0",
  "billingCycle": "31",
  "billingLevel": "1",
  "blockCode1": "",
  "blockCode2": "",
  "blockCodeDate1": "00/00/0000",
  "blockCodeDate2": "00/00/0000",
  "businessUnit": "200",
  "cCMCustomerID": "",
  "cardExpirationDate": "00/00/0000",
  "cardFeeDate": "00/00/0000",
  "cardScheme": "3",
  "chargeOffStatus": "0",
  "collateralCardRequest": "N",
  "collateralCode": "",
  "correspondenceCustomerNumber": "",
  "creditLimit": "$0.00",
  "currencyCode": "36",
  "customerNumber": "0002000002000007799",
  "customerStatementFlag": "0",
  "customerStatementLetterFlag": "1",
  "dateAccountOpened": "17/08/2021",
  "dateClosed": "00/00/0000",
  "dateLastCycle": "31/07/2021",
  "dateLastMaintenance": "09/12/2021",
  "dateNextCRIntPymt": "00/00/0000",
  "dateofNotificationReceived": "00/00/0000",
  "deferMembershipFeeDate": "00/00/0000",
  "dualBillingFlag": "0",
  "dueDay": "0",
  "employeeCode": "",
  "flexBillingFlag": "N",
  "greatestExpiryDate": "16/08/2024",
  "highBalanceAmount": "$0.00",
  "incomeoftheAccount": "$0.00",
  "internalStatus": "D",
  "letterRequest": "",
  "liabilityIndicator": "0",
  "memoBillingCurrency": "36",
  "nextStatementDate": "31/08/2021",
  "numberofChargeOffDays": "0",
  "numberofUnblockedCards": "2",
  "ownerFlag": "",
  "permanentCollector": "",
  "primaryAccountFlag": "",
  "product": "1",
  "reissueScheme": "0",
  "relationshipnumber": "",
  "reportFraudulentActivity": "N",
  "resetChargeoffDaysSwitch": "0",
  "restructureFlag": "N",
  "returnMailCounter": "0",
  "returnMailDate": "00/00/0000",
  "returnMailUser": "",
  "shortName": "TESTING",
  "statementFlag": "",
  "statementFrequency": "1",
  "statementReprintDate": "00/00/0000",
  "statementReprintFlag": "C",
  "systemDefinedChargeOffReason": "",
  "userAccountNumber": "0000000000000000000",
  "userDefinedChargeOffReason": "",
  "vIPStatus": "0"
}
```

### Error Response Payload

```json
{
  "errorCode": "V5BS0004SF",
  "errorMessage": "Get Request - Record not found"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0004SF` | Get Request - Record not found|
