# opencode-trace

This opencode plugin lets you see the raw json requests made to the LLM, and the responses.
* Example: https://ljw1004.github.io/opencode-trace/example.html

## Installation

Add the package to your OpenCode config:

```json
{
  "$schema": "https://opencode.ai/config.json",
  "plugins": ["@ljw1004/opencode-trace"]
}
```

Restart OpenCode and you'll see each transcript stored in `~/opencode-trace`.

Update package plugin with `opencode plugin update @ljw1004/opencode-trace`.
