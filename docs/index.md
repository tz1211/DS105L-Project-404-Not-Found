---
title: "📚 Project Title"
date: 20 March 2023
date-meta: 20 March 2023
---

# 🤖 Project Title

**Team members:** 

- [Litong Zhong (Annabel)](https://github.com/Litong-Annabel)
- [Chengchao Lu (Spark)](https://github.com/Spark-LuC)
- [Yan Zhou (Terry)](https://github.com/tz1211)

## 📝 Project Description   

Are you curious about who will be crowned the next NBA MVP? Our MVP prediction website has got you covered! Get ready for an exciting journey where we dive into the world of elite basketball performance and statistical analysis to forecast the NBA's most valuable player.  

With the NBA showcasing the pinnacle of basketball talent, predicting the MVP award is a thrilling challenge. We crunch the numbers, analyze player stats, and examine historical trends to make insightful predictions. Our goal is to uncover the standout players who have the potential to rise above the competition and leave a lasting impact on the game.

But it doesn't stop there! The MVP race is always full of surprises, with unforeseen developments and breakout performances shaking things up. We'll keep you updated on the latest news, injuries, and team dynamics that could influence the MVP race.

Join our passionate community of fans, experts, and analysts who love nothing more than engaging in lively debates and speculation about the NBA MVP. We provide a platform for sharing opinions, insights, and predictions, fueling the excitement and anticipation surrounding this prestigious award.

Whether you are a die-hard basketball enthusiast or just starting to explore the world of NBA MVP predictions, our user-friendly website is designed to make the experience enjoyable for everyone. So come on board and embark on this thrilling journey with us as we try to unravel the captivating mystery of the next NBA MVP!  

![images - 1](https://github.com/tz1211/DS105L-Project-404-Not-Found/assets/114760508/4443b36e-3b28-4343-b327-a999105f7581)

Data Source: 
* [Basketball Reference](https://www.basketball-reference.com/)  
* [NBA Official Website](skysports.com/nba)  
* [ESPN Sports](espn.com/nba)   
* [NBA News Archive](https://global.nba.com/news)
* [BBC Sports News](https://www.bbc.co.uk/sport) 
* [Muck Rack](https://muckrack.com/)
* [Hugging Face](https://huggingface.co/)


## 📊 Data

### PROCEDURE MAP

<img width="2378" alt="Group Report: 404-not-found" src="https://github.com/tz1211/DS105L-Project-404-Not-Found/assets/114760508/7058c6c0-c454-4bd2-bbf5-8c515871542b">


### :one: Sports Matrix

### Table 1: Basic data

|      |   season | name                  | team                |   age |   %games_played |   minutes_played |   points |   assists |   attempted_field_goals |   attempted_free_throws |   attempted_three_point_field_goals |   blocks |   defensive_rebounds |   games_started |   made_field_goals |   made_free_throws |   made_three_point_field_goals |   offensive_rebounds |   personal_fouls |   steals |   turnovers |   field_goal% |   free_throw% |     3pt% |   assist_percentage |   block_percentage |   box_plus_minus |   defensive_box_plus_minus |   defensive_rebound_percentage |   free_throw_attempt_rate |   offensive_box_plus_minus |   offensive_rebound_percentage |   player_efficiency_rating |   steal_percentage |   three_point_attempt_rate |   total_rebound_percentage |   true_shooting_percentage |   turnover_percentage |   usage_percentage |   value_over_replacement_player |   win_shares_per_48_minutes |   is_mvp |
|-----:|---------:|:----------------------|:--------------------|------:|----------------:|-----------------:|---------:|----------:|------------------------:|------------------------:|------------------------------------:|---------:|---------------------:|----------------:|-------------------:|-------------------:|-------------------------------:|---------------------:|-----------------:|---------:|------------:|--------------:|--------------:|---------:|--------------------:|-------------------:|-----------------:|---------------------------:|-------------------------------:|--------------------------:|---------------------------:|-------------------------------:|---------------------------:|-------------------:|---------------------------:|---------------------------:|---------------------------:|----------------------:|-------------------:|--------------------------------:|----------------------------:|---------:|
| 1121 |     2022 | Bam Adebayo           | MIAMI HEAT          |    24 |        0.682927 |          32.5893 |  19.0714 |   3.39286 |                13.0179  |                 6.07143 |                            0.107143 | 0.785714 |              7.625   |               1 |            7.25    |            4.57143 |                      0         |             2.44643  |          3.05357 | 1.42857  |     2.64286 |      0.556927 |      0.752941 | 0        |                17.5 |                2.6 |              3.8 |                        2.1 |                           26.1 |                     0.466 |                        1.7 |                            8.7 |                       21.8 |                2.2 |                      0.008 |                       17.5 |                      0.608 |                  14.4 |               25   |                             2.7 |                       0.188 |        0 |
| 1122 |     2022 | Jarrett Allen         | CLEVELAND CAVALIERS |    23 |        0.682927 |          32.3036 |  16.1429 |   1.64286 |                 9.73214 |                 4.16071 |                            0.178571 | 1.33929  |              7.32143 |               1 |            6.58929 |            2.94643 |                      0.0178571 |             3.42857  |          1.73214 | 0.785714 |     1.67857 |      0.677064 |      0.708155 | 0.1      |                 8.2 |                3.7 |              3.9 |                        1.2 |                           24.5 |                     0.428 |                        2.7 |                           12   |                       23   |                1.2 |                      0.018 |                       18.4 |                      0.698 |                  12.7 |               18.1 |                             2.7 |                       0.225 |        0 |
| 1123 |     2022 | Giannis Antetokounmpo | MILWAUKEE BUCKS     |    27 |        0.817073 |          32.8955 |  29.8806 |   5.79104 |                18.5821  |                11.4328  |                            3.61194  | 1.35821  |              9.61194 |               1 |           10.2836  |            8.25373 |                      1.0597    |             2        |          3.16418 | 1.07463  |     3.26866 |      0.553414 |      0.721932 | 0.293388 |                31.7 |                4   |             11.2 |                        3.5 |                           30.4 |                     0.615 |                        7.6 |                            6.6 |                       32.1 |                1.6 |                      0.194 |                       18.7 |                      0.633 |                  12.2 |               34.9 |                             7.4 |                       0.281 |        0 |
| 1124 |     2022 | Cole Anthony          | ORLANDO MAGIC       |    21 |        0.792683 |          31.6769 |  16.3385 |   5.67692 |                14.0308  |                 3.89231 |                            6.01538  | 0.261538 |              4.86154 |               1 |            5.49231 |            3.32308 |                      2.03077   |             0.492308 |          2.63077 | 0.707692 |     2.61538 |      0.391447 |      0.853755 | 0.337596 |                28.9 |                0.8 |             -1.2 |                       -0.6 |                           16.2 |                     0.277 |                       -0.6 |                            1.6 |                       13.5 |                1.1 |                      0.429 |                        8.9 |                      0.519 |                  14.2 |               25.1 |                             0.4 |                       0.038 |        0 |
| 1125 |     2022 | OG Anunoby            | TORONTO RAPTORS     |    24 |        0.585366 |          36      |  17.125  |   2.60417 |                14.5208  |                 2.45833 |                            6.60417  | 0.520833 |              3.95833 |               1 |            6.4375  |            1.85417 |                      2.39583   |             1.54167  |          2.72917 | 1.47917  |     1.66667 |      0.443329 |      0.754237 | 0.362776 |                11   |                1.4 |              0.5 |                        0.1 |                           12.6 |                     0.169 |                        0.4 |                            4.4 |                       14.8 |                2.1 |                      0.455 |                        8.3 |                      0.549 |                   9.7 |               20.5 |                             1.1 |                       0.104 |        0 |
| 1126 |     2022 | LaMelo Ball           | CHARLOTTE HORNETS   |    20 |        0.914634 |          32.2933 |  20.1067 |   7.61333 |                16.72    |                 3.24    |                            7.53333  | 0.4      |              5.24    |               1 |            7.17333 |            2.82667 |                      2.93333   |             1.44     |          3.16    | 1.58667  |     3.26667 |      0.429027 |      0.872428 | 0.389381 |                35.7 |                1.2 |              3.4 |                        0.1 |                           17.4 |                     0.194 |                        3.3 |                            4.7 |                       19.7 |                2.4 |                      0.451 |                       11   |                      0.554 |                  15.3 |               28.2 |                             3.3 |                       0.116 |        0 |
| 1127 |     2022 | Lonzo Ball            | CHICAGO BULLS       |    24 |        0.426829 |          34.6286 |  13      |   5.08571 |                10.9429  |                 0.8     |                            7.42857  | 0.885714 |              4.42857 |               1 |            4.62857 |            0.6     |                      3.14286   |             1        |          2.42857 | 1.82857  |     2.34286 |      0.422977 |      0.75     | 0.423077 |                20   |                2.2 |              2.5 |                        1.6 |                           14.3 |                     0.073 |                        0.9 |                            3.3 |                       14.5 |                2.6 |                      0.679 |                        8.8 |                      0.575 |                  17.2 |               17.4 |                             1.4 |                       0.088 |        0 |
| 1128 |     2022 | Harrison Barnes       | SACRAMENTO KINGS    |    29 |        0.939024 |          33.5974 |  16.4286 |   2.41558 |                10.8312  |                 5.36364 |                            4.67532  | 0.181818 |              4.54545 |               1 |            5.07792 |            4.42857 |                      1.84416   |             1.06494  |          1.22078 | 0.688312 |     1.53247 |      0.468825 |      0.825666 | 0.394444 |                10.5 |                0.5 |              0.2 |                       -1.3 |                           14.9 |                     0.495 |                        1.5 |                            3.4 |                       15.7 |                1   |                      0.432 |                        9.1 |                      0.623 |                  10.4 |               18.8 |                             1.4 |                       0.112 |        0 |
| 1129 |     2022 | Scottie Barnes        | TORONTO RAPTORS     |    20 |        0.902439 |          35.3649 |  15.3243 |   3.45946 |                12.5946  |                 2.90541 |                            2.60811  | 0.743243 |              4.89189 |               1 |            6.2027  |            2.13514 |                      0.783784  |             2.63514  |          2.59459 | 1.08108  |     1.83784 |      0.492489 |      0.734884 | 0.300518 |                14.7 |                2.1 |              0.9 |                        0.4 |                           15.8 |                     0.231 |                        0.5 |                            7.7 |                       16.3 |                1.5 |                      0.207 |                       11.5 |                      0.552 |                  11.7 |               19   |                             1.9 |                       0.122 |        0 |
| 1130 |     2022 | RJ Barrett            | NEW YORK KNICKS     |    21 |        0.853659 |          34.5286 |  20.0286 |   2.97143 |                17.0571  |                 5.8     |                            5.77143  | 0.228571 |              4.88571 |               1 |            6.95714 |            4.14286 |                      1.97143   |             0.942857 |          2.02857 | 0.614286 |     2.15714 |      0.407873 |      0.714286 | 0.341584 |                14.9 |                0.7 |             -1.6 |                       -1.3 |                           15.5 |                     0.34  |                       -0.3 |                            2.9 |                       13.7 |                0.9 |                      0.338 |                        9.1 |                      0.511 |                   9.9 |               27.6 |                             0.2 |                       0.046 |        0 |  

* *This table include all the basic information and data of players for further analysis.  

 * Table 1 ----> [player_data.csv](https://github.com/tz1211/DS105L-Project-404-Not-Found/files/11592102/player_data.csv)


### Table 2: Count for MVP  
* *It count all the NBA MVP in the history, and also record who won the MVP a year past and two years past. This table is used for import to the machine learning algorithm for further analysis*  

 * Table 2 ----> [MVP_count.csv](https://github.com/tz1211/DS105L-Project-404-Not-Found/files/11583297/MVP_count.csv)


### :two: Sports News and Media Narratives

### Table 1: Quantified NBA Sports News - Sentiments and Relevance  
* *(Taking the 2019-2020 season from the merged table, the top 10 samples)*  

|    |   time | most_frequent_name   |   textblob_Sentiment |   nltk_Sentiment |   relevance_score |   bert_relevance |   credit_article |   credit_followers |   credit_tweets |   frequency |
|---:|-------:|:---------------------|---------------------:|-----------------:|------------------:|-----------------:|-----------------:|-------------------:|----------------:|------------:|
|  0 |   2020 | Aaron Gordon         |            0.0923111 |        0.0923111 |         0.131483  |         0.567671 |          39434.8 |            34372.6 |         40798   |           5 |
|  1 |   2020 | Al Horford           |            0.05169   |        0.05169   |         0.117488  |         0.54677  |          10781.7 |            34700.3 |         62255.7 |           3 |
|  2 |   2020 | Andre Drummond       |            0.0369387 |        0.0369387 |         0.158727  |         0.532269 |          15995.6 |            60639.6 |         67059.1 |          14 |
|  3 |   2020 | Andrew Wiggins       |            0.0904019 |        0.0904019 |         0.0992229 |         0.573194 |          28212.4 |            36785   |         42379.9 |           7 |
|  4 |   2020 | Anthony Davis        |            0.120779  |        0.120779  |         0.189062  |         0.548409 |          11444.1 |            47184.3 |         50480.3 |          27 |
|  5 |   2020 | Bam Adebayo          |            0.0589134 |        0.0589134 |         0.0640164 |         0.599966 |          21996   |            84859   |         93866   |           1 |
|  6 |   2020 | Ben Simmons          |            0.0598212 |        0.0598212 |         0.196928  |         0.552685 |          16923   |            65297.2 |         72214.3 |          13 |
|  7 |   2020 | Bradley Beal         |            0.0754871 |        0.0754871 |         0.102333  |         0.557063 |          11668.2 |            36245.4 |         45089   |          50 |
|  8 |   2020 | Brandon Ingram       |            0.0879199 |        0.0879199 |         0.0901602 |         0.544744 |          15613.1 |            50384.1 |         56001   |          27 |
|  9 |   2020 | Buddy Hield          |            0.0858989 |        0.0858989 |         0.0941537 |         0.554056 |          23624.3 |            49410.2 |         60888.5 |          26 |
| 10 |   2020 | CJ McCollum          |            0.0737269 |        0.0737269 |         0.276422  |         0.557982 |          14814.5 |            70731   |         70641.2 |           6 |

### Table 2: Quantified BBC Sports News - Sentiments and Relevance  
* *(Taking the 2012-2023 season from the merged table, the top 10 samples)* 








## 📈 Analysis
### 🧐 Qualitative Data Analysis - Part 1: NBA News

NBA news provides a wealth of relevant information about players' performances, team dynamics, injuries, and other factors that can influence MVP selection. Its coverage offers insights from expert analysts, journalists, and commentators who closely follow the league. These professionals often provide valuable perspectives and evaluations of players' performances. Further, NBA is characterized by constantly evolving strategies, player performances, and team dynamics throughout a season. NBA news stay updated with the latest developments and make informed analysis that align with the current landscape of the league. Therefore, NBA news provides an opportunity to discover hidden insights and correlations that might not be apparent through traditional statistical analysis alone. By incorporating unstructured textual data, the model can uncover nuanced relationships between players, teams, playing styles, and other factors that contribute to MVP performances.

Intuitively by leveraging this vast amount of data, the model can learn patterns and relationships that contribute to MVP prediction.


**❓🤔️ However, what are the potential problems** 

**1-** The accuracy and quality of the news can be influenced by the **knowledge, biases, and perspectives of authors**, which can ultimately impact the reliability of data. The experience and expertise of authors can vary significantly, ranging from seasoned sports journalists to inexperienced contributors or even fan-generated content. This variability introduces potential inconsistencies and biases in the reporting, analysis, and interpretation of player performances. 

**2-** Another factor to consider is the **sentiment expressed in the news articles**. NBA news encompasses a wide range of sources, including articles, interviews, social media posts, and press conferences. News coverage often includes subjective opinions, narratives, and emotional tones that can shape the perception of players' performances. Positive or negative sentiment towards a player can influence the overall portrayal and evaluation of their MVP candidacy. If the sentiment within the news data is imbalanced or biased towards certain players or teams, the model may inadvertently learn and amplify these biases, leading to skewed predictions.

**3-** Assessing the **relevance of the news articles** is crucial. Not all news articles will directly contribute to determining the MVP. Some articles may focus on off-court events, rumors, or unrelated topics, which may not provide valuable information for predicting MVP performances accurately. 

**To mitigate these concerns, NBA news are carefully assessed and quantifies into indexes.**


### :one: Credibility of NBA News
[Muck Rack](https://muckrack.com/)
 is a platform that provides insights into the credibility and influence of authors in journalism. 
By considering various metrics such as the number of followers, number of articles published, and number of tweets, Muck Rack can help define the credibility of authors and news:

- **Number of articles published**: 
The number of articles an author has published can provide insights into their experience and productivity. Authors who have consistently published a substantial number of articles may have a deeper understanding of their subject matter and possess a wealth of knowledge and expertise. It indicates their commitment to their profession and suggests they have been actively contributing to the industry.


- **Number of followers**: 
The number of followers an author has on Twitter can be an indicator of their reach and influence. Authors with a large number of followers often have a wider audience and may have established themselves as experts in their respective fields. 
Higher follower counts can suggest that the author's content resonates with readers and that they have built a reputation over time.


- **Number of tweets**: 
The number of tweets an author has shared on Twitter can give an indication of their engagement and activity level in the online community. Regularly posting tweets shows that the author actively participates in discussions, shares valuable insights, and keeps up with current events. 

#### Table: Preliminary Data of "credit_article", "credit_followers" and "credit_tweets" from Muck Rack
* *(Taking the sample from 2019-20 season). This sample is selected intentionally that contains all the cases for this part.* 

|    | title                                                                    |   time | author                               | credit_article   | credit_followers   | credit_tweets   | most_frequent_name    |
|---:|:-------------------------------------------------------------------------|-------:|:-------------------------------------|:-----------------|:-------------------|:----------------|:----------------------|
| 23 | LeBron James, Norman Powell Named Week 20 Players Of The Week            |   2020 | Official Release                     | Default          | Default            | Default         | Luka Dončić           |
| 24 | Power Rankings, Week 20: Lakers End Bucks’ 14-Week Run At Top            |   2020 | John Schuhmann                       | 890              | 84859              | 48341           | Giannis Antetokounmpo |
| 25 | 5 Can’t-Miss Matchups: James Harden vs. LeBron James                     |   2020 | Michael C. Wright                    | None             | None               | None            | James Harden          |
| 26 | 4 NBA Things To Know For 9 March                                         |   2020 | Jeff Case                            | 122              | 91                 | 42              | Giannis Antetokounmpo |
| 27 | Crowning LeBron: Will Lakers Take The Throne?                            |   2020 | Shaun Powell NBA.com               | 651              | None               | None            | Giannis Antetokounmpo |
| 28 | Raptors Top Kings Behind Starters’ 111 Total PTS                         |   2020 | NBA News                             | Default          | Default            | Default         | CJ McCollum           |
| 29 | Cavaliers Hang On To Outlast Spurs In Overtime, 132-129                  |   2020 | Tom Withers AP Sports Writer       | None             | None               | None            | DeMar DeRozan         |
| 30 | Knicks Pull Away In 4th Quarter, Beat Pistons 96-84                      |   2020 | Brian Mahoney AP Basketball Writer | 52               | None               | None            | Julius Randle         |

🧠 What are the **Issues and Challenges?**
- Some News are written anonymously, with the name of the press only.
- The website misses part of the information of a few authors. ie In the sample, Shaun Powell's number of articles published is gathered, but number of followers and tweets are missing.
- Some authors have different more multiple twitter accounts/usernames, which is protected and not accessible via real name only.
  - referred: [Twitter API](https://developer.twitter.com/en/docs/twitter-api)
  

**Inspired during the second presentation, the distribution of data can be used to select the value to replace missing parts.**
  - Statistical Imputation
- For news from "the press", "Official", they are assumed to be generally reliable, if not the most reliable. 
  - "Default" replaced by the 95 percentile from the distribution.

- For authors with part of or all missing data, choose mean, median or mode depending on the corresponding distribution.


#### Graphs: Distribution of Data:  "credit_article", "credit_followers" and "credit_tweets" from Muck Rack
* *(The distributions are used to determine a small number of missing values for few authors and the best number that represents "Default" for official and the press)*  

**Graph 1 Number of Articles**
  - The distribution is highly skewed, hence medium is used for missing values for authors.
![images - 2](https://github.com/tz1211/DS105L-Project-404-Not-Found/blob/main/Data/github_MDtable/article.png)

**Graph 2 Number of Followers **
  - The distribution is reasonably skewed, hence mean is used for missing values for authors.
![images - 3](https://github.com/tz1211/DS105L-Project-404-Not-Found/blob/main/Data/github_MDtable/follower.png)

**Graph 3 Number of Followers **
  - The distribution is reasonably skewed, hence mean is used for missing values for authors.
![images - 4](https://github.com/tz1211/DS105L-Project-404-Not-Found/blob/main/Data/github_MDtable/tweets.png)



### :two: Sentiment and Relevance of NBA News

For NBA News, there are four indexes that analyse the sentiments and relevance of news in addition to the three indicater for credibility.
They are "textblob_Sentiment", "nltk_Sentiment",	"bert_relevance" and "relevance_score". 

- **[NLTK](https://www.nltk.org/) and [TextBlob](https://pypi.org/project/textblob/) provide accessible and straightforward sentiment analysis capabilities. They are chosen for several reasons:**

    - **Availability of Pretrained Models**: NLTK and TextBlob come with default pretrained models for sentiment analysis, which can be suitable for basic sentiment classification tasks. These models have been trained on large corpora and can provide reasonable results for general sentiment analysis in NBA sports news without the need for extensive customization or fine-tuning.

    - **Focus on General Sentiment Analysis and Domain-Specific Lexicons** : NLTK and TextBlob are designed to provide general sentiment analysis capabilities. They provide sentiment analysis models that include domain-specific lexicons, which have been trained on a wide range of texts, including sports-related content. These lexicons contain words and phrases commonly used in NBA sports news, enabling them to capture sentiment nuances specific to the NBA and the sports domain more effectively.

    - **Performance on Informal Language** : NBA sports news sometimes contains informal language, slang, and sports-specific jargon. NLTK and TextBlob models are trained on diverse text sources, including social media and online forums, where informal language prevails. They can better handle and interpret the informal language commonly found in NBA sports news, leading to more accurate sentiment analysis results.

    - **Interpretability for Analysts** : NLTK and TextBlob sentiment analysis models often rely on simple rule-based approaches, making the process more interpretable. It is easy to explain how sentiments are determined based on the presence of positive or negative words in the text. This transparency can be valuable for NBA sports analysts when presenting sentiment analysis results to stakeholders or discussing the sentiment trends in the NBA.

- **BERT relevance is useful for sports news analysis due to the following reasons:**

    - **Contextual Understanding**: BERT (Bidirectional Encoder Representations from Transformers) is a powerful language model that utilizes a deep neural network architecture. It can capture the contextual understanding of words and phrases within a sentence or document. In sports news analysis, where context plays a crucial role, BERT can effectively grasp the relationships between different terms, player names, team names, and game events. This contextual understanding enhances the relevance assessment of sports news articles.

    - **Handling Ambiguity** : Sports news often contains ambiguous references, such as player names that can be shared by multiple athletes or events with similar descriptions. BERT's contextual understanding helps disambiguate such references by considering the surrounding context. It can distinguish between different players with the same name or identify specific events within a broader context, leading to more precise relevance scoring.  


- **In addition to BERT relevance, another definition is also used to assess to what extent is the news related to the topic that we care, who will be the MVP?**
   - [Relevance_code](https://github.com/tz1211/DS105L-Project-404-Not-Found/blob/main/Data/github_MDtable/relevance_code.ipynb)
   - The code analyzes the relevance of sports news articles to a specific statement regarding a player being the MVP. 
   - Both the content and the statement ("player_name + 'will be the MVP'") are preprocessed using the preprocess_text() function. This step involves text cleaning, lowercasing, removing stopwords, and any other necessary transformations to prepare the text for analysis.
   - The code uses the TfidfVectorizer() from scikit-learn to convert the preprocessed content and statement into numerical feature vectors based on their term frequencies and inverse document frequencies (TF-IDF). This vectorization approach assigns higher weights to terms that are more important in a specific document (the news content) or the overall corpus (the statement).
  - The TF-IDF vectors for the content and statement are passed to the cosine_similarity() function to calculate the cosine similarity score. Cosine similarity measures the similarity between two vectors by considering the angle between them. A higher score indicates a higher degree of similarity.
  - The similarity score is divided by the sum of the TF-IDF vector for the content (tfidf_matrix[0].sum()) to normalize it to a range between 0 and 1. Normalization allows for better comparison and interpretation of relevance scores across different articles.

   **It also suits sports news analysis and provide an additional perspective regarding relevance**. 
   - By representing the content and statement as TF-IDF vectors, the code captures the importance of specific terms within the sports news articles and the statement. This approach is particularly useful in sports news analysis, as it allows the identification of relevant articles based on the significance of terms related to players, game events, team dynamics, and other sports-specific information.
   - Utilizing cosine similarity helps measure the similarity between the content and statement vectors, providing a quantitative measure of how closely the news article aligns with the MVP statement. This similarity score reflects the relevance of the article to the MVP prediction and enables ranking or filtering of articles based on their relevance.
   - Normalizing the similarity scores ensures a consistent range of values between 0 and 1, facilitating easier interpretation and comparison of relevance scores. This normalization enables ranking articles based on their relevance scores and assists in distinguishing highly relevant articles from less relevant ones in the sports news analysis.

**How does the data look like 🤔️ **
#### Table: Sample Final Data of NBA NEWS
* *(Taking the sample from 2019-20 season). * 

|    |   time | most_frequent_name      |   textblob_Sentiment |   nltk_Sentiment |   relevance_score |   bert_relevance |   credit_article |   credit_followers |   credit_tweets |   frequency |
|---:|-------:|:------------------------|---------------------:|-----------------:|------------------:|-----------------:|-----------------:|-------------------:|----------------:|------------:|
|  0 |   2020 | Aaron Gordon            |           0.0923111  |       0.0923111  |         0.131483  |         0.567671 |         39434.8  |           34372.6  |         40798   |           5 |
|  1 |   2020 | Al Horford              |           0.05169    |       0.05169    |         0.117488  |         0.54677  |         10781.7  |           34700.3  |         62255.7 |           3 |
|  2 |   2020 | Andre Drummond          |           0.0369387  |       0.0369387  |         0.158727  |         0.532269 |         15995.6  |           60639.6  |         67059.1 |          14 |
|  3 |   2020 | Andrew Wiggins          |           0.0904019  |       0.0904019  |         0.0992229 |         0.573194 |         28212.4  |           36785    |         42379.9 |           7 |
|  4 |   2020 | Anthony Davis           |           0.120779   |       0.120779   |         0.189062  |         0.548409 |         11444.1  |           47184.3  |         50480.3 |          27 |



## 🖼️ Results

## 🖋️ Conclusions

## 📚 References

* [markdown file editting instruction](https://markdown.com.cn/cheat-sheet.html#%E6%80%BB%E8%A7%88)
* [Basketball reference api use instruction](https://jaebradley.github.io/basketball_reference_web_scraper/api/ )
