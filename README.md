# Piggy Metrics (Kubernetes) - Statistics service

[![CircleCI](https://circleci.com/gh/afermon/PiggyMetrics-statistics-service.svg?style=svg)](https://circleci.com/gh/afermon/PiggyMetrics-statistics-service) [![codecov](https://codecov.io/gh/afermon/PiggyMetrics-statistics-service/branch/master/graph/badge.svg)](https://codecov.io/gh/afermon/PiggyMetrics-statistics-service) [![GitHub license](https://img.shields.io/github/license/mashape/apistatus.svg)]((https://github.com/afermon/PiggyMetrics-statistics-service/blob/master/LICENCE))

Performs calculations on major statistics parameters and captures time series for each account. Datapoint contains values, normalized to base currency and time period. This data is used to track cash flow dynamics in account lifetime.

Method	| Path	| Description	| User authenticated	| Available from UI
------------- | ------------------------- | ------------- |:-------------:|:----------------:|
GET	| /statistics/{account}	| Get specified account statistics	          |  | 	
GET	| /statistics/current	| Get current account statistics	| × | × 
GET	| /statistics/demo	| Get demo account statistics	|   | × 
PUT	| /statistics/{account}	| Create or update time series datapoint for specified account	|   | 

For more information please refer to the main repository [afermon/PiggyMetrics-Kubernetes](https://github.com/afermon/PiggyMetrics-Kubernetes)

## Credits

* Forked from [sqshq/PiggyMetrics](https://github.com/sqshq/PiggyMetrics)