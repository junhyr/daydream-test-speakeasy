# UpdateStreamSeedInterpolationMethod

Method for interpolating between multiple seeds. Slerp provides smoother transitions than linear.

## Example Usage

```typescript
import { UpdateStreamSeedInterpolationMethod } from "daydream-test/models/operations";

let value: UpdateStreamSeedInterpolationMethod = "slerp";
```

## Values

```typescript
"linear" | "slerp"
```