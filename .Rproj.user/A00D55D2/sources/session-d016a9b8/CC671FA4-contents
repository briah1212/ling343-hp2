
# Board Games

The data this week comes from [Kaggle](https://www.kaggle.com/jvanelteren/boardgamegeek-reviews/version/3?select=2022-01-08.csv) by way of [Board Games Geek](https://www.boardgamegeek.com/), with a hattip to [David and Georgios ](https://github.com/rfordatascience/tidytuesday/issues/382#issuecomment-1020305849).

Note that the two datasets can be joined on the id column.

This data contains an overview of many games and their user ratings. There is even more data available on [kaggle](https://www.kaggle.com/jvanelteren/boardgamegeek-reviews/version/3?select=2022-01-08.csv) but it is too large for TidyTuesday (user text reviews data > 1 Gb, around 15-19 million reviews!)

Nice overview of the data:

In [Python](https://jvanelteren.github.io/blog/2022/01/19/boardgames.html) and in [R](https://theparttimeanalyst.com/2019/04/21/tidy-tuesday-board-games-xgboost-model/) and another [R](https://rpubs.com/thewiremonkey/476630).

### Get the data here

```{r}
# Get the Data

# Read in with tidytuesdayR package 
# Install from CRAN via: install.packages("tidytuesdayR")
# This loads the readme and all the datasets for the week of interest

# Either ISO-8601 date or year/week works!

tuesdata <- tidytuesdayR::tt_load('2022-01-25')
tuesdata <- tidytuesdayR::tt_load(2022, week = 4)

ratings <- tuesdata$ratings

# Or read in the data manually

ratings <- readr::read_csv('https://raw.githubusercontent.com/rfordatascience/tidytuesday/main/data/2022/2022-01-25/ratings.csv')
details <- readr::read_csv('https://raw.githubusercontent.com/rfordatascience/tidytuesday/main/data/2022/2022-01-25/details.csv')

```
### Data Dictionary

# `ratings.csv`

|variable      |class     |description |
|:-------------|:---------|:-----------|
|num           |double    | Game number |
|id            |double    | Game ID |
|name          |character | Game name |
|year          |double    | Game year |
|rank          |double    | Game rank |
|average       |double    | Average rating  |
|bayes_average |double    | Bayes average rating|
|users_rated   |double    | Users rated |
|url           |character | Game url |
|thumbnail     |character | Game thumbnail  |

# `details.csv`

|variable                |class     |description |
|:-----------------------|:---------|:-----------|
|num                     |double    | Game number |
|id                      |double    | Game ID |
|primary                 |character | Primary name  |
|description             |character | Description of game |
|yearpublished           |double    | Year published |
|minplayers              |double    | Min n of players|
|maxplayers              |double    | Max n of players |
|playingtime             |double    | Playing time in minutes |
|minplaytime             |double    | Min play time |
|maxplaytime             |double    | Max plat tome |
|minage                  |double    | minimum age|
|boardgamecategory       |character | Category |
|boardgamemechanic       |character | Mechanic   |
|boardgamefamily         |character | Board game family   |
|boardgameexpansion      |character | Expansion |
|boardgameimplementation |character | Implementation  |
|boardgamedesigner       |character | Designer |
|boardgameartist         |character | Artist  |
|boardgamepublisher      |character | Publisher     |
|owned                   |double    | Num owned  |
|trading                 |double    | Num trading  |
|wanting                 |double    | Num wanting |
|wishing                 |double    | Num wishing |



### Cleaning Script

