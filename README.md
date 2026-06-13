# Nong.Dev.Net

Nong.Dev.Net is a Claude Code multi-skill plugin for developer tooling. It was split from the GroundPA Toolkit alongside the Nong 3.2.5 migration — 10 skills that help Claude Code agents work with shells, .NET, NuGet, Git platforms, decompilation, email, and download proxies.

## Skills

| Skill | Purpose |
|-------|---------|
| `bash` | Bash scripting and CLI operations — quoting, set -e, trap, tool selection, sandbox, git safety |
| `powershell` | PowerShell 7+ scripting reference — encoding, error handling, modules, credentials, WhatIf |
| `dotnet` | .NET development all-in-one — C#, MSBuild, ASP.NET, EF Core, MAUI, diagnostics, AI |
| `nuget` | NuGet package management via dotnet CLI — install, update, push, pack, sources |
| `github` | Git + GitHub CLI — repo, issue, PR, Actions, release, gist |
| `gitee` | Gitee platform via MCP Server — issue, PR, review, merge, release, notifications |
| `gitcode` | GitCode platform via REST API — issue, PR, review, merge, repo management |
| `ghproxy` | GitHub download acceleration via `gh-proxy.org` |
| `ilspycmd` | Decompile .NET assemblies to C# source |
| `email` | Email operations via ClawEmail CLI |

## Installation

```bash
claude plugin marketplace add https://gitcode.com/angri450/Nong.Dev.Net.git
claude plugin install nong-dev@angri450
```

Restart Claude Code or run `/reload-plugins` after install.

## Repository Boundaries

The installable plugin surface keeps only `.claude-plugin/`, skill directories, README, LICENSE, and manifests. Development logs stay in `log/`.

## License

Apache-2.0
