# CLAUDE.md - Nong.Dev.Net

Nong.Dev.Net is the Claude Code skill layer for developer tooling. It teaches agents how to route shell scripting, .NET development, NuGet management, Git platform operations, decompilation, email, and download proxy work.

Split from the GroundPA Toolkit alongside the Nong 3.2.5 migration — these 10 skills were the non-agricultural companion tools.

## Current Contract

- Plugin version: `1.0.0`.
- Plugin id: `nong-dev`.
- This repository contains skills and documentation only. Deterministic execution belongs in the respective CLIs and SDKs.

## Required Workflow

1. Inspect the relevant `SKILL.md` and linked references before editing.
2. Keep each `SKILL.md` concise — the routing layer. Put detailed rules in `references/`.
3. Record development work under `log/plans/`, `log/changelog/`, `log/debug/`, or `log/guidance/`.

## Skill Boundaries

- `bash` teaches Bash scripting, tool selection, quoting, error handling, and sandbox decisions.
- `powershell` teaches PowerShell 7+ scripting, encoding, modules, credentials, and WhatIf.
- `dotnet` is the .NET routing layer — one reference per domain (C#, MSBuild, ASP.NET, EF Core, MAUI, etc.).
- `nuget` teaches NuGet package management via `dotnet` CLI.
- `github` teaches Git + GitHub CLI — repo, issue, PR, Actions, release, gist.
- `gitee` teaches Gitee platform operations via MCP Server.
- `gitcode` teaches GitCode platform operations via REST API.
- `ghproxy` teaches GitHub download acceleration via `gh-proxy.org`.
- `ilspycmd` teaches .NET assembly decompilation.
- `email` teaches email operations via ClawEmail CLI.

## Credentials

- GitHub: `gh auth` logged in as angri450. Token in Windows Credential Manager.
- NuGet: `NUGET_API_KEY` in user environment.
- Gitee / GitCode: cached in Windows Credential Manager.
- On 401/403: tell the user to refresh their token.

## Legacy Rules

- SKILL.md is the routing kernel. Long guidance goes in references.
- Description must be honest. Do not declare capabilities the tool does not implement.
- No remote CDN in deliverables.
