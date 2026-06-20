# Lightpanda (lightpanda)

Lightpanda is an open-source headless browser built from scratch in Zig for AI agents and large-scale automation. It is not a REST API; its programmable interface is the Chrome DevTools Protocol (CDP) exposed over a WebSocket endpoint, making it a drop-in target for Puppeteer, Playwright, and chromedp clients. It ships as an open-source binary/CLI (AGPL-3.0) and as Lightpanda Cloud, a managed CDP browser service.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/lightpanda/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/lightpanda/refs/heads/main/apis.yml)

## Tags

- Headless Browser
- Browser Automation
- CDP
- WebSocket
- AI Agents
- Web Scraping

## Timestamps

- **Created:** 2026-06-20
- **Modified:** 2026-06-20

## APIs

### Lightpanda CDP WebSocket Interface

Lightpanda's primary programmable interface. The browser runs as a CDP server (`lightpanda serve`) and exposes the Chrome DevTools Protocol over a WebSocket endpoint (default `ws://127.0.0.1:9222`). CDP is a bidirectional JSON-RPC wire protocol over WebSocket - not a REST API. Existing Puppeteer, Playwright, and chromedp scripts connect by pointing `browserWSEndpoint` / `connectOverCDP` at this endpoint instead of Chrome.

- **Human URL:** [https://lightpanda.io/docs](https://lightpanda.io/docs)
- **Base URL:** `ws://127.0.0.1:9222`

#### Tags

- CDP
- WebSocket
- Browser Automation
- Puppeteer
- Playwright

#### Properties

- [Documentation](https://lightpanda.io/docs)
- [GitHub](https://github.com/lightpanda-io/browser)
- [AsyncAPI](asyncapi/lightpanda-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [OpenAPI](openapi/lightpanda-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Lightpanda Cloud

Managed, hosted CDP browser endpoints reached over secure WebSocket (e.g. `wss://euwest.cloud.lightpanda.io/ws`, `wss://uswest.cloud.lightpanda.io/ws`). Authentication is a `token` query-string parameter; query parameters such as `browser=lightpanda|chrome` and `proxy` select the browser engine and egress. Clients connect with the same Puppeteer/Playwright/chromedp CDP tooling. Cloud access is request-based; usage pricing is not publicly reconciled.

- **Human URL:** [https://lightpanda.io/docs/cloud-offer/tools/cdp](https://lightpanda.io/docs/cloud-offer/tools/cdp)
- **Base URL:** `wss://cloud.lightpanda.io/ws`

#### Tags

- Cloud
- Managed Browser
- CDP
- WebSocket

#### Properties

- [Documentation](https://lightpanda.io/docs/cloud-offer/tools/cdp)
- [Website](https://lightpanda.io)
- [AsyncAPI](asyncapi/lightpanda-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)

### Lightpanda CLI / Binary

The open-source command-line binary (AGPL-3.0, written in Zig). `lightpanda serve` starts the CDP-over-WebSocket server; `lightpanda fetch` retrieves and dumps a URL as HTML or markdown; `lightpanda agent` drives the browser with LLM instructions. Distributed via one-line installer, Docker images, and nightly Linux/macOS binaries.

- **Human URL:** [https://github.com/lightpanda-io/browser](https://github.com/lightpanda-io/browser)
- **Base URL:** `https://github.com/lightpanda-io/browser`

#### Tags

- CLI
- Binary
- Fetch
- Agent

#### Properties

- [Documentation](https://lightpanda.io/docs)
- [GitHub](https://github.com/lightpanda-io/browser)

## Common Properties

- [GitHub Organization](https://github.com/lightpanda-io)
- [LinkedIn](https://www.linkedin.com/company/lightpanda)
- [Website](https://lightpanda.io)
- [Documentation](https://lightpanda.io/docs)
- [Plans](plans/lightpanda-plans-pricing.yml)
- [Rate Limits](rate-limits/lightpanda-rate-limits.yml)
- [Fin Ops](finops/lightpanda-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
