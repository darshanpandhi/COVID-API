# COVID-API

## API Description

This **free** API provides COVID-19 statistics in Manitoba for the requested type of cases (**active** or **total**). Optionally, one can request this for a specific **city** and **date** and retrieve that information, otherwise it will return it for the entire province.

**Base URL:** https://api.covid-manitoba.org

## Endpoints and Parameters
**Endpoint:** cases

| Parameter Name | Required / Optional | Default value | Description | Example |
| ------ | ---------- | --- | --- | --- |
| Type   | Required         | No default value as this parameter should always be specified (required) | Filter cases as "total", "active", "deaths" or "recoveries" | deaths |
| Date  | Optional | If no date is provided, total cases will be shown right from the beginning till today | Filter cases by a specific date (in YYYY-MM-DD format) | 2020-11-12 |
| City | Optional | If a city is not specified, cases for the entire province will be shown | Filter the number of cases by a specific city in Manitoba | winnipeg |

## Description of Resources

**covid_data**
  * **GET**/json Get Manitoba covid data.

  
  
## Sample Requests with Sample Responses

### Requests
```
https://api.covid-manitoba.org/covid_data/json?cases=total

https://api.covid-manitoba.org/covid_data/json?cases=total&city='winnipeg'            

https://api.covid-manitoba.org/covid_data/json?cases=active&date=2020-05-30

https://api.covid-manitoba.org/covid_data/json?cases=active&city='winnipeg'&date=2020-05-30

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
