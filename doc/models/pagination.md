
# Pagination

## Structure

`Pagination`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Limit` | `int` | Required | Number of results per page |
| `Offset` | `int` | Required | Number of results skipped |
| `Count` | `int` | Required | Total number of results |
| `Total` | `int` | Required | Total number of available results |

## Example (as JSON)

```json
{
  "limit": 66,
  "offset": 162,
  "count": 210,
  "total": 160
}
```

