# IngestMetrics1

## Example Usage

```typescript
import { IngestMetrics1 } from "daydream-test/models/operations";

let value: IngestMetrics1 = {
  stats: {
    peerConnStats: {
      id: "<id>",
      bytesReceived: 475229,
      bytesSent: 496116,
    },
    connQuality: "bad",
  },
};
```

## Fields

| Field                                                  | Type                                                   | Required                                               | Description                                            |
| ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ |
| `stats`                                                | [operations.Stats1](../../models/operations/stats1.md) | :heavy_check_mark:                                     | N/A                                                    |
| `additionalProperties`                                 | Record<string, *any*>                                  | :heavy_minus_sign:                                     | N/A                                                    |