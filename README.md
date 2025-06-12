# HTTP Status Code 246: Guardrail Check Failed

> A standard for communicating partial failures in AI and ML systems

[![GitHub stars](https://img.shields.io/github/stars/status246/specification)](https://github.com/status246/specification/stargazers)
[![Discussions](https://img.shields.io/github/discussions/status246/specification)](https://github.com/status246/specification/discussions)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

## What is Status 246?

Status 246 "Guardrail Check Failed" indicates that a request was processed successfully, but automated safety checks detected issues worth knowing about.

```http
HTTP/1.1 246 Guardrail Check Failed
Content-Type: application/json

{
  "data": { "response": "Generated content..." },
  "guardrail_results": {
    "verdict": "failed",
    "checks": [
      {
        "id": "content_policy",
        "status": "failed",
        "confidence": 0.85
      }
    ]
  }
}
```

## Why Status 246?

- **Transparency**: Safety violations are explicitly communicated
- **Compliance**: Track policy violations without blocking requests  
- **Observability**: Clear separation between system errors and content issues
- **Flexibility**: Applications decide how to handle flagged content

## Quick Start

- [📖 Read the Specification](specification/draft.md)
- [🛠 Implementation Guide](docs/implementation-guide.md)
- [📋 Examples](examples/)
- [💬 Join Discussion](https://github.com/status246/specification/discussions)

## Implementations

| Platform | Status | Maintainer |
|----------|--------|------------|
| [Express.js](implementations/javascript/express/) | ✅ Complete | [@maintainer] |
| [FastAPI](implementations/python/fastapi/) | ✅ Complete | [@maintainer] |
| [Spring Boot](implementations/java/spring-boot/) | 🚧 In Progress | [@maintainer] |
| [Go Gin](implementations/go/gin/) | 📋 Planned | - |

## Adopters

Organizations using Status 246 in production:

- **Portkey AI** - AI Gateway and Guardrails Platform
- **[Add your organization]** - [Submit a PR](CONTRIBUTING.md)

## Contributing

We welcome contributions! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## Community

- [GitHub Discussions](https://github.com/status246/specification/discussions)
- [Discord Server](https://discord.gg/status246) 
- [Monthly Community Calls](community/meetings.md)

## License

This specification is licensed under [MIT License](LICENSE).
