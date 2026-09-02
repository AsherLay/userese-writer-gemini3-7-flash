# Userese Writer · Gemini 3.7 Flash

只负责怎么写。受众、事实、范围和结构由 [Userese](https://github.com/AsherLay/userese) 先确认。

当前版本：v0.1.0

更适合英文稿。通过 OpenRouter 调用 `google/gemini-3.7-flash`，产出可以逐条核对的 before/after 提案。不重新决定这是写给谁的，不编事实，不改产品文件。

没有经过确认的 `userese-brief/v1`，不要用它来直接改网站文案。它不会被 Userese 自动发现或自动选中；你必须在对话里写出全名。

## 安装

Python 3.10+。把仓库克隆到 Agent 会扫描的 skills 目录。

```bash
# Codex / Claude Code
git clone https://github.com/AsherLay/userese-writer-gemini3-7-flash.git ~/.agents/skills/userese-writer-gemini3-7-flash

# Cursor
git clone https://github.com/AsherLay/userese-writer-gemini3-7-flash.git ~/.cursor/skills/userese-writer-gemini3-7-flash
```

设置 `OPENROUTER_API_KEY`。已经把 OpenRouter 密钥放在 Claude Code 的 `ANTHROPIC_AUTH_TOKEN` 里时，也可以直接用那个。密钥只从当前环境或 `~/.claude/settings.json` 的 `env` 读取，不会写进项目、批次或报告。

对话里这样启动：

```text
使用 $userese-writer-gemini3-7-flash 处理这个已经确认的 Userese brief，只生成提案。
```

首次产生费用前，会说明模型、文案项数和预计批次数。默认 reasoning effort 为 `low`。

完整约束见 [`SKILL.md`](SKILL.md)。另一个可选 Writer：[userese-writer-qwen3-8-flash](https://github.com/AsherLay/userese-writer-qwen3-8-flash)。

## English

This writer only writes. [Userese](https://github.com/AsherLay/userese) already confirmed the reader, facts, scope, and structure.

Current version: v0.1.0

It is a better fit for English copy. It calls OpenRouter (`google/gemini-3.7-flash`) and returns before/after proposals you can check. It does not choose who the copy is for, invent facts, or edit product files.

Do not use it to rewrite a site without a confirmed `userese-brief/v1`. Userese will not auto-detect or auto-select it. You have to type the full name.

### Install

Python 3.10+. Clone into the skills directory your agent scans.

```bash
# Codex / Claude Code
git clone https://github.com/AsherLay/userese-writer-gemini3-7-flash.git ~/.agents/skills/userese-writer-gemini3-7-flash

# Cursor
git clone https://github.com/AsherLay/userese-writer-gemini3-7-flash.git ~/.cursor/skills/userese-writer-gemini3-7-flash
```

Set `OPENROUTER_API_KEY`. If you already keep an OpenRouter key in Claude Code as `ANTHROPIC_AUTH_TOKEN`, that still works. The key is read from the process environment, or from `env` in `~/.claude/settings.json`. It is not written into the project, batches, or reports.

Start with:

```text
Use $userese-writer-gemini3-7-flash on this confirmed Userese brief. Generate proposals only.
```

Before the first paid call, it states the model, item count, and expected batch count. Reasoning effort defaults to `low`.

See [`SKILL.md`](SKILL.md) for the full contract. The other optional writer is [userese-writer-qwen3-8-flash](https://github.com/AsherLay/userese-writer-qwen3-8-flash).

## License

[MIT](LICENSE)。版权人 `AsherLay`，2026。
