# Awesome-HTTP-Traffic-Interception-Capture

# Awesome-HTTP-Traffic-Interception-Capture

# Top HTTP Traffic Interception & Capture Ecosystem

**Curated List of SaaS Platforms & Open-Source GitHub Projects**  
*Focused on MITM Proxying, Request Replay & Self-Hosted Security Workbenches*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **HTTP Traffic Interception & Capture**. These tools help developers and security testers sit between a client and a server—capturing, inspecting, and modifying requests and responses in real time, covering everything from browser-native interceptors to full MITM proxies and Rust-native security workbenches.

**Examples** include mitmproxy, OWASP ZAP, Burp Suite Community, Wireshark, HTTP Toolkit, Requestly, and Perseid (the category leaders).

**Open-source emphasis**: This section highlights every major active project for self-hosted traffic interception, open-source MITM proxies, and community-driven security testing—ideal for teams seeking data sovereignty and avoiding per-seat proxy subscriptions. The open-source landscape is genuinely functional: **mitmproxy** is the scriptable standard for automated interception , **Perseid** is a Rust-native Burp alternative with no JVM overhead , and **Reqlore** offers an accessibility-first pentesting suite .

Contributions welcome! Open an PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

| Product | Description | Pricing (Starting) | Free Tier / Trial Limits |
|---------|-------------|-------------------|--------------------------|
| **[Charles Proxy](https://www.charlesproxy.com/)** | **Long-established desktop MITM proxy with per-host SSL proxying.** A one-time licence covers macOS, Windows, and Linux; 10+ user licences drop to **$30/user** . | **$50 per user** (1–4 licences); Site Licence: **$400** | Free trial with 30-minute session limits |
| **[Fiddler Everywhere](https://www.telerik.com/fiddler)** | Cross-platform debugging proxy with a visual Rules builder. **Commercial use requires a paid subscription**—Lite ($7/user/mo annual) lacks Rules-based traffic manipulation; Pro ($13/user/mo annual) unlocks it . | Pro: **$13/user/month** (annual); Lite: **$7** | Lite plan available; Rules require Pro |
| **[Proxyman](https://proxyman.com/)** | Native macOS/Windows/Linux HTTPS debugging proxy with mock, script, and reverse-proxy capabilities. | **$89 one-time** for 1 seat, 1 year of updates  | Free tier: core capture and inspect; Pro features locked |
| **[Postman Interceptor](https://www.postman.com/)** | Browser extension that captures traffic from the browser and syncs it to Postman. | Included with Postman plans | **Free**: 1 user only (March 2026 restructure) |

## Open-Source GitHub Projects

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[mitmproxy](https://github.com/mitmproxy/mitmproxy)** | [![Stars](https://img.shields.io/github/stars/mitmproxy/mitmproxy?style=social&color=white)](https://github.com/mitmproxy/mitmproxy/stargazers) | **The standard open-source scriptable MITM proxy for automated interception and capture.** **MIT licensed**, Python. **Three interfaces**: `mitmproxy` (interactive console), `mitmweb` (browser UI), and `mitmdump` (headless for CI/scripts) . **Python addons** receive each flow as a mutable object—log, rewrite, mock, or replay traffic programmatically . **TLS interception** via generated CA; per-host decryption control . **Certificate pinning defeats it**—test only against your own apps . **Best for teams wanting programmatic, scriptable interception** in CI pipelines. |
| **[OWASP ZAP](https://github.com/zaproxy/zaproxy)** | [![Stars](https://img.shields.io/github/stars/zaproxy/zaproxy?style=social&color=white)](https://github.com/zaproxy/zaproxy/stargazers) | **The world's most widely deployed open-source DAST proxy.** **Apache-2.0** . **Intercepting proxy with passive scanning (safe) and active scanning (intrusive, test environments only)**. **Baseline scans are CI-ready**—run `zap-baseline.py` on every PR for security header checks without risk . **Official MCP Integration** and optional LLM Support add-ons . **Best for security testing integrated into CI/CD** with a proven, actively maintained codebase. |
| **[Perseid](https://github.com/andyintheshell/perseid)** | [![Stars](https://img.shields.io/github/stars/andyintheshell/perseid?style=social&color=white)](https://github.com/andyintheshell/perseid/stargazers) | **Rust-native Burp Suite alternative—no Java required.** **MIT or Apache-2.0**, **public alpha** with core manual-testing workflows available . **One connected workflow**: capture → inspect → edit → replay, with fuzzing, decoding, and comparison alongside it . **Native desktop app** (Rust/egui) on Linux, macOS, and Windows; no JVM or embedded browser . **HTTP/1.1 and HTTP/2 proxy**, filtered history, target site map, Pretty/Raw/Hex views, and Copy as curl . **Repeater and Intruder** (Sniper, Battering ram, Pitchfork, Cluster bomb) . **WebSocket capture and interception** . **Saves traffic and workbench state in a single `.perseid` project file** . **Trade-off**: prebuilt Windows packages are unsigned; macOS app is ad-hoc signed but not notarized . **Best for security researchers and CTF players** wanting a lightweight Burp-style workflow without JVM overhead. |
| **[Reqlore](https://github.com/ibrasonic/Reqlore)** | [![Stars](https://img.shields.io/github/stars/ibrasonic/Reqlore?style=social&color=white)](https://github.com/ibrasonic/Reqlore/stargazers) | **Accessibility-first web app pentesting suite—a real Burp alternative for screen-reader users.** **Python-native**, local web UI on `127.0.0.1:8787` . **Intercepting MITM proxy** with held-request queue and per-rule filters . **HTTP history** with full search, filter, and export . **Repeater and Intruder** with six engines . **Param miner, GraphQL/WebSocket/SAML/HTTP-2 workbenches**, passive + active scanner with OAST-SSRF check . **JWT workbench** (decode/sign/alg-switch) . **Targets WCAG 2.2 AA** for NVDA, JAWS, Orca, and VoiceOver . **Full unit suite: 2883 passed, 368 skipped** . **Best for security practitioners needing an accessible pentesting suite** without JavaFX barriers. |
| **[OpenSec Studio](https://github.com/saghet/opensec-studio)** | [![Stars](https://img.shields.io/github/stars/saghet/opensec-studio?style=social&color=white)](https://github.com/saghet/opensec-studio/stargazers) | **Ultra-fast Rust-native Burp/ZAP alternative.** **Native Rust**, **<180ms cold boot** and **<95MB RAM** (vs. Burp Pro's 8–15s and 850MB–1.4GB) . **MITM proxy and tamper**, Repeater, Intruder with marker syntax, **Nuclei-compatible YAML vulnerability rules** . **JWT Debugger** detects `alg: none` flaws . **SARIF v2.1.0 export** for CI/CD ingest . **60-day full unrestricted evaluation** . **Best for security researchers wanting a lightweight, fast Burp alternative** with native YAML rule support. |
| **[Wireshark](https://github.com/wireshark/wireshark)** | [![Stars](https://img.shields.io/github/stars/wireshark/wireshark?style=social&color=white)](https://github.com/wireshark/wireshark/stargazers) | **The world's leading network protocol analyzer—a packet sniffer, not an HTTP proxy.** **GPL-2.0** . **Captures everything at the Ethernet frame level**, then lets you filter for `http` to see HTTP traffic . **Shows errors below HTTP** (TCP/IP layer issues) that proxies miss . **Best for diagnosing low-level network problems**—use a proxy (Charles, Fiddler, mitmproxy) when the issue is at the HTTP layer . |

### Additional Strong Open-Source Options

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[HTTP Toolkit](https://github.com/httptoolkit/httptoolkit)** | — | **Polished open-source HTTP(S) debugging proxy and client.** **AGPL-3.0** for UI and desktop wrapper; backend uses Mockttp (Apache-2.0) for powerful mocking . **One-click interception** for browsers, mobile apps, and backend processes . **Cross-platform** (Electron) . **Best for teams wanting a modern GUI** with built-in interception without commercial licensing. |
| **[Requestly](https://github.com/requestly/requestly)** | — | **Browser-native HTTP interception and API mocking without proxy setup.** Trusted by 300,000+ developers; acquired by BrowserStack in May 2025 . **Open-source core** (AGPL desktop-interceptor source); the separate API Client is proprietary . **No system proxy or SSL certificates required** . **Best for frontend developers** wanting to modify traffic without proxy configuration conflicts. |

**Frameworks for building custom systems**: Choose **mitmproxy** for scriptable interception in CI , **OWASP ZAP** for CI-integrated security scanning , or **Perseid** for a lightweight Rust-native Burp workflow  —all without per-seat proxy subscriptions.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- HTTP interception tools capture credentials, session tokens, and sensitive data; **only intercept traffic you own or have explicit authorization to test**. Remove CA certificates from test devices when finished and never share captured flow files carelessly.
- **Tool choice depends on whether you need a full proxy, a packet sniffer, or a security workbench.** **Wireshark is not an HTTP proxy**—it captures everything at the frame level and shows TCP/IP errors below HTTP, but you must filter for `http` to see web traffic . **Charles and Fiddler** are the classic MITM proxies for mobile QA—Charles's per-host SSL proxying list decrypts only the API you target . **mitmproxy is built for automation**: `mitmdump` runs headless in CI, and Python addons let you rewrite flows programmatically . **Perseid and OpenSec Studio are Rust-native Burp alternatives**—Perseid offers a familiar workflow in a native desktop app , while OpenSec Studio claims <180ms startup and <95MB RAM versus Burp Pro's 8–15s and 850MB–1.4GB . **Requestly avoids proxy setup entirely** by intercepting at the browser extension level . **Validate whether you need packet-level analysis (Wireshark), scripted automation (mitmproxy), a full security workbench (ZAP, Perseid, OpenSec), or browser-native interception (Requestly)** before committing.

---

**Made for developers, QA engineers, and security teams intercepting HTTP traffic.**  
Let's make HTTP traffic interception and capture more open, accessible, and proxy-aware.
