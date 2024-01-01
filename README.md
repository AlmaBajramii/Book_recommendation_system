# Book_recommendation_system

## Description:
A Book Recommendation System which recommends the users a selection of books based on their interests.

## Libraries Used:
- ipython-notebook - Python Text Editor
- sklearn - Machine learning library
- seaborn, matplotlib - Visualization libraries
- numpy, scipy- number python library
- pandas - data handling library

## Data Cleaning and Pre-Processing
The dataset consists of three tables; Books, Users, and Ratings. Data from all three tables are cleaned and preprocessed separately as defined below briefly:

### For Books Table:

- Drop all three Image URL features.
- Check for the number of null values in each column. There comes only 3 null values in the table. Replace these three empty cells with ‘Other’.
- Check for the unique years of publications. Two values in the year column are publishers. Also, for three tuples name of the author of the book was merged with the title of the book. Manually set the values for these three above obtained tuples for each of their features using the ISBN of the book.
- Convert the type of the years of publications feature to the integer.
- By keeping the range of valid years as less than 2022 and not 0, replace all invalid years with the mode of the publications that is 2002.
- Upper-casing all the alphabets present in the ISBN column and removal of duplicate rows from the table.

### For Users Table:

- Check for null values in the table. The Age column has more than 1 lakh null values.
- Check for unique values present in the Age column. There are many invalid ages present like 0 or 244.
- By keeping the valid age range of readers as 10 to 80 replace null values and invalid ages in the Age column with the mean of valid ages.
- The location column has 3 values city, state, and country. These are split into 3 different columns named; City, State, and Country respectively.
- In the case of null value, ‘other’ has been assigned as the entity value.
- Removal of duplicate entries from the table.

### For Ratings Table:

- Check for null values in the table.
- Check for Rating column and User-ID column to be an integer.
- Removal of punctuation from ISBN column values and if that resulting ISBN is available in the book dataset only then considering else drop that entity.
- Upper-casing all the alphabets present in the ISBN column.
- Removal of duplicate entries from the table.

## Data Visualization

- Distribution of books published over the years is visualized using a bar chart.
- The top authors and publishers with the most books are visualized using count plots.
- Age distribution of readers is visualized using a histogram.
- Counts of readers from different cities, states, and countries are visualized.
- The distribution of book ratings is visualized.
- Explicit ratings (non-zero) are visualized separately.
- The distribution of explicit ratings is visualized.
- Counts of ratings for each book (Top 15) are visualized.
- 
## Summary
In summary, this project covers data cleaning, exploration, and some basic visualizations to understand the distribution of books, ratings, and user demographics. It provides insights into the characteristics of the datasets and sets the stage for building a book recommendation system.
