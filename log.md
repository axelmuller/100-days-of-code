# 100 Days Of Code - Log

### Day 0: 05/19/2020

**Today's Progress**: I decided to join the 100 Days of Code today
I will try to spend most of the time working on data science projects 

**Thoughts:**  


**Link to work:** 

### Day 1: 05/20/2020

*Today's Progress*: I sorted out a bug in my header processing script and created a postgresql table to store the data in. I was also able to connect my postgres database to python using psycopg2

*Thoughts:* querying a 9GB dataframe with pandas is very slow, at least on my laptop. I hope postgresql will speed up the process.

### Day 2: 05/21/2020

*Today's Progress:* I created queries in postgres to yield new tables that I can use for my analysis in pandas. 

*Thoughts:* doing the aggregation in postgres is much quicker than in pandas. creating the white player table for 73 million games took just 5 minutes on my laptop.


### Day 3: 05/22/2020

*Today's Progress:* Not much needed to go back to postgres and do more queries.

*Thoughts:* I need to get better at SQL (among many other things)

### Day 4: 05/23/2020

*Today's Progress:* I found two errors that prevented me from capturing the titled data and I explored Bokeh, Seaborn, and Holoviews for plotting data

*Thoughts:* Resetting a dictionary requires a copy that acts independent of the original. Also pay attention of where to put resets of values when dealing with loops.

### Day 5: 05/24/2020

*Today's Progress:* I did Hugo's Covid19 tutorial, an altair tutorial, and a pandas tutorial. I spent some time trying to figure out how to load column values that are lists of ints into pandas. Unfortunately, my solutions didn't scale up.

*Thoughts:* Any data wrangling involving larger datasets seems to be better addressed in postgres. 

### Day 6: 05/25/2020

*Today's Progress:* I spent too much time again going back and forth with Pandas and Postgres. I planned to write out csv files of queries and load these into pandas to avoid running queries again and again. The problem I encountered was that I failed to find a satisfactory way to load column values that were postgres arrays into pandas as lists. The method I found didn't scale and crashed the kernel. So I went back to query from within python which circumvents the problem of reading unusual csv files. 

*Thoughts:* I should find out how to store views in postgres, especially when queried through python in order to avoid rerunning queries. 
