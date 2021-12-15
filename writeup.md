## **User conversion for chess.com**

### Ryan Solava

#### Abstract

Over the last year, chess and chess.com in particular has seen an influx of new users.
This is in large part due to the popular Netflix show Queen's Gambit, as well
as other cultural events involving chess. This is an opportunity for chess.com to
grow their userbase, which could eventually be leveraged for increased revenue.
To do this we propose a data science based solution.

The business motivation for the plan is described below. Then the data was
examined in Excel and Tableau to motivate the project, and demonstrate some
preliminary insights.


#### Design

**Opportunity:** There is an influx of new users, but not many become regular users. This is a chance to grow the service if we can convert more of them to regular users.

**Impact hypothesis:** By predicting if a new user is likely to convert to a regular user or not, we can apply interventions to increase conversion and grow the player base.

**Solution Path:** Using classification, we will use data from past games to predict
if a new user is likely to convert to a regular user. And from there apply interventions.
An algorithm such as a random tree classifier could be used.

**Criteria for success:** By using A/B testing, where we apply our model and interventions
to one set of users, but not another, we can see if our interventions increase new user conversion.

#### Data

The data is free available [here](https://database.lichess.org/) from Lichess. Ideally we would use data
from chess.com itself, but that was not available. A random sample of
1000 users from the years 2013-2014, and all of their games over that 2 year
period were used. This came to just under 100000 games.

For each game, the following features were included:

* Players name
* Colors
* Result
* Player ratings
* Opening
* Time control
* Date played

From this data about each game, additional information about the games and the users
themselves were found.

#### Algorithms

No major machine learning algorithms were used here. Pivot tables and vlookup were
used. A classification algorithm would eventually be good to apply to this problem,
perhaps a random forest classifier.

#### Tools

* **Python** was used in a minimal capacity to get a random sample of 1000 users
* **Excel** was the primary tool for analysis. It was used to create new columns
(including columns that related the user and game tables with vlookup) and summary
information with pivot tables
* **Tableau** was used to create interactive visuals

#### Communication

In addition to slides and presentation, two interactive Tableau dashboards display
the data [here](https://public.tableau.com/app/profile/ryan1488/viz/user_conversion/Dashboard1) and [here](https://public.tableau.com/app/profile/ryan1488/viz/chess_conversion/Convertingnewusers).
The spreadsheet and supporting files can be found on my [personal GitHub](https://github.com/rsolava/chess)
