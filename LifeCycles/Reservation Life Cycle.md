

## // Phase 1 - The Origin of Data

```mermaid
journey
    section Availabilty Management
      Product Management: 8 : PI
      Slot Management: 8 : PI, Yield
      Package Management: 8 : PI
    section Price Management
	   Pricing Structures: 7 : Sales, PI, Eng
	   Commission Structures: 7 : Sales, PI
	   Agency Management : 8 : Sales, PI
```

---
<div style="page-break-after: always;"></div>

## // Phase 2 : The Reservation Advent

```mermaid
journey
    section Research
      Availability Search: 8 : Res, CSR
      Res Search: 8 : Res, CSR
    section Booking Process
	   Base Booking Entry : 8 : CSR, Res
	   Pax Data Entry & Classification : 9 : CSR, Res
	   Addons: 7 : CSR, Res
	section Payment
		Credit Card : 9 : CSR, Res
		Voucher : 4 : CSR, Res
		Pre-Paid : 4 : CSR, Res, Acctg
		Cash-Pickup : 1 : CSR, Res, Sales, PI, Acctg
```

### Useability Questions & Concerns
- Questions Pending
	- How to you find people with misspelled names
	- How do you search by alternate identifiers
		- Email, Phone, Guarantee Number (may be alpha)

---
<div style="page-break-after: always;"></div>
# // Phase 3: The Living & Evolving Res
```mermaid
journey
	section Res Manipulation
	  Passenger Data Update: 9 : Res, CSR
	  Pax Reconfirmation: 5 : Res, CSR
	  Reaccomidation : 6 : Res, CSR
	  Rescheduling : 8 : Res, CSR
	  Seating : 2 : Res, CSR, Tower
	  Cancellation : 7 : Res, CSR
```

### Special Case Considerations
- Possible scenarios include
	- Cancellation Policy
	- Cancelation Protection
### Reservation Reconfirmation
- Reservations is included in either an "isReconfirmed" or not.  This meaning that:
	- the passenger has contacted the reservation to confirm their details.
	- the passenger has been contacted by the res center
	- neither of those have happened in which case we need to reach out 

---
<div style="page-break-after: always;"></div>
# // Phase 4: Executing on the Reservation

```mermaid
journey
	section Operations
		Transportation: 1 : Res, CSR, Trx
		Check-In Process: 3 : Res, CSR
		Upgrade/Upsell : 7 : Res, CSR
		Seating & Manifest : 4 : Res, CSR, Tower, Fltln
		Flight Ops Integration: 2 : Res, Csr, Tower, Fltln, FlightOps
	section Case Processes
		Reaccomdation: 3 : Res, CSR
		Refund/Refly : 3 : Res, CSR
		Weather/MX : 3 : Res, Csr
	section Paperwork
		Cashier End of Day : 2 : CSR
		Other Closings : 2 : ??
		
```

---
<div style="page-break-after: always;"></div>
# // Phase 5 : Accounting, Verification, Billing
```mermaid
journey
	section Reporting
		Card Report : 6 : Acctg, CSR
		Cash Report : 6 : Acctg
		Counter Cash-Out Process : 1 : CSR, Acctg
	section Reconciliation
		Correctness Validation: 3 : Acctg
		Invoice/Uninvoice Process: 3 : Acctg
		GL Export Posting : 3 : Acctg
		Payment Processing: 3 : Acctg
		Post Flight Adjustments : 3 : Acctg		
```

---


## Reservation State Chart

refactor with decision of res > 0 or Dispositioned other
```mermaid
stateDiagram-v2
	classDef deepBlue fill:#998CCA,margin:15px

	state "Booking Init. with Booking Hold" as init
	state "Booked" as booked
	state "Re-Confirmed" as confirmed
	state "Checked-In" as checkedin
	state "On Experience" as onexp
	state "Disposition:Complete" as complete
	state "Closed" as closed
	state "Dispositioned:Other" as disp

	class init,booked,confirmed,checkedin,onexp,complete,closed,disp deepBlue
	
	[*] --> init
	init --> booked : Agent takes payment promise
	init --> disp : Agent terminates booking
	booked --> confirmed : Agent contacts guests and reconfirms details.
    booked --> disp : Agent/Guest Cxl
	confirmed --> checkedin : Agent performs check-in
	checkedin --> confirmed : Agent performs uncheck-in
	confirmed --> disp:  Agent/Guest Cxl
	checkedin --> onexp : Guest departs on experience
	onexp --> complete : Guest Returns from Experience
	complete --> closed : Accounting run's their invoice batch process
	closed --> complete : Accounting walks back reservation
	closed --> [*]
	disp --> complete : If VALUE of reservation > 0
```