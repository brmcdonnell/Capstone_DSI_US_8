# Predicting Final Year Performance in Collegiate Track & Field Running Events

## Background

As a coach, a valuable part of collegiate track and field is goal setting with an athlete. Being able to come up with lofty but attainable goals is an important part of the coach-athlete relationship. This model predicts the next season best performance given an athlete's past collegiate data.

## Problem Statement

Using past collegiate results, create a model that predicts the next season best for a collegiate, flat track athlete in a power 5 conference.

## Data Collection

The data for this project was collected from the collegiate track and field results database, <a href="https://www.tfrrs.org/" target="_blank">tfrrs</a> for the Power Five conferences (ACC, Big Ten, Big 12, Pac-12, SEC). The Scrapy library was be used to pull the information for every athlete in each of these conferences over the years tfrrs has results.

Two web crawlers were written; one for High School track data, and one for collegiate data. The high school data spider was written by me, and the collegiate data scraper was written jointly by Brendan and Declan McDonnell. The high school data spider works, and was more of a proof of concept for a larger, ongoing data analysis project. It ultimately was not used for this project, but the scraper was fun to build.

**Disclaimer: This data is not going to be used in any way for commercial or promotional way. The data will not be avaialable for download, and I do not have any ownership rights of the data used in this project.**

## Project Notebooks

- Initial EDA
  - Getting data set up to be manipulated / dummied
- EDA Part II
  - Further exploring the data and dummying out variables
- Data Analysis & Visualizations
  - Includes final model

## Statistical Analysis

The data shown is fairly straightforward. Each row has a result from a meet for an athlete for an event. If an athlete runs two or three events at a meet, you will see two or three events at a meet by the same athlete, and the event and mark will be noted.

To compare athletes that run different events, I had to use a normalization scale that would allow two times from two different events to be compared on a level playing field. For that I used a system known as <a href="http://run-down.com/statistics/calcs_explained.php" target="_blank">Purdy Points</a>. Purdy Points can only be used for flat, running events, which is all that was used for the analysis here.

## <a href="https://docs.google.com/presentation/d/1RGwQ94GQauuH9OJFfJk3fYyaiYZoa2RXGR11X5oOcZk/edit?usp=sharing" target="_blank">Final Presentation</a>

## Conclusions

From the analysis done, the value in this project lies in the accuracy of the model when predicting what an athlete "should" accomplish in the following season. Given the dataset, the model performed relatively well. This would be a good estimate for athletes going into a final season to have a season best to shoot for for flat track events.
