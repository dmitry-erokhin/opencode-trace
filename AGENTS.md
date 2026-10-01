# opencode-trace

This is a plugin designed to capture the raw json requests sent to the LLM, and the raw responses back (after streaming-delta consolidation). It saves them into ~/opencode-trace
- End users should install it as an npm plugin via `"plugins": ["@ljw1004/opencode-trace"]` in `~/.config/opencode/opencode.json`.
- For development: `npm install` once, and change the plugin line to `["/path/to/opencode-trace"]`. Then each time you edit, `npm run typecheck` and `npm run lint` and then exercise it `opencode run --standalone --auto "why is the sky blue?"`. (It uses existing OpenCode configuration to pick up already-configured auth.)
- For iterating on the viewer, you can copy `viewer.js` into your ~/opencode-trace directory, or copy examples into this directory, and they'll preferentially pick up `viewer.js` over their embedded viewer code.
- To deploy, `npm version patch`, `npm login`, `npm publish --dry-run`, `npm publish`. Verify with `npm view "@ljw1004/opencode-trace"`, then test it by installing as above.
