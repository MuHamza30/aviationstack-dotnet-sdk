# Airplanes

Using `airplanes` endpoint, you can get the information about Airplanes like Registration number, Production line, etc.

```csharp
AirplanesController airplanesController = client.AirplanesController;
```

## Class Name

`AirplanesController`


# Get Airplanes

Retrieve airplane data

```csharp
GetAirplanesAsync(
    string accessKey,
    int? limit = 100,
    int? offset = 0,
    string iataTypeCode = null,
    string registrationNumber = null)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accessKey` | `string` | Query, Required | Your AviationStack API access key |
| `limit` | `int?` | Query, Optional | Number of results to return<br><br>**Default**: `100` |
| `offset` | `int?` | Query, Optional | Number of results to skip<br><br>**Default**: `0` |
| `iataTypeCode` | `string` | Query, Optional | IATA type code |
| `registrationNumber` | `string` | Query, Optional | Aircraft registration number |

## Response Type

[`Task<Models.AirplaneResponse>`](../../doc/models/airplane-response.md)

## Example Usage

```csharp
string accessKey = "access_key8";
int? limit = 100;
int? offset = 0;
try
{
    AirplaneResponse result = await airplanesController.GetAirplanesAsync(
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

