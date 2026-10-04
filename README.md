# Search Fragments plugin

Resolves half-remembered books, films, songs and people into a cited answer, a shortlist or a no.

Search Fragments is a free, non-commercial prototype. No account needed.

This repository only configures the hosted Search Fragments MCP server for Cursor, Grok Build and Gemini CLI. It contains no executable code.

- MCP server: `https://searchfragments.com/api/mcp` (Streamable HTTP)
- Tools: `resolve_fragment`, `verify_claim`, `submit_resolution_feedback`
- Network: connects only to `searchfragments.com`. It reads no local files and needs no credentials.
- Docs: https://searchfragments.com/docs
- Privacy: https://searchfragments.com/privacy

## Files

- `.cursor-plugin/plugin.json` and `mcp.json`: Cursor plugin
- `.grok-plugin/plugin.json` and `.mcp.json`: Grok Build plugin
- `gemini-extension.json`: Gemini CLI extension (`gemini extensions install https://github.com/Searchfragments/search-fragments-plugin`)
