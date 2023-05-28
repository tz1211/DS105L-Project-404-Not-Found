---
title: "📚 Project Title"
date: 20 March 2023
date-meta: 20 March 2023
---

# 🤖 Project Title

**Team members:** 

- [Member 1]()
- [Member 2]()
- [Member 3]()

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
### :one: Sports Matrix

### Table 1: First ten rows from merged_data_2010_to_2023   
|    |   year | name                    |   minutes_played |   games_played |   points | team                   |   age |   assists |   attempted_field_goals |   attempted_free_throws |   attempted_three_point_field_goals |   blocks |   defensive_rebounds |   games_started |   made_field_goals |   made_free_throws |   made_three_point_field_goals |   offensive_rebounds |   personal_fouls | positions          | slug      |   steals |   turnovers |
|---:|-------:|:------------------------|-----------------:|---------------:|---------:|:-----------------------|------:|----------:|------------------------:|------------------------:|------------------------------------:|---------:|---------------------:|----------------:|-------------------:|-------------------:|-------------------------------:|---------------------:|-----------------:|:-------------------|:----------|---------:|------------:|
|  0 |   2023 | Jayson Tatum            |             2508 |             67 |     2008 | BOSTON CELTICS         |    24 |       317 |                    1424 |                     568 |                                 632 |       50 |                  524 |              67 |                651 |                488 |                            218 |                   73 |              144 | ['POWER FORWARD']  | tatumja01 |       68 |         198 |
|  1 |   2023 | Joel Embiid             |             2030 |             58 |     1946 | PHILADELPHIA 76ERS     |    28 |       238 |                    1186 |                     691 |                                 174 |      102 |                  490 |              58 |                647 |                591 |                             61 |                  105 |              186 | ['CENTER']         | embiijo01 |       62 |         201 |
|  2 |   2023 | Shai Gilgeous-Alexander |             2135 |             60 |     1884 | OKLAHOMA CITY THUNDER  |    24 |       330 |                    1222 |                     646 |                                 148 |       60 |                  233 |              60 |                624 |                584 |                             52 |                   54 |              163 | ['POINT GUARD']    | gilgesh01 |      102 |         173 |
|  3 |   2023 | Luka Dončić             |             2068 |             57 |     1879 | DALLAS MAVERICKS       |    23 |       458 |                    1257 |                     629 |                                 453 |       28 |                  443 |              57 |                629 |                463 |                            158 |                   48 |              148 | ['POINT GUARD']    | doncilu01 |       83 |         209 |
|  4 |   2023 | Julius Randle           |             2623 |             73 |     1869 | NEW YORK KNICKS        |    28 |       299 |                    1372 |                     515 |                                 612 |       19 |                  604 |              73 |                633 |                391 |                            212 |                  139 |              223 | ['POWER FORWARD']  | randlju01 |       47 |         208 |
|  5 |   2023 | Damian Lillard          |             2073 |             57 |     1836 | PORTLAND TRAIL BLAZERS |    32 |       413 |                    1183 |                     544 |                                 648 |       18 |                  227 |              57 |                548 |                498 |                            242 |                   43 |              108 | ['POINT GUARD']    | lillada01 |       50 |         189 |
|  6 |   2023 | Anthony Edwards         |             2558 |             71 |     1755 | MINNESOTA TIMBERWOLVES |    21 |       315 |                    1380 |                     378 |                                 520 |       51 |                  378 |              71 |                636 |                290 |                            193 |                   39 |              172 | ['SHOOTING GUARD'] | edwaran01 |      114 |         237 |
|  7 |   2023 | Giannis Antetokounmpo   |             1820 |             56 |     1750 | MILWAUKEE BUCKS        |    28 |       312 |                    1142 |                     707 |                                 156 |       45 |                  538 |              56 |                623 |                459 |                             45 |                  126 |              179 | ['POWER FORWARD']  | antetgi01 |       41 |         219 |
|  8 |   2023 | Trae Young              |             2232 |             64 |     1711 | ATLANTA HAWKS          |    24 |       642 |                    1255 |                     541 |                                 418 |        9 |                  146 |              64 |                545 |                480 |                            141 |                   52 |               94 | ['POINT GUARD']    | youngtr01 |       72 |         261 |
|  9 |   2023 | Zach LaVine             |             2439 |             67 |     1678 | CHICAGO BULLS          |    27 |       275 |                    1216 |                     380 |                                 490 |       16 |                  277 |              67 |                584 |                323 |                            187 |                   38 |              143 | ['SHOOTING GUARD'] | lavinza01 |       63 |         171 |
| 10 |   2023 | Donovan Mitchell        |             2165 |             61 |     1669 | CLEVELAND CAVALIERS    |    26 |       281 |                    1236 |                     314 |                                 569 |       23 |                  195 |              61 |                590 |                275 |                            214 |                   58 |              148 | ['SHOOTING GUARD'] | mitchdo01 |       93 |         161 |  

 * Table 1 ----> [merged_player_data_2010_2023.csv](https://github.com/tz1211/DS105L-Project-404-Not-Found/files/11583326/merged_player_data_2010_2023.csv)

### Table 2: Merged_Team_Conference  
* *(Taking the 2022-2023 season from the merged table)*  

|    |   season | Team                   | Conference   |   W |   L |   win_rate |   conference_standing |
|---:|---------:|:-----------------------|:-------------|----:|----:|-----------:|----------------------:|
|  0 |     2023 | Denver Nuggets         | Western      |  53 |  29 |   0.646341 |                     1 |
|  1 |     2023 | Memphis Grizzlies      | Western      |  51 |  31 |   0.621951 |                     2 |
|  2 |     2023 | Sacramento Kings       | Western      |  48 |  34 |   0.585366 |                     3 |
|  3 |     2023 | Phoenix Suns           | Western      |  45 |  37 |   0.54878  |                     4 |
|  4 |     2023 | Los Angeles Clippers   | Western      |  44 |  38 |   0.536585 |                     5 |
|  5 |     2023 | Golden State Warriors  | Western      |  44 |  38 |   0.536585 |                     6 |
|  6 |     2023 | Los Angeles Lakers     | Western      |  43 |  39 |   0.52439  |                     7 |
|  7 |     2023 | Minnesota Timberwolves | Western      |  42 |  40 |   0.512195 |                     8 |
|  8 |     2023 | New Orleans Pelicans   | Western      |  42 |  40 |   0.512195 |                     9 |
|  9 |     2023 | Oklahoma City Thunder  | Western      |  40 |  42 |   0.487805 |                    10 |
| 10 |     2023 | Dallas Mavericks       | Western      |  38 |  44 |   0.463415 |                    11 |
| 11 |     2023 | Utah Jazz              | Western      |  37 |  45 |   0.45122  |                    12 |
| 12 |     2023 | Portland Trail Blazers | Western      |  33 |  49 |   0.402439 |                    13 |
| 13 |     2023 | Houston Rockets        | Western      |  22 |  60 |   0.268293 |                    14 |
| 14 |     2023 | San Antonio Spurs      | Western      |  22 |  60 |   0.268293 |                    15 |
| 15 |     2023 | Milwaukee Bucks        | Eastern      |  58 |  24 |   0.707317 |                     1 |
| 16 |     2023 | Boston Celtics         | Eastern      |  57 |  25 |   0.695122 |                     2 |
| 17 |     2023 | Philadelphia 76ers     | Eastern      |  54 |  28 |   0.658537 |                     3 |
| 18 |     2023 | Cleveland Cavaliers    | Eastern      |  51 |  31 |   0.621951 |                     4 |
| 19 |     2023 | New York Knicks        | Eastern      |  47 |  35 |   0.573171 |                     5 |
| 20 |     2023 | Brooklyn Nets          | Eastern      |  45 |  37 |   0.54878  |                     6 |
| 21 |     2023 | Miami Heat             | Eastern      |  44 |  38 |   0.536585 |                     7 |
| 22 |     2023 | Atlanta Hawks          | Eastern      |  41 |  41 |   0.5      |                     8 |
| 23 |     2023 | Toronto Raptors        | Eastern      |  41 |  41 |   0.5      |                     9 |
| 24 |     2023 | Chicago Bulls          | Eastern      |  40 |  42 |   0.487805 |                    10 |
| 25 |     2023 | Indiana Pacers         | Eastern      |  35 |  47 |   0.426829 |                    11 |
| 26 |     2023 | Washington Wizards     | Eastern      |  35 |  47 |   0.426829 |                    12 |
| 27 |     2023 | Orlando Magic          | Eastern      |  34 |  48 |   0.414634 |                    13 |
| 28 |     2023 | Charlotte Hornets      | Eastern      |  27 |  55 |   0.329268 |                    14 |
| 29 |     2023 | Detroit Pistons        | Eastern      |  17 |  65 |   0.207317 |                    15 |

 * Table 2 ----> [merged_team_conference.csv](https://github.com/tz1211/DS105L-Project-404-Not-Found/files/11583327/merged_team_conference.csv)  

### Table 3: Merged_advanced_data 
* *(This table is ranked by the efficiency of each player. Also taking 2022-2023 season as example)*  

|      |   year | name                  |   age |   assist_percentage |   block_percentage |   box_plus_minus |   defensive_box_plus_minus |   defensive_rebound_percentage |   defensive_win_shares |   free_throw_attempt_rate |   games_played | is_combined_totals   |   minutes_played |   offensive_box_plus_minus |   offensive_rebound_percentage |   offensive_win_shares |   player_efficiency_rating | positions          | slug      |   steal_percentage | team                   |   three_point_attempt_rate |   total_rebound_percentage |   true_shooting_percentage |   turnover_percentage |   usage_percentage |   value_over_replacement_player |   win_shares |   win_shares_per_48_minutes |
|-----:|-------:|:----------------------|------:|--------------------:|-------------------:|-----------------:|---------------------------:|-------------------------------:|-----------------------:|--------------------------:|---------------:|:---------------------|-----------------:|---------------------------:|-------------------------------:|-----------------------:|---------------------------:|:-------------------|:----------|-------------------:|:-----------------------|---------------------------:|---------------------------:|---------------------------:|----------------------:|-------------------:|--------------------------------:|-------------:|----------------------------:|
| 7444 |   2023 | Stanley Umude         |    23 |                 0   |               43.8 |             48.5 |                       32.7 |                            0   |                    0   |                     2     |              1 | False                |                2 |                       15.8 |                            0   |                    0   |                       65.6 | ['SHOOTING GUARD'] | umudest01 |               24.2 | DETROIT PISTONS        |                      1     |                        0   |                      0.532 |                   0   |               39.9 |                             0   |          0   |                       0.629 |
| 7445 |   2023 | Tyler Dorsey          |    26 |                 0   |                0   |             18.2 |                        1.6 |                           14.9 |                    0   |                     0     |              3 | False                |                8 |                       16.6 |                           14.4 |                    0.1 |                       45.9 | ['SHOOTING GUARD'] | dorsety01 |                0   | DALLAS MAVERICKS       |                      0.4   |                       14.7 |                      0.9   |                   0   |               28.3 |                             0   |          0.1 |                       0.37  |
| 7446 |   2023 | A.J. Lawson           |    22 |                 0   |                0   |              5.2 |                        7.6 |                           55.1 |                    0   |                     0     |              1 | False                |                2 |                       -2.3 |                            0   |                    0   |                       34.6 | ['SHOOTING GUARD'] | lawsoaj01 |                0   | MINNESOTA TIMBERWOLVES |                      0     |                       28.1 |                      1     |                   0   |               21.4 |                             0   |          0   |                       0.377 |
| 7447 |   2023 | Nikola Jokić          |    27 |                46.3 |                1.7 |             13   |                        4.4 |                           31.5 |                    3.4 |                     0.402 |             64 | False                |             2172 |                        8.6 |                            8.6 |                   10.8 |                       31.6 | ['CENTER']         | jokicni01 |                1.8 | DENVER NUGGETS         |                      0.143 |                       20.4 |                      0.703 |                  16.8 |               27.1 |                             8.2 |         14.1 |                       0.312 |
| 7448 |   2023 | Joel Embiid           |    28 |                22.5 |                4.7 |              9   |                        2.3 |                           28   |                    3.6 |                     0.583 |             58 | False                |             2030 |                        6.7 |                            6.2 |                    7.5 |                       31.5 | ['CENTER']         | embiijo01 |                1.5 | PHILADELPHIA 76ERS     |                      0.147 |                       17.3 |                      0.653 |                  11.9 |               37.2 |                             5.6 |         11.1 |                       0.262 |
| 7449 |   2023 | Kevin Durant          |    34 |                19.6 |                3.7 |             12.4 |                        2.8 |                           24.3 |                    0.1 |                     0.405 |              3 | False                |               98 |                        9.6 |                            1.1 |                    0.5 |                       30.1 | ['SMALL FORWARD']  | duranke01 |                0.5 | PHOENIX SUNS           |                      0.31  |                       12.5 |                      0.808 |                  10.8 |               24.1 |                             0.4 |          0.6 |                       0.295 |
| 7450 |   2023 | Luka Dončić           |    23 |                43.4 |                1.2 |              9.5 |                        1.6 |                           25.6 |                    2.6 |                     0.5   |             57 | False                |             2068 |                        7.9 |                            2.7 |                    6.7 |                       29.5 | ['POINT GUARD']    | doncilu01 |                2   | DALLAS MAVERICKS       |                      0.36  |                       13.9 |                      0.613 |                  12   |               38.2 |                             6   |          9.3 |                       0.215 |
| 7451 |   2023 | Justin Champagnie     |    21 |                15.4 |                0   |              7.9 |                        1.8 |                           33.4 |                    0   |                     0     |              3 | False                |               11 |                        6.1 |                            9.6 |                    0.1 |                       29   | ['SMALL FORWARD']  | champju01 |                0   | TORONTO RAPTORS        |                      0     |                       20.6 |                      1     |                   0   |               11.6 |                             0   |          0.1 |                       0.33  |
| 7452 |   2023 | Giannis Antetokounmpo |    28 |                32.3 |                2   |              8.2 |                        2.6 |                           29.5 |                    3.4 |                     0.619 |             56 | False                |             1820 |                        5.6 |                            7.5 |                    4.4 |                       28.6 | ['POWER FORWARD']  | antetgi01 |                1.1 | MILWAUKEE BUCKS        |                      0.137 |                       18.9 |                      0.602 |                  13.1 |               38.7 |                             4.7 |          7.7 |                       0.204 |
| 7453 |   2023 | Anthony Davis         |    29 |                12.7 |                5.3 |              6.2 |                        1.8 |                           28   |                    2.8 |                     0.449 |             46 | False                |             1546 |                        4.4 |                           11.1 |                    4.2 |                       27.6 | ['CENTER']         | davisan02 |                1.4 | LOS ANGELES LAKERS     |                      0.086 |                       19.8 |                      0.626 |                  10.2 |               28.8 |                             3.2 |          7   |                       0.216 |

 * Table 3 ----> [merged_advanced_player_data_2010_2023.csv](https://github.com/tz1211/DS105L-Project-404-Not-Found/files/11583329/merged_advanced_player_data_2010_2023.csv)

### Table 4: Count for MVP  
* *It count all the NBA MVP in the history, and also record who won the MVP a year past and two years past. This table is used for import to the machine learning algorithm for further analysis*  

 * Table 4 ----> [MVP_count.csv](https://github.com/tz1211/DS105L-Project-404-Not-Found/files/11583297/MVP_count.csv)


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

* Graph 1 Number of Articles
- The distribution is highly skewed, hence medium is used for missing values for authors.
![images - 2](https://github.com/tz1211/DS105L-Project-404-Not-Found/blob/main/Data/github_MDtable/article.png)

* Graph 2 Number of Followers 
- The distribution is reasonably skewed, hence mean is used for missing values for authors.
![images - 3](https://github.com/tz1211/DS105L-Project-404-Not-Found/blob/main/Data/github_MDtable/follower.png)

* Graph 3 Number of Followers 
- The distribution is reasonably skewed, hence mean is used for missing values for authors.
![images - 4](https://github.com/tz1211/DS105L-Project-404-Not-Found/blob/main/Data/github_MDtable/tweets.png)



### :two: Sentiment and Relevance of NBA News











## 🖼️ Results

## 🖋️ Conclusions

## 📚 References
