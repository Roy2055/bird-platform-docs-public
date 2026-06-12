# Frontend

The frontend is built with Expo, React Native, TypeScript, and Expo Router.

## Main app areas

- bird browsing
- bird detail
- add prediction
- update prediction
- predictions list
- community
- analytics
- settings

## UI priorities in the project

- phone-first layout refinement
- real-device testing on iPhone
- keyboard-aware form handling
- consistent theme support
- support and moderation visibility inside the app
- a clear split between end-user mobile flows and browser-based admin operations

## Separate admin web

There is also a browser-based admin client for:

- species media management
- support-ticket review
- content moderation review
- trust and safety review

It is designed as the primary admin surface.

In coding terms:

- the mobile app stays focused on end-user flows
- the admin web handles operational support, moderation, and enforcement workflows
