
# 🏏T20 Cricket World Cup
 <img src="https://github.com/Mahalak4401/PowerBI_Portfolio_Projects/blob/main/T20%20Cricket%20World%20Cup/T20.gif" alt="An animated example GIF" style="width:750px; height:auto;">



## Problem Statement
To find out the best 11 cricket players based on the T20 world cup.

End-to-end sports data analytics project for your resume. In this project, we will cover web scraping (from the ESPN Cricinfo website), python, pandas, and Power BI to perform analyses on T20 world cup cricket data.

In this end-to-end data analytics project for beginners and advanced users, we have used cricket T20 world cup (2022) data to build insights on a best 11 players team that we can assemble from the earth that can go and play with aliens. We used bright data web scraping to collect data from espncricinfo website then we performed some data transformation and cleaning in pandas, followed by building dashboards in power bi. This is a solid data science resume project that will make your resume stand out in the competition. It is a fully guided data analytics project with all the materials included.

## Steps Involved in this Project

Steps involved in this project :

1. 📝Requirement Scoping

2. 🌐Data Collection using Web Scraping from ESPN Cricinfo website

3. 🧹Data Cleaning and Preprocessing in Pandas
4. 🔄Data Transformation in Power Query
5. ⚒️Data Modelling and Building Parameters in Power BI using DAX
6. 📊Building the Dashboard in Power BI

## Data Modelling

Connected all the datasets with based on some defined primary keys such as team and match ids. Also, created many measures, calculated columns and parameters for data analysis and dash boarding using DAX.
<br>
<div style="margin-bottom: 20px;">
  <img align="left" alt="Coding" width="750" height="350" src="https://github.com/Mahalak4401/PowerBI_Portfolio_Projects/blob/main/T20%20Cricket%20World%20Cup/T20%20Data%20Model.jpeg">
</div>

<br>
## Tools Used 

- Python : Web Scrapping, BeautifulSoup, Pandas, Juypter Notebook, Data Cleaning.
- Power BI : Dashboard, DAX, Calculated Columns, Data Cleaning, Data Modelling, Data Visualization.




## DAX Meaures
Measures used in visualization are:

Total Runs = SUM(t20_batting_summary[runs])

Total Innings Batted =COUNT(t20_batting_summary[matchID])

Total Innings Dismissed = SUM(t20_batting_summary[Out])

Batting Avg = DIVIDE([Total Runs],[Total Innings Dismissed],0)

Total balls faced =SUM(t20_batting_summary[balls])

Strike rate = DIVIDE([Total Runs],[total balls faced],0)*100

Batting Possition = ROUNDUP(AVERAGE(t20_batting_summary[battingPos]),0)

Boundary % = DIVIDE(SUM(t20_batting_summary[Boundary runs]),[Total Runs],0)*100

Avg. balls faced =  AVERAGE(t20_batting_summary[balls])

wickets = SUM(t20_bowling_summary[wickets])

Balls Bowled = SUM(t20_bowling_summary[balls])

Runs Conced = SUM(t20_bowling_summary[runs])

Economy = DIVIDE([Runs Conced],([Balls Bowled]/6),0)

Bowling Strike Rate =DIVIDE([Balls Bowled],[wickets],0)

Bowling Avrage = DIVIDE([Runs Conced],[wickets],0)

Total Innings Bowled = DISTINCTCOUNT(t20_bowling_summary[matchID])

Dot Ball % = DIVIDE(SUM(t20_bowling_summary[zeros]),SUM(t20_bowling_summary[balls]),0)

Player selection = if(ISFILTERED(t20_players_info[name]),"1","0")

Display Text = if([Player selection] = "1"," ","Select Player(s) by clicking the player's name to see their invidual or combined strength")

Color Callout Value =if([Player selection]="0","#E8D166","#1D1D2E")

boundary runs batting =t20_batting_summary[fours]*4 + t20_batting_summary[sixes]*6

boundary runs bowling =t20_bowling_summary[fours]*4+t20_bowling_summary[sixes]*6
