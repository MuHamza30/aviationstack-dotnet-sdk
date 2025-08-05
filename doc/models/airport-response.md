
# Airport Response

## Structure

`AirportResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Pagination` | [`Pagination`](../../doc/models/pagination.md) | Required | - |
| `Data` | [`List<Airport>`](../../doc/models/airport.md) | Required | - |

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
      "airport_name": "airport_name6",
      "iata_code": "iata_code4",
      "icao_code": "icao_code8",
      "latitude": 34.34,
      "longitude": 32.14
    }
  ]
}
```

