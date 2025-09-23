# PeerConnStats1

## Example Usage

```typescript
import { PeerConnStats1 } from "daydream-test/models/operations";

let value: PeerConnStats1 = {
  id: "<id>",
  bytesReceived: 334655,
  bytesSent: 120591,
};
```

## Fields

| Field                  | Type                   | Required               | Description            |
| ---------------------- | ---------------------- | ---------------------- | ---------------------- |
| `id`                   | *string*               | :heavy_check_mark:     | Peer connection ID     |
| `bytesReceived`        | *number*               | :heavy_check_mark:     | Total bytes received   |
| `bytesSent`            | *number*               | :heavy_check_mark:     | Total bytes sent       |
| `additionalProperties` | Record<string, *any*>  | :heavy_minus_sign:     | N/A                    |