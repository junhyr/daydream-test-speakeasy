# UpdateStreamPromptInterpolationMethod

Method for interpolating between multiple prompts. Slerp provides smoother transitions than linear.

## Example Usage

```typescript
import { UpdateStreamPromptInterpolationMethod } from "daydream-test/models/operations";

let value: UpdateStreamPromptInterpolationMethod = "linear";
```

## Values

```typescript
"linear" | "slerp"
```