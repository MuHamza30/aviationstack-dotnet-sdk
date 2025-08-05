# Flights

In order to look up real-time or historical information about one or multiple flights, you can use the Aviationstack's `flights` endpoint.

```csharp
FlightsController flightsController = client.FlightsController;
```

## Class Name

`FlightsController`


# Get Flights

Retrieve real-time and historical flight data

```csharp
GetFlightsAsync(
    string accessKey,
    int? limit = 100,
    int? offset = 0,
    string flightIata = null,
    string flightIcao = null,
    string airlineIata = null,
    string airlineIcao = null,
    string flightNumber = null,
    string depIata = null,
    string depIcao = null,
    string arrIata = null,
    string arrIcao = null,
    Models.FlightStatus2Enum? flightStatus = null,
    DateTime? date = null)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accessKey` | `string` | Query, Required | Your AviationStack API access key |
| `limit` | `int?` | Query, Optional | Number of results to return (max 1000)<br><br>**Default**: `100` |
| `offset` | `int?` | Query, Optional | Number of results to skip<br><br>**Default**: `0` |
| `flightIata` | `string` | Query, Optional | IATA code of the flight |
| `flightIcao` | `string` | Query, Optional | ICAO code of the flight |
| `airlineIata` | `string` | Query, Optional | IATA code of the airline |
| `airlineIcao` | `string` | Query, Optional | ICAO code of the airline |
| `flightNumber` | `string` | Query, Optional | Flight number |
| `depIata` | `string` | Query, Optional | IATA code of departure airport |
| `depIcao` | `string` | Query, Optional | ICAO code of departure airport |
| `arrIata` | `string` | Query, Optional | IATA code of arrival airport |
| `arrIcao` | `string` | Query, Optional | ICAO code of arrival airport |
| `flightStatus` | [`FlightStatus2Enum?`](../../doc/models/flight-status-2-enum.md) | Query, Optional | Status of the flight |
| `date` | `DateTime?` | Query, Optional | Date in YYYY-MM-DD format |

## Response Type

[`Task<Models.FlightResponse>`](../../doc/models/flight-response.md)

## Example Usage

```csharp
string accessKey = "access_key8";
int? limit = 100;
int? offset = 0;
try
{
    FlightResponse result = await flightsController.GetFlightsAsync(
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
| 429 | Rate limit exceeded | [`ErrorResponseException`](../../doc/models/error-response-exception.md) |

