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

## Admin report workspace

The browser-based admin client is designed to support a report-management workflow rather than just a list of forms.

That workspace now maps moderation and trust-and-safety cases into:

- pipeline-style stage columns
- ticket cards with lane/type badges
- queue-health summary metrics
- searchable case lists
- a selected-ticket detail panel with lifecycle timeline

This keeps the visual model aligned with the underlying workflow:

- report creation
- triage
- review
- decision
- enforcement
- closure
