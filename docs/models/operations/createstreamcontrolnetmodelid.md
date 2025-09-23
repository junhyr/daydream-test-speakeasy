# CreateStreamControlnetModelId

⚠️ NOTE: ControlNet model_ids must be unique. Additionally, they must be compatible with the selected base model.

## Example Usage

```typescript
import { CreateStreamControlnetModelId } from "daydream-test/models/operations";

let value: CreateStreamControlnetModelId =
  "lllyasviel/control_v11f1e_sd15_tile";
```

## Values

```typescript
"thibaud/controlnet-sd21-openpose-diffusers" | "thibaud/controlnet-sd21-hed-diffusers" | "thibaud/controlnet-sd21-canny-diffusers" | "thibaud/controlnet-sd21-depth-diffusers" | "thibaud/controlnet-sd21-color-diffusers" | "lllyasviel/control_v11f1p_sd15_depth" | "lllyasviel/control_v11f1e_sd15_tile" | "lllyasviel/control_v11p_sd15_canny" | "xinsir/controlnet-depth-sdxl-1.0" | "xinsir/controlnet-canny-sdxl-1.0" | "xinsir/controlnet-tile-sdxl-1.0"
```