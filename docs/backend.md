# Backend

The backend is built in Python with FastAPI and supports both product features and admin workflows.

## Main responsibilities

- authenticate users
- expose bird species APIs
- create, update, list, and delete predictions
- support community sharing, ratings, reactions, and comments
- support support-message workflows
- support moderation case workflows
- support trust and safety enforcement workflows
- log safety signals from report and block actions
- resolve Firebase-backed media URLs
- enforce prediction image moderation rules
- support account deletion and media cleanup

## Notable backend design areas

- prediction and community APIs
- threaded user feedback and admin reply flow
- moderation reporting, severity classification, and workflow management
- trust and safety action storage and safety-signal logging
- Firebase media signing and storage-path resolution
- cleanup of orphaned or deleted prediction media
- bird question and recognition-related support flows

## Support and moderation model

The backend now treats support, moderation, trust and safety, and blocking as related but distinct flows:

- `Comment / complaint`
  - stored as a threaded support ticket
  - stays open until the user is satisfied
- `Report content`
  - auto-classifies severity first
  - records a binary `action taken` or `no action` outcome
- `Report user`
  - supports account-level trust and safety review
  - can record `warn`, `temporary suspend`, or `permanent ban`
- `Block user`
  - applies immediately without a review queue
  - still creates a safety signal for platform analysis

In coding terms, this means the backend no longer treats every user-safety event as the same kind of ticket.
