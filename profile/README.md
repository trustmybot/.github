# TrustMyBot (TMB)

**Trust me bro, it works.** TrustMyBot is a free, MIT-licensed multi-agent harness for Claude Code: one agent plans, one builds, and a separate reviewer signs off before anything is pushed.

<p align="center">
  <img src="https://raw.githubusercontent.com/trustmybot/plugin/dev/docs/assets/tmb-hero.svg" width="640" alt="Animated pixel-art story. Coding agents call broken work done, forget everything, drift off task, need babysitting and touch files they shouldn't. With TrustMyBot, bro plans from a saved memory, swe agents build, and pr-reviewer rejects failures and gates every push to GitHub.">
</p>

## Install

Requires Claude Code 2.1.295 or later (`claude --version`).

```
/plugin marketplace add trustmybot/marketplace
/plugin install tmb@trustmybot
```

Then ask: `@bro write a todo cli`

## What you get

- **bro** plans and gates. Your one point of contact. Never edits source.
- **swe** builds one task at a time in its own isolated copy of the repo. Never approves its own work.
- **pr-reviewer** reviews independently. `git push` stays blocked until it signs off.
- **Memory that survives restarts.** Plans, decisions and review verdicts are saved in your project, so bro picks up where it left off.
- **Guardrails in code, not in the prompt.** swe can't write outside its own copy, and force-pushes to protected branches are blocked.

Source, docs and changelog: **[trustmybot/plugin](https://github.com/trustmybot/plugin)**. MIT, free forever. This will not change.

## TMB Enterprise (in development, not shipped)

For teams that need more than a local plugin can promise. Planned: hosted shared memory, a queryable audit store with retention and export, SSO and a team dashboard, and support for more model providers.

**Boundary commitment:** Enterprise will never gate features that make the plugin work standalone. The plugin is the open core; Enterprise adds infrastructure for teams.

Want a say in what gets built first? [Open an issue](https://github.com/trustmybot/plugin/issues/new) or reach [@ZaxShen](https://github.com/ZaxShen).

## Which should I use?

| You are... | Use |
|---|---|
| A Claude Code user, solo or on a team, shipping real code | **Plugin**, available now |
| A team needing hosted audit, SSO or other model providers | **Enterprise**, register interest while we build |
| A company with SOC 2 or compliance requirements | **Enterprise**, register interest while we build |

<!-- PENDING GO-LIVE: uncomment once https://trustmybot.org resolves -->
<!-- **Website:** [trustmybot.org](https://trustmybot.org) -->

Built by [@ZaxShen](https://github.com/ZaxShen).
