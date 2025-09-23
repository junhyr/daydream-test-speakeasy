# CreateStreamPromptInterpolationMethod

Method for interpolating between multiple prompts. Slerp provides smoother transitions than linear.

## Example Usage

```typescript
import { CreateStreamPromptInterpolationMethod } from "daydream-test/models/operations";

let value: CreateStreamPromptInterpolationMethod = "slerp";
```

## Values

```typescript
"linear" | "slerp"
```