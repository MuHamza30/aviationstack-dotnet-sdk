
# Tax Response

## Structure

`TaxResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Pagination` | [`Pagination`](../../doc/models/pagination.md) | Required | - |
| `Data` | [`List<Tax>`](../../doc/models/tax.md) | Required | - |

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
      "tax_name": "tax_name8",
      "tax_code": "tax_code8",
      "country_code": "country_code0",
      "country_name": "country_name2"
    }
  ]
}
```

