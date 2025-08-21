# Countries

Using `countries` endpoint, you can look up at destination countries.

```csharp
CountriesController countriesController = client.CountriesController;
```

## Class Name

`CountriesController`


# Get Countries

Retrieve country data

```csharp
GetCountriesAsync(
    int? limit = 100,
    int? offset = 0,
    string countryCode = null,
    string countryName = null)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `limit` | `int?` | Query, Optional | Number of results to return<br><br>**Default**: `100` |
| `offset` | `int?` | Query, Optional | Number of results to skip<br><br>**Default**: `0` |
| `countryCode` | `string` | Query, Optional | Country code |
| `countryName` | `string` | Query, Optional | Country name |

## Response Type

[`Task<Models.CountryResponse>`](../../doc/models/country-response.md)

## Example Usage

```csharp
int? limit = 100;
int? offset = 0;
try
{
    CountryResponse result = await countriesController.GetCountriesAsync(
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

