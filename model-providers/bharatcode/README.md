# BharatCode model provider for Hermes

Registers `bharatcode` as a native Hermes model provider. OpenAI-compatible
chat completions endpoint, API-key auth, live model catalog from the
provider's `/models` endpoint.

- Base URL: `https://bharatcode.ai/api/model/v1`
- Env var: `BHARATCODE_API_KEY`
- Auth: API key
- Models: `deepseek-v4.1-flash`, `qwen-3.8-27b` (live catalog overrides)
- Signup: https://bharatcode.ai (free for .ac.in / .edu.in students)

Install via the Hermes plugin catalog (`hermes plugins install bharatcode-provider`)
or manually — see the repository README.
