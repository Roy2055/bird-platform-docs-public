# Backend

The backend is built in Python with FastAPI and supports both product features and admin workflows.

## Main responsibilities

- authenticate users
- expose bird species APIs
- create, update, list, and delete predictions
- support community sharing, ratings, reactions, and comments
- support support-message workflows
- support moderation case workflows
- resolve Firebase-backed media URLs
- enforce prediction image moderation rules
- support account deletion and media cleanup

## Notable backend design areas

- prediction and community APIs
- user feedback and admin reply flow
- moderation reporting and workflow management
- Firebase media signing and storage-path resolution
- cleanup of orphaned or deleted prediction media
- bird question and recognition-related support flows
