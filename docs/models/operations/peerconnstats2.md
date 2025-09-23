# PeerConnStats2

## Example Usage

```typescript
import { PeerConnStats2 } from "daydream-test/models/operations";

let value: PeerConnStats2 = {
  id: "<id>",
  bytesReceived: 829656,
  bytesSent: 736594,
};
```

## Fields

| Field                  | Type                   | Required               | Description            |
| ---------------------- | ---------------------- | ---------------------- | ---------------------- |
| `id`                   | *string*               | :heavy_check_mark:     | Peer connection ID     |
| `bytesReceived`        | *number*               | :heavy_check_mark:     | Total bytes received   |
| `bytesSent`            | *number*               | :heavy_check_mark:     | Total bytes sent       |
| `additionalProperties` | Record<string, *any*>  | :heavy_minus_sign:     | N/A                    |