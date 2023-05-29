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

### 1️⃣ Quantitative Data (Individual performance + Team performance) 

<details>
<summary><strong>Individual Player Data</strong> (<a href="https://github.com/tz1211/DS105L-Project-404-Not-Found/blob/main/Data/player_data.csv">player_data.csv</a>)</summary>  

<table align="right">
<thead>
<tr>
<th></th>
<th>season</th>
<th>name</th>
<th>team</th>
<th>age</th>
<th>%games_played</th>
<th>minutes_played</th>
<th>points</th>
<th>assists</th>
<th>attempted_field_goals</th>
<th>attempted_free_throws</th>
<th>attempted_three_point_field_goals</th>
<th>blocks</th>
<th>defensive_rebounds</th>
<th>games_started</th>
<th>made_field_goals</th>
<th>made_free_throws</th>
<th>made_three_point_field_goals</th>
<th>offensive_rebounds</th>
<th>personal_fouls</th>
<th>steals</th>
<th>turnovers</th>
<th>field_goal%</th>
<th>free_throw%</th>
<th>3pt%</th>
<th>assist_percentage</th>
<th>block_percentage</th>
<th>box_plus_minus</th>
<th>defensive_box_plus_minus</th>
<th>defensive_rebound_percentage</th>
<th>free_throw_attempt_rate</th>
<th>offensive_box_plus_minus</th>
<th>offensive_rebound_percentage</th>
<th>player_efficiency_rating</th>
<th>steal_percentage</th>
<th>three_point_attempt_rate</th>
<th>total_rebound_percentage</th>
<th>true_shooting_percentage</th>
<th>turnover_percentage</th>
<th>usage_percentage</th>
<th>value_over_replacement_player</th>
<th>win_shares_per_48_minutes</th>
<th>is_mvp</th>
</tr>
</thead>
<tbody><tr>
<td>1121</td>
<td>2022</td>
<td>Bam Adebayo</td>
<td>MIAMI HEAT</td>
<td>24</td>
<td>0.682927</td>
<td>32.5893</td>
<td>19.0714</td>
<td>3.39286</td>
<td>13.0179</td>
<td>6.07143</td>
<td>0.107143</td>
<td>0.785714</td>
<td>7.625</td>
<td>1</td>
<td>7.25</td>
<td>4.57143</td>
<td>0</td>
<td>2.44643</td>
<td>3.05357</td>
<td>1.42857</td>
<td>2.64286</td>
<td>0.556927</td>
<td>0.752941</td>
<td>0</td>
<td>17.5</td>
<td>2.6</td>
<td>3.8</td>
<td>2.1</td>
<td>26.1</td>
<td>0.466</td>
<td>1.7</td>
<td>8.7</td>
<td>21.8</td>
<td>2.2</td>
<td>0.008</td>
<td>17.5</td>
<td>0.608</td>
<td>14.4</td>
<td>25</td>
<td>2.7</td>
<td>0.188</td>
<td>0</td>
</tr>
<tr>
<td>1122</td>
<td>2022</td>
<td>Jarrett Allen</td>
<td>CLEVELAND CAVALIERS</td>
<td>23</td>
<td>0.682927</td>
<td>32.3036</td>
<td>16.1429</td>
<td>1.64286</td>
<td>9.73214</td>
<td>4.16071</td>
<td>0.178571</td>
<td>1.33929</td>
<td>7.32143</td>
<td>1</td>
<td>6.58929</td>
<td>2.94643</td>
<td>0.0178571</td>
<td>3.42857</td>
<td>1.73214</td>
<td>0.785714</td>
<td>1.67857</td>
<td>0.677064</td>
<td>0.708155</td>
<td>0.1</td>
<td>8.2</td>
<td>3.7</td>
<td>3.9</td>
<td>1.2</td>
<td>24.5</td>
<td>0.428</td>
<td>2.7</td>
<td>12</td>
<td>23</td>
<td>1.2</td>
<td>0.018</td>
<td>18.4</td>
<td>0.698</td>
<td>12.7</td>
<td>18.1</td>
<td>2.7</td>
<td>0.225</td>
<td>0</td>
</tr>
<tr>
<td>1123</td>
<td>2022</td>
<td>Giannis Antetokounmpo</td>
<td>MILWAUKEE BUCKS</td>
<td>27</td>
<td>0.817073</td>
<td>32.8955</td>
<td>29.8806</td>
<td>5.79104</td>
<td>18.5821</td>
<td>11.4328</td>
<td>3.61194</td>
<td>1.35821</td>
<td>9.61194</td>
<td>1</td>
<td>10.2836</td>
<td>8.25373</td>
<td>1.0597</td>
<td>2</td>
<td>3.16418</td>
<td>1.07463</td>
<td>3.26866</td>
<td>0.553414</td>
<td>0.721932</td>
<td>0.293388</td>
<td>31.7</td>
<td>4</td>
<td>11.2</td>
<td>3.5</td>
<td>30.4</td>
<td>0.615</td>
<td>7.6</td>
<td>6.6</td>
<td>32.1</td>
<td>1.6</td>
<td>0.194</td>
<td>18.7</td>
<td>0.633</td>
<td>12.2</td>
<td>34.9</td>
<td>7.4</td>
<td>0.281</td>
<td>0</td>
</tr>
<tr>
<td>1124</td>
<td>2022</td>
<td>Cole Anthony</td>
<td>ORLANDO MAGIC</td>
<td>21</td>
<td>0.792683</td>
<td>31.6769</td>
<td>16.3385</td>
<td>5.67692</td>
<td>14.0308</td>
<td>3.89231</td>
<td>6.01538</td>
<td>0.261538</td>
<td>4.86154</td>
<td>1</td>
<td>5.49231</td>
<td>3.32308</td>
<td>2.03077</td>
<td>0.492308</td>
<td>2.63077</td>
<td>0.707692</td>
<td>2.61538</td>
<td>0.391447</td>
<td>0.853755</td>
<td>0.337596</td>
<td>28.9</td>
<td>0.8</td>
<td>-1.2</td>
<td>-0.6</td>
<td>16.2</td>
<td>0.277</td>
<td>-0.6</td>
<td>1.6</td>
<td>13.5</td>
<td>1.1</td>
<td>0.429</td>
<td>8.9</td>
<td>0.519</td>
<td>14.2</td>
<td>25.1</td>
<td>0.4</td>
<td>0.038</td>
<td>0</td>
</tr>
<tr>
<td>1125</td>
<td>2022</td>
<td>OG Anunoby</td>
<td>TORONTO RAPTORS</td>
<td>24</td>
<td>0.585366</td>
<td>36</td>
<td>17.125</td>
<td>2.60417</td>
<td>14.5208</td>
<td>2.45833</td>
<td>6.60417</td>
<td>0.520833</td>
<td>3.95833</td>
<td>1</td>
<td>6.4375</td>
<td>1.85417</td>
<td>2.39583</td>
<td>1.54167</td>
<td>2.72917</td>
<td>1.47917</td>
<td>1.66667</td>
<td>0.443329</td>
<td>0.754237</td>
<td>0.362776</td>
<td>11</td>
<td>1.4</td>
<td>0.5</td>
<td>0.1</td>
<td>12.6</td>
<td>0.169</td>
<td>0.4</td>
<td>4.4</td>
<td>14.8</td>
<td>2.1</td>
<td>0.455</td>
<td>8.3</td>
<td>0.549</td>
<td>9.7</td>
<td>20.5</td>
<td>1.1</td>
<td>0.104</td>
<td>0</td>
</tr>
<tr>
<td>1126</td>
<td>2022</td>
<td>LaMelo Ball</td>
<td>CHARLOTTE HORNETS</td>
<td>20</td>
<td>0.914634</td>
<td>32.2933</td>
<td>20.1067</td>
<td>7.61333</td>
<td>16.72</td>
<td>3.24</td>
<td>7.53333</td>
<td>0.4</td>
<td>5.24</td>
<td>1</td>
<td>7.17333</td>
<td>2.82667</td>
<td>2.93333</td>
<td>1.44</td>
<td>3.16</td>
<td>1.58667</td>
<td>3.26667</td>
<td>0.429027</td>
<td>0.872428</td>
<td>0.389381</td>
<td>35.7</td>
<td>1.2</td>
<td>3.4</td>
<td>0.1</td>
<td>17.4</td>
<td>0.194</td>
<td>3.3</td>
<td>4.7</td>
<td>19.7</td>
<td>2.4</td>
<td>0.451</td>
<td>11</td>
<td>0.554</td>
<td>15.3</td>
<td>28.2</td>
<td>3.3</td>
<td>0.116</td>
<td>0</td>
</tr>
<tr>
<td>1127</td>
<td>2022</td>
<td>Lonzo Ball</td>
<td>CHICAGO BULLS</td>
<td>24</td>
<td>0.426829</td>
<td>34.6286</td>
<td>13</td>
<td>5.08571</td>
<td>10.9429</td>
<td>0.8</td>
<td>7.42857</td>
<td>0.885714</td>
<td>4.42857</td>
<td>1</td>
<td>4.62857</td>
<td>0.6</td>
<td>3.14286</td>
<td>1</td>
<td>2.42857</td>
<td>1.82857</td>
<td>2.34286</td>
<td>0.422977</td>
<td>0.75</td>
<td>0.423077</td>
<td>20</td>
<td>2.2</td>
<td>2.5</td>
<td>1.6</td>
<td>14.3</td>
<td>0.073</td>
<td>0.9</td>
<td>3.3</td>
<td>14.5</td>
<td>2.6</td>
<td>0.679</td>
<td>8.8</td>
<td>0.575</td>
<td>17.2</td>
<td>17.4</td>
<td>1.4</td>
<td>0.088</td>
<td>0</td>
</tr>
<tr>
<td>1128</td>
<td>2022</td>
<td>Harrison Barnes</td>
<td>SACRAMENTO KINGS</td>
<td>29</td>
<td>0.939024</td>
<td>33.5974</td>
<td>16.4286</td>
<td>2.41558</td>
<td>10.8312</td>
<td>5.36364</td>
<td>4.67532</td>
<td>0.181818</td>
<td>4.54545</td>
<td>1</td>
<td>5.07792</td>
<td>4.42857</td>
<td>1.84416</td>
<td>1.06494</td>
<td>1.22078</td>
<td>0.688312</td>
<td>1.53247</td>
<td>0.468825</td>
<td>0.825666</td>
<td>0.394444</td>
<td>10.5</td>
<td>0.5</td>
<td>0.2</td>
<td>-1.3</td>
<td>14.9</td>
<td>0.495</td>
<td>1.5</td>
<td>3.4</td>
<td>15.7</td>
<td>1</td>
<td>0.432</td>
<td>9.1</td>
<td>0.623</td>
<td>10.4</td>
<td>18.8</td>
<td>1.4</td>
<td>0.112</td>
<td>0</td>
</tr>
<tr>
<td>1129</td>
<td>2022</td>
<td>Scottie Barnes</td>
<td>TORONTO RAPTORS</td>
<td>20</td>
<td>0.902439</td>
<td>35.3649</td>
<td>15.3243</td>
<td>3.45946</td>
<td>12.5946</td>
<td>2.90541</td>
<td>2.60811</td>
<td>0.743243</td>
<td>4.89189</td>
<td>1</td>
<td>6.2027</td>
<td>2.13514</td>
<td>0.783784</td>
<td>2.63514</td>
<td>2.59459</td>
<td>1.08108</td>
<td>1.83784</td>
<td>0.492489</td>
<td>0.734884</td>
<td>0.300518</td>
<td>14.7</td>
<td>2.1</td>
<td>0.9</td>
<td>0.4</td>
<td>15.8</td>
<td>0.231</td>
<td>0.5</td>
<td>7.7</td>
<td>16.3</td>
<td>1.5</td>
<td>0.207</td>
<td>11.5</td>
<td>0.552</td>
<td>11.7</td>
<td>19</td>
<td>1.9</td>
<td>0.122</td>
<td>0</td>
</tr>
<tr>
<td>1130</td>
<td>2022</td>
<td>RJ Barrett</td>
<td>NEW YORK KNICKS</td>
<td>21</td>
<td>0.853659</td>
<td>34.5286</td>
<td>20.0286</td>
<td>2.97143</td>
<td>17.0571</td>
<td>5.8</td>
<td>5.77143</td>
<td>0.228571</td>
<td>4.88571</td>
<td>1</td>
<td>6.95714</td>
<td>4.14286</td>
<td>1.97143</td>
<td>0.942857</td>
<td>2.02857</td>
<td>0.614286</td>
<td>2.15714</td>
<td>0.407873</td>
<td>0.714286</td>
<td>0.341584</td>
<td>14.9</td>
<td>0.7</td>
<td>-1.6</td>
<td>-1.3</td>
<td>15.5</td>
<td>0.34</td>
<td>-0.3</td>
<td>2.9</td>
<td>13.7</td>
<td>0.9</td>
<td>0.338</td>
<td>9.1</td>
<td>0.511</td>
<td>9.9</td>
<td>27.6</td>
<td>0.2</td>
<td>0.046</td>
<td>0</td>
</tr>
</tbody></table>

* *This table include boxscore and advanced statistics that reflects players' individual performances. (Source: [Basketball Reference](https://www.basketball-reference.com/))
</details>

<details>
<summary><strong>Team Data</strong> (<a href="https://github.com/tz1211/DS105L-Project-404-Not-Found/blob/main/Data/team_data.csv">team_data.csv</a>)</summary>  

<table align="right">
<thead>
<tr>
<th></th>
<th>season</th>
<th>team</th>
<th>conference</th>
<th>W</th>
<th>L</th>
<th>win_rate</th>
<th>conference_standing</th>
</tr>
</thead>
<tbody><tr>
<td>30</td>
<td>2022</td>
<td>PHOENIX SUNS</td>
<td>Western</td>
<td>64</td>
<td>18</td>
<td>0.7804878048780488</td>
<td>1</td>
</tr>
<tr>
<td>31</td>
<td>2022</td>
<td>MEMPHIS GRIZZLIES</td>
<td>Western</td>
<td>56</td>
<td>26</td>
<td>0.6829268292682927</td>
<td>2</td>
</tr>
<tr>
<td>32</td>
<td>2022</td>
<td>GOLDEN STATE WARRIORS</td>
<td>Western</td>
<td>53</td>
<td>29</td>
<td>0.6463414634146342</td>
<td>3</td>
</tr>
<tr>
<td>33</td>
<td>2022</td>
<td>DALLAS MAVERICKS</td>
<td>Western</td>
<td>52</td>
<td>30</td>
<td>0.6341463414634146</td>
<td>4</td>
</tr>
<tr>
<td>34</td>
<td>2022</td>
<td>UTAH JAZZ</td>
<td>Western</td>
<td>49</td>
<td>33</td>
<td>0.5975609756097561</td>
<td>5</td>
</tr>
<tr>
<td>35</td>
<td>2022</td>
<td>DENVER NUGGETS</td>
<td>Western</td>
<td>48</td>
<td>34</td>
<td>0.5853658536585366</td>
<td>6</td>
</tr>
<tr>
<td>36</td>
<td>2022</td>
<td>MINNESOTA TIMBERWOLVES</td>
<td>Western</td>
<td>46</td>
<td>36</td>
<td>0.5609756097560976</td>
<td>7</td>
</tr>
<tr>
<td>37</td>
<td>2022</td>
<td>LOS ANGELES CLIPPERS</td>
<td>Western</td>
<td>42</td>
<td>40</td>
<td>0.5121951219512195</td>
<td>8</td>
</tr>
<tr>
<td>38</td>
<td>2022</td>
<td>NEW ORLEANS PELICANS</td>
<td>Western</td>
<td>36</td>
<td>46</td>
<td>0.4390243902439024</td>
<td>9</td>
</tr>
<tr>
<td>39</td>
<td>2022</td>
<td>SAN ANTONIO SPURS</td>
<td>Western</td>
<td>34</td>
<td>48</td>
<td>0.4146341463414634</td>
<td>10</td>
</tr>
<tr>
<td>40</td>
<td>2022</td>
<td>LOS ANGELES LAKERS</td>
<td>Western</td>
<td>33</td>
<td>49</td>
<td>0.4024390243902439</td>
<td>11</td>
</tr>
<tr>
<td>41</td>
<td>2022</td>
<td>SACRAMENTO KINGS</td>
<td>Western</td>
<td>30</td>
<td>52</td>
<td>0.3658536585365853</td>
<td>12</td>
</tr>
<tr>
<td>42</td>
<td>2022</td>
<td>PORTLAND TRAIL BLAZERS</td>
<td>Western</td>
<td>27</td>
<td>55</td>
<td>0.3292682926829268</td>
<td>13</td>
</tr>
<tr>
<td>43</td>
<td>2022</td>
<td>OKLAHOMA CITY THUNDER</td>
<td>Western</td>
<td>24</td>
<td>58</td>
<td>0.2926829268292683</td>
<td>14</td>
</tr>
<tr>
<td>44</td>
<td>2022</td>
<td>HOUSTON ROCKETS</td>
<td>Western</td>
<td>20</td>
<td>62</td>
<td>0.2439024390243902</td>
<td>15</td>
</tr>
<tr>
<td>45</td>
<td>2022</td>
<td>MIAMI HEAT</td>
<td>Eastern</td>
<td>53</td>
<td>29</td>
<td>0.6463414634146342</td>
<td>1</td>
</tr>
<tr>
<td>46</td>
<td>2022</td>
<td>BOSTON CELTICS</td>
<td>Eastern</td>
<td>51</td>
<td>31</td>
<td>0.6219512195121951</td>
<td>2</td>
</tr>
<tr>
<td>47</td>
<td>2022</td>
<td>MILWAUKEE BUCKS</td>
<td>Eastern</td>
<td>51</td>
<td>31</td>
<td>0.6219512195121951</td>
<td>3</td>
</tr>
<tr>
<td>48</td>
<td>2022</td>
<td>PHILADELPHIA 76ERS</td>
<td>Eastern</td>
<td>51</td>
<td>31</td>
<td>0.6219512195121951</td>
<td>4</td>
</tr>
<tr>
<td>49</td>
<td>2022</td>
<td>TORONTO RAPTORS</td>
<td>Eastern</td>
<td>48</td>
<td>34</td>
<td>0.5853658536585366</td>
<td>5</td>
</tr>
<tr>
<td>50</td>
<td>2022</td>
<td>CHICAGO BULLS</td>
<td>Eastern</td>
<td>46</td>
<td>36</td>
<td>0.5609756097560976</td>
<td>6</td>
</tr>
<tr>
<td>51</td>
<td>2022</td>
<td>BROOKLYN NETS</td>
<td>Eastern</td>
<td>44</td>
<td>38</td>
<td>0.5365853658536586</td>
<td>7</td>
</tr>
<tr>
<td>52</td>
<td>2022</td>
<td>CLEVELAND CAVALIERS</td>
<td>Eastern</td>
<td>44</td>
<td>38</td>
<td>0.5365853658536586</td>
<td>8</td>
</tr>
<tr>
<td>53</td>
<td>2022</td>
<td>ATLANTA HAWKS</td>
<td>Eastern</td>
<td>43</td>
<td>39</td>
<td>0.524390243902439</td>
<td>9</td>
</tr>
<tr>
<td>54</td>
<td>2022</td>
<td>CHARLOTTE HORNETS</td>
<td>Eastern</td>
<td>43</td>
<td>39</td>
<td>0.524390243902439</td>
<td>10</td>
</tr>
<tr>
<td>55</td>
<td>2022</td>
<td>NEW YORK KNICKS</td>
<td>Eastern</td>
<td>37</td>
<td>45</td>
<td>0.4512195121951219</td>
<td>11</td>
</tr>
<tr>
<td>56</td>
<td>2022</td>
<td>WASHINGTON WIZARDS</td>
<td>Eastern</td>
<td>35</td>
<td>47</td>
<td>0.4268292682926829</td>
<td>12</td>
</tr>
<tr>
<td>57</td>
<td>2022</td>
<td>INDIANA PACERS</td>
<td>Eastern</td>
<td>25</td>
<td>57</td>
<td>0.3048780487804878</td>
<td>13</td>
</tr>
<tr>
<td>58</td>
<td>2022</td>
<td>DETROIT PISTONS</td>
<td>Eastern</td>
<td>23</td>
<td>59</td>
<td>0.2804878048780488</td>
<td>14</td>
</tr>
<tr>
<td>59</td>
<td>2022</td>
<td>ORLANDO MAGIC</td>
<td>Eastern</td>
<td>22</td>
<td>60</td>
<td>0.2682926829268293</td>
<td>15</td>
</tr>
</tbody></table>

This table includes the win percentage and conference standing for each team. (Source: [Basketball Reference](https://www.basketball-reference.com/))
</details>

### 2️⃣ Qualitative Data (Sports News and Media Narratives)

<details>
<summary><strong>Quantified NBA Sports News - Sentiments and Relevance</strong></summary>
(Taking the 2019-2020 season from the merged table, the top 10 samples) 

<table>
<thead>
<tr>
<th align="right"></th>
<th align="right">time</th>
<th align="right">most_frequent_name</th>
<th align="right">textblob_Sentiment</th>
<th align="right">nltk_Sentiment</th>
<th align="right">relevance_score</th>
<th align="right">bert_relevance</th>
<th align="right">credit_article</th>
<th align="right">credit_followers</th>
<th align="right">credit_tweets</th>
<th align="right">frequency</th>
</tr>
</thead>
<tbody><tr>
<td align="right">0</td>
<td align="right">2020</td>
<td align="right">Aaron Gordon</td>
<td align="right">0.0923111</td>
<td align="right">0.0923111</td>
<td align="right">0.131483</td>
<td align="right">0.567671</td>
<td align="right">39434.8</td>
<td align="right">34372.6</td>
<td align="right">40798</td>
<td align="right">5</td>
</tr>
<tr>
<td align="right">1</td>
<td align="right">2020</td>
<td align="right">Al Horford</td>
<td align="right">0.05169</td>
<td align="right">0.05169</td>
<td align="right">0.117488</td>
<td align="right">0.54677</td>
<td align="right">10781.7</td>
<td align="right">34700.3</td>
<td align="right">62255.7</td>
<td align="right">3</td>
</tr>
<tr>
<td align="right">2</td>
<td align="right">2020</td>
<td align="right">Andre Drummond</td>
<td align="right">0.0369387</td>
<td align="right">0.0369387</td>
<td align="right">0.158727</td>
<td align="right">0.532269</td>
<td align="right">15995.6</td>
<td align="right">60639.6</td>
<td align="right">67059.1</td>
<td align="right">14</td>
</tr>
<tr>
<td align="right">3</td>
<td align="right">2020</td>
<td align="right">Andrew Wiggins</td>
<td align="right">0.0904019</td>
<td align="right">0.0904019</td>
<td align="right">0.0992229</td>
<td align="right">0.573194</td>
<td align="right">28212.4</td>
<td align="right">36785</td>
<td align="right">42379.9</td>
<td align="right">7</td>
</tr>
<tr>
<td align="right">4</td>
<td align="right">2020</td>
<td align="right">Anthony Davis</td>
<td align="right">0.120779</td>
<td align="right">0.120779</td>
<td align="right">0.189062</td>
<td align="right">0.548409</td>
<td align="right">11444.1</td>
<td align="right">47184.3</td>
<td align="right">50480.3</td>
<td align="right">27</td>
</tr>
<tr>
<td align="right">5</td>
<td align="right">2020</td>
<td align="right">Bam Adebayo</td>
<td align="right">0.0589134</td>
<td align="right">0.0589134</td>
<td align="right">0.0640164</td>
<td align="right">0.599966</td>
<td align="right">21996</td>
<td align="right">84859</td>
<td align="right">93866</td>
<td align="right">1</td>
</tr>
<tr>
<td align="right">6</td>
<td align="right">2020</td>
<td align="right">Ben Simmons</td>
<td align="right">0.0598212</td>
<td align="right">0.0598212</td>
<td align="right">0.196928</td>
<td align="right">0.552685</td>
<td align="right">16923</td>
<td align="right">65297.2</td>
<td align="right">72214.3</td>
<td align="right">13</td>
</tr>
<tr>
<td align="right">7</td>
<td align="right">2020</td>
<td align="right">Bradley Beal</td>
<td align="right">0.0754871</td>
<td align="right">0.0754871</td>
<td align="right">0.102333</td>
<td align="right">0.557063</td>
<td align="right">11668.2</td>
<td align="right">36245.4</td>
<td align="right">45089</td>
<td align="right">50</td>
</tr>
<tr>
<td align="right">8</td>
<td align="right">2020</td>
<td align="right">Brandon Ingram</td>
<td align="right">0.0879199</td>
<td align="right">0.0879199</td>
<td align="right">0.0901602</td>
<td align="right">0.544744</td>
<td align="right">15613.1</td>
<td align="right">50384.1</td>
<td align="right">56001</td>
<td align="right">27</td>
</tr>
<tr>
<td align="right">9</td>
<td align="right">2020</td>
<td align="left">Buddy Hield</td>
<td align="right">0.0858989</td>
<td align="right">0.0858989</td>
<td align="right">0.0941537</td>
<td align="right">0.554056</td>
<td align="right">23624.3</td>
<td align="right">49410.2</td>
<td align="right">60888.5</td>
<td align="right">26</td>
</tr>
<tr>
<td align="right">10</td>
<td align="right">2020</td>
<td align="right">CJ McCollum</td>
<td align="right">0.0737269</td>
<td align="right">0.0737269</td>
<td align="right">0.276422</td>
<td align="right">0.557982</td>
<td align="right">14814.5</td>
<td align="right">70731</td>
<td align="right">70641.2</td>
<td align="right">6</td>
</tr>
</tbody></table>

</details>

<details>
<summary><strong>Quantified BBC Sports News - Sentiments and Relevance</strong></summary>
(Taking the 2010-2023 season from the merged table, the top 10 samples) 

<table>
<thead>
<tr>
<th align="right"></th>
<th align="right">time</th>
<th align="right">most_frequent_name</th>
<th align="right">textblob_sentiment</th>
<th align="right">sentiment_bert_average_score</th>
<th align="right">sentiment_xlnet_average_score</th>
<th align="right">bert_relevance</th>
<th align="right">relevance_score</th>
<th align="right">frequency</th>
</tr>
</thead>
<tbody><tr>
<td align="right">0</td>
<td align="right">2023</td>
<td align="right">Aaron Gordon</td>
<td align="right">0.107826</td>
<td align="right">0.580768</td>
<td align="right">0.569642</td>
<td align="right">0.592284</td>
<td align="right">0.00804037</td>
<td align="right">22</td>
</tr>
<tr>
<td align="right">1</td>
<td align="right">2023</td>
<td align="right">Al Horford</td>
<td align="right">0.0902433</td>
<td align="right">0.560702</td>
<td align="right">0.602442</td>
<td align="right">0.588029</td>
<td align="right">0.00175832</td>
<td align="right">2</td>
</tr>
<tr>
<td align="right">2</td>
<td align="right">2023</td>
<td align="right">Andrew Wiggins</td>
<td align="right">0.141368</td>
<td align="right">0.597014</td>
<td align="right">0.580687</td>
<td align="right">0.587998</td>
<td align="right">0.0106417</td>
<td align="right">8</td>
</tr>
<tr>
<td align="right">3</td>
<td align="right">2023</td>
<td align="right">Anfernee Simons</td>
<td align="right">0.109778</td>
<td align="right">0.557983</td>
<td align="right">0.569789</td>
<td align="right">0.593048</td>
<td align="right">0.0138669</td>
<td align="right">2</td>
</tr>
<tr>
<td align="right">4</td>
<td align="right">2023</td>
<td align="right">Anthony Davis</td>
<td align="right">0.102784</td>
<td align="right">0.592395</td>
<td align="right">0.570054</td>
<td align="right">0.587705</td>
<td align="right">0.0162172</td>
<td align="right">22</td>
</tr>
<tr>
<td align="right">5</td>
<td align="right">2023</td>
<td align="right">Anthony Edwards</td>
<td align="right">0.0561825</td>
<td align="right">0.602159</td>
<td align="right">0.6101</td>
<td align="right">0.590135</td>
<td align="right">0.0545278</td>
<td align="right">14</td>
</tr>
<tr>
<td align="right">6</td>
<td align="right">2023</td>
<td align="right">Bam Adebayo</td>
<td align="right">0.192308</td>
<td align="right">0.513591</td>
<td align="right">0.590492</td>
<td align="right">0.597262</td>
<td align="right">0.00980593</td>
<td align="right">1</td>
</tr>
<tr>
<td align="right">7</td>
<td align="right">2023</td>
<td align="right">Bojan Bogdanović</td>
<td align="right">0.138098</td>
<td align="right">0.577742</td>
<td align="right">0.575943</td>
<td align="right">0.59157</td>
<td align="right">0.00184185</td>
<td align="right">2</td>
</tr>
<tr>
<td align="right">8</td>
<td align="right">2023</td>
<td align="right">Bradley Beal</td>
<td align="right">0.122245</td>
<td align="right">0.584892</td>
<td align="right">0.581959</td>
<td align="right">0.58885</td>
<td align="right">0.0030606</td>
<td align="right">1</td>
</tr>
<tr>
<td align="right">9</td>
<td align="right">2023</td>
<td align="right">Brandon Ingram</td>
<td align="right">0.0912451</td>
<td align="right">0.608591</td>
<td align="right">0.591863</td>
<td align="right">0.576785</td>
<td align="right">0.00785333</td>
<td align="right">5</td>
</tr>
</tbody></table>

</details>

<details>
<summary><strong>MVP Count</strong> (<a href="https://github.com/tz1211/DS105L-Project-404-Not-Found/blob/main/Data/final_cleaned_data/MVP_count.csv">MVP_count.csv</a>)</summary>
Sample MVP count for Stephen Curry  

<table align="right">
<thead>
<tr>
<th>Name</th>
<th>Year</th>
<th>value</th>
<th>won_last_yr</th>
<th>won_2_yrs_before</th>
</tr>
</thead>
<tbody><tr>
<td>Stephen Curry</td>
<td>2023</td>
<td>2</td>
<td>0</td>
<td>0</td>
</tr>
<tr>
<td>Stephen Curry</td>
<td>2022</td>
<td>2</td>
<td>0</td>
<td>0</td>
</tr>
<tr>
<td>Stephen Curry</td>
<td>2021</td>
<td>2</td>
<td>0</td>
<td>0</td>
</tr>
<tr>
<td>Stephen Curry</td>
<td>2020</td>
<td>2</td>
<td>0</td>
<td>0</td>
</tr>
<tr>
<td>Stephen Curry</td>
<td>2019</td>
<td>2</td>
<td>0</td>
<td>0</td>
</tr>
<tr>
<td>Stephen Curry</td>
<td>2018</td>
<td>2</td>
<td>0</td>
<td>1</td>
</tr>
<tr>
<td>Stephen Curry</td>
<td>2017</td>
<td>2</td>
<td>1</td>
<td>1</td>
</tr>
<tr>
<td>Stephen Curry</td>
<td>2016</td>
<td>1</td>
<td>1</td>
<td>0</td>
</tr>
<tr>
<td>Stephen Curry</td>
<td>2015</td>
<td>0</td>
<td>0</td>
<td>0</td>
</tr>
<tr>
<td>Stephen Curry</td>
<td>2014</td>
<td>0</td>
<td>0</td>
<td>0</td>
</tr>
<tr>
<td>Stephen Curry</td>
<td>2013</td>
<td>0</td>
<td>0</td>
<td>0</td>
</tr>
<tr>
<td>Stephen Curry</td>
<td>2012</td>
<td>0</td>
<td>0</td>
<td>0</td>
</tr>
<tr>
<td>Stephen Curry</td>
<td>2011</td>
<td>0</td>
<td>0</td>
<td>0</td>
</tr>
<tr>
<td>Stephen Curry</td>
<td>2010</td>
<td>0</td>
<td>0</td>
<td>0</td>
</tr>
<tr>
<td>Stephen Curry</td>
<td>2009</td>
<td>0</td>
<td>0</td>
<td>0</td>
</tr>
<tr>
<td>Stephen Curry</td>
<td>2008</td>
<td>0</td>
<td>0</td>
<td>0</td>
</tr>
</tbody></table>

`MVP_count.csv` is designed to capture the number of time a player have won MVP and whether he has won it the previous year or previous 2 years. It is generally agreed upon that players who win their first MVP the previous year tend to win another MVP, whilst players who have won MVP 2 years in a row are highly unlikely to win a third one (sometimes termed "voter fatigue"). This dataset is designed to capture the aspect of "voter fatigue". 
</details>

## Final Merged Data 

### Historical data from 2010-2022 season ([final_cleaned_data.csv](https://github.com/tz1211/DS105L-Project-404-Not-Found/blob/main/Data/final_cleaned_data.csv)) 

<table align="right">
<thead>
<tr>
<th></th>
<th>season</th>
<th>slug</th>
<th>name</th>
<th>team</th>
<th>age</th>
<th>%games_played</th>
<th>minutes_played</th>
<th>points</th>
<th>assists</th>
<th>attempted_field_goals</th>
<th>attempted_free_throws</th>
<th>attempted_three_point_field_goals</th>
<th>blocks</th>
<th>defensive_rebounds</th>
<th>games_started</th>
<th>made_field_goals</th>
<th>made_free_throws</th>
<th>made_three_point_field_goals</th>
<th>offensive_rebounds</th>
<th>personal_fouls</th>
<th>steals</th>
<th>turnovers</th>
<th>field_goal%</th>
<th>free_throw%</th>
<th>3pt%</th>
<th>assist_percentage</th>
<th>block_percentage</th>
<th>box_plus_minus</th>
<th>defensive_box_plus_minus</th>
<th>defensive_rebound_percentage</th>
<th>free_throw_attempt_rate</th>
<th>offensive_box_plus_minus</th>
<th>offensive_rebound_percentage</th>
<th>player_efficiency_rating</th>
<th>steal_percentage</th>
<th>three_point_attempt_rate</th>
<th>total_rebound_percentage</th>
<th>true_shooting_percentage</th>
<th>turnover_percentage</th>
<th>usage_percentage</th>
<th>value_over_replacement_player</th>
<th>win_shares_per_48_minutes</th>
<th>win_rate</th>
<th>conference_standing</th>
<th>num_mvp</th>
<th>won_last_yr</th>
<th>won_2_yrs_before</th>
<th>textblob_sentiment</th>
<th>sentiment_bert_average_score</th>
<th>sentiment_xlnet_average_score</th>
<th>bert_relevance</th>
<th>relevance_score</th>
<th>frequency</th>
<th>is_mvp</th>
</tr>
</thead>
<tbody><tr>
<td>0</td>
<td>2010</td>
<td>aldrila01</td>
<td>LaMarcus Aldridge</td>
<td>PORTLAND TRAIL BLAZERS</td>
<td>24</td>
<td>0.951219512195122</td>
<td>37.46153846153846</td>
<td>17.858974358974358</td>
<td>2.051282051282051</td>
<td>14.987179487179487</td>
<td>3.897435897435898</td>
<td>0.2051282051282051</td>
<td>0.6153846153846154</td>
<td>5.576923076923077</td>
<td>1.0</td>
<td>7.423076923076923</td>
<td>2.948717948717949</td>
<td>0.0641025641025641</td>
<td>2.4615384615384617</td>
<td>2.9615384615384617</td>
<td>0.8589743589743589</td>
<td>1.3333333333333333</td>
<td>0.495295124037639</td>
<td>0.7565789473684211</td>
<td>0.3125</td>
<td>9.9</td>
<td>1.3</td>
<td>1.2</td>
<td>-0.2</td>
<td>18.6</td>
<td>0.26</td>
<td>1.4</td>
<td>8.1</td>
<td>18.2</td>
<td>1.3</td>
<td>0.014</td>
<td>13.3</td>
<td>0.535</td>
<td>7.4</td>
<td>22.9</td>
<td>2.3</td>
<td>0.145</td>
<td>0.6097560975609756</td>
<td>6</td>
<td>0</td>
<td>0</td>
<td>0</td>
<td>0.0</td>
<td>0.0</td>
<td>0.0</td>
<td>0.0</td>
<td>0.0</td>
<td>0</td>
<td>0</td>
</tr>
<tr>
<td>1</td>
<td>2010</td>
<td>allenra02</td>
<td>Ray Allen</td>
<td>BOSTON CELTICS</td>
<td>34</td>
<td>0.975609756097561</td>
<td>35.2375</td>
<td>16.3</td>
<td>2.625</td>
<td>12.1625</td>
<td>3.1625</td>
<td>4.9875</td>
<td>0.3125</td>
<td>2.6</td>
<td>1.0</td>
<td>5.8</td>
<td>2.8875</td>
<td>1.8125</td>
<td>0.5625</td>
<td>2.275</td>
<td>0.8</td>
<td>1.6125</td>
<td>0.4768756423432682</td>
<td>0.9130434782608696</td>
<td>0.3634085213032582</td>
<td>12.3</td>
<td>0.7</td>
<td>1.2</td>
<td>-0.3</td>
<td>8.8</td>
<td>0.26</td>
<td>1.5</td>
<td>2.0</td>
<td>15.2</td>
<td>1.2</td>
<td>0.41</td>
<td>5.5</td>
<td>0.601</td>
<td>10.6</td>
<td>20.2</td>
<td>2.3</td>
<td>0.135</td>
<td>0.6097560975609756</td>
<td>4</td>
<td>0</td>
<td>0</td>
<td>0</td>
<td>0.046541415714644</td>
<td>0.5710958358314302</td>
<td>0.5737237615717782</td>
<td>0.5190211534500122</td>
<td>0.0038996330971015</td>
<td>4</td>
<td>0</td>
</tr>
<tr>
<td>2</td>
<td>2010</td>
<td>anthoca01</td>
<td>Carmelo Anthony</td>
<td>DENVER NUGGETS</td>
<td>25</td>
<td>0.8414634146341463</td>
<td>38.17391304347826</td>
<td>28.159420289855078</td>
<td>3.217391304347826</td>
<td>21.768115942028984</td>
<td>8.869565217391305</td>
<td>2.710144927536232</td>
<td>0.4347826086956521</td>
<td>4.376811594202898</td>
<td>1.0</td>
<td>9.971014492753625</td>
<td>7.36231884057971</td>
<td>0.855072463768116</td>
<td>2.2028985507246377</td>
<td>3.260869565217391</td>
<td>1.2753623188405796</td>
<td>3.028985507246377</td>
<td>0.4580559254327563</td>
<td>0.8300653594771241</td>
<td>0.3155080213903743</td>
<td>15.9</td>
<td>0.9</td>
<td>2.3</td>
<td>-1.2</td>
<td>13.1</td>
<td>0.407</td>
<td>3.5</td>
<td>6.7</td>
<td>22.2</td>
<td>1.7</td>
<td>0.125</td>
<td>9.9</td>
<td>0.548</td>
<td>10.6</td>
<td>33.4</td>
<td>2.9</td>
<td>0.145</td>
<td>0.6463414634146342</td>
<td>4</td>
<td>0</td>
<td>0</td>
<td>0</td>
<td>0.0659319821592549</td>
<td>0.5807402985436576</td>
<td>0.576524725982121</td>
<td>0.531563937664032</td>
<td>0.0585006792499055</td>
<td>5</td>
<td>0</td>
</tr>
<tr>
<td>3</td>
<td>2010</td>
<td>arenagi01</td>
<td>Gilbert Arenas</td>
<td>WASHINGTON WIZARDS</td>
<td>28</td>
<td>0.3902439024390244</td>
<td>36.53125</td>
<td>22.5625</td>
<td>7.1875</td>
<td>19.25</td>
<td>6.46875</td>
<td>5.65625</td>
<td>0.28125</td>
<td>3.625</td>
<td>1.0</td>
<td>7.90625</td>
<td>4.78125</td>
<td>1.96875</td>
<td>0.53125</td>
<td>2.96875</td>
<td>1.28125</td>
<td>3.65625</td>
<td>0.4107142857142857</td>
<td>0.7391304347826086</td>
<td>0.3480662983425414</td>
<td>36.3</td>
<td>0.6</td>
<td>1.7</td>
<td>-1.2</td>
<td>11.6</td>
<td>0.336</td>
<td>2.9</td>
<td>1.6</td>
<td>18.7</td>
<td>1.8</td>
<td>0.294</td>
<td>6.5</td>
<td>0.511</td>
<td>14.2</td>
<td>31.9</td>
<td>1.1</td>
<td>0.072</td>
<td>0.3170731707317073</td>
<td>14</td>
<td>0</td>
<td>0</td>
<td>0</td>
<td>0.132288557912325</td>
<td>0.6023474167263697</td>
<td>0.5754024456890803</td>
<td>0.523616373538971</td>
<td>0.0043846670048157</td>
<td>6</td>
<td>0</td>
</tr>
<tr>
<td>4</td>
<td>2010</td>
<td>arizatr01</td>
<td>Trevor Ariza</td>
<td>HOUSTON ROCKETS</td>
<td>24</td>
<td>0.8780487804878049</td>
<td>36.513888888888886</td>
<td>14.88888888888889</td>
<td>3.8333333333333335</td>
<td>13.875</td>
<td>3.1666666666666665</td>
<td>5.652777777777778</td>
<td>0.5555555555555556</td>
<td>4.513888888888889</td>
<td>0.9861111111111112</td>
<td>5.472222222222222</td>
<td>2.055555555555556</td>
<td>1.8888888888888888</td>
<td>1.0833333333333333</td>
<td>2.25</td>
<td>1.75</td>
<td>2.236111111111111</td>
<td>0.3943943943943944</td>
<td>0.6491228070175439</td>
<td>0.3341523341523341</td>
<td>16.7</td>
<td>1.1</td>
<td>0.5</td>
<td>0.9</td>
<td>14.7</td>
<td>0.228</td>
<td>-0.4</td>
<td>3.3</td>
<td>13.3</td>
<td>2.4</td>
<td>0.407</td>
<td>8.8</td>
<td>0.488</td>
<td>12.8</td>
<td>21.2</td>
<td>1.7</td>
<td>0.058</td>
<td>0.5121951219512195</td>
<td>9</td>
<td>0</td>
<td>0</td>
<td>0</td>
<td>0.0</td>
<td>0.0</td>
<td>0.0</td>
<td>0.0</td>
<td>0.0</td>
<td>0</td>
<td>0</td>
</tr>
<tr>
<td>5</td>
<td>2010</td>
<td>artesro01</td>
<td>Metta World Peace</td>
<td>LOS ANGELES LAKERS</td>
<td>30</td>
<td>0.9390243902439024</td>
<td>33.83116883116883</td>
<td>10.974025974025974</td>
<td>3.038961038961039</td>
<td>9.61038961038961</td>
<td>2.415584415584416</td>
<td>3.844155844155844</td>
<td>0.2727272727272727</td>
<td>3.012987012987013</td>
<td>1.0</td>
<td>3.9740259740259742</td>
<td>1.6623376623376624</td>
<td>1.3636363636363635</td>
<td>1.2857142857142858</td>
<td>2.142857142857143</td>
<td>1.3766233766233766</td>
<td>1.5714285714285714</td>
<td>0.4135135135135135</td>
<td>0.6881720430107527</td>
<td>0.3547297297297297</td>
<td>13.3</td>
<td>0.6</td>
<td>0.5</td>
<td>1.1</td>
<td>9.9</td>
<td>0.251</td>
<td>-0.6</td>
<td>4.3</td>
<td>12.1</td>
<td>2.1</td>
<td>0.4</td>
<td>7.1</td>
<td>0.514</td>
<td>12.8</td>
<td>16.2</td>
<td>1.6</td>
<td>0.098</td>
<td>0.6951219512195121</td>
<td>1</td>
<td>0</td>
<td>0</td>
<td>0</td>
<td>0.0</td>
<td>0.0</td>
<td>0.0</td>
<td>0.0</td>
<td>0.0</td>
<td>0</td>
<td>0</td>
</tr>
<tr>
<td>6</td>
<td>2010</td>
<td>bargnan01</td>
<td>Andrea Bargnani</td>
<td>TORONTO RAPTORS</td>
<td>24</td>
<td>0.975609756097561</td>
<td>34.9875</td>
<td>17.2</td>
<td>1.1625</td>
<td>14.2875</td>
<td>2.925</td>
<td>4.0625</td>
<td>1.3875</td>
<td>4.85</td>
<td>1.0</td>
<td>6.7125</td>
<td>2.2625</td>
<td>1.5125</td>
<td>1.3125</td>
<td>2.6875</td>
<td>0.3125</td>
<td>1.5</td>
<td>0.4698162729658793</td>
<td>0.7735042735042736</td>
<td>0.3723076923076923</td>
<td>5.4</td>
<td>3.0</td>
<td>-0.8</td>
<td>-1.7</td>
<td>15.9</td>
<td>0.205</td>
<td>0.9</td>
<td>4.6</td>
<td>15.5</td>
<td>0.5</td>
<td>0.284</td>
<td>10.4</td>
<td>0.552</td>
<td>8.8</td>
<td>22.3</td>
<td>0.9</td>
<td>0.072</td>
<td>0.4878048780487805</td>
<td>9</td>
<td>0</td>
<td>0</td>
<td>0</td>
<td>0.2366198865733748</td>
<td>0.5677419097527213</td>
<td>0.5666976000951685</td>
<td>0.5314929485321045</td>
<td>0.0018285459338642</td>
<td>1</td>
<td>0</td>
</tr>
<tr>
<td>7</td>
<td>2010</td>
<td>barroea01</td>
<td>Earl Barron</td>
<td>NEW YORK KNICKS</td>
<td>28</td>
<td>0.0853658536585365</td>
<td>33.142857142857146</td>
<td>11.714285714285714</td>
<td>1.1428571428571428</td>
<td>9.714285714285714</td>
<td>4.142857142857143</td>
<td>0.0</td>
<td>0.5714285714285714</td>
<td>6.571428571428571</td>
<td>0.8571428571428571</td>
<td>4.285714285714286</td>
<td>3.142857142857143</td>
<td>0.0</td>
<td>4.428571428571429</td>
<td>3.4285714285714284</td>
<td>0.5714285714285714</td>
<td>1.5714285714285714</td>
<td>0.4411764705882353</td>
<td>0.7586206896551724</td>
<td>0.0</td>
<td>5.2</td>
<td>1.3</td>
<td>-4.5</td>
<td>-2.9</td>
<td>22.9</td>
<td>0.426</td>
<td>-1.5</td>
<td>14.9</td>
<td>14.7</td>
<td>0.9</td>
<td>0.0</td>
<td>18.9</td>
<td>0.508</td>
<td>12.0</td>
<td>17.9</td>
<td>-0.1</td>
<td>0.091</td>
<td>0.3536585365853658</td>
<td>11</td>
<td>0</td>
<td>0</td>
<td>0</td>
<td>0.2366198865733748</td>
<td>0.5935538048329561</td>
<td>0.5683303993681202</td>
<td>0.513433039188385</td>
<td>0.0018285459338642</td>
<td>1</td>
<td>0</td>
</tr>
<tr>
<td>8</td>
<td>2010</td>
<td>battish01</td>
<td>Shane Battier</td>
<td>HOUSTON ROCKETS</td>
<td>31</td>
<td>0.8170731707317073</td>
<td>32.35820895522388</td>
<td>7.970149253731344</td>
<td>2.4477611940298507</td>
<td>6.6716417910447765</td>
<td>1.582089552238806</td>
<td>4.164179104477612</td>
<td>1.1343283582089552</td>
<td>3.5522388059701493</td>
<td>0.9253731343283582</td>
<td>2.656716417910448</td>
<td>1.1492537313432836</td>
<td>1.507462686567164</td>
<td>1.1044776119402986</td>
<td>2.074626865671642</td>
<td>0.7910447761194029</td>
<td>0.9552238805970148</td>
<td>0.3982102908277405</td>
<td>0.7264150943396227</td>
<td>0.3620071684587813</td>
<td>10.9</td>
<td>2.6</td>
<td>1.5</td>
<td>1.4</td>
<td>13.1</td>
<td>0.237</td>
<td>0.1</td>
<td>3.8</td>
<td>11.1</td>
<td>1.2</td>
<td>0.624</td>
<td>8.2</td>
<td>0.541</td>
<td>11.5</td>
<td>11.4</td>
<td>1.9</td>
<td>0.095</td>
<td>0.5121951219512195</td>
<td>9</td>
<td>0</td>
<td>0</td>
<td>0</td>
<td>0.0</td>
<td>0.0</td>
<td>0.0</td>
<td>0.0</td>
<td>0.0</td>
<td>0</td>
<td>0</td>
</tr>
<tr>
<td>9</td>
<td>2010</td>
<td>bellra01</td>
<td>Raja Bell</td>
<td>CHARLOTTE BOBCATS</td>
<td>33</td>
<td>0.0609756097560975</td>
<td>31.4</td>
<td>12.0</td>
<td>2.0</td>
<td>11.0</td>
<td>0.6</td>
<td>4.8</td>
<td>0.4</td>
<td>3.2</td>
<td>1.0</td>
<td>4.8</td>
<td>0.6</td>
<td>1.8</td>
<td>1.0</td>
<td>2.6</td>
<td>0.8</td>
<td>1.0</td>
<td>0.4363636363636363</td>
<td>1.0</td>
<td>0.375</td>
<td>11.3</td>
<td>1.0</td>
<td>2.5</td>
<td>2.0</td>
<td>12.1</td>
<td>0.055</td>
<td>0.5</td>
<td>3.9</td>
<td>12.8</td>
<td>1.4</td>
<td>0.436</td>
<td>8.1</td>
<td>0.533</td>
<td>8.2</td>
<td>18.2</td>
<td>0.2</td>
<td>0.113</td>
<td>0.5365853658536586</td>
<td>7</td>
<td>0</td>
<td>0</td>
<td>0</td>
<td>0.2366198865733748</td>
<td>0.5702846050262451</td>
<td>0.5683994526448457</td>
<td>0.5285742878913879</td>
<td>0.0018285459338642</td>
<td>1</td>
<td>0</td>
</tr>
</tbody></table>

Full df shape: 1216 x 54
* Final dataframe with individual, team, and media narrative data all merged together 
* Used as training set for the Machine Learning algorithm (with column `is_mvp` acting as the label) 

### Merged data for 2023 season ([final_cleaned_data_2023.csv](https://github.com/tz1211/DS105L-Project-404-Not-Found/blob/main/Data/final_cleaned_data_2023.csv))

<table align="right">
<thead>
<tr>
<th></th>
<th>season</th>
<th>slug</th>
<th>name</th>
<th>team</th>
<th>age</th>
<th>%games_played</th>
<th>minutes_played</th>
<th>points</th>
<th>assists</th>
<th>attempted_field_goals</th>
<th>attempted_free_throws</th>
<th>attempted_three_point_field_goals</th>
<th>blocks</th>
<th>defensive_rebounds</th>
<th>games_started</th>
<th>made_field_goals</th>
<th>made_free_throws</th>
<th>made_three_point_field_goals</th>
<th>offensive_rebounds</th>
<th>personal_fouls</th>
<th>steals</th>
<th>turnovers</th>
<th>field_goal%</th>
<th>free_throw%</th>
<th>3pt%</th>
<th>assist_percentage</th>
<th>block_percentage</th>
<th>box_plus_minus</th>
<th>defensive_box_plus_minus</th>
<th>defensive_rebound_percentage</th>
<th>free_throw_attempt_rate</th>
<th>offensive_box_plus_minus</th>
<th>offensive_rebound_percentage</th>
<th>player_efficiency_rating</th>
<th>steal_percentage</th>
<th>three_point_attempt_rate</th>
<th>total_rebound_percentage</th>
<th>true_shooting_percentage</th>
<th>turnover_percentage</th>
<th>usage_percentage</th>
<th>value_over_replacement_player</th>
<th>win_shares_per_48_minutes</th>
<th>win_rate</th>
<th>conference_standing</th>
<th>num_mvp</th>
<th>won_last_yr</th>
<th>won_2_yrs_before</th>
<th>textblob_sentiment</th>
<th>sentiment_bert_average_score</th>
<th>sentiment_xlnet_average_score</th>
<th>bert_relevance</th>
<th>relevance_score</th>
<th>frequency</th>
</tr>
</thead>
<tbody><tr>
<td>0</td>
<td>2023</td>
<td>adebaba01</td>
<td>Bam Adebayo</td>
<td>MIAMI HEAT</td>
<td>25</td>
<td>0.918918918918919</td>
<td>35.13235294117647</td>
<td>21.058823529411764</td>
<td>3.2794117647058822</td>
<td>15.25</td>
<td>5.588235294117647</td>
<td>0.1764705882352941</td>
<td>0.8676470588235294</td>
<td>6.926470588235294</td>
<td>1.0</td>
<td>8.279411764705882</td>
<td>4.485294117647059</td>
<td>0.0147058823529411</td>
<td>2.426470588235294</td>
<td>2.867647058823529</td>
<td>1.1911764705882353</td>
<td>2.588235294117647</td>
<td>0.5429122468659595</td>
<td>0.8026315789473685</td>
<td>0.0833333333333333</td>
<td>16.4</td>
<td>2.5</td>
<td>1.8</td>
<td>0.9</td>
<td>23.9</td>
<td>0.366</td>
<td>0.9</td>
<td>7.8</td>
<td>20.4</td>
<td>1.7</td>
<td>0.012</td>
<td>15.5</td>
<td>0.595</td>
<td>12.8</td>
<td>25.5</td>
<td>2.3</td>
<td>0.142</td>
<td>0.5342465753424658</td>
<td>7</td>
<td>0</td>
<td>0</td>
<td>0</td>
<td>0.1923076923076923</td>
<td>0.5135908424854279</td>
<td>0.5904920101165771</td>
<td>0.5972620844841003</td>
<td>0.00980592516144</td>
<td>1</td>
</tr>
<tr>
<td>1</td>
<td>2023</td>
<td>allenja01</td>
<td>Jarrett Allen</td>
<td>CLEVELAND CAVALIERS</td>
<td>24</td>
<td>0.8378378378378378</td>
<td>33.03225806451613</td>
<td>14.35483870967742</td>
<td>1.6774193548387095</td>
<td>9.225806451612904</td>
<td>3.2580645161290325</td>
<td>0.1451612903225806</td>
<td>1.2096774193548387</td>
<td>6.693548387096774</td>
<td>1.0</td>
<td>5.983870967741935</td>
<td>2.370967741935484</td>
<td>0.0161290322580645</td>
<td>3.1129032258064515</td>
<td>2.2419354838709675</td>
<td>0.8225806451612904</td>
<td>1.403225806451613</td>
<td>0.6486013986013985</td>
<td>0.7277227722772277</td>
<td>0.1111111111111111</td>
<td>7.5</td>
<td>3.4</td>
<td>2.3</td>
<td>1.1</td>
<td>23.9</td>
<td>0.353</td>
<td>1.3</td>
<td>11.1</td>
<td>19.8</td>
<td>1.3</td>
<td>0.016</td>
<td>17.5</td>
<td>0.673</td>
<td>11.6</td>
<td>16.3</td>
<td>2.2</td>
<td>0.204</td>
<td>0.6164383561643836</td>
<td>4</td>
<td>0</td>
<td>0</td>
<td>0</td>
<td>0.1528338695853003</td>
<td>0.6097304433025151</td>
<td>0.5730694161542568</td>
<td>0.5885380506515503</td>
<td>0.0065960140888307</td>
<td>7</td>
</tr>
<tr>
<td>2</td>
<td>2023</td>
<td>antetgi01</td>
<td>Giannis Antetokounmpo</td>
<td>MILWAUKEE BUCKS</td>
<td>28</td>
<td>0.7777777777777778</td>
<td>32.5</td>
<td>31.25</td>
<td>5.571428571428571</td>
<td>20.392857142857142</td>
<td>12.625</td>
<td>2.7857142857142856</td>
<td>0.8035714285714286</td>
<td>9.607142857142858</td>
<td>1.0</td>
<td>11.125</td>
<td>8.196428571428571</td>
<td>0.8035714285714286</td>
<td>2.25</td>
<td>3.196428571428572</td>
<td>0.7321428571428571</td>
<td>3.9107142857142856</td>
<td>0.5455341506129597</td>
<td>0.6492220650636492</td>
<td>0.2884615384615385</td>
<td>32.3</td>
<td>2.0</td>
<td>8.2</td>
<td>2.6</td>
<td>29.5</td>
<td>0.619</td>
<td>5.6</td>
<td>7.5</td>
<td>28.6</td>
<td>1.1</td>
<td>0.137</td>
<td>18.9</td>
<td>0.602</td>
<td>13.1</td>
<td>38.7</td>
<td>4.7</td>
<td>0.204</td>
<td>0.7183098591549296</td>
<td>1</td>
<td>2</td>
<td>0</td>
<td>0</td>
<td>0.1511246958443137</td>
<td>0.5856197835898947</td>
<td>0.5833562986432821</td>
<td>0.5941260457038879</td>
<td>0.0251025381228857</td>
<td>29</td>
</tr>
<tr>
<td>3</td>
<td>2023</td>
<td>anunoog01</td>
<td>OG Anunoby</td>
<td>TORONTO RAPTORS</td>
<td>25</td>
<td>0.7945205479452054</td>
<td>35.724137931034484</td>
<td>16.775862068965516</td>
<td>1.896551724137931</td>
<td>13.10344827586207</td>
<td>2.7413793103448274</td>
<td>5.258620689655173</td>
<td>0.7241379310344828</td>
<td>3.655172413793104</td>
<td>1.0</td>
<td>6.224137931034483</td>
<td>2.293103448275862</td>
<td>2.034482758620689</td>
<td>1.4137931034482758</td>
<td>3.034482758620689</td>
<td>1.9655172413793105</td>
<td>2.155172413793104</td>
<td>0.475</td>
<td>0.8364779874213837</td>
<td>0.3868852459016393</td>
<td>7.7</td>
<td>2.0</td>
<td>0.1</td>
<td>0.7</td>
<td>12.5</td>
<td>0.209</td>
<td>-0.6</td>
<td>4.2</td>
<td>14.4</td>
<td>2.7</td>
<td>0.401</td>
<td>8.0</td>
<td>0.586</td>
<td>13.1</td>
<td>19.6</td>
<td>1.1</td>
<td>0.085</td>
<td>0.4861111111111111</td>
<td>9</td>
<td>0</td>
<td>0</td>
<td>0</td>
<td>0.0</td>
<td>0.0</td>
<td>0.0</td>
<td>0.0</td>
<td>0.0</td>
<td>0</td>
</tr>
<tr>
<td>4</td>
<td>2023</td>
<td>aytonde01</td>
<td>Deandre Ayton</td>
<td>PHOENIX SUNS</td>
<td>24</td>
<td>0.8472222222222222</td>
<td>30.442622950819672</td>
<td>18.311475409836067</td>
<td>1.819672131147541</td>
<td>13.557377049180328</td>
<td>2.9672131147540983</td>
<td>0.3934426229508196</td>
<td>0.7704918032786885</td>
<td>7.508196721311475</td>
<td>1.0</td>
<td>7.983606557377049</td>
<td>2.2295081967213117</td>
<td>0.1147540983606557</td>
<td>2.639344262295082</td>
<td>2.836065573770492</td>
<td>0.5573770491803278</td>
<td>1.819672131147541</td>
<td>0.5888754534461911</td>
<td>0.7513812154696132</td>
<td>0.2916666666666667</td>
<td>9.8</td>
<td>2.3</td>
<td>1.1</td>
<td>-0.1</td>
<td>28.0</td>
<td>0.219</td>
<td>1.2</td>
<td>9.5</td>
<td>20.3</td>
<td>0.9</td>
<td>0.029</td>
<td>18.5</td>
<td>0.616</td>
<td>10.9</td>
<td>23.4</td>
<td>1.5</td>
<td>0.15</td>
<td>0.5352112676056338</td>
<td>4</td>
<td>0</td>
<td>0</td>
<td>0</td>
<td>0.1912495627268354</td>
<td>0.5799142109023201</td>
<td>0.5558537509706286</td>
<td>0.5947425961494446</td>
<td>0.0145873656148506</td>
<td>3</td>
</tr>
<tr>
<td>5</td>
<td>2023</td>
<td>ballla01</td>
<td>LaMelo Ball</td>
<td>CHARLOTTE HORNETS</td>
<td>21</td>
<td>0.4931506849315068</td>
<td>35.22222222222222</td>
<td>23.27777777777778</td>
<td>8.444444444444445</td>
<td>20.02777777777778</td>
<td>3.388888888888889</td>
<td>10.63888888888889</td>
<td>0.3055555555555556</td>
<td>5.25</td>
<td>1.0</td>
<td>8.222222222222221</td>
<td>2.833333333333333</td>
<td>4.0</td>
<td>1.1666666666666667</td>
<td>3.2777777777777777</td>
<td>1.2777777777777777</td>
<td>3.583333333333333</td>
<td>0.4105409153952842</td>
<td>0.8360655737704918</td>
<td>0.3759791122715404</td>
<td>38.5</td>
<td>0.8</td>
<td>2.3</td>
<td>-0.9</td>
<td>16.3</td>
<td>0.169</td>
<td>3.2</td>
<td>3.4</td>
<td>18.0</td>
<td>1.7</td>
<td>0.531</td>
<td>9.7</td>
<td>0.541</td>
<td>14.3</td>
<td>29.9</td>
<td>1.4</td>
<td>0.07</td>
<td>0.3055555555555556</td>
<td>14</td>
<td>0</td>
<td>0</td>
<td>0</td>
<td>0.1414080785448697</td>
<td>0.5672962308853059</td>
<td>0.5853009911068591</td>
<td>0.57403165102005</td>
<td>0.0066773602960005</td>
<td>14</td>
</tr>
<tr>
<td>6</td>
<td>2023</td>
<td>banchpa01</td>
<td>Paolo Banchero</td>
<td>ORLANDO MAGIC</td>
<td>20</td>
<td>0.8904109589041096</td>
<td>33.84615384615385</td>
<td>19.984615384615385</td>
<td>3.615384615384616</td>
<td>15.738461538461538</td>
<td>7.4</td>
<td>4.030769230769231</td>
<td>0.5076923076923077</td>
<td>5.507692307692308</td>
<td>1.0</td>
<td>6.676923076923077</td>
<td>5.492307692307692</td>
<td>1.1384615384615384</td>
<td>1.123076923076923</td>
<td>2.246153846153846</td>
<td>0.8615384615384616</td>
<td>2.7384615384615385</td>
<td>0.4242424242424242</td>
<td>0.7422037422037422</td>
<td>0.282442748091603</td>
<td>16.6</td>
<td>1.4</td>
<td>-1.8</td>
<td>-0.9</td>
<td>18.6</td>
<td>0.47</td>
<td>-0.9</td>
<td>3.7</td>
<td>14.7</td>
<td>1.2</td>
<td>0.256</td>
<td>11.1</td>
<td>0.526</td>
<td>12.6</td>
<td>27.6</td>
<td>0.1</td>
<td>0.041</td>
<td>0.4027777777777778</td>
<td>13</td>
<td>0</td>
<td>0</td>
<td>0</td>
<td>0.2453216374269005</td>
<td>0.5700385173161825</td>
<td>0.5779234568277994</td>
<td>0.5979455709457397</td>
<td>0.0147364798689941</td>
<td>1</td>
</tr>
<tr>
<td>7</td>
<td>2023</td>
<td>banede01</td>
<td>Desmond Bane</td>
<td>MEMPHIS GRIZZLIES</td>
<td>24</td>
<td>0.6805555555555556</td>
<td>31.306122448979597</td>
<td>21.081632653061224</td>
<td>4.224489795918367</td>
<td>16.142857142857142</td>
<td>3.5510204081632653</td>
<td>6.959183673469388</td>
<td>0.3877551020408163</td>
<td>4.387755102040816</td>
<td>1.0</td>
<td>7.571428571428571</td>
<td>3.142857142857143</td>
<td>2.795918367346939</td>
<td>0.7142857142857143</td>
<td>2.489795918367347</td>
<td>0.9387755102040816</td>
<td>2.204081632653061</td>
<td>0.4690265486725664</td>
<td>0.8850574712643678</td>
<td>0.4017595307917889</td>
<td>20.5</td>
<td>1.1</td>
<td>3.2</td>
<td>0.2</td>
<td>14.8</td>
<td>0.22</td>
<td>3.0</td>
<td>2.4</td>
<td>18.7</td>
<td>1.4</td>
<td>0.431</td>
<td>8.6</td>
<td>0.595</td>
<td>11.1</td>
<td>26.3</td>
<td>2.0</td>
<td>0.145</td>
<td>0.6142857142857143</td>
<td>2</td>
<td>0</td>
<td>0</td>
<td>0</td>
<td>0.2637310606060606</td>
<td>0.5798526207605997</td>
<td>0.5645423928896586</td>
<td>0.5514346957206726</td>
<td>0.0135044907831952</td>
<td>1</td>
</tr>
<tr>
<td>8</td>
<td>2023</td>
<td>barneha02</td>
<td>Harrison Barnes</td>
<td>SACRAMENTO KINGS</td>
<td>30</td>
<td>0.9861111111111112</td>
<td>32.816901408450704</td>
<td>14.985915492957746</td>
<td>1.591549295774648</td>
<td>9.661971830985916</td>
<td>5.0</td>
<td>4.422535211267606</td>
<td>0.1408450704225352</td>
<td>3.704225352112676</td>
<td>1.0</td>
<td>4.549295774647887</td>
<td>4.23943661971831</td>
<td>1.647887323943662</td>
<td>0.971830985915493</td>
<td>1.3380281690140845</td>
<td>0.676056338028169</td>
<td>1.0845070422535212</td>
<td>0.4708454810495626</td>
<td>0.847887323943662</td>
<td>0.3726114649681528</td>
<td>6.4</td>
<td>0.4</td>
<td>-1.0</td>
<td>-1.5</td>
<td>12.8</td>
<td>0.517</td>
<td>0.4</td>
<td>3.4</td>
<td>13.9</td>
<td>1.0</td>
<td>0.458</td>
<td>8.2</td>
<td>0.632</td>
<td>8.4</td>
<td>16.9</td>
<td>0.6</td>
<td>0.114</td>
<td>0.6142857142857143</td>
<td>3</td>
<td>0</td>
<td>0</td>
<td>0</td>
<td>0.1073367736760593</td>
<td>0.5629069045186043</td>
<td>0.620891147851944</td>
<td>0.5879122018814087</td>
<td>0.007478692578949</td>
<td>5</td>
</tr>
<tr>
<td>9</td>
<td>2023</td>
<td>barnesc01</td>
<td>Scottie Barnes</td>
<td>TORONTO RAPTORS</td>
<td>21</td>
<td>0.9452054794520548</td>
<td>34.91304347826087</td>
<td>15.492753623188406</td>
<td>4.72463768115942</td>
<td>13.27536231884058</td>
<td>3.333333333333333</td>
<td>2.971014492753623</td>
<td>0.8115942028985508</td>
<td>4.463768115942029</td>
<td>0.9855072463768116</td>
<td>6.0144927536231885</td>
<td>2.579710144927536</td>
<td>0.8840579710144928</td>
<td>2.391304347826087</td>
<td>2.231884057971014</td>
<td>0.9855072463768116</td>
<td>2.028985507246377</td>
<td>0.4530567685589519</td>
<td>0.7739130434782608</td>
<td>0.2975609756097561</td>
<td>19.6</td>
<td>2.2</td>
<td>0.3</td>
<td>-0.3</td>
<td>15.7</td>
<td>0.251</td>
<td>0.6</td>
<td>7.2</td>
<td>15.5</td>
<td>1.4</td>
<td>0.224</td>
<td>11.1</td>
<td>0.525</td>
<td>12.1</td>
<td>20.5</td>
<td>1.4</td>
<td>0.087</td>
<td>0.4861111111111111</td>
<td>9</td>
<td>0</td>
<td>0</td>
<td>0</td>
<td>0.0</td>
<td>0.0</td>
<td>0.0</td>
<td>0.0</td>
<td>0.0</td>
<td>0</td>
</tr>
</tbody></table>

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


### 1️⃣ Credibility of NBA News
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

**Graph 2 Number of Followers**
  - The distribution is reasonably skewed, hence mean is used for missing values for authors.  
![images - 3](https://github.com/tz1211/DS105L-Project-404-Not-Found/blob/main/Data/news_data/github_MDtable/follower.png)

**Graph 3 Number of Tweets**
  - The distribution is reasonably skewed, hence mean is used for missing values for authors.  
![images - 4](https://github.com/tz1211/DS105L-Project-404-Not-Found/blob/main/Data/news_data/github_MDtable/tweets.png)



### 2️⃣ Sentiment and Relevance of NBA News

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


## 🧠 Random Forest Algorithm 



## 🖼️ Results

## 🖋️ Conclusions

## 📚 References

* [markdown file editting instruction](https://markdown.com.cn/cheat-sheet.html#%E6%80%BB%E8%A7%88)
* [Basketball reference api use instruction](https://jaebradley.github.io/basketball_reference_web_scraper/api/ )
* [Hugging Face](https://huggingface.co/)
* [Sentiment Analysis](https://www.analyticsvidhya.com/blog/2021/11/web-scraping-a-news-article-and-performing-sentiment-analysis-using-nlp/)
