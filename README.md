# GitHub Action Trigger Repository - action-repo

This repository is designed to trigger GitHub webhook events such as pull requests, merges, and other repository activities. These events are sent to an external webhook listener service (e.g., your `webhook-repo`) for processing and storage.

---

## Purpose

- Serve as a source of GitHub webhook events for testing and development
- Trigger events like pull requests, merges, and pushes to test webhook listeners
- Work alongside a webhook receiver service to demonstrate full webhook flow

---

## How It Works

- When pull requests are created, updated, merged, or closed in this repo, GitHub automatically generates webhook events
- These events are sent to the webhook listener configured in the repo’s **Settings > Webhooks**
- The webhook listener processes these events (e.g., filtering merged PRs, storing event data)

---

## Usage

1. Fork or clone this repo.

2. Configure the webhook in **Settings > Webhooks**:
   - Payload URL: The URL of your webhook listener service (`webhook-repo`)
   - Content type: `application/json`
   - Select individual events like `Pull requests` or `Push` as needed

3. Create or merge pull requests in this repo to trigger webhook events.

---

## Notes

- This repo contains no backend code; it is purely for generating webhook events.
- Use this repo in combination with a webhook listener to test and demo webhook handling.

---

## Author

Prashant Kumar  
[GitHub Profile](https://github.com/prashantkumar4217)

