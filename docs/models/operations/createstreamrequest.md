# CreateStreamRequest

## Example Usage

```typescript
import { CreateStreamRequest } from "daydream-test/models/operations";

let value: CreateStreamRequest = {};
```

## Fields

| Field                                                                  | Type                                                                   | Required                                                               | Description                                                            |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `pipelineId`                                                           | *operations.PipelineId*                                                | :heavy_minus_sign:                                                     | ID of the processing pipeline to use for this stream                   |
| `pipelineParams`                                                       | [operations.PipelineParams](../../models/operations/pipelineparams.md) | :heavy_minus_sign:                                                     | Configuration parameters for the selected pipeline                     |
| `name`                                                                 | *string*                                                               | :heavy_minus_sign:                                                     | Human-readable name for the stream                                     |
| `outputRtmpUrl`                                                        | *string*                                                               | :heavy_minus_sign:                                                     | Custom RTMP URL for stream output destination                          |