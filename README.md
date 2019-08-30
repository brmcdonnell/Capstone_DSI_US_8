# Predicting Success for 5th Year Track Athletes

## Background

In the NCAA, athletes are allowed to compete for four seasons over a 5 year period. The year in which an doesn't compete is considered a "red-shirt" year. The goal of this project is to take in past collegiate track and field performance and predict an athlete's success if given a fifth year of competition.

## Problem Statement

Using a regression model, I will predict the success level for an NCAA track athletes seeking a fifth year of competition.


## Data Collection

The data for this project will be collected from the collegiate results database, <a href="https://www.tfrrs.org/" target="_blank">tfrrs</a> for the Power Five conferences (ACC, Big Ten, Big 12, Pac-12, SEC). The Scrapy library will be used to pull the information for every athlete in each of these conferences over the years tfrrs has results.

**As of 7/31/2019**, I have written a web crawler that can extract all of the high school athlete data from the <a href="https://www.athletic.net/" target="_blank">Athleteic.net</a> website. This data was relevant for the initial problem statement; however, that data is no longer relevant as the sheer quantity of data extraction was too large for me to easily manipulate. For now, I have scaled back the amount of total data in the project to create a project that can scale with the quantity of the data in the future. This web crawler is available as a Scrapy.spider object in the project repo.

The web crawler for the tfrrs website is nearly written, but it is not yet available. The .ipynb file of progress is available in the repo.

**Disclaimer: This data is not going to be used in any way for commercial or promotional way. The data will not be avaialable for download, and I do not have any ownership rights of the data used in this project.**

## Breaking Down the Problem

1. Success will be defined as a weighted value on a normalized scale from the following measurements:
  1. The amount of improvement from freshman season to senior season. The data will help determine this scale, and time performances will be compared via the <a href="https://www.cs.uml.edu/~phoffman/xcinfo3.html" target="_blank">Purdy points</a> of the results.
  2. The number of points scored at conference championships.
  3. The appearance of an athlete at an NCAA National meet.
  4. The scoring of points at an NCAA National meet.
2. Only track athletes will be analyzed. Cross Country and field event athlete data will not be used in this iteration of the project.
3. For this problem, a regression model will be fit for the success measurement of each athlete.

## Risks & Assumptions

The risk of using this data for a predictive model lies largely in the definition of "success" as an athlete. Some coaches will value place finish at a conference or national level, while others will define success on a scale of improvement. I expect my success measure to account for both of those mentalities, however the weighting towards conference finish will be higher as many of the coaches at the Power Five schools will value conference point scoring as more important than improvement.

The data for this project will be complete for the years of competition (appr. 2009-present).

I expect this model to be a useful tool for coaches for deciding whether an athlete should be kept on for a fifth year if their redshirt season has been used in the prior four years of competition.

## Preliminary EDA

To be completed upon data retrieval.

## Conclusions

TBD.
