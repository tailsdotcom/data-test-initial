# Data Test: Round 1

Thank you for taking the time to complete our initial set of challenges. These are designed to help gauge your abilities on some of the core capabilities of the kind of work we do in our team - and help us to tailor the recruitment experience best to your current skill level. There are no "correct" answers to aim for, all of the problems are open to interpretation, and so feel free to take any approach you see fit to any of them.

Feel free to spend as much or as little time as you'd like, however bear in mind that the purpose of this is just to get a handle on your skill level and start a conversation so be pragmatic in how much time you spend. As a guidline, 20 minutes should be the most time it would be sensible to spend, and you may find you can answer some questions very quickly.

## Challenge 1: _Fetch_

Recently we surveyed some of the dogs in our office and threw a tennis ball, some of them chased it and some of them just rolled over. The results are in the graph below.

![Challenge Picture](https://github.com/tailsdotcom/data-test-initial/blob/master/180810-OnlineGraph.PNG "Chase % for Office Dog Breeds")

Our behavioural team want to understand what this graph shows. What can you conclude from the graph?

## Challenge 2: _Super secret treat_

Our food team has developed a new kind super secret treat which we think all of our dogs are going to love. What we don't know is whether it should be square or round. We sent some samples to a selection of our loyal subscribers and then offered them the opportunity to buy more. The results of that test are below.

| Month | # Dogs offered Square Treat | # Dogs who bought Square Treat  | # Dogs offered Round Treat | # Dogs who bought Round Treat  |
| ----- |:---------------------------:|:-------------------------------:|:--------------------------:|:------------------------------:|
| March | 100                         | 20                              | 150                        | 37
| April | 200                         | 38                              | 150                        | 0
| May   | 300                         | 55                              | 150                        | 39
| June  | 400                         | 75                              | 150                        | 41

Construct a visual (table, graphic or chart) of your chosing to interpret these results and suggest what we should conclude from the results.

## Challenge 3: _Rover the Labrador_

One of the database technologies we use is [MySQL](https://en.wikipedia.org/wiki/MySQL), and we quite often use [SQL](https://en.wikipedia.org/wiki/SQL) to get at the data we need to inform decisions across the business. Below is a query that we've been using but one of the dogs has been editing the code and now we're getting an error.

Rover the Labrador has been in touch about his food and said he prefers chicken to beef, and would like a chicken-based blend rather than his current beef-based one. We've been looking for all of our Labradors that are called Rover, to find out what blends they're on right now, but we're getting a syntax error. Can you correct the query so that it should work?

```sql
SELECT
  dog.dog_name,
  dog.breed,
  dog.signup_date,
  blend.flavour,
  MAX(blend.order_date) as most_recent_blend_date
FROM dog
INNER JOIN blend
  ON (blend.dog_id = dog.dog_id)
WHERE dog.dog_name = 'Rover' 
WHERE dog.breed = 'Labrador'
GROUP BY dog_name, breed, signup_date, flavour
```
Can you correct the query so that it works? For bonus points, can you sort the results by their "most recent blend date" so that dogs who've had a blend more recently appear at the top?
