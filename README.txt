# Hotel Quality Assesment tool (Simple Web scraping application)
## Video Demo:  <URL HERE> -> to be added when the video is ready :-)
## Description:

This is a web scraping application in the form of a Jupyter Notebook that compares a number of destinations in terms of the weighted average rating of their hotels. This comparison presents how "good" the quality of the lodgings of each destination is compared to that of other destinations, and hopefully helps the user with their decision on which place(s) to visit and where to stay in their vacations. 

Destinations may be as big and abstract as countries, islands etc. or as small and specific as city squares, parks, premises of a landmark / monument etc. - and this is where it gets particularly useful and interesting! The user may target as (reasonably) many destinations as they like, and get an insightful bar chart of the regions sorted by their average rating in descending order. The destinations input must be like in the examples (see comments in the notebook). Slight text errors do not matter, as long as there is no region with that slightly different text. if the user is not sure about the exact wording of a destination, it might be a good idea to test it on the website (booking.com) first.

Results are based on a sample of hotels, the size of which is also set by the user. The sample can include up to 1,000 hotels (from 40 result pages of 25 hotels each). If a region has less than that, all hotels are taken into account. If it has more than that, they are still a representative sample of the population. It is recommended that the sample size be set to at least one hundred, which are the first 100 hotels from each destination the search engine returns. It is important to note that the first few result pages are often enough for the site users to select the hotel they will stay at.

The scraper does the following for every destination selected by the user:

1) Performs a search for the destination (no particular dates or other filters) on the home page of Booking.com
2) Visits the result pages consecutively
3) Collects info for every hotel (including the rating and the number of reviews) in each result page that has at least one review and a valid rating until the sample size is reached or there are no more hotels to browse
4) Performs a very basic data cleansing procedure on the information gathered

After the info from all destinations is collected, the individual (hotel) ratings for each destination are weighted with the number of individual reviews to produce a reliable metric. The average ratings by destination are stored together and a sorted bar chart is produced.

Many different scenarios have been carried out to make sure that the code runs smoothly and bug - free. Proper comments are included in the notebook for the user to understand what the code does step by step. The code could have been a little tighter, but it was intentionally left the way it is in order to help anyone understand it and make use of it if they wish. The code can be expanded to do other fantastic things like comparing prices, examining more specific aspects of quality (cleanliness, breakfast etc.), building word trees on the guests'comments and many more.

Since the scraping procedure is quite cumbersome and needs a few minutes to return the output (normally less than 10 minutes for a relatively demanding request), it might be a good idea to avoid multitasking while running it. Just lay back, make a cup of tea, observe it work its magic. Soon you will know which of the places you are interested in has the best hotels to visit!

## Technologies Used

- Python modules (Selenium etc.), Jupyter Notebooks

## Usage

Just open Jupyter Notebooks on your browser, set the folder you wish to run it on, and enjoy!

## Installation

Jupyter Notebook needs to be pre - installed. Other than that, chromedriver.exe is required to be present at the set folder for the magic to happen. (Included here, but also see: https://chromedriver.chromium.org/downloads)

## Credits

Other than me? The people on the internet I guess. There are probably more sophisticated applications out there, but I am proud to declare that this one I built myself!

## License

This is my gift to the world. Anyone may use it as they see fit. However, mentioning the creator will be highly appreciated.
