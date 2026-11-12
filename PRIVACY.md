# Privacy Policy for MCP Server Inspector & Spec Auditor (Chrome Extension)

**Last Updated:** November 12, 2026  
**Author:** Markus van Kempen  
**Website:** [Research | Floor 7½ 🏢🤏](https://markusvankempen.github.io/)

---

## 1. Overview & Single-Purpose Commitment

The **MCP Server Inspector & Spec Auditor** is a developer workbench and specification auditor designed to test, inspect, and evaluate **Model Context Protocol (MCP)** servers, tool JSONSchemas, and progressive disclosure groups.

We are firmly committed to user privacy. The extension operates as a local client-side developer tool.

---

## 2. Data Collection and Usage

### What We Collect
- **Zero Personal Data:** We do **not** collect, store, transmit, profile, or sell any personal identifying information (PII), browsing history, search records, or telemetry.
- **No Third-Party Analytics:** We do not use third-party analytics services (such as Google Analytics or tracking pixels) or advertising SDKs.

### Local Storage Usage (`chrome.storage.local`)
To provide a smooth developer experience, the extension stores configuration items strictly locally on your device:
- **Server Target URLs:** MCP endpoints entered by the user (e.g. `http://localhost:3000/mcp`).
- **Authentication Headers:** User-provided `Authorization` tokens, `X-API-Key` values, `Mcp-Session-Id` identifiers, and custom header JSON objects.
- **Active Settings:** Selected preset endpoints and user UI preferences.

All stored data remains on your local machine and is **never** synchronized to external servers or accessible to third parties.

---

## 3. Network Communications

- **Direct Server Communication:** Network requests (`POST`, `GET`, `OPTIONS`) are initiated **only** when you explicitly connect to a server, execute a tool call, run the specification audit, or test JSON-RPC commands.
- **Destination:** Outbound network requests are sent directly from your browser exclusively to the user-specified target server endpoint or standard public GitHub API (only if you click "Fetch Official GitHub README").
- **No Proxying:** Communications do not route through any intermediary proxy servers operated by the extension author.

---

## 4. Permissions Justification

| Permission | Purpose & Justification |
|---|---|
| `storage` & `unlimitedStorage` | Used solely to persist user-configured endpoints, test configurations, and custom authentication headers locally within the browser. |
| `host_permissions` (`localhost`, `127.0.0.1`, demo server) and `optional_host_permissions` (`http://*/*`, `https://*/*`) | Local development servers and the built-in demo server are available at install. Access to any other MCP server is requested per origin, at runtime, only when you click Connect and approve Chrome's prompt. It can be revoked at any time from `chrome://extensions`. |
| `declarativeNetRequestWithHostAccess` | Registers a single session rule that removes the `Origin` header from the extension's own MCP requests so servers that reject browser origins respond as they would to a standard MCP client. It does not block, redirect, or read any traffic, and does not affect other sites or extensions. |

---

## 5. Security & Best Practices

- We encourage developers to connect to secure endpoints (`https://`) when testing remote servers across the public internet.
- Authentication tokens stored locally are retained only in your Chrome local extension storage sandbox.
- You can clear stored authentication tokens and headers at any time from the **Auth & Headers** tab inside the extension.

---

## 6. Open Source & License

The MCP Server Inspector & Spec Auditor is open-source software licensed under the **Apache License 2.0**. You can inspect the complete source code and verify our privacy practices.

---

## 7. Contact & Inquiries

For questions or feedback regarding this privacy policy or the extension:
- **Author:** Markus van Kempen
- **Research Portal:** [https://markusvankempen.github.io/](https://markusvankempen.github.io/)
- **Repository:** [https://github.com/markusvankempen/mcp-ticket-demo](https://github.com/markusvankempen/mcp-ticket-demo)
