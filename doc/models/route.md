
# Route

## Structure

`Route`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Airline` | [`AirlineInfo`](../../doc/models/airline-info.md) | Optional | - |
| `Departure` | [`AirportInfo`](../../doc/models/airport-info.md) | Optional | - |
| `Arrival` | [`AirportInfo`](../../doc/models/airport-info.md) | Optional | - |

## Example (as JSON)

```json
{
  "airline": {
    "name": "name2",
    "iata": "iata4",
    "icao": "icao4"
  },
  "departure": {
    "airport": "airport6",
    "timezone": "timezone0",
    "iata": "iata6",
    "icao": "icao4",
    "terminal": "terminal8"
  },
  "arrival": {
    "airport": "airport2",
    "timezone": "timezone6",
    "iata": "iata0",
    "icao": "icao0",
    "terminal": "terminal4"
  }
}
```

