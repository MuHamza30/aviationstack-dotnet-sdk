
# Flight Schedule Response

## Structure

`FlightScheduleResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Pagination` | [`Pagination`](../../doc/models/pagination.md) | Required | - |
| `Data` | [`List<FlightSchedule>`](../../doc/models/flight-schedule.md) | Required | - |

## Example (as JSON)

```json
{
  "pagination": {
    "limit": 80,
    "offset": 240,
    "count": 192,
    "total": 242
  },
  "data": [
    {
      "flight_date": "2016-03-13",
      "flight_status": "landed",
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
  ]
}
```

