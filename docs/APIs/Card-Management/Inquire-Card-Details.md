# Inquire Card Details

This service is used to fetch card details.

## Endpoint

`GET /v1/cards/{cardNumber}/details`

## Payload Example

### Request Payload

>Shoud be empty.  
***The Business Unit and Card Number should be sent as query parameters and path variable.***

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/cards/{cardNumber}/details).

The below table identifies the required query parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 3 | Identification number of the organization associated with the account. |
| `cardNumber` | Path Variable | *string* | 19 | Token Number associated with the clear PAN. |

### Successful Response Payload

```json
{
  "cardholderType": "",
  "businessUnit": 600,
  "blockSecurityID": " ",
  "lastCardExpirationDate": "00/00/0000",
  "cardIssueDate": "00/00/0000",
  "lastCardActivation": "N",
  "postalCode": " ",
  "pinOverride": "",
  "typeOfCardRequested": 0,
  "secureCodeActiveForAccount": "",
  "firstIssueBranch": 0,
  "singleOTCCashAuthorizationAllowed": "$0.00",
  "spendingLimitPrepaymentAvailable": "$0.00",
  "maximumAmountRetailAuthorizationsAllowed": "$1,000.00",
  "addressLine1": " ",
  "addressLine2": " ",
  "currentChipSequenceNumber": 0,
  "mailerDate": "00/00/0000",
  "mobileProvisionStatus": "",
  "emblem": 0,
  "cardReissueDeliveryOption": "",
  "blockDate": "00/00/0000",
  "name1TypeIndicator": "",
  "cardholderName1": " ",
  "digitalId": "",
  "cardholderName2": " ",
  "name2TypeIndicator": "",
  "maximumNumberRetailAuthorizationsAllowed": 999999999,
  "stateProvince": " ",
  "maximumAmountSingleATMTransactionAllowed": "$2,000.00",
  "cardReissueDeliveryLocation": 0,
  "maximumAmountATMCashAuthorizationsAllowed": "$1,000.00",
  "warningBulletinDistributionRegion": " ",
  "maximumNumberATMCashAuthorizationsAllowed": 999999999,
  "mobileDeviceID": "",
  "languageIndicator": " ",
  "vISAPlusIndicator": "",
  "embosserRecordStatus": "",
  "maximumAuthorizationsFrequnecy": 1,
  "authorizationCriteriaTableIDNumber": " ",
  "maximumAmountOTCCashAuthorizationsAllowed": "$1,000.00",
  "cardDelayDays": 0,
  "cardNumber": "0009544410000000062",
  "statusDateChange": "00/00/0000",
  "transferEffectiveDate": "00/00/0000",
  "spendingLimitPrepaymentAmount": "$0.00",
  "city": " ",
  "spendingCategoryStatistics": [
    {
      "spendingCategoryNumberWTD1": 999999999,
      "spendingCategoryNumberLTD1": 999999999,
      "spendingCategoryAmountToday1": 0,
      "spendingCategoryNumberToday1": 999999999,
      "spendingCategoryNumberCTD1": 999999999,
      "spendingCategoryAmountCTD1": "$1,000.00",
      "spendingCategoryAmountYTD1": "$1,000.00",
      "spendingCategoryAmountLTD1": "$1,000.00",
      "spendingCategoryNumberYTD1": 999999999,
      "spendingCategoryAmountWTD1": "$1,000.00"
    }
  ],
  "dateCurrentCardValid": "",
  "pOSServiceCode": " ",
  "maximumNumberOTCAuthorizationsAllowed": 999999999,
  "currentCardNeedActivation": "N",
  "nameOnCard": "DAVID TEST 2",
  "nameOn2ndLine": " ",
  "secureIDStatusChanged": "C1X",
  "spendingLimitPrepaymentExpiryDate": "00/00/0000",
  "fraudCardTransferNumber": " ",
  "vISAMiniCardVersion": "",
  "cardsReturnedForEmbosser": 0,
  "reasonCode": "",
  "issuingAttemptsRemaining": 0,
  "cardActivatedDate": "19/08/2021",
  "expirationDate": "16/08/2024",
  "pINOffset": 0,
  "userdefinedField5": " ",
  "userdefinedField4": 0,
  "product": 0,
  "blockCode": " ",
  "numberOfCardsOutstanding": 1,
  "typeOfCard": 0,
  "previousPINOffset": 0,
  "authorizationSpendingLimits": [
    {
      "frequency1": "",
      "number1": 5,
      "maximum1": 0
    }
  ],
  "customersGender": "",
  "warningCode7": "",
  "typeOfMailer": " ",
  "pinDelayDays": 0,
  "customerNumber": " ",
  "userdefinedField1": " ",
  "postToAccountNumber": "0006000022000000076",
  "userdefinedField3": " ",
  "warningCode1": "",
  "userdefinedField2": " ",
  "singleRetailAuthorizationAllowed": "$999,999,999,999,999.99",
  "authorizationAccumulators": [
    {
      "accumulatedAuthorizationAmountCTD1": "$10234.00",
      "accumulatedAuthorizationAmountYTD1": "$123456.00",
      "accumulatedAuthorizationAmountToday1": "$1000.00",
      "accumulatedAuthorizationNumberToday1": 5,
      "accumulatedAuthorizationNumberCTD1": 6,
      "accumulatedAuthorizationNumberYTD1": 8,
      "accumulatedAuthorizationAmountLTD1": "$1234560.00",
      "accumulatedAuthorizationNumberLTD1": 12
    }
  ],
  "cardAction": 1,
  "numberOfCardsRequested": 1,
  "warningBulletinLastDate": "00/00/0000",
  "nextCardExpirationDate": "00/00/0000",
  "previousChipSequenceNumber": 0,
  "pINMailerSuppression": "",
  "datefirstcardVerify": "00/00/0000"
}
```

### Error Response Payload

```json
{
  "errorCode": "V5ED4001EC",
  "errorMessage": "Dual org not found or add pending"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
|`V5ED4001EC` |Dual org not found or add pending|
|`V5ED4001ER` |Bin nbr should be same for account and card|
|`V5ED4001ES` |Dual org not found or add pending|
|`V5ED4001SA` |Org not found|
|`V5ED4001SB` |Org is in add pending|
|`V5ED4001SC` |Org is in purged|
|`V5ED4001SD` |Account not present|
|`V5ED4001SE` |Logo not present|
|`V5ED4001SF` |Invalid org|
|`V5ED4001EJ` |Record not found|
|`V5ED4001EL` |Record not found|
|`V5ED4001EN` |Record purged or add pending|
|`V5ED4002EA` |Invalid card number|
|`V5ED4002ED` |Card number must be provided|
|`V5ED4002ES` |Card number must be equal to post to account nbr|
|`V5ED4002ER` |Bin nbr should be same for both account and card|
|`V5ED4002EE` |Invalid check digit - card number|
|`V5ED4003EA` |Invalid sequence number|
|`V5ED4003ED` |Card seq number must be greater than zero|
|`V5ED4003EQ` |Post to acct for dual org not on file|
|`V5ED4003EW` |Invalid rec number for this account|
|`V5ED4003EX` |Hcs system active and node record not found|
|`V5ED9910ED` |Post to acct invalid check digit|
|`V5ED9910EF` |Post to acct record not found|