# Web-Scraper - Transgender issues in The New York Times

## Description 

Visibility is key to understanding, acceptance, and ultimately, hopefully, equality.  I wanted to measure how transgender representation has evolved over the decades. So, I scraped The New York Times' archives, seeing them as a valid barometer for the cutural milieu.
  



## Table of Contents
* [Results](#Results)
* [Tools](#Tools)
* [Methodology](#Methodology)
* [Data-Cleaning](#Data-Cleaning)
* [Contact](#Contact)

  

## Results

![line graph](/images/nytimes_trans_graph.png)

Articles were few and far between for the 1980s and 1990s. With lesbian and gay issues coming more to the forefront in the 2000s, there was an small increase in transgender related articles. In 2014 and 2015 the number of articles rocketed, most likely due to the visibility of people like actress Laverne Cox and Caitlyn Jenner. The following years, issues such as trans women in sports became a heated topic covered by media.

![pie graph](/images/nytimes_pie_A.jpg)

In the past 20 years, Trans people's representation grew in sections such as Arts, Sports, and Life, indicating broader cultural visibility.


## Tools

Web-Scraper: Jupyter Notebook, BeautifulSoup, Splinter
Database:Pandas
Graphs: Matplotlib


## Methodology

The bot uses Chrome Driver to open New York Times and enter a specified search word between the given dates. This brings up anything that contains even a passing references the word 'transgender', so to ensure that the term is important to the article, the bot only pulls those that contain the word (or a related specified word) in the headline or subheader.

![jupyter_notebook_image](/images/j_notebook.png)

The bot pulls the headline, subheader, URL, date, and section for any given article that matches the requirement and stores it in a database.


## Data-Cleaning

Since the sections were quite broad and sometimes ambiguous, I categorized the sections into bins.

'Arts': ['Movies','Books','Book Review', 'Theater','Arts','Style','Television','Fashion', 'First Chapters','Theater Reviews','Art & Design','Dance','Media','Awards Season','Music','International Arts','Art','The Learning Network','DealBook','Fashion & Beauty','Food']
            
'US New': ['U.S.', 'New York', 'Connecticut', 'Americas','Education','Education Life','Politics','Elections']
            
'World News': ['World','Africa','Europe','Asia Pacific','Global Opinion','Middle East','Canada','Australia']

'Sports': ['Sports','Olympics','College Basketball','Soccer','Golf','N.B.A.', 'Baseball','Hockey','Tennis'],
'Life': ['Home & Garden','Travel','Your Money','Real Estate','Job Market','Smarter Living','Family','Retirement','Self-Care', 'Parenting','Love','Business'],
            
'Science':['Psychology','Science','Technology','Personal Tech','Mind','Climate','Health','Fertility'],
            
'Misc': ['The City','Magazine','Week in Review','Archives','Long Island','Sunday Review','Views','The Upshot','Times Insider', 'T Magazine','Booming','NYT Now', 'Giving','Live','The Daily', 'Today’s Paper','Lesson Plans','Lens','Briefing', 'Letters', 'Move', 'Well', 'Reader Center', 'Podcasts','Crosswords & Games', 'Opinion','Obituaries','Westchester']

As the language evolved over time, I further labeled articles with the term used: Transsexual, Transgender, Other (e.g., non-binary, transvestite, etc.)

![database](/images/ny_trans_db.png)

The application utilizes modularization by separating the GitHub API call and generation of the markdown into separate modules: `api.js` and `generateMarkdown.js`, respectively, inside the `utils` folder.

The application also utilizes, as much as possible, syntax and paradigms introduced in ES6 and beyond, including:

- Arrow functions, 
- `const`, `let`, 
- Template literals, and
- `async/await` to handle `inquirer`, `axios`, and `fs.writeFile` promises.


## Contact

Feel free to contact me with examples or any questions via the information below:

GitHub: [@julia-claira](https://api.github.com/users/julia-claira)

Email: julia-claira@gmail.com
