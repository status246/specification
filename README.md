# HTTP Status Code 246: Guardrail Check Failed

> A standard for communicating partial failures in AI and ML systems

[![GitHub stars](https://img.shields.io/github/stars/status246/specification)](https://github.com/status246/specification/stargazers)
[![Discussions](https://img.shields.io/github/discussions/status246/specification)](https://github.com/status246/specification/discussions)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

## What is Status 246?

Status 246 "Guardrail Check Failed" indicates that a request was processed successfully, but automated safety checks (guardrails) detected issues worth knowing about.

```http
HTTP/1.1 246 Guardrail Check Failed
Content-Type: application/json

{
  "data": {
    "response": "I can help you with that task.",
    "model": "gpt-4",
    "usage": { "tokens": 150 }
  },
  "guardrail_results": {
    "verdict": "failed",
    "checks": [
      {
        "id": "content_policy",
        "status": "failed",
        "confidence": 0.85,
        "message": "Potential policy violation detected"
      }
    ]
  }
}
```

## The Problem

AI systems with safety guardrails face a communication challenge:
- **200 OK** hides safety violations from monitoring systems
- **4xx/5xx errors** inappropriately block requests that should continue
- No standard way to indicate "succeeded with warnings"

## Why Status 246?

- **🔍 Transparency**: Safety violations are explicitly communicated
- **📊 Compliance**: Track and audit policy violations without blocking requests  
- **👁 Observability**: Clear separation between system errors and content policy issues
- **⚡ Flexibility**: Applications can decide how to handle flagged content based on severity

## Quick Start

- [📖 Read the Specification](specification/draft.md)
- [🛠 Implementation Guide](docs/implementation-guide.md)
- [📋 Examples](examples/)
- [💬 Join Discussion](https://github.com/status246/specification/discussions)

## Implementations

| Platform | Status | Maintainer |
|----------|--------|------------|
| [Express.js](implementations/javascript/express/) | ✅ Complete | [@portkey-ai] |
| [FastAPI](implementations/python/fastapi/) | ✅ Complete | [@portkey-ai] |
| [Spring Boot](implementations/java/spring-boot/) | 🚧 In Progress | [@portkey-ai] |
| [Go Gin](implementations/go/gin/) | 📋 Planned | [Help wanted!](CONTRIBUTING.md) |
| [Ruby on Rails](implementations/ruby/rails/) | 📋 Planned | [Help wanted!](CONTRIBUTING.md) |

## Adopters

Organizations using Status 246 in production:

- **[Portkey AI](https://portkey.ai)** - AI Gateway and Guardrails Platform
- **[Add your organization](CONTRIBUTING.md)** - Submit a PR to be listed

## Use Cases

- **AI Chat Applications**: Flag potentially harmful responses while still delivering them
- **Content Generation**: Warn about policy violations in generated text/images
- **Document Processing**: Indicate PII detection without blocking document access
- **API Gateways**: Communicate guardrail violations in AI service routing

## Status Code Behavior

| Status | Guardrail Result | Request Processing | Use Case |
|--------|------------------|-------------------|----------|
| 200 | Passed | Completed | All checks passed, content is safe |
| 246 | Failed | Completed | Issues detected, but request processed |
| 446 | Failed | Blocked | Critical violations, request denied |

## Community

- [GitHub Discussions](https://github.com/status246/specification/discussions) - Technical discussions and Q&A
- [Discord Server](#) - Real-time chat with the community
- [Monthly Community Calls](community/meetings.md) - Regular sync meetings

## Specification Status

This specification is currently in **draft** status. We are:
- Gathering community feedback
- Building reference implementations
- Preparing for IETF submission as an Internet-Draft

## Contributing

We welcome contributions! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on:
- Providing specification feedback
- Creating reference implementations
- Improving documentation
- Reporting issues

## License

This specification is licensed under the [MIT License](LICENSE).

## Acknowledgments

Special thanks to the HTTP Working Group and the broader developer community for their feedback and guidance.

---

**Status 246** is pioneered by [Portkey AI](https://portkey.ai) as part of their commitment to transparent and responsible AI infrastructure.
