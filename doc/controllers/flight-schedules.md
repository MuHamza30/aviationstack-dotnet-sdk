# Flight Schedules

```csharp
FlightSchedulesController flightSchedulesController = client.FlightSchedulesController;
```

## Class Name

`FlightSchedulesController`


# Get Flight Schedules

Retrieve flight schedule information for a specific airport

```csharp
GetFlightSchedulesAsync(
    string accessKey,
    string iataCode,
    Models.TypeEnum type,
    int? limit = 100,
    int? offset = 0)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accessKey` | `string` | Query, Required | Your AviationStack API access key |
| `iataCode` | `string` | Template, Required | [Required] The IATA code of the airport you'd like to request data from. Example: JFK,DXB. |
| `type` | [`TypeEnum`](../../doc/models/type-enum.md) | Template, Required | [Required] Airport schedule type. Available values: departure or arrival. |
| `limit` | `int?` | Query, Optional | Number of results to return<br><br>**Default**: `100` |
| `offset` | `int?` | Query, Optional | Number of results to skip<br><br>**Default**: `0` |

## Response Type

[`Task<Models.FlightScheduleResponse>`](../../doc/models/flight-schedule-response.md)

## Example Usage

```csharp
string accessKey = "access_key8";
string iataCode = "iata_code4";
TypeEnum type = TypeEnum.Departure;
int? limit = 100;
int? offset = 0;
try
{
    FlightScheduleResponse result = await flightSchedulesController.GetFlightSchedulesAsync(
        accessKey,
        iataCode,
        type,
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

