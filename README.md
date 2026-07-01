# Rick Rubin

<p align="center">
  <img src="./skills/rick-rubin/assets/rick-rubin-intuition.png" alt="Rick Rubin with text about making software from intuition and taste" width="720">
</p>

Most AI work is not bad.

It is worse.

It is fine.

It passes. It compiles. It satisfies the prompt. It explains itself too much. It has no pulse.

This is a final listen before shipping.

Not a spec check.

A taste check.

> Is this alive, or merely correct?

## Use It

Install as an Agent Skill:

```bash
npx skills add vinny380/rick-ruibin-skill --skill rick-rubin
```

Install with GitHub CLI:

```bash
gh skill install vinny380/rick-ruibin-skill
```

Install as a Codex plugin:

```bash
codex plugin marketplace add vinny380/rick-ruibin-skill
codex plugin add taste-check@rick-rubin-skills
```

Install as a Claude Code marketplace plugin:

```text
/plugin marketplace add vinny380/rick-ruibin-skill
/plugin install taste-check@rick-rubin-skills
```

Use it:

```text
Claude direct skill install: /rick-rubin judge this landing page copy.
Claude marketplace install: /taste-check:rick-rubin judge this landing page copy.
Codex: Use $rick-rubin to judge this landing page copy.
```

For local plugin development:

```bash
claude --plugin-dir .
```

## Marketplace Shape

This repo is arranged for three paths with one canonical skill file:

- `skills/rick-rubin/SKILL.md` for skills.sh and direct Agent Skills installs
- `.claude-plugin/marketplace.json` plus `.claude-plugin/plugin.json` for Claude Code marketplace distribution
- `.agents/plugins/marketplace.json` plus `.codex-plugin/plugin.json` for Codex plugin marketplace distribution

Claude and Codex install the repo root as the `taste-check` plugin package. The skill itself lives once, under `skills/rick-rubin/`.

## Published Status

Published release:

```text
v1.0.1
https://github.com/vinny380/rick-ruibin-skill/releases/tag/v1.0.1
```

This is installable today through:

- GitHub Agent Skills: `gh skill install vinny380/rick-ruibin-skill`
- skills.sh / open Agent Skills: `npx skills add vinny380/rick-ruibin-skill --skill rick-rubin`
- Codex self-hosted marketplace: `taste-check@rick-rubin-skills`
- Claude Code self-hosted marketplace: `taste-check@rick-rubin-skills`

This is not yet listed in the curated/global Claude or Codex directories. Those are separate curation surfaces. For Claude's community marketplace, submit the plugin here:

```text
https://platform.claude.com/plugins/submit
```

## The Point

Use `/rick-rubin` in Claude Code, or `$rick-rubin` in Codex, when the work needs judgment.

Not more features.

Not more polish.

Judgment.

- Is the interface pulling you in?
- Is the copy saying one true thing?
- Is the code simple because it found its shape, or simple because it gave up?
- Is the feature real, or did it grow extra limbs in a meeting?
- Is the name memorable, or just available?

The skill looks at the thing itself.

It ignores the pitch.

It removes what does not belong.

It says the quiet part plainly.

## The Output

```text
Verdict: alive, flat, overbuilt, or close
Essence: what the work is really trying to be
Cut: what should be removed
One change: the highest-leverage improvement
```

That is enough.

More would be decoration.

## What This Is Not

This is not an impersonation.

No guru voice.

No costume.

No incense in the terminal.

The skill does not talk like anyone. It decides with taste.

The goal is not to sound interesting.

The goal is to make the work better.

## Example

```text
User:
Judge this feature idea:

"AI dashboard with insights, tasks, team updates, automations, integrations,
and weekly strategic recommendations."

/rick-rubin:
Verdict: overbuilt. It sounds useful, but I already want to close it.

Essence: the real product is "tell me what changed and what needs me."

Cut: dashboards, weekly strategy, vague insights, generic automations.

One change: make the first version a daily operator brief:
5 changes, 3 risks, 1 thing to do now.
```

More demos live in [examples](./examples).

## Distribution Notes

For the shorter Claude command:

```bash
npx skills add vinny380/rick-ruibin-skill -a claude-code --skill rick-rubin
```

Then invoke:

```text
/rick-rubin
```

For Claude marketplace installs, plugin skills are namespaced by design:

```text
/taste-check:rick-rubin
```

For Codex marketplace installs:

```text
$rick-rubin
```

skills.sh and GitHub skill search may take time to index new public releases. Direct install works immediately.

## Launch Copy

Post this:

```text
I made a Codex/Claude skill for taste.

Most AI work does not fail because it is wrong.
It fails because it is competent-but-dead.

This skill gives the work a final listen:

Verdict.
Essence.
Cut.
One change.

Correct is the floor.
Alive is the bar.
```

Follow-up:

```text
The best AI reviewer may not ask:
"does this satisfy the prompt?"

It asks:
"do I want to keep looking at this?"

That changes the work.
```

## Files

- `skills/rick-rubin/SKILL.md` - the skill
- `skills/rick-rubin/agents/openai.yaml` - Codex skill metadata
- `skills.sh.json` - skills.sh repo page grouping
- `.claude-plugin/marketplace.json` - Claude marketplace catalog
- `.claude-plugin/plugin.json` - Claude plugin manifest
- `.agents/plugins/marketplace.json` - Codex marketplace catalog
- `.codex-plugin/plugin.json` - Codex plugin manifest
- `examples/` - before/after demos for launch posts and validation
- `skills/rick-rubin/assets/rick-rubin-intuition.png` - README and skill image

## License

MIT
