# Aircraft Types

```csharp
AircraftTypesController aircraftTypesController = client.AircraftTypesController;
```

## Class Name

`AircraftTypesController`


# Get Aircraft Types

Retrieve aircraft type data

```csharp
GetAircraftTypesAsync(
    string accessKey,
    int? limit = 100,
    int? offset = 0,
    string iataCode = null)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accessKey` | `string` | Query, Required | Your AviationStack API access key |
| `limit` | `int?` | Query, Optional | Number of results to return<br><br>**Default**: `100` |
| `offset` | `int?` | Query, Optional | Number of results to skip<br><br>**Default**: `0` |
| `iataCode` | `string` | Query, Optional | IATA code of the aircraft type |

## Response Type

[`Task<Models.AircraftTypeResponse>`](../../doc/models/aircraft-type-response.md)

## Example Usage

```csharp
string accessKey = "access_key8";
int? limit = 100;
int? offset = 0;
try
{
    AircraftTypeResponse result = await aircraftTypesController.GetAircraftTypesAsync(
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

