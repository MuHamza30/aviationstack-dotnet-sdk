
# Airplane Response

## Structure

`AirplaneResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Pagination` | [`Pagination`](../../doc/models/pagination.md) | Required | - |
| `Data` | [`List<Airplane>`](../../doc/models/airplane.md) | Required | - |

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
      "registration_number": "registration_number2",
      "production_line": "production_line0",
      "iata_type_code": "iata_type_code8",
      "model_name": "model_name0",
      "model_code": "model_code6"
    }
  ]
}
```

