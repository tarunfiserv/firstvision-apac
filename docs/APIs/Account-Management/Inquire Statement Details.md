# Inquire Statement Details

 This service is used to fetch statement details for a given account number.

## Endpoint

`GET /v1/accounts/{accountNumber}/statement/details`

## Payload Example

### Request Payload

```json
{
Shoud be empty.
***The Business Unit and Account Number should be sent as query parameters and path variable.***
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountNumber}/statement/details).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 3 | Identification number of the organization associated with the account. |
| `accountNumber` | Path Variable | *string* | 19 | Account Number of the cardholder. | 



### Successful Response Payload

```json
{
  "personalId": "string",
  "businessUnit": 600,
  "dateLastStatement": "2021-05-07",
  "daysInCycle": 13,
  "dueDate": "18/09/2021",
  "alternateCustomerNumber": "string",
  "accountRelationship": "0006000011000000137",
  "storeID": 999999998,
  "interestThisStatement": "$0.00",
  "fSAdjustedPoints": 0,
  "beginningBalanceI": "$0.00",
  "currentPaymentDue": "$0.00",
  "minimumPayment": 0,
  "cashAvailable": "$0.00",
  "fSBeginningBalance": 0,
  "fSEndBalance": 0,
  "creditLimit": "$150,000.00",
  "storeOrg": 600,
  "statementTransactionDetails": [
    {
      "amount": "$1,000.00",
      "cardSequence": 0,
      "merchOrg": 0,
      "authorizationCode": " ",
      "transactionStatus": " ",
      "description": "INITIAL LOAN DISBURSEMENT",
      "cardNBR": "0006000011000000137",
      "store": 999999998,
      "dEPT": " ",
      "transactionCode": 4565,
      "ePPConvInd": " ",
      "reference": "0999999990818000060018",
      "transactionType": "D",
      "merchStore": 0,
      "qUALIND": " ",
      "pLANSEQ": 1,
      "postDate": "18/08/2021",
      "creditPlan": 70001,
      "logicModule": 1,
      "sKU": 0,
      "cATG": 0,
      "effectiveDate": "18/08/2021"
    }
  ],
  "skipPaymentLevel": 0,
  "noOfQualifiedTXNS": "string",
  "creditClass": "N1",
  "fSEarned": 0,
  "beginningBalance": "$0.00",
  "currBalanceXchk": "$1,000.00",
  "currentBalance": 0,
  "deferBillBalance": "$0.00",
  "debitsNumber": 2,
  "internalStatus": "A",
  "scheduledPaymentAmount": "$0.00",
  "unbilledDebitBalance": "$0.00",
  "yTDDisclosedCharge": "$0.00",
  "billIndicator": 0,
  "billingCycle": 18,
  "unResolvedCreditBalance": "$0.00",
  "shortName": "EPHTIARRAUHROE",
  "numberOfPlans": 1,
  "totalPastDue": "$0.00",
  "amountOfQualifiedTXNS": "$0.00",
  "altDueDelqThreshold": "$0.00",
  "statementFlag": "string",
  "qualifyingGraceBalance": "$1,500.00",
  "cashLimit": "$3,000.00",
  "creditsAmount": "$0.00",
  "totalPaymentDue": "$0.00",
  "yTDOverlimitCharge": "$0.00",
  "dateThisStatement": "18/08/2021",
  "yTDInterest": "$0.00",
  "endBalanceI": "$0.00",
  "yTDLateCharge": "$0.00",
  "residenceID": 600,
  "employeeCode": "string",
  "rVLVStatus": "string",
  "endBalance": "$1,500.00",
  "fixedPaymentAmount": "$500.00",
  "cycleDue": 0,
  "debitsAmount": "$1,500.00",
  "corresCustomerNumber": " ",
  "product": 600,
  "creditPlanInterestRateHistory": [
    {
      "creditPlan": 0,
      "periodicInterestRate": "0.0000000%",
      "lMTNO": " ",
      "upToLimit": "$0.00",
      "annualInterestRate": "0.0000000%"
    }
  ],
  "convertedCreditPlanHistory": [
    {
      "creditPlan": 70001,
      "currentBalance": 0,
      "minimumPayment": 0
    }
  ],
  "creditPlanStatementHistory": [
    {
      "periodAvgBalance": "$0.00",
      "deferRecapInt": "$0.00",
      "transferRollIn": "$0.00",
      "currentBalance": "$1,500.00",
      "previousBalance": "$0.00",
      "minimumPay": "$0.00",
      "serviceCharge": "$0.00",
      "calculatedYearBase": 1,
      "interest": "$0.00",
      "purchaseDebits": "$1,5000.00",
      "creditPlan": 70002,
      "paymentsCredits": "$0.00",
      "transferRollOut": "$0.00",
      "aSChrg": "$0.00",
      "actuarialAPR": "0.0000000%",
      "deferInsurance": "$0.00",
      "cycleAverageBalance": "$0.00"
    }
  ],
  "graceExpire": "18/09/2021",
  "lastYTDInterest": "$0.00",
  "openToBuy": "$148,000.00",
  "customerNumber": "0006000011000000137",
  "recency": 0,
  "relationshipNumber": "string",
  "userCode6": " ",
  "graceIntFree": "$0.00",
  "userCode5": " ",
  "fSDisbursedPoints": 0,
  "userCode4": " ",
  "userCode3": " ",
  "totalAmtDueBalance": "$0.00",
  "userCode2": " ",
  "creditsNumber": 0,
  "blockCode1": "string",
  "userCode1": " ",
  "billCurrency": "SGD",
  "blockCode2": "string",
  "projectedDD": "$0.00",
  "currencyConversionRate": 0,
  "lifeToDateCounter": 1
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
| `V5S34003SA` |No Statement History Information Found On File |
| `V5S34003SB` |No Statement History Information Found On File |
| `V5S34003EB` |No Statement History Information Found On File |
| `V5S34003EF` |No Statement History Information Found On File |  
| `V5S34003EG` |No Statement History information found on file '|
