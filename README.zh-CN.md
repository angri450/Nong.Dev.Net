# Nong.Dev.Net

Nong.Dev.Net 是一个 Claude Code 开发者工具多 skill 插件。从 GroundPA Toolkit 随 Nong 3.2.5 迁移拆分出来——10 个 skill，覆盖 shell 脚本、.NET 开发、NuGet 包管理、Git 平台操作、反编译、邮件和下载加速。

## Skill 清单

| Skill | 用途 |
|-------|------|
| `bash` | Bash 脚本与 CLI 操作 — 引号、set -e、trap、工具选择、沙箱、Git 安全 |
| `powershell` | PowerShell 7+ 脚本参考 — 编码、错误处理、模块、凭证、WhatIf |
| `dotnet` | .NET 开发全家桶 — C#、MSBuild、ASP.NET、EF Core、MAUI、诊断、AI |
| `nuget` | NuGet 包管理 — 安装、更新、推送、打包、源管理 |
| `github` | Git + GitHub CLI — 仓库、Issue、PR、Actions、Release、Gist |
| `gitee` | Gitee 平台（MCP Server）— Issue、PR、Review、Merge、Release、通知 |
| `gitcode` | GitCode 平台（REST API）— Issue、PR、Review、Merge、仓库管理 |
| `ghproxy` | GitHub 下载加速 — `gh-proxy.org` 代理 |
| `ilspycmd` | .NET 程序集反编译为 C# 源码 |
| `email` | 邮件操作（ClawEmail CLI） |

## 安装

```bash
claude plugin marketplace add https://gitcode.com/angri450/Nong.Dev.Net.git
claude plugin install nong-dev@angri450
```

安装后重启 Claude Code 或执行 `/reload-plugins`。

## 仓库边界

可安装插件面只保留 `.claude-plugin/`、skill 目录、README、LICENSE 和 manifest。开发日志放在 `log/`。

## 许可证

Apache-2.0
