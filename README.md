# Nong.Dev.Net

Nong.Dev.Net shares its roots with Nong.Toolkit.Net but stands on its own, built for the agricultural agent developer. 11 plugins — one full bundle plus 10 individual skills. Install only what you need.

## Install

### Full bundle

```bash
claude plugin marketplace add https://gitcode.com/angri450/Nong.Dev.Net.git
claude plugin install nong-dev@nong-dev
```

### Individual skills (lower token cost)

```bash
claude plugin marketplace add https://gitcode.com/angri450/Nong.Dev.Net.git
claude plugin install bash@nong-dev              # ~44 tok always-on
claude plugin install powershell@nong-dev
claude plugin install dotnet@nong-dev
# ... install any subset
```

GitHub source:

```bash
claude plugin marketplace add angri450/Nong.Dev.Net
claude plugin install bash@nong-dev
```

After installation, restart Claude Code or run `/reload-plugins`.

## Skills

| Skill | Purpose | Plugin id |
|-------|---------|-----------|
| `bash` | Bash scripting and CLI operations — quoting, set -e, trap, tool selection, sandbox, git safety | `bash@nong-dev` |
| `powershell` | PowerShell 7+ scripting reference — encoding, error handling, modules, credentials, WhatIf | `powershell@nong-dev` |
| `dotnet` | .NET development all-in-one — C#, MSBuild, ASP.NET, EF Core, MAUI, diagnostics, AI | `dotnet@nong-dev` |
| `nuget` | NuGet package management via dotnet CLI — install, update, push, pack, sources | `nuget@nong-dev` |
| `github` | Git + GitHub CLI — repo, issue, PR, Actions, release, gist | `github@nong-dev` |
| `gitee` | Gitee platform via MCP Server — issue, PR, review, merge, release, notifications | `gitee@nong-dev` |
| `gitcode` | GitCode platform via REST API — issue, PR, review, merge, repo management | `gitcode@nong-dev` |
| `ghproxy` | GitHub download acceleration via gh-proxy.org | `ghproxy@nong-dev` |
| `ilspycmd` | Decompile .NET assemblies to C# source | `ilspycmd@nong-dev` |
| `email` | Email operations via ClawEmail CLI | `email@nong-dev` |

## Validation

```bash
claude plugin validate .
claude plugin validate bash
claude plugin validate powershell
```

## License

Apache-2.0
