# TrackStat2

## Example Usage

```typescript
import { TrackStat2 } from "daydream-test/models/operations";

let value: TrackStat2 = {
  type: "<value>",
  jitter: 6322.94,
  packetsLost: 522206,
  packetsReceived: 456702,
  packetLossPct: 5636.71,
  rtt: 2310.74,
};
```

## Fields

| Field                                   | Type                                    | Required                                | Description                             |
| --------------------------------------- | --------------------------------------- | --------------------------------------- | --------------------------------------- |
| `type`                                  | *string*                                | :heavy_check_mark:                      | RTP codec type, e.g. 'audio' or 'video' |
| `jitter`                                | *number*                                | :heavy_check_mark:                      | N/A                                     |
| `packetsLost`                           | *number*                                | :heavy_check_mark:                      | N/A                                     |
| `packetsReceived`                       | *number*                                | :heavy_check_mark:                      | N/A                                     |
| `packetLossPct`                         | *number*                                | :heavy_check_mark:                      | N/A                                     |
| `rtt`                                   | *number*                                | :heavy_check_mark:                      | Round trip time in nanoseconds          |
| `warnings`                              | *string*[]                              | :heavy_minus_sign:                      | N/A                                     |
| `additionalProperties`                  | Record<string, *any*>                   | :heavy_minus_sign:                      | N/A                                     |