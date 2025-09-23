# Streams
(*streams*)

## Overview

### Available Operations

* [createStream](#createstream) - Create a new stream
* [getAllStreams](#getallstreams) - Get all streams for user
* [deleteStream](#deletestream) - Delete a stream
* [updateStream](#updatestream) - Update a stream
* [getStreamById](#getstreambyid) - Get stream by ID
* [getStreamStatus](#getstreamstatus) - Get stream status

## createStream

Creates a new video processing stream with the specified configuration

### Example Usage

<!-- UsageSnippet language="typescript" operationID="createStream" method="post" path="/v1/streams" -->
```typescript
import { DaydreamTest } from "daydream-test";

const daydreamTest = new DaydreamTest({
  bearer: process.env["DAYDREAMTEST_BEARER"] ?? "",
});

async function run() {
  const result = await daydreamTest.streams.createStream();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { DaydreamTestCore } from "daydream-test/core.js";
import { streamsCreateStream } from "daydream-test/funcs/streamsCreateStream.js";

// Use `DaydreamTestCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const daydreamTest = new DaydreamTestCore({
  bearer: process.env["DAYDREAMTEST_BEARER"] ?? "",
});

async function run() {
  const res = await streamsCreateStream(daydreamTest);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("streamsCreateStream failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.CreateStreamRequest](../../models/operations/createstreamrequest.md)                                                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.CreateStreamResponse](../../models/operations/createstreamresponse.md)\>**

### Errors

| Error Type                             | Status Code                            | Content Type                           |
| -------------------------------------- | -------------------------------------- | -------------------------------------- |
| errors.CreateStreamBadRequestError     | 400                                    | application/json                       |
| errors.CreateStreamInternalServerError | 500                                    | application/json                       |
| errors.DaydreamTestDefaultError        | 4XX, 5XX                               | \*/\*                                  |

## getAllStreams

Retrieves all streams belonging to the authenticated user

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getAllStreams" method="get" path="/v1/streams" -->
```typescript
import { DaydreamTest } from "daydream-test";

const daydreamTest = new DaydreamTest({
  bearer: process.env["DAYDREAMTEST_BEARER"] ?? "",
});

async function run() {
  const result = await daydreamTest.streams.getAllStreams();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { DaydreamTestCore } from "daydream-test/core.js";
import { streamsGetAllStreams } from "daydream-test/funcs/streamsGetAllStreams.js";

// Use `DaydreamTestCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const daydreamTest = new DaydreamTestCore({
  bearer: process.env["DAYDREAMTEST_BEARER"] ?? "",
});

async function run() {
  const res = await streamsGetAllStreams(daydreamTest);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("streamsGetAllStreams failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetAllStreamsRequest](../../models/operations/getallstreamsrequest.md)                                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetAllStreamsResponse](../../models/operations/getallstreamsresponse.md)\>**

### Errors

| Error Type                              | Status Code                             | Content Type                            |
| --------------------------------------- | --------------------------------------- | --------------------------------------- |
| errors.GetAllStreamsBadRequestError     | 400                                     | application/json                        |
| errors.GetAllStreamsInternalServerError | 500                                     | application/json                        |
| errors.DaydreamTestDefaultError         | 4XX, 5XX                                | \*/\*                                   |

## deleteStream

Deletes a specific stream by ID for the authenticated user

### Example Usage

<!-- UsageSnippet language="typescript" operationID="deleteStream" method="delete" path="/v1/streams" -->
```typescript
import { DaydreamTest } from "daydream-test";

const daydreamTest = new DaydreamTest({
  bearer: process.env["DAYDREAMTEST_BEARER"] ?? "",
});

async function run() {
  const result = await daydreamTest.streams.deleteStream({
    id: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { DaydreamTestCore } from "daydream-test/core.js";
import { streamsDeleteStream } from "daydream-test/funcs/streamsDeleteStream.js";

// Use `DaydreamTestCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const daydreamTest = new DaydreamTestCore({
  bearer: process.env["DAYDREAMTEST_BEARER"] ?? "",
});

async function run() {
  const res = await streamsDeleteStream(daydreamTest, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("streamsDeleteStream failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.DeleteStreamRequest](../../models/operations/deletestreamrequest.md)                                                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.DeleteStreamResponse](../../models/operations/deletestreamresponse.md)\>**

### Errors

| Error Type                             | Status Code                            | Content Type                           |
| -------------------------------------- | -------------------------------------- | -------------------------------------- |
| errors.DeleteStreamNotFoundError       | 404                                    | application/json                       |
| errors.DeleteStreamInternalServerError | 500                                    | application/json                       |
| errors.DaydreamTestDefaultError        | 4XX, 5XX                               | \*/\*                                  |

## updateStream

Updates pipeline parameters for a specific stream by ID for the authenticated user

### Example Usage

<!-- UsageSnippet language="typescript" operationID="updateStream" method="patch" path="/v1/streams/{id}" -->
```typescript
import { DaydreamTest } from "daydream-test";

const daydreamTest = new DaydreamTest({
  bearer: process.env["DAYDREAMTEST_BEARER"] ?? "",
});

async function run() {
  const result = await daydreamTest.streams.updateStream({
    id: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { DaydreamTestCore } from "daydream-test/core.js";
import { streamsUpdateStream } from "daydream-test/funcs/streamsUpdateStream.js";

// Use `DaydreamTestCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const daydreamTest = new DaydreamTestCore({
  bearer: process.env["DAYDREAMTEST_BEARER"] ?? "",
});

async function run() {
  const res = await streamsUpdateStream(daydreamTest, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("streamsUpdateStream failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.UpdateStreamRequest](../../models/operations/updatestreamrequest.md)                                                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.UpdateStreamResponse](../../models/operations/updatestreamresponse.md)\>**

### Errors

| Error Type                             | Status Code                            | Content Type                           |
| -------------------------------------- | -------------------------------------- | -------------------------------------- |
| errors.UpdateStreamBadRequestError     | 400                                    | application/json                       |
| errors.UpdateStreamNotFoundError       | 404                                    | application/json                       |
| errors.UpdateStreamInternalServerError | 500                                    | application/json                       |
| errors.DaydreamTestDefaultError        | 4XX, 5XX                               | \*/\*                                  |

## getStreamById

Retrieves a specific stream by its ID. Users can only access their own streams unless they have admin privileges.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getStreamById" method="get" path="/v1/streams/{id}" -->
```typescript
import { DaydreamTest } from "daydream-test";

const daydreamTest = new DaydreamTest({
  bearer: process.env["DAYDREAMTEST_BEARER"] ?? "",
});

async function run() {
  const result = await daydreamTest.streams.getStreamById({
    id: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { DaydreamTestCore } from "daydream-test/core.js";
import { streamsGetStreamById } from "daydream-test/funcs/streamsGetStreamById.js";

// Use `DaydreamTestCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const daydreamTest = new DaydreamTestCore({
  bearer: process.env["DAYDREAMTEST_BEARER"] ?? "",
});

async function run() {
  const res = await streamsGetStreamById(daydreamTest, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("streamsGetStreamById failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetStreamByIdRequest](../../models/operations/getstreambyidrequest.md)                                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetStreamByIdResponse](../../models/operations/getstreambyidresponse.md)\>**

### Errors

| Error Type                              | Status Code                             | Content Type                            |
| --------------------------------------- | --------------------------------------- | --------------------------------------- |
| errors.GetStreamByIdBadRequestError     | 400                                     | application/json                        |
| errors.GetStreamByIdNotFoundError       | 404                                     | application/json                        |
| errors.GetStreamByIdInternalServerError | 500                                     | application/json                        |
| errors.DaydreamTestDefaultError         | 4XX, 5XX                                | \*/\*                                   |

## getStreamStatus

Gets the status of a specific stream

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getStreamStatus" method="get" path="/v1/streams/{id}/status" -->
```typescript
import { DaydreamTest } from "daydream-test";

const daydreamTest = new DaydreamTest({
  bearer: process.env["DAYDREAMTEST_BEARER"] ?? "",
});

async function run() {
  const result = await daydreamTest.streams.getStreamStatus({
    id: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { DaydreamTestCore } from "daydream-test/core.js";
import { streamsGetStreamStatus } from "daydream-test/funcs/streamsGetStreamStatus.js";

// Use `DaydreamTestCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const daydreamTest = new DaydreamTestCore({
  bearer: process.env["DAYDREAMTEST_BEARER"] ?? "",
});

async function run() {
  const res = await streamsGetStreamStatus(daydreamTest, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("streamsGetStreamStatus failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetStreamStatusRequest](../../models/operations/getstreamstatusrequest.md)                                                                                         | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetStreamStatusResponse](../../models/operations/getstreamstatusresponse.md)\>**

### Errors

| Error Type                                | Status Code                               | Content Type                              |
| ----------------------------------------- | ----------------------------------------- | ----------------------------------------- |
| errors.GetStreamStatusBadRequestError     | 400                                       | application/json                          |
| errors.GetStreamStatusNotFoundError       | 404                                       | application/json                          |
| errors.GetStreamStatusInternalServerError | 500                                       | application/json                          |
| errors.DaydreamTestDefaultError           | 4XX, 5XX                                  | \*/\*                                     |