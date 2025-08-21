
# Client Class Documentation

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| Timeout | `TimeSpan` | Http client timeout.<br>*Default*: `TimeSpan.FromSeconds(100)` |
| HttpClientConfiguration | [`Action<HttpClientConfiguration.Builder>`](../doc/http-client-configuration-builder.md) | Action delegate that configures the HTTP client by using the HttpClientConfiguration.Builder for customizing API call settings.<br>*Default*: `new HttpClient()` |
| CustomQueryAuthenticationCredentials | [`CustomQueryAuthenticationCredentials`](auth/custom-query-parameter.md) | The Credentials Setter for Custom Query Parameter |

The API client can be initialized as follows:

```csharp
using Aviationstack.Standard;
using Aviationstack.Standard.Authentication;

namespace ConsoleApp;

AviationstackClient client = new AviationstackClient.Builder()
    .CustomQueryAuthenticationCredentials(
        new CustomQueryAuthenticationModel.Builder(
            "access_key"
        )
        .Build())
    .Build();
```

## AviationstackClient Class

The gateway for the SDK. This class acts as a factory for the Controllers and also holds the configuration of the SDK.

### Controllers

| Name | Description |
|  --- | --- |
| FlightsController | Gets FlightsController controller. |
| RoutesController | Gets RoutesController controller. |
| AirportsController | Gets AirportsController controller. |
| AirlinesController | Gets AirlinesController controller. |
| AirplanesController | Gets AirplanesController controller. |
| AircraftTypesController | Gets AircraftTypesController controller. |
| TaxesController | Gets TaxesController controller. |
| CitiesController | Gets CitiesController controller. |
| CountriesController | Gets CountriesController controller. |
| FlightSchedulesController | Gets FlightSchedulesController controller. |
| FlightFutureSchedulesController | Gets FlightFutureSchedulesController controller. |

### Properties

| Name | Description | Type |
|  --- | --- | --- |
| HttpClientConfiguration | Gets the configuration of the Http Client associated with this client. | [`IHttpClientConfiguration`](../doc/http-client-configuration.md) |
| Timeout | Http client timeout. | `TimeSpan` |
| Environment | Current API environment. | `Environment` |
| CustomQueryAuthenticationCredentials | Gets the credentials to use with CustomQueryAuthentication. | [`ICustomQueryAuthenticationCredentials`](auth/custom-query-parameter.md) |

### Methods

| Name | Description | Return Type |
|  --- | --- | --- |
| `GetBaseUri(Server alias = Server.Default)` | Gets the URL for a particular alias in the current environment and appends it with template parameters. | `string` |
| `ToBuilder()` | Creates an object of the AviationstackClient using the values provided for the builder. | `Builder` |

## AviationstackClient Builder Class

Class to build instances of AviationstackClient.

### Methods

| Name | Description | Return Type |
|  --- | --- | --- |
| `HttpClientConfiguration(Action<`[`HttpClientConfiguration.Builder`](../doc/http-client-configuration-builder.md)`> action)` | Gets the configuration of the Http Client associated with this client. | `Builder` |
| `Timeout(TimeSpan timeout)` | Http client timeout. | `Builder` |
| `Environment(Environment environment)` | Current API environment. | `Builder` |
| `CustomQueryAuthenticationCredentials(Action<CustomQueryAuthenticationModel.Builder> action)` | Sets credentials for CustomQueryAuthentication. | `Builder` |

