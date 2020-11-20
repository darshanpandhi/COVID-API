# COVID-API

## Description

This **free** API provides COVID-19 statistics in Manitoba for the requested type of cases (**active** or **total**). Optionally, one can request this for a specific **city** and **date** and retrieve that information, otherwise it will return it for the entire province.

## Endpoints and Parameters
**Endpoint:** https://api.covid-manitoba.org/json

* **case-type (string)**
  * Filter cases by "total" or "active" number of cases
  * Example: total
  * Required
* **city (string)**
  * Filter the number of cases by a specific city in Manitoba
  * Example: winnipeg
  * Optional
* **date (string)**
  * Filter the number of cases by a specific date (in YYYY-MM-DD format)
  * Example: 2020-11-12
  * Optional          
  * If not present, 

## Resources


????

## Sample Requests and Responses

### Requests
```
https://api.covid-manitoba.org/json?cases=total

https://api.covid-manitoba.org/json?cases=total&city='winnipeg'            

https://api.covid-manitoba.org/json?cases=active&date=2020-05-30

https://api.covid-manitoba.org/json?cases=active&city='winnipeg'&date=2020-05-30

```


### Response

The retrieved data is formatted using JSON, as is shown below for the first sample request:


  ```
  {                       
      "results":                          
      {                                        
        "total_cases:"12482",                                
        "inrease_cases_from_previous_day":"389"                      
        "total_deaths":"198",                      
        "increase_deaths_from previous_day":"12"                   
        "total_recovered":"4655"                           
      },                           
       "status":"OK"                                      
    }        
    
  ```
The second, third, and fourth sample request's responses are demonstrated below, respectively.


  ```
  {                       
      "results":                          
      {                                        
        "total_cases:"7786",                                
        "inrease_cases_from_previous_day":"271"                      
        "total_deaths":"142",                      
        "increase_deaths_from previous_day":"8"                   
        "total_recovered":"100"                           
      },                           
       "status":"OK"                                      
    }        
    
  ```
  ```
  {                       
      "results":                          
      {                                        
        "total_cases:"283",                                
        "inrease_cases_from_previous_day":"0"                      
        "total_deaths":"7",                      
        "increase_deaths_from previous_day":"0"                   
        "total_recovered":"283"                           
      },                           
       "status":"OK"                                      
    }        
    
  ```
```
  {                       
      "results":                          
      {                                        
        "total_cases:"206",                                
        "inrease_cases_from_previous_day":"0"                      
        "total_deaths":"5",                      
        "increase_deaths_from previous_day":"0"                   
        "total_recovered":"206"                           
      },                           
       "status":"OK"                                      
    }        
    
  ```
