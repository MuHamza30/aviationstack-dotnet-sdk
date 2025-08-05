
# Getting Started with Aviationstack

## Introduction

AviationStack API provides real-time and historical aviation data including flights, airports, airlines, and more.
This API allows you to access comprehensive aviation information for various use cases.

## Install the Package

If you are building with .NET CLI tools then you can also use the following command:

```bash
dotnet add package Aviation-stack-Api --version 1.0.0
```

You can also view the package at:
https://www.nuget.org/packages/Aviation-stack-Api/1.0.0

## Initialize the API Client

**_Note:_** Documentation for the client can be found [here.](https://www.github.com/MuHamza30/aviationstack-dotnet-sdk/tree/1.0.0/doc/client.md)

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| Timeout | `TimeSpan` | Http client timeout.<br>*Default*: `TimeSpan.FromSeconds(100)` |
| HttpClientConfiguration | [`Action<HttpClientConfiguration.Builder>`](https://www.github.com/MuHamza30/aviationstack-dotnet-sdk/tree/1.0.0/doc/http-client-configuration-builder.md) | Action delegate that configures the HTTP client by using the HttpClientConfiguration.Builder for customizing API call settings.<br>*Default*: `new HttpClient()` |
| CustomQueryAuthenticationCredentials | [`CustomQueryAuthenticationCredentials`](https://www.github.com/MuHamza30/aviationstack-dotnet-sdk/tree/1.0.0/doc/auth/custom-query-parameter.md) | The Credentials Setter for Custom Query Parameter |

The API client can be initialized as follows:

```csharp
using Aviationstack.Standard;
using Aviationstack.Standard.Authentication;

AviationstackClient client = new AviationstackClient.Builder()
    .CustomQueryAuthenticationCredentials(
        new CustomQueryAuthenticationModel.Builder(
            "access_key"
        )
        .Build())
    .Build();
```

## Authorization

This API uses the following authentication schemes.

* [`ApiKeyAuth (Custom Query Parameter)`](https://www.github.com/MuHamza30/aviationstack-dotnet-sdk/tree/1.0.0/doc/auth/custom-query-parameter.md)

## List of APIs

* [Aircraft Types](https://www.github.com/MuHamza30/aviationstack-dotnet-sdk/tree/1.0.0/doc/controllers/aircraft-types.md)
* [Flight Schedules](https://www.github.com/MuHamza30/aviationstack-dotnet-sdk/tree/1.0.0/doc/controllers/flight-schedules.md)
* [Flight Future Schedules](https://www.github.com/MuHamza30/aviationstack-dotnet-sdk/tree/1.0.0/doc/controllers/flight-future-schedules.md)
* [Flights](https://www.github.com/MuHamza30/aviationstack-dotnet-sdk/tree/1.0.0/doc/controllers/flights.md)
* [Routes](https://www.github.com/MuHamza30/aviationstack-dotnet-sdk/tree/1.0.0/doc/controllers/routes.md)
* [Airports](https://www.github.com/MuHamza30/aviationstack-dotnet-sdk/tree/1.0.0/doc/controllers/airports.md)
* [Airlines](https://www.github.com/MuHamza30/aviationstack-dotnet-sdk/tree/1.0.0/doc/controllers/airlines.md)
* [Airplanes](https://www.github.com/MuHamza30/aviationstack-dotnet-sdk/tree/1.0.0/doc/controllers/airplanes.md)
* [Taxes](https://www.github.com/MuHamza30/aviationstack-dotnet-sdk/tree/1.0.0/doc/controllers/taxes.md)
* [Cities](https://www.github.com/MuHamza30/aviationstack-dotnet-sdk/tree/1.0.0/doc/controllers/cities.md)
* [Countries](https://www.github.com/MuHamza30/aviationstack-dotnet-sdk/tree/1.0.0/doc/controllers/countries.md)

## SDK Infrastructure

### Configuration

* [HttpClientConfiguration](https://www.github.com/MuHamza30/aviationstack-dotnet-sdk/tree/1.0.0/doc/http-client-configuration.md)
* [HttpClientConfigurationBuilder](https://www.github.com/MuHamza30/aviationstack-dotnet-sdk/tree/1.0.0/doc/http-client-configuration-builder.md)
* [ProxyConfigurationBuilder](https://www.github.com/MuHamza30/aviationstack-dotnet-sdk/tree/1.0.0/doc/proxy-configuration-builder.md)

### HTTP

* [HttpCallback](https://www.github.com/MuHamza30/aviationstack-dotnet-sdk/tree/1.0.0/doc/http-callback.md)
* [HttpContext](https://www.github.com/MuHamza30/aviationstack-dotnet-sdk/tree/1.0.0/doc/http-context.md)
* [HttpRequest](https://www.github.com/MuHamza30/aviationstack-dotnet-sdk/tree/1.0.0/doc/http-request.md)
* [HttpResponse](https://www.github.com/MuHamza30/aviationstack-dotnet-sdk/tree/1.0.0/doc/http-response.md)
* [HttpStringResponse](https://www.github.com/MuHamza30/aviationstack-dotnet-sdk/tree/1.0.0/doc/http-string-response.md)

### Utilities

* [ApiException](https://www.github.com/MuHamza30/aviationstack-dotnet-sdk/tree/1.0.0/doc/api-exception.md)
* [ApiHelper](https://www.github.com/MuHamza30/aviationstack-dotnet-sdk/tree/1.0.0/doc/api-helper.md)
* [CustomDateTimeConverter](https://www.github.com/MuHamza30/aviationstack-dotnet-sdk/tree/1.0.0/doc/custom-date-time-converter.md)
* [UnixDateTimeConverter](https://www.github.com/MuHamza30/aviationstack-dotnet-sdk/tree/1.0.0/doc/unix-date-time-converter.md)

