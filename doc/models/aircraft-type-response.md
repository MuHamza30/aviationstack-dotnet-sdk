
# Aircraft Type Response

## Structure

`AircraftTypeResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Pagination` | [`Pagination`](../../doc/models/pagination.md) | Required | - |
| `Data` | [`List<AircraftType>`](../../doc/models/aircraft-type.md) | Required | - |

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
      "iata_code": "iata_code4",
      "aircraft_name": "aircraft_name4"
    }
  ]
}
```

