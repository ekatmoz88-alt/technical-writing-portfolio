# MCP Server Inventory

> **Snapshot date:** 2026-11-21  
> **Scope:** MCP servers configured for Cline in VS Code. This inventory describes the local MCP integrations and their relationship to GitHub projects; it is not a list of GitHub repositories.

## 1. Overview

| MCP server | Responsibility | Runtime / transport | Reported status |
|---|---|---|---|
| `github` | GitHub account and repository operations | TypeScript / Node.js, `stdio` | **Active / Ready** |
| `quietgridlabs-c4` | C4 architecture projects for QuietGridLabs | JavaScript / Node.js, `stdio` | **Active / Ready** |
| `ss-tmk-gateway` | Gateway to the `ss-tmk-project` workspace | Python 3, `stdio` | **Degraded / Timeout** |

The GitHub MCP server is an infrastructure integration used to work with repositories. It is not itself one of the repositories in the GitHub account. The three servers have separate responsibilities and should not be treated as interchangeable project components.

## 2. Server records

### 2.1 `github`

**Purpose**

Provides Cline with tools for interacting with the GitHub account `ekatmoz88-alt`, including repository discovery and file, branch, issue, and pull-request operations.

**Reported implementation**

- Package: `@modelcontextprotocol/server-github`
- Runtime: TypeScript / Node.js
- Transport: `stdio`
- API: GitHub REST API and GraphQL API
- Launch command: `npx -y @modelcontextprotocol/server-github`
- Credential: `GITHUB_PERSONAL_ACCESS_TOKEN`, supplied through the process environment

**Reported tool coverage**

The configured server was reported to expose 26 tools. Examples from the inventory:

- `search_repositories`
- `create_or_update_file`
- `get_file_contents`
- `push_files`
- `create_pull_request`

This is a representative list, not a complete verified tool manifest. Tool names and count should be checked against the installed server version when this inventory is updated.

**Reported health**

- Status: Active / Ready
- Connection: connected
- Smoke test: repository discovery across the account; 32 repositories reported
- Search result metadata: `incomplete_results: false`

The 32-repository count is a point-in-time observation, not a permanent account property.

### 2.2 `quietgridlabs-c4`

**Purpose**

Provides access to C4 architecture projects associated with QuietGridLabs.

**Reported implementation**

- Runtime: JavaScript / Node.js
- Transport: `stdio`
- Configuration: local environment file under the `c4-quietgridlabs` workspace
- Launch pattern: Node.js with `--env-file`, followed by the server's `index.js`

Reported launch pattern:

```bash
node --env-file=/path/to/c4-quietgridlabs/mcp-server/.env /path/to/c4-quietgridlabs/mcp-server/index.js
```

Replace the illustrative paths with the actual local paths. Do not commit the `.env` file.

**Reported tools**

- `list_projects`
- `search_project`

The complete tool list and exact input/output schemas have not yet been verified against `index.js`.

**Reported health**

- Status: Active / Ready
- Connection indicator: green

### 2.3 `ss-tmk-gateway`

**Purpose**

Acts as an MCP gateway to the local `ss-tmk-project` workspace.

**Reported implementation**

- Runtime: Python 3
- Transport: `stdio`
- Workspace: `/home/kate/ss-tmk-project/`
- Entry point: `/home/kate/ss-tmk-project/mcp_server.py`

Reported launch command:

```bash
python3 /home/kate/ss-tmk-project/mcp_server.py
```

Reported initialization timeout: 120 seconds.

**Reported tools**

The available tools and their schemas have not yet been verified against `mcp_server.py`.

**Reported health**

- Status: Degraded / Timeout
- Error: `-32001`
- Symptom: initialization exceeded the configured 120-second timeout

This status indicates an initialization/connection problem. It does not, by itself, establish whether the cause is slow startup, a blocking operation, an unavailable dependency, or a protocol/stdio issue.

## 3. Cline configuration reference

Cline stores MCP server configuration in:

```text
~/.cline/data/settings/cline_mcp_settings.json
```

The following is a **sanitized example** for the GitHub server. Replace the token placeholder locally; never publish a real personal access token.

```json
{
  "mcpServers": {
    "github": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-github"],
      "env": {
        "GITHUB_PERSONAL_ACCESS_TOKEN": "<SET_LOCALLY>"
      },
      "disabled": false,
      "autoApprove": []
    }
  }
}
```

The two local servers should be documented in the same configuration file using their verified local commands and environment requirements. Their exact JSON entries are intentionally omitted here because the complete environment-variable names and paths have not been confirmed.

### Security requirements

- Do not commit `cline_mcp_settings.json` if it contains credentials.
- Do not put access tokens, passwords, API keys, or private environment values in this inventory.
- Keep local `.env` files out of Git; use a sanitized `.env.example` only when variable names and purpose are verified.
- Grant each server only the permissions it needs.
- If a token has been exposed, revoke it and issue a replacement.

## 4. API endpoints

For the GitHub integration, the canonical API endpoints are:

- REST API: `https://api.github.com`
- GraphQL API: `https://api.github.com/graphql`

The GitHub website origin `https://github.com` is not an API endpoint.

## 5. Health and verification checklist

| Server | Current observation | Next verification |
|---|---|---|
| `github` | Active / Ready; 32 repositories discovered | Recheck tool manifest and repository visibility when configuration or package version changes |
| `quietgridlabs-c4` | Active / Ready | Inspect `index.js`; record every tool name, description, and input schema |
| `ss-tmk-gateway` | Degraded; initialization timeout after 120 s | Inspect startup path, stdout/stderr handling, dependency initialization, and blocking calls in `mcp_server.py`; then retest initialization |

### Suggested diagnostic sequence for `ss-tmk-gateway`

1. Run the exact Python entry point manually from a terminal and capture stderr.
2. Confirm that startup does not wait for interactive input.
3. Confirm that stdout is reserved for MCP protocol messages; send diagnostic logs to stderr.
4. Check imports, environment variables, local files, and external services required during initialization.
5. Identify network or database calls performed before the server finishes MCP initialization.
6. Retest from Cline after correcting the startup issue. Increase the timeout only if the longer startup is expected and understood.

## 6. Evidence boundaries

This inventory separates **reported configuration** from **verified implementation details**:

- Runtime, transport, launch commands, status indicators, timeout, and the GitHub repository count reflect the supplied configuration/status snapshot dated 2026-11-21.
- The complete tool manifests for `quietgridlabs-c4` and `ss-tmk-gateway` remain unverified until their source files are inspected.
- The GitHub tool examples are representative; the exact installed package version and full tool manifest should be checked before relying on the reported count of 26.
- No credentials or private environment values belong in this document.

## 7. Maintenance

Update this file whenever a server is added, removed, renamed, moved, or changes runtime, transport, launch command, tool surface, or health status. Record the observation date and distinguish a successful connection test from a full functional test of every tool.
