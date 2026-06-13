# 2026-06-11 Nong.Dev.Net initial launch

## What changed

从 Nong.Toolkit.Net 历史 (commit 593b46e, pre-7d1d146 cleanup) 恢复 10 个开发者 skill，建立独立仓库 Nong.Dev.Net。

### Skill 清单

| Skill | Purpose |
|-------|---------|
| `bash` | Bash scripting — quoting, set -e, trap, tool selection, sandbox, git safety |
| `powershell` | PowerShell 7+ — encoding, modules, credentials, WhatIf |
| `dotnet` | .NET all-in-one — C#, MSBuild, ASP.NET, EF Core, MAUI, diagnostics, AI |
| `nuget` | NuGet package management via dotnet CLI |
| `github` | Git + GitHub CLI — repo, issue, PR, Actions, release, gist |
| `gitee` | Gitee platform via MCP Server |
| `gitcode` | GitCode platform via REST API |
| `ghproxy` | GitHub download acceleration via gh-proxy.org |
| `ilspycmd` | .NET assembly decompilation |
| `email` | ClawEmail CLI operations |

### Multi-plugin marketplace

Single repo, 11 plugins (1 bundle + 10 individual):

```
claude plugin install bash@nong-dev              (~40 tok)
claude plugin install powershell@nong-dev
claude plugin install nong-dev@nong-dev          (full bundle)
```

Marketplace name: `nong-dev`。每个 skill 目录有自己的 `.claude-plugin/plugin.json`。

### Plugin infrastructure

- `.claude-plugin/marketplace.json` — name: `nong-dev`, 11 plugin entries
- `.claude-plugin/plugin.json` — root bundle plugin
- 每个 skill 目录 `.claude-plugin/plugin.json` — `"skills": ["./"]`

### CLAUDE.md

包含 Plugin Infrastructure 文档：双文件规则、marketplace name 唯一性、字段参考表、多 plugin 结构说明、Credential 和 Skill Boundaries。

### skills.sh 接入

- `skills.sh.json` — 标准 groupings 格式：Shell / .NET Ecosystem / Git Platforms / Utilities
- `npx skills add angri450/Nong.Dev.Net` 测试通过 — 发现 10 个 skill，安装到 71 个 agent

### 仓库

- GitHub: `https://github.com/angri450/Nong.Dev.Net`
- Gitee: `https://gitee.com/angri450/Nong.Dev.Net`
- GitCode: `https://gitcode.com/angri450/Nong.Dev.Net`

所有 remote 推送为 `main` 分支，三平台 master 分支已删除。

### GitCredential

- GitHub: `GH_TOKEN` 环境变量
- Gitee: Windows Credential Manager (`git:https://gitee.com`)
- GitCode: Windows Credential Manager (`git:https://gitcode.com`)

## Files registered

65 files total:
- 10 SKILL.md files with references, examples, and evals
- 10 sub-skill `.claude-plugin/plugin.json` files
- Root `.claude-plugin/` with `marketplace.json` and `plugin.json`
- `skills.sh.json`, `CLAUDE.md`, `README.md`, `README.zh-CN.md`, `skill.zh`, `LICENSE`, `.gitignore`
- `nuget/nuget.exe` (8.5 MB binary, retained for legacy `packages.config` projects)
