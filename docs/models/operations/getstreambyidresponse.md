# GetStreamByIdResponse

Default Response

## Example Usage

```typescript
import { GetStreamByIdResponse } from "daydream-test/models/operations";

let value: GetStreamByIdResponse = {
  id: "<id>",
  streamKey: "<value>",
  outputStreamUrl: "https://frugal-integer.info/",
  pipelineParams: {
    "key": "<value>",
    "key1": "<value>",
  },
  createdAt: "1710853711616",
  pipelineId: "<id>",
  outputPlaybackId: "<id>",
  name: "<value>",
  author: "<value>",
  fromPlayground: true,
  gatewayHost: "<value>",
  isSmokeTest: true,
  whipUrl: "https://whirlwind-label.com/",
};
```

## Fields

| Field                                                         | Type                                                          | Required                                                      | Description                                                   |
| ------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------- |
| `id`                                                          | *string*                                                      | :heavy_check_mark:                                            | Unique identifier for the stream                              |
| `streamKey`                                                   | *string*                                                      | :heavy_check_mark:                                            | Unique key used for streaming to this endpoint                |
| `outputStreamUrl`                                             | *string*                                                      | :heavy_check_mark:                                            | URL where the processed stream output can be accessed         |
| `pipelineParams`                                              | Record<string, *any*>                                         | :heavy_check_mark:                                            | Current configuration parameters for the stream pipeline      |
| `createdAt`                                                   | *string*                                                      | :heavy_check_mark:                                            | ISO timestamp when the stream was created                     |
| `pipelineId`                                                  | *string*                                                      | :heavy_check_mark:                                            | ID of the processing pipeline being used                      |
| `outputPlaybackId`                                            | *string*                                                      | :heavy_check_mark:                                            | Playback ID for accessing the stream output                   |
| `name`                                                        | *string*                                                      | :heavy_check_mark:                                            | Human-readable name of the stream                             |
| `author`                                                      | *string*                                                      | :heavy_check_mark:                                            | ID of the user who created this stream                        |
| `fromPlayground`                                              | *boolean*                                                     | :heavy_check_mark:                                            | Whether this stream was created from the playground interface |
| `gatewayHost`                                                 | *string*                                                      | :heavy_check_mark:                                            | Gateway server hostname handling this stream                  |
| `isSmokeTest`                                                 | *boolean*                                                     | :heavy_check_mark:                                            | Whether this is a smoke test stream                           |
| `whipUrl`                                                     | *string*                                                      | :heavy_check_mark:                                            | WebRTC WHIP URL for stream ingestion                          |