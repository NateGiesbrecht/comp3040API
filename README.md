## API Description

This API will access weather data in Winninpeg and Brandon MB. Users will be able to enter the date they want data for as a parameter in the API call. There will exist two resources for this api "Brandon" and "Winnipeg". In each of these resources there will be three endpoints, one which retrieves all weather data for a specified date, one which returns only precipitation levels for the given date, and one that returns only UVIndex for the specified date.

## Endpoints

> Winnipeg/AllWeather (<Date\>)

> Winnipeg/Precipitation(<Date\>)

> Winnipeg/UVIndex (<Date\>)

The only required parameter for each of the three endpoint will be "Date". It should be a string formatted in YYYY-MM-DD format.
