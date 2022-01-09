# Project Proposal Template

Question/Need:
* What is the question behind your analysis? What is the purpose of the model/system you plan to build?

Find best placement for vending machines, after looking into metro traffic and average income data or spending per neighberhood. 

## Who benefits from exploring this question or building this model/system?

Start-up company in NYC. Which plans to place vending machines through out NYC with daily fresh plant based meals and snacks in the metro system. 
They would like to know where to place 35 vending machines, traffic and spending money vise. 

Data Description:
## What dataset(s) do you plan to use, and how will you obtain the data?

MTA data and US Census

## What is an individual sample/unit of analysis in this project (i.e., what are your rows)? What characteristics/features do you expect to work with (i.e., what are your columns of interest)?

Entry and exit from stations
Neighbourhood
Times of entry/exit
Income per neighbourhood

## How do you intend to meet the tools requirement of the project?

Sql , pandas, numpy, seaborn, plotly

## Are you planning in advance to need or use additional tools beyond those required?

Dashboard for the business

## MVP Goal:
* What would a minimum viable product (MVP) look like for this project?

* Goal: This analysis seeks to identify the busiest stations and its peak times combined with average income  per neighbourhood. 

* Process: Data exploration to reach this conclusion entailed aggregation of daily and hourly commuter data at the turnstile level, and finally zip code level which can be combined with latitude and longitude retrieval. 

* Preliminary visualization: Figures showing aggregated highest traffic for MTA commuters aggregated for the past 6 months and checking pick hours for those stations. 

* Preliminary conclusions: Finding top busiest stations and combining it with average income will give you different results than only looking into commuter traffic. 
