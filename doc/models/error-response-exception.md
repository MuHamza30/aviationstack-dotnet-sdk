
# Error Response Exception

## Structure

`ErrorResponseException`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Error` | [`Error`](../../doc/models/error.md) | Required | - |

## Example (as JSON)

```json
{
  "error": {
    "code": "code2",
    "message": "message4",
    "details": {
      "key1": "val1",
      "key2": "val2"
    }
  }
}
```

