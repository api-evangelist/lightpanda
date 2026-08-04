# Lightpanda (lightpanda)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
