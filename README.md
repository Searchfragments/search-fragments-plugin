# Search Fragments plugin

The gate before your agent answers: a verdict on whether a half-remembered thing can be reached. Call `gate_probe` first; `resolve_fragment` pieces the fragment together: Found, Leads or Not reachable.

Search Fragments is a free, non-commercial prototype. No account needed.

This repository only configures the hosted Search Fragments MCP server for Cursor, Grok Build and Gemini CLI. It contains no executable code.

- MCP server: `https://searchfragments.com/api/mcp` (Streamable HTTP)
- Tools: `gate_probe` (call first), `resolve_fragment`, `verify_claim`, `submit_resolution_feedback`
- Network: connects only to `searchfragments.com`. It reads no local files and needs no credentials.
- Docs: https://searchfragments.com/docs
- Privacy: https://searchfragments.com/privacy

## Files

- `.cursor-plugin/plugin.json` and `mcp.json`: Cursor plugin
- `.grok-plugin/plugin.json` and `.mcp.json`: Grok Build plugin
- `gemini-extension.json`: Gemini CLI extension (`gemini extensions install https://github.com/Searchfragments/search-fragments-plugin`)
