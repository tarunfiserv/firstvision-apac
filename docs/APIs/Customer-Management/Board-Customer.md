# Board Customer

 This API is used to board the new customer..

## Endpoint

`POST /v1/customers/boardCustomer`

## Payload Example

### Request Payload

```json
{
Shoud be empty.
***The Business Unit and Account Number should be sent as query parameters and path variable.***
}
``` 

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/customers/boardCustomer).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `Base Account Number` | Payload | *string* | 19 | This is the identification number to assign to the new Account Base Segment record. |
| `Create Customer Record` | Payload | *string* | 1 | This is the identification number to assign to the new Customer Name/Address record. |
| `Create Account Record` | Payload | *string* | 1 | This is the code that indicates whether to add a new account record. |
| `Same Cust/Base Number` | Payload | *string* | 1 | This is the code that indicates whether Customer number and BASE Account number are to be the same number. |
| `Create Relationship Record` | Payload | *string* | 1 | This is the code that indicates whether to add a new Relationship record. |
| `Create Embosser Records` | Payload | *string* | 1 | This is the code that indicates whether to add a new Embosser record. |
| `Customer Number` | Payload | *string* | 19 | Identifies the customer number of the Account Base Segment. |
| `Add Insurance Product` | Payload | *string* | 1 | This is the code that indicates whether to add an Insurance Product record. |
| `Business Unit` | Payload | *number* | 3 | Identification number of the business unit associated with the  account or relationship. |
| `Product` | Payload | *number* | 3 | Identification number of the product associated with the  account or relationship. |
| `Owner/Co-owner` | Payload | *number* | 1 | This is the Code that indicates whether to display information  for the owner, co-owner, or both. |
| `Dual Flag` | Payload | *number* | 1 | This field indicates whether CMS adds a duplicate customer  record in the associated business unit for dual currency processing. |
| `Title` | Payload | *string* | 20 | Customer title. |
| `Name Type Ind 1` | Payload | *number* | 1 | Name indiacator 1. |
| `Name Type Ind 2` | Payload | *number* | 1 | Name indiacator 2. |
| `Name Type Ind 3` | Payload | *number* | 1 | Name indiacator 3. |
| `Name Line 1` | Payload | *string* | 40 | Customer name line 1. |
| `Name Line 2` | Payload | *string* | 40 | Customer name line 2. |
| `Name Line 3` | Payload | *string* | 40 | Customer name line 3. |
| `Address Line 1` | Payload | *string* | 40 | Customer address line 1. |
| `Address Line 2` | Payload | *string* | 40 | Customer address line 2. |
| `Address Line 3` | Payload | *string* | 40 | Customer address line 3. |
| `Address Line 4` | Payload | *string* | 40 | Customer address line 4. |
| `City` | Payload | *string* | 30 | Name of customer city. |
| `State` | Payload | *string* | 30 | Name of state. |
| `Postal Code` | Payload | *string* | 10 | Postal code. |
| `Country Code` | Payload | *string* | 03 | code of country. |
| `Residence Flag` | Payload | *number* | 1 | Residential status. |
| `Home Phone` | Payload | *string* | 20 | Residential phone number. |
| `Employee Phone` | Payload | *string* | 20 | Employee phone number. |
| `Date of Birth` | Payload | *number* | 7 | Customer date of birth. |
| `Last Name` | Payload | *string* | 40 | Last name of customer. |
| `Middle Name` | Payload | *string* | 40 | Middle name of customer. |
| `First Name` | Payload | *string* | 40 | First name of customer. |
| `National ID` | Payload | *string* | 25 | Customer national ID number. |
| `Gender` | Payload | *number* | 1 | Gender of customer. |
| `E-Mail` | Payload | *string* | 60 | customer primary mail id. |
| `Alt E-Mail` | Payload | *string* | 50 | Customer alternate mail id. |
| `Mobile Number` | Payload | *string* | 20 | Customer mobile number. |
| `E-Mail Flag` | Payload | *number* | 1 | This is the code that indicates to select mail id for communication. |
| `Core Banking Indicator` | Payload | *string* | 1 | This is the code indicates type of bannking. |
| `Cardholder Flag` | Payload | *number* | 1 | This is the code that indicates whether the card is issued as a primary or secondary card. |
| `Billing Cycle` | Payload | *number* | 2 | Cycle code that indicates the day of the month that CMS performs cycle processing for the account. |
| `Supress letter` | Payload | *number* | 1 | Code that indicates whether CMS suppresses letters for accounts assigned this block code. |
| `Waive Membership Fees` | Payload | *number* | 1 | Code that indicates whether CMS waives account-level membership fees and supplemental card membership fees for accounts assigned this block code. |
| `Suppress TKN at accnt level` | Payload | *number* | 1 | Code that indicates to supress token at account level. |

### Successful Response Payload

```json
{
 

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
| `V5SB4003EA` | Base Account number is required |
| `V5SB4003EG` | Base Account number must be numeric |
| `V5SB4003EH` | Base Account number is required |
| `V5SB4005EA` | Customer NA Account must be blank| 
| `V5SB4005EB` | Customer NA Account required |
| `V5SB4005EG` | Customer NA Account must be blank|  
| `V5SB4005EH` | Customer NA Account must be numeric|  
| `V5SB4008EA` | Relationship not valid for this Org |
| `V5SB4008EB` | Relationship not valid for the dual Org |  
| `V5SB4001EA` | Organization not on file |
| `V5SB4001SA` | Organization not on file |
| `V5SB4002EA` | Logo record not on file |
| `V5SB4002EB` | Logo record is incomplete  |
| `V5SB4009EA` | Relationship number is required | 
| `V5SB4011EA` | Insurance not allowed for prepaid accounts |  
| `V5SB4012EA` | Sweeping not allowed in this Logo record |
| `V5SB4012EB` | HCS must be active for account type values 1,2,3 |  
| `V5SB4012EC` | Account type must be zero fora prepaid account |
| `V5SB4154SA` | Customer number not on file for this Org |
| `V5SB4154SB` | Customer number already exist for this Org |  
| `V5SB4154SC` | Customer number must be generic for presonalized prepaid account |
| `V5SB4154SD` | Generic customer not allowed |
| `V5SB4155EA` | Customer number not on file for the dual Org  |
| `V5SB4155EB` | Generic customer not allowed |
| `V5SB4155EC` | Customer number already exist for the dual Org |
| `V5SB4154EA` | Invalid customer number |
| `V5SB4160EE` | Invalid customer check digit this Org |
| `V5SB4160EG` | Invalid customer check digit dual Org |