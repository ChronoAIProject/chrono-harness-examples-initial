# chrono-harness 首次接入示例

这是没有业务项目的文档宿主，用于验证明确的首次文件清单与后续普通变更。所有跟踪文件均登记到 `.chrono-harness/FILEMAP.json`；不从目录、语言或文件名推断测试，也不添加空项目或空 CI 单元。

## 安装和检查

本轮采用固定测试版 [v0.1.4-dev.43348924098.1.g1ca9aa00be1147202d1cf3935ced4ba186eb3bba](https://github.com/ChronoAIProject/chrono-harness/releases/tag/v0.1.4-dev.43348924098.1.g1ca9aa00be1147202d1cf3935ced4ba186eb3bba)。`.chrono-harness/distribution.json` 锁定清单、安装器摘要、长度和六个工具；生成的 Shell 入口验证这些字节，再调用 Rust 安装器。宿主不编译 Rust、不提交二进制、SDK 或缓存，也不需要 Python、sudo 或全局配置修改。

从仓库根执行：

```sh
sh .chrono-harness/install.sh --host-root .
.chrono-harness/bin/chrono-harness check
```

需要 Git、POSIX Shell、curl 和该发布登记的摘要工具。当前 CI 平台仍为 macOS arm64／`macos-26`；公开发行包也提供 Linux，安装器存在不代表此示例已完成 Linux 的业务检查。

候选须已提交且检出干净。schema 4 的 `canonical_check` 明确选择本地工作树输入程序和 CI 事件输入程序，二者使用相同短命令。PR 检查固定合并提交，以第一父为基线并核第二父是事件 head；dev push 使用实际 before／after。Git 由本轮观察并绑定，不声称本地与 CI 的环境完全相同。

有父提交的普通文档 DELTA 没有业务测试，但必须核文件清单、声明输入、生成工作流及真实检查报告。初始清单仅适用于已确认无父的事件；不能用初始模式跳过普通 DELTA。历史首次公开根为 `4ee7954241eb3c4a40e6cff2c8d2d67beb390a9a`，它及其旧安装锁只是历史事实，不能作为本轮采用成功的证据。

## 指南和 CI

编辑 `.chrono-harness/instructions/` 中的采用源后运行：

```sh
.chrono-harness/bin/chrono-instructions generate --host-root .
```

保留现有英语指南选择；`AGENTS.md` 是目标字面值为 `CLAUDE.md` 的相对符号链接，不手改生成块，也不因安装新二进制覆盖宿主定制。

CI 来源为 `.chrono-harness/ci/github.json`，采用 `chrono-github-ci/v4`；普通检查使用绑定 Git 的 `chrono-ci-check/v2`，保留独立的 `chrono-initial-check/v1` 初始合同：

```sh
.chrono-harness/bin/chrono-ci generate --host-root . --config .chrono-harness/ci/github.json
.chrono-harness/bin/chrono-ci verify --host-root . --config .chrono-harness/ci/github.json
```

规则、CI 或稳定性迁移先经过 feature → integration 的真实 PR，再进入 dev；本仓未启用原生自动合并，现有 GitHub App 无权修改该设置；AI 等适用 CI 全部通过后，用现有合并入口匹配当前 head，按原有保护交付，不申请额外权限或增加确认关卡。CI 成功、PR 合并、dev 落地和新版实际采用分别核对。

## 工作树和恢复

`.chrono-harness/worktree.json` 明确登记 remote、Git、原报告、本地输入和两种分支角色；通过已安装的 `chrono-worktree start` 从最新 dev 创建 feature 或 integration。源码与获取端的已提交政策须符合当前工作树合同；不手造 origin 回执。

中断或部分效果按原 intent、报告、HEAD／index 和实际物理身份恢复，不从目录名、年龄、静默或缺失 PID 推断完成，也不删除未保全源码与提交。维护计划放在登记的 `.chrono-harness/state/` 中，继续使用固定发布的[工作树合同](https://github.com/ChronoAIProject/chrono-harness/blob/v0.1.4-dev.43348924098.1.g1ca9aa00be1147202d1cf3935ced4ba186eb3bba/docs/worktree.md)。

## 验收边界

安装工具不启用完整治理，也不证明完整外部输入、跨平台同判或全部 SPEC。当前共享治理登记仍为 proposed。此次升级的实际范围以本仓 PR、dev 落地运行与安装原回执为准，不能凭本文宣称迁移完成。升级和失败恢复沿用本轮固定发布的[安装与升级合同](https://github.com/ChronoAIProject/chrono-harness/blob/v0.1.4-dev.43348924098.1.g1ca9aa00be1147202d1cf3935ced4ba186eb3bba/docs/distribution.md)。
