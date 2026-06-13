# Nong.Dev.Net

Nong.Dev.Net，与 Nong.Toolkit.Net 同宗同源各自独立，面向农业 agent 开发者。11 个 plugin——1 个全量包 + 10 个独立 skill，按需安装。

## 安装

### 全量安装

```bash
claude plugin marketplace add https://gitcode.com/angri450/Nong.Dev.Net.git
claude plugin install nong-dev@nong-dev
```

### 按需安装单个 skill（更低 token 成本）

```bash
claude plugin marketplace add https://gitcode.com/angri450/Nong.Dev.Net.git
claude plugin install bash@nong-dev              # ~44 tok 常驻
claude plugin install powershell@nong-dev
claude plugin install dotnet@nong-dev
# ... 按需组合
```

GitHub 源：

```bash
claude plugin marketplace add angri450/Nong.Dev.Net
claude plugin install bash@nong-dev
```

安装后重启 Claude Code，或执行 `/reload-plugins`。

## Skills

| Skill | 用途 | Plugin id |
|-------|------|-----------|
| `bash` | Bash 脚本和 CLI 操作 — 引号、set -e、trap、工具选择、沙箱、Git 安全 | `bash@nong-dev` |
| `powershell` | PowerShell 7+ 脚本参考 — 编码、错误处理、模块、凭证、WhatIf | `powershell@nong-dev` |
| `dotnet` | .NET 开发全家桶 — C#、MSBuild、ASP.NET、EF Core、MAUI、诊断、AI | `dotnet@nong-dev` |
| `nuget` | NuGet 包管理 — 安装、更新、推送、打包、源管理 | `nuget@nong-dev` |
| `github` | Git + GitHub CLI — 仓库、Issue、PR、Actions、Release、Gist | `github@nong-dev` |
| `gitee` | Gitee 平台（MCP Server）— Issue、PR、Review、Merge、Release、通知 | `gitee@nong-dev` |
| `gitcode` | GitCode 平台（REST API）— Issue、PR、Review、Merge、仓库管理 | `gitcode@nong-dev` |
| `ghproxy` | GitHub 下载加速 — gh-proxy.org | `ghproxy@nong-dev` |
| `ilspycmd` | .NET 程序集反编译为 C# 源码 | `ilspycmd@nong-dev` |
| `email` | 邮件操作（ClawEmail CLI） | `email@nong-dev` |

## 校验

```bash
claude plugin validate .
claude plugin validate bash
claude plugin validate powershell
```

## 开源协议

Apache-2.0
