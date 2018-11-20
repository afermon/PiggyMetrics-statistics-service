[![Build Status](https://travis-ci.com/afermon/PiggyMetrics-statistics-service.svg?branch=master)](https://travis-ci.com/afermon/PiggyMetrics-statistics-service)
[![codecov](https://codecov.io/gh/afermon/PiggyMetrics-statistics-service/branch/master/graph/badge.svg)](https://codecov.io/gh/afermon/PiggyMetrics-statistics-service)
[![GitHub license](https://img.shields.io/github/license/mashape/apistatus.svg)](https://github.com/sqshq/PiggyMetrics/blob/master/LICENCE)

# Piggy Metrics

**A simple way to deal with personal finances**

This is a proof-of-concept application, which demonstrates [Microservice Architecture Pattern](http://martinfowler.com/microservices/) using Spring Boot, Spring Cloud and Docker.
With a pretty neat user interface, by the way.

![](https://cloud.githubusercontent.com/assets/6069066/13864234/442d6faa-ecb9-11e5-9929-34a9539acde0.png)
![Piggy Metrics](https://cloud.githubusercontent.com/assets/6069066/13830155/572e7552-ebe4-11e5-918f-637a49dff9a2.gif)

## Functional services

PiggyMetrics was decomposed into three core microservices. All of them are independently deployable applications, organized around certain business domains.

<img width="880" alt="Functional services" src="https://cloud.githubusercontent.com/assets/6069066/13900465/730f2922-ee20-11e5-8df0-e7b51c668847.png">

#### Statistics service
Performs calculations on major statistics parameters and captures time series for each account. Datapoint contains values, normalized to base currency and time period. This data is used to track cash flow dynamics in account lifetime.

Method	| Path	| Description	| User authenticated	| Available from UI
------------- | ------------------------- | ------------- |:-------------:|:----------------:|
GET	| /statistics/{account}	| Get specified account statistics	          |  | 	
GET	| /statistics/current	| Get current account statistics	| × | × 
GET	| /statistics/demo	| Get demo account statistics	|   | × 
PUT	| /statistics/{account}	| Create or update time series datapoint for specified account	|   | 

