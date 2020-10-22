# #AECT20 workshop: Simple Collection and Powerful Analysis of Twitter Data Using R

Friday, October 30, 2020 
1pm-4pm EDT

## Homebase

- **Website:** https://bretsw.github.io/aect20-workshop/
- **Repository** with all files for today's workshop: https://github.com/bretsw/aect20-workshop

## Agenda

- Part 1: Setup
  - Slides: [1 - Setup](1-setup.html)
  - Demo Doc: https://rstudio.cloud/project/1421785
- Part 2: Workflow
  - Slides: [2 - Workflow](2-workflow.html)
  - Demo Doc: https://rstudio.cloud/project/1427304

## Need help? Reach out!

- Ask questions in Zoom chat!
- Contact:
  - [staudtwi@msu.edu](mailto:staudtwi@msu.edu)
  - [Twitter: @bretsw](https://twitter.com/bretsw)
  - [Twitter: @spgreenhalgh](https://twitter.com/spgreenhalgh)
  - [Twitter: @jrosenberg6432](https://twitter.com/jrosenberg6432)
  
## Workshop Description

### Introduction

The #AECT20 call for proposals asks presenters to aim to understand “the culture of a group, organization, community, or society in the practice of learning design and research.” One essential dimension of understanding a culture is to study the artifacts and behaviors of group members over time. Indeed, many questions relevant to the field of learning design and technology have a temporal dimension—or at least they should. Specifically, social media studies are obvious sites for change-over-time research questions due to how quickly online practices and norms can change. Despite this, prominent AECT social media scholars have noted the scarcity of such research (Gao et al., 2012) and argued the need for more studies examining social media and time (Veletsianos et al., 2019; Xing & Gao, 2018).

Time travel is hard, if not impossible. As a result, collecting historical data from Twitter can be difficult and expensive. First, access to Twitter data is limited by the platform’s API. For instance, a researcher using the Twitter API today to search for information on #AECT19 or #AECTinspired would not be able to access tweets from the time of the convention in October 2019. Second, getting old tweets is not impossible, but likely expensive—there are companies that collect all tweets and are willing to make these available to academic researchers for the right price. There are also technical solutions to collect past tweets, but these too come at a cost, such as advanced technical skills and the risk of potentially violating Terms of Service agreements.

Our research team’s solution to these Twitter data collection issues is to use a Twitter Archiving Google Sheet (TAGS; https://tags.hawksey.info/). Getting started with TAGS is as simple as setting up a new Google Sheet, which will search the Twitter API every hour going forward, automatically. The tradeoff of using TAGS is that it returns limited metadata compared to what is available from the Twitter API—approximately 20% of all categories of information. That is, TAGS return the time, sender, and text of tweets, but not many additional details such as a list of the hashtags or hyperlinks contained in a tweet. As a result, we first use TAGS to easily collect tweet ID numbers, and then use the programming language R to re-query the Twitter API to collect additional metadata—specifically, using features of the R package rtweet (https://rtweet.info/).

We have formalized our workflow for Twitter research in our R package, tidytags. The purpose of tidytags is to sync together the simplicity of collecting tweets over time with TAGS, the utility of the rtweet package for processing and preparing additional Twitter metadata, and the convenience of curating different analytic functions we have developed during our own social media research across the past five years. This workflow is simple enough for beginning programmers to get started, but powerful enough to serve as the analytic foundation of our research that has been featured in Computers & Education, TechTrends, Journal of Research on Technology in Education, and numerous AECT presentations. Finally, in addition to sharing our workflow through tidytags, we have also summarized what we have learned (e.g., ethical considerations for social media research) in a chapter in the upcoming volume, Research Methods in Learning Design & Technology, edited by Enilda Romero-Hall.

### Workshop Learning Goals

In this session, we provide support and guidance for exploring Twitter data over time using R. Abstract principles will be grounded in the analysis of a dataset that is likely of interest to many AECT participants: tweets related to the AECT 2020 convention.

Interest in R has been growing among LDT researchers, as we have noted from the very enthusiastic participation in R workshops we led at AERA 2019 and AECT 2019, as well as numerous additional requests for information and consultation from colleagues getting started with R. For instance, in a post-survey following our AECT 2019 workshop, one participant noted: “I liked the various uses of data and different types of data. I also got double use between learning R and learning more about collecting social media data - a day well spent!” However, although R is becoming increasingly widely-used, there still remains a steep learning curve for beginners.

The purpose of this half-day workshop is twofold: first, to help beginners get past the intimidation of programming in R, and second, to teach and demonstrate our workflow for collecting and analyzing Twitter data using tidytags. Not that long ago, we too were beginners in data science, social media research, and using R. We remember what it was like to get started, and we enjoy helping others take those first steps in a better supported and less painful way.

Specifically, this workshop introduces participants to the steps for getting started in their own tidytags workflow:
1. Setting up a Twitter Archiving Google Sheet (TAGS) Tweet tracker
2. Viewing tweets collected by TAGS in RStudio
3. Pulling additional tweet metadata
4. Analyzing URLs in tweets (as we did in our 2018 AECT presentation)
5. Geocoding tweeter locations (as we did in our 2018 TechTrends article) and creating map visualizations 
6. Analyzing social networks of tweeters
7. Pulling in additional tweeter information to understand “the culture of a group, organization, community, or society in the practice of learning design and research” (AECT 2020 call for proposals)
8. Exporting edgelists to create network visualizations using the ggraph R package or the open-source software Gephi (https://gephi.org/)

Although the workshop focuses on these practical and applied steps, we frequently frame these in larger, conceptual issues, such as research ethics and research paradigms.

### Who This Workshop is For

The level of instruction will be suitable for participants looking for an introduction to R. This workshop is for both researchers and practitioners interested in using new computational research methods in their work, from a wide variety of scholarly and professional backgrounds. There are no suggested prerequisites for attending, but we do require that participants bring a computer—Mac, Windows, or Linux are all suitable for working in R.