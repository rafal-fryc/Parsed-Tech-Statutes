# Parsed Tech Statutes

Structured JSON outputs from statutes parsed using [TechRegParser](https://github.com/rafal-fryc/TechRegParser), a multi-agent system that extracts requirements from data privacy and tech regulation statutes.

## What's in this repository

Each folder contains parsed JSON files organized by regulatory domain. Every JSON file represents a single statute and includes:

- **Definitions** -- all defined terms with their statutory text and section references
- **Requirements** -- extracted obligations with exact citations, categories, confidence scores, and verification status
- **Structure** -- the statute's section tree (definitions, applicability, rights, duties, exemptions, enforcement)
- **Legislative intent** -- purpose and scope as stated in the statute
- **Metadata** -- parser version, processing timestamps, and verification statistics

### Requirement categories

Each extracted requirement is classified into one of four categories:

| Category | Description |
|---|---|
| **Disclosure** | Must be stated in a privacy policy or notice |
| **Operational** | Internal compliance processes (response times, procedures) |
| **Technical** | System/UI implementation (GPC signals, security measures, link placement) |
| **Legal Framework** | Enforcement mechanisms, penalties, AG authority, cure periods |

## About TechRegParser

TechRegParser uses a multi-agent architecture built on the Anthropic Agent SDK to read, analyze, and extract structured requirements from regulatory statutes. It employs specialized agents for statute reading, section analysis, citation verification, and requirement classification -- with anti-hallucination measures that require every extracted requirement to include a direct quote from the source text.

For more information, see the [TechRegParser repository](https://github.com/rafal-fryc/TechRegParser).

## License

MIT
