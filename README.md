# Travel Recommender System using Collaborative filtering

### Data Science Problem:
Build a recommendation system that helps travelers plan their itinerary. Goal is to be able to have a user input their preferences and be given recommendations at their destination not necessarily just by proximity.

For someone trying to plan out their trip, many times people will google search or look up travel blogs to get an idea of what to do.

### Data/Resources used:
- Website: [Trip by Skyscanner](https://www.trip.skyscanner.com/)
- Data was scraped from Trip by Skyscanner is a website that travelers can post their reviews and recommendations on hotels, restaurants and activities.
- Focusing on Austin, Tx I pulled the top 200 usernames from the leaderboards which resulted in over 5000 reviews.

### Packages
- Using [Beautiful Soup](https://pypi.org/project/beautifulsoup4/) I was able to scrape the data from the website to use in this project.

- Using [Selenium](https://www.seleniumhq.org/) I was able to open a virtual driver that would navigate through the website to pull the data. This was very useful for clicking on "I accept cookies button" and scrolling through the various users to get the data.

### Files:
- [Austin_Leaderboard.ipynb](https://github.com/aL1asWIN/Travel-Recommender-System-using-collaborative-filtering/blob/master/Austin_Leaderboard.ipynb) shows process of how I scraped the top 200 usernames from the Austin leaderboard
- [user_reviews_scraper.ipynb](https://github.com/aL1asWIN/Travel-Recommender-System-using-collaborative-filtering/blob/master/user_reviews_scraper.ipynb) shows process of how to scrape through all the usernames and extract the data. This uses selenium to scroll through each user extracting ratings, place names, categories and text data.
- [recommender_system.ipynb](https://github.com/aL1asWIN/Travel-Recommender-System-using-collaborative-filtering/blob/master/recommender_system.ipynb) shows recommender system using ratings. Created functions that allowed a user to add themselves to the existing dataframe that housed all reviews. Then could make recommendations based on similar users. Also had an item-to-item recommender based on places.

- [test_eda.ipynb](https://github.com/aL1asWIN/Travel-Recommender-System-using-collaborative-filtering/blob/master/test_eda.ipynb) this was testing nlp on the text data. I was not able to fully go through this process and is still in the works


### Executive Summary:
Overall I haven’t quite solved how to beat traditional ways to research travelling preparation. This is a simple baseline recommender system that has the potential to build upon into the future. I didn't quite get to allow users to input exact preferences, but I was able to get an user input to add themselves to an existing dataframe and then allowed the recommender system to give recommendations of similar users.

### Future goals to implement:
- Combine collaborative filtering and content based filtering. Use alternate methods such as Alternating Least Squares 
(ALS)
- Use the review text and dive into NLP further and apply a model ( KNN, Neural Network, etc.)
- Add more cities outside of Austin. Adding more users and cities will increase the amount of data to be used in the system.
- Build a web app through Flask to display an user interactive recommender system
