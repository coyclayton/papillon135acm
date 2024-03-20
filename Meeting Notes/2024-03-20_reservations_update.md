## Attending
- Wolf [[135ACM Team]]
- Coy [[Engineering & Integration]]
- Leina [[Product Integrity & Reservations]]
# Addon's Setup and Handling

## Package/Product Categorization
- Add Hummer and Other to Package Types for clarity
## Addon's
- Package Applicability Selector
	- On page load show all and Type dropdown should show "Display All"
		- the search and/or type dropdown selections narrow the displayed data
	- Add a "Select All" button at the top of the "Select" column that takes the action of selecting all DISPLAYED packages.
	- Adjust modal window title to be more "Breadcrumby"
		- eg:  Addons >> {Add On Title} >> Applicable Packages
- Add a flag that forces an Admin Pin when adding the "Add-on"

## Rework
- Addon Rate Scheduling
	- Two Modes
		- Add field "Add-on Cost Mode"
		- Free Entry
			- Always available but value must be at or less than max authorized value
			- If exceed max authorized value then flag and require supervisor approval to continue
		- Scheduled Value
			- Utilizes a table of Start/End/Effective Dates
			- If no rate set is available for a reservations date parameters then said add-on is not available.
			- Break rates out into "Base Rate" and "Fees" to match the rate structure that is in place throughout the rest of the system.
	- Rename Addon Rate table to "Scheduled Rates"

## Follow-On
- Updates due Mid-Morning Thursday 3/21