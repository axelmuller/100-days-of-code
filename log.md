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

### Day 6: 05/26/2020

*Today's Progress:* very limited mostly dealing with postgres + pandas memory issues

*Thoughts:* I might have to go back and write my postgres queries to csv files and read them in. For documentation purposes this should probably all be done through Python.


### Day 7: 05/27/2020

*Today's Progress:* I got pgadmin4 to work and created a player-centric table. 

*Thoughts:* Timezones, datetime64 are not that straight forward to handle with Bokeh. I will stick with Bokeh for plotting for a while now.

### Day 8: 05/28/2020

*Today's Progress:* not much, bogged down with timedelta and datetime64. Decided to make a new column with the correct type rather than changing the existing type

*Thoughts:* numpy and pandas can be great when dealing with time series but data needs to be of the right type. 

### Day 9: 05/29/2020

*Today's Progress:* i finally found a (clumsy) way to create an index with a timestamp and to change it's timezone. The issue was that grouping by hour in postgres yielded data of the type timedelta.

*Thoughts:* pandas has great tools to work with time series. however grouping by hours and a column yields a df with two indices. That in turn makes plotting with bokeh difficult.

### Day 10: 05/30/2020

*Today's Progress: More timeseries. Slowly getting the data in a shape I need to.

*Thoughts:* I need to apply what I learned to my data and think about what is needed to complete the project.


### Day 11: 05/31/2020

*Today's Progress:* Learned how to plot time series efficiently with pandas. 

*Thoughts:* Need to get my act together with Bokeh. Also decided on a couple of new projects: 1 pdb entries analyzing headers, resolution by year, method, location, synchrotron, protein class, ...
for text mining NIH reporter might offer something. 


### Day 12: 06/02/2020

*Today's Progress:* I finally plotted the relevant time series. In matplotlib and not in bokeh though. Also downloaded more data

*Thoughts:* or text mining NIH reporter might offer something. 

### Day 13: 06/04/2020

*Today's Progress:* Created my first dashboard with Panel and Altair

*Thoughts:* dashboards are cool but maybe not the easiest for sharing without a dedicated server

### Day 14: 06/08/2020

*Today's Progress:* started new project on pdb files. 

*Thoughts:* I initially planned to use grep to parse out relevant header information. While this would be a quick and dirty approach for some of the information I'm interested in it's probably not the best approach for learning how to do things properly. Hence, I decided to do the whole information extraction process in Python.

### Day 15: 06/08/2020

**Today's Progress:** setup neovim for Python and looked into TDD

**Thoughts:** Jupyter lab is great but for TDD it's a good idea to have multiple files open I prefer to do this in the terminal as it gives me more monitor real estate.


### Day 16: 06/09/2020

**Today's Progress:** getting the hang of unit tests

**Thoughts:** The PDB meta data project is much more ambitious then planned, I guess there is just so much cool data that waits to be extracted.


### Day 17: 06/10/2020

**Today's Progress:** finished writing all the functions to extract relevant information from pdb files and tested them

**Thoughts:** I have the feeling I should have tested my code first on extracting a limited number of features.

### Day 18: 06/11/2020

**Today's Progress:** sorted out how to extract all the information, need to figure out how to write it to a clean csv file

**Thoughts:** the process of parsing out the information seems to be reasonably straight forward. Using a template dictionary seems to be a good strategy for scenarios like that.


### Day 19: 06/12/2020

**Today's Progress:** added error handling, this hopefully takes care of the issues

**Thoughts:** when trying to extract data from large files or many files and it's unclear that there is a format enforced it seems to be a good idea to use error handling early on


### Day 20: 06/13/2020

**Today's Progress:** finally managed to process the pdb data and started some data exploration.

**Thoughts:** when processing user provided data it's dangerous to assume that the format will be coherent. 


### Day 21: 06/15/2020

**Today's Progress:** fixed the data error and beamline error. Other issues are due to poor data submitted by users. Also did the first semi useful plots.

**Thoughts:** need to tell a story and select the plots to support it
