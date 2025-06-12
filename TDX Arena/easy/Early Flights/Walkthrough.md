Walkthrough:
	Upon opening the challenge website, we see a rather pleasantly designed airline ticket booking site, and of course, a window for selecting the date and destination, as is common everywhere.
	Scrolling down, we see a company description, as well as "Best for you" offers for ticket purchases.
	However, trying to click any buttons on the site reveals no navigation to another page.
	The only active buttons on the site are:
		Departure and return date selection
		City selection
		Search button
	Also, our challenge URL is "https://host-5mfefq3h-prod.prod.cywar.xyz:32771/"
	Accordingly, our suspicion falls on manipulating the flight dates.
	- Let's try to select regular dates and one of the suggested "advantageous" routes:
		From Tel-Aviv to Paris
		Dates: Departure on 20/06/2025, return on 29/06/2025
	- Click "Search"
		We see a dropdown offer and a "Buy Now" button.
	- What to pay attention to:
		URL change:
		https://host-5mfefq3h-prod.prod.cywar.xyz:32771/flights?src=Tel-Aviv&dst=Paris&from=2025-06-15&to=2025-06-29
	- Let's try to manipulate the URL string to change the dates to invalid ones (past or far in the future):
		When changing the year, the site has protection and asks us to select either dates later than today or a return ticket not more than 2 years from the departure date.
		Let's try to make a flight a couple of days in the past:
			flights?src=Tel-Aviv&dst=Paris&from=2025-06-15&to=2025-06-29 changes to flights?src=Tel-Aviv&dst=Paris&from=2025-06-15&to=2025-06-13
			- Both dates are later than today.
			- No difference greater than 2 years.
		As a result, we see an error screen and our flag.

Challenge solved.
