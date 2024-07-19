
## Actors/Roles
- Reservation Agent (RA)
- Trusted Cash Pickup Employee (TCPE)
- Front Counter Agent (FCA)

## Process Flow

```mermaid
graph TD
	respaid(RA Accepts Payment w/ CP Method *1) -->| RA Records Deposit Slip Number| awaitbatch(Payment entered into cash pickup list *2)
	awaitbatch -->|TCPE Batches Items Together *3| batchPrinted(Batch Printed & Ready for Pickup Run *4)
	batchPrinted --> |TCPE Makes Error & Voids Batch *5| batchvoid(Batch Voided *6)
	batchvoid --> awaitbatch
	batchPrinted -->|TCPE Does Pickup Run| inposs(TCPE visits company terminal bldg *7)
	inposs -->|TCPE Presents FCA w/ Cash & Batch 'invoices'| cashverify(FCA & TCPE verify amounts against batch 'invoice')
	cashverify --> |FCA has open Till| received(FCA receives cash into their till)
	cashverify --> |FCA has no open Till| inposs
	received --> reported(Batches cleared become part of FCA's Closing Drop)
		
```

### Footnotes
1. From this point forward from the reservation's point of view and for the purposes of check-in this reservation is paid.  We become the collectors now.
2. The PAYMENT is now entered into the list of items to be picked up
3. This is a PRIVELEGED action and should not be available to just anybody.  Once a reservation payment is a member of batch it cannot be associated with any other live batch.
4. The trusted employee uses the batch print to go perform the actual collections
5. Its possible that the trusted employee may have made an error when creating the batch. Maybe included something that should not have been included. It happens for more reasons than we can enumerate here.  As long as the batch has not progressed any further then they should be able to void the batch.
6. All payment items associated with the batch should be released and be able to be re-associated with a NEW batch.
	1. Voiding a batch should be tracked for historical reasons.
7. The trusted employee is out on the run at this point collecting cash and counting it in person, verifying the amounts against the batch 'invoice' they have in their possession.  At the completion of the run they physically visit a front counter.