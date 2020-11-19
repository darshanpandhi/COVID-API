# COVID-API

## Description

This **free** API provides COVID-19 statistics in Manitoba for the requested type of cases (**active** or **total**). Optionally, one can request this for a specific **city** and **date** and retrieve that information, otherwise it will return it for the entire province.

## Endpoints and Parameters
**Endpoint:** https://api.covid-manitoba.org/json

* **city (string)**: Latitude in decimal degrees. Optional.
* **date (string)**: Date in YYYY-MM-DD format. Also accepts other date formats and even relative date formats. If not present, date defaults to current date. Optional.

## Resources

The retrieved data is formatted using JSON, as is shown below:

????

## Sample Request and Response

### Request
https://api.covid-manitoba.org/json?city='winnipeg'&lat                             
https://api.covid-manitoba.org/json?date=2020-05-30

### Response
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
