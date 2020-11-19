# COVID-API

## Description

This **free** API provides COVID-19 statistics in Manitoba for the requested type of cases (**active** or **total**). Optionally, one can request this for a specific **city** and **date** and retrieve that information, otherwise it will return it for the entire province.

## Endpoints and Parameters
**Endpoint:** https://api.covid-manitoba.org/json

* **type (string)**: Total or Active Cases. Required.
* **city (string)**: Latitude in decimal degrees. Optional. If missing, it will provide statistics for the entire province.                                  
* **date (string)**: Date in YYYY-MM-DD format. Optional. If missing, it will assume current date.                  

## Resources

The retrieved data is formatted using JSON, as is shown below:

????

## Sample Requests and Responses

### Requests

https://api.covid-manitoba.org/json?cases=total&city='winnipeg'            

https://api.covid-manitoba.org/json?cases=active&date=2020-05-30

https://api.covid-manitoba.org/json?cases=total



### Responses
''
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
''
