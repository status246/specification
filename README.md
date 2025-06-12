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
