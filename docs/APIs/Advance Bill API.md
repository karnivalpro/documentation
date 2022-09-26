# Advance Bill API

## Rest URL

```
POST https://sandbox.kbill.in/api/v1/bills/advance
```

## Request Headers

```
    Content-Type: application/json
    Accept: application/json
    Authorization: {brand-key}
```

The brand key is shared in a seperate email.

# Request Body

```json
{
   "salesOrderNumber" : "2010",
   "customerNumber" : "7983717399",
   "advanceBillRef" : "456556",
   "storeId" : "2321",
   "customerEmail" : "nickagg11@gmail.com",
   "customerName": "Naman Agarwal",
   "salesChannel" : "wab com"
}
```

**Mandatory fields among these are:-** `advanceBillRef`, `storeId`, `customerEmail`/`customerNumber`

## Responses

### HTTP Status Code 201

The bill has been created on Karnival and it'd read as `Created` on status description on API call. On completing this API call, an SMS notification will be sent to the customers phone.The response body will be as follows:-

```json
{
   "status": "success",
   "message": "Entity has been saved.",
   "responseCode": 200,
   "params": {
       "entity.id": "60efcb371a4dc91b3bd041bf",
       "bill.url": "https://test.knvl.me/az/paYxXovs4El"
   },
   "mobileValid": true,
   "emailValid": true
}
```

### HTTP Status Code 400 (Bad Request)

This happens when in the request body you send any of the **mandatory fields as empty**. In this case, the response body will contain the cause of the error. The Bill will **not be created** on the **Karnival** and no SMS will be sent to the customer.

#### Missing Store ID

```json
{
   "status": "failed",
   "message": "Store Id must be present",
   "responseCode": 10
}
```

#### Missing Sales Order Number

```json
{
   "status": "failed",
   "message": "Transaction Number must be present",
   "responseCode": 40
}
```

#### Missing Mobile Number And Email Both

```json
{
   "status": "failed",
   "message": "Mobile Number or Email must be present",
   "responseCode": 60
}
```