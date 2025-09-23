<!-- Start SDK Example Usage [usage] -->
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
<!-- End SDK Example Usage [usage] -->