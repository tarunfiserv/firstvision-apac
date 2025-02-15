# PIN Block Change

The PIN Block Change Service is used to update the PIN Block with the prerequisite that the existing PIN block must be supplied and validated.

## Endpoint

`PUT /v1/cards/{cardNumber}/pinBlockChange`

## Payload Example

### Request Payload

```json
{
  "userFiller": " ",
  "product": 1,
  "signonName": " ",
  "requestedPinBlock": 123456,
  "pinChannel": "A",
  "securitySignon": " ",
  "currentPinBlock": " ",
  "keyAssociation": " ",
  "vgsFiller": " ",
  "pinOffset": 0
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/cards/{cardNumber}/pinBlockChange).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 3 | Identification number of the organization associated with the account. |
| `cardNumber` | Path Variable | *string* | 19 | Token Number associated with the clear PAN. |
| `currentPinBlock` | Payload | *string* | 16 | Current PIN block |
| `requestedPinBlock` | Payload | *string* | 16 | PIN block to be updated |

### Successful Response Payload

```json
{
    "cardNumber": "0009543491000080172",
    "userFiller": "",
    "filler": "",
}
```

### Error Response Payload

```json
{
  "errorCode": "V5CP4005SZ",
  "errorMessage": "Update Access not granted for Requested Pin Block"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
|`V5CP4001SV`| Invalid Business Unit|  
|`V5CP4006SN`| Pin Offset is not numeric |
|`V5CP4005SZ`| Update Access not granted for Requested Pin Block|
|`V5CP4006SZ`| Update Access not granted for Pin Offset |
|`V5CP4007SZ`| Update Access not granted for Pin Channel |
|`V5CP4007SV`| Invalid Pin Channel|
|`V5CP0001SF`| Invalid User|
|`V5CP0021SF`| Not Allowed. System in After hours mode|
|`V5CP0022SF`| Not Allowed. System in After hours Update mode |
