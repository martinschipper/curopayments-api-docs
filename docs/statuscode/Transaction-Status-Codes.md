---
tags: [statuscode, transaction]
---

# Transaction Status Codes

Newly created transactions will have initially have a status code of `0`.

Depending on the payment method the status will be updated to reflect the current status. Every update to the transaction is registered in the Transaction History (visible in the backoffice).

### Status Code Ranges

The global status code ranges are:

Code Range | Description
---------|----------
`0` | Pending; waiting for acquirer.
`1XX` | Authorisation phase 1 codes (credit card).
`2XX` | Transaction completed successfully.
`3XX` | Transaction failed.
`4XX` | Refunds and reversals. These codes will be linked to a separate Refund/Chargeback/Reversal transaction.
`6XX` | Informational code for fraud or retrieval notifications. These codes will only be visible in Transaction History.
`7XX` | Waiting for confirmation or receiving of the transaction.

### List of Status Codes

Status Code | Description
---------|----------
0 | Transaction in progress
100 | Authorization successful
150 | 3D secure status 'Y' (yes), waiting for 3D secure authentication
152 | 3D secure status 'N' (no)
154 | 3D secure status 'U' (unknown)
156 | 3D secure status 'E' (error)
200 | Transaction successful
210 | Recurring transaction successful
300 | Transaction failed
301 | Transaction failed due to anti fraud system
302 | Transaction rejected
308 | Transaction was expired
309 | Transaction was cancelled
310 | Recurring transaction failed
330 | Authorization failed
333 | Card expired
334 | Suspicion of manipulation
341 | Lost card (was reported lost by owner)
343 | Hot card (known fraud with this card)
344 | Pickup card (card is flagged/blocked)
350 | Transaction failed, time-out for 3D secure authentication
351 | Transaction failed, non-3DS transactions are not allowed
352 | Transaction failed 3DS verification
370 | Wait time expired
399 | Acquirer request error
400 | Refund to consumer
404 | Reversal by system (transaction was never received or bounced)
410 | Chargeback by consumer
420 | Chargeback (2nd attempt)
450 | Authorization cancelled
511 | Subscription has expired
601 | Fraud notification received from bank
603 | Representment notification received from bank
604 | Retrieval notification received from bank
610 | Second chargeback notification received from bank
700 | Transaction is waiting for user action
701 | Waiting for capture
702 | Waiting for execution date
710 | Waiting for confirmation recurring
711 | Subscription waiting for payment
750 | Waiting for confirmation (from external party like a bank)
751 | Underpaid, waiting for merchant action
760 | Waiting for asynchroneous batch capture
761 | Waiting for batch capture
762 | Waiting for batch execution date
811 | Subscription on hold (automatic)
812 | Subscription on hold (manual)
