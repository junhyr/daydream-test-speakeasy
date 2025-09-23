# InferenceStatus

## Example Usage

```typescript
import { InferenceStatus } from "daydream-test/models/operations";

let value: InferenceStatus = {};
```

## Fields

| Field                     | Type                      | Required                  | Description               |
| ------------------------- | ------------------------- | ------------------------- | ------------------------- |
| `pipeline`                | *string*                  | :heavy_minus_sign:        | N/A                       |
| `startTime`               | *number*                  | :heavy_minus_sign:        | Unix seconds              |
| `lastParamsUpdateTime`    | *number*                  | :heavy_minus_sign:        | Unix seconds              |
| `lastParams`              | *any*                     | :heavy_minus_sign:        | Model/pipeline parameters |
| `lastParamsHash`          | *string*                  | :heavy_minus_sign:        | N/A                       |
| `inputFps`                | *number*                  | :heavy_minus_sign:        | N/A                       |
| `outputFps`               | *number*                  | :heavy_minus_sign:        | N/A                       |
| `lastInputTime`           | *number*                  | :heavy_minus_sign:        | Unix seconds              |
| `lastOutputTime`          | *number*                  | :heavy_minus_sign:        | Unix seconds              |
| `restartCount`            | *number*                  | :heavy_minus_sign:        | N/A                       |
| `lastRestartTime`         | *number*                  | :heavy_minus_sign:        | Unix seconds              |
| `lastRestartLogs`         | *string*[]                | :heavy_minus_sign:        | N/A                       |
| `lastError`               | *string*                  | :heavy_minus_sign:        | N/A                       |
| `streamId`                | *string*                  | :heavy_minus_sign:        | N/A                       |
| `additionalProperties`    | Record<string, *any*>     | :heavy_minus_sign:        | N/A                       |