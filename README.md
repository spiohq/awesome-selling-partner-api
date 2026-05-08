# Awesome Selling Partner API [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Curated developer resources for the Amazon Selling Partner API (SP-API): libraries, tools, guides, and communities.

The Selling Partner API is Amazon's REST-based suite of APIs for sellers and vendors. This list focuses on what **developers** need to build SP-API integrations: official documentation, actively-maintained client libraries, infrastructure tooling, and learning material.

**Out of scope:** seller-facing SaaS products (repricers, inventory tools, analytics dashboards), Amazon advertising tooling, and anything that isn't directly useful when writing code against SP-API. Inactive projects are pruned regularly; see the contribution guidelines for the maintenance criteria.

## Contents

- [Official Resources](#official-resources)
  - [Documentation and Reference](#documentation-and-reference)
  - [Official SDKs and Models](#official-sdks-and-models)
  - [Sample Solutions and Tooling](#sample-solutions-and-tooling)
  - [Policy and Compliance](#policy-and-compliance)
- [Client Libraries](#client-libraries)
  - [PHP](#php)
  - [Node.js and TypeScript](#nodejs-and-typescript)
  - [Python](#python)
  - [Java](#java)
  - [C# and .NET](#c-and-net)
  - [Go](#go)
  - [Ruby](#ruby)
  - [Rust](#rust)
- [Developer Tooling](#developer-tooling)
  - [Proxies and Gateways](#proxies-and-gateways)
  - [Notifications and Event Pipelines](#notifications-and-event-pipelines)
  - [Code Generation](#code-generation)
- [Guides and Tutorials](#guides-and-tutorials)
- [Video Content](#video-content)
- [Communities](#communities)
- [Disclosure](#disclosure)

## Official Resources

### Documentation and Reference

- [SP-API Documentation Portal](https://developer-docs.amazon.com/sp-api) - Full reference for every API, schema, and use case.
- [SP-API Release Notes](https://developer-docs.amazon.com/sp-api/docs/sp-api-release-notes) - Authoritative changelog with RSS feed.
- [SP-API Changelog](https://developer-docs.amazon.com/sp-api/changelog) - Breaking-change announcements and deprecation timelines.
- [Usage Plans and Rate Limits](https://developer-docs.amazon.com/sp-api/docs/usage-plans-and-rate-limits) - Token-bucket algorithm reference.
- [Strategies to Optimize Rate Limits](https://developer-docs.amazon.com/sp-api-blog/docs/strategies-to-optimize-rate-limits-for-your-application-workloads) - Throttling strategies, dynamic plans, and batch patterns.
- [Selling Partner API Blog](https://developer-docs.amazon.com/sp-api-blog/docs) - Implementation notes, architecture guidance, and use-case deep dives from the SP-API team.

### Official SDKs and Models

- [amzn/selling-partner-api-models](https://github.com/amzn/selling-partner-api-models) - OpenAPI models, JSON schemas, and Java + C# auth/auth helper libraries. The authoritative source for all SP-API specs.
- [amzn/selling-partner-api-sdk](https://github.com/amzn/selling-partner-api-sdk) - Official prebuilt SDKs for Java, PHP, JavaScript, Python, and C#. Apache-2.0.
- [SP-API SDKs overview](https://developer-docs.amazon.com/sp-api/docs/sp-api-sdks) - When to choose a prebuilt SDK versus a generated one.

### Sample Solutions and Tooling

- [amzn/selling-partner-api-samples](https://github.com/amzn/selling-partner-api-samples) - End-to-end sample solutions (pricing, B2B repricing, FBA inbound, Data Kiosk, listings) deployable on AWS, plus Jupyter labs and code recipes.
- [Using Postman for SP-API](https://developer-docs.amazon.com/sp-api/docs/using-postman-for-selling-partner-api-models) - Official Postman workspace and pre-built flows.
- [SP-API on AWS Quick Start](https://aws-ia.github.io/cfn-ps-amazon-selling-partner-api/) - CloudFormation Partner Solution provisioning IAM role and sample Lambda.
- [Data Kiosk Schema Explorer Guide](https://developer-docs.amazon.com/sp-api/docs/schema-explorer-guide) - Building GraphQL queries interactively against published schemas.

### Policy and Compliance

- [Security and Compliance Overview](https://developer-docs.amazon.com/sp-api/docs/security-compliance-overview) - DPP and AUP requirements summary.
- [Key Security Controls Guidance](https://developer-docs.amazon.com/sp-api/docs/guidance-to-address-key-security-controls-in-sp-api-integration) - DPP control mapping with concrete implementation steps.
- [Updates to the Data Protection Policy and Acceptable Use Policy](https://developer-docs.amazon.com/sp-api/changelog/updates-to-the-data-protection-policy-and-acceptable-use-policy) - November 2025 update introducing "Solution Provider" terminology.

## Client Libraries

Only actively-maintained libraries are listed. "Actively maintained" means a release within the last 12 months and tracking of recent SP-API model changes. Inactive projects (such as `clousale/amazon-sp-api-php`, `ScaleLeap/selling-partner-api-sdk`, and `ericcj/amz_sp_api`) have been pruned.

### PHP

- [jlevers/selling-partner-api](https://github.com/jlevers/selling-partner-api) - Modern Saloon-based PHP 8.2+ client with DTOs, full Seller and Vendor coverage, and automatic Restricted Data Token handling. BSD-3-Clause.
- [amazon-php/sp-api-sdk](https://github.com/amazon-php/sp-api-sdk) - Early-stage PSR-compliant SDK designed to pass Amazon DPP audits, with strict semantic-versioning around Amazon's BC breaks. MIT.
- [highsidelabs/laravel-spapi](https://github.com/highsidelabs/laravel-spapi) - Laravel wrapper around `jlevers/selling-partner-api` with multi-seller credential management. BSD-3-Clause.
- [amzn/selling-partner-api-sdk (PHP)](https://github.com/amzn/selling-partner-api-sdk/tree/main/php) - Amazon's official PHP 8.3+ SDK with built-in rate limiter and RDT support. Apache-2.0.

### Node.js and TypeScript

- [jrl84/amazon-sp-api](https://github.com/jrl84/amazon-sp-api) - Most-installed community client (`amazon-sp-api` on npm) with internal rate limiting, automatic token refresh, and report download helpers.
- [bizon/selling-partner-api-sdk](https://github.com/bizon/selling-partner-api-sdk) - Modular TypeScript SDK with per-API packages (`@sp-api-sdk/*`), auto-generated types, dual CJS/ESM output, and notification/report/feed schemas.
- [amzn/selling-partner-api-sdk (JavaScript)](https://github.com/amzn/selling-partner-api-sdk/tree/main/javascript) - Amazon's official JavaScript SDK with built-in rate limiter. Apache-2.0.

### Python

- [saleweaver/python-amazon-sp-api](https://github.com/saleweaver/python-amazon-sp-api) - The most widely used Python client, with httpx-based transport, Data Kiosk support, and active monthly releases. PyPI: `python-amazon-sp-api`.
- [amzn/selling-partner-api-sdk (Python)](https://github.com/amzn/selling-partner-api-sdk/tree/main/python) - Amazon's official Python SDK. Apache-2.0.

### Java

- [amzn/selling-partner-api-sdk (Java)](https://github.com/amzn/selling-partner-api-sdk/tree/main/java) - Amazon's official Java SDK with built-in rate limiter and RDT support; the best starting point for Java integrations. Apache-2.0.
- [amzn/selling-partner-api-models — sellingpartner-api-aa-java](https://github.com/amzn/selling-partner-api-models/tree/main/clients/sellingpartner-api-aa-java) - Official auth-and-auth helper library, used when generating clients via swagger-codegen against the OpenAPI models.

### C# and .NET

- [abuzuhri/Amazon-SP-API-CSharp](https://github.com/abuzuhri/Amazon-SP-API-CSharp) - The dominant community .NET library (`FikaAmazonAPI`), tracking recent SP-API versions including FBA Inbound v2024-03-20.
- [amzn/selling-partner-api-sdk (C#)](https://github.com/amzn/selling-partner-api-sdk/tree/main/csharp) - Amazon's official C# SDK (`software.amzn.spapi` on NuGet). Apache-2.0.
- [amzn/selling-partner-api-models — sellingpartner-api-aa-csharp](https://github.com/amzn/selling-partner-api-models/tree/main/clients/sellingpartner-api-aa-csharp) - Official auth-and-auth helper library for use with swagger-codegen-generated C# clients.

### Go

- [amzapi/selling-partner-api-sdk](https://github.com/amzapi/selling-partner-api-sdk) - Go toolkit using oapi-codegen, with sample code for Sellers, Reports, Orders, and Listings.
- [fond-of-vertigo/amazon-sp-api](https://github.com/fond-of-vertigo/amazon-sp-api) - Hand-maintained Go client with broad API coverage (Authorization, Catalog, FBA, Feeds, Finances, Listings, Orders, Reports, Tokens, and more); includes golangci-lint and race-detector CI. Apache-2.0.
- [renabled/amzn-sp-api-go](https://github.com/renabled/amzn-sp-api-go) - Auto-generated Go client rebuilt twice daily from `amzn/selling-partner-api-models` via a scheduled CI workflow, keeping it current with every SP-API model change. MIT.

### Ruby

- [lineofflight/peddler](https://github.com/lineofflight/peddler) - Ruby interface auto-generated from the latest OpenAPI models, covering all SP-API endpoints, reports, notifications, feeds, and Data Kiosk. Lightweight via Zeitwerk; provides type-safe response parsing.

### Rust

> ⚠️ Rust support for SP-API is early-stage. The crate below is the only currently-published option, with fewer than 1k total downloads as of May 2026. Treat as experimental; consider generating a client via `oapi-codegen` from `amzn/selling-partner-api-models` instead.

- [houxd/amazon-spapi](https://github.com/houxd/amazon-spapi) - Rust client library for SP-API (`amazon-spapi` on crates.io). MIT.

## Developer Tooling

### Proxies and Gateways

- [Spio Smart Proxy](https://github.com/spiohq/smart-proxy) - Open-source SP-API reverse proxy with per-account token-bucket rate limiting, response caching, automatic Restricted Data Token minting, and built-in DPP-compliant PII redaction. Single Go binary, embedded SQLite, dashboard. AGPL-3.0. Maintained by the curator (see [Disclosure](#disclosure)).

### Notifications and Event Pipelines

- [Notifications API v1 Use Case Guide](https://developer-docs.amazon.com/sp-api/docs/notifications-api-v1-use-case-guide) - Official setup guide for SQS and EventBridge destinations.
- [Set up notifications using SQS](https://developer-docs.amazon.com/sp-api/docs/set-up-notifications-with-amazon-sqs) - Step-by-step SQS workflow including IAM permission templates.
- [Build Event-Driven Architecture with SP-API](https://developer-docs.amazon.com/sp-api/docs/sp-api-event-driven-architecture) - EventBridge-based notification pipeline overview and tutorial.

### Code Generation

- [highsidelabs/saloon-sdk-generator](https://github.com/highsidelabs/saloon-sdk-generator) - PHP SDK generator built on Saloon, used to generate `jlevers/selling-partner-api` from the OpenAPI specs.
- [oapi-codegen](https://github.com/oapi-codegen/oapi-codegen) - Go code generator from OpenAPI 3.x specs; the recommended approach for generating Go SP-API clients from `amzn/selling-partner-api-models`.
- [OpenAPI Generator](https://openapi-generator.tech/) - Multi-language generator used by the official Amazon SDKs and many community libraries; supports 50+ target languages.

## Guides and Tutorials

- [Building Listings Management Workflows](https://developer-docs.amazon.com/sp-api/docs/building-listings-management-workflows-guide) - Official guide for migrating to JSON listings feeds and the Listings Items API.
- [Listings Management Workflow Migration](https://developer-docs.amazon.com/sp-api/docs/listings-management-workflow-migration) - Official migration reference mapping legacy XML/flat-file feeds to `JSON_LISTINGS_FEED` and the Listings Items API, with field-level data mapping tables.
- [Tutorial: Automate SP-API Calls Using the Python SDK](https://developer-docs.amazon.com/sp-api/docs/tutorial-automate-your-sp-api-calls-using-python-sdk) - Official step-by-step tutorial covering LWA token exchange, client generation from the OpenAPI models, and a working Orders API example.
- [Data Kiosk Workflow Guide](https://developer-docs.amazon.com/sp-api/docs/data-kiosk-workflow-guide) - End-to-end workflow for GraphQL-based reporting.
- [Pell Software: Developing with the SP-API](https://www.pellsoftware.com/developing-amazon-sp-api/) - First-time Node.js integration walkthrough.
- [Highside Labs documentation](https://docs.highsidelabs.co/) - Feed Transformer and SP-API Starter Kit docs, plus multi-seller patterns and Laravel integration deep-dives.
- [Deltologic SP-API guide](https://www.deltologic.com/blog/a-step-by-step-guide-to-understanding-and-using-amazons-selling-partner-api) - Multi-module video course covering setup through Notifications.

## Video Content

- [SP-API Developer University on YouTube](https://www.youtube.com/@amazon-sp-api) - Amazon's official channel with webinars, demos, and fireside chats.
- [SP-API Developer University Hub](https://developer.amazonservices.com/developer-university) - On-demand webinar index with topic filtering.

## Communities

- [amzn/selling-partner-api-models GitHub Discussions](https://github.com/amzn/selling-partner-api-models/discussions) - The most active SP-API technical forum, with responses from Amazon Solutions Architects.
- [Stack Overflow: amazon-selling-partner-api tag](https://stackoverflow.com/questions/tagged/amazon-selling-partner-api) - Q&A archive.
- [Spio Community](https://spiohq.com) - Discourse instance for SP-API developers, run by the curator (see [Disclosure](#disclosure)).

## Disclosure

This list is maintained by Stefan, founder of Spio. Two of the entries are projects I am personally involved with: **Spio Smart Proxy** under Proxies and Gateways, and the **Spio Community** under Communities. Spio Smart Proxy is the only purpose-built open-source SP-API reverse proxy out there, and there is no comparable developer community to point readers to. Both follow the same inclusion criteria as every other entry, and contributors are welcome to PR for their removal if they no longer meet the bar.

## Contributing

Contributions are welcome. Read the [contribution guidelines](CONTRIBUTING.md) first. The list prunes inactive libraries and seller-facing tooling; please check the criteria before opening a PR.

---

To the extent possible under law, the curator has waived all copyright and related or neighboring rights to this work.
[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)
