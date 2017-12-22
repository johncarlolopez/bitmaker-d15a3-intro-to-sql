![Bitmaker](https://github.com/johncarlolopez/bitmaker-reference/blob/master/bitmakerlogo.svg)
# 03 - Intro to SQL Queries
### Friday, Dec 22nd
[See assignment in Alexa.](https://alexa.bitmaker.co/wdi/72/assignments/2244/latest)

![Tables](https://github.com/johncarlolopez/bitmaker-d15a3-intro-to-sql/blob/master/intro_sql_erd.png)

your task is to compose SQL queries for the following questions:

## My(John) answers are in ```code format```

Find all the robots from Star Wars.
```
SELECT * FROM robots WHERE source = 'Star Wars';
```
Find the robot with an "anxious" personality.
```
SELECT * FROM robots WHERE personality = 'anxious';
```
Find all recipes that are nut free.
```
SELECT * FROM recipes WHERE nut_free = true;
```
Count the number of recipes that are gluten free but not vegetarian.
```
SELECT COUNT(*) FROM recipes where gluten_free = true AND vegetarian = false;
```
Find the animal with the most legs.
```
SELECT * FROM animals WHERE number_of_legs = (SELECT MAX(number_of_legs) from animals);
```
Find the board game(s) that takes the least amount of time to play.
```
SELECT * FROM board_games WHERE mins_to_play = (SELECT MIN(mins_to_play) from board_games);
```
Find the recipe that takes the most time to prepare.
```
SELECT * FROM recipes WHERE minutes_required = (SELECT MIN(minutes_required) from recipes);
```
Find all the robots whose name starts with the letter M.
```
SELECT * FROM robots where name LIKE 'M%';
```
Count the number of board games that can be played by 8 people.
```
SELECT COUNT(*) FROM board_games WHERE min_players <= 8 AND max_players >= 8;
```
Find all animals that are swimming and egg-laying.
```
SELECT * FROM animals WHERE swimming = true AND egg_laying = true;
```
Find all animals that are swimming and egg-laying but not flying.
```
SELECT * FROM animals WHERE swimming = true AND egg_laying = true AND flying = false;
```
Find the board game that supports the largest number of people.
```
SELECT * FROM board_games WHERE max_players = (SELECT MAX(max_players) from board_games);
```
