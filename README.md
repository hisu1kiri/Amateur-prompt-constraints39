# Amateur Prompt Constraints

A personal, experimental project for making AI assistance more consistent through prompt-level constraints.
This is not a formal standard and does not guarantee model behavior.

Public project：**Amateur Prompt Constraints**。Repository slug：`amateur-prompt-constraints`。Public author：**Hisu1kiri**。
Current internal protocol / runtime identity：**PAIP V1.1-derived packaging snapshot**；运行时协议标识与 Skill name 保持 PAIP / `paip`。公开项目名称的选择不构成协议重命名或行为变更。

PAIP（Personal AI Protocol）为 substantive requests 提供证据与前提检查、独立判断，以及连续性、决策、学习、来源验证和状态完整性路由。本目录提供其当前来源快照的 Codex Skill 包装。

## 版本与来源

- Protocol identity：目标协议标识为 **PAIP V1.1**。取得的原始文件仍保留其 V1、RC1、Preview 等原有标识。
- Packaging identity：**0.1.0-candidate.1**；本次为同一 runtime 的最小 publication candidate，未创建 release。
- Input：2026-10-05 已验证 packaging candidate 中的 `SKILL.md` 和五个运行时 references；来自已取得并固定 hash 的本地 RC1 source snapshot。运行文件按原字节复制。
- Input package tree SHA-256：`043bc1d037924e977beb4ca0e996a1966cd1eac3a52bc7bb7371e5cc9772325c`。
- Source bundle SHA-256：`ea5f0854ade0c91c09790478c5a86d511aeabb167133c3c7c0e33f26efc15e19`。

**Historical Frozen V1.1 exact canonical file identity remains unverified.**

Freeze verdict 已被确认为后续审核裁定；原始 Freeze 审核文件、历史 PASS 与具体协议文件的 hash binding 尚未取得。取得的本地 RC1 ZIP 与 Library 原始字节的身份绑定未确认；Library Manifest 的渲染观察与选定原字节存在已记录差异，未合并或改写运行文件。这些是 provenance limitations，本目录不认证历史 Frozen release 的精确字节集合。

## 安装

安装**整个 `paip` 目录**，不能只复制 `references`。安装后 `SKILL.md` 必须位于 Skill root，五个 references 保持原相对位置。

当前官方 Skills 安装表列出的用户目录为 `$HOME/.agents/skills`，因此通用用户安装位置为 `$HOME/.agents/skills/paip`；项目安装位置为 `.agents/skills/paip`，按当前工作目录至 repository root 的作用域发现。[官方 Build skills](https://learn.chatgpt.com/docs/build-skills)

本次验收主机和其内置 Skill Installer 使用 `$CODEX_HOME/skills/paip`。对已确认支持该位置的目标安装，可优先沿用这一目录；`CODEX_HOME` 未设置时，内置 installer 的默认位置为 `~/.codex/skills/paip`。这是本机 installer 路径，与当前网页安装表的用户路径不同，不应假定任意版本都会发现两者。`CODEX_HOME` 的官方默认值为 `~/.codex`。[官方环境变量说明](https://learn.chatgpt.com/docs/config-file/environment-variables)

同一目标环境选择一种已支持的位置，避免安装多个同名 Skill。当前官方文档说明新安装和文件变化会自动检测；未显示时重启 Codex。修改 Skills 配置后也应重启。[官方 Build skills](https://learn.chatgpt.com/docs/build-skills)

## 文件与加载方式

```text
paip/
  SKILL.md
  references/
    PAIP_V1_MANIFEST.md
    PAIP_V1_CONTINUITY.md
    PAIP_V1_DECISION.md
    PAIP_V1_LEARNING.md
    PAIP_V1_EVIDENCE_STATE.md
  README.md
  CHANGELOG.md
  LICENSE
  .gitignore
```

Codex 先获得 Skill metadata，选用 Skill 后读取完整 `SKILL.md`；相关 references 按需加载。Core 已包含在 `SKILL.md`，reference 路径相对该文件解析。本 README 服务人类安装与审核，不是协议运行入口。[官方 Build skills](https://learn.chatgpt.com/docs/build-skills)

## 验证安装

确认目标 Codex 的 Skill 列表包含 `paip`，并核对六个运行文件与已审核的 publication manifest hash。需要观察加载时，可使用一个未点名 Skill 的普通 substantive request，通过原生读取记录确认 `SKILL.md` 和相关 reference 被取得；不需要重跑已有 blind/gate suite。答案正确或出现协议术语不能单独证明加载。

截至 2026-10-05 的验收裁定已确认：正常 Codex Chat 中一个未点名 PAIP 的 substantive Build-vs-Buy 请求取得并使用了 Decision reference。此项为已完成的 native routed-reference coverage；单次验收不构成所有未来请求的确定性触发保证，普通 Skill 正文也不会因安装而在未触发时常驻。

## 许可

本项目采用 [MIT License](LICENSE)。

Copyright (c) 2026 Hisu1kiri
