Current as of 2024-03-26
## Working Goals:
* [[Reservation Life Cycle]] <font color="orange">( In Progress )</font>
* [[Flight Operation Life Cycle]] <font color="gray">( Exists / Integration Not Started )</font>
* [[Credit Card Processing]] <font color="orange">( In Progress )</font> 


```mermaid
flowchart TD
	Workable
	Untested
	Active
	Unaddressed
	Broken

	classDef workable fill:#196f3d
	classDef untested fill:#D35400
	classDef active fill:#EC407A
	classDef broken fill:#A93226
	classDef unaddr fill:#0D47A1

	class Workable workable
	class Untested untested
	class Active active
	class Unaddressed unaddr
	class Broken broken
```


```mermaid
flowchart TD
	package[Packaging & Products] --> reservations[Reservation Management]
	inventory[Inventory Control] --> reservations
	agencies[Agency Management] --> reservations
	pricing[Rate & Commission Mgmt] --> reservations
	payment[Payment Processing] --> reservations
	payment --> checkin[Check-In Mgmt & Cash Handling]
	payment --> api[API Integration]
	reservations --> checkin
	reservations --> transport[Ground Transportation]
	transport --> checkin
	api --> reservations
	api --> 3pi
	checkin --> flight[Flight Operations **]
	flight --> eod[Cashier / End of Day Processes ]
	eod --> accounting[Invoicing, Billing, & Reconciliation]
	accounting --> 3pi[3rd Party Integrations]
	accounting --> stats[Statistics]
	accounting --> salesRep[Sales Feedback and Reporting]
	archive[ALPro Data Archive] --> stats
	archive --> salesRep
	archive --> accounting

	classDef workable fill:#196f3d
	classDef untested fill:#D35400
	classDef active fill:#EC407A
	classDef broken fill:#A93226
	classDef unaddr fill:#0D47A1

	class package workable
	class inventory workable
	class pricing untested
	class agencies workable
	class reservations active
	class api active
	class transport untested
	class payment active
	class checkin active
	class accounting active
	class flight untested
	class checkin unaddr
	class eod unaddr
	class stats unaddr
	class stats unaddr
	class salesRep unaddr
	class 3pi unaddr
	class archive unaddr
	
	
```


## Additional Indexes
- [[Team Index|Subject Matter Experts Index]]
