Follow up meeting to [[Meeting 2024-03-20 Reservations Design]] , part of the [[Reservation Life Cycle]]
## Attending 
- Leina ([[Product Integrity & Reservations]])
- Bryce ([[135ACM Team]])
- Coy ([[Engineering & Integration]])


## Discussion
- Reviewed request to add "Hummer" to package classification. They added "Vehicle".  Pointed out that the taxonomy and classification of that term is not great as both airplanes and helicopters are syntactically "vehicles" but that the case label works for us.  Allowing these to be dynamically provisioned in settings is likely to be the better route but not critically important.
- Reviewed and Demonstrated the updated Add-On creation and also clarified use cases.
- Reviewed and finalized requested Add-On pricing functionality and reviewed the completed "Rework" items from previous meeting.
	- They work as intended
- Reviewed supervisor PIN policy.  Bryce wanted to do double check that we wanted to enter the supervisor pin only once per edit instance.  We confirmed this.
	- On create: reservations add-ons with the 'require authorization' or that exceed the max authorized value will require a supervisor pin prior to creation.
	- On edit:  same conditions but will require supervisor pin before changes are committed
- Bryce committed to having the details wired together by tomorrow and will let Leina know when she's ready to full process test.
- This may be the last thing on the reservations front we have to wrap up.

## Follow-On
- Quick call with Leina tomorrow to confirm ready. (3/26)


---
#reservations 