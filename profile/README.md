# DevelopSolutions

Developer tools and security infrastructure. Small, self-contained projects that solve one problem completely: local AI runtimes, attack surface analysis, and the tooling around them.

The work here shares a set of constraints. Runs on your own hardware. Minimal dependencies. Configuration derived from the machine rather than pasted from a tutorial. Documented well enough that someone else can operate it.

## Projects

**[ailocal](https://github.com/DevelopSolutionsLLC/ailocal)** — Local model runtime for Apple Silicon. Runs Claude Code, Codex CLI, and VS Code Copilot against models on your own machine through one gateway that speaks both the OpenAI and Anthropic APIs. Ollama serves the models; a LiteLLM proxy fronts them on loopback. Hardware-derived configuration selects a model profile from available memory, so installation is `ailocal install` and verification is `ailocal check`. Python, standard library only, no runtime dependencies. Apache-2.0. [Architecture](https://github.com/DevelopSolutionsLLC/ailocal/blob/main/docs/architecture.md) · [Security](https://github.com/DevelopSolutionsLLC/ailocal/blob/main/docs/security.md) · [Troubleshooting](https://github.com/DevelopSolutionsLLC/ailocal/blob/main/docs/troubleshooting.md)

**[mycelium](https://github.com/DevelopSolutionsLLC/mycelium)** — Continuous threat exposure management. Seed it with a domain, IP, or ASN and it maps the attack surface as a graph: subdomains, ports, services, certificates, and CVEs, discovered by open-source recon tools running as isolated workers. Every finding is a node, every causal relationship a directed edge, so a seed-to-CVE path is one query. Go, NATS JetStream, Neo4j. Early.

**[job-radar](https://github.com/DevelopSolutionsLLC/job-radar)** — Job search pipeline. Scans Greenhouse, Ashby, Lever, BambooHR, Teamtailor, and Workday through an adapter registry, checks whether listings are still live, ranks them against a resume-derived seniority profile, and tracks applications. Node.js, MIT.

## Utilities

Smaller tools, each solving one operational problem.

**[monitorACL](https://github.com/DevelopSolutionsLLC/monitorACL)** — C++ daemon that repairs Active Directory ACL inheritance on QNAP shared folders using inotify and setfacl.

**[killswitch](https://github.com/DevelopSolutionsLLC/killswitch)** — OpenVPN killswitch for Debian-family Linux. UFW rules plus a systemd monitor, applied in a strict order so a protected service cannot transmit outside the tunnel.

**[handbrake-encode](https://github.com/DevelopSolutionsLLC/handbrake-encode)** — HandBrakeCLI wrapper that selects x264 or x265 by source resolution, detects HDR, and runs jobs in detachable screen sessions.

## About

DevelopSolutions LLC is owned and operated by [Victor Chevalier](https://github.com/VTChevalier), an engineering leader with twenty years across commercial software, telecom, and classified systems, currently leading engineering for a Continuous Threat Exposure Management platform.

[vtchevalier.com](https://vtchevalier.com) · [Contact](https://github.com/VTChevalier)
