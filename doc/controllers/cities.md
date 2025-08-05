# Cities

Using `cities` endpoint, you can look up at destination cities.

```csharp
CitiesController citiesController = client.CitiesController;
```

## Class Name

`CitiesController`


# Get Cities

Retrieve city data

```csharp
GetCitiesAsync(
    string accessKey,
    int? limit = 100,
    int? offset = 0,
    string countryCode = null,
    string cityName = null)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accessKey` | `string` | Query, Required | Your AviationStack API access key |
| `limit` | `int?` | Query, Optional | Number of results to return<br><br>**Default**: `100` |
| `offset` | `int?` | Query, Optional | Number of results to skip<br><br>**Default**: `0` |
| `countryCode` | `string` | Query, Optional | Country code |
| `cityName` | `string` | Query, Optional | City name |

## Response Type

[`Task<Models.CityResponse>`](../../doc/models/city-response.md)

## Example Usage

```csharp
string accessKey = "access_key8";
int? limit = 100;
int? offset = 0;
try
{
    CityResponse result = await citiesController.GetCitiesAsync(
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

