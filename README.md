## API Description

This API will access weather data in Winninpeg and Brandon MB. Users will be able to enter the date they want data for as a parameter in the API call. There will exist two resources for this api "Brandon" and "Winnipeg". In each of these resources there will be three endpoints, one which retrieves all weather data for a specified date, one which returns only precipitation levels for the given date, and one that returns only UVIndex for the specified date.

## Endpoints

> Winnipeg/AllWeather (<Date\>)

> Winnipeg/Precipitation(<Date\>)

> Winnipeg/UVIndex (<Date\>)

The only required parameter for each of the three endpoint will be "Date". It should be a string formatted in YYYY-MM-DD format.


## Description of Resources

This API has access to data for Winnipeg and Brandon. They are grouped into two separate resources:

> /Brandon

Accesing the Brandon resource will return only data related to Brandon MB.

> /Winnipeg

Each of the resources will return data in the following formats based on the endpoint used: 

##### 1. All weather endpoint 
```json
{
  "results": {
    "UVIndex": 5,
    "Precipitation": "10%",
    "Temperature": "20C",
    "snowfall": "0",
    "snowDepth": "0cm",
    "cloudCoverage": "30%",
    "airDensity": 1.5
  },
  "status": "OK"
}
```
##### 2. Precipitation endpoint
```json
{
  "results": {
    "Precipitation": "10%"
  },
  "status": "OK"
}
```

##### 3. UVIndex endpoint 
```json
{
  "results": {
    "UVIndex": 5,
  },
  "status": "OK"
}
```
Accesing the Winnipeg resource will return only data related to Winnipeg MB.

## Sample Request

##### Request

```
https://group11.com/winnipeg/AllWeather?date=2020-08-01
```

##### Result

```json
{
  "results": {
    "UVIndex": 5,
    "Precipitation": "10%",
    "Temperature": "20C",
    "snowfall": "0",
    "snowDepth": "0cm",
    "cloudCoverage": "30%",
    "airDensity": 1.5
  },
  "status": "OK"
}
```
