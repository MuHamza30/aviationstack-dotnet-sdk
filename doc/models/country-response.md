
# Country Response

## Structure

`CountryResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Pagination` | [`Pagination`](../../doc/models/pagination.md) | Required | - |
| `Data` | [`List<Country>`](../../doc/models/country.md) | Required | - |

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
      "country_name": "country_name2",
      "country_code": "country_code0",
      "country_iso2": "country_iso22",
      "country_iso3": "country_iso32"
    }
  ]
}
```

