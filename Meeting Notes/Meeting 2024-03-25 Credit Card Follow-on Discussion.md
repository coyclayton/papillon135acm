# Architecture Discussion for Auth.net vs TranSafe
2024-03-25 : 15:30
Follow up to [[Meeting 2024-03-07 Credit Card Processing]] meeting

## Attending:
- Wolf Zon ([[135ACM Team|**]])
- Mark Weatherford ([[i3 Verticals & TranSafe|**]])
- Coy Clayton ([[Engineering & Integration|**]])

## Entry Summary
- All sides are confused on the architecture of our current processing relationships.
- Coy's goal was to establish if i3 Verticals / TranSafe had a worthy competitor to Authorize.net
- Mark thought that there was a card gateway relationship between Auth.net and ALPro.  There is NOT!

## Discussion
- Took some doing but Mark now understands that there is NOT a card gateway relationship between Auth.net and ALPro
	- Reservations Center and Front Desk phone calls are using ALPro (via TSYS) for manual entry, card not present transactions
	- Card Present Transactions are also running thru TSYS
	- Mark did not clearly understand this,  he does now.
- Based on the reports that Barb provided Mark back in 2022 Mark was able to divine and clarify the payment structure as follows:
	- Auth.net is Gateway to Chase PaymentTech (now just chase)
	- ALPro uses TSYS Virtual Terminal as Gateway and Processor is Chase PaymentTech
	- The airline did not provide the reports but it is safe to say that the structure on the airline side is identical.
- Current proposal
	- suggest moving i3 Verticals into the place of Chase PaymentTech for NON-E-Commerce merchant ids
	- leaving Auth.net ecommerce MIDS (merchant ids) with Chase PaymentTech
		- <font color="yellow">There is the possibility that we could loose volume discounts for online transactions</font>
- By switching our Auth.net gateway to i3 Verticals/TranSafe:
	- all the lookup and transaction introspection we do now would be done inside 135ACM thus eliminating a security checkpoint and interlinking reservation and payment data. This would drastically improve consistency in our payment system.

## Actions Items
- Mark to setup a demo of TranSafe virtual terminal/gateway service for Coy's evaluation
- Coy to work with [[Core Papillon Accounting]] and [[Core GCSA Accounting]] to determine the cost impacts (if any) of leaving Auth.net transactions with Chase.

---
#creditCards 