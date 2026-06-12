# Architecture

Bird Platform is built as a connected mobile-plus-backend platform with media and moderation layers.

```mermaid
flowchart LR
    App["Mobile App (Expo / React Native)"] --> API["FastAPI Backend"]
    App --> FirebaseClient["Firebase client upload path"]
    FirebaseClient --> Pending["Pending prediction media"]
    Pending --> Moderation["Media moderation workflow"]
    Moderation --> Approved["Approved prediction media"]
    API --> DB["SQLite"]
    API --> FirebaseAdmin["Firebase Admin / signed URLs"]
    AdminWeb["Admin Web"] --> API
    API --> Safety["Safety signals and trust actions"]
```

## Main design choices

- **Prediction-centered data model** for community sharing rather than a separate post model
- **SQLite-backed app database** for portability and simpler project operations
- **Firebase Storage** for media handling and signed URL resolution
- **Forward-only moderation workflow** for clear, auditable admin decisions
- **Separate support, moderation, trust and safety, and block-user lanes** for clearer operational behavior
- **Browser-based admin workspace** as the primary operational admin surface
- **Expo / React Native** for a practical cross-platform mobile workflow
- **FastAPI** for straightforward Python API delivery and integration
