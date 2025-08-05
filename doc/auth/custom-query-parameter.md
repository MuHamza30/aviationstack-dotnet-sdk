
# Custom Query Parameter



Documentation for accessing and setting credentials for ApiKeyAuth.

## Auth Credentials

| Name | Type | Description | Setter | Getter |
|  --- | --- | --- | --- | --- |
| access_key | `string` | Your AviationStack API access key | `AccessKey` | `AccessKey` |



**Note:** Auth credentials can be set using `CustomQueryAuthenticationCredentials` in the client builder and accessed through `CustomQueryAuthenticationCredentials` method in the client instance.

## Usage Example

### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

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


