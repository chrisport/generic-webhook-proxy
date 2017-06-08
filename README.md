# Generic Webhook Proxy 

## Basic idea
Have this server running to receive webhooks from any other service (e.g. Github), store its result and let other services poll results. For further capabilities see To do.

## To do:
Base:
- Dynamically create callback endpoints (via API)
- Store callbacks in-memory
- Provide interface to poll result

Enhancements:
- Provide per-hook options on callback endpoint creation and later via management-API
  - TTL after hook is received
  - generate or define path
  - password-protect receive-endpoint
  - filter stored content (maybe you just want one field or you don't need the actual content at all, [Stormpath](https://stormpath.com/blog/linking-and-resource-expansion-rest-api-tips))
- provide adapter for using different dbs instead of storing the hooks in-memory
- provide webhook multiplexing capabilities
- provide interface to modify existing hooks:
  - add upstream webhooks that are triggered (multiplex webhook)
  - change/set properties from callback creation
- provide interface for general settings:
  - Authentication
  - List/Delete registered hooks

Projects with related ideas:
- Multiplexing Heroku WebHooks in Go: https://github.com/jelder/bownse
