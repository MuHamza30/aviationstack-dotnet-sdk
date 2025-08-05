
# Live Info

## Structure

`LiveInfo`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Updated` | `DateTime?` | Optional | Last update time |
| `Latitude` | `double?` | Optional | Current latitude |
| `Longitude` | `double?` | Optional | Current longitude |
| `Altitude` | `double?` | Optional | Current altitude |
| `Direction` | `double?` | Optional | Current direction |
| `SpeedHorizontal` | `double?` | Optional | Horizontal speed |
| `SpeedVertical` | `double?` | Optional | Vertical speed |
| `IsGround` | `bool?` | Optional | Whether aircraft is on ground |

## Example (as JSON)

```json
{
  "updated": "2016-03-13T12:52:32.123Z",
  "latitude": 51.58,
  "longitude": 49.38,
  "altitude": 168.94,
  "direction": 193.8
}
```

