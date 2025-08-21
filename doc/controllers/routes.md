# Routes

The aviationstack API `routes` endpoint is capable of providing data about airline routes, updated every 24 hours.

```csharp
RoutesController routesController = client.RoutesController;
```

## Class Name

`RoutesController`


# Get Routes

Retrieve airline route information

```csharp
GetRoutesAsync(
    int? limit = 100,
    int? offset = 0,
    string airlineIata = null,
    string airlineIcao = null)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `limit` | `int?` | Query, Optional | Number of results to return<br><br>**Default**: `100` |
| `offset` | `int?` | Query, Optional | Number of results to skip<br><br>**Default**: `0` |
| `airlineIata` | `string` | Query, Optional | IATA code of the airline |
| `airlineIcao` | `string` | Query, Optional | ICAO code of the airline |

## Response Type

[`Task<Models.RouteResponse>`](../../doc/models/route-response.md)

## Example Usage

```csharp
int? limit = 100;
int? offset = 0;
try
{
    RouteResponse result = await routesController.GetRoutesAsync(
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

