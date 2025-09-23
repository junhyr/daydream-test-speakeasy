# GetStreamStatusData1

## Example Usage

```typescript
import { GetStreamStatusData1 } from "daydream-test/models/operations";

let value: GetStreamStatusData1 = {
  streamId: "<id>",
  requestId: "<id>",
  pipelineId: "<id>",
};
```

## Fields

| Field                                                                      | Type                                                                       | Required                                                                   | Description                                                                |
| -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| `streamId`                                                                 | *string*                                                                   | :heavy_check_mark:                                                         | Stream identifier                                                          |
| `requestId`                                                                | *string*                                                                   | :heavy_check_mark:                                                         | Gateway request identifier                                                 |
| `pipelineId`                                                               | *string*                                                                   | :heavy_check_mark:                                                         | Pipeline identifier                                                        |
| `type`                                                                     | *string*                                                                   | :heavy_minus_sign:                                                         | Event type (e.g. 'status')                                                 |
| `orchestratorInfo`                                                         | [operations.OrchestratorInfo](../../models/operations/orchestratorinfo.md) | :heavy_minus_sign:                                                         | N/A                                                                        |
| `inferenceStatus`                                                          | [operations.InferenceStatus](../../models/operations/inferencestatus.md)   | :heavy_minus_sign:                                                         | N/A                                                                        |
| `gatewayStatus`                                                            | [operations.GatewayStatus1](../../models/operations/gatewaystatus1.md)     | :heavy_minus_sign:                                                         | N/A                                                                        |
| `pipeline`                                                                 | *string*                                                                   | :heavy_minus_sign:                                                         | Model/pipeline name (if present)                                           |
| `additionalProperties`                                                     | Record<string, *any*>                                                      | :heavy_minus_sign:                                                         | N/A                                                                        |