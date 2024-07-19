
## Attending
- Wolf Zon [[135ACM Team]]
- Coy Clayton [[Engineering & Integration]]

## Review & Rework
- Day pax view was not showing because not default manifest type was assigned.
- Single lines inventory displays are normal
	- REQ:  Create a warning at the line items that would warn of of potentially split party.
		- EG: 4 aircraft with 1 empty seat per a/c would show 4 seats, but that does not mean we can seat 4 peeps.
- Cash pickup batch voiding:  Done
	- REW: Must be able to view voided batches.  Use VOID as a disposition
	- NOTRV: Process
	- BUG:  Unable to find reservation numbers in Res from Res # in cash pickup window
- BUG:  Cannot find reservation in 
- UX Bug: Confirmation Number, Res No,  PNR all the same number but listed differently throughout the application
- Point of Sale Management:
	- Looks great as is.
	- REQ:  Add a notes field to the close process.
	- REQ:  If difference other than zero notes MUST be added in order to continue close.
	- UX:  Entry fields should be blue
	- Good with Request.
	- See Figure Below #1

## Follow-on

* Wolf would like Lei and Andrea to be present for [[Cadence Mtg 2024-05-16]] to go thru the reservations process from end to end and identify problems in the process.
* Coy to Coordinate availability be EOD Tuesday

## Figures

Figure #1
![[CloseOpenDrawerInterrface.png]]


## Misc
---
#requests #rework #ux 