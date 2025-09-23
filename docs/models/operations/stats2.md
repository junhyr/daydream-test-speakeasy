# Stats2

## Example Usage

```typescript
import { Stats2 } from "daydream-test/models/operations";

let value: Stats2 = {
  peerConnStats: {
    id: "<id>",
    bytesReceived: 17152,
    bytesSent: 458202,
  },
  connQuality: "bad",
};
```

## Fields

| Field                                                                  | Type                                                                   | Required                                                               | Description                                                            |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `peerConnStats`                                                        | [operations.PeerConnStats2](../../models/operations/peerconnstats2.md) | :heavy_check_mark:                                                     | N/A                                                                    |
| `trackStats`                                                           | [operations.TrackStat2](../../models/operations/trackstat2.md)[]       | :heavy_minus_sign:                                                     | N/A                                                                    |
| `connQuality`                                                          | [operations.ConnQuality2](../../models/operations/connquality2.md)     | :heavy_check_mark:                                                     | Connection quality assessment                                          |
| `additionalProperties`                                                 | Record<string, *any*>                                                  | :heavy_minus_sign:                                                     | N/A                                                                    |