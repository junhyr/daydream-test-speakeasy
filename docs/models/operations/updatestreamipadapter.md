# UpdateStreamIpAdapter

IP adapter — Turns on IP-Adapter style conditioning and is fully hot-swappable. Available for SDXL, SDXL-faceid, SD1.5

## Example Usage

```typescript
import { UpdateStreamIpAdapter } from "daydream-test/models/operations";

let value: UpdateStreamIpAdapter = {
  scale: 7568.21,
  enabled: true,
};
```

## Fields

| Field                                                                                                                                      | Type                                                                                                                                       | Required                                                                                                                                   | Description                                                                                                                                |
| ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------ |
| `scale`                                                                                                                                    | *number*                                                                                                                                   | :heavy_check_mark:                                                                                                                         | N/A                                                                                                                                        |
| `enabled`                                                                                                                                  | *boolean*                                                                                                                                  | :heavy_check_mark:                                                                                                                         | N/A                                                                                                                                        |
| `type`                                                                                                                                     | [operations.UpdateStreamType](../../models/operations/updatestreamtype.md)                                                                 | :heavy_minus_sign:                                                                                                                         | Type of IP adapter. Use 'faceid' for SDXL-faceid models, 'regular' for others                                                              |
| `weightType`                                                                                                                               | [operations.UpdateStreamWeightType](../../models/operations/updatestreamweighttype.md)                                                     | :heavy_minus_sign:                                                                                                                         | Weight interpolation method for IP adapter style conditioning. Controls how the style influence changes throughout the generation process. |