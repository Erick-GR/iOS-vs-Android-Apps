# iOS-vs-Android-Apps

This project consists of a comparison between the applications on the Google playstore and the Apple appstore. The main objetive is to extract the app categories for each store and save it in a database. This way it will be possible to compare information like average price per category, app quantity per store, range of prices, etc.

## Extract

The first step was to find the dataset from where to extract the information. For this, the page [Kaggle](https://www.kaggle.com/) was revised and from a wide variety of datasets the following two were selected:

- [Google Play Store Apps](https://www.kaggle.com/gauthamp10/google-playstore-apps)
- [Mobile App Store (7200 apps)](https://www.kaggle.com/ramamet4/app-store-apple-data-set-10k-apps)

The datasets we used are in .csv format, which we can use easily with Python's library Pandas. There are divided by Google or Apple.

## Transform

Each dataset needed a different type of transformation. The Apple App Store dataset was clean enough so there was only the need to erase some rows, but no columns. On the other hand, the Google Playstore contained some rows that needed erasing from the dataset. 

On both tables we droped duplicates in case their exists with the id of the original database, and drop `NA` . Then we selected which columns were useful and have consistency. And finally we homologate the category names in both databases, in order to divide our database by category. This is the category relation:

- **Apple** -- **Google**
- Book --  BOOKS_AND_REFERENCE
- Business -- BUSINESS
- Catalogs -- no se
- Education -- EDUCATION
- Entertainment -- ENTERTAINMENT
- Finance -- FINANCE
- Food & Drink -- FOOD_AND_DRINK
- Games -- GAMES (todos jaja)
- Health & Fitness -- HEALTH_AND_FITNESS
- Lifestyle -- LIFESTYLE
- Medical -- MEDICAL
- Music --MUSIC_AND_AUDIO
- Navigation -- MAPS_AND_NAVIGATION
- News -- NEWS_AND_MAGAZINES
- Photo & Video -- PHOTOGRAPHY
- Productivity -- PRODUCTIVITY
- Reference -- BOOKS_AND_REFERENCE
- Shopping -- SHOPPING
- Social Networking  -- SOCIAL
- Sports -- SPORTS
- Travel -- TRAVEL
- Utilities -- TOOLS
- Weather -- WEATHER

## Load

Using Python, Jupyter Notebooks, Sqlalchemy, Pgadmin 4 and Pandas, we loaded our database directly from the jupyter file. The main datasets were divided into smaller dataframes that consisted of one category per dataframe. The connection to the database was made using Sqlalchemy and each table was uploaded automatically.

If further analysis of the datasets needs to be made, the user can access to the databases created and filter or join the tables in order to find data such as a comparison between the average prices per category of each company, total app count, etc.
