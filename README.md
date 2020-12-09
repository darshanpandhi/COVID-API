# COVID-MANITOBA API

## API Description

The Covid-Manitoba API provides vital statistics regarding the ongoing pandemic. It provides information about the number of cases in the Manitoba population as well as information on the current healthcare situation in the province.

**Base URL:** https://api.covid-manitoba.org

## Resources

The covid-manitoba API has 2 resources:

1. **Resource:** population
    ```
    /population
   ```
    
    The population resource has two endpoints: *total-cases* and *active-cases*
    
    <br>
    

2. **Resource:** healthcare
    ```
    /healthcare
   ```

    The healthcare resource has one endpoint: *hospitals*
    
     <br>
     
 **Note:** The responses will be formatted using JSON.
 
 <br>

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


## Sample Requests with Sample Responses

 <br>


```
https://api.covid-manitoba.org/population/total-cases
```

<details>
    <summary> Sample Response {...} </summary>
    
```
{                       
    "results":                          
    {                                        
        "cases:                         12482,                                
        "time_period_start_date":       "2020-01-01",
        "time_period_end_date":         "2020-11-24",
        "region":                       "Manitoba"
    },                           
        "status":                       "OK"                                      
} 
```

---
</details>


 <br>

```
https://api.covid-manitoba.org/population/active-cases?city=brandon
```


<details>
    <summary> Sample Response {...} </summary>
    
```
{                       
    "results":                          
    {                                        
        "cases:                         2482,                                
        "time_period_start_date":       "2020-01-01",
        "time_period_end_date":         "2020-11-24",
        "region":                       "Brandon"
    },                           
        "status":                       "OK"                                      
} 
```
---
</details>

 <br>

```
https://api.covid-manitoba.org/population/active-cases?city=selkirk&date=2020-11-24
```

<details>
    <summary> Sample Response {...} </summary>
    
```
{                       
    "results":                          
    {                                        
        "cases:                         482,                                
        "time_period_start_date":       "2020-11-24",
        "time_period_end_date":         "2020-11-24",
        "region":                       "Selkirk"
    },                           
        "status":                       "OK"                                      
} 
```
---
</details>

 <br>

```
https://api.covid-manitoba.org/healthcare/hospitals
```

<details>
    <summary> Sample Response {...} </summary>
    
```
{                       
    "results":                          
    {                                        
        "number_of_hospitals:           21,                                
        "number_of_available_beds":     298,
        "region":                       "Manitoba"
    },                           
        "status":                       "OK"                                      
} 
```
---
</details>

 <br>

```
https://api.covid-manitoba.org/population/active-cases?date=5-2020-24
```
<details>
    <summary> Sample Response {...} </summary>
    
```
{                       
    "results":                          
    {   
    
    },                           
        "status":                       "INVALID_REQUEST"                                      
} 
```

 **Note:** This is because the date parameter was not specified in its required format of YYYY-MM-DD
 
</details>


