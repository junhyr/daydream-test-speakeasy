# CreateStreamSeedInterpolationMethod

Method for interpolating between multiple seeds. Slerp provides smoother transitions than linear.

## Example Usage

```typescript
import { CreateStreamSeedInterpolationMethod } from "daydream-test/models/operations";

let value: CreateStreamSeedInterpolationMethod = "slerp";
```

## Values

```typescript
"linear" | "slerp"
```