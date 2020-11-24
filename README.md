# COVID-MANITOBA API

## API Description

Covid-Manitoba API provides vital statistics regarding the ongoing pandemic. It provides information regarding the number of cases in the Manitoba population as well as information regarding the current healthcare situation in the province.

**Base URL:** https://api.covid-manitoba.org


## Resources

The covid-manitoba API has 2 resources:

1. **Resource:** population
    ```
    /population
   ```
    
    The population resource has two endpoints: *total-cases* and *active-cases*
    

2. **Resource:** healthcare
    ```
    /healthcare
   ```

    The healthcare resource has one endpoint: *hospitals*


## Endpoints and Parameters

1. **Endpoint:** total-cases
     ```
    GET         /population/total-cases
   ```

    This endpoint is used to **GET** the number of total COVID cases.
    
    <details>
        <summary>Parameters {...} </summary>


    | Parameter Name | Required / Optional | Default value | Description | Example |
    | ------ | ---------- | --- | --- | --- |
    | Date  | Optional | If no date is provided, total cases will be shown right from the beginning till today | Filter total cases by a specific date (in YYYY-MM-DD format) | 2020-11-12 |
    | City | Optional | If a city is not specified, total cases for the entire province will be shown | Filter total cases by a specific city in Manitoba | winnipeg |

    ---

    </details>
    
    <br>

2. **Endpoint:** active-cases

     ```
    GET         /population/active-cases
   ```
    
    This endpoint is used to **GET** the number of active COVID cases.

    <details>
        <summary>Parameters {...} </summary>


    | Parameter Name | Required / Optional | Default value | Description | Example |
    | ------ | ---------- | --- | --- | --- |
    | Date  | Optional | If no date is provided, active cases will be shown right from the beginning till today | Filter active cases by a specific date (in YYYY-MM-DD format) | 2020-11-12 |
    | City | Optional | If a city is not specified, active cases for the entire province will be shown | Filter active cases by a specific city in Manitoba | winnipeg

    ---

    </details>
    
    <br>


3. **Endpoint:** hospitals

     ```
    GET         /healthcare/hospitals
   ```


    This endpoint is used to **GET** the number of hospitals equipped to handle COVID patients.

    <details>
    <summary> Parameters {...} </summary>
    

    This endpoint supports no parameters.


    </details>
    
     <br>


## Resources

The covid-manitoba API has 2 resources:

1. **Resource:** population
    ```
    /population
   ```
    
    The population resource has two endpoints: *total-cases* and *active-cases*
    
1. ```
    /population
   ```
    
    The population resource has two endpoints: *total-cases* and *active-cases*
    
1. **Resource:** /population
    
    The population resource has two endpoints: *total-cases* and *active-cases*

2. **Resource:** /healthcare

    The healthcare resource has one endpoint: *hospitals*


## Endpoints and Parameters

1. **Endpoint:** /population/total-cases

    This endpoint is used to **GET** the number of total COVID cases.
    
    <details>
        <summary>Parameters {...} </summary>


    | Parameter Name | Required / Optional | Default value | Description | Example |
    | ------ | ---------- | --- | --- | --- |
    | Date  | Optional | If no date is provided, total cases will be shown right from the beginning till today | Filter total cases by a specific date (in YYYY-MM-DD format) | 2020-11-12 |
    | City | Optional | If a city is not specified, total cases for the entire province will be shown | Filter total cases by a specific city in Manitoba | winnipeg |

    ---

    </details>

2. **Endpoint:** /population/active-cases

    This endpoint is used to **GET** the number of active COVID cases.

    <details>
        <summary>Parameters {...} </summary>


    | Parameter Name | Required / Optional | Default value | Description | Example |
    | ------ | ---------- | --- | --- | --- |
    | Date  | Optional | If no date is provided, active cases will be shown right from the beginning till today | Filter active cases by a specific date (in YYYY-MM-DD format) | 2020-11-12 |
    | City | Optional | If a city is not specified, active cases for the entire province will be shown | Filter active cases by a specific city in Manitoba | winnipeg

    --- 

    </details>


3. **Endpoint:** /healthcare/hospitals


    This endpoint is used to **GET** the number of hospitals equipped to handle COVID patients.

    <details>
    <summary> Parameters {...} </summary>
    

    This endpoint supports no parameters.


    </details>


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
