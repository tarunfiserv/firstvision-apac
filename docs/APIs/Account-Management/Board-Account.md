# Board Account

This API is used to board the new account.

## Endpoint

`POST /v1/accounts/boardAccount`

## Payload Example

### Request Payload

```json
{
"expirationDateOfPctOverride": 0,
  "primaryAccountFlag": " ",
  "businessUnit": 600,
  "alternateCustomerNumber": " ",
  "expiryDateOfTempCreditLimit": 0,
  "cashPlanNumber": 0,
  "processingControlLevel": " ",
  "expireDateOfTheOverride": 0,
  "authorizationCriteriaTable": " ",
  "billingCurrency": 0,
  "ibsSavingsRoutingNumber": 12345,
  "ibsSavingsAccountNumber": 12345,
  "issuanceId": 600,
  "addInsuranceProduct": "N",
  "creditLimit": 15000,
  "billingLevel": 1,
  "suppressTknAtAccntLevel": 0,
  "product": 600,
  "corporateIdNumber": 0,
  "idOfThePctOverrideTables": " ",
  "owningBranchNumber": 999999998,
  "dualBillingFlag": 0,
  "retailPlanNumber": 0,
  "cardTechnology": 0,
  "customerNumber": 1000000007,
  "ibsDdaRoutingNumber": 0,
  "startDateOfPctOverride": 0,
  "residenceId": 600,
  "ibsDdaAccountNumber": " ",
  "startDateOfTheOverride": 0,
  "suppressLetter": 0,
  "waiveMembershipFees": 0,
  "billingCycle": 18,
  "coreBankingIndicator": "B",
  "cardNumberingScheme": 0,
  "relationshipLevelBillingCycle": 0,
  "customerSelectedDueDay": 0,
  "mobilePiFlag": 0,
  "shortName": "ABCDE",
  "temporaryCreditLimit": 0
}
``` 

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/accounts/boardAccount).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `Base Account Number` | Payload | *string* | 19 | This is the identification number to assign to the new Account Base Segment record. |
| `Create Customer Record` | Payload | *string* | 1 | This is the identification number to assign to the new Customer Name/Address record. |
| `Create Account Record` | Payload | *string* | 1 | This is the code that indicates whether to add a new account record. |
| `Same Cust/Base Number` | Payload | *string* | 1 | This is the code that indicates whether Customer number and Base account number are to be the same number. |
| `Create Relationship Record` | Payload | *string* | 1 | This is the code that indicates whether to add a new Relationship record. |
| `Create Embosser Records` | Payload | *string* | 1 | This is the code that indicates whether to add a new Embosser record. |
| `Business Unit` | Payload | *number* | 3 | Identification number of the business unit associated with the  account or relationship. |
| `Product` | Payload | *number* | 3 | Identification number of the product associated with the  account or relationship. |
| `Customer Number` | Payload | *string* | 19 | This is the code that indicates customer number. |
| `Add Insurance Product` | Payload | *string* | 01 | This is the code that indicates whether to add an Insurance Product record. |
| `Corporate ID Number` | Payload | *number* | 10 | Corporate identification number assigned to commercial card accounts. |
| `Primary Account Flag` | Payload | *string* | 01 | This is a flag that indicates whether the account is the primary account in a relationship. |
| `Short Name` | Payload | *string* | 20 | This is the short name of the account holder. |
| `Credit Limit` | Payload | *string* | 17 | This is the Credit limit of the account. |
| `Billing Currency` | Payload | *number* | 03 | This is ISO currency code that identifies the currency of this account. |
| `Billing Level` | Payload | *number* | 01 | This is the Code which indicates whether billing occurs for the account at the relationship level or subordinate account level. |
| `Dual Billing Flag` | Payload | *number* | 01 | This is the flag that indicates whether CMS uses the foreign or local currency to request the minimum payment. |
| `Alternate Customer Number` | Payload | *string* | 19 | This is the number that identifies the alternate Customer Name/ Address record containing an alternate address for statements and other correspondence. |
| `Customer Selected Due Day` | Payload | *number* | 02 | Day of the month the customer has selected as the payment due date. |
| `Card Numbering Scheme` | Payload | *number* | 01 | Card numbering scheme that determines the card numbers that are assigned to Embosser records associated with the account. |
| `Billing Cycle` | Payload | *number* | 02 | This flag indicates the day of the month that CMS performs cycle processing for the account. 
| `Residence ID` | Payload | *string* | 03 | This flag identifies the state, province or country in which the  account holder resides. |
| `Issuance ID` | Payload | *string* | 03 | This is the flag which identifies the state, province or country in which the account was issued. |
| `ID Of The PCT Override Tables` | Payload | *string* | 03 | Code that identifies an existing Processing Control Table (PCT ID) used to establish special pricing controls for the account. |
| `Start Date Of The Override` | Payload | *date* | DD/MM/YYYY | This is the date on which the special pricing controls start for the account. |
| `Expire Date Of The Override` | Payload | *date* | DD/MM/YYYY | This is the date on which the special pricing controls expire for the account. |
| `Processing Control Level` | Payload | *string* | 01 | This is a flag which indicates the processing control level for accounts in this product. |
| `Start Date Of PCT Override` | Payload | *date* | DD/MM/YYYY | This is the date on which the processing control level override starts for the account. |
| `Expiration Date Of PCT override` | Payload | *date* | DD/MM/YYYY | This is the date on which the processing control level override expires for the account. |
| `Cash Plan Number` | Payload | *number* | 05 | The default values for this field are set on the Account  Processing table assigned to the account. |
| `Retail Plan Number` | Payload | *number* | 05 | The default values for this field are set on the Account Processing table assigned to the account. |
| `Card Technology` | Payload | *number* | 01 | This is the flag that identifies the current card technology used for this account. |
| `Temporary Credit Limit` | Payload | *string* | 17 | This is the temporary line of credit for the account in whole monetary units. |
| `Expiry Date of Temp Credit Limit` | Payload | *date* | DD/MM/YYYY | This is the date on which the temporary line of credit expires. |
| `Owning Branch Number` | Payload | *number* | 09 | This field is the number of the branch that owns this account  and location of financial reporting for this account. |
| `Mobile PI Flag` | Payload | *number* | 1 | Flag that indicates whether mobile payment instruments (PI)  are allowed for this account. |
| `Authorization Criteria Table` | Payload | *string* | 03 | Identification number of the Authorization Criteria table assigned to the account. |
| `Supress letter` | Payload | *number* | 1 | Code that indicates whether CMS suppresses letters for accounts assigned this block code. |
| `Waive Membership Fees` | Payload | *number* | 1 | Code that indicates whether CMS waives account-level membership fees and supplemental card membership fees for accounts assigned this block code. |
| `IBS DDA Routing Number` | Payload | *number* | 10 | This is ABA-assigned routing and transit number that identifies the financial institution at which the checking account is held. |
| `IBS DDA Account Number` | Payload | *string* | 17 | Customer mobile number. |
| `IBS Savings Routing Number` | Payload | *number* | 10 | This is ABA-assigned routing and transit number that identifies the financial institution at which the savings account is held. |
| `IBS Savings Account Number` |  Payload | *string* | 17 | This is the savings account number. |
| `Suppress TKN at accnt level` | Payload | *number* | 1 | Code that indicates to supress token at account level. |
| `Core Banking Indicator` | Payload | *string* | 1 | This is the code indicates type of bannking. |
| `Cardholder Flag` | Payload | *number* | 1 | This is the code that indicates whether the card is issued as a primary or secondary card. 
| `Billing Cycle` | Payload | *number* | 2 | Cycle code that indicates the day of the month that CMS performs cycle processing for the account. |

### Successful Response Payload

```json
{
  "product": 1,
  "businessUnit": 600,
  "accountNumber": 0006000011000002430
}
```

### Error Response Payload

```json
{
   "errorCode" :  "V5SB4003EA" ,
   "errorMessage" : "Base Account number is required"   
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5SB4003EA` | Base account number is required |
| `V5SB4003EG` | Base account number must be numeric |
| `V5SB4003EH` | Base account number required |
| `V5SB4005EA` | Customer NA account must be blank |
| `V5SB4005EB` | Customer NA account required |
| `V5SB4005EG` | Customer NA account must be blank |
| `V5SB4005EH` | Customer NA account must be numeric |
| `V5SB4008EA` | Relationship not valid for this ORG |
| `V5SB4008EB` | Relationship not valid for the dual ORG |
| `V5SB4001EA` | Organization not on file |
| `V5SB4001SA` | Organization not on file |
| `V5SB4002EA` | LOGO record not on file |
| `V5SB4002EB` | LOGO record incomplete |
| `V5SB4009EA` | Relationship number required |
| `V5SB4011EA` | Insurance not allowed for prepaid account |
| `V5SB4012EA` | Sweeping not allowed in this LOGO |
| `V5SB4012EB` | HCS must be active for account type values 1,2,3 |
| `V5SB4012EC` | Account type must be zero for prepaid account |
| `V5SB4157EC` | Account number exist on relationship file for this ORG |
| `V5SB4157ED` | Account number exist on relationship file for DUAL ORG |
| `V5SB4158EA` | Account number cannot duplicate existing embosser for this ORG |
| `V5SB4158EB` | Account number cannot duplicate existing embosser for DUAL ORG |
| `V5SB4151EA` | LOGO does not allow billing account generation |
| `V5SB4151EB` | Maximum nummber 20 attemptds made on billing ACCOUNT |
| `V5SB4151EC` | Generated account number IS greater than ending billing number|
| `V5SB4151ED` | LOGO does not ALLOW account number generation |
| `V5SB4151EE` | Maximum nummber 20 attemptds made on Base account number |
| `V5SB4151EG` | Generated account number IS greater than Base account number|
| `V5SB4152EB` | ORG does not allow account number generation |
| `V5SB4160EA` | Invalid Base account number digit for this ORG |
| `V5SB4160EB` | Invalid Base account number for this Org |
| `V5SB4160EC` | Invalid Base account number digit for DUAL ORG |
| `V5SB4160ED` | Invalid Base account number for DUAL ORG|