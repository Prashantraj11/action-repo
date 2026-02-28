# action-repo

This repository is used as the source of GitHub webhook events for the [webhook-repo](https://github.com/Prashantraj11/webhook-repo) project.

## Purpose

A GitHub Webhook is configured on this repository to send event notifications to a Flask backend whenever any of the following actions occur:

- **Push** -- code is pushed to any branch
- **Pull Request** -- a pull request is opened, updated, or closed
- **Merge** -- a pull request is merged

The webhook sends a POST request with the event payload to the Flask backend, which parses and stores the data in MongoDB.

## Webhook Configuration

- **Payload URL:** `https://<ngrok-url>/webhook`
- **Content type:** `application/json`
- **Events:** Pushes, Pull requests

## Related Repository

- **webhook-repo:** https://github.com/Prashantraj11/webhook-repo
  Contains the Flask backend, MongoDB integration, and frontend UI.
