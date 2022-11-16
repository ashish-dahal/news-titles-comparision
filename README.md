
**News Comparison Analysis**



**Table of Contents**

=====================
[Introduction	4](#_Toc83583283)

[Data Collection	4](#_Toc83583284)

[Data Analysis	5](#_Toc83583285)

[Conclusion	7](#_Toc83583286)

























**Figures and Tables**


[Figure 1: Articles published in December 2019 and December 2020	5](E:\Google Drive\EDISS Courses\Data Science\Mini Project 1 - Report \(Ashish Dahal\).docx#_Toc83589851)

[Figure 2: Distribution of news title length	6](#_Toc83589852)

[Figure 3: Articles in Different Categories of December 2019 and  December 2020	6](E:\Google Drive\EDISS Courses\Data Science\Mini Project 1 - Report \(Ashish Dahal\).docx#_Toc83589853)











# **Introduction**
`	`In general, most people only go through news titles to get information while browsing the news websites. For this, the news websites try to make their title as self-explanatory as possible without reading the whole content. In the project, we analyze the news titles of an English-speaking online news agency during the first two weeks of December 2019 and December 2020. Essentially, we will try to find meaningful differences and/or similarities regarding the news titles between the time spans and formulate hypotheses on why it happened just based on the news titles and their category. 
# **Data Collection**
In every data science project, one needs to bear in mind various considerations regarding the data collection like the data itself and its source, method of collection etc., and plan accordingly.  For this project, the method of data collection was **web scraping**. And the tool chosen for web scraping was **Beautiful Soup 4 (bs4)** library. Also, several news websites were researched for the viability of the project and finally, the website (source) chosen for scraping was [The Wall Street Journal](https://www.wsj.com/news/archive/).

*Table 1: Data Collection Details*

| Choice |         | Reason for Choosing |
| :----: | :-----: | :-----------------: |
|        |         |                     |                                             |  |
|        | Method  |                     | Web Scraping                                |  | - As there are not many news websites that provide API’s for accessing the news data, web scraping was convenient, cheaper and easier                                                                                                                                                                                                                                                                                                                                      |
|        |         |                     |                                             |  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|        |  Tool   |                     | Beautiful Soup Library                      |  | <p>- It is faster, requires less effort to set up, and works best with static websites</p><p>- Has comprehensive documentation and has good community support </p>                                                                                                                                                                                                                                                                                                         |
|        |         |                     |                                             |  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|        | Website |                     | The wall street Journal                     |  | <p>- Reason considered:</p><p>&emsp;- The website has a news archive page </p><p>&emsp;- The website doesn’t load articles dynamically, hence less complex</p><p>&emsp;- The news articles of specific dates can be accessed through URL</p><p>&emsp;- Next pages in the article list of a particular date can be accessed through URL</p><p>&emsp;- The website has a consistent HTML structure and CSS classes</p><p>&emsp;- It has a category for each news article</p> |
|        |         |                     |                                             |  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|        |         |                     |                                             |  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|        |  Data   |                     | Article Title, Category, Author, Link, Date |
# **Data Analysis**
`	`The ‘matplotlib’ library was used to visualize the news data. A combination of visual charts was used to analyze the data like conventional bar charts, line charts, histograms. For more comprehensive analysis of the content of the news titles, a library called ‘wordcloud’ was used in order to visualize the most frequent words in the news titles in 2019 and 2020. 

`	`Some of the interesting observations during the analysis were as below:

1. **The news publication pattern:**

![](Aspose.Words.e2652a5b-3958-4b12-b577-7ec734a0feab.009.png)











*Figure 1: Articles published in December 2019 and December 2020*
![](Aspose.Words.e2652a5b-3958-4b12-b577-7ec734a0feab.010.png)


`	`The wall street journal had a regular pattern for publishing news. The pattern was repeatable and was similar with both years where the news published during the weekends plummeted and rose gradually during the weekdays in  a similar fashion.

1. **Normal Distribution of News Title Length**

![](Aspose.Words.e2652a5b-3958-4b12-b577-7ec734a0feab.011.png)

*Figure 2: Distribution of news title length*

The distribution of the length of news title by the wall street journal followed the normal distribution. The average number of characters in the title was 53.

1. **The interest of the viewers and news category differences**

*Figure 3: Articles in Different Categories of December 2019 and  December 2020*
![](Aspose.Words.e2652a5b-3958-4b12-b577-7ec734a0feab.012.png)![](Aspose.Words.e2652a5b-3958-4b12-b577-7ec734a0feab.013.png)













`	`It seems like the audience of wall street journal are more interested in business news and political news, as the number of articles in these categories is quite high compared to others.

`	`Also, the health category rapidly picked up pace in 2020 after the covid-19 pandemic.
# **Conclusion**
`	`Although the project was straightforward, some scientific bottlenecks posed a challenge during the data scraping phase. The challenges were related to the way the web server handled the HTTP requests, problems on the connections established with the webserver, balancing data vs overhead to get geta.

1. **HTTP requests**

There was some backend logic that prevented the HTTP requests without proper headers to access actual content and served irrelevant default content. It was solved by using proper user-agent headers on request.get() method.

1. **Limitations on connections**

The server was arbitrarily resetting the connection due to improper HTTP headers. It was also solved after passing proper headers.

1. **Getting data vs the overhead**

The author of the article was mentioned inside the article so the author had to be manually fetched from specific links of the article which added 29 minutes overhead to the scraping time. It was solved by passing N/A to the author values.

`	`However, all of the mentioned bottlenecks were solved and the analysis part followed seamlessly.
7
