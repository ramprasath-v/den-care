# Third-party software and services

CareCircle depends on third-party open-source packages and hosted AWS services. Those components are not relicensed by CareCircle's MIT License. Their original licenses and service terms continue to apply.

The locked Python environment currently includes these direct dependencies:

| Component | Purpose | Upstream license |
| --- | --- | --- |
| Boto3 and Botocore | AWS service clients and request signing | Apache-2.0 |
| Python MCP SDK | FastMCP server and Streamable HTTP transport | MIT |
| Strands Agents | Supervisor and agents-as-tools planning | Apache-2.0 |
| Pydantic and pydantic-settings | Typed contracts and configuration | MIT |
| Starlette | Python web application | BSD-3-Clause |
| Uvicorn | ASGI server | BSD-3-Clause |
| Amazon Transcribe Streaming SDK for Python | Browser-audio transcription | Apache-2.0 |
| pytest and pytest-asyncio | Test suite | MIT / Apache-2.0 |
| HTTPX | ASGI and HTTP tests | BSD-3-Clause |

The checked-in AgentCore CDK project directly uses `@aws/agentcore-cdk`, `aws-cdk-lib`, and `constructs`, each distributed under Apache-2.0. Container builds use the official Python 3.11 slim image and `uv`; their own distribution terms and included operating-system package notices apply.

The browser UI contains project-authored HTML, CSS, JavaScript, and an inline project-authored SVG favicon. It does not bundle third-party fonts, photographs, music, audio, or trademark artwork.

Exact resolved versions are recorded in `uv.lock`, `requirements-voice.txt`, and `infra/agentcore/CareCirclePhase3/agentcore/cdk/package-lock.json`. Anyone redistributing a compiled container should retain the license notices included by its dependencies and review the resulting image's software bill of materials. AWS, Alexa, Ring, Claude, Python, and other names belong to their respective owners and are used only to identify compatible services or dependencies.
