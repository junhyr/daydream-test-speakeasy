# TrackStat1

## Example Usage

```typescript
import { TrackStat1 } from "daydream-test/models/operations";

let value: TrackStat1 = {
  type: "<value>",
  jitter: 4485.04,
  packetsLost: 895053,
  packetsReceived: 842263,
  packetLossPct: 8158.52,
  rtt: 7239.93,
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