# Trust My Bot

**Multi-agent engineering workflow. Replace hallucination with discipline.**

Stop single-agent chaos. TMB runs your project like a real engineering team:
a planner who scopes, an executor who builds, and an independent reviewer
who catches what you'd miss.

---

## 🌐 [trustmybot/plugin](https://github.com/trustmybot/plugin) — Claude Code, MIT, free forever

The shipped product. Drop-in multi-agent workflow for any Claude Code project.

- **bro** — single Human entry point + planner. Discusses, designs, writes task specs, verifies SWE's work, closes tasks atomically. Never edits source.
- **swe** — executor. One task per spawn, isolated git worktree, atomic close. Cannot self-approve.
- **pr-reviewer** — independent 3rd party. Reviews diffs at push time. Read-only on files.

Plus: SQLite trajectory memory (resume across sessions, no codebase-rediscovery tax), hard-enforcement hooks (no prompt-discipline ceiling), 6-layer enforcement model from server-side middleware down to prompts. Detailed [agent contract](https://github.com/trustmybot/plugin/blob/main/docs/architecture/RESPONSIBILITIES.md) and [enforcement matrix](https://github.com/trustmybot/plugin/blob/main/docs/architecture/ENFORCEMENT.md).

```
/plugin marketplace add trustmybot/plugin
/plugin install tmb@trustmybot
```

**MIT-licensed, free forever. This will not change.** Community PRs welcome.

---

## 💼 TMB Enterprise — *in development, not yet shipped*

A commercial tier for teams whose needs an MIT plugin alone can't promise.

Planned features:

- 🧠 **Hosted trajectory memory** — cross-session, cross-agent, cross-team
- 📊 **Audit store** — queryable history of every decision, with retention + export
- 🔒 **Hard permission isolation** — beyond what hooks can enforce
- 🌍 **Cross-provider** — OpenAI, Gemini, Groq, Mistral, DeepSeek, local models
- 🏢 **Team features** — SSO, audit export, dashboard, priority support

**Boundary commitment:** Enterprise will never gate features that make the plugin work standalone. The plugin is the open core; Enterprise adds infrastructure for teams.

If your team needs these and you'd like to influence what gets built first, [open an issue](https://github.com/trustmybot/plugin/issues/new) or reach out to [@ZaxShen](https://github.com/ZaxShen).

---

## Which should I use?

| You are... | Use |
|---|---|
| A Claude Code user exploring multi-agent workflows | **Plugin** — available now |
| A solo dev shipping side projects | **Plugin** — available now |
| A team needing hosted audit, cross-provider LLM, or SSO | **Enterprise** — express interest while we build |
| A company with SOC2 / compliance requirements | **Enterprise** — express interest while we build |

---

Built by [@ZaxShen](https://github.com/ZaxShen).
