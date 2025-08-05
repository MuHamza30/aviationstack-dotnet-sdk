
# Airline Response

## Structure

`AirlineResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Pagination` | [`Pagination`](../../doc/models/pagination.md) | Required | - |
| `Data` | [`List<Airline>`](../../doc/models/airline.md) | Required | - |

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
      "airline_name": "airline_name8",
      "iata_code": "iata_code4",
      "icao_code": "icao_code8",
      "fleet_size": "fleet_size0",
      "fleet_average_age": "fleet_average_age0"
    }
  ]
}
```

