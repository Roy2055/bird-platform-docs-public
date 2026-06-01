# Firebase And Media

Firebase is used primarily for media storage and signed URL resolution.

## Main media responsibilities

- prediction image uploads
- prediction sound uploads
- species media storage
- signed URL generation for app consumption
- moderation-aware prediction image workflow

## Prediction image moderation path

```mermaid
flowchart TD
    A["User selects image"] --> B["Upload to pending storage"]
    B --> C["Moderation workflow evaluates image"]
    C --> D{"Approved?"}
    D -->|Yes| E["Move to approved storage"]
    D -->|No| F["Reject upload"]
    E --> G["Backend returns approved media path"]
    G --> H["Prediction can be saved"]
```

## Cleanup maturity

The platform also includes cleanup support so deleted predictions and deleted accounts do not leave media behind unnecessarily.
