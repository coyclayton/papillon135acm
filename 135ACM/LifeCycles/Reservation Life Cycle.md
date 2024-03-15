# // Phase 1 : Setup
### Product Created
* <font color="orange">OK: Functionality acceptable</font>
## Slots Created
 * <font color="orange">OK: Functionality acceptable</font>
## Package Created
* <font color="orange">OK: Functionality acceptable</font>
## Pricing, Net, and Commission Structures Established
- <font color="coral">UNTESTED: Functionality Not Thoroughly Vetted</font>
- Prime to be a bugs nest

---
# // Phase 2 : The Reservation Advent
## Availability Searched
* <font color="orange">OK:  Pending Acceptance Testing</font>
## Reservation Created
- <font color="magenta">BLOCKED:  Process breaking bugs exist</font>
#### Reservation Payment
- <font color="green">OK:  CC Workflow</font>
- <font color="coral">PENDING: Voucher Workflow</font>
- <font color="coral">PENDING: Pre-Paid Workflow</font>
- <font color="coral">PENDING:  Cash-Pickup Workflow</font>
## Passengers Seated
* <font color="grey">UNKNOWN : Unable to Test</font>
* Unknown when this occurs

---
# // Phase 3: The Living & Evolving Res
## Reservation Searched
- <font color="orange">OK: Functionality</font>
- Questions Pending
	- How to you find people with misspelled names
	- How do you search by alternate identifiers
		- Email, Phone, Guarantee Number (may be alpha)

## Reservation Updated/Reconfigured
- <font color="coral">UNKNOWN:  Pending Update</font>
- Possible scenarios include
	- Moving reservation to different date, time, or even package.
	- Canceling reservation
		- Complications include
			- ? Cancellation Policy
			- ? Cancelation Protection
## Reservation Reconfirmation
- <font color="coral">UNKNOWN:  Pending Update</font>
- Reservations is included in either an "is reconfirmed state".  This meaning that
	- the passenger has contacted the reservation to confirm their details.
	- the passenger has been contacted by the res center
	- neither of those have happened in which case we need to reach out 

---
# // Phase 4: Executing on the Reservation

## Transportation Pick-up
 - <font color="grey">UNKNOWN:  Unable to reach process</font>

## Reservation Check-In & Payment
- <font color="magenta">BLOCKED:  Unable to complete step,  breaking bugs exist.</font>

#### Upgrade/Upsell/Fee Payment Process
- <font color="grey">UNKNOWN:  Unable to reach process</font>

## Reservation Manifesting & Operations
* <font color="grey">UNKNOWN: Unable to reach workflow</font>
* See [[Flight Operation Life Cycle]]

## Customer Satisfaction/Re-accommodation Pathway
- <font color="grey">UNKNOWN:  Unable to reach workflow</font>
- Possible workflows include
	- Refund / Refly / or Cost Adjustments due to weather
	- Rescheduling due to unplanned MX or WX
## Front Counter Cash-out & End-Of-Day
- <font color="grey">UNKNOWN:  Unable to reach workflow</font>

---
# // Phase 5 : Accounting, Verification, Billing

## Counter Cash-out Validation
- <font color="grey">UNKNOWN:  Unable to reach workflow</font>
## Reservation Validated for Correctness
- <font color="magenta">BREAKING: Breaking bugs exist but in progress</font>
- Cash Reports, CC Reports, etc.  Labels are present but data displayed is not correct.

## Reservation Invoiced & Change Locked
- <font color="magenta">UNFINISHED: Some foundational parts in place.</font>

## Reservation Un-Invoiced (Unhappy Path)
- <font color="grey">UNKNOWN:  Unable to reach path.</font>
