# Airports

To get data about Airports across the globe, you can use the API's `airports` endpoint.

```csharp
AirportsController airportsController = client.AirportsController;
```

## Class Name

`AirportsController`


# Get Airports

Retrieve airport data

```csharp
GetAirportsAsync(
    string accessKey,
    int? limit = 100,
    int? offset = 0,
    string iataCode = null,
    string icaoCode = null,
    string countryCode = null,
    string cityName = null)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accessKey` | `string` | Query, Required | Your AviationStack API access key |
| `limit` | `int?` | Query, Optional | Number of results to return<br><br>**Default**: `100` |
| `offset` | `int?` | Query, Optional | Number of results to skip<br><br>**Default**: `0` |
| `iataCode` | `string` | Query, Optional | IATA code of the airport |
| `icaoCode` | `string` | Query, Optional | ICAO code of the airport |
| `countryCode` | `string` | Query, Optional | Country code |
| `cityName` | `string` | Query, Optional | City name |

## Response Type

[`Task<Models.AirportResponse>`](../../doc/models/airport-response.md)

## Example Usage

```csharp
string accessKey = "access_key8";
int? limit = 100;
int? offset = 0;
try
{
    AirportResponse result = await airportsController.GetAirportsAsync(
        accessKey,
        limit,
        offset
    );
}
catch (ApiException e)
{
    // TODO: Handle exception here
    Console.WriteLine(e.Message);
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request | [`ErrorResponseException`](../../doc/models/error-response-exception.md) |
| 401 | Unauthorized | [`ErrorResponseException`](../../doc/models/error-response-exception.md) |

