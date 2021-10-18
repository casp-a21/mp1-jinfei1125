# Mini Project 1: The Sexist Job in 2021: Data Science

Author: Jinfei Zhu

# Research Question

I become interested in this topic because in a university-wide social event, in the self-introduction part, it looks like everyone's study interests have something related to data analysis, computer science, statistics, and machine learning, Python, R, so on and so on. Of course, I am one of them. Besides this, if you google 'the sexist job in 2021', you will surprisingly (or unsurprisingly?) find that the answer of top 10 search engine results is the same: data scientist (I created a quick snapshot of the search result as a small archive).

[](google-search-result.png)

So I begin to wonder, what's the time trend of the job of data scientist? Does more and more opportunities appear in the data science arear? Do the number of jobs available change evenly across the year, or is there any seasonal trend?  Will there be any annual trend too? For example, due to the pandemic, the job opportunity in 2020 could be less than usual, and 2008 - 2009 was greatly impacted by the Great Depression. Another possible question is When will these titles with new grad / summer intern comes out? 

## Construct my archive

To collect the data for new job openings, the first thing I can come up with is to scrape **LinkedIn**. LinkedIn has been trusted by both job seekers and companies, and has become a formal platform for people to connect. Many new jobs are posted every day and it has a filter to help us find out job positions within certain area and key words. To restrict my search result in a reasonable amount, I use this url to limit my craper result `https://www.linkedin.com/jobs/search/?keywords=data%20scientist&location=Chicago&position=1&pageNum=0`. This url will provide us with the opennings of data scientists in Chicago. The scraping codes can be found at two notebooks in this repository: 1 Static Web Scraping with Requests, and 2 Dynamic Web Scraping with Selenium.

One problem I encountered in building my archive is that LinkedIn is a Dynamic Website, which means many important information doesn't appear directly in the HTML. So if I just make a simple requests and use BeautifulSoup to parse it, plenty of information is missed. To solve this, I have to use [selenium](https://www.selenium.dev/), which is a tool to automate browsers and it has a [python package](https://selenium-python.readthedocs.io/installation.html). I would also need [Chromedriver](https://chromedriver.chromium.org/home), which could open a window automatically and mimic human's browsing habits.


# Archive Evaluation

## Is my data appropriate?

I believe my data is appropriate to investigate the job market trend and it's updating really quick. The job information data on linedin is born-digital, which means

## Transformation 



## Temporal and Spatial Resolution

To echo the content we learn from Large Scale Computing, I could set a scheduled task in Elastic Container Service to run the webscraping daily, last for a year, so I could find out if the number of jobs available has seasonal changes and yearly changes. For example, year 2020 is notoriously for job-seekers to land a job due to covid. 


## Ethical Concerns

While job descriptions are public data and can be accessed by everyone using the internet, do companies really want users to keep these data? While job-seekers post their names, job experience and education background online, as well as personal summaries, or even their resume and personal contact information. These cause increase ethical concerns

## Can this crawler last a long time?

The website is making constantly changes. For example, `job-result-card__location` has been changed to `job-search-card__location` from March to October, and this kind of small changes are hard to catch.

Besides, LinkedIn has a `robots.txt` file that disallow all users to scrape its website, although we can apply to be added to its whitelist. In fact, many 




# Reference

- [Scrape Linkedin Guide](https://maoviola.medium.com/a-complete-guide-to-web-scraping-linkedin-job-postings-ad290fcaa97f)

- [Debug ChromeDriver](https://stackoverflow.com/questions/60362018/macos-catalinav-10-15-3-error-chromedriver-cannot-be-opened-because-the-de)

- [ChromeDriver Setup](https://zwbetz.com/download-chromedriver-binary-and-add-to-your-path-for-automated-functional-testing/)

- [Set PATH variable](https://www.cyberciti.biz/faq/appleosx-bash-unix-change-set-path-environment-variable/) and [another tutorial](https://www.kenst.com/2015/03/including-the-chromedriver-location-in-macos-system-path/) and [a helpful debug video](https://www.youtube.com/watch?v=7R5n0sNSza8&ab_channel=StudentEngineer)

- [CSS Selector](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors)

- [Job Market Trend Analysis](https://medium.com/henry-jia/job-market-trend-analysis-d6b290b71e41)

- [selenium documentation](https://www.selenium.dev/documentation/webdriver)

- [An Introduction to robots.txt](https://www.linkedin.com/learning/advanced-seo-developing-an-seo-friendly-website/robots-txt?autoAdvance=true&autoSkip=false&autoplay=true&resume=true&u=57690273) and LinkedIn's [robots.txt](https://www.linkedin.com/robots.txt) and [Prohibited Software and Extensions](https://www.linkedin.com/help/linkedin/answer/56347/prohibited-software-and-extensions?lang=en)

- [A Complete Guide to Web Scraping LinkedIn Job Postings](https://maoviola.medium.com/a-complete-guide-to-web-scraping-linkedin-job-postings-ad290fcaa97f)

- [BeautifulSoup Documentations](https://www.crummy.com/software/BeautifulSoup/bs4/doc/#find-all)

- [scraping glassdoor](https://towardsdatascience.com/selenium-tutorial-scraping-glassdoor-com-in-10-minutes-3d0915c6d905)

- [linedin scrapper](https://github.com/joeyism/linkedin_scraper)

- Course Slides and Codes

