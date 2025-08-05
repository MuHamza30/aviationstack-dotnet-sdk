
# Airport Info

## Structure

`AirportInfo`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Airport` | `string` | Optional | Airport name |
| `Timezone` | `string` | Optional | Timezone |
| `Iata` | `string` | Optional | IATA code |
| `Icao` | `string` | Optional | ICAO code |
| `Terminal` | `string` | Optional | Terminal |
| `Gate` | `string` | Optional | Gate |
| `Delay` | `int?` | Optional | Delay in minutes |
| `Scheduled` | `DateTime?` | Optional | Scheduled time |
| `Estimated` | `DateTime?` | Optional | Estimated time |
| `Actual` | `DateTime?` | Optional | Actual time |
| `EstimatedRunway` | `DateTime?` | Optional | Estimated runway time |
| `ActualRunway` | `DateTime?` | Optional | Actual runway time |

## Example (as JSON)

```json
{
  "airport": "airport2",
  "timezone": "timezone6",
  "iata": "iata0",
  "icao": "icao0",
  "terminal": "terminal4"
}
```

