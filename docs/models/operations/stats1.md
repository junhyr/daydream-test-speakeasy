# Stats1

## Example Usage

```typescript
import { Stats1 } from "daydream-test/models/operations";

let value: Stats1 = {
  peerConnStats: {
    id: "<id>",
    bytesReceived: 475229,
    bytesSent: 496116,
  },
  connQuality: "unknown",
};
```

## Fields

| Field                                                                  | Type                                                                   | Required                                                               | Description                                                            |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `peerConnStats`                                                        | [operations.PeerConnStats1](../../models/operations/peerconnstats1.md) | :heavy_check_mark:                                                     | N/A                                                                    |
| `trackStats`                                                           | [operations.TrackStat1](../../models/operations/trackstat1.md)[]       | :heavy_minus_sign:                                                     | N/A                                                                    |
| `connQuality`                                                          | [operations.ConnQuality1](../../models/operations/connquality1.md)     | :heavy_check_mark:                                                     | Connection quality assessment                                          |
| `additionalProperties`                                                 | Record<string, *any*>                                                  | :heavy_minus_sign:                                                     | N/A                                                                    |