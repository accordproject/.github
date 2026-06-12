<p align="center">
  <strong>Open-source standards and tooling for humans and AI agents to draft, validate, and compute legally-meaningful contracts.</strong><br>
  Linux Foundation project · Apache-2.0
</p>

<p align="center">
  <a href="https://docs.accordproject.org"><img src="https://img.shields.io/badge/docs-accordproject.org-19C6C8" alt="Docs"></a>
  <a href="https://discord.gg/Zm99SKhhtA"><img src="https://img.shields.io/badge/community-Discord-5865F2" alt="Discord"></a>
  <a href="https://github.com/accordproject"><img src="https://img.shields.io/badge/license-Apache--2.0-brightgreen" alt="License"></a>
</p>

---

## What we build

Accord Project provides the open standard — and reference implementation — for **computable contracts**: structured, typed, executable agreements.

### The three components

| Component | What it is | Repo |
|---|---|---|
| **Concerto** | Schema language for contract data. Generates TypeScript, Java, Go, Python, JSON Schema from one `.cto` file. | [concerto](https://github.com/accordproject/concerto) |
| **TemplateMark** | Markdown-based contract template format. Variables + conditional logic. Readable by humans and LLMs. | [markdown-transform](https://github.com/accordproject/markdown-transform) |
| **APAP** | Agreement Protocol API — REST + MCP server. Agents call contracts as tools. | [apap](https://github.com/accordproject/apap) |

### How they fit together

```
Natural language request
        │
        ▼
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │  TemplateMark│────▶│   Concerto   │────▶│    APAP      │
  │   (template) │     │   (schema)   │     │ (MCP / REST) │
  └──────────────┘     └──────────────┘     └──────────────┘
        │                     │                     │
     Prose text           Type-safe data        AI tool calls
                           validation
```

## Quick start

```bash
# Use the template engine API in your project
npm install @accordproject/template-engine
```

**Try it live:**
- [Template Playground](https://playground.accordproject.org) — draft and test templates in your browser
- [Concerto Playground](https://concerto-playground.accordproject.org) — paste a schema, see 7 language targets

## For AI builders

Accord Project templates are structured data sources for LLM workflows:

- **TemplateMark** is Markdown — LLMs already understand it at training-data scale
- **Concerto schemas** validate LLM-generated data before it reaches the contract
- **APAP MCP endpoint** exposes templates as tool calls to any MCP client
- **TypeScript logic** compiles statically — agent-generated code fails at compile time, not runtime

See the [AI & Agent Workflows guide](https://docs.accordproject.org/docs/accordproject-ai) and the [2024 Whitepaper](https://accordproject.org/whitepaper-2024/).

## Community

- [Discord](https://discord.gg/Zm99SKhhtA) — join the Technology Working Group
- [Blog](https://accordproject.org/news) — blog & news
- [Governance](https://github.com/accordproject/governance) — TSC and working groups

<p align="center">
  <a href="https://www.linuxfoundation.org">
    <img src="https://img.shields.io/badge/a%20Linux%20Foundation%20project-gray?logo=linux" alt="Linux Foundation">
  </a>
</p>
