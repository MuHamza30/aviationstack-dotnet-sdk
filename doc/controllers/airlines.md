# Airlines

You can use the API's `airlines` endpoint to get data about airlines operating all over the world

```csharp
AirlinesController airlinesController = client.AirlinesController;
```

## Class Name

`AirlinesController`


# Get Airlines

Retrieve airline data

```csharp
GetAirlinesAsync(
    string accessKey,
    int? limit = 100,
    int? offset = 0,
    string iataCode = null,
    string icaoCode = null,
    string countryCode = null)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accessKey` | `string` | Query, Required | Your AviationStack API access key |
| `limit` | `int?` | Query, Optional | Number of results to return<br><br>**Default**: `100` |
| `offset` | `int?` | Query, Optional | Number of results to skip<br><br>**Default**: `0` |
| `iataCode` | `string` | Query, Optional | IATA code of the airline |
| `icaoCode` | `string` | Query, Optional | ICAO code of the airline |
| `countryCode` | `string` | Query, Optional | Country code |

## Response Type

[`Task<Models.AirlineResponse>`](../../doc/models/airline-response.md)

## Example Usage

```csharp
string accessKey = "access_key8";
int? limit = 100;
int? offset = 0;
try
{
    AirlineResponse result = await airlinesController.GetAirlinesAsync(
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

