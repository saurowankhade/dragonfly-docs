# Dragonfly Documentation

Official documentation for **Dragonfly**, a free REST API client for Visual Studio Code. Dragonfly lets you send HTTP requests, organize them into collections, and scan your Express and Next.js code to build the requests for you, all without leaving the editor.

- Website: https://usedragonfly.xyz
- VS Code Marketplace: https://marketplace.visualstudio.com/items?itemName=saurabhwankhade.dragonfly
- Install command: `ext install saurabhwankhade.dragonfly`

## What is Dragonfly

Dragonfly is a REST API client built into VS Code and a lightweight alternative to Postman, Thunder Client and Insomnia. Most API clients hand you a blank request and wait for a URL. Dragonfly reads your project first: run a scan and it picks up your Express and Next.js routes, then turns them into a collection foldered to match your codebase, so the endpoints you already wrote are ready to send.

Everything stays on your machine. Collections, environments and request history live in VS Code storage, and tokens go into VS Code secure storage. No account, no sign in, no paid tier, no telemetry. MIT licensed.

## Key features

- **Request builder** for method, URL, params, headers, body and auth, docked in the Activity Bar
- **Route discovery** that scans Express and Next.js routes (App Router and Pages Router) and builds a collection from them
- **Collection import** from Postman, Thunder Client, Insomnia and HAR
- **OpenAPI and Swagger import**, one request per operation grouped into folders by tag
- **cURL import** that fills the request form from a pasted command
- **Environments** with `{{variable}}` substitution and one-click switching
- **Authentication** with Bearer Token, API Key and Basic Auth, secrets kept in VS Code secure storage
- **Copy as code** to export any request as cURL, Node.js, Python, Go, PHP, Java or Rust
- **Request history** saved automatically to the Activity view

## Documentation

This site is built with [Mintlify](https://mintlify.com). Pages are MDX files with YAML frontmatter, and configuration lives in `docs.json`.

| Section | Pages |
| --- | --- |
| Get started | Introduction, Quickstart |
| Guides | Route discovery, Request builder, Collections and environments, Authentication, Importing, Copy as code, Request history |
| Reference | Commands, How it compares, FAQ, Changelog |

## Local development

Install the [Mintlify CLI](https://www.npmjs.com/package/mint):

```bash
npm i -g mint
```

Run the dev server from the project root, where `docs.json` lives:

```bash
mint dev
```

Preview at `http://localhost:3000`. Check internal links before publishing:

```bash
mint broken-links
```

## Frequently asked questions

**How do I test an API endpoint inside VS Code?**
Install Dragonfly, open it from the Activity Bar, build a request with a method, URL, headers, body and auth, then press Send. The response opens next to your code.

**Can it find the API routes in my project automatically?**
Yes. Run Scan Workspace for Routes and Dragonfly parses your Express and Next.js source, then builds a collection from what it finds.

**Is Dragonfly free?**
Yes. No account, no paid tier, no telemetry. MIT licensed.

## Feedback

Dragonfly is in beta. Send bug reports and feature requests to saurowankhade@gmail.com.
