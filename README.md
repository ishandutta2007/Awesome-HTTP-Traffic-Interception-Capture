# Awesome-HTTP-Traffic-Interception-Capture

## Top HTTP Traffic Interception & Capture Ecosystem

**Curated List of SaaS Platforms & Open-Source GitHub Projects**  
*Focused on MITM Proxying, Request Replay & Self-Hosted Security Workbenches*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **HTTP Traffic Interception & Capture**. These tools help developers and security testers sit between a client and a server—capturing, inspecting, and modifying requests and responses in real time, covering everything from browser-native interceptors to full MITM proxies and Rust-native security workbenches.

**Examples** include mitmproxy, OWASP ZAP, Burp Suite, Wireshark, HTTP Toolkit, Requestly, and Perseid.

**Open-source emphasis**: This section highlights active projects for self-hosted traffic interception, open-source MITM proxies, and community-driven security testing—ideal for teams seeking data sovereignty and avoiding per-seat proxy subscriptions.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## Sector Overview & Market Dynamics

The global market for HTTP traffic interception, web debugging proxies, and DAST (Dynamic Application Security Testing) is estimated at approximately **$3.6B to $4.3B**, with high-growth segments like DAST projected to exceed **$12B+ by 2032** at an estimated CAGR of 14–17%. 

Market dynamics reflect a **moderately fragmented landscape**: while foundational developer environments and enterprise security suites (such as Postman and PortSwigger's Burp Suite) command strong user lock-in and high brand concentration, the broader sector remains decentralized with specialized standalone utilities across desktop debugging (Proxyman, Fiddler, Charles), browser-layer interceptors (Requestly), and robust, independent open-source tools (mitmproxy, OWASP ZAP).

## SaaS/Hosted Platforms

| Product | Company Valuation / Revenue | Description | Pricing (Starting) | Free Tier / Trial Limits |
|---------|-----------------------------|-------------|-------------------|--------------------------|
| **[Postman Interceptor](https://www.postman.com/)** | **$5.6B Valuation** (~$270M–$315M ARR) | Browser extension and proxy agent capturing HTTP/HTTPS traffic to route and sync with Postman collections. | **$9/month** (Solo, billed annually) or **$19/user/month** (Team, billed annually) | **Free forever plan**: Capped at 1 user account; basic local interceptor sync, cloud collaboration restricted. |
| **[Requestly](https://requestly.com/)** | **$4.0B Valuation (Parent BrowserStack)** (~$3M ARR pre-acquisition) | Browser extension and desktop client enabling network rule manipulation, header redirects, and API mocking without proxy setup. | **$8/member/month** (Lite plan, billed annually) | **Free forever plan**: Capped at 5 total rules (3 active rules max), 5 API mocks, and non-commercial personal use. |
| **[Fiddler Everywhere](https://www.telerik.com/fiddler)** | **$1.79B Market Cap** (~$978M Revenue, Progress Software) | Cross-platform desktop proxy debugging suite with visual traffic inspection, custom rule builders, and team request sharing. | **$13/user/month** (Pro, billed annually; commercial use) or **$7/user/month** (Lite) | **10-day free trial**: Fully functional, unconstrained access across all Pro/Enterprise features for 10 days. |
| **[Burp Suite Professional](https://portswigger.net/burp)** | **$112M Private Equity Round** (~$35M–$40M ARR, PortSwigger) | Industry-standard web application security workbench and intercepting proxy with automated scanners, intruder, and repeater. | **$499/user/year** (Burp Suite Professional) | **Free forever plan (Burp Community Edition)**: Capped manual toolkit—no project saving, scanner disabled, and Intruder attack speeds throttled. |
| **[Proxyman](https://proxyman.com/)** | **~$600K–$900K ARR** (Bootstrapped indie business) | High-performance native macOS, iOS, Windows, and Linux HTTPS debugging proxy with SSL proxying and local script tampering. | **$89 one-time** (Standard seat with 1 year of updates) | **Free forever plan**: Unlimited basic traffic capture; restricted to max 2 active rules (Map Local/Remote, Breakpoints) and 2 pinned domains. |
| **[Charles Proxy](https://www.charlesproxy.com/)** | **Bootstrapped Indie** (<$5M estimated revenue, XK72 Ltd) | Long-standing desktop web debugging proxy with SSL decryption, bandwidth throttling, and AJAX/AMF recording. | **$50 one-time** (1–4 single-user licenses; $400 site license) | **30-day free trial**: Unrestricted 30-day trial; after 30 days, sessions automatically shut down after 30 minutes of continuous use with startup delays. |

## Open-Source GitHub Projects

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[mitmproxy](https://github.com/mitmproxy/mitmproxy)** | [![Stars](https://img.shields.io/github/stars/mitmproxy/mitmproxy?style=social&color=white)](https://github.com/mitmproxy/mitmproxy/stargazers) | **The standard open-source scriptable MITM proxy for automated interception and capture.** MIT licensed, Python. Provides CLI (`mitmproxy`), web UI (`mitmweb`), and headless (`mitmdump`) interfaces with Python addon extensions for programmatic flow tampering. |
| **[bettercap](https://github.com/bettercap/bettercap)** | [![Stars](https://img.shields.io/github/stars/bettercap/bettercap?style=social&color=white)](https://github.com/bettercap/bettercap/stargazers) | **Swiss army knife for 802.11, BLE, IPv4, and IPv6 network reconnaissance and MITM attacks.** Written in Go with modular interactive packet capture, HTTPS proxy interception, and active protocol credential sniffers. |
| **[OWASP ZAP](https://github.com/zaproxy/zaproxy)** | [![Stars](https://img.shields.io/github/stars/zaproxy/zaproxy?style=social&color=white)](https://github.com/zaproxy/zaproxy/stargazers) | **The world's most widely deployed open-source DAST proxy.** Apache-2.0, Java. Features intercepting proxying, passive analysis, automated vulnerability scanners, baseline CI checks, and official LLM/MCP integrations. |
| **[Wireshark](https://github.com/wireshark/wireshark)** | [![Stars](https://img.shields.io/github/stars/wireshark/wireshark?style=social&color=white)](https://github.com/wireshark/wireshark/stargazers) | **The world's leading network protocol analyzer.** GPL-2.0, C/C++. Captures raw frames across interfaces, inspects packet dissections, and isolates HTTP/HTTPS traffic at the packet and socket layer. |
| **[AnyProxy](https://github.com/alibaba/anyproxy)** | [![Stars](https://img.shields.io/github/stars/alibaba/anyproxy?style=social&color=white)](https://github.com/alibaba/anyproxy/stargazers) | **Fully configurable HTTP/HTTPS proxy in Node.js by Alibaba.** Apache-2.0. Offers a customizable web-based traffic inspector dashboard and JavaScript-based interception rule hooks. |
| **[Requestly](https://github.com/requestly/requestly)** | [![Stars](https://img.shields.io/github/stars/requestly/requestly?style=social&color=white)](https://github.com/requestly/requestly/stargazers) | **Open-source core client and extension for network interception and API mocking.** Modifies network traffic directly in browser sessions without requiring system-wide proxy or certificate configuration. |
| **[HTTP Toolkit](https://github.com/httptoolkit/httptoolkit)** | [![Stars](https://img.shields.io/github/stars/httptoolkit/httptoolkit?style=social&color=white)](https://github.com/httptoolkit/httptoolkit/stargazers) | **Open-source HTTP(S) debugging proxy and interactive client.** AGPL-3.0. Features one-click interception targeting Android apps, Docker containers, browsers, and terminal sessions with Mockttp under the hood. |
| **[Proxify](https://github.com/projectdiscovery/proxify)** | [![Stars](https://img.shields.io/github/stars/projectdiscovery/proxify?style=social&color=white)](https://github.com/projectdiscovery/proxify/stargazers) | **Versatile, portable proxy by ProjectDiscovery for capturing, manipulating, and replaying HTTP/HTTPS traffic on the fly.** Apache-2.0, Go. Supports request dumping, upstream proxy chaining, and traffic matching rules. |
| **[BrowserMob Proxy](https://github.com/lightbody/browsermob-proxy)** | [![Stars](https://img.shields.io/github/stars/lightbody/browsermob-proxy?style=social&color=white)](https://github.com/lightbody/browsermob-proxy/stargazers) | **Automated HTTP capture utility tailored for Selenium and functional test suites.** Apache-2.0, Java. Captures performance data in HAR (HTTP Archive) format and manipulates browser traffic programmatically. |
| **[Martian](https://github.com/google/martian)** | [![Stars](https://img.shields.io/github/stars/google/martian?style=social&color=white)](https://github.com/google/martian/stargazers) | **Google library and programmable proxy for intercepting and modifying HTTP/S traffic.** Apache-2.0, Go. Configured via declarative JSON modifiers, filters, and verifiers for end-to-end integration testing. |
| **[Perseid](https://github.com/andyintheshell/perseid)** | [![Stars](https://img.shields.io/github/stars/andyintheshell/perseid?style=social&color=white)](https://github.com/andyintheshell/perseid/stargazers) | **Rust-native Burp Suite alternative—zero JVM runtime overhead.** MIT/Apache-2.0. Native desktop workbench (egui) featuring HTTP/1.1 and HTTP/2 interception, Repeater, Intruder, and WebSocket inspection. |
| **[OpenSec Studio](https://github.com/saghet/opensec-studio)** | [![Stars](https://img.shields.io/github/stars/saghet/opensec-studio?style=social&color=white)](https://github.com/saghet/opensec-studio/stargazers) | **Ultra-fast Rust DevSecOps & DAST workbench.** Combines an intercepting MITM proxy, tamper console, Repeater, Intruder, and Nuclei-compatible YAML scanning engines with cold boot times under 180ms. |
| **[Reqlore](https://github.com/ibrasonic/Reqlore)** | [![Stars](https://img.shields.io/github/stars/ibrasonic/Reqlore?style=social&color=white)](https://github.com/ibrasonic/Reqlore/stargazers) | **Accessibility-first web pentesting suite built as semantic HTML5.** Intercepting MITM proxy, request hold queues, Repeater, and Intruder engines designed for screen-reader (NVDA, JAWS, Orca) compatibility. |

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format and star-sorted order).
3. Include: name, link, star badge, accurate pricing/limits, and brief description.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- HTTP interception tools capture credentials, session tokens, and sensitive data; **only intercept traffic you own or have explicit authorization to test**. Remove CA certificates from test devices when finished and never share captured flow files carelessly.
- **Tool choice depends on whether you need a full proxy, a packet sniffer, or a security workbench.** Packet-level sniffers like Wireshark capture everything down to the frame level, while proxy tools like mitmproxy, Burp Suite, Charles, and Proxyman focus directly on decrypting, rewriting, and replaying HTTP/HTTPS layer exchanges.

---

**Made for developers, QA engineers, and security teams intercepting HTTP traffic.**  
Let's make HTTP traffic interception and capture more open, accessible, and proxy-aware.
