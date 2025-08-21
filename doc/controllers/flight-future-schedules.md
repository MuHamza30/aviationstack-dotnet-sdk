# Flight Future Schedules

```csharp
FlightFutureSchedulesController flightFutureSchedulesController = client.FlightFutureSchedulesController;
```

## Class Name

`FlightFutureSchedulesController`


# Get Future Flight Schedules

Retrieve future flight schedule information for a specific airport and date

```csharp
GetFutureFlightSchedulesAsync(
    string iataCode,
    Models.TypeEnum type,
    DateTime date,
    int? limit = 100,
    int? offset = 0)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `iataCode` | `string` | Template, Required | [Required] The IATA code of the airport you'd like to request data from. Example: JFK,DXB. |
| `type` | [`TypeEnum`](../../doc/models/type-enum.md) | Template, Required | [Required] Airport schedule type. Available values: departure or arrival. |
| `date` | `DateTime` | Template, Required | [Required] Filter your results by providing a flight date in the format YYYY-MM-DD. |
| `limit` | `int?` | Query, Optional | Number of results to return<br><br>**Default**: `100` |
| `offset` | `int?` | Query, Optional | Number of results to skip<br><br>**Default**: `0` |

## Response Type

[`Task<Models.FlightScheduleResponse>`](../../doc/models/flight-schedule-response.md)

## Example Usage

```csharp
string iataCode = "iata_code4";
TypeEnum type = TypeEnum.Departure;
DateTime date = DateTime.Parse("2016-03-13");
int? limit = 100;
int? offset = 0;
try
{
    FlightScheduleResponse result = await flightFutureSchedulesController.GetFutureFlightSchedulesAsync(
        iataCode,
        type,
        date,
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

