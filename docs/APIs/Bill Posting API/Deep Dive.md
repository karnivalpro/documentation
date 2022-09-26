| Field Name             | Description                                                                                                                   |
| ---------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| posNumber              | POS terminal Identification Number                                                                                            |
| userId                 | user ID of logged-in user                                                                                                     |
| userName               | User name of logged in user                                                                                                   |
| BillNumber             | Bill Number/invoice Number Should be unique Across the brand. (Mandatory Field)                                               |
| BillStatus             | sent/paid/overdue.                                                                                                            |
| BillType               | tax_invoice-(1)/return_invoice(2)/exchange_invoice(3)/salesorder(4)/Homedelivery(5)                                           |
| purchaseDate           | DD-MM-YYYY date of Billing                                                                                                    |
| purchaseTime           | Time of billing in HH:MM:SS 24 hour format                                                             (Eg. 16:40:20)         |
| ComfortCall            | If there is some future delivery or Follow up with the customer.                                                              |
| Linkedbill             | Applicable in case of return invoice. Invoice number against which return invoice is being generated.                         |
| SalesorderNumber       | If the bill type is a sales order, then Instead of BillNumber we should mention SalesOrderNumber.                             |
| Fitting charge         | if we are charging extra charge eg. Delivery charge.                                                                          |
| PlaceofSupply          | State Code/State name of Delivery                                                                                             |
| Sales Channel          | Source channel of sale (ecom,app,omni,offline)                                                                                |
| Employee id and name   | Store sales manager details.                                                                                                  |
| transactionNumber      | If the invoice has Transaction  Number.                                                                                       |
| invoiceReferenceNumber | IRN number(Incase of b2b invoice)                                                                                             |
| dynamicQrCode          | b2bQRcode                                                                                                                     |
| trackingNo             | Courier Tracking Number.                                                                                                      |
| courierBookingDate     | Booking date of Courier.                                                                                                      |
| courierName            | Courier name (Eg. Bluedart,Fedex)                                                                                             |
| expectedDeliveryDate   | Expected date of Delivery.                                                                                                    |
| linkedBillDateTime     | date time of reference bill.                                                                                                  |
| salesOrderDateTime     | date time of sales order number.                                                                                              |
| courierReferenceNo     | reference Number of courier(Eg. Shipment number)                                                                              |
| invoiceAddresses       | Its delivery address. Applicable on home delivery orders. We have customer address details(billing address) in customer info. |