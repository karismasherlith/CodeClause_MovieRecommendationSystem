# CodeClause_MovieRecommendationSystem
Python Code for Movie Recommendation System

1. IMPORTING MODULES
   - pandas: The pandas library helps provide structured data frames for the manipulation and analysation of large sets of data in the form of CSV files.
   - train_test_split: This library is used for splitting the dataset into training and testing subsets.
   - cosine_similarity: This function calculates the cosine similarity between two vectors or sets of vectors.
   - CountVectorizer: This is used to convert a text document into a matrix of token counts, which is very common during the natural processing of datasets.
     
2. LOADING DATASETS
   - The 2 datasets are loaded into 2 different data frames named 'ratings_data' and 'titles_data' with the help of the read_csv() function.
   - The 'ratings_data' contains the dataset related to ratings of movies by users.
   - The 'titles_data' contains the dataset of the movie titles provided.
     
3. MERGING DATASETS
   - Both the data frames are then merged based on the common column 'item_id' and stored into the 'movie_data' data frame.
     
4. STRUCTURE OF THE MERGED SET
   - The structure of the merged data frame is understood by displaying the first 5 rows of the data frame 'movie_data' with the help of .head() function.
     
5. SHAPE OF DATASET
   - The total number of rows and columns in the data frame is returned by using the .shape() function.
     
6. INFORMATION OF DATASET
    - The basic information regarding the data frame is obtained using the .info() function.
    - This contains information such as the number of null values, column names and their data type etc.
      
7. CALCULATING THE AVERAGE RATING FOR EACH MOVIE
    - We first convert the merged data into a data frame format and then group them by titles along with the mean average rating for that particular movie and store it in a 'ratings' data frame.
    - We then calculate the number of ratings provided for each of the titles by grouping them and naming the column as 'num_of_ratings'.
    - The data frame at the end consists of the number of ratings for each movie and the average rating for that particular movie.
      
8. CHECKING THE RATING DATASET
    - We then understand the new data frame and its structure with the help of the .head() function.
    - This gives out 5 rows and shows the columns and the values they hold.
      
9. CREATING PIVOT TABLE
    - We then create a pivot table named 'user_ratings' from the 'movie_data' data frame.
    - This pivot table will take the 'user_id' as the index, the 'title' as the column names and the 'rating' as the values for the pivot table.
    - We then find out the structure of this pivot table by displaying the first 5 rows of the table with the help of the .head() function.
      
10. CREATING SPARSE MATRIX
    - This helps us to fill out any missing values in the pivot table with 0.
      
11. CALCULATING SIMILARITIES
    - We calculate the similarity between each pair of movies by taking 'user_ratings' as the input.
    - 1 represents exact similarity, 0 represents no similarity and -1 represents perfect dissimilarity.
        
12. MANUAL TESTING
    - We create a function which takes the movie title from the user.
    - We first extract just the movie name by splitting it from '(' and then convert it into lower case format.
    - We then find the index of the movie from the 'titles_data' which contains the user input movie title name.
    - A list of tuples is created containing the index and the similarity which was found in previous steps.
    - The list is then sorted based on descending score so that the value with the highest similarity is displayed.
    - The top 5 movies that are similar are then stored in a list named 'top_movies' and then returned.
    - When the function is called it first asks the user to enter a movie name and then return 5 similar movies excluding the entered movie.
      
