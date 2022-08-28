# WeRateDogs


This analysis is based on tweets made from #WeRateDogs.
So, I did be going from Gathering phase to Assessing phase and lastly to Cleaning phase. 

<img src= https://video.udacity-data.com/topher/2017/October/59dd4e05_dog-pred/dog-pred.png width="600" height = '600'>

<h2><ins><font color = 'green'> Gathering Phase </font></ins></h2>

This wrangling report is based on the tweets made related to #WeRateDogs, Here, we gathered our datasets using three different methods, which are -- <li> The normal download method </li>
                      <li> via request mathod </li>
                      <li> via web scraping using Tweepy library </li>
                      
 So, the first dataset is gotten by downloading the dataset given to us, The second dataset is gotten using the request library by using the link provided to us, While the last dataset is gotten using the Tweepy library by using an API to get the necessary info needed.

<h2><ins><font color = 'green'> Accessing Phase </font></ins></h2>

After gathering the datasets, I now have to access it.
Accessment is done in two phases  -- <li> Via visual accessment </li>
                                     <li> via Programmatic accessment </li>
                          
After doing this accessments, we were able to bring out some issues wrong with the datasets which we split into two types --
<li> Quality issues </li>
<li> Tidiness issues </li>

The issues derived  are --

<h3> Quality issue </h3><br>

<li> Remove retweets and replies (text column starts with RT @) as a user can retweet their on tweet.</li>
<li> Columns likes 'in_reply_to_status_id', 'in_reply_to_user_id', 'retweeted_status_id ', 'retweeted_status_user_id', s'retweeted_status_timestamp' and 'expanded_urls' has null values..</li>
<li> Incorrect Datatype -- Tweet_id column should be an object and not int since we cannot make any arithmetic operation with it,<br>
    The timestamp column should be in datetime data type and not object datatype .<br>
    tweet_id should be an object not int datatype for the df2 dataset too <br></li>
<li> The timestamp should be split into date and time </li>
<li> Get the exact tweet source. </li>
<li> We have some entries which are not names at the name column. </li>
<li> Texts in 'p1', 'p2', 'p3' column should all be in lower case to avoid reading the same text differently. </li>
<li> Rename 'p1', 'p1_conf', 'p1_dog', 'p2', 'p2_conf', 'p2_dog', 'p3', 'p3_conf','p3_dog' columns to make more meaning. -- Second Dataset </li>

<h3> Tidiness issue </h3><br>

<li> Doggo, floofer, pupper, puppo columns are like dog nick names / names , it should be made into a single column. </li>
<li> Some of the tables have similar columns, so they should be merge together. </li>

<h2><ins><font color = 'green'> Cleaning Phase </font></ins></h2>

Firstly, I made a copy of each datasets, then had to address the issues by cleaning them.
After that, I merged the whole datasets together , Then store it as <b>'twitter_archive_master.csv'</b>.

After this, I did analysis on the clean dataset, Pls check the file above for full view.

