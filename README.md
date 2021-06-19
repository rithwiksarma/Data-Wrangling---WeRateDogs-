# Data-Wrangling---WeRateDogs-

<h1> Wrangling Report </h1>

<h2> Data Gathering </h2>

From three different sources:

<ol>
  
  <li> <h4> The WeRateDogs Twitter archive : </h4> The WeRateDogs Twitter archive provided by Udacity. This contains basic tweet data for all 5000+ of their tweets, but not everything.I manually downloaded this file manually by clicking the following link: twitter_archive_enhanced.csv </li>
  
  <li> <h4>The tweet image predictions :</h4>  What breed of dog (or other object, animal, etc.) is present in each tweet according to a neural network. This file (image_predictions.tsv) is hosted on Udacity's servers and should be downloaded programmatically using the Requests library and the following URL: image_predictions.tsv  
  </li>
  
  <li> 
    <h4> Data via the Twitter API : </h4>  Querying the twitter API using Tweepy library to get basic data such as retweet count, favorite count, etc. </li>
 
  
 </ol>




<h2> Data Assessing </h2>

<h3> Quality Issues </h3>

<h4> twitter_enhanced_df : </h4> 
<ul>
  <li> Some rows in rating_denominator have a rating of more than 10 and some with less than 10 </li>
  <li> Some rows in rating_numerator have an extremely high rating </li>
  <li> Datatype of timestamp retweeted_status_timestamp is object instead of datetime </li>
  <li> Erraneous values in name ('a', 'an', 'O', 'JD' etc) </li>
  <li> Expanded_urls has "NaN" valued rows </li>
  <li> name contains "None" values </li>
  <li> Unwanted columns (retweeted_status_id , retweeted_status_user_id, retweeted_status_timestamp) </li>

  </ul>

<h4> image_predictions_df : </h4> 
<ul>
  <li> Unnecessary columns. Only wanted columns are taken in </li>
  </ul>
  
  
  <h4> api_data_df : </h4> 
<ul>
  <li> Datatype of date_time is object instead of datetime </li>
  </ul>
  
  
<h3> Tidiness Issues </h3>
<ul>
  
  <li> 4 columns present for each stage in dog's life (doggo, pupper, puppo, floofer) </li>
  <li> No need for three dataframes. Can be combined into one </li>
  
  </ul>
