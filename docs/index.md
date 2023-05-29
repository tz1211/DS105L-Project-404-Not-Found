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

# 📝 Project Description   

Are you curious about who will be crowned the next NBA MVP? Our MVP prediction website has got you covered! Get ready for an exciting journey where we dive into the world of elite basketball performance and statistical analysis to forecast the NBA's most valuable player.  

With the NBA showcasing the pinnacle of basketball talent, predicting the MVP award is a thrilling challenge. We crunch the numbers, analyze player statistics, and examine historical trends to make insightful predictions. Our goal is to uncover the standout players who have the potential to rise above the competition and leave a lasting impact on the game.

Whether you are a die-hard basketball enthusiast or just starting to explore the world of NBA MVP predictions, our user-friendly website is designed to make the experience enjoyable for everyone. So come on board and embark on this thrilling journey with us as we try to unravel the captivating mystery of the next NBA MVP!  

![images - 1](https://github.com/tz1211/DS105L-Project-404-Not-Found/assets/114760508/4443b36e-3b28-4343-b327-a999105f7581)

Data Source: 
* [Basketball Reference](https://www.basketball-reference.com/)  
* [NBA Official Website](skysports.com/nba)  
* [ESPN Sports](espn.com/nba)   
* [NBA News Archive](https://global.nba.com/news)
* [BBC Sports News](https://www.bbc.co.uk/sport) 
* [Muck Rack](https://muckrack.com/)


# 📊 Data

## PROCEDURE MAP

<img width="2378" alt="Group Report: 404-not-found" src="https://github.com/tz1211/DS105L-Project-404-Not-Found/assets/114760508/7058c6c0-c454-4bd2-bbf5-8c515871542b">

## Approach 

Converntional basketball wisdom dictates that the MVP award is traditionally determined by 3 aspects: 
* **Individual performance** (How good is the player?) 
  * Includes basic boxscore (e.g. points per game, assists per game) as well as advanced player metrics such as win share per 48, value over replacement player, player efficiency rating, etc. 
* **Team performance** (Can the player carry a winning team?)
  * Includes the team's win percentage and conference standing 
* **Media narrative** (Is there a strong story behind a player's MVP bid?) 
  * Includes aspects such as voter fatigue (people don't like to award MVP to the same player over and over again), intriguing story for winning MVP (e.g. youngest MVP ever), and amount of media attention a player is getting. 

Usually, the MVP award goes to players who are high on both individual performance and team performance (i.e. "best player on the best team"). However, media narratives and factors such as voter fatigue plays a big role sometimes in determining the ultimate winner of the award (e.g. Derrick Rose won the MVP award in 2011 as the youngest ever MVP winner even though many people believed that Lebron James had a more impressive season statistically). 

Therefore, in this section, we will be collecting and showing data that aim to capture these 3 aspects respectively. 

### :one: Quantitative Data (Individual performance + Team performance) 

<details>
<summary><strong>Individual Player Data</strong> (<a href="https://github.com/tz1211/DS105L-Project-404-Not-Found/blob/main/Data/player_data.csv">player_data.csv</a>)</summary>  
 

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
 

* *This table include boxscore and advanced statistics that reflects players' individual performances. (Source: [Basketball Reference](https://www.basketball-reference.com/))
</details>

<details>
<summary><strong>Team Data</strong> (<a href="https://github.com/tz1211/DS105L-Project-404-Not-Found/blob/main/Data/team_data.csv">team_data.csv</a>)</summary>  
 

|      |season|team     |conference           |W                  |L  |win_rate          |conference_standing|
|------|------|---------|---------------------|-------------------|---|------------------|-------------------|
|30    |2022  |PHOENIX SUNS|Western              |64                 |18 |0.7804878048780488|1                  |
|31    |2022  |MEMPHIS GRIZZLIES|Western              |56                 |26 |0.6829268292682927|2                  |
|32    |2022  |GOLDEN STATE WARRIORS|Western              |53                 |29 |0.6463414634146342|3                  |
|33    |2022  |DALLAS MAVERICKS|Western              |52                 |30 |0.6341463414634146|4                  |
|34    |2022  |UTAH JAZZ|Western              |49                 |33 |0.5975609756097561|5                  |
|35    |2022  |DENVER NUGGETS|Western              |48                 |34 |0.5853658536585366|6                  |
|36    |2022  |MINNESOTA TIMBERWOLVES|Western              |46                 |36 |0.5609756097560976|7                  |
|37    |2022  |LOS ANGELES CLIPPERS|Western              |42                 |40 |0.5121951219512195|8                  |
|38    |2022  |NEW ORLEANS PELICANS|Western              |36                 |46 |0.4390243902439024|9                  |
|39    |2022  |SAN ANTONIO SPURS|Western              |34                 |48 |0.4146341463414634|10                 |
|40    |2022  |LOS ANGELES LAKERS|Western              |33                 |49 |0.4024390243902439|11                 |
|41    |2022  |SACRAMENTO KINGS|Western              |30                 |52 |0.3658536585365853|12                 |
|42    |2022  |PORTLAND TRAIL BLAZERS|Western              |27                 |55 |0.3292682926829268|13                 |
|43    |2022  |OKLAHOMA CITY THUNDER|Western              |24                 |58 |0.2926829268292683|14                 |
|44    |2022  |HOUSTON ROCKETS|Western              |20                 |62 |0.2439024390243902|15                 |
|45    |2022  |MIAMI HEAT|Eastern              |53                 |29 |0.6463414634146342|1                  |
|46    |2022  |BOSTON CELTICS|Eastern              |51                 |31 |0.6219512195121951|2                  |
|47    |2022  |MILWAUKEE BUCKS|Eastern              |51                 |31 |0.6219512195121951|3                  |
|48    |2022  |PHILADELPHIA 76ERS|Eastern              |51                 |31 |0.6219512195121951|4                  |
|49    |2022  |TORONTO RAPTORS|Eastern              |48                 |34 |0.5853658536585366|5                  |
|50    |2022  |CHICAGO BULLS|Eastern              |46                 |36 |0.5609756097560976|6                  |
|51    |2022  |BROOKLYN NETS|Eastern              |44                 |38 |0.5365853658536586|7                  |
|52    |2022  |CLEVELAND CAVALIERS|Eastern              |44                 |38 |0.5365853658536586|8                  |
|53    |2022  |ATLANTA HAWKS|Eastern              |43                 |39 |0.524390243902439 |9                  |
|54    |2022  |CHARLOTTE HORNETS|Eastern              |43                 |39 |0.524390243902439 |10                 |
|55    |2022  |NEW YORK KNICKS|Eastern              |37                 |45 |0.4512195121951219|11                 |
|56    |2022  |WASHINGTON WIZARDS|Eastern              |35                 |47 |0.4268292682926829|12                 |
|57    |2022  |INDIANA PACERS|Eastern              |25                 |57 |0.3048780487804878|13                 |
|58    |2022  |DETROIT PISTONS|Eastern              |23                 |59 |0.2804878048780488|14                 |
|59    |2022  |ORLANDO MAGIC|Eastern              |22                 |60 |0.2682926829268293|15                 |  
 
 

* *This table includes the win percentage and conference standing for each team. (Source: [Basketball Reference](https://www.basketball-reference.com/))
</details>

### :two: Qualitative Data (Sports News and Media Narratives)

<details>
<summary><strong>Quantified NBA Sports News - Sentiments and Relevance</strong></summary>
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
</details>

<details>
<summary><strong>Quantified BBC Sports News - Sentiments and Relevance</strong></summary>
* *(Taking the 2010-2023 season from the merged table, the top 10 samples)* 
 
|    |   time | most_frequent_name      |   textblob_sentiment |   sentiment_bert_average_score |   sentiment_xlnet_average_score |   bert_relevance |   relevance_score |   frequency |
|---:|-------:|:------------------------|---------------------:|-------------------------------:|--------------------------------:|-----------------:|------------------:|------------:|
|  0 |   2023 | Aaron Gordon            |            0.107826  |                       0.580768 |                        0.569642 |         0.592284 |        0.00804037 |          22 |
|  1 |   2023 | Al Horford              |            0.0902433 |                       0.560702 |                        0.602442 |         0.588029 |        0.00175832 |           2 |
|  2 |   2023 | Andrew Wiggins          |            0.141368  |                       0.597014 |                        0.580687 |         0.587998 |        0.0106417  |           8 |
|  3 |   2023 | Anfernee Simons         |            0.109778  |                       0.557983 |                        0.569789 |         0.593048 |        0.0138669  |           2 |
|  4 |   2023 | Anthony Davis           |            0.102784  |                       0.592395 |                        0.570054 |         0.587705 |        0.0162172  |          22 |
|  5 |   2023 | Anthony Edwards         |            0.0561825 |                       0.602159 |                        0.6101   |         0.590135 |        0.0545278  |          14 |
|  6 |   2023 | Bam Adebayo             |            0.192308  |                       0.513591 |                        0.590492 |         0.597262 |        0.00980593 |           1 |
|  7 |   2023 | Bojan Bogdanović        |            0.138098  |                       0.577742 |                        0.575943 |         0.59157  |        0.00184185 |           2 |
|  8 |   2023 | Bradley Beal            |            0.122245  |                       0.584892 |                        0.581959 |         0.58885  |        0.0030606  |           1 |
|  9 |   2023 | Brandon Ingram          |            0.0912451 |                       0.608591 |                        0.591863 |         0.576785 |        0.00785333 |           5 |
</details>

<details>
<summary><strong>MVP Count</strong> (<a href="https://github.com/tz1211/DS105L-Project-404-Not-Found/blob/main/Data/final_cleaned_data/MVP_count.csv">MVP_count.csv</a>)</summary>
Sample MVP count for Stephen Curry 

|Name         |Year|value|won_last_yr|won_2_yrs_before|
|-------------|----|-----|-----------|----------------|
|Stephen Curry|2023|2    |0          |0               |
|Stephen Curry|2022|2    |0          |0               |
|Stephen Curry|2021|2    |0          |0               |
|Stephen Curry|2020|2    |0          |0               |
|Stephen Curry|2019|2    |0          |0               |
|Stephen Curry|2018|2    |0          |1               |
|Stephen Curry|2017|2    |1          |1               |
|Stephen Curry|2016|1    |1          |0               |
|Stephen Curry|2015|0    |0          |0               |
|Stephen Curry|2014|0    |0          |0               |
|Stephen Curry|2013|0    |0          |0               |
|Stephen Curry|2012|0    |0          |0               |
|Stephen Curry|2011|0    |0          |0               |
|Stephen Curry|2010|0    |0          |0               |
|Stephen Curry|2009|0    |0          |0               |
|Stephen Curry|2008|0    |0          |0               |
 * `MVP_count.csv` is designed to capture the number of time a player have won MVP and whether he has won it the previous year or previous 2 years. It is generally agreed upon that players who win their first MVP the previous year tend to win another MVP, whilst players who have won MVP 2 years in a row are highly unlikely to win a third one (sometimes termed "voter fatigue"). This dataset is designed to capture the aspect of "voter fatigue". 
</details>

## Final Merged Data 

### Historical data from 2010-2022 season ([final_cleaned_data.csv](https://github.com/tz1211/DS105L-Project-404-Not-Found/blob/main/Data/final_cleaned_data.csv)) 

|      |season|slug     |name             |team                  |age|%games_played     |minutes_played    |points            |assists           |attempted_field_goals|attempted_free_throws|attempted_three_point_field_goals|blocks            |defensive_rebounds|games_started     |made_field_goals  |made_free_throws  |made_three_point_field_goals|offensive_rebounds|personal_fouls    |steals            |turnovers         |field_goal%       |free_throw%       |3pt%              |assist_percentage|block_percentage|box_plus_minus|defensive_box_plus_minus|defensive_rebound_percentage|free_throw_attempt_rate|offensive_box_plus_minus|offensive_rebound_percentage|player_efficiency_rating|steal_percentage|three_point_attempt_rate|total_rebound_percentage|true_shooting_percentage|turnover_percentage|usage_percentage|value_over_replacement_player|win_shares_per_48_minutes|win_rate          |conference_standing|num_mvp|won_last_yr|won_2_yrs_before|textblob_sentiment|sentiment_bert_average_score|sentiment_xlnet_average_score|bert_relevance    |relevance_score   |frequency|is_mvp|
|------|------|---------|-----------------|----------------------|---|------------------|------------------|------------------|------------------|---------------------|---------------------|---------------------------------|------------------|------------------|------------------|------------------|------------------|----------------------------|------------------|------------------|------------------|------------------|------------------|------------------|------------------|-----------------|----------------|--------------|------------------------|----------------------------|-----------------------|------------------------|----------------------------|------------------------|----------------|------------------------|------------------------|------------------------|-------------------|----------------|-----------------------------|-------------------------|------------------|-------------------|-------|-----------|----------------|------------------|----------------------------|-----------------------------|------------------|------------------|---------|------|
|0     |2010  |aldrila01|LaMarcus Aldridge|PORTLAND TRAIL BLAZERS|24 |0.951219512195122 |37.46153846153846 |17.858974358974358|2.051282051282051 |14.987179487179487   |3.897435897435898    |0.2051282051282051               |0.6153846153846154|5.576923076923077 |1.0               |7.423076923076923 |2.948717948717949 |0.0641025641025641          |2.4615384615384617|2.9615384615384617|0.8589743589743589|1.3333333333333333|0.495295124037639 |0.7565789473684211|0.3125            |9.9              |1.3             |1.2           |-0.2                    |18.6                        |0.26                   |1.4                     |8.1                         |18.2                    |1.3             |0.014                   |13.3                    |0.535                   |7.4                |22.9            |2.3                          |0.145                    |0.6097560975609756|6                  |0      |0          |0               |0.0               |0.0                         |0.0                          |0.0               |0.0               |0        |0     |
|1     |2010  |allenra02|Ray Allen        |BOSTON CELTICS        |34 |0.975609756097561 |35.2375           |16.3              |2.625             |12.1625              |3.1625               |4.9875                           |0.3125            |2.6               |1.0               |5.8               |2.8875            |1.8125                      |0.5625            |2.275             |0.8               |1.6125            |0.4768756423432682|0.9130434782608696|0.3634085213032582|12.3             |0.7             |1.2           |-0.3                    |8.8                         |0.26                   |1.5                     |2.0                         |15.2                    |1.2             |0.41                    |5.5                     |0.601                   |10.6               |20.2            |2.3                          |0.135                    |0.6097560975609756|4                  |0      |0          |0               |0.046541415714644 |0.5710958358314302          |0.5737237615717782           |0.5190211534500122|0.0038996330971015|4        |0     |
|2     |2010  |anthoca01|Carmelo Anthony  |DENVER NUGGETS        |25 |0.8414634146341463|38.17391304347826 |28.159420289855078|3.217391304347826 |21.768115942028984   |8.869565217391305    |2.710144927536232                |0.4347826086956521|4.376811594202898 |1.0               |9.971014492753625 |7.36231884057971  |0.855072463768116           |2.2028985507246377|3.260869565217391 |1.2753623188405796|3.028985507246377 |0.4580559254327563|0.8300653594771241|0.3155080213903743|15.9             |0.9             |2.3           |-1.2                    |13.1                        |0.407                  |3.5                     |6.7                         |22.2                    |1.7             |0.125                   |9.9                     |0.548                   |10.6               |33.4            |2.9                          |0.145                    |0.6463414634146342|4                  |0      |0          |0               |0.0659319821592549|0.5807402985436576          |0.576524725982121            |0.531563937664032 |0.0585006792499055|5        |0     |
|3     |2010  |arenagi01|Gilbert Arenas   |WASHINGTON WIZARDS    |28 |0.3902439024390244|36.53125          |22.5625           |7.1875            |19.25                |6.46875              |5.65625                          |0.28125           |3.625             |1.0               |7.90625           |4.78125           |1.96875                     |0.53125           |2.96875           |1.28125           |3.65625           |0.4107142857142857|0.7391304347826086|0.3480662983425414|36.3             |0.6             |1.7           |-1.2                    |11.6                        |0.336                  |2.9                     |1.6                         |18.7                    |1.8             |0.294                   |6.5                     |0.511                   |14.2               |31.9            |1.1                          |0.072                    |0.3170731707317073|14                 |0      |0          |0               |0.132288557912325 |0.6023474167263697          |0.5754024456890803           |0.523616373538971 |0.0043846670048157|6        |0     |
|4     |2010  |arizatr01|Trevor Ariza     |HOUSTON ROCKETS       |24 |0.8780487804878049|36.513888888888886|14.88888888888889 |3.8333333333333335|13.875               |3.1666666666666665   |5.652777777777778                |0.5555555555555556|4.513888888888889 |0.9861111111111112|5.472222222222222 |2.055555555555556 |1.8888888888888888          |1.0833333333333333|2.25              |1.75              |2.236111111111111 |0.3943943943943944|0.6491228070175439|0.3341523341523341|16.7             |1.1             |0.5           |0.9                     |14.7                        |0.228                  |-0.4                    |3.3                         |13.3                    |2.4             |0.407                   |8.8                     |0.488                   |12.8               |21.2            |1.7                          |0.058                    |0.5121951219512195|9                  |0      |0          |0               |0.0               |0.0                         |0.0                          |0.0               |0.0               |0        |0     |
|5     |2010  |artesro01|Metta World Peace|LOS ANGELES LAKERS    |30 |0.9390243902439024|33.83116883116883 |10.974025974025974|3.038961038961039 |9.61038961038961     |2.415584415584416    |3.844155844155844                |0.2727272727272727|3.012987012987013 |1.0               |3.9740259740259742|1.6623376623376624|1.3636363636363635          |1.2857142857142858|2.142857142857143 |1.3766233766233766|1.5714285714285714|0.4135135135135135|0.6881720430107527|0.3547297297297297|13.3             |0.6             |0.5           |1.1                     |9.9                         |0.251                  |-0.6                    |4.3                         |12.1                    |2.1             |0.4                     |7.1                     |0.514                   |12.8               |16.2            |1.6                          |0.098                    |0.6951219512195121|1                  |0      |0          |0               |0.0               |0.0                         |0.0                          |0.0               |0.0               |0        |0     |
|6     |2010  |bargnan01|Andrea Bargnani  |TORONTO RAPTORS       |24 |0.975609756097561 |34.9875           |17.2              |1.1625            |14.2875              |2.925                |4.0625                           |1.3875            |4.85              |1.0               |6.7125            |2.2625            |1.5125                      |1.3125            |2.6875            |0.3125            |1.5               |0.4698162729658793|0.7735042735042736|0.3723076923076923|5.4              |3.0             |-0.8          |-1.7                    |15.9                        |0.205                  |0.9                     |4.6                         |15.5                    |0.5             |0.284                   |10.4                    |0.552                   |8.8                |22.3            |0.9                          |0.072                    |0.4878048780487805|9                  |0      |0          |0               |0.2366198865733748|0.5677419097527213          |0.5666976000951685           |0.5314929485321045|0.0018285459338642|1        |0     |
|7     |2010  |barroea01|Earl Barron      |NEW YORK KNICKS       |28 |0.0853658536585365|33.142857142857146|11.714285714285714|1.1428571428571428|9.714285714285714    |4.142857142857143    |0.0                              |0.5714285714285714|6.571428571428571 |0.8571428571428571|4.285714285714286 |3.142857142857143 |0.0                         |4.428571428571429 |3.4285714285714284|0.5714285714285714|1.5714285714285714|0.4411764705882353|0.7586206896551724|0.0               |5.2              |1.3             |-4.5          |-2.9                    |22.9                        |0.426                  |-1.5                    |14.9                        |14.7                    |0.9             |0.0                     |18.9                    |0.508                   |12.0               |17.9            |-0.1                         |0.091                    |0.3536585365853658|11                 |0      |0          |0               |0.2366198865733748|0.5935538048329561          |0.5683303993681202           |0.513433039188385 |0.0018285459338642|1        |0     |
|8     |2010  |battish01|Shane Battier    |HOUSTON ROCKETS       |31 |0.8170731707317073|32.35820895522388 |7.970149253731344 |2.4477611940298507|6.6716417910447765   |1.582089552238806    |4.164179104477612                |1.1343283582089552|3.5522388059701493|0.9253731343283582|2.656716417910448 |1.1492537313432836|1.507462686567164           |1.1044776119402986|2.074626865671642 |0.7910447761194029|0.9552238805970148|0.3982102908277405|0.7264150943396227|0.3620071684587813|10.9             |2.6             |1.5           |1.4                     |13.1                        |0.237                  |0.1                     |3.8                         |11.1                    |1.2             |0.624                   |8.2                     |0.541                   |11.5               |11.4            |1.9                          |0.095                    |0.5121951219512195|9                  |0      |0          |0               |0.0               |0.0                         |0.0                          |0.0               |0.0               |0        |0     |
|9     |2010  |bellra01 |Raja Bell        |CHARLOTTE BOBCATS     |33 |0.0609756097560975|31.4              |12.0              |2.0               |11.0                 |0.6                  |4.8                              |0.4               |3.2               |1.0               |4.8               |0.6               |1.8                         |1.0               |2.6               |0.8               |1.0               |0.4363636363636363|1.0               |0.375             |11.3             |1.0             |2.5           |2.0                     |12.1                        |0.055                  |0.5                     |3.9                         |12.8                    |1.4             |0.436                   |8.1                     |0.533                   |8.2                |18.2            |0.2                          |0.113                    |0.5365853658536586|7                  |0      |0          |0               |0.2366198865733748|0.5702846050262451          |0.5683994526448457           |0.5285742878913879|0.0018285459338642|1        |0     |

Full df shape: 1216 x 54
* Final dataframe with individual, team, and media narrative data all merged together 
* Used as training set for the Machine Learning algorithm (with column `is_mvp` acting as the label) 

### Merged data for 2023 season ([final_cleaned_data_2023.csv](https://github.com/tz1211/DS105L-Project-404-Not-Found/blob/main/Data/final_cleaned_data_2023.csv)) 

|      |season|slug     |name             |team                  |age|%games_played     |minutes_played    |points            |assists           |attempted_field_goals|attempted_free_throws|attempted_three_point_field_goals|blocks            |defensive_rebounds|games_started     |made_field_goals  |made_free_throws  |made_three_point_field_goals|offensive_rebounds|personal_fouls    |steals            |turnovers         |field_goal%       |free_throw%       |3pt%              |assist_percentage|block_percentage|box_plus_minus|defensive_box_plus_minus|defensive_rebound_percentage|free_throw_attempt_rate|offensive_box_plus_minus|offensive_rebound_percentage|player_efficiency_rating|steal_percentage|three_point_attempt_rate|total_rebound_percentage|true_shooting_percentage|turnover_percentage|usage_percentage|value_over_replacement_player|win_shares_per_48_minutes|win_rate          |conference_standing|num_mvp|won_last_yr|won_2_yrs_before|textblob_sentiment|sentiment_bert_average_score|sentiment_xlnet_average_score|bert_relevance    |relevance_score   |frequency|
|------|------|---------|-----------------|----------------------|---|------------------|------------------|------------------|------------------|---------------------|---------------------|---------------------------------|------------------|------------------|------------------|------------------|------------------|----------------------------|------------------|------------------|------------------|------------------|------------------|------------------|------------------|-----------------|----------------|--------------|------------------------|----------------------------|-----------------------|------------------------|----------------------------|------------------------|----------------|------------------------|------------------------|------------------------|-------------------|----------------|-----------------------------|-------------------------|------------------|-------------------|-------|-----------|----------------|------------------|----------------------------|-----------------------------|------------------|------------------|---------|
|0     |2023  |adebaba01|Bam Adebayo      |MIAMI HEAT            |25 |0.918918918918919 |35.13235294117647 |21.058823529411764|3.2794117647058822|15.25                |5.588235294117647    |0.1764705882352941               |0.8676470588235294|6.926470588235294 |1.0               |8.279411764705882 |4.485294117647059 |0.0147058823529411          |2.426470588235294 |2.867647058823529 |1.1911764705882353|2.588235294117647 |0.5429122468659595|0.8026315789473685|0.0833333333333333|16.4             |2.5             |1.8           |0.9                     |23.9                        |0.366                  |0.9                     |7.8                         |20.4                    |1.7             |0.012                   |15.5                    |0.595                   |12.8               |25.5            |2.3                          |0.142                    |0.5342465753424658|7                  |0      |0          |0               |0.1923076923076923|0.5135908424854279          |0.5904920101165771           |0.5972620844841003|0.00980592516144  |1        |
|1     |2023  |allenja01|Jarrett Allen    |CLEVELAND CAVALIERS   |24 |0.8378378378378378|33.03225806451613 |14.35483870967742 |1.6774193548387095|9.225806451612904    |3.2580645161290325   |0.1451612903225806               |1.2096774193548387|6.693548387096774 |1.0               |5.983870967741935 |2.370967741935484 |0.0161290322580645          |3.1129032258064515|2.2419354838709675|0.8225806451612904|1.403225806451613 |0.6486013986013985|0.7277227722772277|0.1111111111111111|7.5              |3.4             |2.3           |1.1                     |23.9                        |0.353                  |1.3                     |11.1                        |19.8                    |1.3             |0.016                   |17.5                    |0.673                   |11.6               |16.3            |2.2                          |0.204                    |0.6164383561643836|4                  |0      |0          |0               |0.1528338695853003|0.6097304433025151          |0.5730694161542568           |0.5885380506515503|0.0065960140888307|7        |
|2     |2023  |antetgi01|Giannis Antetokounmpo|MILWAUKEE BUCKS       |28 |0.7777777777777778|32.5              |31.25             |5.571428571428571 |20.392857142857142   |12.625               |2.7857142857142856               |0.8035714285714286|9.607142857142858 |1.0               |11.125            |8.196428571428571 |0.8035714285714286          |2.25              |3.196428571428572 |0.7321428571428571|3.9107142857142856|0.5455341506129597|0.6492220650636492|0.2884615384615385|32.3             |2.0             |8.2           |2.6                     |29.5                        |0.619                  |5.6                     |7.5                         |28.6                    |1.1             |0.137                   |18.9                    |0.602                   |13.1               |38.7            |4.7                          |0.204                    |0.7183098591549296|1                  |2      |0          |0               |0.1511246958443137|0.5856197835898947          |0.5833562986432821           |0.5941260457038879|0.0251025381228857|29       |
|3     |2023  |anunoog01|OG Anunoby       |TORONTO RAPTORS       |25 |0.7945205479452054|35.724137931034484|16.775862068965516|1.896551724137931 |13.10344827586207    |2.7413793103448274   |5.258620689655173                |0.7241379310344828|3.655172413793104 |1.0               |6.224137931034483 |2.293103448275862 |2.034482758620689           |1.4137931034482758|3.034482758620689 |1.9655172413793105|2.155172413793104 |0.475             |0.8364779874213837|0.3868852459016393|7.7              |2.0             |0.1           |0.7                     |12.5                        |0.209                  |-0.6                    |4.2                         |14.4                    |2.7             |0.401                   |8.0                     |0.586                   |13.1               |19.6            |1.1                          |0.085                    |0.4861111111111111|9                  |0      |0          |0               |0.0               |0.0                         |0.0                          |0.0               |0.0               |0        |
|4     |2023  |aytonde01|Deandre Ayton    |PHOENIX SUNS          |24 |0.8472222222222222|30.442622950819672|18.311475409836067|1.819672131147541 |13.557377049180328   |2.9672131147540983   |0.3934426229508196               |0.7704918032786885|7.508196721311475 |1.0               |7.983606557377049 |2.2295081967213117|0.1147540983606557          |2.639344262295082 |2.836065573770492 |0.5573770491803278|1.819672131147541 |0.5888754534461911|0.7513812154696132|0.2916666666666667|9.8              |2.3             |1.1           |-0.1                    |28.0                        |0.219                  |1.2                     |9.5                         |20.3                    |0.9             |0.029                   |18.5                    |0.616                   |10.9               |23.4            |1.5                          |0.15                     |0.5352112676056338|4                  |0      |0          |0               |0.1912495627268354|0.5799142109023201          |0.5558537509706286           |0.5947425961494446|0.0145873656148506|3        |
|5     |2023  |ballla01 |LaMelo Ball      |CHARLOTTE HORNETS     |21 |0.4931506849315068|35.22222222222222 |23.27777777777778 |8.444444444444445 |20.02777777777778    |3.388888888888889    |10.63888888888889                |0.3055555555555556|5.25              |1.0               |8.222222222222221 |2.833333333333333 |4.0                         |1.1666666666666667|3.2777777777777777|1.2777777777777777|3.583333333333333 |0.4105409153952842|0.8360655737704918|0.3759791122715404|38.5             |0.8             |2.3           |-0.9                    |16.3                        |0.169                  |3.2                     |3.4                         |18.0                    |1.7             |0.531                   |9.7                     |0.541                   |14.3               |29.9            |1.4                          |0.07                     |0.3055555555555556|14                 |0      |0          |0               |0.1414080785448697|0.5672962308853059          |0.5853009911068591           |0.57403165102005  |0.0066773602960005|14       |
|6     |2023  |banchpa01|Paolo Banchero   |ORLANDO MAGIC         |20 |0.8904109589041096|33.84615384615385 |19.984615384615385|3.615384615384616 |15.738461538461538   |7.4                  |4.030769230769231                |0.5076923076923077|5.507692307692308 |1.0               |6.676923076923077 |5.492307692307692 |1.1384615384615384          |1.123076923076923 |2.246153846153846 |0.8615384615384616|2.7384615384615385|0.4242424242424242|0.7422037422037422|0.282442748091603 |16.6             |1.4             |-1.8          |-0.9                    |18.6                        |0.47                   |-0.9                    |3.7                         |14.7                    |1.2             |0.256                   |11.1                    |0.526                   |12.6               |27.6            |0.1                          |0.041                    |0.4027777777777778|13                 |0      |0          |0               |0.2453216374269005|0.5700385173161825          |0.5779234568277994           |0.5979455709457397|0.0147364798689941|1        |
|7     |2023  |banede01 |Desmond Bane     |MEMPHIS GRIZZLIES     |24 |0.6805555555555556|31.306122448979597|21.081632653061224|4.224489795918367 |16.142857142857142   |3.5510204081632653   |6.959183673469388                |0.3877551020408163|4.387755102040816 |1.0               |7.571428571428571 |3.142857142857143 |2.795918367346939           |0.7142857142857143|2.489795918367347 |0.9387755102040816|2.204081632653061 |0.4690265486725664|0.8850574712643678|0.4017595307917889|20.5             |1.1             |3.2           |0.2                     |14.8                        |0.22                   |3.0                     |2.4                         |18.7                    |1.4             |0.431                   |8.6                     |0.595                   |11.1               |26.3            |2.0                          |0.145                    |0.6142857142857143|2                  |0      |0          |0               |0.2637310606060606|0.5798526207605997          |0.5645423928896586           |0.5514346957206726|0.0135044907831952|1        |
|8     |2023  |barneha02|Harrison Barnes  |SACRAMENTO KINGS      |30 |0.9861111111111112|32.816901408450704|14.985915492957746|1.591549295774648 |9.661971830985916    |5.0                  |4.422535211267606                |0.1408450704225352|3.704225352112676 |1.0               |4.549295774647887 |4.23943661971831  |1.647887323943662           |0.971830985915493 |1.3380281690140845|0.676056338028169 |1.0845070422535212|0.4708454810495626|0.847887323943662 |0.3726114649681528|6.4              |0.4             |-1.0          |-1.5                    |12.8                        |0.517                  |0.4                     |3.4                         |13.9                    |1.0             |0.458                   |8.2                     |0.632                   |8.4                |16.9            |0.6                          |0.114                    |0.6142857142857143|3                  |0      |0          |0               |0.1073367736760593|0.5629069045186043          |0.620891147851944            |0.5879122018814087|0.007478692578949 |5        |
|9     |2023  |barnesc01|Scottie Barnes   |TORONTO RAPTORS       |21 |0.9452054794520548|34.91304347826087 |15.492753623188406|4.72463768115942  |13.27536231884058    |3.333333333333333    |2.971014492753623                |0.8115942028985508|4.463768115942029 |0.9855072463768116|6.0144927536231885|2.579710144927536 |0.8840579710144928          |2.391304347826087 |2.231884057971014 |0.9855072463768116|2.028985507246377 |0.4530567685589519|0.7739130434782608|0.2975609756097561|19.6             |2.2             |0.3           |-0.3                    |15.7                        |0.251                  |0.6                     |7.2                         |15.5                    |1.4             |0.224                   |11.1                    |0.525                   |12.1               |20.5            |1.4                          |0.087                    |0.4861111111111111|9                  |0      |0          |0               |0.0               |0.0                         |0.0                          |0.0               |0.0               |0        |

Full df shape: 105 x 53
* **Note**: The 2023 season data is collected up till 19/03/2023. Therefore, the subsequent predictions made based on this data will only reflect the information available up to that point. 


## 📈 Analysis

### 🧐 Qualitative Data Analysis  

**The qualitative aspect of project dives into NBA news and BBC sports news that could help to predict the MVP (Most Valuable Player) of each NBA season**. 

**It takes two approaches to ensure the news provide different perspectives**.

**For NBA News, they are scraped from the NBA sports news archive**. 

**For BBC sports news, it take a slightly different approach. It startes by searching for specific player names and leverage the algorithm of the search bar on the BBC sports website**. 

**Stay tuned for some fascinating insights!😆


### Part 1: NBA News

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
![images - 2](https://github.com/tz1211/DS105L-Project-404-Not-Found/blob/main/Data/news_data/github_MDtable/article.png)

**Graph 2 Number of Followers **
  - The distribution is reasonably skewed, hence mean is used for missing values for authors.
![images - 3](https://github.com/tz1211/DS105L-Project-404-Not-Found/blob/main/Data/news_data/github_MDtable/follower.png)

**Graph 3 Number of Tweets **
  - The distribution is reasonably skewed, hence mean is used for missing values for authors.
![images - 4](https://github.com/tz1211/DS105L-Project-404-Not-Found/blob/main/Data/news_data/github_MDtable/tweets.png)



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

**What does the data look like** 🤔️

**After all the data are gathered, they are combined with unique combination of "time" + " most frequent name", the quantitative data take the average, and the number of dataset of same player is called frequency**.
#### Table: Sample Final Data of NBA NEWS
* *(Taking the sample from 2019-20 season). * 

|    |   time | most_frequent_name      |   textblob_Sentiment |   nltk_Sentiment |   relevance_score |   bert_relevance |   credit_article |   credit_followers |   credit_tweets |   frequency |
|---:|-------:|:------------------------|---------------------:|-----------------:|------------------:|-----------------:|-----------------:|-------------------:|----------------:|------------:|
|  0 |   2020 | Aaron Gordon            |           0.0923111  |       0.0923111  |         0.131483  |         0.567671 |         39434.8  |           34372.6  |         40798   |           5 |
|  1 |   2020 | Al Horford              |           0.05169    |       0.05169    |         0.117488  |         0.54677  |         10781.7  |           34700.3  |         62255.7 |           3 |
|  2 |   2020 | Andre Drummond          |           0.0369387  |       0.0369387  |         0.158727  |         0.532269 |         15995.6  |           60639.6  |         67059.1 |          14 |
|  3 |   2020 | Andrew Wiggins          |           0.0904019  |       0.0904019  |         0.0992229 |         0.573194 |         28212.4  |           36785    |         42379.9 |           7 |
|  4 |   2020 | Anthony Davis           |           0.120779   |       0.120779   |         0.189062  |         0.548409 |         11444.1  |           47184.3  |         50480.3 |          27 |

### Part 2: BBC News


**While [BBC Sports News](https://www.bbc.co.uk/sport) tends to be more objective and focused on reporting factual information, it doesn't mean that sentiment-free. Nuances can still be hidden within the text. To ensure that these nuances are discovered, more advanced sentiment analysis techniques in addition to TextBlob**.

In this part, **sentiment_bert_average_score and sentiment_xlnet_average_score alongside TextBlob can provide a more comprehensive understanding of the sentiment in BBC News articles**. These models, BERT and XLNet, are designed to capture more nuanced and contextual sentiment information. 
Leveraging these models enhances the accuracy of sentiment analysis and uncover subtle sentiment variations that may contribute to predicting the NBA MVP more effectively.

**BUT**🤔️
One limitation of using BBC sports news for sentiment analysis is from gathering news content using web scraping. Since the website formatting may over time, this becomes especially challenging when the timeframe being analyzed is broad.
In situations where the web scraping fails to retrieve the content, the code will relying solely on the news title for sentiment analysis which poses a limitation. While the title can provide some insight, it may not capture the full sentiment or context present in the article's body. 

## 🖼️ Results

## 🖋️ Conclusions

## 📚 References

* [markdown file editting instruction](https://markdown.com.cn/cheat-sheet.html#%E6%80%BB%E8%A7%88)
* [Basketball reference api use instruction](https://jaebradley.github.io/basketball_reference_web_scraper/api/ )
* [Hugging Face](https://huggingface.co/)
* [Sentiment Analysis](https://www.analyticsvidhya.com/blog/2021/11/web-scraping-a-news-article-and-performing-sentiment-analysis-using-nlp/)
