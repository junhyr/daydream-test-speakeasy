# IngestMetrics2

## Example Usage

```typescript
import { IngestMetrics2 } from "daydream-test/models/operations";

let value: IngestMetrics2 = {
  stats: {
    peerConnStats: {
      id: "<id>",
      bytesReceived: 17152,
      bytesSent: 458202,
    },
    connQuality: "good",
  },
};
```

## Fields

| Field                                                  | Type                                                   | Required                                               | Description                                            |
| ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ |
| `stats`                                                | [operations.Stats2](../../models/operations/stats2.md) | :heavy_check_mark:                                     | N/A                                                    |
| `additionalProperties`                                 | Record<string, *any*>                                  | :heavy_minus_sign:                                     | N/A                                                    |