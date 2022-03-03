# Update Account Charge-Off

 This service is used to update account status.

## Endpoint

`PUT /v1/accounts/{accountNumber}/chargeoff`

## Payload Example

### Request Payload

```json
{
  "dateofNotificationReceived": "01/01/2018",
  "systemDefinedChargeOffReason": "C"
} 
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/accounts/{accountNumber}/chargeoff).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountNumber` | Path Variable | Query Parameter | 19 | Account Number of the cardholder. | 
| `businessUnit` | Path Variable |*number* | 3 | Identification number of the organization associated with the account. |
| `dateofNotificationReceived` | Payload |*Date* | DD/MM/YYYY | Date on which a bankruptcy notification was received or date on which a fraudulent loan was discovered. |
| `systemDefinedChargeOffReason` | Payload |*string* | 1 | Code that identifies the charge-off reason for the account |

### Successful Response Payload

```json
{
  "accountNumber": "0000000001000000057",
  "businessUnit": "600",
  "chargeOffStatus": "3",
  "dateofNotificationReceived": "01/01/2018",
  "numberofChargeOffDays": "0",
  "systemDefinedChargeOffReason": "C"
}
```

### Error Response Payload

```json
{
  "errorCode": "V5BS0109SA",
  "errorMessage": "Invalid Internal Status"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0010SF` |Update Request - Record not found|
| `V5BS0109SA` |Invalid Internal Status|
| `V5BS0109SB` |Proc Date Must Be Greater Than Greatest Exp Date For Purged Acct| 
| `V5BS0109SC` |Status Cannot Change To Closed When Insurance Is Active| 
| `V5BS0110EB` |Rsn Code Must Be Defined|                            
| `V5BS0110EC` |Cannot Use Chgoff Rsn Defined In Logo Lvl For Chgoff Sta'2'| 
| `V5BS0110SA` |Entered Auto C/O Rsn Code - Chg To Manual Rsn|   
| `V5BS0110SD` |Cannot Use Rsn Defined For Auto Chgoff Accts|          
| `V5BS0110SE` |This Charge Off Status Is Not Allowed For Edit Or Act Has Dispute| 
| `V5BS0110SF` |Cannot Charge Off An Account With A Zero Or Credit Balance|        
| `V5BS0110SG` |Cannot Reset Chargeoff On Account When Days Is > 0|                
| `V5BS0110SH` |Chgoff Status Update Is Not Allowed During Add|                   
| `V5BS0184SA` |Not A Valid Date|
| `V5BS0125SA` |Cannot Set A Block Code On A Billing Account|
| `V5BS0125SB` |Block Code 1 Must Be Alphabetic|
| `V5BS0125SC` |Block Code 1 Cannot Be Replaced With One Of A Lower Priority|
| `V5BS0127SA` |Cannot Set A Block Code On A Billing Account|
| `V5BS0127SB` |Block Code 2 Must Be Alphabetic|
| `V5BS0127SC` |Block Code Cannot Be Replaced With One Of A Lower Priority|
