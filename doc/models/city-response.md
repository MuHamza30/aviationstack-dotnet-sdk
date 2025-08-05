
# City Response

## Structure

`CityResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Pagination` | [`Pagination`](../../doc/models/pagination.md) | Required | - |
| `Data` | [`List<City>`](../../doc/models/city.md) | Required | - |

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
      "city_name": "city_name6",
      "city_code": "city_code0",
      "country_code": "country_code0",
      "country_name": "country_name2"
    }
  ]
}
```

