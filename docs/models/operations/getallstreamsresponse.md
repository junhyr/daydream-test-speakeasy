# GetAllStreamsResponse

Default Response

## Example Usage

```typescript
import { GetAllStreamsResponse } from "daydream-test/models/operations";

let value: GetAllStreamsResponse = {
  success: false,
  data: [],
};
```

## Fields

| Field                              | Type                               | Required                           | Description                        |
| ---------------------------------- | ---------------------------------- | ---------------------------------- | ---------------------------------- |
| `success`                          | *boolean*                          | :heavy_check_mark:                 | Whether the request was successful |
| `data`                             | *any*[]                            | :heavy_check_mark:                 | Array of stream objects            |