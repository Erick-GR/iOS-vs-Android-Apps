# iOS-vs-Android-Apps
A comparisson between Google playstore and Apple appstore.

## Extract

Datasets sources:
- Apple Apps: https://www.kaggle.com/ramamet4/app-store-apple-data-set-10k-apps
- Google Apps: https://www.kaggle.com/lava18/google-play-store-apps

The datasets we used are in csvs format, which we can use easily with Python's library Pandas. There are divided by Google or Apple.

## Transform

First, we drop duplicates in case their exists with the id of the original database, and drop `NA` . Then we select which columns were useful and have consistency. And finally we homologate the category names in both databases, in order to divide our database by category.

## Load

Using our Python code we load our databases in SQL authomatically.

