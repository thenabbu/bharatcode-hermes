# bharatcode-hermes

[BharatCode](https://bharatcode.ai) model provider plugin for
[Hermes Agent](https://github.com/NousResearch/hermes-agent) — listed in the
Hermes plugin catalog as `bharatcode-provider`.

One API key, native `/model` integration: after install, users only paste
`BHARATCODE_API_KEY` — no manual provider wiring.

## Install (plugin catalog)

```bash
hermes plugins install bharatcode-provider
```

Then set the key and pick the provider:

```bash
# ~/.hermes/.env
BHARATCODE_API_KEY=...
```

```text
/model bharatcode/deepseek-v4.1-flash
```

## Install (manual)

```bash
git clone https://github.com/thenabbu/bharatcode-hermes
cp -r bharatcode-hermes/model-providers/bharatcode ~/.hermes/plugins/
```

Restart the Hermes gateway after installing.

## Models

- `deepseek-v4.1-flash` — 1M context, heavy tier
- `qwen-3.8-27b` — 262k context, vision

The live catalog is fetched from the endpoint's `/models` route, so this list
stays accurate without a plugin update.

## Notes

- The API key lives only in your local `.env` — the plugin never transmits it
  anywhere except `bharatcode.ai`.
- No self-updating code: the catalog SHA pin is the trust model. Updates land
  via SHA-bump PRs in `NousResearch/hermes-agent`.
