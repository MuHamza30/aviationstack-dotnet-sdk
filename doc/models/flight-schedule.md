
# Flight Schedule

## Structure

`FlightSchedule`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `FlightDate` | `DateTime?` | Optional | Date of the flight |
| `FlightStatus` | [`FlightStatusEnum?`](../../doc/models/flight-status-enum.md) | Optional | Status of the flight |
| `Departure` | [`AirportInfo`](../../doc/models/airport-info.md) | Optional | - |
| `Arrival` | [`AirportInfo`](../../doc/models/airport-info.md) | Optional | - |
| `Airline` | [`AirlineInfo`](../../doc/models/airline-info.md) | Optional | - |
| `Flight` | [`FlightInfo`](../../doc/models/flight-info.md) | Optional | - |
| `Aircraft` | [`AircraftInfo`](../../doc/models/aircraft-info.md) | Optional | - |

## Example (as JSON)

```json
{
  "flight_date": "2016-03-13",
  "flight_status": "incident",
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
  },
  "airline": {
    "name": "name2",
    "iata": "iata4",
    "icao": "icao4"
  }
}
```

