# YouTube-Game-Hype
 web scrapping project that visualize and analyzes the relationship between YouTube views and a game's review score

“Is the Hype real?”

“Is the Hype real?” is a project that seeks to understand the relationship between the statistics associated with a game’s YouTube release video and how well it is received by the critic. It makes use of Beautiful Soup to retrieve information from both YouTube and GameSpot. The information is then compiled into a Pandas data frame, from where it can be analyzed extensively. 
The code is divided in three parts: (1) Web Scraping; (2) Data handling and; (3) Analysis. More specific information about the code can be found inside the Jupyter Notebook, where each piece of code is explained. The overall hypothesis is that games that have more views on YouTube are more likely to receive better scores by GameSpot and Metacritic . 
In the first part all the core functions are defined, and they range from functions that get URLs, functions that take these URLs and extract meaningful information from the website, to finally functions that wrap everything up into a Pandas DataFrame framework. Data Handling deals with the technical issues steaming from the fact that all data is returned as strings. So, it converts numbers to integers and dates do datetime format. It also removes missing data.
The most interesting part, and where more room for development lies, is the analysis part. Here I take advantage of Seaborn package, which is very useful for statistical data visualization. With it it is possible to explore how our variables are distributed. It is clear, for example, that Metacritic reviews tend to be more uniformly distributed then GameSpot ones. Some useful information can already be extracted, such as which game had the worst reviews and which game had the worst YouTube dislike ratio. 
We use joint plots to analyze the relationship between our main variables: views and review score. We could further use linear regression analysis from statsmodels package, but from the visualization we clearly see that there is no linear relationship between them two. Other relationships are explored, for example the impact of dislike ratio on review scores, but it also doesn’t show any relationship.
This suggests that small titles that don’t receive much attention from the public also get good grades. If we constrain the maximum number of views to 1 million we can see a more clear relationship, as demonstrated in the end of the analysis on the Jupyer Notebook.
One clear improvement that can be made to this code is for it to access a much larger pool of games to search. This, however, would require us to optimize the speed of the code, given that it already takes around 6 minutes to retrieve information about 50 games.



