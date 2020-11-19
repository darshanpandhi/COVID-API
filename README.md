# COVID-API

## Description

This **free** API provides COVID-19 statistics in Manitoba for the requested type of cases (**active** or **total**). Optionally, one can request this for a specific **city** and **date** and retrieve that information, otherwise it will return it for the entire province.

## Endpoints and Parameters
**Endpoint:** https://api.covid-manitoba.org/json

* **case-type (string)**
  * Filter cases by showing "total" or "active" number of cases. 
  * Example: total
  * Required
* **city (string)**
  * Filter the number of cases by a specific city in Manitoba.
  * Example: winnipeg
  * Optional
* **date (string)**
  * Filter the number of cases by a specific date.
  * Format: YYYY-MM-DD. 
  * If not present, 
  * Optional               

## Resources


????

## Sample Requests and Responses

### Requests
```
https://api.covid-manitoba.org/json?cases=total&city='winnipeg'            

https://api.covid-manitoba.org/json?cases=active&date=2020-05-30

https://api.covid-manitoba.org/json?cases=total
```


### Response

The retrieved data is formatted using JSON, as is shown below for total cases:


  ```
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
  ```
