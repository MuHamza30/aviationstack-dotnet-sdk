# Taxes

Using `taxes` endpoint, you can get the data about different aviation taxes.

```csharp
TaxesController taxesController = client.TaxesController;
```

## Class Name

`TaxesController`


# Get Taxes

Retrieve aviation tax data

```csharp
GetTaxesAsync(
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
| `iataCode` | `string` | Query, Optional | IATA code |

## Response Type

[`Task<Models.TaxResponse>`](../../doc/models/tax-response.md)

## Example Usage

```csharp
string accessKey = "access_key8";
int? limit = 100;
int? offset = 0;
try
{
    TaxResponse result = await taxesController.GetTaxesAsync(
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

