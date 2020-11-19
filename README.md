# COVID-API

## Description

This **free** API returns COVID-19 data for a given day, region, and 

## Endpoints and Parameters
**Endpoint:** https://api.covid-manitoba.org/json

* **city (string)**: Latitude in decimal degrees. Optional.
* **date (string)**: Date in YYYY-MM-DD format. Also accepts other date formats and even relative date formats. If not present, date defaults to current date. Optional.

## Resources

## Sample Request and Response

###Request
https://api.covid-manitoba.org/json?city='winnipeg'&lat
https://api.covid-manitoba.org/json?date=2020-05-30

###Response
  {
      "results":
      {
        "total_cases:"342",
        "inrease_cases_from_previous_day":"50"
        "total_deaths":"12",
        "increase_deaths_from previous_day":"1"
        "total_recovered":"100"
      },
       "status":"OK"
    }
